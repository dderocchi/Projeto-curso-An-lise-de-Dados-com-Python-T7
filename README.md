# Projeto-curso-An-lise-de-Dados-com-Python-T7
Primeira tentativa de análise
README_DeniseDeRocchi_AnáliseDeDadoscomPython_V7

Para dar inicio ao projeto, foi selecionada a base de dados sugerida, no endereço https://www.kaggle.com/datasets/namespaiva/base-varejo/data . O arquivo csv foi renomeado como varejo.csv . 

A primeira etapa foi verificar o número de registros (com o comando (len): 830 mil) e as colunas do arquivo csv. 

Total de registros: 830 mil
Colunas: 13 colunas

A seguir, foi usados o comando dtype para verificar o tipo de dados na base de dados, comparando com a informação disponível sobre a forma como a base de dados foi organizada: 

DATA - data da compra - object
CO_ID - código da compra (nota fiscal - int64 (número inteiro)
CL_ID - código do cliente - int64 (número inteiro)
CL_GENERO - gênero do cliente - object
CL_EC - estado civil, indicado por um código numérico - int64 (número inteiro)
1: Casado ou união estável; 2: Divorciado; 3: Separado; 4. Solteiro; 5: Viúvo 
CL_FHL - número de filhos do cliente - int64
CL_SEG - classe econômica do cliente (A,B ou C) - object
PR_ID - código do produto adquirido - int64
PR_CAT - categoria do produto adquirido - object
PR_NOME -nome do produto adquirido - object

Como as colunas de 10 a 13 constam como “unnamed” e na visualização dos primeiros registros delas contém NaN (not a number), considerei um indicativo da necessidade de limpeza destas colunas. 

Para verificar se de fato as colunas e outros registros precisavam ser limpas, foi utilizado o comando print(df_varejo.info)
As linhas repetidas foram excluídas com o comando drop_duplicates()
A tentativa de ajustar a data, com o comando datetime não foi possível, pois ele não aceitou os registros no modelo dia/mês/ano. Não encontrei uma forma de fazer o ajuste.
Utilizei o comando drop para excluir as últimas 4 colunas, que nao continham dados. 

Um novo arquivo, sem os registros duplicados, foi exportado como “varejook” para dar sequência à análise
