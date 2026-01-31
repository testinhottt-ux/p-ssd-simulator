🧲 Simulador p-SSD: Computação Probabilística e Modelo de Ising
![License: MIT](https://img.shooray](https://opensource.org/licenses/MIT)Status: Simulação


https://testinhottt-ux.github.io/p-ssd-simulator/pbitreal.html



https://testinhottt-ux.github.io/p-ssd-simulator/pbit2.html



https://testinhottt-ux.github.io/p-ssd-simulator/pbit.html

Um simulador web interativo e visualmente imersivo baseado no Modelo de Ising para demonstrar o comportamento de P-Bits (Probabilistic Bits) e relaxação termodinâmica em memórias tipo X-LC (Crossbar Logic).

Este projeto utiliza física rigorosa para simular como spins interagem, relaxam e convergem para estados de baixa energia, contrastando a computação estocástica com métodos digitais clássicos.

Nota: Este projeto é puramente educacional e experimental, focado na visualização de conceitos avançados de Spintrônica e Computação Física.

📚 Contexto Físico
A simulação baseia-se na implementação de P-Bits descrita por Camsari, Sutton e Datta (Nature, 2017). O estado de um bit flutua estocasticamente entre 0 e 1, influenciado por seus vizinhos e uma temperatura termodinâmica.

A probabilidade de o spin ser +1 (UP) é governada pela função de ativação sigmoide (tangente hiperbólica):

P(σ=+1)=21​[1+tanh(β⋅h)] Onde:

β: Inverso da temperatura (1/T). Quanto maior a temperatura, mais "barulho" ou aleatoriedade.
h: Campo local, resultante da soma das interações dos vizinhos (J) e do campo externo/bias (Hext​).
✨ Funcionalidades
Visualização em Tempo Real: Grid de 40x40 células representando spins individuais.
Interface Estilo Cyberpunk: Monitoramento visual de alto contraste para facilitar a leitura de dados termodinâmicos.
Painel de Controle Interativo:
Temperatura (T): Controla a entropia do sistema (ruído térmico).
Campo Externo (Bias): Simula a força do dado lido de uma memória NAND Flash tentando alinhar o spin.
Acoplamento (J): Controla a força de interação (ferromagnetismo) entre vizinhos.
Inspetor de Célula: Visualização matemática detalhada de uma célula aleatória (Valor h, tanh, Random e Spin final).
Simulação Assíncrona: Emula a natureza física onde MTJs (Magnetoresistência Túnel) atualizam independentemente, não em ciclos de clock síncronos.
🚀 Como Executar
Não requer instalação de Node.js, Python ou dependências complexas. É HTML puro.

Opção 1: GitHub Pages (Recomendado)
Siga o guia passo a passo que enviei anteriormente para hospedar este código gratuitamente online.

Opção 2: Localmente
Clone este repositório ou baixe o arquivo index.html.
Dê um duplo clique no arquivo index.html.
O simulador abrirá no seu navegador padrão.
🎮 Controles e Uso
Parâmetro	Slider Range	Efeito na Simulação
Temperatura	0.1 - 5.0	Baixo (<1.0): O sistema "congela" em domínios estáveis (menos erro).
Alto (>3.0): Sistema entra em estado de caos térmico (aleatoriedade).
Campo Externo (Bias)	0 - 5.0	Força um alinhamento preferencial (Up). Se 0, o sistema segue apenas a interação vizinha.
Acoplamento (J)	0 - 2.0	Define se os vizinhos se gostam (ferromagnético) ou não. 0 significa partículas independentes.
Botões
Pausar Simulação: Congela o estado da grade para análise.
Inverter Spins Aleatórios: Injeta "caos" na grade, forçando o sistema a relaxar novamente para um estado de menor energia.
🛠️ Estrutura Técnica
Frontend: HTML5, CSS3 (Grid Layout), JavaScript Vanilla (ES6+).
Otimização: Utiliza requestAnimationFrame para animações fluidas e atualização de subconjuntos de células para manter alta performance no navegador (evitando travar a UI).
Algoritmo: Modelo de Ising com Condições de Contorno Periódicas (Toroidal), onde a borda direita toca a esquerda e a de baixo toca a de cima.
📄 Licença
Este projeto é licenciado sob a Licença MIT - veja o arquivo LICENSE para detalhes.

📚 Referências Científicas
Camsari, K. Y., Sutton, B. M., & Datta, S. (2017). "Massively parallel probabilistic computing with Ising chips." Nature Communications, 8(1), 1-10.
Sutton, B. M., et al. (2017). "In-Memory Computing with Probabilistic Spin Logic."
👨‍💻 Autor
[Tiago B. D. Maciel ] 
Divirta-se explorando a física dos bits probabilísticos! 🚀
