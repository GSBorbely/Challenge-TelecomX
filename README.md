# **Telecom X - Análise de Evasão de Clientes**

A Telecom está passando por problemas no grande aumento de evasões de clientes e este projeto teve como objetivo demonstrar maneiras de evitar estas evasões (churn) buscando formas de entender quais foram os motivos que influenciaram esta decisão. Após a análise dos dados de diversas váriaveis, foram identificados fatores predominantes que possivelmente foram a razão destas evasões. 

Neste projeto foi utilizada a linguagem de programação Python e suas bibliotecas para analisar os dados, extrair as informações e aplicá-las nas tomadas de decisões. 

# **Extração dos Dados**
Os dados foram extraidos através de uma API em formato JSON

# Objetivos do Projeto
* Analisar os dados e entender os motivos das evasões
* Apresentar insights através da análise de dados
* Apresentar conclusões relacionadas a análise
* Apresentar recomendações após a análise e oferecer soluções para a diminuição das evasões

 # **Análise do Dataset e o tratamento das inconsistências**
Após observar os dados do Dataset, foi preciso normalizar as tabelas que estavam aninhadas. Normalizei cada uma das colunas e inseri cada uma delas em dataframes diferentes para facilitar suas leituras. Após normaliza-las, juntei-as a tabela original com o pd.concat. Depois de concatená-las observei cada uma das colunas em busca de inconsistência nos dados;

*   Encontrei na tabela 'Churn' 224 linhas sem valor, alterando-as para "Unknown'
*  Coluna account_Charges.Monthly: Alteração no tipo da coluna para Float64, possibilitando a manipulação dos valores. Alterei também os 11 valores que estavam vazios, tornando-os NaN com a importação da Biblioteca Numpy.

*   Dataframe separado para eliminar os valores abaixo de 0 na tabela customer_tenure, facilitando assim os cálculos posteriormente.

Após o tratamento das inconsistências, criei a coluna account_charges_Daily, que foi utilizada para ter uma visão mais detalhada dos dados. 

# **Padronização e Transformação de Dados**

*   Transformação da coluna Churn em valores binários para facilitar o cálculo de evasões. Resolvi criar uma outra coluna para manter os dados originais.

*  Transformação da coluna customer_gender em valores binários para facilitar o 
cálculo da média de gênero.

*   Transformação dacoluna customer_Partner em valores binários para facilitar o cálculo da média de parceiros.

*   Transformação da coluna customer_Dependents em valores binários para facilitar o cálculo da média de dependentes.

*  Transformação da coluna phone_PhoneService em valores binários para facilitar o cálculo da média da quantidade de clientes com serviço telefônico.

*   Transformação da coluna account_PaperlessBilling em valores binários para facilitar o cálculo da média da quantidade de clientes com Fatura digital

  # **Análise Descritiva**
Após a análise dos dados foi possivel obter alguns insights. Inicialmente o objetivo foi identificar a porcentagem de Evasões.
