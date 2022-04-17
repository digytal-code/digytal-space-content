# Enums

Enum é um tipo especial de classe onde os objetos são previamente criados, imutáveis e disponíveis por toda aplicação.

Usamos Enum quando o nosso modelo de negócio contém objetos de mesmo contexto que já existem de pré-estabelecida com a certeza de não haver tanta alteração de valores.

#### **Exemplos:**

**Grau de Escolaridade**: Analfabeto, Fundamental, Médio, Superior

**Estado Civil**: Solteiro, Casado, Divorciado, Viúvo

**Estados Brasileiros**: São Paulo, Rio de Janeiro, Piauí, Maranhão.

{% hint style="warning" %}
Não confunda uma lista de constantes com enum.
{% endhint %}

Enquanto que uma constante é uma variável de tipo com valor imutável, um enum é um conjunto de objetos já pre-definidos na aplicação.

Como um enum é um conjunto de objetos, logo, estes objetos podem conter atributos e métodos. Veja o exemplo de um enum para disponibilizar os quatro estados brasileiros citados acima, contendo informações de: Nome, Sigla e um método que pega o nome do de cada estado e já retorna para tudo maiúsculo.

```java
// Criando o enum EstadoBrasileiro para ser usado em toda a aplicação.
public enum EstadoBrasileiro {
	SAO_PAULO ("SP","São Paulo"),
	RIO_JANEIRO ("RJ", "Rio de Janeiro"),
	PIAUI ("PI", "Piauí"),
	MARANHAO ("MA","Maranhão") ;
	
	private String nome;
	private String sigla;
	
	private EstadoBrasileiro(String sigla, String nome) {
		this.sigla = sigla;
		this.nome = nome;
	}
	public String getSigla() {
		return sigla;
	}
	public String getNome() {
		return nome;
	}
	public String getNomeMaiusculo() {
		return nome.toUpperCase();
	}
	
}

```

Agora **NÃO** precisaremos criar objetos que representam cada estado toda vez que formos precisarmos destas informações, basta usar o **enum** acima e escolher a opção (objeto) já pré-definido em qualquer parte do nosso sistema.
