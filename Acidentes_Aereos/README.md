# Análise de Ocorrências Aeronáuticas da Aviação Civil Brasileira

## Objetivo
Este projeto tem como objetivo realizar uma análise exploratória de dados sobre ocorrências aeronáuticas (acidentes, incidentes graves e incidentes) da aviação civil brasileira. O estudo visa identificar padrões, tendências geográficas, tipos de ocorrências mais comuns e os fatores contribuintes, utilizando dados públicos fornecidos pelo CENIPA (Centro de Investigação e Prevenção de Acidentes Aeronáuticos).

## Bases de Dados
As bases de dados utilizadas são extraídas diretamente do portal de dados abertos do CENIPA, garantindo a utilização de dados reais. Os arquivos são interligados por chaves de relacionamento, permitindo análises combinadas.

ocorrencia.csv: Detalhes gerais de cada ocorrência (data, local, classificação, fatalidades, etc.).
ocorrencia_tipo.csv: Classificação e tipo de cada ocorrência.
aeronave.csv: Informações detalhadas sobre a aeronave envolvida (fabricante, tipo de motor, fase da operação, etc.).
fator_contribuinte.csv: Fatores contribuintes identificados na investigação de cada ocorrência.
Tarefas de Análise de Dados
A seguir, apresento uma lista de tarefas criadas por um modelo de linguagem de IA para guiar a prática de manipulação, agregação, filtragem e visualização de dados com a biblioteca Pandas em Python.

### Tarefa 1: Análise Temporal e Geográfica
1. Mês mais perigoso: Calcule e plote um gráfico de barras que mostre o total de ocorrências por mês do ano. Identifique o mês com o maior número de ocorrências.
2. Top 5 estados: Liste os 5 estados brasileiros com o maior número de ocorrências registradas.
3. Tendência anual: Plote um gráfico de linhas mostrando a evolução do número total de ocorrências ao longo dos anos.

### Tarefa 2: Análise da Ocorrência e Aeronave
1. Tipos de aeronave: Qual o tipo de veículo (aeronave_tipo_veiculo) mais envolvido em ocorrências classificadas como ACIDENTE? (Dica: Você precisará juntar as bases de dados de ocorrência e aeronave).
2. Fase da operação: Calcule a contagem de ocorrências por fase da operação (aeronave_fase_operacao) e identifique as três fases mais comuns.
3. Ocorrências fatais: Liste o número total de fatalidades por ano.

### Tarefa 3: Análise de Fatores Contribuintes
1. Fator principal: Qual o fator contribuinte mais frequente (fator_nome) que foi associado a ocorrências de ACIDENTE?
2. Fatores por tipo de aeronave: Crie um gráfico de barras com os 10 fatores contribuintes mais comuns para aeronaves de tipo HELICÓPTERO.
3. Fatalidades por fator: Analise os fatores contribuintes associados às ocorrências que tiveram fatalidades.

### Tarefa 4: Limpeza e Enriquecimento de Dados
1. Conversão de Datas: Converta a coluna de data das ocorrências para o formato datetime do Pandas para facilitar as análises temporais.
2. Preenchimento de Nulos: A coluna de fatalidades (ocorrencia_fatalidades) pode conter valores nulos. Preencha esses valores com 0 para garantir que a coluna seja numérica e possa ser usada em cálculos.
3. Criação de Coluna: Crie uma nova coluna chamada Regiao no DataFrame de ocorrências com base no estado (aeronave_uf). 4. Você pode agrupar os estados por região (Norte, Nordeste, Sudeste, Sul, Centro-Oeste).

Observações
A chave de relacionamento principal entre as bases é codigo_ocorrencia.
A coluna de data é ocorrencia_dia.
O encoding dos arquivos é 'latin-1'.