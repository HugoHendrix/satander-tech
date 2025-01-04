
### **Operadores Booleanos:**
Os operadores booleanos avaliam expressões e retornam valores `true` ou `false`.

1. **Igualdade e Relacionais:**
   - Igualdade estrita: `===` (compara valor e tipo)
   - Igualdade não estrita: `==` (compara apenas valor, fazendo coerção)
   - Diferente estrito: `!==`
   - Maior/menor que: `>`, `<`
   - Maior/menor ou igual: `>=`, `<=`

   Exemplo:
   ```javascript
   console.log(5 === "5"); // false
   console.log(5 == "5");  // true
   console.log(10 > 5);    // true
   ```

2. **Lógicos:**
   - **E lógico (`&&`)**: Retorna `true` se todas as expressões forem verdadeiras.
   - **Ou lógico (`||`)**: Retorna `true` se ao menos uma expressão for verdadeira.
   - **Negação (`!`)**: Inverte o valor lógico.

   Exemplo:
   ```javascript
   console.log(true && false); // false
   console.log(true || false); // true
   console.log(!true);         // false
   ```

---

### **Condicionais:**
Controlam o fluxo do programa com base em condições.

1. **`if`, `else if`, `else`:**
   ```javascript
   let idade = 18;

   if (idade >= 18) {
     console.log("Maior de idade");
   } else if (idade >= 16) {
     console.log("Pode votar");
   } else {
     console.log("Menor de idade");
   }
   ```

2. **`switch`:**
   Usado para múltiplas condições baseadas em um valor específico.
   ```javascript
   let cor = "vermelho";

   switch (cor) {
     case "vermelho":
       console.log("Pare!");
       break;
     case "verde":
       console.log("Siga!");
       break;
     default:
       console.log("Atenção!");
   }
   ```

---

### **Conjunções Lógicas:**
1. **E (`&&`):**
   Avalia a próxima expressão apenas se a primeira for `true`.
   ```javascript
   console.log(5 > 3 && 8 < 10); // true
   ```

2. **Ou (`||`):**
   Avalia a próxima expressão apenas se a primeira for `false`.
   ```javascript
   console.log(5 > 10 || 8 < 10); // true
   ```

---

### **Negação:**
O operador `!` inverte o valor lógico.
```javascript
console.log(!true);  // false
console.log(!false); // true
console.log(!(5 > 3)); // false
```

---

