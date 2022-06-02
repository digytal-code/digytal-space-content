# Interface

{% hint style="warning" %}
Antes de tudo, **NÃO** estamos nos referindo a interface gráfica. Tudo bem 😁😉
{% endhint %}

Como vimos anteriormente, **Herança** é um dos pilares de POO, mas uma curiosidade que se deve ser esclarecida na linguagem Java é que a mesma não permite o que conhecemos como **Herança Múltipla**.

Á medida que vão surgindo novas necessidades, novos equipamentos (objetos) nascem para atender as expectativas de oferecer ferramentas com finalidades bem específicas como por exemplo: Impressoras, Digitalizadoras, Copiadoras e etc.

Observem que não há uma especificação de marca, modelo e ou capacidades de execução das classes citadas acima, isto é o que consideramos o nível mais abstrato da orientação a objetos que denominamos como **interfaces**.

Ilustração de interfaces dos equipamentos citados acima.

![](<../.gitbook/assets/image (11) (1).png>)

Representação de objetos reais com base nas interfaces citadas acima.

![](<../.gitbook/assets/image (20) (1).png>)

> Então o que você está dizendo é que **interfaces** é o mesmo que **classes**? Um molde para representação dos objetos reais ?

Este é um dos maiores questionamentos dos desenvolvedores no que se refere a modelo de classes da aplicação.

Como citado acima Java não permite herança múltipla, logo, vamos imaginar que recebemos o desafio de projetar uma nova classe para criar objetos que representem as três características citadas acima e que iremos denominar de **EquipamentoMultifunional**.

![](<../.gitbook/assets/image (11).png>)

Para uma melhor compreensão, vamos analisar os diagramas de classes abaixo, comparando o conceito de herança entre classes e interfaces.

**Cenário 1**

![Exemplo de aplicação de Herança entre classes](<../.gitbook/assets/image (3).png>)

**Cenário 2**

![Ilustração do uso de interfaces para aplicar Herança Múltipla](<../.gitbook/assets/image (20).png>)

