
### **1. Status do Repositório**
Antes de gravar mudanças, é útil verificar o estado atual do repositório:
```bash
git status
```
Esse comando mostra:
- Arquivos modificados.
- Arquivos não rastreados.
- Arquivos prontos para commit.

---

### **2. Adicionando Arquivos ao Controle de Versão**
Antes de registrar as mudanças, os arquivos devem ser adicionados à área de **staging** (área de preparação).

- **Adicionar um arquivo específico:**
  ```bash
  git add arquivo.txt
  ```
- **Adicionar todos os arquivos (na pasta atual e subpastas):**
  ```bash
  git add .
  ```

---

### **3. Gravando as Alterações com um Commit**
Após adicionar os arquivos, você pode gravar as alterações usando o comando **commit**.

- **Commit simples com mensagem:**
  ```bash
  git commit -m "Descrição das mudanças realizadas"
  ```

- **Commit com descrição detalhada:**
  ```bash
  git commit
  ```
  Isso abrirá o editor padrão configurado, onde você pode escrever uma mensagem de commit mais detalhada.

#### **Boas práticas ao escrever mensagens de commit:**
- Seja claro e objetivo.
- Use o tempo verbal no imperativo, como: "Adicione suporte ao login" ou "Corrija bug na função de busca".
- Explique o motivo das alterações, se necessário.

---

### **4. Verificando o Histórico de Commits**
Após gravar mudanças, você pode visualizar o histórico de commits:
```bash
git log
```
- Para um histórico resumido:
  ```bash
  git log --oneline
  ```

---

### **5. Alterando um Commit Recente (Opcional)**
Se você cometeu um erro ou esqueceu de adicionar algo, pode corrigir o último commit.

- Para adicionar arquivos ao último commit:
  ```bash
  git add arquivo-esquecido.txt
  git commit --amend
  ```

- Para editar a mensagem do último commit:
  ```bash
  git commit --amend -m "Nova mensagem"
  ```

> **Atenção:** Evite alterar commits que já foram enviados para um repositório remoto.

---

### **6. Removendo Arquivos da Área de Staging**
Se você adicionou um arquivo por engano, pode removê-lo da área de staging sem apagar o arquivo:
```bash
git reset arquivo.txt
```

---

### **7. Excluindo Alterações Não Gravadas**
- **Reverter modificações em um arquivo específico:**
  ```bash
  git checkout -- arquivo.txt
  ```
- **Reverter todas as alterações não gravadas:**
  ```bash
  git reset --hard
  ```

---

### **8. Salvando Mudanças Temporárias (Stash)**
Se você precisa trocar de branch sem perder seu trabalho atual, pode salvar temporariamente as alterações com o **stash**:
```bash
git stash
```
Para recuperar as mudanças:
```bash
git stash apply
```

---
