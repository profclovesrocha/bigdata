# Mercado de trabalho

## Por que essa disciplina tem peso na sua carreira

Praticamente toda empresa média ou grande hoje coleta mais dados do que consegue
usar. A escassez não é de dados nem de ferramentas — é de gente que saiba ligar uma
pergunta de negócio a um dado que a responda. É esse o trabalho, em qualquer um dos
cargos abaixo.

O detalhe que muita gente ignora: os papéis mais bem pagos da área **não** são os
mais matemáticos. São os que combinam capacidade técnica razoável com clareza para
comunicar o resultado. A parte da disciplina que parece "menos técnica" — o
Observatório de Dados, a apresentação do seminário — é justamente o que o mercado
paga.

## Os cargos, e o que cada um realmente faz

### Engenheiro de Dados

Constrói e mantém os canos por onde o dado passa: ingestão, pipelines, ETL,
armazenamento, orquestração. Se o dado chegou limpo e no horário na mesa do
analista, foi ele.

- **Stack:** SQL forte, Python, Spark, Kafka, Airflow, uma nuvem (AWS/GCP/Azure),
  modelagem de dados, Docker.
- **É a maior demanda do mercado brasileiro** e a porta de entrada mais realista
  para quem vem de desenvolvimento.
- **Na disciplina:** aula 02 (infraestrutura) e aula 03 (ETL, MapReduce).

### Analista de Dados

Responde perguntas de negócio com os dados que existem. Constrói dashboards, mede
indicadores, investiga por que um número caiu.

- **Stack:** SQL (o principal), Excel de verdade, Power BI ou Looker, estatística
  descritiva, e muita habilidade de comunicação.
- **É a porta de entrada mais acessível** — a barreira técnica é a menor e dá para
  chegar lá ainda na graduação.
- **Na disciplina:** aulas 04, 06–07 (interfaces, Observatório) e aula 08 (dados
  regionais de educação).

### Cientista de Dados

Usa estatística e machine learning para prever e classificar, não só descrever.
Menos vagas que os dois anteriores, e quase sempre exigindo experiência prévia.

- **Stack:** Python (pandas, scikit-learn), estatística inferencial, ML, SQL,
  capacidade de desenhar experimentos.
- **Na disciplina:** aula 05 (estudo de caso de mineração de dados) e o
  [e-book de ML](../05-recursos/ebook-machine-learning-codigos.pdf).

### Analytics Engineer

Cargo mais recente, no meio do caminho: pega o dado bruto que o engenheiro
entregou e o transforma em modelos confiáveis e documentados para o analista usar.

- **Stack:** SQL avançado, dbt, modelagem dimensional, Git, testes de dados.
- Bom caminho para quem gosta de SQL mas não quer administrar infraestrutura.

### Arquiteto de Dados

Decide a estrutura geral: que tecnologias, como os dados se relacionam, como
governar acesso e qualidade. É cargo sênior — objetivo de médio prazo, não primeiro
emprego.

## O caminho realista

```
Estágio / Analista Jr.  →  Analista Pleno  →  Engenheiro / Cientista  →  Sênior / Arquiteto
   (SQL + BI)              (+ Python)          (+ cloud, escala)         (+ decisão técnica)
```

Quase ninguém entra direto como cientista de dados. O caminho comum é entrar
analisando dados com SQL e BI, e migrar depois. **SQL é o denominador comum de
todos os cargos** — se você for aprender uma coisa só desta disciplina com
profundidade, aprenda SQL.

## O mercado em Recife e Pernambuco

Vocês estão em uma das melhores praças do país para essa área fora do eixo Rio–SP:

- **Porto Digital** — um dos maiores parques tecnológicos do Brasil, com centenas
  de empresas no Recife Antigo, muitas com times de dados.
- **Empresas locais de dados e IA** — a [aula 09](../01-aulas/aula-09-di2win-apresentacao-institucional.pdf)
  é a apresentação institucional da **Di2win**, uma empresa pernambucana de
  processamento inteligente de documentos. Aproveite: aula com empresa é
  oportunidade de contato, não hora de mexer no celular.
- **Setor público e cidades inteligentes** — prefeituras, governo do estado e
  iniciativas como as vistas nos desafios
  ([GovInPlay, InovaRecife](../03-desafios/README.md)) contratam e abrem editais.
  O tema do Observatório de Dados das aulas 04, 06 e 07 é exatamente esse mercado.
- **Trabalho remoto** — boa parte das vagas de dados no Brasil é remota, o que
  amplia muito o alcance de quem mora fora do eixo.

## Sobre salários

Não confie em número que alguém cita de cabeça, inclusive este documento. Consulte
as fontes que publicam dados agregados e atualizados:

- **State of Data Brazil** (Data Hackers + Bain) — a pesquisa anual mais completa
  sobre a área no Brasil, com salário por cargo, senioridade e região. É a melhor
  referência disponível, e é gratuita.
- **Glassdoor** e **Love Mondays** — faixas por empresa, com viés de amostra.
- **Vagas abertas com faixa declarada** no LinkedIn e no Gupy — o dado mais
  atualizado que existe, porque é o que está sendo pago agora.

O que dá para afirmar com segurança: a área paga acima da média de TI para a mesma
senioridade, a diferença entre júnior e pleno é grande, e inglês de leitura muda
a faixa de forma perceptível.

## O que fazer ainda na graduação

**1. Tenha um portfólio, não um currículo.** Três projetos publicados no GitHub
valem mais que uma lista de cursos. E você já tem material para isso: o projeto do
seminário e os desafios desta disciplina.

**2. Um projeto de portfólio bom tem quatro coisas:** uma pergunta clara, dados
públicos, código que roda, e um README que explica a conclusão para quem não vai
ler o código. A maioria dos portfólios falha na quarta.

**3. Use dados brasileiros.** Um projeto sobre a educação de Olinda ou sobre gastos
do Congresso diz mais sobre você em uma entrevista no Recife do que o milésimo
notebook sobre o Titanic. As fontes estão em
[`../05-recursos/datasets.md`](../05-recursos/datasets.md).

**4. Aprenda Git de verdade.** Não só `commit` e `push` — branch, pull request,
resolver conflito. É requisito eliminatório em qualquer time.

**5. Inglês de leitura.** A documentação boa está toda em inglês, e sempre
desatualizada em português.

**6. Certificações, com moderação.** As de nuvem (AWS, Google Cloud, Azure) ajudam
a passar por filtro de recrutador em vaga de engenharia. Nenhuma substitui
portfólio, e nenhuma vale a pena antes de você saber SQL bem.

## Como usar esta disciplina a seu favor

| O que você faz aqui | Como isso vira emprego |
| --- | --- |
| Projeto do seminário | Primeiro item do portfólio, publicado no GitHub com README |
| [Desafios](../03-desafios/README.md) com dados públicos | Prova de que você trabalha com dado real, sujo, não com dataset de curso |
| [Notebook dos gastões](../02-notebooks/) | Demonstra web scraping + pandas + visualização, três habilidades cobradas |
| SQL da [aula 03](../01-aulas/aula-03-exemplo-schema.sql) | A competência mais pedida em entrevista técnica de dados |
| Apresentar o seminário | Treino direto da parte que mais reprova candidato em entrevista final |

O aluno que sai desta disciplina com um repositório organizado e um projeto que ele
consegue explicar em cinco minutos está à frente de boa parte dos candidatos a
estágio — não por saber mais, mas por conseguir mostrar.
