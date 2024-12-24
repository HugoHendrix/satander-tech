### Tabelas no HTML: Guia Completo

---

#### **1. Estrutura Básica de uma Tabela**
A estrutura de uma tabela no HTML é composta por tags que organizam cabeçalhos, linhas e células. 

```html
<table>
  <thead>
    <tr>
      <th>Nome</th>
      <th>Idade</th>
      <th>Profissão</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>João</td>
      <td>30</td>
      <td>Engenheiro</td>
    </tr>
    <tr>
      <td>Maria</td>
      <td>28</td>
      <td>Designer</td>
    </tr>
  </tbody>
</table>
```

---

#### **2. Tags que Compõem uma Tabela**
- `<table>`: Define a tabela.
- `<thead>`: Agrupa o cabeçalho da tabela.
- `<tbody>`: Agrupa o corpo da tabela.
- `<tfoot>`: (Opcional) Agrupa o rodapé da tabela.
- `<tr>`: Representa uma linha na tabela.
- `<th>`: Representa uma célula de cabeçalho (negrito e alinhada ao centro por padrão).
- `<td>`: Representa uma célula comum da tabela.

---

#### **3. Linhas e Colunas**
- As linhas são definidas com a tag `<tr>`.
- As colunas são criadas com `<td>` dentro de cada linha `<tr>`.
- Cabeçalhos de coluna são criados com `<th>`.

Exemplo:
```html
<table>
  <tr>
    <th>Coluna 1</th>
    <th>Coluna 2</th>
  </tr>
  <tr>
    <td>Celula 1</td>
    <td>Celula 2</td>
  </tr>
</table>
```

---

#### **4. Mesclando Células com `rowspan` e `colspan`**
- `rowspan`: Mescla células verticalmente, unindo várias linhas.
- `colspan`: Mescla células horizontalmente, unindo várias colunas.

Exemplo:
```html
<table>
  <tr>
    <th>Nome</th>
    <th colspan="2">Detalhes</th>
  </tr>
  <tr>
    <td>João</td>
    <td>Engenheiro</td>
    <td>30 anos</td>
  </tr>
  <tr>
    <td rowspan="2">Maria</td>
    <td>Designer</td>
    <td>28 anos</td>
  </tr>
  <tr>
    <td>Fotógrafa</td>
    <td>29 anos</td>
  </tr>
</table>
```

---

#### **5. Atributos da Tag `<table>`**
- `border`: Define a largura da borda (ex.: `border="1"`).
- `cellpadding`: Define o espaçamento interno das células.
- `cellspacing`: Define o espaçamento entre células.
- `width` e `height`: Determinam a largura e altura da tabela.
- `align`: Define o alinhamento da tabela (obsoleto, use CSS).

---

#### **6. Boas Práticas com Tabelas**
1. Use `<thead>`, `<tbody>` e `<tfoot>` para organizar e melhorar a semântica.
2. Utilize classes ou IDs para estilizar tabelas com CSS.
3. Inclua `scope` no `<th>` para melhorar a acessibilidade:
   ```html
   <th scope="col">Nome</th>
   ```
4. Evite o uso excessivo de `rowspan` e `colspan`, pois podem dificultar a manutenção.
5. Sempre use tabelas para exibir dados tabulares, não para layout.

---

#### **7. Estilizando com CSS**

```html
<style>
  table {
    width: 100%;
    border-collapse: collapse;
  }
  th, td {
    border: 1px solid #ddd;
    padding: 8px;
    text-align: left;
  }
  th {
    background-color: #f2f2f2;
  }
</style>
```

