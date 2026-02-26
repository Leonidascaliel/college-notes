## O que é uma trigger no SQL?

Uma **trigger** é um bloco de código que executa **automaticamente** quando ocorre um evento em uma tabela ou view.

Ela é disparada por operações como:
- `INSERT`
- `UPDATE`
- `DELETE`

Ou seja, diferente de uma procedure, você **não chama a trigger manualmente**. O próprio banco executa.
#### Exemplo:
A estrutura do **Trigger** será sempre assim, a unica coisa que muda é o seu "Miolo" do **Begin** até **End**.

	CREATE TRIGGER exemplo
	ON clientes
	AFTER INSERT
	AS
	BEGIN
	PRINT('Novo cliente cadastrado!');
	END;