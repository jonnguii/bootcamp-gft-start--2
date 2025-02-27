# 📌 Tópicos Fundamentais do Git  

Este módulo aborda conceitos essenciais do Git, incluindo sua estrutura, segurança e funcionamento:

### SHA-1 ✅
### OBJETOS FUNDAMENTAIS ✅
### SISTEMA DISTRIBUIDO ✅
### SEGURANÇA ✅
---

## 🔹 SHA-1  
O **Secure Hash Algorithm 1 (SHA-1)** é um algoritmo de hash usado pelo Git para garantir a integridade dos dados. 
Ele gera uma chave hash de **40 dígitos** para cada commit, garantindo que qualquer alteração no código resulte em um novo identificador único. 
Isso permite que o Git acompanhe todas as versões do projeto de forma confiável.  


##  📦 Objetos Fundamentais  


### 📁 Blob (Binary Large Object)
Um **blob** é um objeto do Git utilizado para rastrear o **conteúdo de um arquivo**, de forma a manter a integridade desses dados com hashes geradas pelo SHA-1. Quando um arquivo é adicionado, o Git gera um blob. Esse blob é responsável por armazenar o **conteúdo puro** desse arquivo, descartando títulos e rótulos. Ao fazer isso, ele gera uma hash. Toda vez que o conteúdo do arquivo (rastreado pelo blob) é modificado, uma nova hash é gerada. Portanto, cada vez que um arquivo é adicionado, um novo blob é criado, ou seja, cada blob é responsável por rastrear cada arquivo.


### 🌳 Tree (Árvores)
As **trees** são estruturas que apontam e armazenam os blobs, funcionando de maneira semelhante às pastas do computador.

- Cada **pasta** é representada por uma tree.
- Cada **arquivo** é representado por um blob.

### Exemplo de Estrutura de Tree:
```
Projetos (Tree) 
├── texto.txt (blob)
└── imagem.png (blob)
	└── Arquivos (Tree)
	  └── Antigos.csv (blob)
```

### 📅 Commit
Os **commits** são registros de alterações feitas em um repositório Git. Quando realizamos um commit, movemos nossas alterações para uma área de segurança, conhecida como **staging** (pré-oficial). A estrutura de um commit inclui:

- **Hash SHA-1**: Cada commit possui sua própria hash única.
- **Tree**: O commit aponta para uma tree que representa o estado atual do repositório.
  - **Cada tree** contém seus blobs ou subtrees.
    - **Cada blob** armazena os arquivos correspondentes.
- **Mensagem**: Uma descrição do que foi alterado, fornecida com o parâmetro `-m`.
- **Autor e Data**: Informações sobre quem fez o commit e quando.



## 🌐 Sistema Distribuído
O **Git** é um sistema de controle de versão distribuído, isso se dá baseado nas premissas que o faz ser seguro:

- **Integridade de Dados**: Cada objeto (blobs, trees, commits) possui um hash SHA-1 único, garantindo que os dados não sejam corrompidos e que cada versão do código seja rastreável.
  
- **Rastreabilidade**: Com a estrutura de commits e mensagens, é fácil acompanhar o histórico de alterações e entender a evolução do projeto.

- **Staging Area**: Antes de realizar um commit, as alterações podem ser organizadas e revisadas na área de staging, proporcionando maior controle sobre o que será salvo.

- **Armazenamento Local e em Nuvem**: O Git permite que os desenvolvedores trabalhem offline em suas cópias locais e sincronizem as alterações com um repositório remoto, seja em um servidor ou na nuvem.

- **Branches**: A criação de branches facilita o desenvolvimento de novas funcionalidades ou correções sem afetar o código principal, promovendo uma colaboração eficaz entre equipes.



🔑 SSH e Token

O SSH (Secure Shell) e o Token PAT (Personal Access Token) são medidas de segurança para proteger a comunicação entre sua máquina local e o repositório GitHub.

- SSH: O SSH gera um par de chaves criptografadas (pública e privada), permitindo que você não precise mais digitar sua senha toda vez que executar git push ou git pull. 
Além de acelerar o processo, ele fornece um nível extra de segurança, prevenindo ataques.

- Token PAT: O Personal Access Token (PAT) é gerado com uma combinação de caracteres e pode ter uma data de expiração. 
Ele substituiu o método tradicional de login com e-mail e senha, garantindo mais segurança ao acessar repositórios privados via HTTPS.




