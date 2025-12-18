# 🦠 Análise Preditiva de Óbito em Casos de SRAG com IA

📊 **Disciplina:** Introdução à Ciência de Dados – IFB  
👨‍🎓 **Autores:**  
- Marques Herminio  
- Davi Campos Parente  

📅 **Período dos dados:** 2019–2024
🤖 **Modelo inicial:** Regressão Logística  


---

## 📌 Sobre o Projeto


> ⚠️ Os notebooks assumem que os arquivos de dados estejam localizados
> na pasta `./dados`, na raiz do projeto.

---

## 🎯 Objetivo

Este projeto tem como objetivo aplicar técnicas de **Ciência de Dados** e
**Aprendizado de Máquina** para analisar e prever o **desfecho clínico
(óbito ou cura)** de pacientes hospitalizados com **Síndrome Respiratória
Aguda Grave (SRAG)** no Brasil, utilizando dados públicos do período de
**2019 a 2025**.

Busca-se identificar padrões clínicos e epidemiológicos associados a maior
risco de óbito, contribuindo para análises exploratórias e estudos
epidemiológicos em saúde pública.

---

## 📊 Dados e Escopo

- **Fonte:** Base de dados SRAG – OpenDataSUS  
- **Período:** 2019 a 2025  
- **Volume inicial:** Milhões de registros anuais  
- **Amostragem:** Subamostragem aleatória para viabilizar o processamento  
- **População analisada:** Casos hospitalizados com evolução definida  

---

## 🛠️ Metodologia e Pipeline

### 1️⃣ Definição das Variáveis

**Variável Alvo (Target):**
- `EVOLUCAO`
  - 1 → Cura  
  - 2 → Óbito  
- Conversão final para formato binário:
  - 0 → Cura  
  - 1 → Óbito  

**Variáveis Explicativas:**
- Dados demográficos: sexo e raça  
- Sintomas respiratórios: febre, tosse, dispneia, dessaturação  
- Comorbidades: cardiopatia, diabetes, obesidade, asma, imunodepressão  
- Indicadores de gravidade: internação em UTI e suporte ventilatório  
- Situação vacinal contra COVID-19  

---

### 2️⃣ Tratamento dos Dados

- Conversão de variáveis categóricas para formato numérico  
- Filtragem de registros com evolução indefinida  
- Remoção de valores ausentes nas variáveis selecionadas  
- Normalização das variáveis preditoras com `StandardScaler`  
- Divisão da base em conjuntos de treino (70%) e teste (30%) com estratificação  

---

### 3️⃣ Análises Realizadas

- Análise exploratória das variáveis clínicas e demográficas  
- Avaliação do desbalanceamento entre classes  
- Inspeção da correlação entre comorbidades e desfecho  
- Visualização da importância das variáveis no modelo  

---

### 4️⃣ Modelagem Preditiva

**Modelo Utilizado:**
- Regressão Logística para classificação binária  

**Métricas de Avaliação:**
- Acurácia  
- F1-score  
- Área sob a Curva ROC (AUC-ROC)  
- Matriz de Confusão  
- Curva ROC  

O modelo apresentou desempenho inicial satisfatório, com capacidade razoável
de discriminar entre casos de óbito e cura, considerando as limitações
impostas pelo desbalanceamento natural da base.

---

## 🔍 Principais Insights

### 📌 Fatores Associados ao Óbito
- Internação em UTI  
- Uso de suporte ventilatório  
- Baixa saturação de oxigênio  
- Presença de comorbidades crônicas, especialmente cardiopatias e diabetes  

### ⚠️ Desafios Identificados
- Forte desbalanceamento entre as classes  
- Dependência da qualidade do preenchimento das fichas de notificação  
- Limitações no uso de variáveis clínicas autorreferidas  

---

## 🚀 Tecnologias Utilizadas

- **Linguagem:** Python  
- **Bibliotecas:**
  - `pandas` & `numpy` – Manipulação de dados  
  - `matplotlib` & `seaborn` – Visualização  
  - `scikit-learn` – Modelagem preditiva e métricas  
  - `gdown` – Download automatizado dos dados  
  - `os` – Manipulação de arquivos  

---

## 📌 Considerações Finais

Os resultados obtidos demonstram o potencial do uso de técnicas de
Aprendizado de Máquina para apoiar análises epidemiológicas em grandes
bases públicas de saúde. Como trabalhos futuros, pretende-se explorar
outros algoritmos, técnicas de balanceamento e ajustes de
hiperparâmetros para melhoria do desempenho preditivo.

---

📚 *Projeto desenvolvido para a disciplina de Introdução à Ciência de Dados – IFB.*


---

## 🗂️ Estrutura do Repositório

```bash
📁 artigo        # Artigo científico do projeto
📁 dados         # Bases SRAG (2019–2025)
📁 notebooks     # Análises e modelagem
📄 README.md
📄 .gitignore
