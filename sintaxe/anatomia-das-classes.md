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

* **Nome de variável e métodos**: toda variável deve ser escrita com letra minúscula, porém se a palavra for composta, a primeira letra da segunda palavra deverá ser MAIÚSCULA, exemplo:                 `ano` e `ano`**`F`**`abricacao.`

{% hint style="info" %}
Existe uma regra adicional para variáveis quando na mesma queremos identificar que ela não sofrerá alteração de valor, exemplo: queremos determinar que uma variável de nome **br** sempre representará **"Brasil"** e nunca mudará seu valor, logo, determinamos como escrita o código abaixo:
{% endhint %}

```
String BR = "Brasil"
Double PI = 3.14
Integer ESTADOS_BRASILEIRO = 27
Integer ANO_2000 = 2000
```

## Declarando variáveis e métodos

Como identificar que entre declaração de variáveis e métodos em nossa programa? Existe uma estrutura comum para ambas as finalidades, exemplo:

* Declarar uma variável em Java é sempre a seguinte estrutura

```
// Estrutura

Tipo nomeBemDefinido = Atribuição (opcional em alguns casos)

// Exemplo

Integer idade = 23;
Double altura = 1.62;
Dog spike; //observe que aqui a variável spike não tem valor, é normal
```

## Identação

asd

![](<../.gitbook/assets/image (5).png>)

## Organizando nossos arquivos

À medida que nosso sistema vai sendo evoluído, surgem novos arquivos (código fonte) em nossa estrutura de arquivos do projeto. Isso exige que seja realizado uma organização destes arquivos através de pacotes (packages).
