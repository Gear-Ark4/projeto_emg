# 🧠 Interface Cérebro-Máquina: Classificação de Gestos via EMG
**Transição de Carreira: Da Biologia à Engenharia de Software Biomédico**

Este projeto demonstra o desenvolvimento de um pipeline completo para processamento de sinais eletromiográficos (EMG) e classificação de gestos utilizando Inteligência Artificial. 

## 🧬 Conectando Biologia e Tecnologia
Como profissional vindo da área de Biologia, utilizei o conhecimento em fisiologia neuromuscular para interpretar os sinais elétricos captados pelo dataset **NinaPro DB2**. O foco foi transformar a despolarização das fibras musculares em comandos digitais.

## 🛠️ Tecnologias e Ferramentas
- **Linguagem:** Python 3.12
- **Processamento de Sinais:** SciPy (Filtro Butterworth Passa-Banda 20-450Hz)
- **Análise de Dados:** Pandas & NumPy
- **Machine Learning:** Scikit-Learn (Random Forest Classifier)
- **Visualização:** Matplotlib
- **Ambiente:** VS Code com Jupyter Notebooks & Virtualenv

## 📈 Pipeline do Projeto
1. **Limpeza Stark:** Aplicação de filtro digital para remoção de ruídos de movimento e interferência elétrica.
2. **Feature Engineering:** Extração de características biométricas (MAV, RMS e Zero Crossing) em janelas de 200ms.
3. **IA:** Treinamento de um modelo capaz de prever intenções de movimento.
4. **Simulação:** Teste em tempo real simulando o acionamento de uma prótese robótica.

## 🚀 Próximos Passos
- [ ] Implementar processamento multicanal (usando os 12 sensores do dataset).
- [ ] Testar arquiteturas de Deep Learning (Redes Neurais).
- [ ] Otimizar a latência para processamento em tempo real.


---

### 🚀 Atualização: Expansão Multicanal (V2.0)

Nesta segunda fase do projeto, realizei a **Expansão Multicanal**, integrando todos os 12 sensores eletromiográficos disponíveis no dataset.

#### Principais Melhorias:
* **Vetorização de Sinais:** Otimização do pipeline para processar matrizes 12x mais densas utilizando computação vetorizada com NumPy.
* **Feature Engineering Multidimensional:** Extração de 36 características biomecânicas simultâneas (12 canais x 3 features: MAV, RMS, ZC).
* **Evolução da IA:** O modelo Random Forest foi recalibrado para lidar com o aumento na complexidade dos dados.

#### Resultados Obtidos:
* **Acurácia Inicial (1 Sensor):** 41.07%
* **Nova Acurácia (12 Sensores):** **73.69%**

#### 🔬 Análise Crítica
A expansão demonstrou que a sinergia entre diferentes grupos musculares é fundamental para a precisão do movimento. Embora o sistema já seja funcional para próteses básicas, identifiquei divergências pontuais em gestos complexos (ex: Gesto 2 vs Gesto 4). Este comportamento é esperado dada a similaridade morfológica de certos movimentos do antebraço e serve de base para as próximas otimizações de filtragem.

---

### 🗺️ Próximos Passos (Roadmap de Otimização)

Para elevar o sistema ao nível de aplicação clínica (Acurácia > 90%), os próximos "cortes" técnicos planejados são:

#### 1. Incremento de Features no Domínio do Tempo
Adição de características que capturam a dinâmica da variação do sinal:
* **Waveform Length (WL):** Para medir a complexidade acumulada da forma de onda.
* **Slope Sign Change (SSC):** Para identificar variações na frequência dominante e fadiga muscular.

#### 2. Implementação de Janelas com Sobreposição (Sliding Windows)
Atualmente as janelas são estáticas. A implementação de *overlap* de 50% permitirá que o modelo aprenda as transições entre gestos, reduzindo divergências como a observada entre o Gesto 2 e 4.

#### 3. Otimização de Hiperparâmetros
Utilização de `GridSearchCV` para encontrar a configuração ideal da "Random Forest" (profundidade das árvores e número de estimadores), visando minimizar o erro em gestos morfologicamente similares.

#### 4. Deep Learning (Futuro)
Migração da arquitetura para Redes Neurais Convolucionais (CNN) ou LSTM, permitindo que a própria rede aprenda filtros espaciais entre os 12 sensores.
