### **Operador Ternário em JavaScript**

O operador ternário é uma forma compacta de escrever uma instrução condicional `if-else`. Ele é chamado de "ternário" porque usa três partes: uma condição, uma expressão para o caso verdadeiro e uma para o caso falso.

---

### **Sintaxe**
```javascript
condição ? expressão1 : expressão2;
```

- **`condição`**: Uma expressão que será avaliada como `true` ou `false`.
- **`expressão1`**: Executada se a condição for `true`.
- **`expressão2`**: Executada se a condição for `false`.

---

### **Exemplo Básico**
```javascript
let idade = 18;
let mensagem = idade >= 18 ? "Maior de idade" : "Menor de idade";
console.log(mensagem);
```
**Saída:**  
`Maior de idade`

---

### **Comparação com `if-else`**
**Usando `if-else`:**
```javascript
let idade = 18;
let mensagem;

if (idade >= 18) {
  mensagem = "Maior de idade";
} else {
  mensagem = "Menor de idade";
}

console.log(mensagem);
```

**Usando operador ternário:**
```javascript
let idade = 18;
let mensagem = idade >= 18 ? "Maior de idade" : "Menor de idade";
console.log(mensagem);
```

O operador ternário torna o código mais compacto e legível em casos simples.

---

### **Aninhando Operadores Ternários**
Você pode aninhar operadores ternários, mas isso pode prejudicar a legibilidade.

Exemplo:
```javascript
let nota = 85;

let resultado = nota >= 90
  ? "Excelente"
  : nota >= 70
  ? "Bom"
  : "Precisa melhorar";

console.log(resultado);
```
**Saída:**  
`Bom`

---

### **Usando com Funções ou Operações**
```javascript
let numero = 5;
let tipo = numero % 2 === 0 ? "Par" : "Ímpar";
console.log(tipo);
```
**Saída:**  
`Ímpar`

---

### **Boas Práticas**
1. Use o operador ternário apenas para condições simples.
2. Evite aninhar operadores ternários em excesso para não comprometer a legibilidade.
3. Prefira `if-else` para condições mais complexas.

