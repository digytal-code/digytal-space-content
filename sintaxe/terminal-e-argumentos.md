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

![](<../.gitbook/assets/image (15).png>)

Mesmo usando uma IDE, nós sempre precisaremos identificar aonde se encontram as classes do nosso projeto, no meu caso está em: **C:\estudos\dio-trilha-java-basico\java-terminal.**

![](<../.gitbook/assets/image (6).png>)

## Terminal

Vamos ilustrar como executar uma classe, depois de compilada, sem precisar usar a IDE.

1. Abra o MS-DOS ou Power Shell
2. Localize o diretório do seu projeto: **`cd C:\estudos\dio-trilha-java-basico\java-terminal`**
3. Acesse a pasta **** _bin_: ** `cd bin`**
4. Agora digite o comando:**`java MinhaClasse` ** _(nome da sua classe sem a extensão .**class**)_&#x20;

![](<../.gitbook/assets/image (14).png>)

## Argumentos

Quando executamos uma classe que contenha o método main, o mesmo permite que passemos um array `[]` de argumentos do tipo String. Logo podemos após a definição da classe a ser executada informar estes parâmetros, exemplo:

```
java MinhaClasse agumentoUm argumentoDois
```
