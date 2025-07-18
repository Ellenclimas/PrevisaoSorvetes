# PrevisaoSorvetes
# Prevendo Vendas de Sorvete com Azure ML e MLflow

## Visão Geral do Projeto
Este projeto tem como objetivo prever a quantidade de vendas de sorvete com base em dados históricos de temperatura e preço. Utilizando **Python** com **Azure Machine Learning (Azure ML)** para construir e registrar um modelo de regressão.

  ## 📌 Pastas
- **`data/`**: Contém o arquivo de dados `tabela_sorvete.xlsx`.
- **`src/`**: Contém o código Python para carregar os dados, treinar o modelo e registrar no MLflow.


---

## 🚀 **Processo**
### 1️⃣ **Configuração do ambiente no Azure ML**
1. Criei um workspace no **Azure Machine Learning**.
2. Subi o arquivo de dados (`tabela_sorvete.xlsx`) para o workspace.

### 2️⃣ **Dados**
**Problema encontrado:**
- Inicialmente, houve um erro de **UnicodeDecodeError** ao carregar os dados.
- Solução: Ajustei a codificação ao ler o arquivo com `encoding="ISO-8859-1"`.

### 3️⃣ **Treinamento do Modelo**
1. Separei os dados em **treino** e **teste** usando `train_test_split`.
2. Treinei um modelo de **regressão linear** com `LinearRegression()`.
3. Avaliei o modelo com o **erro quadrático médio (MSE)**.

### 4️⃣ **Registro no MLflow**
1. Configurei o tracking URI do **MLflow** para o Azure ML.
2. Criei e registrei um experimento no MLflow.
3. Armazenei o modelo treinado e métricas de desempenho.


## 🔍 **Insights Obtidos**
🔹 **Importância da Limpeza dos Dados**: Pequenos erros, como colunas com espaços extras ou caracteres especiais, podem impedir a execução do código.

🔹 **Uso do MLflow**: Muito útil para versionar experimentos e comparar modelos.

🔹 **Integração com Azure ML**: O pipeline fica mais escalável, permitindo monitorar experimentos em tempo real.

---

Projeto desenvolvido como parte da exploração do Azure ML e MLflow. 🚀

