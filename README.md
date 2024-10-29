# Análise de Dados para Previsão de Preços de Casas

Este projeto realiza uma análise de dados para previsão de preços de casas, utilizando técnicas de engenharia de recursos e modelos preditivos em Python. A base de dados contém informações sobre propriedades residenciais, incluindo características de construção, condições de qualidade, localização, entre outros fatores que influenciam no preço final do imóvel.

## Objetivos

1. **Explorar e tratar os dados**: Compreender a estrutura dos dados, lidar com valores ausentes e realizar transformações necessárias.
2. **Engenharia de Recursos**: Criar novas colunas com informações derivadas, como combinações de qualidade, área total de cômodos e proporções entre quartos e banheiros.
3. **Modelagem Preditiva**: Aplicar algoritmos de aprendizado de máquina para construir um modelo de previsão de preços de casas com base nos dados tratados.

## Estrutura do Projeto

- **data/**: Contém os arquivos de dados utilizados no projeto.
- **notebooks/**: Notebooks Jupyter com os passos de análise, visualização e modelagem dos dados.
- **src/**: Código fonte do projeto, com scripts para pré-processamento, engenharia de recursos e modelos de previsão.
- **README.md**: Descrição geral do projeto e instruções para reprodução.

## Pré-Processamento de Dados

Os principais passos do pré-processamento incluem:

1. **Tratamento de valores ausentes**: Preenchimento de dados faltantes em colunas categóricas e numéricas.
2. **Label Encoding**: Transformação de variáveis categóricas em valores numéricos para o uso nos modelos.
3. **Conversão de Qualidade**: Transformação de colunas de qualidade para uma escala numérica de 1 a 5, onde `Ex = 5` e `Po = 1`, facilitando a comparação de acabamentos e condições gerais.

## Engenharia de Recursos

Foram criados novos recursos que ajudam a melhorar a precisão do modelo, incluindo:

- **ExteriorQuality**: Combinação das colunas `ExterQual` e `ExterCond`.
- **TotalRooms**: Soma do número de quartos e banheiros.
- **LotSizePerRoom**: Proporção entre o tamanho do lote e o total de cômodos.
- **GarageQuality**: Combinação da qualidade e condição da garagem.

Esses novos recursos ajudam a capturar informações complexas sobre a qualidade e o tamanho do imóvel.

## Modelos Preditivos

Modelos de aprendizado de máquina, como Regressão Linear e Random Forest, foram utilizados para prever o preço das casas. Os modelos foram avaliados com métricas como RMSE (Root Mean Squared Error) e R², e o melhor modelo foi escolhido para a previsão final.

## Requisitos

- Python 3.8+
- Pandas
- Scikit-learn
- Jupyter Notebook
