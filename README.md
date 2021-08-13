# Churn Prediction

Disclaimer: O Contexto a seguir, é completamente fictício, a empresa, o contexto, as perguntas de negócio foram criadas apenas para o desenvolvimento do projeto, e se baseiam em um projeto do site https://sejaumdatascientist.com/.

<p align="center">
  <img width="1000" height="400" src="https://www.callcentrehelper.com/images/stories/2020/05/penny-jar-760.jpg"/>
</p>

## Contexto de negócio

A TopBank é uma grande empresa de serviços bancários. Ela atua principalmente nos países da Europa oferecendo produtos financeiros, desde contas bancárias até investimentos, passando por alguns tipos de seguros e produto de investimento.

O modelo de negócio da empresa é do tipo serviço, ou seja, ela comercializa serviços bancários para seus clientes através de agências físicas e um portal online. 

O principal produto da empresa é uma conta bancária, na qual o cliente pode depositar seu salário, fazer saques, depósitos e transferência para outras contas. Essa conta bancária não tem custo para o cliente e tem uma vigência de 12 meses, ou seja, o cliente precisa renovar o contrato dessa conta para continuar utilizando pelos próximos 12 meses.

Segundo o time de Analytics da TopBank, cada cliente que possui essa conta bancária retorna um valor monetário de 15% do valor do seu salário estimado, se esse for menor que a média e 20% se esse salário for maior que a média, durante o período vigente de sua conta. Esse valor é calculado anualmente. 

Por exemplo, se o salário mensal de um cliente é de R$1.000,00 e a média de todos os salários do banco é de R$800. A empresa, portanto, fatura R$ 200 anualmente com esse cliente. Se esse cliente está no banco há 10 anos, a empresa já faturou R$2.000,00 com suas transações e utilização da conta. 

Nos últimos meses, o time de Analytics percebeu que a taxa de clientes cancelando suas contas e deixando o banco, atingiu números inéditos na empresa. Preocupados com o aumento dessa taxa, o time planejou um plano de ação para diminuir taxa de evasão de clientes.

Preocupados com a queda dessa métrica, o time de Analytics da TopBottom, contratou você como consultor de Data Science para criar um plano de ação, com o objetivo de reduzir a evasão de clientes, ou seja, impedir que o cliente cancele seu contrato e não o renove por mais 12 meses. Essa evasão, nas métricas de negócio, é conhecida como Churn.

## O Desafio

Como um Consultor de Ciência de Dados, você precisa criar um plano de ação para diminuir o número de clientes em churn e mostrar o retorno financeiro da sua solução.

Ao final da sua consultoria, você precisa entregar ao CEO da TopBottom um modelo em produção, que receberá uma base de clientes via API e retornará essa mesma base “scorada”, ou seja, um coluna à mais com a probabilidade de cada cliente entrar em churn.

Além disso, você precisará fornecer um relatório reportando a performance do seu modelo e o impacto financeiro da sua solução. Questões que o CEO e o time de Analytics gostariam de ver em seu relatório:

1. Qual a taxa atual de Churn da TopBank? Como ela varia mensalmente?
2. Qual a Performance do modelo em classificar os clientes como churns?
3. Qual o retorno esperado, em termos de faturamento, se a empresa utilizar seu modelo para evitar o churn dos clientes?

Uma possível ação para evitar que o cliente entre em churn é oferecer um cupom de desconto, ou alguma outro incentivo financeiro para ele renovar seu contrato por mais 12 meses.

Para quais clientes você daria o incentivo financeiro e qual seria esse valor, de modo a maximizar o ROI (Retorno sobre o investimento). Lembrando que a soma dos incentivos não pode ultrapassar os  R$10.000,00

## Dados

O conjunto de dados que será utilizado para criar a solução para a TopBottom, está disponível na plataforma do Kaggle. Esse é o link: https://www.kaggle.com/mervetorkan/churndataset

Cada linha representa um cliente e cada coluna contém alguns atributos que descrevem esse cliente. O conjunto de dados inclui informações sobre:

- RowNumber: O número da coluna

- CustomerID: Identificador único do cliente

- Surname: Sobrenome do cliente.

- CreditScore: A pontuação de Crédito do cliente para o mercado de consumo.

