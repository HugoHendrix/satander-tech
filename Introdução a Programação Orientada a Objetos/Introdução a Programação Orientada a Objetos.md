### **Introdução à Programação Orientada a Objetos (POO)**

A **Programação Orientada a Objetos (POO)** é um paradigma de programação baseado no conceito de **objetos**, que são instâncias de **classes**. Esses objetos podem conter **dados** e **métodos** para manipular esses dados. A POO é focada em organizar o código de maneira modular, reutilizável e fácil de entender.

#### **Principais Conceitos de POO:**

1. **Classe:** Define a estrutura de objetos. Ela é um modelo ou molde que descreve as características (atributos) e comportamentos (métodos) que os objetos dessa classe terão.

2. **Objeto:** É uma instância de uma classe, representando uma entidade concreta.

---

### **1. Classes e Objetos**

- **Classe:** Define os atributos e métodos comuns de objetos.
- **Objeto:** Cada instância de uma classe.

**Exemplo:**
```javascript
class Carro {
  constructor(marca, modelo) {
    this.marca = marca;
    this.modelo = modelo;
  }

  descricao() {
    return `${this.marca} - ${this.modelo}`;
  }
}

const meuCarro = new Carro("Toyota", "Corolla");
console.log(meuCarro.descricao()); // Toyota - Corolla
```

---

### **2. Encapsulamento**
O **encapsulamento** é a prática de esconder os detalhes internos do objeto, fornecendo métodos públicos para acessar e manipular esses dados. Isso promove a proteção dos dados e a integridade do estado do objeto.

- **Atributos privados:** São declarados usando uma convenção (geralmente um `_` antes do nome) ou utilizando modificadores de acesso (em algumas linguagens como `private` ou `protected`).

**Exemplo de encapsulamento:**
```javascript
class Pessoa {
  constructor(nome, idade) {
    this._nome = nome; // Atributo privado
    this.idade = idade;
  }

  // Método público
  getNome() {
    return this._nome;
  }

  setNome(nome) {
    this._nome = nome;
  }
}

const pessoa = new Pessoa("João", 25);
console.log(pessoa.getNome()); // João
pessoa.setNome("Maria");
console.log(pessoa.getNome()); // Maria
```

---

### **3. Herança**
A **herança** permite que uma classe herde atributos e métodos de outra classe, promovendo reutilização de código e a criação de hierarquias.

**Exemplo de herança:**
```javascript
class Animal {
  constructor(nome) {
    this.nome = nome;
  }

  falar() {
    console.log(`${this.nome} faz um som.`);
  }
}

class Cachorro extends Animal {
  falar() {
    console.log(`${this.nome} late.`);
  }
}

const cachorro = new Cachorro("Rex");
cachorro.falar(); // Rex late.
```

---

### **4. Polimorfismo**
**Polimorfismo** significa "muitas formas". Ele permite que objetos de diferentes classes sejam tratados de maneira uniforme, com a mesma interface, mas com comportamentos diferentes. Isso é possível por meio da sobrescrita (override) de métodos.

**Exemplo de polimorfismo:**
```javascript
class Gato extends Animal {
  falar() {
    console.log(`${this.nome} mia.`);
  }
}

const gato = new Gato("Tom");
gato.falar(); // Tom mia.

const cachorro = new Cachorro("Rex");
cachorro.falar(); // Rex late.
```

---

### **5. Abstração**
A **abstração** refere-se à ocultação de detalhes de implementação e à exposição apenas das funcionalidades essenciais. Isso é feito utilizando **interfaces** ou **classes abstratas**.

- **Classes abstratas** são aquelas que não podem ser instanciadas diretamente e servem como base para outras classes.
- **Interfaces** definem um contrato que as classes devem seguir.

**Exemplo de abstração com classe abstrata:**
```javascript
class Forma {
  constructor() {
    if (this.constructor === Forma) {
      throw new Error("Classe abstrata não pode ser instanciada.");
    }
  }

  area() {
    throw new Error("Método 'area' deve ser implementado.");
  }
}

class Quadrado extends Forma {
  constructor(lado) {
    super();
    this.lado = lado;
  }

  area() {
    return this.lado * this.lado;
  }
}

const quadrado = new Quadrado(4);
console.log(quadrado.area()); // 16
```

---

### **6. Métodos e Atributos**

- **Métodos:** Funções associadas a uma classe, que definem comportamentos.
- **Atributos:** Variáveis associadas a uma classe, que representam as características dos objetos.

**Exemplo de métodos e atributos:**
```javascript
class ContaBancaria {
  constructor(saldo) {
    this.saldo = saldo;
  }

  depositar(valor) {
    this.saldo += valor;
  }

  sacar(valor) {
    this.saldo -= valor;
  }

  obterSaldo() {
    return this.saldo;
  }
}

const conta = new ContaBancaria(1000);
conta.depositar(500);
conta.sacar(200);
console.log(conta.obterSaldo()); // 1300
```

---

### **7. Construtores e Destruidores**

- **Construtores:** Métodos especiais usados para inicializar objetos.
- **Destruidores:** Métodos que são chamados automaticamente quando o objeto é destruído (mais comum em linguagens como C++).

**Exemplo de construtor:**
```javascript
class Carro {
  constructor(marca, modelo) {
    this.marca = marca;
    this.modelo = modelo;
  }
}

const carro = new Carro("Honda", "Civic");
```

---

### **8. Interfaces e Classes Abstratas**
As **interfaces** são contratos que definem métodos que uma classe deve implementar. Já as **classes abstratas** fornecem uma implementação parcial, mas não podem ser instanciadas.

**Exemplo de interface (JavaScript não possui suporte nativo, mas podemos simular):**
```javascript
class Usuario {
  login() {
    throw new Error("Método 'login' não implementado.");
  }
}

class Admin extends Usuario {
  login() {
    console.log("Admin logado");
  }
}
```

---

### **9. Relações entre Classes**

- **Associação:** Um objeto contém uma referência a outro objeto.
- **Agregação:** Um tipo especial de associação, onde um objeto pode existir independentemente do outro.
- **Composição:** Uma relação mais forte onde o ciclo de vida de um objeto depende do outro.

**Exemplo de composição:**
```javascript
class Motor {
  constructor() {
    this.ligado = false;
  }

  ligar() {
    this.ligado = true;
  }
}

class Carro {
  constructor() {
    this.motor = new Motor(); // Composição
  }
}
```

---

### **Resumo:**
- **POO** organiza o código em **objetos** e **classes**, com foco em **encapsulamento**, **herança**, **polimorfismo**, e **abstração**.
- A POO facilita a **manutenção** e **reutilização** do código, promovendo práticas como **divisão de responsabilidades** e **modularidade**.

