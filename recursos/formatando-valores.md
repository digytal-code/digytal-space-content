---
description: Nem tudo o que se vê, é o que é.
---

# Formatando valores

Linguagens de programação, usam variáveis para representar tipos de dados, em nossa aplicação. Mas precisamos compreender que, nem sempre precisamos apresentar os resultados, sem antes dar um toque de sofisticação.

Abaixo temos uma representação literal de alguns valores numéricos e datas como padrão na linguagem.

```java
// arquivo FormatandoValores.java
public static void main(String[] args) {
		
  Double preco = 10.2786;

  Date hoje = new Date();

  LocalDateTime agora = LocalDateTime.now();

  Integer itemPedido = 001;

  System.out.println(preco); // 10.2786
  System.out.println(hoje); // Wed Nov 03 10:14:26 BRT 2021
  System.out.println(agora); // 2021-11-03T10:14:26.158
  System.out.println(itemPedido); // 1 
}
```

Observem que, os resultados impressos, não foram nada agradáveis, é ai que surge a necessidade de formatar nossos valores literais, com [NumberFormat](https://docs.oracle.com/javase/7/docs/api/java/text/NumberFormat.html), [DateFormat](https://docs.oracle.com/javase/7/docs/api/java/text/DateFormat.html) e [String.format()](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html#format\(java.lang.String,%20java.lang.Object...\)).

**NumberFormat**

Classe responsável por disponibilizar, formas de formatação de valores numéricos e converter textos em números, com base em um formato.

```java
// arquivo FormatandoNumeros.java
public static void main(String[] args) {
		
  Double preco = 10.2786;
  
  //Definindo um formatador padrão MOEDA de acordo seu sistema operacinal
  NumberFormat formatter = NumberFormat.getCurrencyInstance();

  String precoFormatado = formatter.format(preco);

  System.out.println(precoFormatado); // R$ 10,28
  
  //Definindo um formatador padrão NÚMERO de acordo seu sistema operacinal
  formatter = NumberFormat.getInstance();

  precoFormatado = formatter.format(preco);

  System.out.println(precoFormatado); // 10,279
  
  Double porcentagem = 0.653;

  //formatando valores decimais como porcentagem				
  formatter = NumberFormat.getPercentInstance();
		
  System.out.println(formatter.format(porcentagem)); //65%

}
		
```

{% hint style="danger" %}
Formatar números e datas, é um processo relativamente simples, na linguagem Java, mas você precisa garantir qual o idioma [Locale](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) , que o usuário da sua aplicação está utilizando.
{% endhint %}

```java
// arquivo FormatandoNumeros.java
public static void main(String[] args) {
		
  Double preco = 10.2786;
  
  //Especificando o idioma nas minhas formatações
  Locale locale = Locale.FRANCE;

  NumberFormat formatter = NumberFormat.getCurrencyInstance(locale);

  String precoFormatado = formatter.format(preco);

  System.out.println(precoFormatado);

}
```

#### DateFormat

Muito semelhante ao Number, podemos realizar a formatação de datas, para atender alguma necessidade da aplicação.

```java
// arquivo FormatandoDatas.java
public static void main(String[] args) {
		
   Date hoje = new Date();
   
   //Precisamos determinar como queremos formatar nossa data e hora
   DateFormat formatter = DateFormat.getDateInstance(DateFormat.SHORT);

   String dataFormatada = formatter.format(hoje);

   System.out.println(dataFormatada); // 03/11/21

   formatter = DateFormat.getDateTimeInstance(DateFormat.SHORT,DateFormat.SHORT);

   String dataHoraFormatada = formatter.format(hoje);

   System.out.println(dataHoraFormatada); // 03/11/21 10:48		
}
```

{% hint style="info" %}
Existem 4 tipos de formatos : SHORT, MEDIUM,LONG e FULL. Vamor fazer um array de formatos e imprimir todas as possibilidades?
{% endhint %}

```java
// arquivo FormatandoDatas.java
public static void main(String[] args) {
		
	Date hoje = new Date();
	
	int [] formatos = {DateFormat.SHORT,DateFormat.MEDIUM, DateFormat.LONG, DateFormat.FULL};
	for(int formato: formatos) {
		DateFormat formatter = DateFormat.getDateTimeInstance(formato, formato);
		
		String dataHoraFormatada = formatter.format(hoje);
		
		System.out.println(dataHoraFormatada);
	}
	
//RESULTADOS

// SHORT   -  03/11/21 10:57
// MEDIUM  -  03/11/2021 10:57:51
// LONG    -  3 de Novembro de 2021 10h57min51s BRT
// FULL    -  Quarta-feira, 3 de Novembro de 2021 10h57min51s BRT
	
}
```

**LocalDateFormat**

Não é muito diferente formatar datas, utilizando o projeto Java Time, existem classes de formatação, bem semelhantes a DateFormat.

```
//arquivo FormatandoDatas.java
public static void main(String[] args) {
		
  LocalDateTime hoje = LocalDateTime.now();
        
  //Usando formato MEDIUM para formatar a data
  String dataFormatada = hoje.format(DateTimeFormatter.ofLocalizedDateTime(FormatStyle.MEDIUM));

  System.out.println("MEDIUM format: " + dataFormatada);

  //Customizando um padrão de formatação
  dataFormatada = hoje.format(DateTimeFormatter.ofPattern("dd-MMM-yy HH:mm"));
 
  System.out.println("CUSTOM format: " +dataFormatada);

//RESULTADOS

// MEDIUM format: 03/11/2021 11:17:39
// CUSTOM format: 03-nov-21 11:17
}
```

{% hint style="success" %}
Como podemos perceber, nos exemplos acima, a formatação é converter um valor real, em uma representação, do tipo texto String.
{% endhint %}

#### Exercícios

1. Considerando o número 568543.298, formate para no mínimo 3 idiomas;
2. Utilizando o pacote Java Time, defina uma variável que represente uma data comemorativa e imprima o resultado conforme a seguir: **30/jun/84 10:35:48**.



**Referências**

{% embed url="http://tutorials.jenkov.com/java-internationalization/numberformat.html" %}

{% embed url="http://tutorials.jenkov.com/java-internationalization/decimalformat.html" %}

