# Cases

Vamos explorar alguns outros cenários com fluxo condicionais, repetições e excepcionais.

**Case 1**: Vamos imaginar que em um processo seletivo existe o valor base salarial de R$ 2.000,00 e o salário pretentido pelo candidato. Vamos elaborar um controle de fluxo onde:&#x20;

* Se o valor salario base for maior que valor salario pretentido, imprima : **LIGAR PARA O CANDIDATO**;
* Senão Se o valor salario base for igual ao valor salario pretentido, imprima : **LIGAR PARA O CANDIDATO COM CONTRA PROPOSTA**;
* Senão imprima: **AGUARDANDO RESULTADO DEMAIS CANDIDATOS**

```java
// Método que simula o valor pretendido

import java.util.concurrent.ThreadLocalRandom;
static double valorPretendido() {
     return ThreadLocalRandom.current().nextDouble(1800, 2200);
}
```

&#x20;**Case 2**: Foi solicitado que nosso sistema garanta que diante das inúmeras candidaturas sejam selecionados apenas no máximo 5 candidatos para entrevista onde o salário pretendido seja menor ou igual ao salário base.

```java
// Array com a lista de candidatos

String [] candidatos = {"FELIPE","MARCIA","JULIA","PAULO","AUGUSTO","MONICA","FABRICIO","MIRELA","DANIELA","JORGE"};
```

**Case 3**: Agora é hora imprimir a lista dos candidatos selecionados para disponibilizar para o RH entrar em contato.

**Case 4**: O RH deverá realizar uma ligação com no máximo 03 tentativas para candidato selecionado e caso o candidato atenda, deve-se imprimir:&#x20;

* **"CONSEGUIMOS CONTATO COM **_**`[CANDIDATO]`**_**` ``` APÓS **_**`[TENTATIVA]`**_** TENTATIVA(S)"**
* do contrário imprima: **"NÃO CONSEGUIMOS CONTATO COM O **_**`[CANDIDATO]`**_**"**

****

{% tabs %}
{% tab title="Soluções" %}
Hora de aplicar os conceitos apresentados, implementando as soluções para cada case apresentado
{% endtab %}

{% tab title="Case 1" %}
```java
public class ProcessoSeletivo {
	public static void main(String[] args) {
		//salario base maior que salario pretendido
		case1(2000.0, 1900.0);
		
		//salario base igual que salario pretendido
		case1(2000.0, 2000.0);
		
		//salario base igual que salario pretendido
		case1(1900.0, 2000.0);V
	}
	static void case1(double salarioBase, double salarioPretendido) {
		
		if(salarioBase > salarioPretendido) {
			System.out.println("LIGAR PARA O CANDIDATO");
		}
		else if(salarioBase == salarioPretendido) {
			System.out.println("LIGAR PARA O CANDIDATO COM CONTRA PROPOSTA");
		}
		else {
			System.out.println("AGUARDANDO RESULTADO DEMAIS CANDIDATOS");
		}
	}
}

```
{% endtab %}
{% endtabs %}
