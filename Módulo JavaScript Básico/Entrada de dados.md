
### **Entrada de Dados em JavaScript:**
1. **`window.prompt`:**  
   Permite obter entrada do usuário diretamente na interface do navegador.  
   Exemplo:  
   ```javascript
   let nome = window.prompt("Qual é o seu nome?");
   console.log(`Olá, ${nome}!`);
   ```

2. **Outras formas de entrada de dados:**
   - **HTML e `input`:**  
     Combine com JavaScript para capturar valores:  
     ```html
     <input type="text" id="entrada" />
     <button onclick="capturar()">Enviar</button>
     <script>
       function capturar() {
         let valor = document.getElementById("entrada").value;
         console.log(`Você digitou: ${valor}`);
       }
     </script>
     ```

   - **Node.js com `readline-sync`:**  
     Instale a biblioteca e use no terminal:  
     ```bash
     npm install readline-sync
     ```
     Exemplo:  
     ```javascript
     const readline = require('readline-sync');
     let nome = readline.question("Qual é o seu nome? ");
     console.log(`Olá, ${nome}!`);
     ```

---

### **Outras Funcionalidades do Objeto `window`:**
- **Alerta:**  
  ```javascript
  window.alert("Mensagem de alerta!");
  ```
- **Confirmação:**  
  ```javascript
  let confirma = window.confirm("Você confirma?");
  console.log(confirma ? "Sim" : "Não");
  ```
- **Manipulação do navegador:**  
  - `window.open(url)`: Abre uma nova aba.  
  - `window.location`: Obtém ou altera a URL atual.  

---

### **`npm` e Bibliotecas:**
1. **O que é `npm`:**  
   O Node Package Manager (`npm`) gerencia pacotes (bibliotecas e ferramentas) para JavaScript e Node.js.

2. **Arquivos `node_modules` e `package.json`:**
   - **`node_modules`:** Pasta onde as dependências instaladas estão localizadas.  
   - **`package.json`:** Lista as dependências, scripts e metadados do projeto.  
     Exemplo de criação:
     ```bash
     npm init -y
     ```

3. **Como usar uma biblioteca:**
   - Instale a biblioteca:  
     ```bash
     npm install biblioteca-nome
     ```
   - Importe e use:  
     ```javascript
     const biblioteca = require('biblioteca-nome');
     ```

---

### **Outras Bibliotecas Recomendadas para Iniciantes:**
1. **`moment`:** Manipulação de datas e horários.  
   ```bash
   npm install moment
   ```
   Exemplo:  
   ```javascript
   const moment = require('moment');
   console.log(moment().format('DD/MM/YYYY'));
   ```

2. **`chalk`:** Adiciona cores ao console.  
   ```bash
   npm install chalk
   ```
   Exemplo:  
   ```javascript
   const chalk = require('chalk');
   console.log(chalk.green("Texto verde!"));
   ```

3. **`axios`:** Para fazer requisições HTTP.  
   ```bash
   npm install axios
   ```
   Exemplo:  
   ```javascript
   const axios = require('axios');
   axios.get('https://api.example.com').then(response => console.log(response.data));
   ```


