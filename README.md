# Projeto Machine Learning

## Contexto e Descrição do Problema/Dor de Negócio

O regime de cotas na geração de energia é um sistema no qual os produtores de energia têm uma quantidade pré-estabelecida de energia que devem produzir em um determinado período. Produtores que não atingem suas cotas de geração de energia podem ser submetidos a penalidades. No contexto do Brasil, o regime de cotas é particularmente relevante para incentivar a produção de energia através de fontes renováveis, contribuindo para a redução de emissões de gases de efeito estufa e para a segurança e diversificação da matriz energética nacional.
Portanto, o propósito principal deste projeto é emular um cenário onde se pretende prever a geração para fins de mitigar possíveis penalizações decorrentes da não conformidade com os regimes de cotas. Neste sentido, para fins de exemplificação de como poderia ser desenvolvido um modelo preditivo, serão utilizados os dados de energias renováveis intermitentes (eólica e solar) do subsistema do Nordeste do Brasil, gerados a partir dos dados de Balanço de Energia nos Subsistemas do Brasil, disponibilizados pelo Operador Nacional do Sistema Elétrico (ONS).

1) **Dados Disponíveis**
Para emular usinas híbridas de geração (eólica e solar) o projeto se baseia em dados disponibilizados pelo ONS (Balanço de Energia nos Subsistemas de 2014 a 2023).

2) **Aplicação de Machine Learning**
Machine Learning é utilizado para modelar e prever a geração de energia renovável. Por meio de algoritmos de aprendizado, busca-se identificar padrões na série temporal e realizar previsões precisas para futuras gerações de energia.

3) **Utilização do Modelo no Dia-a-Dia**
O modelo servirá como uma ferramenta para operadores e gestores de energia, auxiliando na tomada de decisões estratégicas e operacionais, tais como ajustes na produção, para conformidade com as cotas de geração.

4) **Métrica de Avaliação**
A eficácia do modelo é avaliada por métricas como MAE, MSE, RMSE, MAPE e PDA e explained_variance_score, que quantificam a diferença entre os valores previstos e reais, permitindo uma análise robusta do desempenho do modelo.

5) **Avaliação do Modelo (Desenho do Piloto)**
A avaliação será realizada através de comparação entre as previsões do modelo e os dados reais dos meses de 2023, permitindo identificar os ajustes necessários para melhorar a precisão do modelo.
 

# Estrutura da Análise de Dados
![image](https://github.com/arnaldorosentino/MBA_ML_Projetc/assets/104164948/69317c91-134c-459a-84d9-cd5e448ff4b2)

## 1) Inicialização (Importação de Bibliotecas)
   É a fase onde se importam as bibliotecas necessárias para realizar a análise de séries temporais. As bibliotecas são conjuntos de funções e métodos que permitem a execução de tarefas específicas na análise.

## 2) Importação e Ajuste de Dataset (Tratamento dos Dados)
   Importa-se o conjunto de dados e realiza-se ajustes necessários, como limpeza e transformação de dados, para garantir que estão em um formato adequado para análise.

## 3) Análise Exploratória e Pré-Processamento
   Aqui, a série temporal é visualizada, decomposta em seus componentes (tendência, sazonalidade e ruído) e avaliada quanto à sua estacionariedade. Utiliza-se teste de Dickey Fuller para analisar a estacionaridade e, se necessário, aplica-se diferenciação para tornar a série estacionária. A Análise de Autocorrelação (ACF) e Autocorrelação Parcial (PACF) também é realizada nesta etapa.

## 4) Modelagem
   São aplicados diferentes modelos estatísticos, como AR, MA, ARMA e ARIMA, para encontrar o melhor modelo preditivo. A qualidade destes modelos é avaliada por meio de métricas de erro.

## 5) Transformação Inversa e Previsões Futuras
   Após a modelagem com a série transformada, realiza-se uma transformação inversa para visualizar os dados em sua escala original e efetuar previsões futuras.
