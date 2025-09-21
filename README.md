# Projeto: Simulação de Circuitos Quânticos com Qiskit

Este projeto demonstra a criação, simulação e visualização de **circuitos quânticos simples** utilizando o **Qiskit**, a biblioteca de computação quântica da IBM.

---

## Tecnologias Utilizadas

- Python 3.x  
- Qiskit (`qiskit`, `qiskit-aer`, `qiskit-ibm-runtime`)  
- Matplotlib (para visualização de circuitos e histogramas)

---

## Funcionalidades

1. **Criação de Circuitos Quânticos**  
   - Circuito de 2 qubits com portas Hadamard e CNOT.  
   - Circuito de 1 qubit para medições probabilísticas.

2. **Simulação de Circuitos**  
   - Utilização do **Sampler** do Qiskit Aer para simular medições.  
   - Execução do circuito múltiplas vezes (`shots = 1024`) para obter distribuições de probabilidade.

3. **Visualização de Resultados**  
   - Desenho do circuito com `qc.draw("mpl")`.  
   - Histograma mostrando a distribuição dos resultados.


# Exemplos de Circuitos Quânticos com Qiskit ⚛️

Este repositório contém dois exemplos fundamentais de **computação quântica** usando a biblioteca **Qiskit** da IBM. Eles demonstram conceitos-chave como superposição, emaranhamento e medição de forma prática.

---

## 💻 Exemplo 1: Emaranhamento Quântico (Estado de Bell)

Este primeiro script (`bell_state_circuit.py`) cria um circuito com dois qubits que gera um **estado de emaranhamento quântico**, também conhecido como **Estado de Bell**.

### O que o código faz?

1.  **Inicialização do Circuito**: Cria um circuito quântico com dois qubits.
2.  **Porta Hadamard (H)**: Aplica uma porta `Hadamard` ao primeiro qubit. Esta porta o coloca em um estado de superposição, onde ele tem a mesma probabilidade de ser 0 ou 1.
3.  **Porta CNOT (Controlled-NOT)**: Aplica uma porta `CNOT` (também conhecida como `cx`) com o primeiro qubit como controle e o segundo como alvo. A porta CNOT inverte o estado do segundo qubit somente se o primeiro qubit estiver em 1.
4.  **Emaranhamento**: A combinação das portas Hadamard e CNOT cria um **estado de Bell**, onde os dois qubits estão perfeitamente emaranhados. Isso significa que a medição de um qubit instantaneamente determina o estado do outro, independentemente da distância entre eles.

---

## 🔬 Exemplo 2: Superposição e Medição

Este segundo script (`superposition_and_measurement.py`) explora o conceito de superposição em um único qubit e a medição que o "colapsa" para um estado clássico.

### O que o código faz?

1.  **Criação do Circuito**: Cria um circuito com um qubit e um bit clássico. O bit clássico é essencial para armazenar o resultado da medição do qubit.
2.  **Porta Hadamard (H)**: Aplica uma porta `Hadamard` ao qubit, que o coloca em **superposição** (aproximadamente 50% de chance de ser medido como `0` e 50% como `1`).
3.  **Medição**: Realiza a medição do qubit. A medição é o processo que transforma o estado quântico em um valor clássico, ou seja, força o qubit a "escolher" entre `0` ou `1`.
4.  **Simulação com Sampler**: Utiliza o `Sampler` do Qiskit para executar o circuito um número de vezes (no caso, 1024) em um simulador. O Sampler é a ferramenta mais moderna e recomendada para obter distribuições de probabilidade de medições.
5.  **Análise dos Resultados**: O código obtém a distribuição de probabilidade das medições e as converte em contagens (`counts`).
6.  **Visualização**: Gera um **histograma** para visualizar graficamente a distribuição das contagens (`counts`), mostrando a frequência com que o resultado `0` e `1` foram obtidos.
