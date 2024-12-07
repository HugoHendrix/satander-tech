Aqui estão as explicações para os tópicos mencionados:  

---

### **1. Pascalina, multiplicação e divisão**
A **Pascalina** foi uma das primeiras calculadoras mecânicas, inventada em 1642 por **Blaise Pascal**, matemático e filósofo francês.  
- **Função principal**: Realizava somas e subtrações automaticamente por meio de rodas dentadas.  
- **Multiplicação e divisão**: Embora a máquina não realizasse essas operações diretamente, elas poderiam ser feitas repetindo operações de soma (para multiplicação) ou subtração (para divisão).  

A Pascalina foi um marco na história da computação por ser uma das primeiras máquinas a automatizar cálculos.  

---

### **2. Lógica binária/booleana**
- **Lógica binária**: É baseada no sistema numérico binário (0 e 1), que é a base de toda computação moderna.  
  - Um bit pode ter dois estados: **0** (desligado) ou **1** (ligado).  
  - Operações lógicas e aritméticas no computador são realizadas com base nesse sistema.  

- **Lógica booleana**: Criada por **George Boole**, é um sistema algébrico que opera com valores **verdadeiro (1)** e **falso (0)**.  
  - **Operadores principais**:
    - **AND** (E): Retorna 1 apenas se ambos os valores forem 1.  
    - **OR** (OU): Retorna 1 se pelo menos um dos valores for 1.  
    - **NOT** (NÃO): Inverte o valor, transformando 0 em 1 e vice-versa.

A lógica booleana é fundamental para o design de circuitos e programação.

---

### **3. Linguagem Pascal**
- **Origem**: Criada em 1970 por **Niklaus Wirth**.  
- **Objetivo**: Ser uma linguagem educacional para ensinar conceitos de programação estruturada.  
- **Características principais**:
  - Sintaxe simples e estruturada.
  - Uso frequente em aprendizado acadêmico e criação de algoritmos.  

Embora tenha perdido popularidade para outras linguagens mais modernas, o Pascal influenciou a criação de linguagens como o Delphi.

---

### **4. Linguagem COBOL**
- **Origem**: Desenvolvida em 1959 por uma equipe liderada por **Grace Hopper**, com o objetivo de ser uma linguagem de programação voltada para negócios.  
- **Acrônimo**: **COBOL** significa *Common Business-Oriented Language*.  
- **Características principais**:
  - Foco na manipulação de grandes volumes de dados.
  - Sintaxe parecida com a linguagem humana para facilitar a leitura.  
  - Ainda é amplamente usada em bancos, governos e grandes empresas para sistemas legados.

---

### **5. Quem foi Gottfried Wilhelm Leibniz?**
**Gottfried Wilhelm Leibniz** (1646–1716) foi um matemático, filósofo e inventor alemão, considerado uma das mentes mais brilhantes da história.  
- **Contribuições na matemática**: Desenvolveu o cálculo diferencial e integral de forma independente de Newton.  
- **Na computação**:
  - Criou a **máquina de calcular de Leibniz**, que conseguia realizar somas, subtrações, multiplicações e divisões.  
  - Propôs a **base binária**, percebendo que 0 e 1 poderiam ser usados para representar qualquer número.  



---

### **COBOL**
COBOL tem uma sintaxe descritiva e estruturada, sendo ideal para operações de negócios.  

#### **Exemplo: Programa para somar dois números**
```cobol
IDENTIFICATION DIVISION.
PROGRAM-ID. SomaNumeros.

DATA DIVISION.
WORKING-STORAGE SECTION.
    01 NUMERO-1 PIC 9(3) VALUE 0.
    01 NUMERO-2 PIC 9(3) VALUE 0.
    01 RESULTADO PIC 9(4) VALUE 0.

PROCEDURE DIVISION.
    DISPLAY "Informe o primeiro número: " WITH NO ADVANCING.
    ACCEPT NUMERO-1.
    DISPLAY "Informe o segundo número: " WITH NO ADVANCING.
    ACCEPT NUMERO-2.
    COMPUTE RESULTADO = NUMERO-1 + NUMERO-2.
    DISPLAY "O resultado da soma é: " RESULTADO.
    STOP RUN.
```

**Explicação:**
- **IDENTIFICATION DIVISION**: Declara o programa e suas informações.  
- **DATA DIVISION**: Define variáveis e seus tipos.  
- **PROCEDURE DIVISION**: Contém a lógica do programa (entrada, processamento e saída).  

---

### **Pascal**
Pascal é mais compacto e com sintaxe estruturada, sendo usado para ensinar conceitos de algoritmos.  

#### **Exemplo: Programa para somar dois números**
```pascal
program SomaNumeros;
var
  numero1, numero2, resultado: Integer;
begin
  Write('Informe o primeiro número: ');
  ReadLn(numero1);
  Write('Informe o segundo número: ');
  ReadLn(numero2);
  resultado := numero1 + numero2;
  WriteLn('O resultado da soma é: ', resultado);
end.
```

**Explicação:**
- **program**: Declara o nome do programa.  
- **var**: Declara as variáveis.  
- **begin...end**: Delimita o bloco principal do código.  
- **Write** e **ReadLn**: Para entrada e saída de dados.  

---

### Comparação:
1. **COBOL** é muito descritivo e ideal para tarefas relacionadas a processamento de dados em grande escala.  
2. **Pascal** é mais direto e estruturado, sendo ótimo para ensinar conceitos de programação.  

