<div align="center">

# Pedro Correa Siqueira  
## Cientista da Computação em Desenvolvimento  

<style>
:root {
  --bg-color: #ffffff;
  --text-color: #333333;
  --border-color: #e1e4e8;
  --heading-color: #0366d6;
  --link-color: #0366d6;
  --quote-color: #6a737d;
}

[data-theme="dark"] {
  --bg-color: #0d1117;
  --text-color: #c9d1d9;
  --border-color: #30363d;
  --heading-color: #58a6ff;
  --link-color: #58a6ff;
  --quote-color: #8b949e;
}

.theme-toggle {
  background: var(--bg-color);
  color: var(--text-color);
  border: 1px solid var(--border-color);
  padding: 8px 16px;
  border-radius: 6px;
  cursor: pointer;
  font-size: 14px;
  margin: 10px 0;
  transition: all 0.3s ease;
}

.theme-toggle:hover {
  opacity: 0.8;
  transform: translateY(-1px);
}

.markdown-body {
  background-color: var(--bg-color);
  color: var(--text-color);
  transition: background-color 0.3s ease, color 0.3s ease;
}

h1, h2, h3 {
  color: var(--heading-color);
  transition: color 0.3s ease;
}

hr {
  border-color: var(--border-color);
  transition: border-color 0.3s ease;
}

blockquote {
  color: var(--quote-color);
  border-left-color: var(--border-color);
}

a {
  color: var(--link-color);
}

.theme-indicator {
  font-size: 12px;
  color: var(--quote-color);
  margin-top: 5px;
}
</style>

<button class="theme-toggle" onclick="toggleTheme()">
  <span id="theme-icon">🌓</span>
  <span id="theme-text">Alternar Tema</span>
</button>
<div class="theme-indicator" id="theme-status">Detectando tema do sistema...</div>

<script>
function setTheme(theme) {
  document.documentElement.setAttribute('data-theme', theme);
  localStorage.setItem('theme', theme);
  updateThemeUI(theme);
}

function updateThemeUI(theme) {
  const themeText = document.getElementById('theme-text');
  const themeIcon = document.getElementById('theme-icon');
  const themeStatus = document.getElementById('theme-status');
  
  if (theme === 'dark') {
    themeText.textContent = 'Modo Claro';
    themeIcon.textContent = '☀️';
    themeStatus.textContent = 'Tema escuro ativado';
  } else {
    themeText.textContent = 'Modo Escuro';
    themeIcon.textContent = '🌙';
    themeStatus.textContent = 'Tema claro ativado';
  }
}

function toggleTheme() {
  const currentTheme = document.documentElement.getAttribute('data-theme');
  const newTheme = currentTheme === 'dark' ? 'light' : 'dark';
  setTheme(newTheme);
}

function detectSystemTheme() {
  if (window.matchMedia && window.matchMedia('(prefers-color-scheme: dark)').matches) {
    return 'dark';
  }
  return 'light';
}

function initializeTheme() {
  // Verificar tema salvo primeiro
  const savedTheme = localStorage.getItem('theme');
  
  if (savedTheme) {
    setTheme(savedTheme);
  } else {
    // Detectar tema do sistema
    const systemTheme = detectSystemTheme();
    setTheme(systemTheme);
    
    // Atualizar quando o tema do sistema mudar
    if (window.matchMedia) {
      window.matchMedia('(prefers-color-scheme: dark)').addEventListener('change', e => {
        if (!localStorage.getItem('theme')) { // Só mudar automaticamente se não houver preferência salva
          setTheme(e.matches ? 'dark' : 'light');
        }
      });
    }
  }
}

// Inicializar tema quando a página carregar
document.addEventListener('DOMContentLoaded', initializeTheme);
</script>

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6b/Bloch_sphere.svg/400px-Bloch_sphere.svg.png" alt="Bloch Sphere - Representação geométrica do estado quântico de um qubit" width="350px"/>
</p>

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;|\psi\rangle=\alpha|0\rangle+\beta|1\rangle" alt="Quantum State Superposition"/>
</p>

<br>

**Desenvolvedor Full Stack** • **Pesquisador em Computação Científica** • **Estudioso de Computação Quântica**

> Especialista em desenvolvimento de software escalável e computação científica de alto desempenho.  
> Experiência consolidada em arquiteturas backend robustas, com crescente dedicação aos fundamentos teóricos da Ciência da Computação, Matemática Aplicada e Computação Quântica.

<br>

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;H=\frac{1}{\sqrt{2}}\begin{pmatrix}1&1\\1&-1\end{pmatrix}" alt="Hadamard Gate"/>
</p>

---

## ▎Perfil Acadêmico e Profissional

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;\hat{H}\psi=E\psi" alt="Schrödinger Equation"/>
</p>

Profissional com formação sólida em desenvolvimento de sistemas complexos, focado no estudo e aplicação de conceitos avançados em Ciência da Computação teórica e aplicada. Combino experiência prática no desenvolvimento de soluções enterprise com um crescente interesse nos fundamentos matemáticos e físicos da computação.

### **Áreas de Especialização**

