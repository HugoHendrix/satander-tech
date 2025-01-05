### **Lendo Arquivos JSON no JavaScript**

#### **1. Lendo JSON em Node.js**
Para ler um arquivo JSON, você pode usar o módulo `fs` do Node.js. 

```javascript
const fs = require('fs');

// Lendo arquivo JSON
fs.readFile('dados.json', 'utf8', (err, data) => {
  if (err) {
    console.error('Erro ao ler o arquivo:', err);
    return;
  }
  
  // Convertendo JSON string para um objeto
  const objeto = JSON.parse(data);
  console.log(objeto);
});
```

---

### **2. Convertendo JSON String para Objeto**
No JavaScript, você pode usar o método `JSON.parse()`.

#### **Exemplo:**
```javascript
const jsonString = '{"nome": "Maria", "idade": 30, "ativo": true}';
const objeto = JSON.parse(jsonString);

console.log(objeto.nome); // Maria
console.log(objeto.idade); // 30
```

---

### **3. Convertendo Objeto para JSON String**
Para converter um objeto JavaScript para JSON no formato string, use o método `JSON.stringify()`.

#### **Exemplo:**
```javascript
const objeto = {
  nome: "João",
  idade: 25,
  hobbies: ["futebol", "leitura"]
};

const jsonString = JSON.stringify(objeto);

console.log(jsonString);
// {"nome":"João","idade":25,"hobbies":["futebol","leitura"]}
```

#### **Opções do `JSON.stringify`**
Você pode passar argumentos adicionais para formatar ou personalizar a saída:
```javascript
const jsonStringFormatado = JSON.stringify(objeto, null, 2);
console.log(jsonStringFormatado);
// Saída formatada e indentada:
// {
//   "nome": "João",
//   "idade": 25,
//   "hobbies": [
//     "futebol",
//     "leitura"
//   ]
// }
```

---

### **Resumo: JSON Manipulação no JavaScript**

| **Tarefa**                           | **Método**        |
|--------------------------------------|-------------------|
| Lendo JSON String do arquivo         | `fs.readFile`     |
| Convertendo JSON String para Objeto  | `JSON.parse()`    |
| Convertendo Objeto para JSON String  | `JSON.stringify()`|

