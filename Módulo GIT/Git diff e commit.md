### **O que é `git diff` e como ele funciona?**

O comando `git diff` é usado para visualizar as diferenças entre versões do código em um repositório Git. Ele mostra as alterações realizadas em arquivos, linha por linha, permitindo entender o que foi modificado antes de gravar (commit) ou enviar (push) essas mudanças.

---

### **Principais usos do `git diff`:**

1. **Verificar alterações não adicionadas à área de staging:**
   ```bash
   git diff
   ```
   Mostra as diferenças entre o diretório de trabalho e a área de staging.

2. **Comparar arquivos na área de staging com o último commit:**
   ```bash
   git diff --staged
   ```
   Útil para verificar o que será incluído no próximo commit.

3. **Comparar dois commits específicos:**
   ```bash
   git diff commit1 commit2
   ```
   Substitua `commit1` e `commit2` pelos hashes dos commits que deseja comparar.

4. **Comparar mudanças em um arquivo específico:**
   ```bash
   git diff arquivo.txt
   ```

5. **Comparar mudanças entre branches:**
   ```bash
   git diff branch1 branch2
   ```
   Exibe as diferenças entre dois branches.

---

### **O que é `git commit` e como ele funciona?**

O comando `git commit` é usado para gravar alterações na história do repositório. Ele move as mudanças da área de staging para o repositório local, criando um ponto no histórico do projeto.

---

### **Como usar o `git commit`:**

1. **Commit básico com mensagem curta:**
   Após adicionar arquivos à área de staging:
   ```bash
   git commit -m "Descrição breve das mudanças"
   ```

2. **Commit com mensagem detalhada:**
   Para abrir o editor de texto configurado e escrever uma descrição mais longa:
   ```bash
   git commit
   ```

3. **Commit de todos os arquivos modificados (sem usar `git add`):**
   ```bash
   git commit -a -m "Mensagem do commit"
   ```

4. **Alterar a mensagem do último commit:**
   ```bash
   git commit --amend -m "Nova mensagem"
   ```

---

### **Fluxo comum de uso de `git diff` e `git commit`:**

1. Modifique os arquivos do projeto.
2. Verifique as alterações realizadas:
   ```bash
   git diff
   ```
3. Adicione as alterações à área de staging:
   ```bash
   git add .
   ```
4. Verifique as diferenças na área de staging:
   ```bash
   git diff --staged
   ```
5. Faça o commit das alterações:
   ```bash
   git commit -m "Descrição das mudanças"
   ```

