### Classe Array List
ArrayList é uma classe do Java (`java.util.ArrayList`) que implementa uma lista redimensionável, permitindo adicionar, remover e manipular elementos dinamicamente, diferente dos arrays tradicionais de tamanho fixo. Ele é parte do _Collection Framework_, armazena objetos, aceita valores `null` e permite acesso rápido via índices.

Permite a instanciação de objetos cujo o propósito é realizar o agrupamento dinâmico de objetos de uma mesma classe.

Exemplo: 

	ArrayList<Funcionario>funcionarios = new ArrayList<Funcionarios>();

### Interação
```
1. funcionarios.add(f); = Insere o objeto no ArrayList.
```
```
2. funcionarios.size(); = Devolve a quantidade de objetos agrupados no ArrayList.
```
```
3. funcionarios.get(x); = Acessa um objeto no ArrayList a partir de um índice sequencial. Onde: 0 <= x <size();
```

#### Exemplo

```
import java.util.ArrayList; 
public class Exemplo { public static void main(String[] args) { 
ArrayList<String> nomes = new ArrayList<>(); 
nomes.add("Ana"); 
nomes.add("Bruno"); 
System.out.println(nomes.get(0)); // Saída: Ana nomes.remove(1); // Remove Bruno } }
```