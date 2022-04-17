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
