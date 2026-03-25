### Como criar um ponteiro?
Para criarmos um ponteiro em **Java**, é necessário criar uma classe principal e utilizar o código:
O ponteiro nesse caso é o "**objRet**".

`public class Aplic {`

    `public static void main(String[] args) {`
        `//definicao de um ponteiro para um objeto`
        `Retangulo objRet;`
        
        `//instanciação(alocação) de um objeto da classe retangulo.`
        `objRet = new Retangulo();`
        
        `//passagem de mensagem`
        `objRet.setAltura(5.0);`
        `objRet.setBase(8.0);`
        
        `System.out.println("Medida da area do retangulo: " + objRet.calcArea());`
        `System.out.println("Medida do Perimetro do retangulo: " + objRet.caclPerimetro());`
    `}`
    
`}`

Assim como nesse exemplo abaixo.
Nesse caso, o **ponteiro** é o "**entrada**". Posteriormente foi selecionado o nextDouble().

![[Pasted image 20260311102514.png|697]]
