
### **1. Conceito de número computável e o infinito como obstáculo**
- **Número computável**: Um número é considerado computável se é possível criar um algoritmo que calcule suas casas decimais com precisão arbitrária. Por exemplo:
  - **Exemplo de números computáveis**: \(\pi\), \(\sqrt{2}\), e \(\phi\) (mesmo sendo infinitos, existem algoritmos que podem calcular cada uma de suas casas).
  - **Números não computáveis**: Existem números que, mesmo existindo matematicamente, não podem ser calculados porque não há um algoritmo finito para descrevê-los.

- **O infinito como obstáculo**:
  - A computação lida com sistemas finitos: memória, tempo e operações.
  - O infinito desafia a computação porque é impossível representá-lo de forma exata ou manipulá-lo completamente em uma máquina que opera com recursos limitados.

---

### **2. Números racionais e irracionais**
- **Números racionais**:
  - São números que podem ser escritos como uma fração \( \frac{a}{b} \), onde \(a\) e \(b\) são inteiros e \(b \neq 0\).
  - Exemplos: \( \frac{1}{2} \), \(3\), \(0.25\) (decimais finitos ou periódicos).

- **Números irracionais**:
  - Não podem ser representados como frações e possuem decimais infinitos e não periódicos.
  - Exemplos: \(\pi\), \(\sqrt{2}\), e \(\phi\).
  - Eles são fundamentais em muitas áreas da matemática e aparecem frequentemente em cálculos geométricos e na natureza.

---

### **3. Phi (\(\phi\))**
- **Definição**: O número \(\phi\), ou **razão áurea**, é um número irracional aproximado por \(1.6180339887...\).
- **Fórmula**: \(\phi = \frac{1 + \sqrt{5}}{2}\).
- **Importância**:
  - Aparece em proporções geométricas, arte, arquitetura e na natureza (como no arranjo de folhas e conchas).
  - Está relacionado à sequência de Fibonacci: a razão entre dois números consecutivos da sequência tende a \(\phi\).

---

### **4. Representação de número e a limitação de memória**
Na computação, os números são representados em sistemas digitais com precisão limitada devido à memória finita:
- **Números inteiros**:
  - Representados diretamente em formato binário.
  - Limitados por um intervalo fixo, como 32 ou 64 bits (\( -2^{31} \) a \( 2^{31}-1\) em 32 bits).
- **Números reais**:
  - Representados como números de ponto flutuante (\(mantissa \times 2^{expoente}\)).
  - Perdem precisão para representar números muito grandes, muito pequenos ou irracionais.
  - Exemplo: \( \pi \) é truncado ou arredondado ao ser armazenado.

**Problema**: A limitação de memória torna impossível representar números infinitos ou irracionais com precisão total.

---

### **5. Alan Turing e o conceito de número computável**
- **Alan Turing (1912–1954)**:
  - Matemático e pioneiro da ciência da computação.
  - Introduziu o conceito de **máquinas de Turing**, modelos abstratos que formalizam o que significa computar.

- **Números computáveis**:
  - Turing definiu números computáveis como aqueles cujas casas decimais podem ser geradas por uma máquina de Turing.
  - Ele mostrou que nem todos os números são computáveis, como alguns números definidos por problemas indecidíveis.

**Exemplo prático**:
- O número \(\pi\) é computável porque existe um algoritmo que pode calcular suas casas decimais.
- Outros números, como alguns definidos no problema da parada (decidir se um programa irá parar ou continuar executando para sempre), são não computáveis.

--- 

### **Resumo:**
1. **Números computáveis** são aqueles que podem ser gerados por um algoritmo, mas o infinito (ou números não computáveis) representa um obstáculo para a computação.
2. Números racionais são expressos como frações; irracionais têm decimais infinitos e não periódicos.
3. \(\phi\), a razão áurea, é um número irracional com relevância matemática e estética.
4. A representação numérica na computação é limitada por memória e precisão.
5. Alan Turing ajudou a formalizar o conceito de números computáveis e os limites do que é possível computar.