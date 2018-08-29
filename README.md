# DocumentEmbeddingsOG

Nanodegree Engenheiro de Machine Learning - Projeto Final
Aluno: Fábio Corrêa Cordeiro

## Resumo
O presente projeto final consiste na utilização de algoritmos de aprendizado não
supervisionados conhecidos como Doc2Vec para representar documentos de um
corpus através de vetores (Le et al., 2014). Esses vetores serão utilizados para
treinar algoritmos de aprendizado supervisionado e gerar modelos de classificação
nos subdomínios de Óleo e Gás. Desta forma será possível identificar quais
documentos estão semanticamente relacionados, além de classificá-los nos
subdomínios.

Esse projeto é uma evolução do trabalho “Word Embeddings em português para o
domínio específico de Óleo e Gás” (Gomes, 2018), disponível em
https://github.com/diogosmg/wordEmbeddingsOG. Esse projeto consistiu em testar
algoritmos de vetorização de palavras (Mikolov et al., 2013) de forma que fosse
possível identificar similaridades semânticas entre palavras de um mesmo domínio
de conhecimento.

## Descrição do problema
Neste projeto são resolvidos dois problemas. O primeiro é, dado um determinado
documento, identificar quais outros documentos de um determinado corpus são
similares. O segundo problema é classificar esse documento em um dos
subdomínios de Óleo & Gás.

O corpus utilizado é composto por 290 projetos finais (monografias de graduação,
dissertações de mestrado e teses de doutorado) do Programa de Recursos
Humanos da Agência Nacional do Petróleo, Gás Natural e Biocombustível (PRHANP).
Esses documentos estavam originalmente em formato PDF que, em alguns
casos, haviam sido digitalizados. Foram utilizadas técnicas de reconhecimento de
caracteres (OCR - optical character recognition) para extrair os textos para o
formato TXT. Todos esses documentos contém, após serem preprocessados, um
total 3.308.466 palavras e um vocabulário de 52.880 palavras únicas.

Como o conjunto de documentos não é exageradamente grande, a extração dos
subdomínios foi feita manualmente. Em geral a indústria de Óleo & Gás é dividida
em “Upstream” (atividades que vão desde estudos geológicos, descoberta do
petróleo até a sua produção) e “Downstream” (atividades que vão do refino do
petróleo, produção dos derivados, distribuição e comercialização). Também foi
incluído o subdomínio “Interdisciplinar” que contempla os documentos
relacionados às disciplinas que afetam à toda a cadeia de Óleo e Gás (meio
ambiente e desenvolvimento de novos materiais, por exemplo).

## Métricas
A avaliação de similaridade entre os documentos foi feita através da comparação
empírica principalmente utilizando a visualização dos resultados. Para reforçar as
comparações criamos alguns documentos sintéticos a partir de documentos
originais pertencentes ao corpus. A expectativa foi encontrar o documentos
sintéticos e os originais próximos.

Já para a avaliação da classificação dos documentos foram calculadas as métricas
de acurácia, precisão, revocação e F1-Score. Como não há nenhuma preferência
entre minimizar os falsos positivos ou falsos negativos usamos o F1-Score como
métrica principal para as tomadas de decisão.

## Os seguintes arquivos compõe este projeto:

Relatório Final.pdf - Relatório final do projeto
Projeto Final.ipynb - Scripts detalhado do projeto em usando Jupyter Notebook.
PRH - Pasta contendo 290 arquivos com os projetos final do Programa de Recursos Humanos da ANP em formato TXT.
corpus_unificado - Pasta onde serão gravados os arquivos unificados.
corpus_preprocessado - Pasta onde serão gravados e posteriormente lido os arquivos preprocessado

## Outros arquivos de apoio:

Extração do PRH.ipynb - Script para extrair o nome dos arquivos da pasta PRH e os primeiros 300 caracteres do texto
lista_PRH.csv - Planilha gerada pelo script Extração do PRH.ipynb
lista_PRH_editada.csv - Planilha anotada manualmente contendo o nome do arquivo da padta PRH com seu respectivo título e subdomínio de Óleo & Gás.
teste_recuperação_original_1.txt - Documento retirado da pasta PRH para gerar um arquivo sintético
teste_recuperação_original_2.txt - Documento retirado da pasta PRH para gerar um arquivo sintético
teste_recuperação_sintético_1.txt - Documento sintético gerado do arquivo teste_recuperação_original_1.txt
teste_recuperação_sintético_2.txt - Documento sintético gerado do arquivo teste_recuperação_original_2.txt
Projeto Final - Escolha dos parâmetros.ipynb - Script com a 1° rodada de escolha dos parâmetros
Projeto Final - Escolha dos parâmetros - v2.ipynb - Script com a 2° rodada de escolha dos parâmetros
A_Busca.pdf - Arquivo com introdução e prólogo do livro "A Busca" usado como teste 
A_Busca.txt - Arquivo com introdução e prólogo do livro "A Busca" usado como teste

## Bibliotecas utilizadas:

- numpy
- datetime
- pandas
- collections
- os
- pathlib
- random
- re
- nltk
- string
- unicodedata
- gensim
- sklearn
- bokeh
- wordcloud
- matplotlib
