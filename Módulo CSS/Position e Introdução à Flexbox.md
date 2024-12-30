
### **Position**
A propriedade `position` controla como um elemento é posicionado no documento ou em relação a outros elementos.

**Valores principais de `position`:**

1. **`static` (padrão):**
   - Os elementos seguem o fluxo normal do documento.
   - Sem comportamento especial.
   ```css
   div {
     position: static;
   }
   ```

2. **`relative`:**
   - O elemento é posicionado relativo à sua posição normal.
   - Pode usar as propriedades `top`, `right`, `bottom`, `left`.
   ```css
   div {
     position: relative;
     top: 10px; /* Move para baixo 10px */
     left: 20px; /* Move para a direita 20px */
   }
   ```

3. **`absolute`:**
   - Posiciona o elemento em relação ao ancestral mais próximo com `position: relative`, `absolute` ou `fixed`.
   - Se não houver, é posicionado em relação ao `<html>`.
   ```css
   div {
     position: absolute;
     top: 50px;
     right: 10px;
   }
   ```

4. **`fixed`:**
   - Posiciona o elemento em relação à viewport (a tela do usuário).
   - O elemento permanece fixo mesmo ao rolar a página.
   ```css
   div {
     position: fixed;
     bottom: 0;
     right: 0;
   }
   ```

5. **`sticky`:**
   - Combina características de `relative` e `fixed`.
   - O elemento se comporta como `relative` até atingir um limite especificado (usando `top`, `bottom`, etc.).
   ```css
   div {
     position: sticky;
     top: 10px; /* Fica preso ao topo após rolar 10px */
   }
   ```

---

### **Flexbox**
Flexbox (Flexible Box Layout) é uma técnica poderosa para criar layouts dinâmicos e responsivos. Ele organiza elementos dentro de um contêiner flexível.

**Propriedade principal:**
- `display: flex;`: Define que o elemento é um contêiner flexível.

**Propriedades do Contêiner (pai):**

1. **`flex-direction`:** Direção do eixo principal.
   - `row` (padrão): Da esquerda para a direita.
   - `row-reverse`: Da direita para a esquerda.
   - `column`: De cima para baixo.
   - `column-reverse`: De baixo para cima.
   ```css
   div {
     display: flex;
     flex-direction: row;
   }
   ```

2. **`justify-content`:** Alinha os itens no eixo principal.
   - `flex-start` (padrão): Início do eixo.
   - `flex-end`: Fim do eixo.
   - `center`: Centro.
   - `space-between`: Espaço igual entre os itens.
   - `space-around`: Espaço igual ao redor dos itens.
   ```css
   div {
     display: flex;
     justify-content: center;
   }
   ```

3. **`align-items`:** Alinha os itens no eixo cruzado.
   - `stretch` (padrão): Ocupa o eixo cruzado completamente.
   - `flex-start`: No início do eixo cruzado.
   - `flex-end`: No fim do eixo cruzado.
   - `center`: No centro do eixo cruzado.
   - `baseline`: Alinhados pela linha base do texto.
   ```css
   div {
     display: flex;
     align-items: center;
   }
   ```

4. **`flex-wrap`:** Controla se os itens devem quebrar linha.
   - `nowrap` (padrão): Sem quebra de linha.
   - `wrap`: Quebra linha se necessário.
   - `wrap-reverse`: Quebra linha na direção inversa.
   ```css
   div {
     display: flex;
     flex-wrap: wrap;
   }
   ```

---

**Propriedades dos Itens (filhos):**

1. **`flex`:** Define a capacidade de crescimento, encolhimento e tamanho base do item.
   - `flex: 1;` significa que o item pode crescer e ocupar o espaço disponível igualmente com os outros.
   ```css
   .item {
     flex: 1;
   }
   ```

2. **`align-self`:** Alinha individualmente um item no eixo cruzado, ignorando `align-items`.
   ```css
   .item {
     align-self: flex-end;
   }
   ```

3. **`order`:** Define a ordem dos itens.
   - O padrão é `0`. Valores negativos ou positivos alteram a ordem.
   ```css
   .item {
     order: 1;
   }
   ```

---

### **Exemplo Prático de Flexbox**
```html
<div class="flex-container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```

```css
.flex-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  background-color: #f4f4f9;
  padding: 20px;
}

.item {
  background-color: #0056b3;
  color: white;
  padding: 10px;
  margin: 5px;
  flex: 1;
  text-align: center;
  border-radius: 5px;
}
```

---

### **Exemplo Prático Combinando Position e Flexbox**
```html
<header class="sticky-header">
  <nav>
    <ul class="menu">
      <li>Home</li>
      <li>Sobre</li>
      <li>Contato</li>
    </ul>
  </nav>
</header>
<div class="content">
  <p>Conteúdo principal...</p>
</div>
```

```css
.sticky-header {
  position: sticky;
  top: 0;
  background-color: #282c34;
  padding: 10px 20px;
  z-index: 1000;
}

.menu {
  display: flex;
  justify-content: space-around;
  list-style: none;
  margin: 0;
  padding: 0;
}

.menu li {
  color: white;
  cursor: pointer;
}
```

Esse exemplo cria um menu que usa **Flexbox** para alinhamento e **Position Sticky** para fixar no topo ao rolar a página.

---

