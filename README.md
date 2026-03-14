# Previsão de Preços de Imóveis no Airbnb (Rio de Janeiro)

![Python](https://img.shields.io/badge/Python-3.x-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Scikit--Learn-orange)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen)

## Contexto do Projeto

Neste projeto foi desenvolvido um modelo de Machine Learning capaz de prever o preço de imóveis anunciados no Airbnb no Rio de Janeiro com base nas características do imóvel.

O projeto simula um cenário real de análise de dados onde é necessário:

- Analisar um dataset real
- Limpar e tratar os dados
- Explorar padrões presentes nas informações
- Construir modelos de previsão
- Comparar diferentes algoritmos de Machine Learning

Todo o processo foi realizado utilizando Python e bibliotecas de análise de dados e aprendizado de máquina.

---

## Objetivo

O objetivo deste projeto é construir um modelo capaz de **estimar o preço de um imóvel no Airbnb** com base em variáveis como:

- capacidade de hóspedes
- número de quartos
- número de banheiros
- número de camas
- tipo de acomodação
- localização
- comodidades disponíveis

Além da construção do modelo, o projeto também busca entender **quais fatores mais influenciam na formação do preço dos anúncios**.

---

## Etapas do Projeto

O desenvolvimento foi dividido nas seguintes etapas:

1. Importação e análise inicial do dataset  
2. Limpeza e tratamento de dados  
3. Remoção de outliers  
4. Engenharia de variáveis  
5. Análise exploratória de dados (EDA)  
6. Preparação dos dados para Machine Learning  
7. Treinamento de múltiplos modelos  
8. Comparação de desempenho entre modelos  
9. Seleção das variáveis mais importantes  
10. Treinamento do modelo final

---

## Modelos Testados

Durante o projeto foram testados diferentes algoritmos de regressão:

- Linear Regression
- Random Forest Regressor
- Extra Trees Regressor
- Gradient Boosting Regressor
- HistGradientBoosting Regressor

---

## Resultados Obtidos

O melhor desempenho foi obtido utilizando o modelo **HistGradientBoostingRegressor**.

Resultados aproximados:

| Modelo | R² | Erro Médio (MAE) |
|------|------|------|
| Linear Regression | 0.43 | 204 |
| Random Forest | 0.56 | 166 |
| Extra Trees | 0.54 | 164 |
| Gradient Boosting | 0.54 | 172 |
| HistGradientBoosting | **0.59** | **159** |

O modelo final conseguiu explicar aproximadamente **59% da variação dos preços presentes no dataset**.

---

## Tecnologias Utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook

---

## Estrutura do Projeto

```
📁 dataset/
│
├── abril_2018.csv
├── abril2019.csv
├── abril2020.csv
│
📄 data_science.ipynb
📄 modelo_airbnb.pkl
📄 README.md
📄 requirements.txt
```

## Como Executar o Projeto

### 1 - Clonar o repositório

```
git clone <url-do-repositorio>
```

Entrar na pasta:

```
cd nome-do-repositorio
```

### 2 - Criar ambiente virtual

```
python -m venv venv
```

### 3 - Ativar o ambiente

Windows:

```
venv\Scripts\activate
```

### 4 - Instalar dependências

```
pip install -r requirements.txt
```

### 5 - Abrir o notebook

```
jupyter notebook
```

Abra o arquivo:

```
data_science.ipynb
```

## Dataset

O dataset utilizado contém informações sobre anúncios do Airbnb no Rio de Janeiro, incluindo características dos imóveis, localização e preços.

O conjunto de dados utilizado corresponde à versão utilizada durante o desenvolvimento do projeto (dados de 2019).

Devido ao tamanho do dataset, os arquivos **não estão incluídos neste repositório**.

### Download do dataset

O dataset pode ser baixado no link abaixo:

https://drive.google.com/drive/folders/1rkHsGUynA0RNRliQ7aXAvS9PotNTQVV8?usp=sharing

Após baixar o dataset, extraia os arquivos e coloque-os dentro da pasta:

```
dataset/
```

## Possíveis Melhorias Futuras

Algumas melhorias que podem ser implementadas:

- Aplicação de técnicas mais avançadas de feature engineering
- Criação de uma API para previsão de preços
- Construção de um dashboard interativo

## Utilização do Modelo

Após o treinamento, o modelo final pode ser salvo utilizando a biblioteca `joblib`.

Exemplo:

```
import joblib

joblib.dump(modelo_final, "modelo_airbnb.pkl")
```

## Conclusão

Este projeto demonstra a aplicação prática de um fluxo completo de Data Science, incluindo preparação de dados, análise exploratória e construção de modelos de Machine Learning.

A análise revelou que variáveis relacionadas ao tamanho do imóvel, capacidade de hóspedes e tipo de acomodação possuem forte influência na formação do preço dos anúncios.

O modelo final desenvolvido pode servir como base para sistemas de estimativa de preços ou ferramentas de apoio à decisão para anfitriões da plataforma.

Projeto desenvolvido para fins de estudo, prática e construção de portfólio.
