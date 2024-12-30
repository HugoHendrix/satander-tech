### **Seletores no CSS**
Seletores permitem aplicar estilos a elementos específicos no HTML.

**Tipos Comuns de Seletores:**

1. **Seletores Simples:**
   - **Elemento (tag):** Aplica a todas as tags do tipo especificado.
     ```css
     p {
       color: blue;
     }
     ```
   - **Classe (`.`):** Aplica a elementos com uma classe específica.
     ```css
     .highlight {
       background-color: yellow;
     }
     ```
   - **ID (`#`):** Aplica a elementos com um ID específico.
     ```css
     #main {
       font-size: 20px;
     }
     ```

2. **Seletores Combinados:**
   - **Descendente:** Seleciona elementos dentro de outro elemento.
     ```css
     div p {
       color: red;
     }
     ```
   - **Filho (`>`):** Seleciona apenas os filhos diretos.
     ```css
     ul > li {
       list-style: none;
     }
     ```
   - **Irmão adjacente (`+`):** Seleciona o próximo irmão imediato.
     ```css
     h1 + p {
       font-style: italic;
     }
     ```

3. **Pseudoclasses:**
   - **Exemplos úteis:**
     ```css
     a:hover {
       color: green;
     }
     li:first-child {
       font-weight: bold;
     }
     ```

4. **Atributos:**
   - **Estilizar com base em atributos:**
     ```css
     input[type="text"] {
       border: 1px solid gray;
     }
     ```

---

### **Data-Attributes**
Data-attributes são atributos personalizados usados para armazenar dados em elementos HTML.

**Como usar no HTML:**
```html
<div data-user="123" data-role="admin">John Doe</div>
```

**Como selecionar no CSS:**
- `[data-atributo="valor"]`: Seleciona elementos com um valor específico.
  ```css
  [data-role="admin"] {
    color: red;
  }
  ```

- `[data-atributo^="prefixo"]`: Seleciona elementos cujo valor começa com algo.
  ```css
  [data-user^="1"] {
    font-weight: bold;
  }
  ```

---

### **Responsividade**
A responsividade adapta o layout para diferentes tamanhos de tela.

1. **Unidades Relativas:**
   - **`%`**: Relativo ao elemento pai.
   - **`em/rem`**: Baseado no tamanho da fonte.
   - **`vw/vh`**: Relativo à largura/altura da viewport.

   ```css
   div {
     width: 50%;
     font-size: 2vw;
   }
   ```

2. **Media Queries:**
   - Permite aplicar estilos específicos para diferentes tamanhos de tela.
     ```css
     @media (max-width: 768px) {
       body {
         font-size: 14px;
       }
     }
     ```

3. **Design Responsivo com Flexbox:**
   ```css
   .container {
     display: flex;
     flex-wrap: wrap;
   }

   .item {
     flex: 1 1 200px; /* Cresce e encolhe com tamanho mínimo de 200px */
     margin: 10px;
   }
   ```

---

### **Animações**
Animações permitem criar efeitos visuais dinâmicos.

1. **Transições (`transition`):**
   - Aplica mudanças suaves a propriedades CSS.
     ```css
     button {
       background-color: blue;
       transition: background-color 0.3s ease;
     }

     button:hover {
       background-color: green;
     }
     ```

2. **Animações com `@keyframes`:**
   - Define etapas de uma animação.
     ```css
     @keyframes fadeIn {
       from {
         opacity: 0;
       }
       to {
         opacity: 1;
       }
     }

     .fade {
       animation: fadeIn 2s ease-in-out;
     }
     ```

3. **Propriedades de animação:**
   - `animation-name`: Nome da animação definida no `@keyframes`.
   - `animation-duration`: Duração da animação.
   - `animation-timing-function`: Tipo de curva de movimento (`ease`, `linear`, etc.).
   - `animation-iteration-count`: Quantas vezes repetir a animação (`infinite` para contínua).

   **Exemplo Completo:**
   ```css
   .box {
     width: 100px;
     height: 100px;
     background-color: red;
     animation: slide 3s ease-in-out infinite;
   }

   @keyframes slide {
     0% {
       transform: translateX(0);
     }
     50% {
       transform: translateX(100px);
     }
     100% {
       transform: translateX(0);
     }
   }
   ```

4. **Transformações (`transform`):**
   - Usado em conjunto com animações ou transições.
     ```css
     .rotate {
       transform: rotate(45deg);
     }

     .scale {
       transform: scale(1.5);
     }
     ```

---

### **Exemplo Combinado de Responsividade e Animações**
```css
@keyframes grow {
  from {
    transform: scale(1);
  }
  to {
    transform: scale(1.2);
  }
}

.card {
  width: 300px;
  height: 200px;
  background-color: lightblue;
  margin: 10px auto;
  animation: grow 2s infinite alternate;
}

@media (max-width: 768px) {
  .card {
    width: 90%;
  }
}
```

**HTML Associado:**
```html
<div class="card">Este é um cartão responsivo e animado!</div>
```

