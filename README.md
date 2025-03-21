# PrevisaoSorvetes
# Prevendo Vendas de Sorvete com Azure ML e MLflow

## Visão Geral do Projeto
Este projeto tem como objetivo prever a quantidade de vendas de sorvete com base em dados históricos de temperatura e preço. Utilizando **Python** com **Azure Machine Learning (Azure ML)** e **MLflow** para construir e registrar um modelo de regressão.

## 📌 Estrutura do Projeto
- **`data/`**: Contém o arquivo de dados `tabela_sorvete.xlsx`.
- **`src/`**: Contém o código Python para carregar os dados, treinar o modelo e registrar no MLflow.
- **`readme.md`**: Documento explicativo sobre o projeto.

---

## 🚀 **Passo a Passo da Implementação**
### 1️⃣ **Configuração do Azure ML**
1. Criar um workspace no **Azure Machine Learning**.
2. Subir o arquivo de dados (`tabela_sorvete.xlsx`) para o workspace.

### 2️⃣ **Carregar os Dados**
**Problema encontrado:**
- Inicialmente, houve um erro de **UnicodeDecodeError** ao carregar os dados.
- Solução: Ajustei a codificação ao ler o arquivo com `encoding="ISO-8859-1"`.

### 3️⃣ **Treinamento do Modelo**
1. Separar os dados em **treino** e **teste** usando `train_test_split`.
2. Treinar um modelo de **regressão linear** com `LinearRegression()`.
3. Avaliar o modelo com o **erro quadrático médio (MSE)**.

### 4️⃣ **Registro no MLflow**
1. Configurar o tracking URI do **MLflow** para o Azure ML.
2. Criar e registrar um experimento no MLflow.
3. Armazenar o modelo treinado e métricas de desempenho.


## 🔍 **Insights Obtidos**
🔹 **Importância da Limpeza dos Dados**: Pequenos erros, como colunas com espaços extras ou caracteres especiais, podem impedir a execução do código.

🔹 **Uso do MLflow**: Muito útil para versionar experimentos e comparar modelos.

🔹 **Integração com Azure ML**: O pipeline fica mais escalável, permitindo monitorar experimentos em tempo real.

---

Projeto desenvolvido como parte da exploração do Azure ML e MLflow. 🚀

