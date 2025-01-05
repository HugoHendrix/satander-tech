
### **Programação Paralela**
Refere-se à execução de múltiplas tarefas ao mesmo tempo, aproveitando múltiplos núcleos de CPU. Embora o JavaScript seja single-threaded por padrão, algumas operações, como I/O, podem ser delegadas a threads separadas por meio do **Event Loop**.

---

### **Programação Assíncrona**
No JavaScript, o assincronismo permite que o código inicie uma tarefa e continue executando sem esperar que ela termine. Isso melhora a performance em operações demoradas, como chamadas de API ou leitura de arquivos.

---

### **Assincronismo: Leitura de Arquivo**
No Node.js, a leitura assíncrona de arquivos pode ser feita assim:
```javascript
const fs = require('fs');

fs.readFile('arquivo.txt', 'utf8', (err, data) => {
  if (err) {
    console.error("Erro ao ler o arquivo:", err);
    return;
  }
  console.log("Conteúdo do arquivo:", data);
});
```

---

### **Callbacks**
São funções passadas como argumento para outras funções e executadas quando a tarefa é concluída.
```javascript
function saudacao(nome, callback) {
  console.log(`Olá, ${nome}!`);
  callback();
}

saudacao("João", () => {
  console.log("Seja bem-vindo!");
});
```

---

### **`setTimeout`**
Cria um atraso antes de executar uma função.
```javascript
setTimeout(() => {
  console.log("Executado após 2 segundos!");
}, 2000);
```

---

### **Promises**
Promises representam operações assíncronas com três estados:
- **Pending:** Aguardando execução.
- **Fulfilled:** Concluído com sucesso.
- **Rejected:** Ocorreu um erro.

#### **Exemplo com `fetch`**
```javascript
fetch('https://api.example.com/dados')
  .then(response => response.json())
  .then(data => console.log(data))
  .catch(error => console.error("Erro:", error))
  .finally(() => console.log("Operação concluída"));
```

---

### **`async` / `await`**
Permite trabalhar com código assíncrono como se fosse síncrono.

#### **Exemplo**
```javascript
async function buscarDados() {
  try {
    const response = await fetch('https://api.example.com/dados');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error("Erro:", error);
  }
}

buscarDados();
```

---

### **Callback Hell**
Ocorre quando muitos callbacks são aninhados, tornando o código difícil de ler e manter.
```javascript
fs.readFile('arquivo1.txt', 'utf8', (err, data1) => {
  if (err) throw err;
  fs.readFile('arquivo2.txt', 'utf8', (err, data2) => {
    if (err) throw err;
    console.log(data1, data2);
  });
});
```

**Solução:** Use Promises ou `async`/`await`.


