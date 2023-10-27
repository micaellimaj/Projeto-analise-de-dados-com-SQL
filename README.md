# Projeto análise de banco de dados com linguagem 'SQL'

Os dados foram obtidos em uma pesquisa realizada com alunos dos cursos de matemática e língua portuguesa do ensino médio. Ele contém muitas informações sociais, de gênero e de estudo interessantes sobre os alunos. E nesse projeto iremos focar na análise de dados utilizando linguagem SQL para fazer consultas no bucket criado na plataforma da AWS, e com essas consultas gerar insights significativos e filtrar os dados com base nos nossos objetivos. Teremos como foco inicial o dataset dos estudantes de matemática que iremos utilizar para fazer as análises e logo em seguida utilizaremos o dataset dos estudantes de lingua portuguesa para trabalhar com múltiplas tabelas. Nesse projeto utlizamos conceitos fundamentais de consuta, como seleção e junção de dados e sua devida estruturação de consulta, além de agrupamento e métodos estatísticos para gerar insights.

Os datasets utilizados para esse projeto podem ser encontrados nos seguintes links:
* Alunos de matemática: https://www.kaggle.com/datasets/uciml/student-alcohol-consumption/data?select=student-mat.csv
* Alunos de português: https://www.kaggle.com/datasets/uciml/student-alcohol-consumption/data?select=student-por.csv

## Painel:

Para auxiliar a análise dos dados eu decidir criar um relatório no Power BI com os dados dos alunos de matemática que nós traz visuais gráficos, tabelas e segmentadores de dados relevantes, tornando a análise mais completa para a geração de insights. Segue o link abaixo para o relatório:
* https://bit.ly/micael-lima-analista-de-dados-relatorio-avaliacao-estudantil

## Tecnologias utilizadas:

* <img src="https://img.shields.io/badge/Python-000000?style=for-the-badge&logo=python&logoColor=yellow1" alt="icon python" > 
* <img src="https://img.shields.io/badge/Power_BI-000000?style=for-the-badge&logo=powerbi&logoColor=yellow" alt="icon power bi">
* <img src="https://img.shields.io/badge/Colab-F9AB00?style=for-the-badge&logo=googlecolab&color=525252" alt="icon colab">

## Colunas dos dados

Vale resaltar que ambos os datasets possuem as mesmas colunas.


*   **School**: escola do aluno (binário: 'GP' - Gabriel Pereira ou 'MS' - Mousinho da Silveira).
*   **sex**: sexo do aluno (binário: 'F' - feminino ou 'M' - masculino).
*   **age**: idade do aluno (numérico: de 15 a 22).
*   **address**: tipo de endereço residencial do aluno (binário: 'U' - urbano ou 'R' - rural).
*   **famsize**: tamanho da família (binário: 'LE3' - menor ou igual a 3 ou 'GT3' - maior que 3).
*   **Pstatus**: situação de coabitação dos pais (binário: 'T' - morando juntos ou 'A' - separados).
*   **Medu**: escolaridade da mãe (numérico: 0 - nenhuma, 1 - ensino fundamental (4º ano), 2 - 5º ao 9º ano, 3 - ensino médio ou 4 - ensino superior).
*   **Fedu**: escolaridade do pai (numérico: 0 - nenhuma, 1 - ensino fundamental (4º ano), 2 - 5º ao 9º ano, 3 - ensino médio ou 4 - ensino superior).
*   **Mjob**: trabalho da mãe (nominal: 'professor', 'cuidados de saúde', 'serviços' civis (por exemplo, administrativo ou policial), 'em_casa' ou 'outros').
*   **Fjob**: trabalho do pai (nominal: 'professor', 'cuidados de saúde', 'serviços' civis (por exemplo, administrativo ou policial), 'em_casa' ou 'outros').
*   **reason**: razão para escolher esta escola (nominal: perto de ‘casa’, ‘reputação’ da escola, preferência de ‘curso’ ou ‘outro’).
*   **guardian**: tutor do aluno (nominal: 'mãe', 'pai' ou 'outro').
*   **traveltime**:  tempo de viagem da casa para a escola (numérico: 1 - <15 min., 2 - 15 a 30 min., 3 - 30 min. a 1 hora, ou 4 - >1 hora).
*   **studytime**: tempo de estudo semanal (numérico: 1 - <2 horas, 2 - 2 a 5 horas, 3 - 5 a 10 horas ou 4 - >10 horas).
*   **failures**:  número de falhas de classe anteriores (numérico: n se 1<=n<3, caso contrário 4).
*   **schoolsup**: apoio educacional extra (binário: sim ou não).
*   **famsup**: apoio educacional familiar (binário: sim ou não).
*   **paid**: aulas extras remuneradas dentro da disciplina do curso (Matemática ou Português) (binário: sim ou não).
*   **activities**: atividades extracurriculares (binário: sim ou não)
*   **nursery**: frequentou a creche (binário: sim ou não).
*   **higher**: quer fazer ensino superior (binário: sim ou não).
*   **internet**: acesso à Internet em casa (binário: sim ou não).
*   **romantic**: com relacionamento amoroso (binário: sim ou não).
*   **famrel**: qualidade das relações familiares (numérico: de 1 - péssimo a 5 - excelente).
*   **freetime**: tempo livre depois da escola (numérico: de 1 - muito baixo a 5 - muito alto).
*   **goout**: sair com amigos (numérico: de 1 - muito baixo a 5 - muito alto).
*   **Dalc**:  consumo diário de álcool (numérico: de 1 - muito baixo a 5 - muito alto).
*   **Walc**: consumo de álcool no final de semana (numérico: de 1 - muito baixo a 5 - muito alto)
*   **health**: estado de saúde atual (numérico: de 1 – muito ruim a 5 – muito bom)
*   **absences**: número de faltas escolares (numérico: de 0 a 93).
*   **G1**: nota do primeiro período (numérico: de 0 a 20).
*   **G2**: nota do segundo período (numérico: de 0 a 20).
*   **G3**: nota final (numérico: de 0 a 20, meta de saída).


## Desenvolvimento

Foram aplicadas diversas técnicas para a construção desse projeto como:

* Verificação da estrutura e do tipo do dados correto com python para saber como criariamos a tabela no AWS.
* Utilização de buckets para armazenamento de dados.
* Uso do Athena para fazer consultas 'SQL'.
* Trabalho com criação de tabelas.
* Seleção e filtragem dos dados.
* Uso de agregações nos dados e métodos estatísticos.
* Utilização de consultas com múltiplas tabelas e junção dos dados.
* Uso de subqueries e agregações por particionamento.

## Bibliotecas Python:

```
import pandas as pd
```
