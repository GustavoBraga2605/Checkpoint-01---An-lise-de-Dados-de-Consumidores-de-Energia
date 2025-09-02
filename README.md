# Checkpoint-01---Soluções em Energias Renováveis e Sustentáveis
## Integrantes:
Gustavo Cordeiro Braga - RM: 562247
Kaio Correa Fernandes da Conceição - RM: 563443
Murilo Justino Arcanjo - RM: 565470
Rafael Quattrer Dalla Costa - RM: 562052

# Projeto de Predição de Consumo de Energia

Este repositório contém dois notebooks relacionados à análise e previsão do consumo de energia em ambientes domésticos, utilizando diferentes abordagens de **Machine Learning** e análise exploratória de dados.  

## Estrutura do Repositório

- **Dataset_Appliances-Energy-Prediction.ipynb**  
  Notebook focado na previsão do consumo de energia de eletrodomésticos (appliances), explorando séries temporais e modelos preditivos.

- **Dataset_Household-Power-Consumption.ipynb**  
  Notebook baseado no dataset de consumo de energia residencial, com análises exploratórias, tratamento de dados e modelagem.

- **energydata_complete.csv**  
  Base de dados utilizada para os experimentos do primeiro notebook, contendo informações de consumo energético em uma residência ao longo do tempo.

- **household_power_consumption.txt**  
  Base de dados utilizada no segundo notebook, contendo informações detalhadas do consumo energético de uma residência europeia ao longo de 4 anos.

---

## Instruções de Execução

1. Certifique-se de ter instalado o **Python 3.8+** e o **Jupyter Notebook**.  
   Caso não tenha, instale executando:
   ```bash
   pip install jupyterlab
   ```

2. Instale as dependências necessárias (caso não possua):
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```

3. Abra o Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

4. Execute cada célula do notebook em sequência para reproduzir as análises e resultados.

---

## Detalhes dos Datasets

### `energydata_complete.csv`
Este dataset contém registros de consumo de energia em uma residência, coletados a cada 10 minutos.  
Fonte: [UCI Machine Learning Repository – Appliances Energy Prediction Data Set](https://archive.ics.uci.edu/ml/datasets/Appliances+energy+prediction)

#### Principais Colunas:
- **date**: Timestamp da coleta (YYYY-MM-DD HH:MM:SS).  
- **Appliances**: Consumo de energia dos eletrodomésticos (em Wh).  
- **lights**: Consumo de energia das luzes (em Wh).  
- **T1 – T9**: Temperaturas em diferentes áreas da residência (°C).  
- **RH_1 – RH_9**: Umidade relativa em diferentes áreas da residência (%).  
- **T_out**: Temperatura externa (°C).  
- **Press_mm_hg**: Pressão atmosférica (mmHg).  
- **Windspeed**: Velocidade do vento (m/s).  
- **Visibility**: Visibilidade (km).  
- **Tdewpoint**: Ponto de orvalho (°C).  
- **rv1, rv2**: Variáveis aleatórias para teste (sem relevância preditiva).  

#### Características:
- Número de instâncias: ~ 19.735 registros.  
- Frequência de amostragem: 10 minutos.  
- Objetivo: Prever o consumo de energia dos eletrodomésticos a partir das variáveis climáticas e ambientais.  

---

### `household_power_consumption.txt`
Este dataset contém medições de consumo elétrico de uma residência localizada na França, entre **dezembro de 2006 e novembro de 2010**.  
Fonte: [UCI Machine Learning Repository – Individual household electric power consumption Data Set](https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption)

#### Principais Colunas:
- **Date**: Data no formato dd/mm/yyyy.  
- **Time**: Horário da medição (hh:mm:ss).  
- **Global_active_power**: Potência ativa global (kW).  
- **Global_reactive_power**: Potência reativa global (kW).  
- **Voltage**: Tensão (V).  
- **Global_intensity**: Intensidade de corrente global (A).  
- **Sub_metering_1**: Consumo do submedidor 1 (Wh).  
- **Sub_metering_2**: Consumo do submedidor 2 (Wh).  
- **Sub_metering_3**: Consumo do submedidor 3 (Wh).  

#### Características:
- Número de instâncias: ~ 2.075.259 registros.  
- Frequência de amostragem: 1 minuto.  
- Período coberto: 4 anos (2006–2010).  
- Objetivo: Analisar e modelar o consumo energético de uma residência, explorando padrões de uso e possíveis previsões de demanda.  

---

## Comparação dos Datasets Utilizados

- **Appliances Energy Prediction (energydata_complete.csv)**  
  - Dados coletados a cada 10 minutos.  
  - Ênfase em variáveis ambientais (temperatura, umidade, vento, visibilidade).  
  - Foco na previsão de consumo de **eletrodomésticos (Appliances)**.  

- **Household Power Consumption (household_power_consumption.txt)**  
  - Dados coletados a cada 1 minuto.  
  - Ênfase em medições elétricas (potência ativa, reativa, tensão, intensidade).  
  - Foco no **consumo global da residência** e análise de submedidores.  

---

## Entrega

O objetivo desta entrega é:
- Reproduzir e documentar a análise dos dois datasets apresentados.  
- Entender o impacto de variáveis climáticas e de ocupação no consumo energético.  
- Explorar modelos preditivos para prever consumo energético.
