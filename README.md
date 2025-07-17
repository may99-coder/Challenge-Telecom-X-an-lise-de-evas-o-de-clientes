# 📄 Challenge Telecom X: Análise de Evasão de Clientes (Churn)

---

## 🧭 1. Introdução

Este projeto tem como objetivo analisar a **evasão de clientes (churn)** de uma empresa de telecomunicações. A evasão ocorre quando um cliente cancela seu contrato com a empresa, e compreender os motivos desse comportamento é crucial para desenvolver estratégias de retenção eficazes.

Com base em um conjunto de dados fornecido, exploramos características dos clientes e serviços contratados para identificar padrões que se associam a maiores taxas de cancelamento.

---

## 🧹 Limpeza e Tratamento de Dados

Para garantir a qualidade dos dados e a precisão das análises, os seguintes passos foram realizados:

* **Importação e normalização dos dados JSON:** Os dados foram extraídos de um arquivo JSON e convertidos em um DataFrame do Pandas, facilitando a manipulação e a análise estruturada.
* **Identificação e remoção de dados ausentes e inconsistentes:** Linhas com informações faltantes ou inválidas foram removidas para garantir que a análise fosse precisa e não enviesada.
* **Conversão de formatos e variáveis categóricas:** Valores textuais como "Sim" e "Não" foram convertidos para formato binário (1 e 0), e outras colunas foram ajustadas para seus tipos apropriados.
* **Criação da coluna "Contas Diárias":** Foi criada uma nova variável para representar o gasto diário dos clientes, dividindo o valor total (`Charges.Total`) pela quantidade de meses de contrato (`tenure`), a fim de identificar padrões de comportamento financeiro.
* **Tradução e padronização dos dados:** As colunas e seus valores foram traduzidos para o português para tornar os resultados mais acessíveis. Também foi feita a padronização de rótulos em variáveis categóricas, como a conversão de "Male" para "Masculino" e "Female" para "Feminino".

---

## 🔍 Análise Exploratória de Dados (EDA)

Com os dados devidamente tratados, foi realizada uma análise exploratória com o objetivo de identificar padrões de comportamento e fatores associados à evasão (Churn). As principais análises e visualizações realizadas foram:

* **Distribuição da Evasão (Churn):** A análise inicial examinou a proporção de clientes que cancelaram o serviço em relação aos que permaneceram. Essa visão geral permitiu dimensionar o problema e serviu de base para aprofundamentos posteriores.
* **Análises por Perfil Demográfico:** Foram gerados gráficos para avaliar a evasão com base em características dos clientes, como:
    * Gênero
    * Faixa etária (idosos ou não)
    * Presença de dependentes
    Essas comparações ajudaram a entender se determinados grupos apresentam maior propensão ao cancelamento.
* **Análises por Perfil Contratual e de Serviço:** Exploramos também o churn em relação a:
    * Tipo de contrato
    * Método de pagamento
    * Tipo de serviço de internet
    * Gasto mensal e tempo de permanência (`tenure`)

### Tipos de Gráficos Utilizados:

* **Gráficos de barras verticais:** Para comparar contagens absolutas entre grupos.
* **Gráficos de setores (pizza):** Para ilustrar proporções de churn.
* **Boxplots:** Para visualizar a distribuição de variáveis numéricas por grupo (ex: gasto mensal por churn).
* **Histograma e violino (opcional):** Para verificar concentração e dispersão de valores.

Essas visualizações possibilitaram a identificação de tendências importantes e diferenças marcantes entre os perfis de clientes que permanecem e os que cancelam os serviços.

---

## ✅ Conclusões e Insights

Com base nas análises realizadas, podemos destacar os seguintes pontos:

* A maioria dos clientes permanece, mas uma parte relevante ainda cancela o serviço.
* Clientes com **contratos mensais** apresentam taxas significativamente maiores de evasão.
* A forma de pagamento influencia no churn: quem paga via **cartão eletrônico** tende a sair mais.
* Clientes que ficam **menos tempo na empresa (tenure baixo)** cancelam com mais frequência.
* Clientes com **gastos mensais mais altos** também demonstram maior propensão ao cancelamento.

---

## 💡 Recomendações

Com base nos padrões identificados, recomendamos:

* **Incentivar contratos de longo prazo**, oferecendo benefícios e descontos.
* **Acompanhar de perto os novos clientes (primeiros meses)**, oferecendo suporte proativo.
* **Analisar criticamente planos com valores mensais mais altos**, verificando se há insatisfação com custo-benefício.
* **Focar em retenção personalizada** para clientes com perfil de risco (contrato mensal + pagamento eletrônico + tenure baixo).
* **Aplicar modelos preditivos** com base nos dados para prever e agir preventivamente em potenciais casos de churn.
