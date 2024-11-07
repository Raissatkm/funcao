# Documentação de Funções em JavaScript

## O que é uma função?

Uma **função** em JavaScript é um bloco de código projetado para realizar uma tarefa específica. Funções ajudam a organizar o código, tornar o código reutilizável e facilitar a manutenção.

### Estrutura de uma Função

A sintaxe básica de uma função é a seguinte:

```jsx

function nomeDaFuncao(parâmetros) {
  // código a ser executado
  return resultado; // opcional
}

```

- `function`
    - Palavra-chave que define uma função.
- `nomeDaFuncao`
    - O nome da função, que deve ser único e descritivo.
- `parâmetros`
    - Variáveis que representam os valores de entrada da função (opcional).
- `return`
    - Retorna um valor quando a função é chamada (opcional).

### Exemplo Básico

Vamos criar uma função que soma dois números:

```jsx

function somar(a, b) {
  return a + b;
}let resultado = somar(5, 3);
console.log(resultado); // Saída: 8

```

Neste exemplo:

- `absomar`
    
    e
    
    são parâmetros da função
    
    .
    
- `return a + b;`
    
    retorna o valor da soma para o local onde a função foi chamada.
    

### Tipos de Funções

1. **Funções Nomeadas**
    
    São funções com um nome especificado. Exemplo:
    
    ```jsx
   
    function saudacao() {
      console.log("Olá!");
    }saudacao(); // Saída: Olá!
    
    ```
    
2. **Funções Anônimas**
    
    Funções sem um nome. Elas são frequentemente usadas como funções de retorno de chamada.
    
    ```jsx
   
    const saudacao = function() {
      console.log("Oi!");
    };saudacao(); // Saída: Oi!
    
    ```
    
3. **Funções de Setas (Arrow Functions)**
    
    Introduzidas no ES6, são uma forma mais curta de escrever funções.
    
    ```jsx
  
    const somar = (a, b) => a + b;console.log(somar(2, 3)); // Saída: 5
    
    ```
    
    **Observação** : As funções de seta não são `this`próprias e são comumente usadas em funções mais simples e callbacks.
    

### Parâmetros Padrão

Você pode definir valores padrão para configurações que não foram passadas na chamada da função:

```jsx

function saudacao(nome = "Amigo") {
  console.log(`Olá, ${nome}!`);
}saudacao(); // Saída: Olá, Amigo!
saudacao("Ana"); // Saída: Olá, Ana!

```

### Funções de Alta Ordem

Funções que conferem outras funções como cláusulas ou retorno de funções.

```jsx

function executarOperacao(a, b, operacao) {
  return operacao(a, b);
}const multiplicar = (x, y) => x * y;
console.log(executarOperacao(5, 3, multiplicar)); // Saída: 15

```

### Escopo e`return`

- **Escopo**
    
    : Variáveis definidas dentro de uma função só são acessíveis dentro dela (escopo local).
    
- **`return**return`
    
    : A palavra-chave
    
    encerra a função e retorna um valor.
    

```jsx

function multiplicar(a, b) {
  let resultado = a * b;
  return resultado;
}console.log(multiplicar(4, 5)); // Saída: 20

```

### Exercício Prático

Crie uma função que calcula a área de um retângulo:

```jsx

function calcularAreaRetangulo(largura, altura) {
  return largura * altura;
}console.log(calcularAreaRetangulo(5, 10)); // Saída: 50

```

---

Esse guia fornece uma introdução sólida sobre como criar e usar funções em JavaScript, cobrindo desde a estrutura básica até funções de alta ordem e o uso de `return`!
