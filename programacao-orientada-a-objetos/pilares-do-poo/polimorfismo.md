---
description: Um mesmo comportamento de várias maneiras
---

# Polimorfismo

Podemos observar no contexto de **Abstração** e **Herança** que conseguimos criar uma singularidade estrutural de nossos elementos. Isso quer dizer que, qualquer classe que deseja representar um serviço de mensagens, basta estender a classe **`ServicoMensagemInstantanea`** e implementar os respectivos métodos _abstratos_. O que vale reforçar aqui é, cada classe terá a mesma ação executando procedimentos de maneira especializada.&#x20;

Este o resultado do que denominamos como Polimorfismo. Veja o exemplo abaixo:

```java
public class ComputadorPedrinho {
	public static void main(String[] args) {
		
		ServicoMensagemInstantanea smi = null;
		
		/*
		    NÃO SE SABE QUAL APP 
		    MAS QUALQUER UM DEVERÁ ENVIAR E RECEBER MENSAGEM
		 */
		String appEscolhido="???"; 
		
		if(appEscolhido.equals("msn"))
			smi = new MSNMessenger();
		else if(appEscolhido.equals("fbm"))
			smi = new FacebookMessenger();
		else if(appEscolhido.equals("tlg"))
			smi = new Telegram();
		
			
		smi.enviarMensagem();
		smi.receberMensagem();
	}
}
```

{% hint style="info" %}
Para concluirmos a compreensão, Polimorfismo permite que as classes mais abstratas determinem ações uniformes para que cada classe filha concreta implementem os comportamentos de forma específica.
{% endhint %}

#### Referências

{% embed url="https://pt.wikipedia.org/wiki/Polimorfismo_(ci%C3%AAncia_da_computa%C3%A7%C3%A3o)" %}

####
