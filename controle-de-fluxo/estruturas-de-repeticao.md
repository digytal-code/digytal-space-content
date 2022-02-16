# Estruturas de repetição

> Laços de repetição, também conhecidos como laços de iteração ou simplesmente loops, são comandos que permitem iteração de código, ou seja, que comandos presentes no bloco sejam repetidos diversas vezes.&#x20;
>
> &#x20;                                                                               https://diegomariano.com/lacos-de-repeticao-2/



Laços ou repetições são representados pelas seguintes estruturas:

* **For** (para)
* **While** (enquanto)
* **Do While** (faça enquanto)

## For

O comando **`for`** (na tradução literal para a língua portuguesa “para”) permite que uma variável contadora seja testada e incrementada a cada iteração, sendo essas informações definidas na chamada do comando. O comando for recebe como entrada uma variável contadora, a condição e o valor de incrementarão.

![](<../.gitbook/assets/image (14).png>)

Vamos imaginar que Joãozinho precisa conter até 20 carneirinhos para pegar no sono:

```java
// ExemploFor.java
public class ExemploFor {
	public static void main(String[] args) {
		for(int carneirinhos = 1 ; carneirinhos <=20; carneirinhos ++) {
			System.out.println(carneirinhos + " - Carneirinho(s)");
		}
	}
}

```

Vamos explicar a estrutura do código acima:

**For position**

1. int carneirinhos = 1`;` -> O programa entende que a variável carneirinhos começa com o valor igual a 1 e isso acontece somente uma vez;
2. carneirinhos `< = 20;` -> O programa verifica se a variável carneirinhos ainda é menor que 20;
3. O programa começa a executar o algorítimo, no nosso caso imprimir a quantidade de carneirinhos em contagem;
4. carneirinhos `++` -> O programa aumenta em mais 1 o valor da variável carneirinhos;
5. O fluxo é finalizado quando a variável carneirinhos for igual a 20.

```java
// Outras estruturas

//estrutura 1
for(int carneirinhos = 1 ; carneirinhos <=20; carneirinhos ++) {
     System.out.println(carneirinhos + " - Carneirinho(s)");
}

//estrutura 2
//o que importa é somente o bloco condicional
int carneirinhos = 1;
for( ; carneirinhos <=20; ) {
     System.out.println(carneirinhos + " - Carneirinho(s)");
     carneirinhos ++;
}

//for( somente 1x ; deve ser uma expresão boolean; acontecerá a cada final da execução ) { }
```

### For Each



## While

O laço **`while`** (na tradução literal para a língua portuguesa “enquanto”) determina que enquanto uma condição for válida, o bloco de código será executado. O laço **`while`** testa a condição antes de executar o código, logo, caso a condição seja inválida no primeiro teste o bloco nem será executado.

![](<../.gitbook/assets/image (12).png>)

## Do While

O laço **`do / while`** (na tradução literal para a língua portuguesa “faça…enquanto”), assim como o laço while, determina que enquanto uma determinada condição for válida o bloco de código será executado. Entretanto, **`do / while`** testa a condição após executar o código, assim sendo, mesmo que a condição seja considerada inválida no primeiro teste o bloco será executado pelo menos uma vez.

![](<../.gitbook/assets/image (13).png>)
