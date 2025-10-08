# **Projeto Ifood - Análise exploratória de dados** :bulb:

## Índice
- [1. Contexto](https://github.com/giulia-tuffanelli/projeto_ifood/edit/main/README.md#1-contexto)
- [2. Ferramentas](https://github.com/giulia-tuffanelli/projeto_ifood/edit/main/README.md#2-ferramentas)
- [3. Técnicas](https://github.com/giulia-tuffanelli/projeto_ifood/edit/main/README.md#3-t%C3%A9cnicas)
- [4. Produtos da análise](https://github.com/giulia-tuffanelli/projeto_ifood/edit/main/README.md#4-produtos-da-an%C3%A1lise)
- [5. Principais insights](https://github.com/giulia-tuffanelli/projeto_ifood/edit/main/README.md#5-principais-insights-)
- [6. Conclusão](https://github.com/giulia-tuffanelli/projeto_ifood/edit/main/README.md#6-conclus%C3%A3o)

## 1. Contexto

A empresa GT Data Analysis recebeu uma demanda do cliente fictício "Ifood" para realizar uma análise exploratória de um determinado conjunto de dados, com objetivo de identificar o perfil de clientes cadastrados nessa base e fazer correlações entre os dados que complementem o entendimento desse perfil. Esses resultados irão guiar algumas decisões sobre campanhas de marketing no aplicativo, para aumentar o número de pedidos na plataforma e entender melhor os clientes.

A base de dados está em formato excel, obtidos através da plataforma EBA Renata Biaggi.

O conjunto de dados é composto por clientes da empresa "Ifood" com dados sobre:

- Perfis de clientes
- Preferências do produto
- Sucessos/fracassos da campanha
- Desempenho do canal de vendas (app)


## 2. Ferramentas

Bibliotecas Python para Análise Exploratória de Dados (EDA)
- Pandas
- Seaborn
- Matplotlib


## 3. Técnicas

O projeto foi desenvolvido por meio de EDA, considerando-se as seguintes etapas:

3.1 Análise exploratória dos dados (EDA)

Etapa de exploração univariada inicial de dados para entender os tipos de variável, investigar valores únicos, verificar valores ausentes ou nulos, verificar a qualidade dos dados (por exemplo: escrita inconsistente, zeros onde não deveriam existir, unidades inconsistentes) e analisar a distribuição das variáveis categóricas e numéricas. Essa etapa é fundamental para a organização dos dados e qualidade das análises subsequentes.

3.2 Correlação entre os dados

Nesta etapa fiz uma análise multivariada para entender o perfil dos clientes e verificar algumas perguntas levantadas pelo time de negócios através dessa correlação. 

  - Estado civil x número de filhos
  - Gastos na plataforma x número de filhos
  - Renda anual familiar x gastos na plataforma

## 4. Produtos da análise

[Notebook detalhado das análises em python.]()

## 5. Principais insights 📈

<ins>Importância da verificação de dados nulos:</ins> A presença de campos em branco em uma base de dados pode distorcer medidas estatísticas e levar a resultados enviesados. Na análise dessa base entendi que os campos estavam nulos porque significam que a pessoa não tem aquela determinada característica, já que essas colunas só tem nulos ou um outro determinado valor. Para melhorar a análise posterior, criei colunas booleanas no dataframe para que todos os atributos de cliente tenham o valor 0 em caso de nulo e 1 caso não.

<ins>Gastos na plataforma (expenses):</ins> O desvio padrão está bastante elevado e quase igual ao valor médio . A mediana (50%) é de R$ 343,00 , bem menor que a média R$562,00 e 75% dos clientes gastam até R$964,00. Isso sugere que a maioria das famílias gasta pouco com compras no aplicativo, mas existe um grupo reduzido com gastos muito altos e isso distorce o gasto médio.

<ins>Renda anual familiar (Income):</ins> A média é de R$ 51.622,00 e está próxima da mediana R$ 51.287,00, o que sugere uma distribuição de renda relativamente simétrica entre os clientes.  

<img width="297" height="194" alt="image" src="https://github.com/user-attachments/assets/4b3c9a32-ff67-4367-901f-38d6494df240" />

<ins>Grau de escolaridade (education_level):</ins> A maioria dos clientes possui educação de nível superior. Poucos clientes concluíram somente o nível básico. 

<img width="280" height="233" alt="image" src="https://github.com/user-attachments/assets/9c487c14-f4c8-41bd-b575-b2e0494bcec5" />

<ins>Estado civil (marital_status):</ins> A maior parte dos clientes são casados ou moram juntos. Poucos clientes são divorciados ou viúvos.

<img width="280" height="233" alt="image" src="https://github.com/user-attachments/assets/4d628724-cdd3-4d58-9c6d-5e44e60169c1" />

<ins>Estado civil (marital_status) x Número de filhos:</ins> Todos os gupos tem perfil parecido, com maioria entre 0 e 1 filho. O grupo Divorced(divorciado) tem a distribuição mais concentrada, com quase todos com 1 filho. 3 filhos já é considerado um valor *outlier*.	

<img width="280" height="233" alt="image" src="https://github.com/user-attachments/assets/fb2f10f3-34d1-4333-a8b5-ba2e58bce6ab" />

<ins>Gastos na plataforma (expenses) x Número de filhos:</ins> Obtivemos um resultado esperado nesse caso, em que as famílias sem filhos são as que mais gastam com compras no aplicativo. Conforme aumenta o número de filhos, as despesas medianas diminuem bastante (de aprox. R$ 1.100,00 sem filhos para aprox. R$ 100,00 com 2 ou 3 filhos). Apesar disso, nas famílias com 1 a 3 filhos temos *outliers*, ou seja, poucas famílias com filhos que gastam muito acima da média de seu grupo.

<img width="280" height="233" alt="image" src="https://github.com/user-attachments/assets/6589072a-8a7b-417f-ab30-bd5a68279508" />

<ins>Renda anual (income) x Gastos na plataforma (expenses):</ins> Aparentemente existe uma correlação diretamente proporcional, em que pessoas que tem maior renda também são as que gastam mais.

<img width="280" height="233" alt="image" src="https://github.com/user-attachments/assets/97291e60-000e-4e30-a3fd-ad381dc053cb" />

<ins>Renda anual x Número de filhos:</ins>	As famílias sem filhos possuem maior renda, mas com uma grande dispersão entre elas. Também há uma tendência decrescente entre renda e filhos, à medida que o número de filhos aumenta, a renda mediana diminui. Famílias com filhos mostram menor renda média e menor variação entre elas.

<img width="280" height="233" alt="image" src="https://github.com/user-attachments/assets/632ceafd-1242-4d43-ad98-5578818ea0dd" />

## 6. Conclusão 

A análise indica que o público da plataforma é formado principalmente por clientes que possuem uma renda anual compatível com a renda média geral, com ensino superior e até um filho. 

As famílias sem filhos tem maior renda e gastam mais dinheiro na plataforma, tendo um potencial de consumo mais alto. Já as famílias com filhos tem renda e gastos menores, indicando perfil mais sensível ao preço. Existe ainda uma pequena parte dos clientes que tem um gasto muito alto, o que eleva a média geral de gastos na plataforma, por isso acredito que esse seja um público estratégico para ações de fidelização e oferta de produtos *premium*. 

A maioria dos clientes gasta pouco, em geral, o que pode indicar a necessidade de campanhas promocionais personalizadas para aumentar o ticket médio.

Portanto, a segmentação dos clientes em faixas de renda, como alta, média e baixa renda, por exemplo, aliado à uma correlação com a quantidade de filhos pode otimizar os resultados das campanhas de marketing, aumentar a fidelização e as vendas na plataforma.

<img width="103" height="103" alt="image" src="https://github.com/user-attachments/assets/3e15a85f-f9bd-4919-ba21-75bc0263f32e" />
