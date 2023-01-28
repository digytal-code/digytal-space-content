---
description: A hora é agora!
---

# Trabalhando com datas

A classe Calendar, é representada pelo padrão de calendário gregoriano, que representa a contagem dos anos, meses, semanas e dias e que tem como base, as estações do ano, isso quer dizer que criamos um objeto que representa, um determinado momento do tempo.

Até antes do Java 8, era comum utilizarmos a classe [java.util.Calendar](https://docs.oracle.com/javase/8/docs/api/java/util/Calendar.html) , para representar e realizar operações com objetos do tipo Data\Hora e [java.util.Date](https://docs.oracle.com/javase/8/docs/api/java/util/Date.html), somente quando para representação. Dai veio o projeto Java Time, contendo um conjunto de novos recursos, relacionados ao trabalho com Data\Hora na linguagem Java.

![](../.gitbook/assets/images.jfif)

#### Calendar

Classe apropriada para a realização de operações, como adicionar dia, subtrair mês, rolar hora e retronar uma instância de java.util.Date.

```java
//arquivo CalendarioData.java
public static void main(String[] args) {
    Calendar agora = Calendar.getInstance();
    
    //obtendo partes do tempo
    int dia = agora.get(Calendar.DAY_OF_MONTH);
    int mes = agora.get(Calendar.MONTH);// que mês é esse ?
    int ano = agora.get(Calendar.YEAR);
    
    int hora = agora.get(Calendar.HOUR);
    int minuto = agora.get(Calendar.MINUTE);
    int segundo = agora.get(Calendar.SECOND);
    
    //alterando uma parte do tempo
    
    agora.add(Calendar.DAY_OF_MONTH, 2);// aumentando o dia do mês para +2 dias
    
    System.out.println(agora);
    
    //convertendo um Calendar em um Data para fins mais convencionais
    Date dataAgora = agora.getTime();
    System.out.println(dataAgora);
}
```

**Date**

A classe java.util.Date, não é mais tão utilizada em novos projetos, sua única finalidade é definir uma compatibilidade de atributos, que representam Data\Hora em sua aplicação, hoje recomenda-se utilizar o projeto **Java Time**.

**Java Time**

Como mencionado acima, o projeto Java Time traz uma forma de trabalhar com Data\Hora, em nossa aplicação. Diante dos inúmeros recursos oferecidos pelo projeto, precisamos dominar suas 03 principais classes: **LocalDate**, **LocalTime** ou **LocalDateTime**.

```java
// arquivo CalendarioData.java
public static void main(String[] args) {
		
       LocalDate dataAtual = LocalDate.now();
		
       LocalTime horaAtual = LocalTime.now();

       LocalDateTime dataHoraAtual = LocalDateTime.now();

       //pegadinha do malandro
       dataAtual.plusDays(2);
 
       //forma correta
       dataAtual = dataAtual.plusDays(2);
		
       System.out.println(dataAtual);

       LocalDate amanha = dataAtual.plusDays(1);

      System.out.println(amanha);
}
```

**Momento exato**

Podemos de forma simples, definir momentos para nossas variáveis temporais, conforme código abaixo:

```java
// arquivo CalendarioData.java
public static void main(String[] args) {
      //passando os valores como paremtros		
      LocalDate descobertaBrasil = LocalDate.of(1500,4,22);
      System.out.println(descobertaBrasil);
      
      //usando o padrão americano para definir uma data como String 
      descobertaBrasil = LocalDate.parse("1500-04-22");
      System.out.println(descobertaBrasil);
       
      //utilizando um formatter para converter uma String em LocalDate 
      DateTimeFormatter formatter = DateTimeFormatter.ofPattern("dd/MM/yyyy");
      descobertaBrasil = LocalDate.parse("22/04/1500",formatter);
      System.out.println(descobertaBrasil);

}
```

**Comparando datas**

É comum termos que comparar se duas datas são iguais, maior ou menor entre si, para isso, as classes Java Time, possuem métodos para realizar este tipo de validação, retornando um valor `boolean` (sim\não).

```java
// arquivo CalendarioData.java
public static void main(String[] args) {
		
      LocalDate ontem = LocalDate.now().minusDays(1);
      System.out.println(ontem);

      LocalDate hoje = LocalDate.now();
      System.out.println(hoje);

      boolean verdade = hoje.isAfter(ontem);

      System.out.println(verdade);

      verdade = ontem.isBefore(hoje);
      System.out.println(verdade);

      verdade = hoje.isEqual(ontem);
      System.out.println(verdade);

}
```

Exercício:

Considerando a data 29/02/2020, utilizando o projeto Java Time, realize, obtenha e apresente as seguintes informações abaixo:

1. Imprima se o ano é bissexto;
2. Imprima o dia da semana;
3. Calcule uma nova data, adicionando +1 mes e subtraindo -12 dias.

{% hint style="success" %}
Documentação oficial [Java8 LocalDate](https://docs.oracle.com/javase/8/docs/api/java/time/LocalDate.html).
{% endhint %}





#### Referências

{% embed url="https://www.baeldung.com/java-8-date-time-intro" %}

{% embed url="https://www.ti-enxame.com/pt/java/diferencas-entre-o-java-8-date-time-api-java.time-e-o-joda-time/1046710409" %}

{% embed url="https://stackoverflow.com/questions/22463062/how-to-parse-format-dates-with-localdatetime-java-8" %}
