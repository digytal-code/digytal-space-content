---
description: Todas as ações da aplicações, são consideradas métodos.
---

# Métodos

Na programação orientada a objetos, métodos, correspondem a funções ou sub-rotinas disponíveis em nossas classes.

Existe uma convenção estrutural, para todos os métodos que é determinada pelos aspectos abaixo:

1. **Qual a proposta principal do método?** Você se perguntar constantemente até compreender a real finalidade do mesmo.
2. **Qual o tipo de retorno esperado após executar o método?** Você deve analisar se o método será responsável por retornar algum valor ou não.
3. **Quais os parâmetros serão necessários para execução do método?** Os métodos às vezes precisarão de argumentos, como critérios para a execução.
4. **O método possui o risco de apresentar alguma exceção?** Exceções são comuns na execução de métodos, às vezes, é necessário prever e tratar a possível existência de uma exceção.
5. **Qual a visibilidade do método?** Avaliar se será necessário que o método seja visível a toda aplicação, somente em pacotes, através de herança ou somente a nível a própria classe.

Abaixo, temos um exemplo de uma classe com dois métodos e suas respectivas considerações:

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

{% hint style="warning" %}
O tipo **void** representa ausência de valor retornado por um método.
{% endhint %}

Agora que você compreendeu, que a estrutura do método segue um padrão de requisitos, como seria a estrutura de um método que tivesse a finalidade de formatar ceps? Onde o **cep** (parâmetro)  é um numero **inteiro** e deve **retornar** o cep em forma de **texto** (String), exemplo:

* **INPUT**     :  65300000
* **OUTPUT** :  65.300-000
