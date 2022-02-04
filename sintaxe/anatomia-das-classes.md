---
description: Uma classe bem estruturada não quer guerra com ninguém
---

# Anatomia das classes

A escrita de códigos de um programa é a composição de palavras pré definidas pela linguagem mais as expressões que utilizamos para determinar o nome do nossos arquivos, classes, atributos e métodos.&#x20;

É muito comum mesclarmos expressões no idioma americano com os nosso vocabulário, existem projetos que recomendam que toda a implementação do seu programa seja escrita na língua inglesa.

![](<../.gitbook/assets/image (8).png>)

* 99,9% das nossas classes iniciarão com `public class;`
* Toda classe precisa de nome, exemplo `MinhaClasse;`
* O nome do arquivo deve idêntico ao nome da classe publica;
* Após o nome definir o corpo `{ }` aonde iremos compor nossas classes com atributos e métodos.

![](<../.gitbook/assets/image (12).png>)

* É de suma importância que agora você consiga se localizar dentro do conjunto de chaves `{ }` existentes em sua classe.
* &#x20;Dentro de uma aplicação recomenda-se que somente uma classe possua o método `main`, responsável por iniciar todo o nosso programa.
* O método main recebe seu nome `main`, sempre terá a visibilidade `public`, será difinido como `static`, não retornará nenhum valor com `void` e receberá um parâmetro do tipo array de caracteres `String[]`.

## Padrão de nomenclatura

Quando se trata de escrever códigos na linguagem Java é recomendado seguir algumas convenções de escrita diante dos itens abaixo:

*   **Arquivo .java**:  Todo arquivo .java deve começar com letra MAIÚSCULA e se palavra for composta, a segunda palavra deve também ser maiúscula, exemplo:&#x20;

    `Calculadora.java`, `CalculadoraCientifica.java`
* **Nome da classe no arquivo**: A classe deve possuir o mesmo nome do arquivo.java, exemplo:

```
// arquivo CalculadoraCientifica.java

public class CalculadoraCientifica {

}
```

* **Nome de variável**: toda variável deve ser escrita com letra minúscula, porém se a palavra for composta, a primeira letra da segunda palavra deverá ser MAIÚSCULA, exemplo:                 `ano` e `ano`**`F`**`abricacao.`

{% hint style="info" %}
Existe uma regra adicional para variáveis quando na mesma queremos identificar que ela não sofrerá alteração de valor, exemplo: queremos determinar que uma variável de nome **br** sempre representará **"Brasil"** e nunca mudará seu valor, logo, determinamos como escrita o código abaixo:
{% endhint %}

```
String BR = "Brasil"
double PI = 3.14
int ESTADOS_BRASILEIRO = 27
int ANO_2000 = 2000
```

{% hint style="danger" %}
Recomendações: Para declarar uma variável nós podemos utilizar caracteres, números e símbolos, porém devemos seguir algumas regras da linguagem.
{% endhint %}

* Deve conter apenas letras, \_ (underline), $ ou os números de 0 a 9
* Deve obrigatoriamente se iniciar por uma letra (preferencialmente), \_ ou $
* Deve iniciar com uma letra minúscula (boa prática – ver abaixo)
* Não pode conter espaços
* Não podemos usar palavras-chave da linguagem
* O nome deve ser único dentro de um escopo

```
// Declação inválida de variáveis

int numero&um = 1; //Os únicos símbolos permitidos são _ e $
int 1numero = 1;    //Uma variável não pode começar com númerico
int numero um = 1; //Não pode ter espaço no nome da variável
int long = 1; //long faz parte das palavras reservadas da linguagem
 
 // Declaração válida de veriáveis
int numero$um = 1;
int numero1 = 1;
int numeroum = 1;
int longo = 1;
		

```

## Declarando variáveis e métodos

Como identificar que entre declaração de variáveis e métodos em nossa programa? Existe uma estrutura comum para ambas as finalidades, exemplo:

* Declarar uma variável em Java é sempre a seguinte estrutura

```
// Estrutura

Tipo NomeBemDefinido = Atribuição (opcional em alguns casos)

// Exemplo

int idade = 23;
double altura = 1.62;
Dog spike; //observe que aqui a variável spike não tem valor, é normal
```

* Declarando métodos em Java segue uma estrutura bem simples:

```
// Estrutura

TipoRetorno NomeObjetivoNoInfinitivo Parametro(s)

//Exemplo

int somar (int numeroUm, int numero2)

String formatarCep (long cep)
```

{% hint style="warning" %}
Como parte da estrutura de declaração de variáveis e métodos também temos o aspecto da **visibilidade**, mas ainda não é necessário nesta etapa de estudos.
{% endhint %}

## Identação

Basicamente **indentar** é um termo utilizado para escrever o código do programa de forma hierárquica, facilitando assim a visualização e o entendimento do programa.

![](<../.gitbook/assets/image (5).png>)

Abaixo veja um exemplo de um algoritmo de validação de aprovação de estudante de forma sem e com identação:

{% tabs %}
{% tab title="Sem Identação" %}
```java
// arquivo BoletimEstudantil.java

public class BoletimEstudantil {
public static void main(String[] args) {
int mediaFinal = 6;
if(mediaFinal<6)	
System.out.println("REPROVADO"); 
else if(mediaFinal==6)
System.out.println("PROVA MINERVA"); 
else
System.out.println("APROVADO"); 		
}
}
```
{% endtab %}

{% tab title="Com Identação" %}
```java
public class BoletimEstudantil {
	public static void main(String[] args) {
		int mediaFinal = 6;
		if (mediaFinal < 6)
			System.out.println("REPROVADO");
		else if (mediaFinal == 6)
			System.out.println("PROVA MINERVA");
		else
			System.out.println("APROVADO");
	}
}
```
{% endtab %}
{% endtabs %}

## Organizando nossos arquivos

À medida que nosso sistema vai sendo evoluído, surgem novos arquivos (código fonte) em nossa estrutura de arquivos do projeto. Isso exige que seja realizado uma organização destes arquivos através de pacotes (packages).

![Ilustração de uso de pacotes](<../.gitbook/assets/image (2).png>)

Com o uso de pacotes as nossas classes (.java) passa é possuir duas identificação, o nome simples e nome qualificado:

* **Nome Simples**: Nome do arquivo, exemplo `ContaBanco`.
* **Nome Qualificado**: Nome do pacote + nome do arquivo, exemplo: `com.suaempresa.ContaBanco`.&#x20;
