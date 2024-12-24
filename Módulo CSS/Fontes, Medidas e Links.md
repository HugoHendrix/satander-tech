### **Fontes no CSS**
Fontes determinam o estilo visual do texto, e o CSS oferece várias propriedades para controlá-las.

**Propriedades principais:**
1. **`font-family`**: Define o tipo da fonte. É recomendado fornecer uma lista de fontes, da mais específica para a mais genérica (fallback).
   ```css
   body {
     font-family: 'Arial', 'Helvetica', sans-serif;
   }
   ```

2. **`font-size`**: Define o tamanho da fonte. Pode ser em **px**, **em**, **rem**, **%**, ou **vw/vh**.
   ```css
   p {
     font-size: 16px;
   }
   ```

3. **`font-style`**: Altera o estilo para itálico, normal, ou oblíquo.
   ```css
   em {
     font-style: italic;
   }
   ```

4. **`font-weight`**: Controla a espessura do texto, de `100` (fino) a `900` (grosso), ou com palavras-chave como `normal` ou `bold`.
   ```css
   h1 {
     font-weight: bold;
   }
   ```

5. **`letter-spacing`**: Ajusta o espaçamento entre letras.
   ```css
   h2 {
     letter-spacing: 2px;
   }
   ```

6. **`line-height`**: Define o espaçamento entre linhas.
   ```css
   p {
     line-height: 1.5;
   }
   ```

---

### **Medidas no CSS**
Medidas definem dimensões de elementos (largura, altura, margens, etc.). Podem ser absolutas ou relativas.

1. **Medidas Absolutas:**
   - **px (pixels):** Tamanho fixo independente do ambiente.
     ```css
     div {
       width: 200px;
     }
     ```
   - **cm, mm, in:** Usados raramente.

2. **Medidas Relativas:**
   - **% (porcentagem):** Baseado no tamanho do elemento pai.
     ```css
     div {
       width: 50%;
     }
     ```
   - **em:** Relativo ao tamanho da fonte do elemento pai.
     ```css
     p {
       font-size: 1.2em; /* 120% do tamanho da fonte do pai */
     }
     ```
   - **rem:** Relativo ao tamanho da fonte raiz (`html`).
     ```css
     h1 {
       font-size: 2rem; /* 2x o tamanho da fonte do <html> */
     }
     ```
   - **vw e vh (viewport width/height):** Relativo à largura/altura da tela.
     ```css
     section {
       width: 80vw;
       height: 50vh;
     }
     ```

---

### **Links no CSS**
Links são estilizados usando o seletor de pseudoclasse `a`.

**Pseudoclasses principais:**
1. **`a:link`**: Link normal (não visitado).
2. **`a:visited`**: Link visitado.
3. **`a:hover`**: Quando o cursor passa sobre o link.
4. **`a:active`**: Quando o link é clicado.

**Exemplo básico:**
```css
a {
  text-decoration: none; /* Remove o sublinhado */
  color: blue;
}

a:hover {
  color: darkblue;
}

a:visited {
  color: purple;
}

a:active {
  color: red;
}
```

**Dica para botões de links:**
Você pode transformar links em botões estilizados:
```css
a {
  display: inline-block;
  background-color: #0056b3;
  color: white;
  text-decoration: none;
  padding: 10px 20px;
  border-radius: 5px;
  transition: background-color 0.3s;
}

a:hover {
  background-color: #003d80;
}
```

---

### **Exemplo Prático Combinando Fontes, Medidas e Links**
```css
body {
  font-family: 'Roboto', sans-serif;
  font-size: 16px;
  line-height: 1.6;
  color: #333;
}

h1 {
  font-size: 2.5rem;
  font-weight: bold;
  text-align: center;
  margin-bottom: 20px;
}

p {
  font-size: 1rem;
  line-height: 1.8;
  margin-bottom: 15px;
}

a {
  color: #0056b3;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
```
