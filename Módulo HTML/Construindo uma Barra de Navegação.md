# Barra de Navegação Simples e Responsiva

## **1. Estrutura HTML**

Comece com a estrutura básica:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Barra de Navegação</title>
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#home">Início</a></li>
        <li><a href="#sobre">Sobre</a></li>
        <li><a href="#servicos">Serviços</a></li>
        <li><a href="#contato">Contato</a></li>
      </ul>
    </nav>
  </header>
</body>
</html>
```

---

## **2. Estilização com CSS**

```css
/* Estilo da barra de navegação */
nav {
  background-color: #333;
  padding: 0.5em;
}

nav ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-around;
}

nav ul li a {
  text-decoration: none;
  color: white;
  padding: 0.5em 1em;
  font-weight: bold;
  transition: background-color 0.3s;
}

nav ul li a:hover {
  background-color: #555;
  border-radius: 5px;
}
```

---

## **3. Tornando Responsivo**

Adicione responsividade para dispositivos menores:

```css
@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
    align-items: center;
  }

  nav ul li {
    margin: 0.5em 0;
  }
}
```

---

## **4. Menu Responsivo com JavaScript**

### HTML Modificado:

```html
<header>
  <nav>
    <button id="menu-toggle">&#9776;</button>
    <ul id="menu">
      <li><a href="#home">Início</a></li>
      <li><a href="#sobre">Sobre</a></li>
      <li><a href="#servicos">Serviços</a></li>
      <li><a href="#contato">Contato</a></li>
    </ul>
  </nav>
</header>
```

### CSS Modificado:

```css
#menu {
  display: flex;
}

#menu-toggle {
  display: none;
  background: none;
  border: none;
  color: white;
  font-size: 1.5em;
  cursor: pointer;
}

@media (max-width: 768px) {
  #menu {
    display: none;
    flex-direction: column;
  }

  #menu.show {
    display: flex;
  }

  #menu-toggle {
    display: block;
  }
}
```

### JavaScript:

```html
<script>
  const toggleButton = document.getElementById('menu-toggle');
  const menu = document.getElementById('menu');

  toggleButton.addEventListener('click', () => {
    menu.classList.toggle('show');
  });
</script>
```


