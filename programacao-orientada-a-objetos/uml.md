# UML

Linguagem de Modelagem Unificada ou UML é uma notação que possibilita a representação gráfica do projeto.

![](<../.gitbook/assets/image (17) (1).png>)

Na UML temos três conceitos necessários de entender: **diagramas**, **elementos** e **relacionamentos**.

![](<../.gitbook/assets/image (7) (1).png>)

As notações UML são distribuídas em duas categorias de diagramas, a estrutural e comportamental conforme listagem abaixo:

### Diagramas estruturais

* **Diagrama de classe:** O Diagrama de Classes é utilizado para fazer a representação de estruturas de classes de negócio, interfaces e outros componentes do sistema. Por esta característica, este diagrama é considerado o mais importante para a UML, pois auxilia a maioria dos demais diagramas.
* **Diagrama de objetos**: Este diagrama representa os objetos existentes em um determinado instante ou fato  na aplicação. Assim conseguimos ter uma perspectiva do estado de nossos objetos mediante a interação dos usuários no sistema.&#x20;

{% hint style="info" %}
Existem outras categorias de diagramas estruturais e comportamentais, porém iremos focar nos citados acima.
{% endhint %}

### Diagrama de classe

O diagrama de classes ilustra **graficamente ** como classes serão estruturadas e interligadas entre si diante da proposta do nosso software.

Em diagrama a estrutura das classes é constituída por:

**Identificação:** Nome e/ou finalidade da classe

**Atributos:** Propriedades e/ou características

**Operações:** Ações e/ou métodos

### Relacionamentos

Em um diagrama as classes podem existir de forma independente, mas obviamente haverá em alguma etapa da aplicação e necessidade de algumas se relacionarem, o que devemos compreender é o nível de dependência entre elas:

#### Associação

Uma associação define um relacionamento entre duas classes, permitindo que um objeto tenha acesso a estrutura de um outro objeto.

![](<../.gitbook/assets/image (7).png>)

* **Agregação:** Em uma agregação a classe principal contém uma relação com outra classe mas ela pode existir sem a classe agregadora. Imagina em um cadastro de Candidatos, podemos encontrar candidatos que ainda não possuem uma Profissão.

![Candidato é classe principal e a Profissao agregação](<../.gitbook/assets/image (10).png>)

* **Composição:** A composição já caracteriza uma dependência existencial entre a classe principal e classe associada. Imaginamos que uma Admissão só poderá existir contendo suas informações básicos e a composição do Candidato selecionado.

![Admissao é a classe principal e Candidato compõe a Admissão](<../.gitbook/assets/image (1).png>)

#### Multiplicidade

Nem sempre o relacionamento entre as classes será de **um para um**, um determinado cenário poderá exigir multiplicidades específicos conforme opções abaixo:

* 1\. -> Representa uma associação **contendo um elemento**.&#x20;
* \*. -> Representa uma associação **contendo uma lista de elementos**.
* 0..1 -> Representa uma associação **contendo zero ou um elemento**.&#x20;
* 0..\* -> Representa uma associação **contendo zero ou uma lista de elementos**.&#x20;
* 1..\* -> Representa uma associação **contendo um ou uma lista de elementos**.&#x20;

![](<../.gitbook/assets/image (13).png>)

### Ferramentas

Existem inúmeras ferramentas de diagramação tanto online, pagas e gratuitas.

![](<../.gitbook/assets/image (17).png>)

{% embed url="https://www.saashub.com/staruml-alternatives" %}

#### Referência

{% embed url="https://micreiros.com/uml-e-os-diagramas-estruturais" %}

{% embed url="https://www.ateomomento.com.br/uml-diagrama-de-classes" %}

{% embed url="https://www.macoratti.net/vb_uml2.htm" %}
