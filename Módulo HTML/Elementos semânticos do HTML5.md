# **Elementos Semânticos do HTML5**

---

### **O que são Elementos Semânticos?**
Elementos semânticos possuem significados claros e específicos para navegadores e desenvolvedores, descrevendo a função ou o conteúdo de uma seção. Eles melhoram a **acessibilidade**, o **SEO** e a **manutenção** do código.

---

### **Boas Práticas com Elementos Semânticos**
1. **Use tags semânticas sempre que possível**: Substitua `<div>` e `<span>` por elementos como `<header>`, `<article>`, e `<footer>` para um código mais descritivo.
2. **Organize hierarquicamente**: Estruture o conteúdo usando `<main>`, `<section>` e `<article>` de forma lógica.
3. **Acessibilidade**:
   - Use atributos ARIA quando necessário para melhorar a navegação assistiva.
   - Certifique-se de que os títulos (`<h1>` a `<h6>`) sejam usados em ordem lógica.
4. **SEO**:
   - Marque conteúdos importantes com `<article>` e `<header>` para ajudar os mecanismos de busca a entender o propósito da página.
5. **Evite redundância**:
   - Não use elementos semânticos para fins puramente visuais.

---

### **Para que servem os elementos semânticos?**
1. **Melhoria na Acessibilidade**: Ajuda leitores de tela e tecnologias assistivas a interpretar a página.
2. **SEO**: Os mecanismos de busca priorizam conteúdos estruturados e marcados corretamente.
3. **Manutenção do Código**: Um código bem estruturado é mais fácil de entender e modificar.
4. **Boas Práticas de Desenvolvimento**: Torna o HTML mais moderno e padronizado.

---

### **Principais Tags Semânticas**
| Tag             | Função                                                                 |
|------------------|------------------------------------------------------------------------|
| `<header>`       | Cabeçalho da página ou de uma seção.                                  |
| `<nav>`          | Área de navegação com links importantes.                              |
| `<main>`         | Conteúdo principal da página (apenas um por documento).               |
| `<section>`      | Agrupa conteúdo relacionado, usado para dividir a página em seções.   |
| `<article>`      | Conteúdo independente, como posts de blog ou artigos.                 |
| `<aside>`        | Informações complementares, como barras laterais.                     |
| `<footer>`       | Rodapé da página ou de uma seção, contém informações como copyright.  |
| `<figure>`       | Agrupa imagens ou ilustrações com legendas.                           |
| `<figcaption>`   | Adiciona legenda a um elemento `<figure>`.                            |
| `<time>`         | Representa datas ou horários.                                         |
| `<mark>`         | Destaca textos importantes.                                           |
| `<summary>`      | Título visível em um elemento `<details>`.                            |
| `<details>`      | Adiciona conteúdo que pode ser expandido ou contraído pelo usuário.   |

---

### **ARIA (Accessible Rich Internet Applications)**
**ARIA** é um conjunto de atributos para melhorar a acessibilidade de elementos que não possuem comportamento semântico nativo. É essencial para interfaces interativas.

#### **Principais Usos do ARIA**
1. **Tornar elementos não semânticos acessíveis**: Por exemplo, adicionar roles em `<div>` e `<span>`.
2. **Comunicar estados dinâmicos**: Indicar estados como "expandido", "colapsado", ou "desabilitado".
3. **Compatibilidade com leitores de tela**: Ajuda na navegação assistiva.

#### **Atributos ARIA Comuns**
| Atributo        | Descrição                                       |
|------------------|------------------------------------------------|
| `role`           | Define o papel de um elemento (`button`, `menu`). |
| `aria-label`     | Fornece uma descrição acessível para o elemento. |
| `aria-labelledby`| Referencia outro elemento para fornecer um rótulo. |
| `aria-hidden`    | Indica se um elemento deve ser ignorado por leitores de tela. |
| `aria-expanded`  | Indica se um elemento expansível está aberto ou fechado. |
| `aria-disabled`  | Marca um elemento como desabilitado.           |
| `aria-live`      | Define a importância de notificações dinâmicas. |

---

### **Exemplo Combinando Tags Semânticas e ARIA**
```html
<header role="banner">
  <nav role="navigation" aria-label="Menu Principal">
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">Sobre</a></li>
      <li><a href="#contact">Contato</a></li>
    </ul>
  </nav>
</header>

<main>
  <section>
    <article>
      <h1>Notícia Importante</h1>
      <p>Conteúdo do artigo...</p>
    </article>
  </section>
</main>

<footer role="contentinfo">
  <p>&copy; 2024 Minha Empresa</p>
</footer>
```