- **Ciência da Computação**: Algoritmos avançados, complexidade computacional e estruturas de dados otimizadas  
- **Matemática Aplicada**: Métodos numéricos, álgebra linear computacional e análise matemática  
- **Computação Quântica**: Algoritmos quânticos, mecânica quântica aplicada e implementações em sistemas quânticos  

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;CNOT=\begin{pmatrix}1&0&0&0\\0&1&0&0\\0&0&0&1\\0&0&1&0\end{pmatrix}" alt="CNOT Gate"/>
</p>

Especialista em arquiteturas de microserviços e sistemas distribuídos, com foco na intersecção entre computação clássica e quântica. Explorando como os princípios da mecânica quântica podem revolucionar os paradigmas computacionais tradicionais.

---

## ▎Stack Tecnológico

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;\nabla^2\psi+\frac{2m}{\hbar^2}(E-V)\psi=0" alt="Quantum Wave Equation"/>
</p>

### **Linguagens de Programação**
- **Backend Enterprise**: Java, Kotlin, Ruby, Python  
- **Computação Científica**: Julia — linguagem especializada para computação numérica de alto desempenho  
- **Frontend Moderno**: JavaScript com Vue.js e React  

### **Arquiteturas e Frameworks**
- **Spring Boot**: APIs enterprise com padrões arquiteturais avançados  
- **Ruby on Rails**: Aplicações web escaláveis seguindo princípios de desenvolvimento ágil  
- **Microserviços**: Design e implementação de arquiteturas distribuídas  
- **Vue.js & React**: Construção de interfaces reativas e single-page applications  

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;e^{i\pi}+1=0" alt="Euler's Identity"/>
</p>

### **Ecossistema Julia para Computação Científica**
- **DifferentialEquations.jl**: Resolução numérica de sistemas de equações diferenciais  
- **LinearAlgebra.jl**: Operações otimizadas de álgebra linear  
- **Plots.jl**: Visualização científica e análise gráfica  
- **DataFrames.jl**: Manipulação de conjuntos de dados estruturados  
- **Flux.jl**: Frameworks de aprendizado de máquina científico  
- **Optimization.jl**: Algoritmos de otimização para pesquisa operacional  

<p align="center">
  <img src="https://math.vercel.app/?from=\Large%20\Delta%20x\Delta%20p\geq\frac{\hbar}{2}" alt="Heisenberg Uncertainty Principle"/>
</p>

### **Infraestrutura e Dados**
- **Containerização**: Docker, Kubernetes para orquestração de aplicações  
- **Bancos de Dados**: MySQL, PostgreSQL, MongoDB  
- **Plataformas Cloud**: Supabase, Firebase  
- **Controle de Versão**: Git com metodologias avançadas  

### **Ferramentas de Desenvolvimento**
- **IDEs**: IntelliJ IDEA, Zed Editor  
- **Computação Científica**: Jupyter Notebooks para prototipagem  
- **Documentação**: LaTeX para publicações científicas, Markdown para projetos  

---

## ▎Área de Pesquisa e Estudos

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;U=e^{-i\frac{H}{\hbar}t}" alt="Quantum Time Evolution"/>
</p>

### **Fundamentos Computacionais**
- **Algoritmos e Complexidade**: Análise assintótica, estruturas de dados avançadas, algoritmos paralelos  
- **Matemática Computacional**: Métodos numéricos, álgebra linear, análise de convergência  
- **Teoria da Computação**: Fundamentos teóricos e aplicações práticas  

<p align="center">
  <img src="https://math.vercel.app/?from=\Large%20QFT|x\rangle=\frac{1}{\sqrt{N}}\sum_{y=0}^{N-1}e^{2\pi%20ixy/N}|y\rangle" alt="Quantum Fourier Transform"/>
</p>

### **Computação Quântica**
- **Algoritmos Fundamentais**: Shor, Grover, Quantum Fourier Transform  
- **Simulação Quântica**: Implementação de sistemas quânticos em computadores clássicos  
- **Aplicações**: Otimização, criptografia quântica, vantagens computacionais  

<p align="center">
  <img src="https://math.vercel.app/?from=\Large%20\rho=\sum_i%20p_i|\psi_i\rangle\langle\psi_i|" alt="Density Matrix"/>
</p>

### **Domínios de Aplicação**
- **Física Computacional**: Simulação de fenômenos físicos complexos  
- **Bioinformática**: Análise computacional de dados genômicos  
- **Otimização**: Resolução de problemas combinatórios e NP-difíceis  
- **Modelagem Estocástica**: Sistemas dinâmicos e simulações de Monte Carlo  

---

## ▎Estatísticas de Desenvolvimento

<p align="center">
  <img src="https://latex.codecogs.com/svg.latex?\Large&space;\langle\phi|\psi\rangle=\int\phi^*\psi\,dx" alt="Quantum Inner Product"/>
</p>

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=baku01&layout=compact&theme=default" alt="Distribuição de Linguagens"/>
</p>

---

<p align="center">
  <img src="https://math.vercel.app/?from=\Large%20\frac{\partial\psi}{\partial%20t}=-\frac{i}{\hbar}H\psi" alt="Time-dependent Schrödinger Equation"/>
</p>

> *"Nature isn't classical, dammit, and if you want to make a simulation of nature, you'd better make it quantum mechanical, and by golly it's a wonderful problem, because it doesn't look so easy."*  
> **— Richard P. Feynman**  
> *Simulating Physics with Computers (1981)*

</div>
