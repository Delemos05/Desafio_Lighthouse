Projeto: Previsão de Preços de Imóveis
Este projeto tem como objetivo prever o preço de imóveis usando dados fornecidos sobre as características dos apartamentos. Utilizamos técnicas de aprendizado de máquina (machine learning) para construir um modelo capaz de estimar os preços com base em variáveis como localização, tipo de imóvel, disponibilidade e outras.

Requisitos
Antes de começar, certifique-se de ter os seguintes requisitos instalados:

Anaconda 3
Jupyter Notebook 
Bibliotecas Utilizadas
As bibliotecas utilizadas no projeto são as seguintes:

pandas: Manipulação e análise de dados
NumPy: Operações matemáticas e vetoriais
Scikit-learn: Algoritmos de machine learning para regressão e métricas de avaliação
Matplotlib: Criação de gráficos e visualizações
Seaborn: Visualização de dados aprimorada (baseada no Matplotlib)
wordcloud: nuvem de palavras
xgboost: metódo de treibamento principal
pickle: usei para criar e ler arquivos pkl onde armazenamos os modelos

Instalação
Siga estas etapas para configurar o ambiente e executar o projeto.

1. Clone o repositório

git clone [https://github.com/seu-usuario/nome-do-projeto.git](https://github.com/Delemos05/Desafio_Lighthouse)
2. Navegue até o diretório do projeto
cd nome-do-projeto
3. Crie um ambiente virtual (opcional)
É altamente recomendado criar um ambiente virtual para manter as dependências isoladas:

4. Instale as dependências
Instale as bibliotecas necessárias para o projeto executando:
conda activate base
conda install -c conda-forge xgboost
conda install -c conda-forge wordcloud



5. Execute o Jupyter Notebook 
jupyter notebook

Estrutura do Projeto

nome-do-projeto/
│
├── teste_indicium_precificacao            # Dataset usado no projeto
│              
│
├── Teste.ipynb               # Notebooks Jupyter com EDA e experimentos
│  
│
├── model_DTR.pkl/model_XBGR.pkl/...                     # Modelos treinados ou scripts de treinamento
│         
│
├── requirements.txt            # Arquivo com as dependências do projeto
│
└── README.md                   # Arquivo com instruções do projeto
Funcionalidades
Análise Exploratória dos Dados (EDA): Inclui gráficos e análises estatísticas para entender as correlações entre as variáveis.
Modelo de Previsão: Utiliza algoritmos de regressão para prever os preços dos imóveis.
Métricas de Avaliação: Avaliação do modelo usando métricas como RMSE, MAE, R².
Treinamento e Validação: Divisão dos dados em conjuntos de treinamento e teste para garantir a precisão do modelo.
Exportação do Modelo: Salvamento do modelo treinado para uso futuro.
Exemplo de Uso
Suponha que você tenha um apartamento com as seguintes características:


apartamento = {
    'nome': 'Skylit Midtown Castle',
    'bairro_group': 'Manhattan',
    'bairro': 'Midtown',
    'latitude': 40.75362,
    'longitude': -73.98377,
    'room_type': 'Entire home/apt',
    'minimo_noites': 1,
    'numero_de_reviews': 45,
    'reviews_por_mes': 0.38,
    'disponibilidade_365': 355
}
O modelo será capaz de prever um preço estimado com base nessas características.

Métricas de Avaliação
Para avaliar a performance do modelo, usamos as seguintes métricas:

RMSE (Root Mean Squared Error): Mede o erro quadrático médio, dando mais peso a grandes erros.
MAE (Mean Absolute Error): Média do erro absoluto entre previsões e valores reais.
R² (Coeficiente de Determinação): Mede a proporção da variação no preço que o modelo é capaz de explicar.
Hipóteses de Negócio
Durante a análise exploratória, foram levantadas as seguintes hipóteses de negócio:

Localização Impacta o Preço: Apartamentos localizados em áreas centrais, como Manhattan, tendem a ser mais caros.
Número de Noites Mínimas e Disponibilidade: Apartamentos com alta disponibilidade ao longo do ano e poucas noites mínimas tendem a ter preços maiores.
Textos e Descrições de Propriedades: Propriedades de alto valor geralmente têm descrições mais elaboradas e sofisticadas.

requirements.txt (Dependências)

Anaconda 3
numpy==1.21.2
scikit-learn==0.24.2
matplotlib==3.4.3
seaborn==0.11.2
joblib==1.0.1
