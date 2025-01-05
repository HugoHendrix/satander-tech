### **O que é uma API?**
API significa **Application Programming Interface**. É um conjunto de regras e definições que permite que diferentes sistemas ou softwares se comuniquem entre si. APIs permitem que:
- Aplicações troquem dados ou funcionalidades.
- Sistemas sejam integrados sem expor detalhes internos.

#### **Exemplo no dia a dia:**
Pense em um restaurante:
- O cliente (você) pede um prato.
- O garçom (API) leva o pedido para a cozinha (sistema) e traz o prato pronto.
- Você não precisa saber como o prato foi preparado.

---

### **Como usar uma API?**
1. **Entender a documentação:**
   - Todas as APIs possuem documentação explicando como acessar e usar seus endpoints.

2. **Fazer requisições:**
   - Requisições podem ser feitas com ferramentas como:
     - `fetch` no navegador.
     - Bibliotecas como `axios`.
     - Ferramentas externas como Postman ou Insomnia.

3. **Requisições comuns (métodos HTTP):**
   - `GET`: Busca informações.
   - `POST`: Envia dados.
   - `PUT`: Atualiza dados.
   - `DELETE`: Remove dados.

---

### **Tipos de APIs**
1. **APIs abertas (ou públicas):**
   - Disponíveis para qualquer desenvolvedor.
   - Exemplo: API de clima do OpenWeather.

2. **APIs restritas:**
   - Exigem autenticação ou são limitadas a parceiros.

3. **APIs locais:**
   - Executadas em uma máquina local ou servidor interno.

4. **Browser APIs:**
   - Fornecidas pelo navegador (ex.: `DOM API`, `Fetch API`).

---

### **API REST**
**REST** (Representational State Transfer) é um estilo arquitetural para APIs.

#### **Características principais:**
1. **Stateless:** O servidor não armazena o estado do cliente.
2. **Recursos identificados por URIs:** Cada recurso tem uma URL única.
3. **Métodos HTTP claros:**
   - `GET`, `POST`, `PUT`, `DELETE`, etc.
4. **Formatos comuns:** Geralmente usa JSON ou XML.

---

### **API RESTful**
Uma API é chamada de **RESTful** se seguir corretamente os princípios REST. Exemplo de uma API RESTful:
- URL: `https://api.exemplo.com/usuarios`
  - `GET /usuarios`: Retorna todos os usuários.
  - `POST /usuarios`: Cria um novo usuário.
  - `PUT /usuarios/1`: Atualiza o usuário com ID 1.
  - `DELETE /usuarios/1`: Remove o usuário com ID 1.

---

### **Browser APIs**
As **Browser APIs** são APIs nativas oferecidas pelos navegadores, que permitem interagir com diferentes funcionalidades do navegador e da web.

#### **Exemplos de Browser APIs:**
1. **DOM API:** Manipula elementos HTML.
   ```javascript
   document.querySelector('h1').textContent = 'Olá, Mundo!';
   ```

2. **Fetch API:** Faz requisições HTTP.
   ```javascript
   fetch('https://api.exemplo.com/dados')
     .then(response => response.json())
     .then(data => console.log(data));
   ```

3. **Geolocation API:** Obtém localização do usuário.
   ```javascript
   navigator.geolocation.getCurrentPosition(position => {
     console.log(position.coords.latitude, position.coords.longitude);
   });
   ```

4. **LocalStorage API:** Armazena dados no navegador.
   ```javascript
   localStorage.setItem('nome', 'João');
   console.log(localStorage.getItem('nome'));
   ```

