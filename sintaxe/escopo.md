---
description: Onde escrever em uma página branca em branco?
---

# Escopo

Uma parte fundamental na elaboração de algoritmos simples ou complexos é determinar a  localização do código em questão. Sem um domínio sobre escopo de códigos seu projeto tende a conter falhas estruturais e comprometer a proposta principal da aplicação.&#x20;

```java
public class Conta {
	//variavel da classe conta
	double saldo=10.0;
	
	public void sacar(Double valor) {
		//variavel do método
		double novoSaldo = saldo - valor;
	}
	public void imprimirSaldo(){
		//disponível em toda classe
		System.out.println(saldo);
		//somente o método sacar conhece esta variavel
		System.out.println(novoSaldo);
	
	}
}
```
