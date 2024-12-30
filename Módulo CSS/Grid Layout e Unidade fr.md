### **Grid Layout e Unidade `fr` no CSS**

O **CSS Grid Layout** é um sistema de layout poderoso que organiza elementos em uma grade composta de linhas e colunas, proporcionando controle preciso sobre o posicionamento e dimensionamento.

---

### **Introdução ao Grid Layout**

1. **Propriedade Principal: `display: grid`**
   - Define o elemento como um contêiner de grade.
   ```css
   .container {
     display: grid;
   }
   ```

2. **Linhas e Colunas:**
   - Criadas com as propriedades `grid-template-rows` e `grid-template-columns`.
   ```css
   .container {
     grid-template-rows: 100px 200px;
     grid-template-columns: 1fr 2fr;
   }
   ```

---

### **Unidade `fr`**
- A unidade `fr` (fração) representa uma parte proporcional do espaço disponível no contêiner.
- É ideal para criar layouts flexíveis e responsivos.

**Exemplo Básico:**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr; /* 4 partes no total */
}
```
- A primeira e terceira colunas ocupam 1 fração cada.
- A segunda coluna ocupa 2 frações, ou seja, o dobro do espaço das outras.

---

### **Propriedades do Grid**

1. **`grid-template-rows` e `grid-template-columns`:**
   - Definem as dimensões da grade.
   ```css
   .container {
     grid-template-rows: 150px auto;
     grid-template-columns: 1fr 2fr 1fr;
   }
   ```

2. **`gap`:**
   - Define o espaçamento entre as linhas e colunas.
   ```css
   .container {
     gap: 10px; /* Espaçamento uniforme */
   }
   ```

3. **`grid-area`:**
   - Permite nomear áreas na grade para facilitar o layout.
   ```css
   .container {
     display: grid;
     grid-template-areas:
       "header header header"
       "sidebar content content"
       "footer footer footer";
   }

   .header {
     grid-area: header;
   }

   .sidebar {
     grid-area: sidebar;
   }

   .content {
     grid-area: content;
   }

   .footer {
     grid-area: footer;
   }
   ```

4. **`justify-items` e `align-items`:**
   - Controlam o alinhamento de conteúdo dentro das células.
     - `justify-items`: Alinha horizontalmente (`start`, `end`, `center`, `stretch`).
     - `align-items`: Alinha verticalmente.

---

### **Alocação de Itens na Grade**

1. **`grid-column` e `grid-row`:**
   - Especificam a posição e extensão de um item.
   ```css
   .item1 {
     grid-column: 1 / 3; /* Ocupa da 1ª à 2ª coluna */
     grid-row: 1 / 2;   /* Ocupa a 1ª linha */
   }
   ```

2. **`grid-auto-rows` e `grid-auto-columns`:**
   - Criam automaticamente dimensões para linhas ou colunas extras.
   ```css
   .container {
     grid-auto-rows: 100px;
   }
   ```

---

### **Exemplo Completo**
```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr; /* Três colunas proporcionais */
  grid-template-rows: 100px auto 100px; /* Três linhas */
  gap: 20px;
}

.item1 {
  grid-column: 1 / 4; /* Ocupa toda a linha */
}

.item2 {
  grid-column: 1 / 2;
}

.item3 {
  grid-column: 2 / 4;
  grid-row: 2 / 3;
}
```

**HTML Associado:**
```html
<div class="container">
  <div class="item1">Header</div>
  <div class="item2">Sidebar</div>
  <div class="item3">Content</div>
  <div class="item4">Footer</div>
</div>
```

---

### **Grid vs Flexbox**
- **Flexbox:** Melhor para layouts unidimensionais (linha ou coluna).
- **Grid:** Ideal para layouts bidimensionais (linhas e colunas).

---

### **Exemplo Responsivo com Grid e `fr`**
```css
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 20px;
}

.item {
  background-color: lightblue;
  padding: 20px;
  text-align: center;
}
```

**HTML Associado:**
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
  <div class="item">Item 4</div>
</div>
```

**Como funciona:**
- O `auto-fit` ajusta o número de colunas baseado no espaço disponível.
- O `minmax(200px, 1fr)` garante que cada coluna tenha pelo menos 200px, mas pode crescer proporcionalmente.

