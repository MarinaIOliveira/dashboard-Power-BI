# dashboard-Power-BI

**Data Discovery, OLAP e Visualização de Dados**

Trabalho OLPA (Online Analytical Processing)

Alunos(as):

Anderson Carvalho                                                     	
Angela de Mendonça Pereira                                   	
Camila Coutinho Magalhães Marques                    	
Marina Iolanda Oliveira  

Escolhemos a base de dados do ProUni com as informações de 2014, 2015, 2016. A base ProUni (http://dadosabertos.mec.gov.br/prouni) foi escolhida devido a quantidade de informações relevantes. Para estados utilizamos a wikipedia (https://pt.wikipedia.org/wiki/Unidades_federativas_do_Brasil).

Dashboards gerados com a ferramenta de visualização Power BI. O Power BI foi escolhido como ferramenta devido a usabilidade, recursos disponíveis e conhecimento prévio.

As métricas utilizadas foram:
Quantidade de Faculdades, quantidade de cursos,
Quantidade de bolsas: por sexo, ano, deficiente, raça, região, turno, tipo de bolsa.   

O objetivo da analise é identificar padrões relacionados a distribuição das bolsas como as dimensões já citadas no slide anterior.

**Tratamento dos dados**

Base de dados (arquivo csv) separada por ano. Tivemos que unificar em uma única tabela.
Na base oficial não temos o campo “Estado” somente “UF”, com isso não conseguimos plotar o gráfico. Subimos uma nova tabela de uma fonte externa (wikipedia) com o “Estado” e “UF” fazendo a ligação (Join) entre as duas tabelas.
O gráfico Mapa de Forma não reconhece os estados acentuados, portanto tivemos que criar uma função (RemoveAcento) para retirar os acentos.

Criamos as seguintes medidas:
 -Quantidade de bolsas
 -Quantidade de faculdades
 -Quantidade de cursos
 -Quantidade de bolsas – sexo feminino
 -Quantidade de bolsas – sexo masculino
 -Bolsa parcial 50%
 -Bolsa integral
 -Turno Curso a distância
 -Turno Integral 
 -Turno Matutino
 -Turno Noturno
 -Turno Vespertino

**ANALISE RESULTADOS**

  -A raça parda é a predominante de bolsas do programa ProUni, onde a raça negra é predominante no Brasil. A raça, no preenchimento do questionário é escolhida pelo próprio candidato, não levando em consideração a informação oficial da certidão de nascimento.
  -Existe uma diferença de distribuição de bolsas entre mulheres e homens. Entre os anos de 2014 a 2016 esse número foi de 25% a mais de bolsas para o público feminino. 
  -2/3 das bolsas são integrais.
  -A região sudeste é predominante na distribuição de bolsas ficando com aproximadamente 50% do total.
  -Os deficientes beneficiados pela bolsa não chegam a 1% (5.628 de um total de 715.510 beneficiados)
  -O turno predominante é o noturno, ultrapassando 50% do total. Provavelmente esse índice indica que os beneficiados precisam trabalhar durante o horário comercial.
  -Os tres cursos predominantes de bolsa são: Administração, Direito e Pedagogia (nuvem de palavras).
