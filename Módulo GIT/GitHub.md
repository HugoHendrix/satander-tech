### **O que é GitHub?**

O **GitHub** é uma plataforma de hospedagem de código baseada em Git. Ele permite que desenvolvedores armazenem, colaborem e gerenciem seus projetos, além de oferecer ferramentas para controle de versão, automação e integração contínua.

---

### **Principais Recursos do GitHub**

1. **Repositórios:** 
   - Hospedagem de código com controle de versão.
   - Repositórios podem ser públicos (acessíveis por todos) ou privados.

2. **Colaboração:** 
   - Controle de permissões para equipes.
   - Funcionalidades como pull requests e revisões de código.

3. **Branches:** 
   - Criação e gerenciamento de múltiplas linhas de desenvolvimento.

4. **Automação com GitHub Actions:** 
   - Configuração de pipelines de CI/CD diretamente no GitHub.

5. **Issues e Projetos:** 
   - Rastreamento de tarefas, bugs e melhorias.

6. **Pages:** 
   - Hospedagem gratuita de sites estáticos.

7. **Segurança:** 
   - Ferramentas para análise de vulnerabilidades no código.

---

### **Criando e Configurando um Repositório no GitHub**

#### **1. Criar um repositório**
1. Acesse [github.com](https://github.com) e faça login.
2. Clique em **New repository** ou no botão **+** no canto superior direito.
3. Configure:
   - Nome do repositório.
   - Descrição (opcional).
   - Visibilidade (público ou privado).
   - Inicialize com um **README**, se desejar.

4. Clique em **Create repository**.

---

#### **2. Conectar o Repositório Local ao GitHub**
Após criar o repositório, copie sua URL.

1. No terminal, dentro da pasta do seu projeto:
   ```bash
   git remote add origin <URL-do-repositório>
   ```

2. Enviar arquivos do repositório local para o remoto:
   ```bash
   git push -u origin main
   ```

---

### **Trabalhando com GitHub**

#### **1. Clonar um repositório existente**
Se você deseja começar a trabalhar em um repositório existente:
```bash
git clone <URL-do-repositório>
```

#### **2. Criar um pull request**
Os **pull requests** permitem sugerir mudanças em um projeto.

1. Faça as alterações em um novo branch.
2. Envie o branch para o repositório remoto:
   ```bash
   git push origin <nome-do-branch>
   ```
3. No GitHub, vá até a aba **Pull Requests** e clique em **New Pull Request**.
4. Compare os branches e descreva as mudanças realizadas.

#### **3. Trabalhar com Issues**
As **issues** ajudam a organizar tarefas e rastrear bugs.
1. Na aba **Issues**, clique em **New Issue**.
2. Descreva o problema ou tarefa e clique em **Submit new issue**.

---

### **Publicando Sites no GitHub Pages**

Você pode hospedar um site estático no GitHub Pages.

1. Crie ou configure seu repositório.
2. Adicione arquivos HTML, CSS e JavaScript ao repositório.
3. Vá até as configurações do repositório e ative o **GitHub Pages**:
   - Escolha o branch e a pasta para publicação.
4. Acesse o link fornecido pelo GitHub.

---

### **Segurança e Boas Práticas no GitHub**

1. **Não compartilhe informações sensíveis:** 
   - Evite salvar senhas, tokens ou credenciais no repositório.
   - Use arquivos `.env` e ferramentas de segurança.

2. **Configure o `.gitignore`:**
   - Adicione arquivos e pastas que não devem ser rastreados pelo Git.

3. **Proteja o branch principal:**
   - Configure permissões para evitar alterações diretas no branch principal.

4. **Use mensagens de commit claras:**
   - Adote boas práticas na descrição das mudanças.

