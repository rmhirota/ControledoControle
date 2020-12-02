
<!-- README.md is generated from README.Rmd. Please edit that file -->

# Introdução

No presente projeto vamos apresentar o trabalho final do curso de “Web
scraping” da [Curso-R](www.curso-r.com). A ideia foi desenvolver
ferramentas para raspar dados do Supremo Tribunal Federal (STF) e fazer
algumas análises exploratórias em cima destes.

Espera-se, num futuro, desenvolver pacotes para análises mais profundas,
inclusive em outros Tribunais. Os feedbacks são muito bem vindos\!

### Delimitação do tema

Vamos aqui nos ater ao [**Supremo Tribunal Federal**](www.stf.jus.br), a
Corte cuja atuação (e omissão…) causa o maior impacto social, político e
econômico em nossa sociedade.

Mais especificamente, vamos analisar as causas que envolvem diretamente
o controle concentrado de constitucionalidade. Isso é, vamos examinar as
classes processuais relativas a:

  - [Ação Direta de Inconstitucionalidade
    (ADI)](https://pt.wikipedia.org/wiki/A%C3%A7%C3%A3o_direta_de_inconstitucionalidade),

  - [Ação Declaratória de Constitucionalidade
    (ADC)](https://pt.wikipedia.org/wiki/A%C3%A7%C3%A3o_declarat%C3%B3ria_de_constitucionalidade),

  - [Ação Declaratória de Inconstitucionalidade por Omissão
    (ADO)](https://pt.wikipedia.org/wiki/A%C3%A7%C3%A3o_direta_de_inconstitucionalidade_por_omiss%C3%A3o)
    e

  - [Arguição de Descumprimento de Preceito Fundamental
    (ADPF)](https://pt.wikipedia.org/wiki/Argui%C3%A7%C3%A3o_de_descumprimento_de_preceito_fundamental).

Não é apenas por essas classes processuais que a Suprema Corte decide,
mas elas representam a atividade mais tradicional e típica de um
Tribunal Constitucional em sua concepção clássica. Faz sentido, então,
prestigiar e analisar a atuação do STF sob esse aspecto.

Ainda, é possível verificar nessas ações como se dá conflitos relevantes
não apenas entre sociedade civil e poder público mas também entre os
Poderes Legislativo e Executivo bem como evidencia a (falta de) atuação
da Procuradoria-Geral da República.

Durante a pandemia, também, essas ações têm sido especialmente
importantes para definição de esferas de responsabilidade (vide ADPF
722), a discussão sobre o plano de vacinação, etc, etc.

A ideia é mapear aspectos como quantidade de ações por tipo/ano, quais
os principais litigantes dessas ações (considerando-se os poucos
legitimados para tanto), quais os principais temas dessas ações, as
palavras-chave mais utilizadas nas petições iniciais, etc.

Com os dados ora obtidos espera-se poder realizar todas essas análises
(e várias outras), ainda que a limitação de tempo até a entrega final
provavelmente não permita esgotá-las.

### Utilidade e pertinência de *web scraping*

Justifica-se a utilidade tendo-se em vista a importância (crescente?) do
STF no cotidiano, não só das pessoas em carreiras jurídicas mas também
da academia e das cidadãs e cidadãos comuns.

Trata-se de serviço público (cujo acesso à justiça é, inclusive,
previsto na Constituição Federal) que, a despeito de sua importância,
ainda é um ilustre desconhecido.

De outro lado, não existe ainda disponibilizados dados abertos desse
Tribunal e tampouco existe API que viabilize extração ordenada de dados.
Portanto, até o momento, raspar os dados utilizando as técnicas
aprendidas no curso é uma opção necessária e viável no presente caso.

Por fim, reitere-se que os processos judiciais são públicos por força do
[artigo 93, IX da Constituição
Federal](http://www.planalto.gov.br/ccivil_03/constituicao/constituicao.htm#art93ix.),
que determina que “*todos os julgamentos do Poder Judiciário serão
públicos*”.

## Descrição da Página

O portal do STF pode ser acessado pelo seguinte endereço:
<http://portal.stf.jus.br/> que dá acesso direto à home. Lá, no topo da
página, é possível realizar a consulta por processos:

![](img/home-stf.png)

A ferramenta de consulta é um formulário que permite que se preencha a
classe processual escolhida e o número. Na sequência, de forma
invisível, o site irá identificar o número de “incidente” e nos
redirecionar para a ferramente de busca interna (uma espécie de “API
escondida”) que nos dará dados como os andamentos e as partes:

![](img/andamentos.png)

![](img/partes.png)

Outra das abas possiveis de ser analisada é a de “Peças processuais” que
dá efetivo acesso a uma espécie de “pasta virtual” dos procesos,
permitindo visualizar documentos, petições e decisões judiciais.

![](img/pagina_peças.png)

É através dessas páginas, portanto, que pretendemos navegar e extrair
dados para as análises futuras.

### fluxo

achar a lista de processos separar o que quero buscar incidentes

numero interno que identifica o processo

ir em cada página através do incidente buscar as abas de dados,
detalhes, etc

abrir página com visualizador de documentos identificar qual é o
primeiro

baixar o pdf da inicial

### documentar a tabela

## algumas análises feitas

## próximos passos

### sugestões de análises

### sugestões de pacote a ser feito

painel de análise das ações de controle concentrado assuntos mais
frequentes autores rodar no git hub actions
