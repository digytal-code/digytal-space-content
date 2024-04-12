---
description: A classe mais utilizada, na linguagem Java.
---

# A poderosa String

Que a linguagem é composta por inúmeras classes, isso nós sabemos, mas precisamos dominar cada uma delas, de forma que nos deixe familiarizado, com todo o poder em se utilizar Java.

Abaixo, vamos explorar um pouco mais a String, umas das classes mais poderosas da linguagem. Recomendamos que este exercício, seja realizado com o máximo de classes e cenários possíveis, para aprimorar suas habilidades como desenvolvedor.

1. Primeiramente precisamos estar familiarizado, com a documentação, veja a classe [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html);
2. Mapeie os métodos, mais comuns e mais utilizados;
3. Testes, documentação no github, testes documentação no github.

Abaixo, vamos explorar alguns dos recursos da classe String.

**Criando uma variável e atribuindo valores:**

```java
//usando do new
String cidade = new String("SAO PAULO");

//forma literal
String pais = "BRAZIL"; 

//retorno de métodos
Integer numero = 123;
String textoNumero = numero.toString();
		
```

#### Concatenação

```java
String nome = "GLEYSON";
String sobrenome="SAMPAIO";

String nomeCompleto = nome + " " + sobrenome;

System.out.println(nomeCompleto);

//Ver versão do Java
nomeCompleto = nome.concat(" ").concat(sobrenome);

System.out.println(nomeCompleto);
```

#### Alterando estado

```
String nomeCompleto = "Gleyson Sampaio";
System.out.println(nomeCompleto);

String nomeMaiusculo = nomeCompleto.toUpperCase();
System.out.println(nomeMaiusculo);

String nomeMinusculo = nomeCompleto.toLowerCase();
System.out.println(nomeMinusculo);

```

#### Quebrando um texto String

Existem duas maneiras de se dividir um texto, utilizando String, um é o padrão delimitado, onde você determina um delimitador: "\[" , ";" , "|"  espaço e etc. Ou o padrão posicional pegando uma parte do texto, pelo intervalo definido entre, início e fim.

```java
//uso do delimitador ;
String padraoCsv = "GLEYSON SAMPAIO;gleyson@digytal.com.br;INSTRUTOR JAVA";
String dadosCadastro [] = padraoCsv.split(";");
System.out.println("Nome: " + dadosCadastro [0]);
System.out.println("Email: " + dadosCadastro [1]);
System.out.println("Profissao: " + dadosCadastro [2]);


//padrão posicional ;
String dadosPagamento = "00861027202110070000029100";
System.out.println("Agencia:" + dadosPagamento.substring(0,4) );
System.out.println("Conta:" + dadosPagamento.substring(4,8) );
System.out.println("Data:" + dadosPagamento.substring(8,16) );
System.out.println("Data:" + dadosPagamento.substring(16,26) );
```

**Exercício**

1. Apresente mais 2 ou 3 métodos essenciais, da classe String;
2. Implemente um algoritmo conforme especificação abaixo:

Abaixo temos um texto, que representa um cupom de uma lanchonete, que foi solicitada a localização e impressão dos campos, conforme textos abaixo:

```
Layout 1: Data;NumeroPedido;Valor;Cep;Numero
Texto  1: 20211008;0000787;001999;65300000;352

Layout 2: Id Item(4), Descricao(20), Quant(2), R$ Unit(4), R$ Total(4)
Texto  2: 0037MASTER DOG          0307002100 
```
