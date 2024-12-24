# Tags de Formatação de Texto

### **Diferença entre `<b>` (bold) e `<strong>`**
Ambas tornam o texto em **negrito**, mas têm significados diferentes:
- **`<b>`**: Usada apenas para estilização visual, sem significado semântico.
  ```html
  <p>Este texto está em <b>negrito</b>.</p>
  ```
- **`<strong>`**: Indica importância ou urgência, com significado semântico (lida por leitores de tela).
  ```html
  <p>Este texto tem <strong>importância</strong>.</p>
  ```

---

### **Diferença entre `<i>` e `<em>`**
Ambas aplicam **itálico**, mas também têm significados distintos:
- **`<i>`**: Usada para estilização visual, sem significado adicional.
  ```html
  <p>Este texto está em <i>itálico</i>.</p>
  ```
- **`<em>`**: Indica ênfase semântica (enfatizado por leitores de tela).
  ```html
  <p>Este texto tem <em>ênfase</em>.</p>
  ```

---

### **Tag `<u>` e `text-decoration: underline`**
- **`<u>`**: Adiciona **sublinhado** ao texto, mas deve ser usada apenas em casos específicos, como nomes próprios ou erros ortográficos.
  ```html
  <p>Este texto está <u>sublinhado</u>.</p>
  ```
- **`text-decoration: underline`**: Substitui o `<u>` no CSS, permitindo mais controle de estilização.
  ```html
  <p style="text-decoration: underline;">Texto sublinhado com CSS.</p>
  ```

---

### **Tag `<s>`**
Adiciona um **traço sobre o texto**, indicando algo removido, incorreto ou obsoleto.
```html
<p>Este texto está <s>desatualizado</s>.</p>
```

---

### **Tag `<mark>`**
Destaca o texto como se fosse marcado com um marca-texto.
```html
<p>Este texto está <mark>destacado</mark>.</p>
```

---

### **Tag `<pre>`**
Preserva a **formatação original** do texto, incluindo quebras de linha e espaços.
```html
<pre>
Texto com
  espaçamento e
    quebras de linha.
</pre>
```

---

### **Tag `<code>`**
Indica um trecho de **código de programação**. É geralmente usado dentro de `<pre>` ou em inline.
```html
<p>Use a tag <code>&lt;html&gt;</code> para definir um documento HTML.</p>
```

---

### **Tag `<blockquote>`**
Indica uma **citação longa** de outro texto ou fonte. Pode incluir o atributo `cite` com o URL da origem.
```html
<blockquote cite="https://www.exemplo.com">
  Esta é uma citação de um texto importante.
</blockquote>
```

---

### **Tag `<sub>`**
Representa texto em **subscrito** (abaixo da linha base).
```html
<p>H<sub>2</sub>O é a fórmula química da água.</p>
```

---

### **Tag `<sup>`**
Representa texto em **sobrescrito** (acima da linha base).
```html
<p>2<sup>2</sup> = 4</p>
```
