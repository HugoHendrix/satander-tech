### **Estruturas de Controle de Fluxo Condicionais:**
As estruturas de controle de fluxo condicionais permitem que o programa tome decisões com base em condições.

#### **1. `if`, `else if`, `else`:**
Usado para verificar condições e executar blocos de código diferentes.
```javascript
let idade = 20;

if (idade >= 18) {
  console.log("Maior de idade");
} else {
  console.log("Menor de idade");
}
```

#### **2. Operador Ternário:**
Uma maneira curta de escrever condições simples.
```javascript
let resultado = idade >= 18 ? "Maior de idade" : "Menor de idade";
console.log(resultado);
```

#### **3. `switch`:**
Útil quando se tem várias opções baseadas em um único valor.
```javascript
let dia = "segunda";

switch (dia) {
  case "segunda":
    console.log("Início da semana!");
    break;
  case "sexta":
    console.log("Quase fim de semana!");
    break;
  default:
    console.log("Outro dia qualquer.");
}
```

---

### **Estruturas Condicionais:**
1. **Condicionais simples:**
   Usam apenas um `if`.
   ```javascript
   if (true) {
     console.log("Condição verdadeira");
   }
   ```

2. **Condicionais compostas:**
   Incluem `else` ou `else if` para mais cenários.
   ```javascript
   if (condicao1) {
     // Código
   } else if (condicao2) {
     // Código
   } else {
     // Código
   }
   ```

---

### **Escopo:**
O escopo define onde as variáveis estão acessíveis no código.

1. **Escopo Global:**
   Variáveis declaradas fora de funções estão disponíveis globalmente.
   ```javascript
   let global = "Disponível em todo lugar";
   ```

2. **Escopo de Função:**
   Variáveis declaradas dentro de funções só podem ser acessadas dentro delas.
   ```javascript
   function exemplo() {
     let local = "Apenas dentro desta função";
   }
   ```

3. **Escopo de Bloco:**
   Criado por blocos como `{}` com `let` ou `const`.
   ```javascript
   {
     let bloco = "Apenas dentro deste bloco";
   }
   ```

---

### **Identação:**
É a organização do código para torná-lo mais legível.

#### **Regras práticas:**
- Use dois espaços ou um tab para cada nível de bloco.
- Mantenha consistência no projeto.
- Exemplo:
  ```javascript
  if (condicao) {
    // Código identado
    console.log("Bloco de código");
  }
  ```

---

### **Boas Práticas com Nomes de Variáveis:**
1. **Seja descritivo:** O nome deve indicar a finalidade da variável.
   ```javascript
   let idadeUsuario = 25; // Bom
   let x = 25; // Ruim
   ```

2. **Use camelCase:**
   Comece com letra minúscula e capitalize palavras subsequentes.
   ```javascript
   let nomeCompleto;
   ```

3. **Evite nomes genéricos ou abreviações:**  
   Use nomes claros.
   ```javascript
   let contador; // Bom
   let c; // Ruim
   ```

4. **Não use palavras reservadas:**  
   Evite nomes como `class`, `return`, etc.

