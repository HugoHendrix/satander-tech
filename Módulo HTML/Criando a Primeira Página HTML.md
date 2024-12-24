### Estrutura Básica do HTML

O código abaixo representa a estrutura básica de um documento HTML:

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

**Explicação:**
1. `<!DOCTYPE html>`: Declara o tipo de documento como HTML5.
2. `<html lang="en">`: A tag `<html>` é o contêiner raiz do documento HTML. O atributo `lang="en"` especifica o idioma do conteúdo (inglês neste caso).
3. `<head>`: Contém metainformações sobre o documento (explicado abaixo).
4. `<body>`: Contém o conteúdo visível da página.

---

### Tag `<head>`

A tag `<head>` é usada para armazenar metainformações sobre o documento HTML que não são exibidas diretamente na página. Alguns elementos comuns encontrados no `<head>` incluem:

1. **`<meta charset="UTF-8">`**: Define o conjunto de caracteres utilizado, como UTF-8, para garantir suporte a caracteres especiais.
2. **`<meta name="viewport" content="width=device-width, initial-scale=1.0">`**: Torna o site responsivo, ajustando a largura à tela do dispositivo.
3. **`<title>`**: Define o título da página exibido na aba do navegador.

Outros elementos que podem aparecer:
- Links para arquivos CSS: `<link rel="stylesheet" href="styles.css">`
- Links para ícones: `<link rel="icon" href="favicon.ico">`
- Scripts JavaScript externos ou internos.

---

### Tag `<body>`

A tag `<body>` contém todo o conteúdo que será exibido no navegador. Isso inclui:

- Texto (parágrafos, títulos, listas, etc.)
- Imagens
- Vídeos
- Links
- Botões
- Formularios

**Exemplo:**
```HTML
<body>
    <h1>Bem-vindo!</h1>
    <p>Este é um exemplo de conteúdo HTML.</p>
</body>
```

---

### Sobre Indentação

Indentação é o espaçamento usado para organizar o código de maneira hierárquica, facilitando a leitura e a manutenção.

- **Boas práticas:** Use dois ou quatro espaços por nível de hierarquia.
- Exemplos:

```HTML
<html>
    <head>
        <title>Exemplo</title>
    </head>
    <body>
        <h1>Conteúdo</h1>
    </body>
</html>
```

Ferramentas como editores de código (explicados abaixo) ajudam a padronizar a indentação.

---

### Tag `<title>`

A tag `<title>` define o título da página que aparece na aba do navegador e também é importante para SEO.

- **Exemplo:**
```HTML
<title>Minha Primeira Página</title>
```

---

### Sobre Editores de Código

Editores de código são ferramentas projetadas para facilitar o desenvolvimento de códigos. Alguns recursos comuns incluem:

- Destaque de sintaxe
- Auto-completar
- Indentação automática
- Integração com ferramentas de controle de versão

Exemplos populares: Visual Studio Code (VS Code), Sublime Text, Atom.

---

### Sobre o VS Code

O Visual Studio Code (VS Code) é um editor de código da Microsoft, gratuito e muito popular.

**Vantagens:**
- Suporte para múltiplas linguagens (HTML, CSS, JavaScript, etc.)
- Extensões que adicionam funcionalidades, como Emmet e Prettier.
- Debug integrado.
- Interface amigável e altamente customizável.

**Dica:** Baixe extensões como "Live Server" para visualizar instantaneamente as alterações no navegador.

---

### Meta e SEO

A tag `<meta>` é usada para fornecer metainformações ao navegador e motores de busca.

- **`<meta name="description" content="Breve descrição do conteúdo da página">`**: Ajuda os motores de busca a entenderem o conteúdo do site.
- **`<meta name="keywords" content="HTML, tutorial, SEO">`**: Palavras-chave relacionadas à página (menos usado atualmente).

**SEO (Search Engine Optimization):**
- Práticas para melhorar o ranqueamento nos motores de busca.
- Inclui o uso correto de tags HTML, como `<title>`, `<meta>`, e boas práticas no conteúdo da página.

---

### Documentação MDN HTML

A Mozilla Developer Network (MDN) oferece uma documentação abrangente e confiável sobre HTML.

- **URL:** [https://developer.mozilla.org/pt-BR/docs/Web/HTML](https://developer.mozilla.org/pt-BR/docs/Web/HTML)
- Contém:
  - Referência a todas as tags HTML.
  - Exemplos práticos.
  - Guia para boas práticas.

Utilize a documentação MDN como sua principal fonte de consulta para aprender e solucionar dúvidas sobre HTML.