- Geography: O país onde o cliente reside.

- Gender: O gênero do cliente.

- Age: A idade do cliente.

- Tenure: Número de anos que o cliente permaneceu ativo.

- Balance: Valor monetário que o cliente tem em sua conta bancária.

- NumOfProducts: O número de produtos comprado pelo cliente no banco.

- HasCrCard: Indica se o cliente possui ou não cartão de crédito.

- IsActiveMember: Indica se o cliente fez pelo menos uma movimentação na conta bancário dentro de 12 meses.

- EstimateSalary: Estimativa do salário mensal do cliente.

- Exited: Indica se o cliente está ou não em Churn.

## Planejamento da solução

**1. Entendimento do negócio e problemas e serem resolvidos** - Buscar entender os reais motivos da necessidade da previsão de churn e como o probelma pode ser resolvido através de machine learning, quais aspectos serão considerados na hora da predição e quão melhor a solução proposta pode ser considerando os modelos de predição utilizados atualmente na empresa.    

**2. Coleta de dados** - Acesso a plataforma do Kaggle para download dos arquivos que serão usados.

**3. Limpeza dos dados** - Os dados são analisados usando diferentes técnicas para verificar a existência de dados faltantes, outliers (valor discrepantes) , ou qualquer tipo de inconsistências para que assim possam ser tratados devidamente e não impactar nas análises futuras. 

**4. Exploração dos dados** - Busca um melhor entendimento do negócio através da geração de insights e das variáveis mais importantes na modelagem do modelo de Machine Learning. Diversas hipóteses foram levantadas e validadas para obtenção de um conhecimento de negócio mais profundo, verificando também a correlação entre os atributos para que se possa ter uma ideia da importância de cada um para o modelo de machine learning. 

**5. Preparação dos dados** - Os dados foram transformados, balanceados e regularizados para que atendam as premissas de funcionamento dos algoritmos de machine learning, nesta etapa é importante deixar os dados preparados para que os algoritmos possam ter o melhor desempenho possível, e possíveis inconsistencias no dataset não interfiram no resultado final.

**6. Seleção de features** - Após a preparação dos dados nesta seção algoritmos, como o Boruta e o feature importance, selecionarão as melhores colunas a serem utilizadas para o treinamento do modelo de machine learning. Elas serão analisadas e selecionadas de acordo com descobertas feitas na análise exploratória e levando em conta o contexto de nagócio.

**7. Aplicação dos algoritmos de machine learning** - Nesta etapa foram escolhidos os algoritmos de machine learning que seriam usados e então os mesmos foram treinados com os dados já preparados e prontos, cada algoritmo foi testado usando seus devidos parâmetros e posteriormente estratégias de cross validation foram usadas para verificar o real resultado do medelo, bem como tecnicas de hyperparameter fine tunning para encontrar os melhores parâmetros para o modelo escolhido. 

**8. Avaliação do algoritmo** - O algoritmo é avaliado com base em algumas métricas e nesse ponto verifica-se ou não a necessidade de realizar mais um ciclo para melhorar o desempenho final.

**9. Tradução do erro em métricas de negócio** - Com o melhor modelo escolhido, treinado e otimizado a taxa de erro encontrada é trasnformada em mátricas de negócio para que se saiba concretamente quanto de retorno financeiro aquela solução trouxe para a empresa. 

**10. Deploy do modelo em produção** - O modelo foi colocado em produção no ambiente cloud Heroku para que as predições possam ser utilizadas através de requisições a uma API.

## Melhores Insights

 - **Pesosas que possuem cartão de crédito e são ativas entram mais em churn**
 
<p align="center">
  <img width="650" height="400" src="https://user-images.githubusercontent.com/76128123/125992392-95ebfdd6-4ebc-492f-972c-2778e1ad0b7c.png"/>
</p>
 

 - **Mulheres entram 27% a mais em churn do que homens**
 
 <p align="center">
  <img width="650" height="400" src="https://user-images.githubusercontent.com/76128123/125992466-36c62ff3-13f2-4c61-8402-0ff44b9c1f9a.png"/>
</p>
 


 - **Pessoas com salário maior do que a média entram mais em churn**
 
 <p align="center">
  <img width="650" height="400" src="https://user-images.githubusercontent.com/76128123/125992592-7106905c-9cb0-4f84-b055-453c08a4aad4.png"/>
