1. Faça uma Trigger que registre no Log o nome do professor excluído
2. Crie uma tabela de produtos com estoque, e outra para lançamentos de saída (venda).
3. Ao inserir uma saída, faça uma Trigger para validar se existe estoque suficiente para executar a operação, caso tenha, atualize o estoque.

-- =========================================
-- LIMPEZA (caso já exista)
-- =========================================
IF OBJECT_ID('trg_validar_estoque', 'TR') IS NOT NULL
	DROP TRIGGER trg_validar_estoque;

IF OBJECT_ID('vendas', 'U') IS NOT NULL
	DROP TABLE vendas;

IF OBJECT_ID('produtos', 'U') IS NOT NULL
	DROP TABLE produtos;

GO

-- =========================================
-- TABELA DE PRODUTOS
-- =========================================
CREATE TABLE produtos
(
	id INT IDENTITY(1,1) PRIMARY KEY,
	nome VARCHAR(100) NOT NULL,
	estoque INT NOT NULL CHECK (estoque >= 0),
	preco DECIMAL(10,2) NOT NULL
);

-- =========================================
-- TABELA DE VENDAS (SAÍDA)
-- =========================================
CREATE TABLE vendas
(
	id INT IDENTITY(1,1) PRIMARY KEY,
	id_produto INT NOT NULL,
	quantidade INT NOT NULL CHECK (quantidade > 0),
	data_venda DATETIME NOT NULL DEFAULT GETDATE(),

	FOREIGN KEY (id_produto) REFERENCES produtos(id)
);

GO

-- =========================================
-- TRIGGER: VALIDA E ATUALIZA ESTOQUE
-- =========================================
CREATE TRIGGER trg_validar_estoque
ON vendas
AFTER INSERT
AS
BEGIN
	SET NOCOUNT ON;

	-- Verifica se há estoque suficiente
	IF EXISTS (
		SELECT 1
		FROM inserted i
		JOIN produtos p ON p.id = i.id_produto
		WHERE p.estoque < i.quantidade
	)
	BEGIN
		RAISERROR('Estoque insuficiente para realizar a venda.', 16, 1);
		ROLLBACK TRANSACTION;
		RETURN;
	END

	-- Atualiza o estoque
	UPDATE p
	SET p.estoque = p.estoque - i.quantidade
	FROM produtos p
	JOIN inserted i ON p.id = i.id_produto;
END;
GO

-- =========================================
-- TESTE
-- =========================================

-- Inserindo produto
INSERT INTO produtos (nome, estoque, preco)
VALUES ('Notebook', 10, 3500.00);

-- Venda válida
INSERT INTO vendas (id_produto, quantidade)
VALUES (1, 3);

-- Venda inválida (estoque insuficiente)
INSERT INTO vendas (id_produto, quantidade)
VALUES (1, 20);

-- Verificar resultado
SELECT * FROM produtos;
SELECT * FROM vendas;