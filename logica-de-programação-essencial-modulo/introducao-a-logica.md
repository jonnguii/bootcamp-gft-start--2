
---

🚀 **Lógica de Programação Essencial**

## 📌  **Conteúdo**

- ### **Entendendo o que é lógica**
- ### **O que são algoritmos e pseudocódigo**
- ### **Aprendendo fluxograma, variáveis e constantes**
- ### **Tomadas de decisões e expressões**
- ### **Como utilizar a concatenação**

---

🔍 **1. Entendendo o que é Lógica**

Lógica é o conceito de coerência e conectividade entre determinado assunto.

✏️ Exemplo:

✅ Se não há trânsito de veículos à esquerda nem à direita de uma rua, eu atravesso.  
❌ Caso contrário, eu aguardo.

---

💻 **2. O que é Lógica de Programação**

Lógica de programação é basicamente criar uma forma precisa e lógica de executar uma sequência de comandos de computadores para resolver um problema da forma mais otimizada possível.

✏️ Exemplo:

```java
int numero = 10;

if (numero % 2 == 0) {
    Console.WriteLine("O número é par.");
} else {
    Console.WriteLine("O número é ímpar.");
}
```

---

🔢 **3. O que são Algoritmos e Pseudocódigo**

Algoritmos, de forma resumida, são a sequência de passos com a única finalidade de resolver um problema ou alcançar um objetivo.

✏️ Exemplo:

```
🚗 ### Algoritmo: Dirigir um carro

1. Entrar no carro.
2. Colocar o cinto de segurança.
3. Verificar se o carro está no ponto morto e se o freio de mão está puxado.
4. Ligar o carro.
5. Pressionar o pedal do freio.
6. Engatar a primeira marcha (ou colocar no "D" se for automático).
7. Soltar o freio de mão.
8. Soltar o freio do pé aos poucos e acelerar suavemente.
9. Seguir as regras de trânsito e dirigir com atenção.
10. Para parar o carro, reduzir a velocidade, frear suavemente e estacionar em um local seguro.
11. Engatar o ponto morto e puxar o freio de mão.
12. Desligar o carro e sair com segurança.
```

📝 **Pseudocódigo** é a forma de escrever código utilizando sua linguagem nativa ou uma linguagem simples, de forma a estimular seu cérebro a lógica com mais facilidade.

✏️ Exemplo:

```text
JOGO SIMPLES DE LÓGICA COM 4 PERSONAGENS: OVELHA, REPOLHO, LOBO E PESCADOR. [https://www.novelgames.com/en/wolf/]
- O PESCADOR PRECISA ATRAVESSAR O RIACHO COM OS 3 OUTROS PERSONAGENS, PORÉM, ATENDENDO OS SEGUINTES REQUISITOS:
- LOBO NÃO PODE FICAR SOZINHO COM A OVELHA
- OVELHA NÃO PODE FICAR SOZINHA COM O REPOLHO
- O LOBO PODE FICAR SOZINHO COM O REPOLHO

Pseudocódigo utilizando linguagem portuguesa clara:

START GAME
Ovelha entra no barco
Atravessa
Ovelha sai do barco
Atravessa
Repolho entra no barco
Atravessa
Repolho sai do barco
Ovelha entra no barco
Atravessa
Ovelha sai do barco
Lobo entra no barco
Atravessa
Lobo sai do barco
Atravessa
Ovelha entra no barco
Atravessa
Ovelha sai do barco
GAME END
```

⚡ **Pseudocódigo** é diferente de uma linguagem de programação. Enquanto uma linguagem de programação possui uma sintaxe pré-definida, o pseudocódigo é a forma que você usa para estruturar o seu código, com coerência e lógica.

---

🔄 **4. Aprendendo Fluxograma, Variáveis e Constantes**

🔹 **Fluxogramas** são a forma gráfica de representar um algoritmo.

