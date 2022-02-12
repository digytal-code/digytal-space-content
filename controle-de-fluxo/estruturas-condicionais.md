# Estruturas condicionais

A Estrutura Condicional possibilita a escolha de um grupo de ações e comportamentos a serem executadas quando determinadas condições são ou não satisfeitas. A Estrutura Condicional pode ser **Simples** ou **Composta**.

## Condicionais Simples

Quando ocorre uma validação de execução de fluxo somente quando a condição for positiva, consideramos como uma estrutura **Simples**, exemplo:

![](<../.gitbook/assets/image (6).png>)

```java
// CaixaEletronico.java
public class CaixaEletronico {
    public static void main(String[] args) {

       double saldo = 25.0;
       double valorSolicitado = 17.0;

       if(valorSolicitado < saldo)
        saldo = saldo - valorSolicitado;

        System.out.println(saldo);

    }
}
```

## Condicionais Composta

Algumas vezes o nosso programa deverá seguir mais de uma jornada de execução condionado a uma regra de negócio, este cenário é demoninado **Estrutura Composto**. Vejamos o exemplo abaixo:

![](../.gitbook/assets/if-else.png)

```java
// ResultadoEscolar.java
public class ResultadoEscolar {
    public static void main(String[] args) {

       int nota = 6;
       
       if(nota >= 7)
        System.out.println("Aprovado");

       else
        System.out.println("Reprovado");
    }
}
```

{% hint style="success" %}
Vale ressaltar aqui que no Java um bloco **`if/else`** as vezes necessita de adicionar um bloco de **`{ }`**se a lógica conter mais de uma linha.
{% endhint %}
