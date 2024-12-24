
### **Cores no CSS**
As cores podem ser definidas de várias maneiras no CSS:
- **Palavras-chave:** Nomes de cores, como `red`, `blue`, `green`.
- **Valores Hexadecimais:** Exemplo: `#FF5733`.
- **Valores RGB:** Exemplo: `rgb(255, 87, 51)`.
- **Valores RGBA:** Inclui opacidade. Exemplo: `rgba(255, 87, 51, 0.5)`.
- **Valores HSL:** Matiz, Saturação e Luminosidade. Exemplo: `hsl(30, 100%, 50%)`.

**Propriedade principal:**
- `color`: Define a cor do texto.

**Exemplo:**
```css
h1 {
  color: #FF5733; /* Laranja em hexadecimal */
}
```

---

### **Background no CSS**
O background é o plano de fundo de um elemento e pode incluir cores, imagens ou gradientes.

**Propriedades principais:**
1. **`background-color`**: Define uma cor sólida de fundo.
   ```css
   div {
     background-color: lightblue;
   }
   ```
2. **`background-image`**: Adiciona uma imagem de fundo.
   ```css
   body {
     background-image: url('imagem.jpg');
   }
   ```
3. **`background-repeat`**: Define se a imagem de fundo será repetida.
   ```css
   body {
     background-repeat: no-repeat;
   }
   ```
4. **`background-position`**: Alinha a imagem de fundo.
   ```css
   body {
     background-position: center;
   }
   ```
5. **`background-size`**: Ajusta o tamanho da imagem.
   ```css
   body {
     background-size: cover;
   }
   ```

**Exemplo completo:**
```css
section {
  background-color: #282c34;
  background-image: url('texture.png');
  background-repeat: no-repeat;
  background-position: top right;
  background-size: 50px 50px;
}
```

---

### **Textos no CSS**
O CSS oferece diversas propriedades para estilizar o texto.

**Propriedades principais:**
1. **`font-family`**: Define a fonte.
   ```css
   p {
     font-family: 'Arial', sans-serif;
   }
   ```
2. **`font-size`**: Define o tamanho da fonte.
   ```css
   h2 {
     font-size: 18px;
   }
   ```
3. **`font-weight`**: Define a espessura do texto.
   ```css
   strong {
     font-weight: bold;
   }
   ```
4. **`line-height`**: Define o espaçamento entre linhas.
   ```css
   p {
     line-height: 1.5;
   }
   ```
5. **`text-align`**: Alinha o texto.
   ```css
   h1 {
     text-align: center;
   }
   ```
6. **`text-decoration`**: Adiciona ou remove sublinhados, linhas ou estilos decorativos.
   ```css
   a {
     text-decoration: none;
   }
   ```
7. **`text-transform`**: Controla a capitalização.
   ```css
   h2 {
     text-transform: uppercase;
   }
   ```

**Exemplo completo:**
```css
article {
  font-family: 'Georgia', serif;
  font-size: 16px;
  font-weight: 400;
  line-height: 1.8;
  text-align: justify;
  color: #333;
}
```

---

### **Combinação de Estilos**
Você pode combinar cores, backgrounds e textos para criar uma página estilosa. Exemplo:

```css
body {
  background-color: #f4f4f9;
  color: #333;
  font-family: 'Roboto', sans-serif;
}

h1 {
  color: #0056b3;
  text-align: center;
  text-transform: uppercase;
}

button {
  background-color: #0056b3;
  color: white;
  font-size: 16px;
  padding: 10px 20px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
```
