### **`git log` e `git restore` no Git**

Esses dois comandos têm funções diferentes, mas complementares no gerenciamento de um repositório.

---

## **`git log`: Visualizando o histórico de commits**

O comando `git log` é usado para visualizar o histórico de commits do repositório. Ele mostra informações detalhadas sobre cada commit, como o hash (identificador único), autor, data e mensagem do commit.

### **Usos básicos de `git log`:**

1. **Exibir o histórico padrão:**
   ```bash
   git log
   ```
   Exibe os commits mais recentes no formato completo.

2. **Exibir um histórico resumido:**
   ```bash
   git log --oneline
   ```
   Mostra cada commit em uma única linha, com hash abreviado e mensagem.

3. **Exibir o histórico com gráfico de branches:**
   ```bash
   git log --oneline --graph --all
   ```
   Útil para visualizar a relação entre branches e commits.

4. **Filtrar commits por autor:**
   ```bash
   git log --author="Nome do Autor"
   ```

5. **Filtrar commits por palavra-chave na mensagem:**
   ```bash
   git log --grep="palavra-chave"
   ```

6. **Limitar o número de commits exibidos:**
   ```bash
   git log -n 5
   ```
   Mostra apenas os 5 commits mais recentes.

7. **Exibir mudanças associadas a um commit específico:**
   ```bash
   git show <hash-do-commit>
   ```

---

## **`git restore`: Revertendo mudanças em arquivos**

O comando `git restore` é usado para desfazer alterações em arquivos no diretório de trabalho. Ele substitui partes da funcionalidade do antigo `git checkout` e do `git reset` para trabalhar de forma mais clara.

### **Usos básicos de `git restore`:**

1. **Reverter mudanças não adicionadas à área de staging:**
   ```bash
   git restore arquivo.txt
   ```
   Restaura o arquivo ao estado do último commit.

2. **Remover um arquivo da área de staging:**
   ```bash
   git restore --staged arquivo.txt
   ```
   Faz o arquivo voltar ao estado "não rastreado".

3. **Reverter todas as alterações no diretório de trabalho:**
   ```bash
   git restore .
   ```
   Atenção: Isso desfaz todas as mudanças locais.

---

### **Fluxo prático com `git log` e `git restore`:**

1. **Verificar o histórico de commits:**
   ```bash
   git log --oneline
   ```

2. **Identificar o hash de um commit para restaurar o estado de um arquivo:**
   ```bash
   git restore --source <hash> arquivo.txt
   ```
   Isso restaura o arquivo ao estado do commit especificado.

3. **Restaurar um arquivo específico ao estado do branch atual:**
   ```bash
   git restore arquivo.txt
   ```

