 # VARIÁVEIS JAVASCRIPT

   **Para que servem as variáveis**:  
   Variáveis armazenam dados que podem ser usados e manipulados em diferentes partes de um programa. Elas ajudam a tornar o código reutilizável e dinâmico.

   **Como criar variáveis**:  
   Em JavaScript, você pode criar variáveis usando:
   - `var` (antigo, com escopo funcional)
   - `let` (preferido, com escopo de bloco)
   - `const` (para valores que não mudam).  
   Exemplo:  
   ```javascript
   let nome = "João";
   const idade = 25;
   var cidade = "São Paulo";
   ```

   **Usar ponto e vírgula (;) no final do código**:  
   O ponto e vírgula é opcional na maioria dos casos, pois JavaScript usa "Automatic Semicolon Insertion" (ASI). Porém, é uma boa prática usá-lo para evitar ambiguidades.

   **Como nomear variáveis**:  
   - Comece com letras, `_` ou `$`.  
   - Não use números no início.  
   - Escolha nomes descritivos e claros.  

   **Convenção camelCase no JavaScript**:  
   Em camelCase, a primeira palavra começa com letra minúscula, e as palavras subsequentes começam com maiúsculas:  
   Exemplo: `minhaVariavel`.

   **Comentários no JavaScript**:  
   - Comentário de uma linha:  
     ```javascript
     // Este é um comentário
     ```
   - Comentário de múltiplas linhas:  
     ```javascript
     /* Este é um 
        comentário de várias linhas */
     ```

   **Tipos de variáveis**:  
   - `string`: Texto  
   - `number`: Números  
   - `boolean`: Verdadeiro ou falso  
   - `null`: Intencionalmente vazio  
   - `undefined`: Não definido  
   - `object`: Estruturas complexas  
   - `symbol`: Identificador único  

   **Tipagem dinâmica**:  
   JavaScript permite mudar o tipo de uma variável em tempo de execução:  
   ```javascript
   let valor = 42;    // Número
   valor = "Texto";   // Agora é uma string
   ```

   **Tipagem fraca**:  
   Você pode realizar operações entre diferentes tipos de dados, às vezes com resultados inesperados:  
   ```javascript
   console.log("5" - 2); // 3 (conversão automática para número)
   ```

    **TypeScript**:  
    Uma extensão do JavaScript que adiciona tipagem estática, ajudando a prevenir erros antes da execução.  
    Exemplo:  
    ```typescript
    let nome: string = "João"; // Tipo explícito
    ```

    **Tipagem forte no Python**:  
    Diferente do JavaScript, Python não converte automaticamente tipos em operações:  
    ```python
    print("5" + 2)  # Erro: não pode somar string e número
    ```

   **`typeof`**:  
   O operador `typeof` é usado para verificar o tipo de uma variável ou expressão.  
   Exemplo:  
   ```javascript
   console.log(typeof "texto");  // "string"
   console.log(typeof 42);       // "number"
   console.log(typeof true);     // "boolean"
   console.log(typeof {});       // "object"
   console.log(typeof undefined); // "undefined"
   console.log(typeof null);     // "object" (peculiaridade do JS)
   ```

   **Atribuições**:  
   A atribuição em JavaScript é feita com o sinal `=`. Você também pode usar operadores compostos para atribuir e operar simultaneamente:  
   ```javascript
   let x = 10;     // Atribuição simples
   x += 5;         // Igual a x = x + 5
   x *= 2;         // Igual a x = x * 2
   ```

   **Por que não usar `var`?**  
   - `var` tem escopo funcional e ignora escopo de bloco, o que pode causar comportamentos inesperados:  
     ```javascript
     if (true) {
       var teste = "Oi";
     }
     console.log(teste); // Funciona mesmo fora do bloco
     ```
   - `var` permite redeclarar a mesma variável no mesmo escopo, o que pode levar a bugs:  
     ```javascript
     var x = 10;
     var x = 20; // Aceito sem erro
     ```

   **Diferenças entre `let` e `const`**:  
   - **`let`**:  
     - Pode ser reatribuído, mas não redeclarado no mesmo escopo.  
     - Respeita escopo de bloco.  
     ```javascript
     let idade = 25;
     idade = 30; // Ok
     let idade = 35; // Erro
     ```
   - **`const`**:  
     - É imutável: você não pode reatribuir.  
     - Também respeita escopo de bloco.  
     ```javascript
     const nome = "Ana";
     nome = "João"; // Erro
     ```



---  
