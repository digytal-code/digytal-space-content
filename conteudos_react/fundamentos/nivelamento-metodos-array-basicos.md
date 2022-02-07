# Nivelamento de JavaScript I - Métodos de Array Básicos

Antes de prosseguir no aprendizado de React, é necessário estarmos todos no mesmo nível de conhecimento em JavaScript. Isso é importante, pois React nada mais é do que uma biblioteca JavaScript e iremos abordar conceitos de nível intermediário (e alguns avançados) da linguagem. Portanto, se você ainda é novo em JavaScript, ou se precisa de uma revisão dos principais aspectos da linguagem, é recomendado que você não pule os módulos de nivelamento e leia todos na íntegra.

{% hint style="warning" %}
Atenção: esse módulo já considera que você possua o conhecimento básico de JavaScript e lógica de programação, portanto, não será uma aula aprofundada sobre os conceitos expostos, mas sim uma revisão.
{% endhint %}

## Métodos de Array Básicos

A principal finalidade de uma Array é guardar informações de modo ordenado, ou seja, para cada elemento da array, temos uma informação. Por ser um tipo de estrutura de dados tão comum em programação, o JavaScript já vem com alguns métodos pré-definidos para facilitar o manuseio de uma array pelo desenvolvedor.

Além disso, em 2015, o JavaScript teve uma das suas maiores e mais populares atualizações, que ficou conhecida como o momento de transição entre o JavaScript antigo e o Javascript Moderno. Essa atualização trouxe inúmeras novidades à linguagem, entre elas uma nova variedade de métodos de arrays. Esses métodos são _MUITO IMPORTANTES_ para React, pois são utilizados com frequência na biblioteca. Portanto, é crucial que você tenha noção de como utilizá-los.

### Método Array.push()

Considere a array:

```
let arrayAlunos = ["João", "Maria", "Carlos", "Ana"];
```

Essa array representa os alunos matriculados em uma escola. A aluna "Denise" se matriculou hoje, portanto, a array precisa ser atualizada. O método _push()_ adiciona o elemento especificado em seu parâmetro para o _final_ da Array:

![](../.gitbook/assets/push.png)

### Método Array.concat()

O método concat _cria um novo array_ unindo todos os elementos que foram passados como parâmetro, na ordem dada. Ele é diferente do push, que modifica a array original ao invés de criar uma nova array.

Esse método é frequentemente utilizado para fazer o "merge" entre duas arrays diferentes, gerando uma NOVA array como consequência.

Considere a array "arrayAlunos2", vamos concatená-la com a "arrayAlunos" do exemplo anterior:

![](../.gitbook/assets/concat.png)

_Exemplo extra_ (Concatenando 3 arrays de uma vez só):

![](../.gitbook/assets/concat3.png)

### Método Array.pop()

É o oposto do método push. Ao invés de adicionar o elemento no final da array, o método pop() _REMOVE o último elemento_ da array.

Considere a array "frutas" do exemplo anterior:

![](../.gitbook/assets/arraypop.png)

### Método Array.reverse()

É um método bem simples e direto: ele reverte a ordem dos elementos da Array.

![](../.gitbook/assets/reverse.png)

### Método Array.splice()

O método splice() altera o conteúdo de uma array adicionando novos elementos enquanto remove elementos antigos. É uma mistura dos métodos anteriores.

Considere a Array "cores":

```
let cores = ["Vermelho", "Verde", "Bola", "Azul"];
```

Você deve ter observado que há um erro nela, pois o elemento na posição 2 é "Bola", e "Bola" não é uma cor.

{% hint style="warning" %}
Lembre-se que, em programação, começamos a contar a partir do zero. Portanto, "Vermelho" está na posição 0, "Verde" na posição 1, e assim em diante... Posição também é chamado de "Index".
{% endhint %}

Iremos utilizar o método splice() para _REMOVER_ o elemento "Bola" da array e, simultaneamente, adicionar o elemento "Amarelo". A sintaxe do método splice() é assim:

![](../.gitbook/assets/splicesintax.png)

Portanto, o código fica assim:

![](../.gitbook/assets/arraypop.png)

O método splice() pode parecer um pouco confuso no começo, mas a prática vai fazer você memorizá-lo. Não se preocupe em gravar todos os métodos agora, apenas em ter uma noção de que eles existem e pra que servem. Sempre que precisar, você pode voltar à essa aula para revisá-los.

## Conclusão

Esses métodos básicos são úteis na hora de manusear arrays. Ainda existem outros métodos, os quais iremos aprender nos próximos módulos de nivelamento, mas precisamos visualizar outros conteúdos antes, como Arrow Functions.

Você pode ver todos os exemplos mostrados acima neste codepen: https://codepen.io/athosfeitosa/pen/MWOJWEO
