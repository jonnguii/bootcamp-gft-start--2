# 🚀 Instalando o JDK e a IDE para Java

## 1️⃣ Instalando a IDE (Ambiente de Desenvolvimento Integrado)

O primeiro passo para trabalhar com Java é instalar o **JDK** (Java Development Kit) e uma **IDE** (Ambiente de Desenvolvimento Integrado). Existem várias opções de IDE, mas a que utilizaremos é a:

### 🔹 **IntelliJ IDEA**
[Link para download: IntelliJ IDEA](https://www.jetbrains.com/idea/)

### Passos de instalação:
1. Baixe o instalador para o seu sistema operacional (Windows, macOS ou Linux).
2. Execute o instalador e siga as instruções na tela.
3. Após a instalação, abra a IDE e configure seu JDK (Java Development Kit).

---

## 2️⃣ Instalando o JDK (Java Development Kit)

Antes de prosseguir, é importante entender a **importância do JDK**, que é essencial para compilar e executar programas Java. Para nós, desenvolvedores, o JDK nos oferece:

1. **Java Compiler (`javac`)**: Compila o código-fonte em Java (.java) para **bytecode**, gerando arquivos `.class`.
2. **JVM (Java Virtual Machine)**: Executa o bytecode em qualquer plataforma. Ela lê os arquivos compilados `.class` e os executa.
3. **JRE (Java Runtime Environment)**: Ambiente de execução responsável por rodar as aplicações Java, por meio da **JVM**, que executa o bytecode.

### 📝 Resumo:
- **Desenvolvedores** usam o **JDK** para obter **ferramentas de desenvolvimento**, como **javac** (compilador), **javadoc** (gerador de documentação) e outras, além do **JRE** e **JVM**.
- **Não-desenvolvedores** utilizam apenas o **JRE**, que fornece a **JVM**, suficiente para **executar** a aplicação.

---

### 🔧 Passos para Instalar o JDK:

1. **Baixar o JDK**
   [Link para download do JDK:](https://www.oracle.com/ae/java/technologies/downloads/)

2. **Passos de instalação**
   - **Windows**
     - Baixe o instalador `.exe` para Windows.
     - Execute o instalador e siga as instruções na tela.
     - Durante a instalação, anote o caminho onde o JDK será instalado (por exemplo: `C:\Program Files\Java\jdk-10`).

3. **Configurando o JDK no Sistema**
   Após instalar o JDK, é necessário adicionar o **JAVA_HOME** e o **PATH** no sistema para que o Java funcione corretamente.

   Em resumo, para que os projetos encontrem caminhos de instalação ou diretórios com arquivos necessários, configuramos **variáveis de ambiente**.  
   As **variáveis de ambiente** são valores armazenados no sistema operacional, que contêm informações sobre diretórios, caminhos (**path**) e ambientes de execução necessários para que a aplicação rode corretamente.

---

### ⚙️ No Windows:

1. **Abra o menu de Variáveis de Ambiente:**
   - Abra o menu iniciar e escreva: **"Variáveis de ambiente"** ou, se sua máquina estiver em inglês, pesquise **"Environment variables"**.
   - Na aba **"Avançado"** ou **"Advanced"**, clique em **"Variáveis de Ambiente"** ou **"Environment Variables"**.

2. **Adicione a variável `JAVA_HOME`:**
   - Clique em **"Nova..."** (**New...**) em **Variáveis do sistema** (**System variables**).
   - **Nome da variável**: `JAVA_HOME`
   - **Valor da variável**: O caminho onde o JDK foi instalado, por exemplo: `C:\Program Files\Java\jdk-10`.

3. **Adicione o JDK ao PATH:**
   - Encontre a variável **Path** nas **variáveis do sistema** e clique em **"Editar"** (**Edit**).
   - Clique em **"Novo"** (**New**) e adicione o caminho até a pasta **bin** do JDK, por exemplo: `C:\Program Files\Java\jdk-10\bin`.

4. **Verifique a instalação:**
   - Abra o **Prompt de Comando** e digite o seguinte comando:
   
```
java -version
```
Isso deve mostrar a versão do JDK que você acabou de instalar.



## 3️⃣ Instalando o Maven e o Gradle

🔨 O que são Maven e Gradle?

O Maven e o Gradle são construtores de build utilizados para gerenciar projetos Java. 
Eles automatizam diversas tarefas que precisaríamos fazer manualmente, como:

Gerenciamento de dependências

Compilação e empacotamento do código

Execução de testes automatizados

Gerenciamento do ciclo de vida do projeto

O Maven é baseado em XML (pom.xml), enquanto o Gradle utiliza arquivos Groovy/Kotlin (build.gradle).


### 📌 Instalando o Maven


Baixe o Maven:

Download do Maven

Extraia os arquivos:

Extraia o arquivo para um local como C:\Program Files\Apache Maven

Configure as Variáveis de Ambiente:

Crie uma variável MAVEN_HOME apontando para o diretório extraído

Adicione C:\Program Files\Apache Maven\bin ao Path

Verifique a instalação:

mvn -version


### 📌 Instalando o Gradle





Baixe o Gradle:

Download do Gradle

Extraia os arquivos:

Extraia o arquivo para um local como C:\Program Files\Gradle

Configure as Variáveis de Ambiente:

Crie uma variável GRADLE_HOME apontando para o diretório extraído

Adicione C:\Program Files\Gradle\bin ao Path

Verifique a instalação:

gradle -v


## 4️⃣ Um princípio muito importante utilizado em projetos Java são os chamados wrappers.

O que é um Wrapper? 🛠️

O wrapper é uma ferramenta que corrige o problema de vários desenvolvedores de uma equipe/projeto utilizarem versões diferentes dos softwares de construção de builds, como Gradle ou Maven.

📌 Benefícios do Wrapper:

Garante que todos utilizem a mesma versão do Maven ou Gradle

Permite rodar projetos sem precisar instalar o Maven ou Gradle manualmente

Por exemplo, no Gradle, ao rodar o comando:

```
gradlew build
```

o projeto usará a versão específica definida nele, sem depender da instalação global.