</p>
 


## Machine Learning Models

Os algoritmos utilizados para fazer a predição foram:

- Modelo Dummy Clisifier para que fosse possível ter um modelo base de comparação,
- Logistic Regression;
- KNN;
- Naive Bayes;
- SVC;
- Random Forest Classifier;
- XGBoost Classifier.

Após a realização dos testes com todos os algoritmos e verificação das métricas de performnace, verificou-se um melhor desempenho nos algoritmos baseados em árvores ( Random Forest e XBBoost) e então a decisão foi usar o algoritmo XGBoost pois é um algoritmo mais leve do que o Random Forest quando exportado e colocado em produção. 

## Resultados

Através da interpretação do erro do modelo de machine learning e guiado pelas perguntas de negócio foi possível avalia-lo de meneira a agregar valor para o cliete, com os resultados financeiros apresentados a seguir. Os resultados serão exibidos de acordo com as perguntas de negócio propostas no começo do projeto.

**1. Qual a taxa atual de Churn da TopBank?**

 A taxa atual de churn do TopBank é de 20.4%
 
 <p align="center">
  <img width="650" height="400" src="https://user-images.githubusercontent.com/76128123/125993866-a311599c-2949-4d42-826e-87f57a3bb19a.png"/>
</p>
 

  **2. Qual a Performance do modelo em classificar os clientes como churns?**
  
  https://user-images.githubusercontent.com/76128123/125993988-162698d8-55b9-4cba-9c31-86440635f2fe.png
  

  O modelo possuou uma acurácia de 76%, conseguindo identificar os clientes que de fato entraram em churn em 67% dos casos (métrica Recall).
  
  **3. Qual o retorno esperado, em termos de faturamento, se a empresa utilizar seu modelo para evitar o churn dos clientes?**
  
  - Para realização do cálculo de retorno financeiro foi utilizado uma amostra de 1000 clientes (10% do dataset).
  - Para comparação com os dados reais foram utlizados os valores da predição final do modelo.

  
  **O retorno total de todos os clientes que entraram em churn é de $3.658.649,98
  **O retorno total  dos clientes que o modelo previu que entrariam em churn é de $2.540.855,07
   
   - Se fosse possível evitar que todos os clientes entrassem em churn seria possível recuperar aproximadamente 70% do valor total.
 
  **4. Incentivo Financeiro**
  
   Uma possível ação para evitar que o cliente entre em churn é oferecer um cupom de desconto, ou algum outro incentivo financeiro para ele renovar seu contrato por mais 12     meses.

   Para quais clientes você daria o incentivo financeiro e qual seria esse valor, de modo a maximizar o ROI (Retorno sobre o investimento). Lembrando que a soma dos incentivos não pode ultrapassar os $10.000,00
   
   
  Ainda levando em conta a amostra de 1000 clientes, foi possível analisar a probabilidade de cada cliente entrar em churn segundo o algoritmo e decidir de qual forma o incentivo finaceiro seria oferecido. Após algumas análises foram definidas as seguintes estratágias (foram considerados apenas clientes que o algoritmo previu como "positivos" para o churn):
  
  Foi definido um ponto de corte (threshold) de 0.95, ou seja, a probabilidade dos clientes entrarem em churn foi comparada com esse ponto de corte e a partir disso foram definidos "grupos" que receberiam o incentivo.

- Clientes com uma probabilidade de mais de 95% não receberiam o incentivo, pois foi considerado que possuem uma probabilidade muito grande a entrarem em churn e seria muito  difícil convence-los a renovar o contrato mesmo com um incentivo finaceiro.
- Clientes com uma probabilidade maior do que 90% e menor do que 95% receberiam um incentivo de 250.
- Clientes com uma probabilidade entre 90% e 70% receberiam um incentivo de 200.
- Clientes com uma probabilidade menor do que 70% receberiam um incentivo de 100.

Supondo que fosse possível evitar que todos os clientes que receberam o incentivo entrassem em churn, e então consequentemente renovassem seus contratos, seria possível obter um retorno finaceiro de **$ 938.235,39**, a partir de um investimento de $9.800 que foi o budget máximo definido. 

## Conclusão 
