# Visibilidade dos recurso

## Modificadores

Em Java, utilizamos três palavras reservadas e um conceito default (sem nehuma palavra reservada) para definir os quatro tipo de visibilidade de atributos, métodos e até mesmo classes no que se refere ao acesso por outras classes. Iremos ilustrar do mais visível ao mais restrito tipo de visibilidade nos arquivos em nosso projeto.

Para uma melhor ilustração, iremos representar os conceitos de visibilidade de recursos através do contexto em uma lanchonete que vende lanche natural e suco.

### **Modificador public**&#x20;

Como o próprio nome representa, quando nossa classe, método e atributo é definido como public, qualquer outra classe em qualquer outro pacote pode visualizar tais recursos.

![](../.gitbook/assets/lanchonete\_1.png)

{% tabs %}
{% tab title="Cozinheiro" %}
```java
package lanchonete;

public class Cozinheiro {
	public void adicionarLancheNoBalcao() {
		System.out.println("ADICIONANDO LANCHE NATURAL HAMBURGER NO BALCAO");
	}
	public void adicionarSucoNoBalcao() {
		System.out.println("ADICIONANDO SUCO NO BALCAO");
	}
	public void adicionarComboNoBalcao() {
		adicionarLancheNoBalcao();
		adicionarSucoNoBalcao();
	}
	public void prepararLanche() {
		System.out.println("PREPARANDO LANCHE TIPO HAMBURGUER");
	}
	public void prepararVitamina() {
		System.out.println("PREPARANDO SUCO");
	}
	public void prepararCombo() {
		prepararLanche();
		prepararVitamina();
	}
	public void selecionarIngredientesLanche() {
		System.out.println("SELECIONADO O PÃO, SALADA, OVO E CARNE");
	}
	public void selecionarIngredientesVitamina() {
		System.out.println("SELECIONADO FRUTA, LEITE E SUCO");
	}
	public void lavarIngredientes() {
		System.out.println("LAVANDO INGREDIENTES");
	}
	public void baterVitaminaLiquidificador() {
		System.out.println("BATENDO VITAMINA LIQUIDIFICADOR");
	}
	public void fritarIngredientesLancheNatural() {
		System.out.println("FRITANDO A CARNE E OVO PARA O HAMBURGER");
	}
}

```
{% endtab %}

{% tab title="Almoxarife" %}
```java
package lanchonete;

public class Almoxarife {
	public void controlarEntrada() {
		System.out.println("CONTROLANDO A ENTRADA DOS ITENS");
	}
	public void controlarSaida() {
		System.out.println("CONTROLANDO A SAIDA DOS ITENS");
	}
	public void entregarIngredientes() {
		System.out.println("ENTREGANDO INGREDIENTES");
		//...?
	}
}
```
{% endtab %}

{% tab title="Atendente" %}
```java
package lanchonete;

public class Atendente {
	public void servindoMesa() {
		//...?
		System.out.println("SERVINDO MESA");
	}
	public void pegarLancheCozinha() {
		System.out.println("PEGANDO O LANCHE NA COZINHA");
	}
	public void receberPagamento() {
		System.out.println("RECEBENDO PAGAMENTO");
	}

```
{% endtab %}

{% tab title="Cliente" %}
```java
package lanchonete;

public class Cliente {
	public void escolherLanche() {
		System.out.println("ESCOLHENDO O LANCHE");
	}
	public void fazerPedido() {
		System.out.println("FAZENDO O PEDIDO");
	}
	public void pagarConta() {
		System.out.println("PAGANDO A CONTA");
	}
	public void consultarSaldoAplicativo() {
		System.out.println("CONSULTANDO SALDO NO APLICATIVO");
	}
}
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
**Acredite!** Nem tudo preciso ser visto por todos :rolling\_eyes:
{% endhint %}
