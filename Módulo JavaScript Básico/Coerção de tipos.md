### **Coerção de Tipos:**

#### **1. Coerção Implícita:**
O JavaScript tenta automaticamente converter um tipo de dado para outro, dependendo do contexto da operação.

Exemplos:
```javascript
console.log("5" - 3);  // 2 (string é convertida para número)
console.log("5" + 3);  // "53" (número é convertido para string)
console.log(5 * "2");  // 10 (string é convertida para número)
console.log(5 == "5"); // true (valores são convertidos para o mesmo tipo)
```

#### **2. Coerção Explícita:**
O desenvolvedor converte manualmente um tipo de dado para outro usando métodos ou operadores.

Exemplos:
```javascript
// String para Número
let num = Number("123");
console.log(num); // 123

// Número para String
let str = String(123);
console.log(str); // "123"

// Boolean para Número
console.log(Number(true));  // 1
console.log(Number(false)); // 0

// Número para Boolean
console.log(Boolean(0));    // false
console.log(Boolean(42));   // true

// Parse de strings para números (inclui ponto flutuante)
console.log(parseInt("123.45")); // 123
console.log(parseFloat("123.45")); // 123.45
```

---

### **Arrays:**
Um **array** é uma estrutura de dados usada para armazenar vários valores em uma única variável.

#### **1. Criação:**
```javascript
let frutas = ["maçã", "banana", "laranja"];
```

#### **2. Acessando Elementos:**
```javascript
console.log(frutas[0]); // "maçã"
```

#### **3. Métodos Comuns:**
- **Adicionar elementos:**
  ```javascript
  frutas.push("uva");  // Adiciona ao final
  frutas.unshift("manga"); // Adiciona ao início
  ```
- **Remover elementos:**
  ```javascript
  frutas.pop();  // Remove o último
  frutas.shift(); // Remove o primeiro
  ```
- **Encontrar elementos:**
  ```javascript
  console.log(frutas.indexOf("banana")); // 1
  ```
- **Iterar sobre arrays:**
  ```javascript
  frutas.forEach((fruta) => console.log(fruta));
  ```

#### **4. Outras Operações Importantes:**
- **Tamanho do array:**
  ```javascript
  console.log(frutas.length); // Número de elementos
  ```
- **Copiar um array:**
  ```javascript
  let copia = [...frutas];
  ```
- **Juntar elementos:**
  ```javascript
  console.log(frutas.join(", ")); // "maçã, banana, laranja"
  ```
- **Ordenar elementos:**
  ```javascript
  frutas.sort(); // Alfabética
  ```

