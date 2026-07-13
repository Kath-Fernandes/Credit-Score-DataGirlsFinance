## Data Girls Finance - Análise de Risco e Concessão de Crédito

Projeto de análise exploratória de dados e previsão de score de crédito para o case Data Girls Finance - Projeto Final do Bootcamp Análise de Dados


# Descrição do Projeto
Este projeto foi desenvolvido simulando a atuação em uma equipe de dados da fintech fictícia Data Girls Finance. O objetivo principal é entender o perfil financeiro e comportamental dos clientes para apoiar a área de crédito na tomada de decisões estratégicas e na mitigação de riscos de inadimplência.
O projeto utiliza o dataset "Credit Score Classification" para explorar padrões e construir um dashboard interativo no Power BI, culminando em recomendações acionáveis para o negócio.

# Link para o Dataset Original: [Kaggle - Credit Score Classification](https://www.kaggle.com/datasets/parisrohan/credit-score-classification)



# Objetivos
- Identificar padrões comportamentais e demográficos associados às classificações de score de crédito (Alto Risco, Risco Moderado, Baixo Risco).
- Criar indicadores (KPIs) que auxiliem na análise rápida da saúde da carteira de clientes.
- Fornecer recomendações estratégicas embasadas em dados para melhorar a concessão de crédito e reduzir a inadimplência.


# Metodologia e Pipeline de Dados
O projeto seguiu um pipeline clássico de análise de dados, focado em qualidade e usabilidade visual:
1. Extração e Entendimento dos Dados:
   - Importação da base de dados contendo variáveis cadastrais (idade, profissão), financeiras (renda, contas, empréstimos) e comportamentais (atrasos, pagamentos).

2. Limpeza e Transformação (ETL via Power Query):
   - Tratamento de valores nulos e inconsistentes (ex: padronização de registros como "Não Informado" ).
   - Criação de colunas calculadas condicionais para agrupamento analítico (ex: criação das faixas etárias e faixas de renda).

3. Modelagem e Cálculos (DAX):
   - Desenvolvimento de medidas explícitas em DAX para garantir cálculos dinâmicos e precisos (Média de Dias de Atraso, Renda Média Anual, Percentuais de Risco por Categoria, etc.).

4. Visualização de Dados (Power BI):
   - Construção de um dashboard com 5 páginas utilizando princípios de UI/UX, com paleta de cores consistente (escala de roxos para o tema da marca e semáforo vermelho/amarelo/verde para os níveis de risco).

# Guia de Uso do Dashboard
O dashboard foi projetado para uma navegação fluida. Utilize o menu inferior para transitar entre as visões:
Página 1 - Capa:Apresentação corporativa do relatório.
Página 2 - Indicadores do Perfil Financeiro: Analise a média de renda e valor investido distribuídos por faixa etária. *Dica: Utilize os filtros superiores para segmentar as informações por nível de Score.*
Página 3 - Análise de Score de Crédito: Verifica como a carteira está distribuída entre Alto/Moderado/Baixo Risco e cruza essa classificação com o volume de pagamentos atrasados e profissões.
Página 4 - Análise de Risco e Comportamento: Visão avançada de correlação. O gráfico de dispersão (Scatter Plot) cruza Renda vs Atraso. Avalie também o forte impacto do comportamento de "Pagamento Mínimo" no score final.
Página 5 - Insights e Recomendações: Resumo executivo. Apresenta os principais KPIs da carteira e traduz as descobertas dos dados em planos de ação claros para a diretoria.


 Principais Insights Descobertos
A análise exploratória revelou padrões críticos para a operação de crédito:
O Peso do Atraso: Clientes de Alto Risco possuem uma média crítica de 30 dias de atraso e 156 pagamentos atrasados no histórico, sendo este o maior indicativo de inadimplência.
O Perigo do 'Pagamento Mínimo':Entre os clientes que pagam apenas o mínimo da fatura, a chance de possuírem um Baixo Risco cai para apenas 7%, enquanto o Alto Risco dispara para 36%.
Idade como Fator de Segurança: O público mais jovem (18-24 anos) concentra a maior fatia de Alto Risco (45,82%), enquanto clientes com 55+ anos são o porto seguro da carteira (quase 50% em Baixo Risco).
Renda Média: O perfil de Baixo Risco sustenta uma renda anual (R$ 6 Mi) cerca de 50% maior que o perfil de Alto Risco (R$ 4 Mi).

# Recomendações Estratégicas propostas
1. Educação Financeira: Direcionar campanhas maciças para a base de Risco Moderado (maioria da carteira), visando migrá-los para o Baixo Risco.
2. Políticas Conservadoras para Jovens: Desenvolver limites iniciais mais baixos para a faixa de 18 a 34 anos para mitigar a inadimplência de entrada.
3. Gatilhos de Alerta: Criar automações sistêmicas que alertem a área de risco quando um cliente começar a pagar o valor mínimo da fatura consecutivamente.
4. Foco em 55+: Direcionar ofertas de produtos premium para a base de clientes com mais de 55 anos, aproveitando a alta estabilidade desse grupo.
