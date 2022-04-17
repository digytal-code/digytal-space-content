# Construtores

Sabemos que para criar um objeto na linguagem Java utilizamos a seguinte estrutura de código:

```java
Classe novoObjeto = new Classe();
```

Desta forma será criado um novo objeto na memória, este recurso também é conhecido como instanciar um novo objeto.

Muitas das vezes já queremos que na criação (instanciação) de um objeto, a linguagem já solicite para quem for criar este novo objeto defina algumas propriedades essenciais. Abaixo iremos ilustrar uma classe Pessoa onde a mesma terá os atributos: Nome, CPF, Endereço.

```java
public class Pessoa {
	private String nome;
	private String cpf;
	private String endereco;
	
	public String getNome() {
		return nome;
	}
	public String getCpf() {
		return cpf;
	}
	public String getEndereco() {
		return endereco;
	}
	public void setEndereco(String endereco) {
		this.endereco = endereco;
	}
	//...
	//setters de nome e cpf ?
}

```

