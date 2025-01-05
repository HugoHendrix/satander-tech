### **HOF (Higher-Order Functions) em JavaScript**

As **Higher-Order Functions (HOFs)** são funções que fazem uma das seguintes operações:

1. **Recebem outras funções como argumentos.**
2. **Retornam outras funções como resultado.**

Esse conceito é essencial em linguagens de programação funcional, como JavaScript, e facilita operações como manipulação de arrays, callbacks e pipelines de dados.

---

### **Exemplo Simples**
```javascript
function saudacao(nome) {
  return `Olá, ${nome}!`;
}

function executarComSaudacao(func, nome) {
  console.log(func(nome));
}

executarComSaudacao(saudacao, "João");
// Saída: Olá, João!
```

- A função `executarComSaudacao` recebe uma função (`func`) e um argumento (`nome`), mostrando como HOF pode ser usada para reutilização de código.

---

### **HOFs no JavaScript: Métodos de Array**
Os métodos nativos de arrays, como `map`, `filter` e `reduce`, são exemplos de HOFs.

#### **1. `map`: Transformação de Arrays**
Cria um novo array aplicando uma função em cada elemento do array original.
```javascript
const numeros = [1, 2, 3, 4];
const dobrados = numeros.map(num => num * 2);
console.log(dobrados);
// Saída: [2, 4, 6, 8]
```

---

#### **2. `filter`: Filtragem de Arrays**
Retorna um novo array com elementos que atendem a uma condição.
```javascript
const numeros = [1, 2, 3, 4];
const pares = numeros.filter(num => num % 2 === 0);
console.log(pares);
// Saída: [2, 4]
```

---

#### **3. `reduce`: Redução de Arrays**
Reduz um array a um único valor, acumulando os resultados de uma função.
```javascript
const numeros = [1, 2, 3, 4];
const soma = numeros.reduce((acumulador, atual) => acumulador + atual, 0);
console.log(soma);
// Saída: 10
```

---

### **Retornando Funções**
Uma HOF pode retornar outra função, criando "fábricas de funções".
```javascript
function criarSaudacao(saudacao) {
  return function (nome) {
    return `${saudacao}, ${nome}!`;
  };
}

const saudacaoFormal = criarSaudacao("Boa tarde");
console.log(saudacaoFormal("Maria"));
// Saída: Boa tarde, Maria!
```

---

### **Callbacks com HOF**
HOFs são muito úteis com callbacks, como em eventos ou operações assíncronas.
```javascript
function executarTarefa(callback) {
  console.log("Executando tarefa...");
  callback();
}

executarTarefa(() => console.log("Tarefa concluída!"));
// Saída:
// Executando tarefa...
// Tarefa concluída!
```

---

### **Benefícios das HOFs**
1. **Reutilização de Código**: Menos repetição e mais modularidade.
2. **Legibilidade**: Código mais limpo e intuitivo.
3. **Funcionalidade**: Suporte a programação funcional com manipulação avançada de dados.

