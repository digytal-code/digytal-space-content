---
description: Do zero ao infinito, cuidado com o NaN! Haha
---

# Trabalhando com números

Trabalhar com números é relativamente simples, atribuir valores, realizar algumas operações e pronto, temos um novo resultado. Mas cuidado, é sempre bom avaliar com muita atenção, características como comprimento e precisão, antes de determinar, o tipo numérico para sua variável. Um caso simples é o exemplo abaixo:

```java
//arquivo Numeros.java
public static void main(String[] args) {

      //mundo perfeito
      byte numero = 128;
	
      //nossa!! precisamos converter, por quê ?
      byte numero = (byte) 129;
      
     //nossa!! imprimiu -127 o que aconteceu ?
      System.out.println(numero);
		
}
```

{% hint style="info" %}
Uma variável do tipo **byte,** só permite valores de -128 a 127, logo, o limite foi ultrapassado e a JVM realizou um ajuste de bytes.
{% endhint %}

Vamos para mais um caso:

```java
//arquivo Numeros.java
public static void main(String[] args) {

    int numero = 5;
    
    //caramba, 5 é menor que 127 e por quê não funcinou ?
    byte agoraPode = numero; 
    
    //agora funcionou através do casting explícito!
    byte maneiraCorreta = (byte) numero; 

}
```

{% hint style="info" %}
No exemplo acima, o Java não consegue converter de forma direta, um tipo **int** para um tipo **byte**, exigindo assim o que chamamos de [casting](http://www.universidadejava.com.br/materiais/java-casting-tipos-primitivos/).
{% endhint %}

Passando parâmetros:

Um outro ponto muito importante, é executar métodos que esperam parâmetros numéricos, veja o exemplo abaixo:

```java
//arquivo Numeros.java
public static void main(String[] args) {
    byte numero = 5;
    imprimirNumeroByte(numero);
    
    //Não, impossível, o que foi desta vez hein?
    imprimirNumeroByte(3);
    
}
static void imprimirNumeroByte(byte numero) {
    System.out.println(numero);
}
```

{% hint style="info" %}
Nas linhas 3 e 4, nós definimos que a variável número, é do tipo **byte,** igual ao tipo no parâmetro, porém na linha 7 informa o valor 3 direto, e para o Java, o número literal é do tipo **int**, logo ai, você já percebe que Java não é Javascript.
{% endhint %}

{% hint style="warning" %}
Vale lembrar, que precisamos compreender, quando estamos utilizando tipos primitivos ou classes [Wrappers](wrappers.md).
{% endhint %}

#### Exercícios

1. Pesquise sobre o uso dos tipos de dados primitivos,a classes wrapers, na linguagem Java e apresente um resumo;
2. Converta um número do tipo long (16405365619876L), para um tipo int e apresente o resultado com justificativa;
3. Converta um número do tipo double (12.765), para um tipo long e apresente o resultado com justificativa;
4. Tente fazer os mesmos procedimentos acima, utilizando classes **wrappers** e apresente o resultado com justificativa.



#### Referências

{% embed url="http://www.universidadejava.com.br/materiais/java-casting-tipos-primitivos" %}
