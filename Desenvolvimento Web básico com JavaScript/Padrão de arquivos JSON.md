
### **JSON (JavaScript Object Notation)**

#### **Por que tem esse nome?**
JSON significa **JavaScript Object Notation**. Foi criado como um formato leve para troca de dados, inspirado na sintaxe de objetos do JavaScript. Apesar disso, JSON é independente de linguagem e amplamente utilizado em APIs, configuração de sistemas, entre outros.

---

### **Como usar JSON?**
JSON é usado para armazenar e trocar dados de forma estruturada. Exemplos comuns incluem APIs, configurações de aplicativos e persistência de dados.

#### **Exemplo de JSON:**
```json
{
  "nome": "João",
  "idade": 25,
  "hobbies": ["futebol", "leitura", "viajar"],
  "ativo": true
}
```

---

### **Estrutura do JSON**
1. **Objetos:** Envolvidos por `{}`, contendo pares `chave: valor`.
   ```json
   { "nome": "Maria" }
   ```
2. **Arrays:** Envolvidos por `[]`, contendo valores ou objetos.
   ```json
   [ "maçã", "banana", "laranja" ]
   ```
3. **Tipos de Valores Suportados:**
   - Strings: `"texto"`
   - Números: `123`, `12.5`
   - Booleanos: `true`, `false`
   - Nulo: `null`
   - Arrays
   - Objetos

---

### **Vantagens do JSON**
1. **Leve e Simples:** Ideal para troca de dados.
2. **Compatibilidade:** Suportado em diversas linguagens.
3. **Legibilidade:** Fácil de entender e escrever.
4. **Eficiente:** Facilita a integração entre sistemas.

---

### **Parsing: Como manipular JSON no JavaScript**
1. **Conversão de JSON para Objeto:**
   Use `JSON.parse()` para transformar uma string JSON em um objeto.
   ```javascript
   const jsonData = '{"nome": "João", "idade": 30}';
   const obj = JSON.parse(jsonData);
   console.log(obj.nome); // João
   ```

2. **Conversão de Objeto para JSON:**
   Use `JSON.stringify()` para transformar um objeto em uma string JSON.
   ```javascript
   const pessoa = { nome: "Maria", idade: 25 };
   const jsonString = JSON.stringify(pessoa);
   console.log(jsonString); // {"nome":"Maria","idade":25}
   ```

---

### **npm e npx**
1. **npm (Node Package Manager):**
   Gerenciador de pacotes usado para instalar bibliotecas e ferramentas no ecossistema Node.js.
   ```bash
   npm install nome-pacote
   ```

2. **npx:**
   Executa pacotes diretamente sem precisar instalá-los globalmente.
   ```bash
   npx nome-comando
   ```

---

### **Padronização com `.prettierrc`**
O Prettier é uma ferramenta para formatar automaticamente o código. O arquivo `.prettierrc` permite personalizar as regras de formatação.

#### **Exemplo de `.prettierrc`:**
```json
{
  "semi": true,
  "singleQuote": true,
  "tabWidth": 2
}
```

---

### **Padronização com ESLint**
O ESLint ajuda a identificar e corrigir problemas no código com base em regras configuráveis.

#### **Exemplo de Configuração `.eslintrc.json`:**
```json
{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": "eslint:recommended",
  "rules": {
    "indent": ["error", 2],
    "quotes": ["error", "single"],
    "semi": ["error", "always"]
  }
}
```

---

### **Links para documentação e estudos**
1. **JSON Oficial:** [https://www.json.org/json-en.html](https://www.json.org/json-en.html)
2. **MDN JSON:** [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/JSON)
3. **npm:** [https://www.npmjs.com/](https://www.npmjs.com/)
4. **Prettier:** [https://prettier.io/](https://prettier.io/)
5. **ESLint:** [https://eslint.org/](https://eslint.org/)

