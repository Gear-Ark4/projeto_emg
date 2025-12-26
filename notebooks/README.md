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