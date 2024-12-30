### **O que é Flexbox?**
O **Flexbox** é um sistema de layout do CSS projetado para facilitar o alinhamento, espaçamento e organização de elementos em um contêiner flexível.

---

### **Propriedade Principal: `display: flex`**
- Aplica o modo flexível a um contêiner.
- Os itens dentro do contêiner se tornam "itens flexíveis" e podem ser organizados de várias maneiras.

**Exemplo básico:**
```css
.container {
  display: flex;
}
```

---

### **Propriedades do Contêiner Flex**
1. **`flex-direction`**: Define a direção dos itens no contêiner.
   - `row` (padrão): Alinha os itens na horizontal, da esquerda para a direita.
   - `row-reverse`: Horizontal, da direita para a esquerda.
   - `column`: Alinha os itens na vertical, de cima para baixo.
   - `column-reverse`: Vertical, de baixo para cima.

   ```css
   .container {
     flex-direction: column;
   }
   ```

2. **`justify-content`**: Alinha os itens ao longo do eixo principal.
   - `flex-start` (padrão): Alinha os itens no início.
   - `flex-end`: Alinha os itens no final.
   - `center`: Centraliza os itens.
   - `space-between`: Distribui os itens com espaçamento entre eles.
   - `space-around`: Adiciona espaçamento ao redor de cada item.
   - `space-evenly`: Espaçamento igual entre os itens.

   ```css
   .container {
     justify-content: space-around;
   }
   ```

3. **`align-items`**: Alinha os itens ao longo do eixo cruzado.
   - `stretch` (padrão): Itens esticam para preencher o contêiner.
   - `flex-start`: Alinha os itens no início do eixo cruzado.
   - `flex-end`: Alinha os itens no final do eixo cruzado.
   - `center`: Centraliza os itens no eixo cruzado.
   - `baseline`: Alinha os itens pela linha de base do texto.

   ```css
   .container {
     align-items: center;
   }
   ```

4. **`flex-wrap`**: Define se os itens devem quebrar linha ou permanecer em uma única linha.
   - `nowrap` (padrão): Itens permanecem em uma única linha.
   - `wrap`: Itens quebram linha se necessário.
   - `wrap-reverse`: Itens quebram linha, mas em ordem inversa.

   ```css
   .container {
     flex-wrap: wrap;
   }
   ```

5. **`align-content`**: Alinha linhas em contêineres com `flex-wrap`.
   - Funciona como `justify-content`, mas para múltiplas linhas.

   ```css
   .container {
     align-content: space-between;
   }
   ```

---

### **Propriedades dos Itens Flexíveis**
1. **`order`**: Define a ordem de exibição dos itens.
   ```css
   .item-1 {
     order: 2;
   }
   .item-2 {
     order: 1;
   }
   ```

2. **`flex-grow`**: Controla quanto espaço extra o item deve ocupar.
   ```css
   .item {
     flex-grow: 1; /* Ocupa espaço proporcional */
   }
   ```

3. **`flex-shrink`**: Define como o item reduz seu tamanho quando necessário.
   ```css
   .item {
     flex-shrink: 0; /* Não reduz de tamanho */
   }
   ```

4. **`flex-basis`**: Define o tamanho inicial do item.
   ```css
   .item {
     flex-basis: 200px;
   }
   ```

5. **`align-self`**: Alinha um item individualmente, ignorando `align-items`.
   ```css
   .item {
     align-self: flex-end;
   }
   ```

---

### **Exemplo Prático com Flexbox**
```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  height: 200px;
  border: 2px solid #ccc;
  padding: 10px;
}

.item {
  background-color: #007bff;
  color: white;
  padding: 20px;
  margin: 5px;
  flex-grow: 1; /* Todos os itens crescem igualmente */
  text-align: center;
}
```

**HTML associado:**
```html
<div class="container">
  <div class="item">Item 1</div>
  <div class="item">Item 2</div>
  <div class="item">Item 3</div>
</div>
```

---

### **Dicas para Alinhamentos**
#### **Centralizar um elemento horizontal e verticalmente com Flexbox:**
```css
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; /* Altura total da janela */
}
```

#### **Criar um layout responsivo com Flexbox:**
```css
.container {
  display: flex;
  flex-wrap: wrap;
}

.item {
  flex: 1 1 200px; /* Cresce, encolhe, e define um tamanho base */
  margin: 10px;
}
```

