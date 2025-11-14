# README: Digital Audio Transmission Simulation in Jupyter Notebook using Pulse Code Modulation and Line Coding

This project simulates a complete digital audio transmission system using Python in a Jupyter Notebook environment.

## Prerequisites
- Python 3.6+
- Jupyter Notebook
- Python libraries: NumPy, SciPy, Matplotlib, PyGame

Install the required dependencies:
```bash
pip install numpy scipy matplotlib pygame notebook
```

## How to Run
1. Start the Jupyter Notebook:
```bash
jupyter notebook
```
2. Open the notebook file `Simulacao_Transmissao_Digital.ipynb`
3. Run the cells in sequence:
   - To run all cells: Kernel > Restart & Run All
   - To run cells individually: Shift+Enter

## Notebook Structure

### 1. Initial Setup
- Importing libraries
- Global parameters (bits per sample, SNR range)

### 2. Audio Processing
- Read WAV file
- Normalization and PCM quantization
- Binary encoding (8 bits/sample)

### 3. Line Coding Schemes
- Implementation of three schemes:
  - On-Off (1 → 1V, 0 → 0V)
  - Polar (1 → +1V, 0 → -1V)
  - Manchester (1 → [+1, -1], 0 → [-1, +1])

### 4. Channel Simulation
- Adding AWGN noise
- Threshold detection
- Calculation of BER (Bit Error Rate)

### 5. Results Analysis
- Comparative BER vs. SNR chart
- Waveform visualizations
- Performance statistics

## Expected Outputs
1. **BER vs. SNR Chart**: Comparison of the performance of the three coding schemes
2. **Signal Visualizations**:
   - Original waveform
   - Quantized signal
   - Encoded signals
   - Noisy signals
3. **Statistics**:
   - Error rate for each coding scheme
   - Signal and noise power
   - Number of transmitted bits

## Recommendations
1. Use short WAV files for quick simulation
2. For better audio quality, increase `BITS_PER_SAMPLE`
3. Adjust the SNR range to test different noise scenarios

## Customization
Adjust these parameters in the second cell:
```python
AUDIO_FILE = "your_audio.wav"      # Input file
BITS_PER_SAMPLE = 8                # Quantization resolution
SNR_dB = np.arange(SNR_MIN, SNR_MAX + SNR_STEP, SNR_STEP) # dB              
```

## Expected Results
- **Best performance**: Polar coding
- **Worst performance**: On-Off coding
- **Manchester**: Intermediate, with synchronization advantage


# README: Simulação de Transmissão Digital de Áudio em Jupyter Notebook a partir da Pulse Code Modulation e Codificação de Linha

Este projeto simula um sistema completo de transmissão digital de áudio usando Python em um ambiente Jupyter Notebook.

## Pré-requisitos
- Python 3.6+
- Jupyter Notebook
- Bibliotecas Python: NumPy, SciPy, Matplotlib, PyGame

Instale as dependências:
```bash
pip install numpy scipy matplotlib pygame notebook
```

## Como Executar
1. Inicie o Jupyter Notebook:
```bash
jupyter notebook
```
2. Abra o notebook `Simulacao_Transmissao_Digital.ipynb`
3. Execute as células sequencialmente:
   - Todas as células: Kernel > Restart & Run All
   - Células individuais: Shift+Enter

## Estrutura do Notebook

### 1. Configuração Inicial
- Importação de bibliotecas
- Parâmetros globais (bits por amostra, faixa de SNR)

### 2. Processamento de Áudio
- Leitura de arquivo WAV
- Normalização e quantização PCM
- Codificação para binário (8 bits/amostra)

### 3. Codificações de Linha
- Implementação de três esquemas:
  - On-Off (1 → 1V, 0 → 0V)
  - Polar (1 → +1V, 0 → -1V)
  - Manchester (1 → [+1,-1], 0 → [-1,+1])

### 4. Simulação de Canal
- Adição de ruído AWGN
- Detecção por limiar
- Cálculo de BER (Bit Error Rate)

### 5. Análise de Resultados
- Gráfico comparativo BER vs SNR
- Visualização de formas de onda
- Estatísticas de desempenho

## Saídas Esperadas
1. **Gráfico BER vs SNR**: Comparação do desempenho das três codificações
2. **Visualizações de Sinais**:
   - Forma de onda original
   - Sinal quantizado
   - Sinais codificados
   - Sinais com ruído
3. **Estatísticas**:
   - Taxa de erro para cada codificação
   - Potência do sinal e ruído
   - Número de bits transmitidos

## Recomendações
1. Usar arquivos WAV curtos para simulação rápida
2. Para melhor qualidade de áudio, aumente `BITS_POR_AMOSTRA`
3. Ajuste a faixa de SNR para observar diferentes cenários de ruído


## Personalização
Ajuste estes parâmetros na segunda célula:
```python
ARQUIVO_AUDIO = "seu_audio.wav"  # Arquivo de entrada
BITS_POR_AMOSTRA = 8             # Resolução de quantização
SNR_dB = np.arange(SNR_MIN , SNR_MAX + PASSO_SNR , PASSO_SNR) #dB              
```

## Resultados Esperados
- **Melhor desempenho**: Codificação Polar
- **Pior desempenho**: Codificação On-Off
- **Manchester**: Intermediário, com vantagem de sincronismo

