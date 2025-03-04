## 🌟 O que é o Java?

Java é uma linguagem de programação criada pela empresa **Sun Microsystems** e, posteriormente, adquirida pela **Oracle Corporation**. 🚀

Java se tornou uma das linguagens mais populares no desenvolvimento de software.

A principal característica do Java é o conceito de **"write once, run anywhere"** (escreva uma vez, execute em qualquer lugar). 
Isso significa que, uma vez que você escreve um código Java, ele pode ser executado em qualquer sistema operacional sem a necessidade de modificações, 
desde que haja uma **JVM** (Java Virtual Machine) instalada no dispositivo. 🌍💻

## ⚙️ Como o Java funciona?

A ideia de **"rodar em qualquer plataforma"** é possível por meio da **compilação** do código Java. 
Quando você escreve um código em Java, ele tem a extensão `.java`. 
Esse código é compilado em um arquivo `.class`, que contém o que é conhecido como **Bytecode**. 
O Bytecode é uma versão intermediária do código que não é específica para nenhum sistema operacional.

Esse Bytecode é interpretado e executado pela **JVM (Java Virtual Machine)**.
A JVM é responsável por traduzir o Bytecode para instruções específicas do sistema onde o programa está sendo executado, 
permitindo que o código Java seja executado em qualquer plataforma que tenha a JVM instalada. 🖥️💡

### 🛠️ Fluxo de execução do Java:

1. **Escrita do código**: Você escreve o código fonte em Java com a extensão `.java`.
2. **Compilação**: O código fonte é compilado para um arquivo `.class`, contendo o Bytecode.
3. **Execução**: O arquivo `.class` é executado pela JVM, que interpreta o Bytecode e o traduz para o sistema específico.

Isso permite que o código Java seja extremamente portátil, pois não depende de compilar e ajustar o código para diferentes plataformas. 🌐




## 🌱 Compilando um arquivo java

O objetivo aqui é entender como funciona o processo de compilação e execução do código Java.

### 1. Estrutura

Primeiro, criamos uma pasta chamada **hello-java**, e dentro dessa pasta, criamos o arquivo `Hello.java` com o seguinte código:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

Agora, vamos para qualquer shell e no meu caso, vou usar o Prompt de Comando (CMD) no Windows:

Acessar a pasta onde está o arquivo Hello.java através do terminal:
```
cd caminho\para\a\pasta\hello-java
```

Usamos o comando "javac" para compilar o arquivo Hello.java. Isso cria o arquivo Bytecode com a extensão .class.:

```
javac Hello.java
```

Após compilar, podemos visualizar o conteúdo do arquivo Hello.java usando o comando type no CMD (isso funciona no Windows). 
Esse comando imprime o conteúdo do arquivo no terminal:

```
type Hello.java
```
O terminal mostrará o conteudo:

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}
```

Agora, vamos tentar visualizar o arquivo .class gerado:

```
type Hello.class
```

Saída no terminal:

```
��C��pclassd] lqH#t[a<8*A<2����3▒▒▒▒▒
```


O conteúdo do arquivo .class não faz sentido quando lido dessa forma, pois é o Bytecode Java. 
Esse é o código intermediário que a JVM (Java Virtual Machine) interpreta e executa.
