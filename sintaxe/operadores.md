---
description: >-
  Símbolos especiais que tem um significado próprio para a linguagem e estão
  associados a determinadas operações.
---

# Operadores

Geralmente as primeiras palavras que ouvimos em um curso de programação são: um programa é um conjunto de instruções lógicas que, quando executadas, produzem algum resultado. Com isso em mente, ao começar a criar as primeiras linhas de código, logo você notará que é comum receber dados do usuário, prover alguma lógica para processá-los e então apresentar o resultado desse processamento.

![](<../.gitbook/assets/image (12).png>)

## Classificação do operadores

### Atribuição

O operador de atribuição é utilizado para definir o valor inicial ou sobrescrever o valor de uma variável onde em Java definimos um tipo, nome e opcionalmente atribuímos um valor à variável.

```java
//classe Operadores.java
String nome = "GLEYSON";
int idade = 22;
double peso = 68.5;
char sexo = 'M';
boolean doadorOrgao = false;
Date dataNascimento = new Date();
```

### Aritméticos

O operador aritmético é utilizado para realizar operações matemáticas em entre valores numéricos, podendo se tornar ou não uma expressão mais complexa.

```java
//classe Operadores.java
double soma = 10.5 + 15.7;
int subtração = 113 - 25;
int multiplicacao = 20 * 7;
int divisao = 15 / 3;
double resultado = (10 * 7) + (20/4);
```

{% hint style="warning" %}
O operador de soma (+) em variáveis do tipo texto, realizar a “concatenação de textos”.
{% endhint %}

```java
//classe Operadores.java
String nomeCompleto = "LINGUAGEM" + "JAVA";
		
//qual o resultado das expressoes abaixo?
String concatenacao ="?"; 

concatenacao = 1+1+1+"1";

concatenacao = 1+"1"+1+1;

concatenacao = 1+"1"+1+"1";

concatenacao = "1"+1+1+1;

concatenacao = "1"+(1+1+1);
```

### Unário

Esses operadores são aplicados especificamente sobre um operador. Eles realizam alguns trabalhos básicos como incremental, decremental e inversão de valores numéricos e booleanos.

* (+) Operador unário de valor positivo – números são positivos sem esse operador explicitamente;
* (-) Operador unário de valor negativo – nega um número ou expressão aritmética;
* (++) Operador unário de incremento de valor – incrementa o valor em 1 unidade;
* (--) Operador unário de decremento de valor – decrementa o valor em 1 unidade;
* (!) Operador unário lógico de negação – nega o valor de uma expressão booleana;

```java
//classe Operadores.java
int numero = 5;
		
//Imprimindo o numero negativo
System.out.println(- numero);

//incrementando numero em mais 1 numero, imprime 6
numero ++;
System.out.println(numero);

//incrementando numero em mais 1 numero, imprime 7
System.out.println(numero ++);// ops algo de errado não está certo

System.out.println(numero);// agora sim, numero virou 7

//ordem de precedencia conta aqui
System.out.println(++ numero);

boolean verdadeiro = true;

System.out.println("Inverteu " + !verdadeiro);
```

{% hint style="danger" %}
Muito cuidado com ordem de precedência dos operadores unários
{% endhint %}

### Relacionais

Os operadores relacionais, assim como os de igualdade, avaliam dois operandos. Neste caso, mais precisamente, definem se o operando à esquerda é igual, diferente, menor, menor ou igual, maior ou maior ou igual ao da direita, retornando um valor booleano.

* \== Quando desejamos verificar se uma variável é igual que outra.
* != Quando desejamos verificar se uma variável é igual que outra.
* \> Quando desejamos verificar se uma variável é maior que outra.
* \>= Quando desejamos verificar se uma variável é maior ou igual a outra
* < Quando desejamos verificar se uma variável é menor que outra.
* <= Quando desejamos verificar se uma variável é menor ou igual a outra.

```java
//classe Operadores.java
int numero1 = 1;
int numero2 = 2;

if(numero1 > numero2)
	System.out.print("Numero 1 maior que numero 2");

if(numero1 < numero2)
	System.out.print("Numero 1 menor que numero 2");

if(numero1 >= numero2)
	System.out.print("Numero 1 maior ou igual que numero 2");

if(numero1 <= numero2)
	System.out.print("Numero 1 menor ou igual que numero 2");

if(numero1 != numero2)
	System.out.print("Numero 1 é diferente de numero 2");jav
```

#### Comparações avançadas

Quando se refere a comparação de conteúdos na linguagem devemos ter um certo domínio de como o Java trata o armazenamento deste valores na memória.

{% hint style="success" %}
Quando estiver mais familiarizado com linguagem, recomendamos se aprofundar no conceito, espaço em memória **Stack** versus **Heap**.
{% endhint %}

Vamos a alguns exemplos para ilustrar:

**== versus equals:** Existe uma relevância forte em realizar comparações com **==** e **equals** na qual precisamos ter uma compreensão de quais as regras seguidas pela linguagem **** , exemplo:

```
// ComparacaoAvancada.java

 public static void main(String[] args) {
        
        int numero1 = 130;
        int numero2 = 130;
        System.out.println(numero1 == numero2); //true
        
        Integer numero1 = 130;
        Integer numero2 = 130;

        System.out.println(numero1 == numero2); //false
        
        // A razão pela qual o resultado é false, é devido o Java tratar os valores
        // Como objetos a partir de agora.
        // Qual a solução ?
        // Quando queremos comparar objetos, usamos o método equals
        
         System.out.println(numero1.equals(numero2)); 
 }
```









### Lógicos

Os operadores lógicos representam o recurso que nos permite criar expressões lógicas maiores a partir da junção de duas ou mais expressões. Para isso, aplicamos as operações lógicas E (representado por “&&”) e OU (representado por “||”).

```java
// classe Operadores.java
boolean condicao1=true;

boolean condicao2=false;

if(condicao1 && condicao2)
	System.out.print("Os dois valores precisam ser verdadeiros");;

if(condicao1 || condicao2)
	System.out.print("Um dos valores precisa ser verdadeiro");
```

#### Expressões lógicas avançadas

### Ternário

Condição ternária é uma forma resumida para definir uma condição e escolher por um dentre dois valores. Você deve pensar numa condição ternária como se fosse uma condição IF normal, porém, de uma forma em que toda a sua estrutura estará escrita numa única linha.

```java
// classe Operadores.java
int a, b;

a = 5;
b = 6;

/*
if(a==b)
   resultado = "verdadeiro";
else
   resultado = "falso";
*/

String resultado = (a==b) ? "verdadeiro" : "false";

System.out.println(valor);
```

{% hint style="info" %}
O operador ternário considera qualquer tipo de valor como resposta.
{% endhint %}



