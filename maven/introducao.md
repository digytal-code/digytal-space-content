# Introdução

Apache Maven, ou Maven, é uma ferramenta de automação de compilação utilizada primariamente em projetos Java.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

## Para quê serve ?

Mesmo tendo uma das principais funções como o gerenciamento de dependências, o maven também é capaz de auxiliar na compilação, build e deploy de nossos projetos desenvolvidos em Java.

Toda a configuração do projeto fica centralizada em arquivo demonidade de `pom.xml`&#x20;



```xml
<!Estrutura simples do arquivo pom.xml>

<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
  <modelVersion>4.0.0</modelVersion>

  <groupId>com.suaempresa.ou.seuprojeto</groupId>
  <artifactId>projeto-maven</artifactId>
  <version>1.0</version>

  <name>projeto-maven</name>
  
  <properties>
    <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    <maven.compiler.source>1.7</maven.compiler.source>
    <maven.compiler.target>1.7</maven.compiler.target>
	
     <sua.propriedade> ... </sua.propriedade> 
  </properties>

  <dependencies>
    <dependency>
      <groupId>junit</groupId>
      <artifactId>junit</artifactId>
      <version>4.11</version>
    </dependency>
	
     <dependency>
	 ...
     </dependency>
	
  </dependencies>

  <build>
  
   ...
  
  </build>
  
</project>
```
