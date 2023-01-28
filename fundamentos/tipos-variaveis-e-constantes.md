# Tipos, variáveis e constantes

## Tipos de dados

No Java, existem algumas palavras reservadas, para a representação dos tipos de dados básicos, que precisam ser manipulados para a construção de programas. Estes tipos de dados são conhecidos como tipos primitivos.



| Tipo  | Memória | Valor Mínimo               | Valor Máximo              |
| ----- | ------- | -------------------------- | ------------------------- |
| byte  | 1 byte  | -128                       | 127                       |
| short | 2 byte  | -32.768                    | 32.767                    |
| int   | 4 bytes | -2.147.483.648             | 2.147.483.647             |
| long  | 8 bytes | -9.223.372.036.854.775.808 | 9.223.372.036.854.775.807 |

Números que podem conter partes fracionárias, podem ser representados por dois tipos:



| Tipo   | Memória | Mínimo         | Máximo        | Precisão      |
| ------ | ------- | -------------- | ------------- | ------------- |
| float  | 4 bytes | -3,4028E + 38  | 3,4028E + 38  | 6 – 7 dígitos |
| double | 8 bytes | -1,7976E + 308 | 1,7976E + 308 | 15 dígitos    |

_Apesar de o tipo float ocupar metade da memória, consumida por um tipo double, ele é menos utilizado. Ele sofre de uma limitação, que compromete seu uso, em determinadas situações: somente mantém uma precisão decimal entre 6 e 7 dígitos._

{% hint style="info" %}
_O ponto mais relevante, em compreender a definição dos tipos de dados é o momento da definição do tipo, para uma variável. **Qual tipo de dados, eu utilizaria para determinar a idade de uma pessoa ou o salário de um funcionário ?**_
{% endhint %}

O padrão para se declarar uma variável sempre é: tipo + nome + atribuição de valor (opcional):

```java
int idade;
int anoFabricacao = 2021;
int x = 0;
```

```java
public class TipoDados {
	public static void main(String[] args) {
		byte idade = 123;
		short ano = 2021;
		int cep = 21070333; // se começar com zero, talvez tenha que ser outro tipo
		long cpf = 98765432109L; // se começar com zero, talvez tenha que ser outro tipo
		float pi = 3.14F;
		double salario = 1275.33;
	}
}
```

{% hint style="warning" %}
Observe que, o tipo long precisa terminar com L, o tipo float precisa terminar com F e alguns cenários do dia-a-dia podem estimular uma alteração de tipos de dados convencional.
{% endhint %}

## Variáveis e Constantes

Na programação, uma **variável** é uma palavra (_geralmente abreviada, mas não recomendado_) que representa um valor arbitrário, não totalmente especificado, ou desconhecido.

No Java, utilizamos identificadores que representam uma referência (ponteiro) a um valor em memória, e esta referência pode ser redirecionada a outro valor e assim por diante, por isso,  chamamos este identificador de variável, pois pode alterar o seu valor.

Abaixo, temos um exemplo explicativo sobre uso de variáveis e constantes:

```java
public class ExemploVariavel {
	public static void main(String[] args) {
		/*
		 * esta linha é considerada como declaração de variável iniciamos a existência
		 * variavel numero com valor 5 regra: tipo + nome + valor
		 */
		int numero = 5;

		/*
		 * na linha abaixo iremos alterar o valor do varíavel para 10 observe que o tipo
		 * não é mais necessário, pois a variável já foi declarada anteriormente
		 */
		numero = 10;

		System.out.print(numero);
		
		/*
		 * ao usar a palavra reservada final, você determina que jamais
		 * esta variavel poderá obter outro valor;
		 * logo a linha 25 vai apresentar um erro de compilação
		 * isso é considerado uma CONSTANTE na linguagem Java
		 */
		final double pi = 3.14;
		
		pi=3.15;
	}
}
```

#### Exercício

1. Declare de forma legível, variáveis que representam seus dados pessoais como: nome, cpf, idade, altura, doador orgao, email, telefone e data de nascimento.
2. Informe os valores de cada variável, considerando o tipo com dados reais ou fictícios.



#### Referências

{% embed url="https://tableless.com.br/java-tipos-de-dados" %}
