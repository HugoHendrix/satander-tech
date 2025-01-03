### **Operadores Matemáticos:**
1. **Básicos:**
   - Soma: `+`
   - Subtração: `-`
   - Multiplicação: `*`
   - Divisão: `/`
   - Resto da divisão: `%`
   - Exponenciação: `**`

   Exemplos:
   ```javascript
   let a = 10, b = 3;
   console.log(a + b); // 13
   console.log(a - b); // 7
   console.log(a * b); // 30
   console.log(a / b); // 3.333...
   console.log(a % b); // 1
   console.log(a ** b); // 1000
   ```

2. **Incremento/Decremento:**
   - Incrementar: `++`
   - Decrementar: `--`

   Exemplos:
   ```javascript
   let x = 5;
   x++; // Agora x é 6
   x--; // Agora x é 5 novamente
   ```

3. **Operadores compostos:**
   - Soma e atribuição: `+=`
   - Subtração e atribuição: `-=`
   - Multiplicação e atribuição: `*=`
   - Divisão e atribuição: `/=`
   - Exponenciação e atribuição: `**=`

   Exemplos:
   ```javascript
   let y = 10;
   y += 5; // Agora y é 15
   y *= 2; // Agora y é 30
   ```

---

### **Biblioteca `Math`:**
A biblioteca `Math` fornece funções e constantes para cálculos matemáticos.

1. **Constantes importantes:**
   - `Math.PI`: Valor de π (3.14159...)
   - `Math.E`: Base do logaritmo natural (2.718...)

2. **Funções úteis:**
   - **Arredondamento:**
     ```javascript
     Math.round(4.7); // 5
     Math.floor(4.7); // 4
     Math.ceil(4.3);  // 5
     ```
   - **Raiz quadrada:**
     ```javascript
     Math.sqrt(16); // 4
     ```
   - **Potências:**
     ```javascript
     Math.pow(2, 3); // 8
     ```
   - **Mínimo e máximo:**
     ```javascript
     Math.min(1, 2, 3); // 1
     Math.max(1, 2, 3); // 3
     ```
   - **Gerar números aleatórios:**
     ```javascript
     Math.random(); // Número entre 0 e 1
     ```

---

### **Documentação Oficial:**
A documentação do `Math` está disponível no MDN Web Docs:  
[Documentação Math no MDN](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Global_Objects/Math)

