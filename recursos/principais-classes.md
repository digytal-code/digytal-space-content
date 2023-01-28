---
description: Tudo no Java, são classes.
---

# Principais classes

Como sabemos, em uma linguagem baseada no paradigma da orientação a objetos, nós desenvolvemos todo nosso código, em arquivos que são denominados classes. Pois bem, os recursos oferecidos pela própria linguagem, também estão disponíveis em classes, que são referências em nosso cotidiano.

Para termos um maior domínio na linguagem, é imprescindível conhecer e dominar algumas classes existentes na plataforma, para isso, iremos apresentar as que são utilizadas com mais frequência e o que você pode desfrutar com sua utilização.

> Pensar em desenvolvimento estruturado em classes, é como imaginar a família organizando a ceia de natal, onde cada membro é responsável por um prato.
>
> Regina: Perú / Augusto: Pernil / Fernanda: Pavê / Ana: Arroz com uva passa (Nãããoooo)!!!

| Classe                                             | Contexto                                                                                                                                                                                                                                     |
| -------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| String                                             | Classe que armazena textos e que podemos realizar operações de concatenação de palavras, tornar uma palavra maiúscula ou minúscula, podemos obter uma parte de um texto ou um conjunto de palavras a partir de um divisor.                   |
| Math                                               | Classe que contém a possibilidade de realizar operações matemáticas, como seno, cosseno, mínimo e máximo de dois valores e etc.                                                                                                              |
| Integer, Long, Byte, Short, Double                 | Classes da categoria das classes wrappers, é o objeto das nossas representações númericas, para cada tipo primitivo, ex.: Integer, Long, Double, Byte, Shor,  contendo métodos de conversão de texto para os respectivos tipos entre outros. |
| BigDecimal                                         | Classe numérica, mais recomendada para realizar um grande volume de operações matemáticas, diante de valores decimais.                                                                                                                       |
| Calendar, Date, LocalDate,     LocalDateTime, Time | Classes, com a finalidade de representar, data, datahora, somente hora e relacionar operações como adicionar um dia, adicionar uma hora e etc.                                                                                               |
| DateFormat, NumberFormat                           | Classes, com a finalidade de formatar datas e números considerando um formato ou um "locale" convenção padrão de formatação.                                                                                                                 |

```java
public class ClassePrincipal {
	public static void main(String[] args) {
		//String.class
		String nome = new String ("GLEYSON"); // classe que mantém um estado
		nome = nome + " SAMPAIO";
		nome = nome.concat(" OLIVEIRA");
		System.out.println(nome);
		
		//Math.class
		int minimo = Math.min(5, 8); // classe utilitária
		System.out.println("O valor mínimo entre 5 e 8 é:" + minimo);
		
		//Integer.class
		String textoNumero = "123";
		Integer numero = Integer.valueOf(textoNumero);
		System.out.println("Convertendo um texto numérico, é um tipo número " + numero);
		
		//BigDecimal.class
		BigDecimal calculo = BigDecimal.ZERO;
		calculo = calculo.add(new BigDecimal(3.7555));
		calculo = calculo.subtract(new BigDecimal(1.022));
		System.out.println("O resultado é :"+ calculo);
		
		//Calendar.class
		Calendar calendar = Calendar.getInstance();
		calendar.add(Calendar.DAY_OF_MONTH, 2);
		Date data = calendar.getTime();
		System.out.println("A nova data é " + data);
		
		//LocalDate.class
		LocalDate date = LocalDate.now();
		date = date.plusDays(2);
		System.out.println("A nova data é " + date);
	}
}

```

{% hint style="info" %}
Você pode visualizar, todos os recursos de todas a classes da linguagem Java, no site oficial da oracle, através de uma documentação bem estruturada. Veja o exemplo da documentação da classe [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html) na versão 8.
{% endhint %}

#### Exercícios

1. Apresentar de 2 a 4 novos métodos, das classes citadas acima;
2. Apresentar com exemplos, as finalidades dos novos métodos, descritos conforme exercício 1;
3. Apresentar de 2 a 4 novas classes, mais utilizadas no dia-a-dia e alguns métodos comuns. &#x20;

