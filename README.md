# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

## Execução:

- Selecionado dataset [dataset-1000-com-preco-promocional-e-renovacao-estoque.csv]
- Utilizado o tipo Quick Build
- O forecast na variável Quantidade_Estoque

## Resultados

- A variável Preço impacta em 60.54% o forecast

### Métricas
- Avg wQL = 0.346 -> mede o erro na previsão ponderado por cada variável, na distribuição da variável target. Quanto mais perto de zero, melhor.
- MAPE = 0.971 -> média de erro das previsões, em relação aos valores reais, em porcentagens. Quanto mais perto de zero, melhor.
- WAPE = 0.581 -> média de erro das previsões, em relação aos valores reais, mas com ponderações de itens de maior importância. Quanto mais perto de zero, melhor.
- RMSE = 36.006 -> raiz quadrada dos erros quadráticos, resultando na diferença média entre valor previsto e real, o que realça grandes erros. Quanto mais perto de zero, melhor.
- MASE = 0.852 -> comparação do erro do forecast com um modelo simples. Espera-se que seja < 1.
<br/>
Como observado, as métricas do dataset não são boas. Ele precisa ser trabalhado e, certamente, treinado no tipo Stardart ajudará também a melhorar a situação, pois este perde em velocidade porém ganha em qualidade. 
  

 ![image](https://github.com/user-attachments/assets/b96fc696-34e6-4873-8638-75282a6c90e9)



### Um exemplo de forecast para o item 18:
- P50 = 61 -> o percentil 50 indica a média esperada na previsão, o planejamento médio de reposição de estoque considerando contextos de demandas comuns.
- P10 = 36 -> o percentil 10 indica o limite onde vão abaixo dos 10% das previsões, condizente com cenários de baixa demanda.
- P90 = 95 -> o percentil 90 indica o limite onde vão acima dos 90% das previsões, condizente com cenários de alta demanda.

Com estes tipos de valores, combinados com tendências de mercado e decisões de investimento da própria empresa, é possível criar análises baseadas em dados para embasar melhores decisões de negócios. 

![image](https://github.com/user-attachments/assets/363dfa20-0c3a-40cf-9dcd-05ed797a0d53)




<br/>


A ferramenta é muito poderosa e versátil. Possui opções para conexão com diversos DB, vários tipos de análise, opções de exportação. Pareceu bom.


<br/>
<br/>





# Instruções do Laboratório

## 📋 Pré-requisitos

Antes de começar, certifique-se de ter uma conta na AWS. Se precisar de ajuda para criar sua conta, confira nosso repositório [AWS Cloud Quickstart](https://github.com/digitalinnovationone/aws-cloud-quickstart).


## 🎯 Objetivos Deste Desafio de Projeto (Lab)

![image](https://github.com/digitalinnovationone/lab-aws-sagemaker-canvas-estoque/assets/730492/72f5c21f-5562-491e-aa42-2885a3184650)

- Dê um fork neste projeto e reescreva este `README.md`. Sinta-se à vontade para detalhar todo o processo de criação do seu Modelo de ML para uma "Previsão de Estoque Inteligente".
- Para isso, siga o [passo a passo] descrito a seguir e evolua as suas habilidades em ML no-code com o Amazon SageMaker Canvas.
- Ao concluir, envie a URL do seu repositório com a solução na plataforma da DIO.


## 🚀 Passo a Passo

### 1. Selecionar Dataset

-   Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de ML. Sinta-se à vontade para gerar/enriquecer seus próprios datasets, quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
-   Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
-   Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.
