### **Listas**
O CSS permite personalizar tanto **listas ordenadas (`<ol>`)** quanto **não ordenadas (`<ul>`)**.

**Propriedades principais:**
1. **`list-style-type`**: Define o tipo de marcador.
   ```css
   ul {
     list-style-type: square;
   }

   ol {
     list-style-type: decimal-leading-zero; /* 01, 02, 03... */
   }
   ```

2. **`list-style-position`**: Define a posição do marcador.
   - `inside`: O marcador fica dentro da margem do item.
   - `outside`: O marcador fica fora da margem.
   ```css
   ul {
     list-style-position: inside;
   }
   ```

3. **`list-style-image`**: Usa uma imagem personalizada como marcador.
   ```css
   ul {
     list-style-image: url('marker.png');
   }
   ```

---

### **Tabelas**
O CSS ajuda a estilizar tabelas criadas com `<table>`, `<tr>`, `<th>`, `<td>`.

**Propriedades principais:**
1. **Bordas:**
   ```css
   table, th, td {
     border: 1px solid black;
     border-collapse: collapse; /* Remove bordas duplicadas */
   }
   ```

2. **Espaçamento e preenchimento:**
   ```css
   td {
     padding: 10px;
     text-align: center; /* Centraliza o texto */
   }
   ```

3. **Zebra stripe (linhas alternadas):**
   ```css
   tr:nth-child(even) {
     background-color: #f2f2f2;
   }
   ```

---

### **Box Model**
O Box Model é o modelo que define como os elementos HTML são renderizados, com quatro áreas:
1. **Conteúdo (`content`)**: O conteúdo real.
2. **Preenchimento (`padding`)**: Espaço entre o conteúdo e a borda.
3. **Borda (`border`)**: Envolve o preenchimento.
4. **Margem (`margin`)**: Espaço entre a borda do elemento e outros elementos.

**Propriedades principais:**
```css
div {
  width: 200px;
  padding: 10px;
  border: 5px solid black;
  margin: 15px;
}
```

**Visualização:**
- Largura total = `content` + `padding` + `border` + `margin`.

---

### **Border-box**
Por padrão, a largura de um elemento não inclui `padding` e `border`. A propriedade `box-sizing: border-box;` muda isso, incluindo `padding` e `border` na largura total.

**Exemplo:**
```css
div {
  width: 200px;
  box-sizing: border-box; /* Inclui borda e preenchimento */
  padding: 10px;
  border: 5px solid black;
}
```

---

### **Pseudoclasses: `first-child` e `nth-child`**
1. **`first-child`**: Aplica estilos ao primeiro elemento filho.
   ```css
   p:first-child {
     color: blue;
   }
   ```

2. **`nth-child`**: Aplica estilos com base na posição do elemento filho.
   - `nth-child(even)`: Elementos pares.
   - `nth-child(odd)`: Elementos ímpares.
   - `nth-child(n)`: Combinação personalizada.
   ```css
   li:nth-child(3) {
     font-weight: bold;
   }

   tr:nth-child(2n) {
     background-color: #f9f9f9; /* Linhas pares */
   }
   ```

---

### **Display**
A propriedade `display` controla como os elementos são exibidos na página.

**Principais valores:**
1. **`block`**: Ocupa toda a largura disponível (ex.: `<div>`).
   ```css
   div {
     display: block;
   }
   ```

2. **`inline`**: Ocupa apenas o espaço necessário (ex.: `<span>`).
   ```css
   span {
     display: inline;
   }
   ```

3. **`inline-block`**: Como `inline`, mas permite dimensões (largura e altura).
   ```css
   button {
     display: inline-block;
     width: 100px;
     height: 50px;
   }
   ```

4. **`none`**: Esconde o elemento.
   ```css
   div {
     display: none;
   }
   ```

5. **`flex`**: Layout flexível para organizar elementos.
   ```css
   div {
     display: flex;
     justify-content: center;
     align-items: center;
   }
   ```

6. **`grid`**: Sistema de layout baseado em grade.
   ```css
   div {
     display: grid;
     grid-template-columns: 1fr 1fr 1fr; /* Três colunas iguais */
   }
   ```

---

### **Exemplo Prático Combinado**
```css
body {
  font-family: 'Arial', sans-serif;
}

ul {
  list-style-type: square;
  padding: 0;
}

table {
  width: 100%;
  border-collapse: collapse;
}

th, td {
  padding: 10px;
  text-align: left;
  border: 1px solid #ddd;
}

tr:nth-child(even) {
  background-color: #f9f9f9;
}

div {
  display: flex;
  justify-content: space-around;
  align-items: center;
  border: 2px solid black;
  padding: 20px;
  margin: 20px;
  box-sizing: border-box;
}
```

