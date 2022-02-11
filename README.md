# Java Básico

Iremos apresentar todos os requisitos necessários para você começar a desenvolver em uma das linguagens mais utilizadas no mercado.

![](<.gitbook/assets/image (7).png>)

### Simples

Java é uma linguagem de programação simples e de fácil compreensão, pois não contém as mesmas complexidades existentes nas linguagens de programação predecessoras. Devido a necessidade de funcionamento em dispositivos eletrônicos onde menos memória e recursos estão disponíveis, a simplicidade era o objetivo do design dos povos Javasoft. Java contém sintaxe semelhante a C e C++, portanto, os programadores que estão vindo dessas linguagens e estão mudando para Java não enfrentarão nenhum problema em termos de sintaxe.

### Orientada a Objeto <a href="#object-oriented" id="object-oriented"></a>

Java é uma linguagem de programação orientada a objetos. Isso significa que em Java tudo é escrito em termos de CLASSES e OBJETOS. O nosso maior desafio ao começar a desenvolver com Java é que, para ter um software consistente, é necessário compreender os pilares da Orientação a Objetos, como:&#x20;

1. Classe e objeto
2. Encapsulamento
3. Abstração  &#x20;
4. Herança
5. Polimorfismo

### Plataforma independente <a href="#platform-independent" id="platform-independent"></a>

O objetivo de design do Javasoft People é desenvolver uma linguagem que funcione em qualquer plataforma. Aqui plataforma significa um tipo de sistema operacional e tecnologia de hardware. Java permite que programadores escrevam seus programas em qualquer máquina com qualquer configuração e executem em qualquer outra máquina com configurações diferentes.&#x20;

O código-fonte é compilado para bytecode, que não está vinculado a nenhuma plataforma. Na verdade, este bytecode só é compreensível pela Java Virtual Machine (JVM) que está instalada em nosso sistema. Vamos conhecer um pouco mais sobre este conceito logo a seguir.

### Portátil

O conceito WORA (Write Once, Run Anywhere) e o recurso independente de plataforma tornam o Java portátil.&#x20;

Isso significa que não existe a necessidade de produzir uma versão compilada para cada sistema computacional em que se deseje executar a aplicação. Os desenvolvedores podem obter o mesmo resultado em qualquer máquina, escrevendo o código apenas uma vez.&#x20;

A razão por trás disso é JVM e bytecode. Suponha que você escreveu qualquer código em Java, então esse código é primeiro convertido em bytecode equivalente que só é legível pela JVM.

A portabilidade da linguagem é uma das principais vantagens para desenvolvedores e empresas que não querem se limitar a um único ambiente.

### Robusta

A linguagem de programação Java é robusta, o que significa que é capaz de lidar com o encerramento inesperado de um programa. Existem duas razões por trás disso:&#x20;

* Tratamento de Exceções&#x20;

Exceções são "erros" inesperados. As exceções ocorrem quando algo imprevisto acontece. Podem ser provenientes de erros de lógica ou acesso a recursos que não estejam disponíveis. Um exemplo disso é, por exemplo, atribuir um valor textual (string) à uma variável do tipo integer (número inteiro). Se ocorrer uma exceção no código Java, nenhum dano acontecerá, enquanto em outras linguagens de baixo nível, o programa travará.&#x20;

Para **tratar as exceções em Java** são utilizados os comandos try e catch.

* _Garbage Collector_ (Coletor de Lixo)

Outra razão pela qual o Java é forte está em seus recursos de gerenciamento de memória.  Ao contrário de outras linguagens de baixo nível, Java fornece um coletor de lixo de tempo de execução oferecido pela JVM, que coleta todas as variáveis ​​não utilizadas. Por isso, um **Garbage Collector** tem a função de alocar memória e garantir que quaisquer objetos referenciados permaneçam na memória. Além disso, o GC também busca recuperar a memória alocada pelos objetos que não são mais alcançáveis pelo código que está sendo executado.&#x20;

### Segura

Na era de hoje, a segurança é uma grande preocupação de todos os aplicativos. Atualmente todos os dispositivos estão conectados uns aos outros usando a Internet e isso abre porta para possíveis vulnerabilidades, como vírus ou hackers. E nossa construção de aplicativo usando Java também precisa de algum tipo de segurança. Assim, a linguagem também fornece recursos de segurança para os programadores. Problemas como ameaças de vírus, adulteração, espionagem e representação\* podem ser tratados ou minimizados usando Java. A linguagem também contém recursos de criptografia e descriptografia para proteger seus dados contra _espionagem_ e _adulteração_ na Internet.&#x20;

_\*Uma representação é um ato de fingir ser outra pessoa na internet._

### Interpretada

Nas linguagens de programação, você aprendeu que eles usam o compilador OU interpretador, mas a linguagem de programação Java usa os dois. Os programas Java são compilados para gerar arquivos de bytecode e a JVM interpreta o arquivo de bytecode durante a execução.&#x20;

### Multi-thread

Thread é um subprocesso leve e independente de um programa em execução (ou seja, processo) que compartilha recursos. E quando vários threads são executados simultaneamente é chamado de multi-threading.

O servidor também usa multithreading para fornecer seus serviços a várias solicitações de clientes. Em Java, você pode criar threads de duas maneiras, implementando a interface Runnable ou estendendo a classe Thread.&#x20;