✏️ Exemplo:  
![Image](https://github.com/user-attachments/assets/a862a364-eb29-4cb5-bb00-dce0e27c33c6)

🔹 **Variáveis** são entidades que alocam um espaço na memória do computador, a partir de sua criação em código, utilizando os mais variados tipos (Números Inteiros [int], Texto [string], Caractere [char], Números Decimais [float], Condicional [boolean]).

✏️ Exemplo:

```java
public class Main {
    public static void main(String[] args) {
        int idade = 20; // Atribuindo o valor 20 à variável idade
        String nome = "João"; // Atribuindo o valor "João" à variável nome
        double altura = 1.75; // Atribuindo o valor 1.75 à variável altura

        System.out.println("Nome: " + nome);
        System.out.println("Idade: " + idade);
        System.out.println("Altura: " + altura);
    }
}
```

🔹 **Constantes** são variáveis fixas, ou seja, não podem ter seu valor alterado após ser atribuído.

✏️ Exemplo:

```java
public class Main {
    public static void main(String[] args) {
        final String Filho_do_meu_pai = "William"; // Constante com valor fixo
        // Filho_do_meu_pai = "João"; // Isso causaria um erro de compilação, pois não podemos alterar uma constante.

        System.out.println("Nome do seu irmão: " + Filho_do_meu_pai);
    }
}
```

---

🧠 **5. Tomadas de Decisões e Expressões**

Existem algumas expressões e estruturas no mundo da programação, baseadas em convenções lógicas. As mais usadas são as condicionais (if/else, switch/case).

As tomadas de decisões em lógica de programação, partem de estruturas como essas:

Chamamos esse bloco de código usando condicionais de 'Loop'.  
O **if/else** representa a seguinte lógica:

"Se X coisa for verdadeira, faça Y. Caso contrário, faça Z."  
Ou seja, quando uma condição é atendida, ela retorna um valor lógico ("Verdadeiro ou Falso").

✏️ Exemplo:

```java
import java.util.Scanner;

public class VerificarIdade {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);  // Criação de scanner para receber a idade do usuário

        System.out.print("Digite a sua idade: "); // Solicitar a idade da pessoa
        int idade = scanner.nextInt();
        
        if (idade >= 18) {         // Verificar se a pessoa tem idade suficiente para dirigir
            System.out.println("Você pode dirigir."); 
        } else {
            System.out.println("Você não pode dirigir.");
        }
        
        scanner.close();      // Fechar o scanner
    }
}
```

Dessa forma, percebemos uma otimização do fluxo do algoritmo, entregando o resultado esperado de forma coesa e seguindo uma estrutura convencional e universal.

Abordando o exemplo acima, também incluímos expressões aritméticas, como o uso do **Maior Igual (>=)**:

### Expressões Aritméticas:
- **Maior Igual (>=):** `>=` ➡️ 🟰
- **Menor Igual (<=):** `<=` ➡️ 🔽
- **Igual (==):** `==` ➡️ 🎯
- **Diferente de (!=):** `!=` ➡️ ❌
- **Soma (+):** `+` ➡️ ➕
- **Subtração (-):** `-` ➡️ ➖
- **Multiplicação (*):** `*` ➡️ ✖️
- **Divisão (/):** `/` ➡️ ➗
- **Incremento (++)**: `++` ➡️ ⬆️
- **Decremento (--)**: `--` ➡️ ⬇️

### Estruturas de controle:
- **Condicional (if, else):** `if` ➡️ ✅, `else` ➡️ ❌
- **Switch (case):** `switch` ➡️ 🔄
- **Laços (loops):** `for` ➡️ 🔁, `while` ➡️ 🔂, `do-while` ➡️ 🔃

---

🔗 **6. Como Utilizar a Concatenação**

🔤 A chamada **"Concatenação"** é a junção de 2 ou mais tipos de variáveis na programação.

```java
String nome = "João";
int idade = 20;

System.out.println("O nome do Desenvolvedor Backend é: " + nome + " e ele tem " + idade + " anos.");
```

Neste exemplo, temos dois tipos de variáveis: Inteiros e Texto. 
Essas variáveis tiveram valores atribuídos e, ao apresentar ao usuário, o operador `+` é o responsável por 
fazer a junção do texto (dentre aspas `""`) com as variáveis.

---

🏗️ **Estrutura de Repetição**

A estrutura de repetição é uma funcionalidade utilizada na lógica de programação que nos permitem repetir um determinado número de vezes um código.
Ela nos permite economizar poder computacional e elimina o processo de inserção manual de dados de grande porte.

```java
int numero = 0; 
    int limite = 10; 

        while (numero <= limite) {
            System.out.println("9x" + numero + " = " + numero * 9);
            numero++;
        }
```