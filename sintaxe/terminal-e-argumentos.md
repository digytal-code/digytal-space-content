# Terminal e Argumentos

Nem sempre executamos nosso programa Java pelo terminal, já pensou nossos clientes tendo que instalar o Eclipse ou VsCode para rodar o sistema em sua empresa ?

Com a JVM devidamente configurada, nós podemos criar um executável do nosso programa e disponibilizar o instalador para qualquer sistema operacional.

No nosso caso iremos aprender como executar um programa Java via terminal como MS - DOS ou terminal do VsCode.

Vamos criar uma classe chamada `MinhaClasse.java` com o código abaixo:

```java
public class MinhaClasse {
    public static void main(String[] args) {
        System.out.println("Oi, fui executado pelo Terminal");
    }
}
```

{% hint style="info" %}
Observe que nosso projeto Java criado por um IDE, ele terá uma pasta chamada **bin**. É nesta pasta que ficarão os arquivos **.class**, o nosso `bytecode`.
{% endhint %}
