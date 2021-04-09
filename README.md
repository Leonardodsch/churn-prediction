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

## Melhores Insights

## Machine Learning Models

## Resultados

## Conclusão 
