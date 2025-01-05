### **Introdução ao ReactJS**

**ReactJS** é uma biblioteca JavaScript criada pelo Facebook para construir interfaces de usuário. Seu foco principal é tornar o desenvolvimento de aplicações web dinâmicas, modulares e interativas de forma eficiente e escalável.

#### **Por que usar React?**
1. **Componentização:** Divida a interface em componentes reutilizáveis.
2. **Virtual DOM:** Atualizações eficientes no DOM real, melhorando o desempenho.
3. **Unidirectional Data Flow:** O fluxo de dados previsível facilita o entendimento e a manutenção do código.
4. **Comunidade Ativa:** Muitas bibliotecas e ferramentas disponíveis.

---

### **Componentização**
Componentes são os blocos de construção no React. Eles podem ser:
- **Funcionais:** Declarados como funções e utilizam hooks.
- **De Classe (Legado):** Declarados como classes e utilizam métodos de ciclo de vida.

#### **Exemplo de Componente Funcional:**
```javascript
function Saudacao({ nome }) {
  return <h1>Olá, {nome}!</h1>;
}
```

#### **Componentes são Reutilizáveis:**
```javascript
function App() {
  return (
    <div>
      <Saudacao nome="João" />
      <Saudacao nome="Maria" />
    </div>
  );
}
```

---

### **Props e Estados**
#### **Props (Propriedades):**
- São dados passados para os componentes.
- Imutáveis dentro do componente.
- Exemplo:
  ```javascript
  function Mensagem({ texto }) {
    return <p>{texto}</p>;
  }
  ```

#### **State (Estado):**
- Representa dados locais de um componente.
- Mutável e usado para controlar interatividade.
- Exemplo com hook `useState`:
  ```javascript
  import React, { useState } from 'react';

  function Contador() {
    const [contador, setContador] = useState(0);

    return (
      <div>
        <p>Contagem: {contador}</p>
        <button onClick={() => setContador(contador + 1)}>Incrementar</button>
      </div>
    );
  }
  ```

---

### **Ciclo de Vida dos Componentes (React Legado)**
Nos componentes de classe, o ciclo de vida possui três estágios principais:
1. **Montagem:** Quando o componente é criado e inserido no DOM.
   - `constructor`
   - `componentDidMount`

2. **Atualização:** Quando as props ou o estado mudam.
   - `componentDidUpdate`

3. **Desmontagem:** Quando o componente é removido do DOM.
   - `componentWillUnmount`

#### **Exemplo:**
```javascript
import React, { Component } from 'react';

class ExemploCicloVida extends Component {
  componentDidMount() {
    console.log('Componente montado!');
  }

  componentDidUpdate() {
    console.log('Componente atualizado!');
  }

  componentWillUnmount() {
    console.log('Componente desmontado!');
  }

  render() {
    return <h1>Olá, React!</h1>;
  }
}
```

---

### **O Papel de um Bundler no Desenvolvimento Web**
Um **bundler** como o **Webpack** ou **Vite**:
1. **Agrupa Arquivos:** Combina arquivos JavaScript, CSS, imagens, etc., em pacotes menores.
2. **Transpila Código:** Usa ferramentas como Babel para converter código moderno em versões compatíveis com navegadores antigos.
3. **Otimização:** Minifica o código e melhora o desempenho da aplicação.

---

### **Resumo**
O React permite criar aplicações modulares e dinâmicas com:
- Componentes reutilizáveis.
- Controle de dados por meio de props e estados.
- Métodos de ciclo de vida para gerenciar comportamentos dinâmicos.
