### **Introdução ao TypeScript**

**TypeScript** é um superset do **JavaScript** que adiciona **tipagem estática** e **outros recursos** poderosos para facilitar o desenvolvimento de aplicações escaláveis e de fácil manutenção. Ele compila para JavaScript, o que significa que qualquer código JavaScript válido também é válido em TypeScript.

#### **Por que usar TypeScript?**
1. **Tipagem Estática:** Ajuda a evitar erros no momento de desenvolvimento.
2. **Ferramentas de autocompletar:** Melhor suporte em editores de código.
3. **Compatibilidade com JavaScript:** Toda biblioteca JavaScript pode ser usada com TypeScript.
4. **Escalabilidade:** Ideal para grandes projetos, com fácil refatoração de código.

---

### **Fundamentos do TypeScript**

#### **1. Tipos de Dados Básicos**
TypeScript permite definir tipos explícitos para variáveis, funções e objetos.

- **Tipos primitivos:** `string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`.
  
Exemplo:
```typescript
let nome: string = "João";
let idade: number = 25;
let ativo: boolean = true;
```

#### **2. Arrays e Tuplas**
- **Arrays**: Defina o tipo dos elementos com `[]`.
  ```typescript
  let numeros: number[] = [1, 2, 3];
  ```
- **Tuplas**: Arrays com tipos fixos.
  ```typescript
  let pessoa: [string, number] = ["João", 25];
  ```

---

### **Interfaces e Tipos**
Interfaces e tipos permitem definir a forma de objetos e funções de maneira robusta.

#### **Interfaces**
Uma interface define a estrutura de um objeto, incluindo propriedades e seus tipos.
```typescript
interface Pessoa {
  nome: string;
  idade: number;
  ativo?: boolean; // opcional
}

const joao: Pessoa = { nome: "João", idade: 25 };
```

#### **Tipos**
São usados para criar aliases de tipos complexos.
```typescript
type Produto = {
  nome: string;
  preco: number;
};

const produto: Produto = { nome: "Camiseta", preco: 50 };
```

---

### **Classes e Objetos**
O TypeScript também suporta **orientação a objetos**, com **classes** e **métodos**.

```typescript
class Carro {
  marca: string;
  modelo: string;

  constructor(marca: string, modelo: string) {
    this.marca = marca;
    this.modelo = modelo;
  }

  descricao(): string {
    return `${this.marca} - ${this.modelo}`;
  }
}

const meuCarro = new Carro("Toyota", "Corolla");
console.log(meuCarro.descricao());
```

---

### **Funções e Tipos de Retorno**

Em TypeScript, é possível especificar os tipos de entrada e saída de funções.

```typescript
function soma(a: number, b: number): number {
  return a + b;
}
console.log(soma(5, 3)); // 8
```

---

### **Tipos Genéricos**
Genéricos permitem que funções, classes ou interfaces trabalhem com múltiplos tipos de forma segura.

```typescript
function identidade<T>(valor: T): T {
  return valor;
}

console.log(identidade("Texto")); // Tipo string
console.log(identidade(123)); // Tipo number
```

---

### **Integração do TypeScript com React**
TypeScript pode ser usado com React para garantir que os componentes estejam tipados corretamente.

#### **Componente funcional com TypeScript e React:**
```tsx
import React from 'react';

interface Props {
  nome: string;
  idade: number;
}

const Saudacao: React.FC<Props> = ({ nome, idade }) => {
  return <h1>Olá, {nome}. Você tem {idade} anos!</h1>;
};

export default Saudacao;
```

---

### **Ferramentas de Build e Configuração do TypeScript**

1. **Configuração do TypeScript (tsconfig.json):**
   O arquivo `tsconfig.json` define as opções de compilação do TypeScript, como:
   - `target`: Define a versão do JavaScript de saída (ex: `ES5`, `ES6`).
   - `strict`: Ativa verificações rigorosas de tipo.
   
   Exemplo de `tsconfig.json`:
   ```json
   {
     "compilerOptions": {
       "target": "ES6",
       "strict": true,
       "esModuleInterop": true
     }
   }
   ```

2. **Compilação com `tsc`:**
   Após a configuração, você pode compilar os arquivos TypeScript para JavaScript usando o comando:
   ```bash
   tsc
   ```

3. **Integração com Webpack ou outras ferramentas:**
   TypeScript pode ser integrado com bundlers como Webpack para transformar código TypeScript em JavaScript.

---

### **Resumo:**
- **TypeScript** é uma poderosa extensão do JavaScript com **tipagem estática**, aumentando a segurança e escalabilidade do código.
- **Interfaces e tipos** permitem criar contratos claros entre funções e objetos.
- **Funções genéricas** permitem escrever código mais flexível.
- **Integração com React** traz tipagem para componentes e propriedades.

