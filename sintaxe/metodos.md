---
description: Todas as ações da aplicações são consideradas métodos
---

# Métodos

Na programação orientada a objetos, métodos correspondem a funções ou sub-rotinas disponíveis em nossas classes.

Os métodos deverão ser nomeados com verbos, através de uma mistura de letras minúsculas e maiúsculas. Em princípio todas as letras que compõem o nome devem ser mantidas em minúsculo, com exceção da primeira letra de cada palavra composta a partir da segunda palavra.

Exemplos sugeridos para nomenclatura de métodos:

```java
somar(int n1, int n2){}

abrirConexao(){}

concluirProcessamento() {}

findById(int id){} // não se assuste, você verá muito método em inglês em sua jornada

calcularImprimir(){} // há algo de errado neste método, ele deveria ter uma única finalidade

```

{% hint style="info" %}
ATENÇÃO! Não existe em **Java** o conceito de **métodos** globais. Todos os **métodos** devem sempre ser definidos dentro de uma classe.
{% endhint %}

Existe uma convenção estrutural para todos os métodos que é determinada pelos aspectos abaixo:

#### Critério de definição de métodos

1. **Qual a proposta principal do método?** Você se perguntar constantemente até compreender a real finalidade do mesmo.
2. **Qual o tipo de retorno esperado após executar o método?** Você deve analisar se o método será responsável por retornar algum valor ou não.

OBS: Caso o método não retorne nenhum valor, ele será representado pela palavra-chave `void`.&#x20;

1. **Quais os parâmetros serão necessários para execução do método?** Os métodos as vezes precisão de argumentos como critérios para a execução.
2. **O método possui o risco de apresentar alguma exceção?** Exceções são comuns na execução de métodos, as vezes é necessário prever e tratar a possível existência de uma exceção.
3. **Qual a visibilidade do método?** Será necessário que o método seja visível a toda aplicação, somente em mesmo pacotes, através de herança ou somente a nível a própria classe.

Abaixo temos um exemplo de uma classe com dois métodos e suas respectivas considerações:

```java
public class MyClass {
	
	public double somar(int num1, int num2){
		//LOGICA - FINALIDADE DO MÉTODO
		return ... ;
	}
	
	public void dizerOla(String nome){
		//LOGICA - FINALIDADE DO MÉTODO
		//AQUI NÃO PRECISA DO RETURN
		//POIS NÃO SERÁ RETORNADO NENHUM RESULTADO
	}
	
}
```
