# **Projeto Ifood - Análise exploratória de dados** :bulb:

## Índice
- [1. Contexto](https://github.com/giulia-tuffanelli/projeto_ifood/edit/main/README.md#1-contexto)
- [2. Ferramentas]()
- [3. Técnicas]()
- [4. Produtos da análise]()
- [5. Insights obtidos]()
- [6. Conclusão]()

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

Nesta etapa fiz uma análise multivariada para entender o perfil dos clientes e verificar algumas perguntas levantadas pelo time de negócios através da correlação entre os dados. 

  - Estado civil x número de filhos
  - Gastos na plataforma x número de filhos
  - Renda anual familiar x gastos na plataforma

## 4. Produtos da análise

[Notebook detalhado das análises em python.]()

## 5. Insights obtidos

<ins>Importância da verificação de dados nulos:</ins> A presença de campos em branco em uma base de dados pode distorcer medidas estatísticas e levar a resultados enviesados. Na análise dessa base entendi que os campos estavam nulos porque significam que a pessoa não tem aquela determinada característica, já que essas colunas só tem nulos ou um outro determinado valor. Para melhorar a análise posterior, criei colunas booleanas no dataframe para que todos os atributos de cliente tenham o valor 0 em caso de nulo e 1 caso não.
	
<ins>Renda anual familiar (Income):</ins> A distribuição de renda entre os clientes é muito assimétrica, tem alta dispersão e tem uma média pouco representativa, com forte impacto de outliers de alta renda. Por isso, uma sugestão para análises futuras seria segmentar os clientes em faixas de renda, como baixo, médio e alto, por exemplo. Isso permitiria uma análise mais individualizada do perfil consumidor de cada segmento e pode otimizar direcionamento de campanhas e promoções.


		
		
	
	
		○ Sobre o estado civil e número de filhos, nota-se que a maioria dos clientes são casados e tem até 2 filhos. Porém, os gastos na plataforma são consideravelmente maiores entre os casais sem filhos, o que também é útil para direcionar melhor as ofertas e otimizar gastos com campanhas. 
		
		
		

