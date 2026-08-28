# Como estudar

## Como usar este repositório

O repositório é numerado na ordem em que você deve usá-lo:

```
00-inicio/       Você está aqui. Contexto antes do conteúdo.
01-aulas/        Slides, na ordem do curso. É a espinha dorsal.
02-notebooks/    O código de sala. Rode, quebre, conserte.
03-desafios/     Onde o conteúdo vira projeto.
04-avaliacoes/   Regras do jogo: notas, datas, grupos.
05-recursos/     Aprofundamento e fontes de dados.
```

A regra prática: **cada aula em `01-aulas/` deve terminar em algo feito nas pastas
02 ou 03**. Slide lido sem prática vira conteúdo que você reconhece na prova mas
não sabe usar — e o projeto vale mais que a prova.

## A rotina que funciona

Big Data é uma disciplina cumulativa: a aula 04 assume a 03, que assume a 02. Ficar
para trás custa caro. Uma hora por semana bem gasta rende mais que cinco horas na
véspera da prova.

**Depois de cada aula (30–40 min):**

1. Abra os slides e escreva, com suas palavras, **três frases** sobre o que foi
   dado. Não copie do slide — se você não consegue escrever sem olhar, você não
   entendeu ainda.
2. Anote os termos novos no seu caderno e confira o
   [`glossario.md`](glossario.md).
3. Escreva **uma pergunta** que ficou em aberto. Leve na aula seguinte.

**Uma vez por semana (1h):**

4. Rode algum código relacionado. Pode ser o notebook da aula, uma consulta SQL,
   qualquer coisa que execute.
5. Revise as três frases das aulas anteriores — não as reescreva, só tente
   lembrar antes de olhar. Esse esforço de lembrar é o que fixa.

## O teste de Feynman

O melhor detector de "eu achei que sabia": explique o conceito em voz alta, como se
fosse para alguém do primeiro período, sem usar o jargão. Se você travar, o ponto
onde travou é exatamente o que você não entendeu. Volte ali, e só ali.

Funciona bem em dupla, e funciona ainda melhor com os temas que caem em prova:
MapReduce, os 5 Vs, a diferença entre OLTP e OLAP, e as etapas do ETL.

## Como estudar para a prova escrita (estilo ENADE)

A prova é de **10 questões objetivas**, no formato ENADE. Esse formato tem uma
mecânica própria, e treinar a mecânica vale tanto quanto saber o conteúdo.

- **O texto-base importa.** Questão ENADE quase sempre traz um caso, um gráfico ou
  uma citação antes da pergunta. Leia o enunciado **antes** do texto-base: você
  descobre o que procurar e lê o texto uma vez só.
- **Cuidado com as absolutas.** Alternativas com "sempre", "nunca", "todo",
  "exclusivamente" costumam estar erradas — a área é cheia de "depende do caso".
- **Nas questões de asserção-razão** ("I. … PORQUE II. …"), avalie cada asserção
  isoladamente como verdadeira ou falsa **primeiro**, e só depois pergunte se a II
  justifica a I. Duas frases verdadeiras sem relação causal é a pegadinha clássica.
- **Simulado oficial da disciplina:** <https://abre.ai/bigdata-enade-style>.
  Faça uma vez cedo, para saber onde você está, e de novo perto da prova.
- **Erre no simulado, não na prova.** Para cada erro, escreva uma linha explicando
  *por que* a alternativa certa é certa. Só marcar a resposta correta não ensina nada.

Os temas com maior chance de cair, por serem definições fechadas: os 5 Vs, as
etapas do ETL, o funcionamento do MapReduce, OLTP × OLAP, e tipos de dado
(estruturado, semiestruturado, não estruturado).

## Como atacar o projeto (60% da AV2)

O projeto quebra por motivos previsíveis. Na ordem em que costumam acontecer:

1. **Escolher o tema tarde.** Escolha na primeira semana possível. Os temas
   disponíveis estão em [`../03-desafios/README.md`](../03-desafios/README.md).
2. **Escolher uma pergunta grande demais.** "Analisar a educação de Olinda" não é
   uma pergunta, é um assunto. "As notas de matemática de Olinda caíram entre 2014
   e 2024, e isso acompanha a queda de investimento?" é uma pergunta — tem
   resposta, e a resposta pode ser não.
3. **Só descobrir no fim que o dado não existe.** Antes de se comprometer com a
   pergunta, **baixe o dado e abra**. Veja quantas linhas tem, quais colunas, o
   quanto está vazio. Uma hora aqui economiza duas semanas.
4. **Confundir gráfico com conclusão.** Um gráfico mostra o quê; você precisa dizer
   o e daí. Toda visualização do trabalho deve vir acompanhada de uma frase que
   comece com "isso significa que…".
5. **Deixar a escrita para o final.** Escreva o texto enquanto analisa. Você vai
   descobrir buracos no raciocínio que a análise sozinha esconde.

O guia oficial do seminário está em
[`../04-avaliacoes/README.md`](../04-avaliacoes/README.md) — leia antes de começar,
não depois.

## Se sua base está fraca

Sem vergonha nenhuma nisso — a maior parte da turma está no mesmo lugar. Tape o
buraco em paralelo com a disciplina, não em vez dela:

- **SQL:** comece pelo [minicurso da disciplina](../05-recursos/minicurso-de-sql.pdf)
  e pratique no [schema de exemplo da aula 03](../01-aulas/aula-03-exemplo-schema.sql).
  Meta mínima: `SELECT` com `WHERE`, `JOIN` entre duas tabelas, `GROUP BY` com
  `COUNT` e `SUM`. Isso já cobre a maioria dos casos reais.
- **Python:** você precisa de listas, dicionários, `for`, `if` e funções. Só isso.
  O resto é biblioteca.
- **pandas:** aprenda cinco operações e você faz 80% do trabalho — ler um arquivo,
  filtrar linhas, selecionar colunas, agrupar e agregar, ordenar.
- **Estatística:** média, mediana, desvio padrão, e principalmente saber que
  **correlação não é causalidade**. Essa última cai em prova e derruba projeto.

## Erros comuns na disciplina

- **Achar que Big Data é sempre a resposta.** Saber dizer "esse volume não justifica
  um cluster" é sinal de maturidade, não de ignorância.
- **Pular a limpeza dos dados.** No mundo real, é a maior parte do trabalho. Dado
  sujo produz gráfico bonito e conclusão errada.
- **Decorar os 5 Vs sem exemplo.** Na prova ENADE eles aparecem dentro de um caso,
  não como pergunta direta. Tenha um exemplo próprio para cada um.
- **Estudar só pelo slide.** O slide é o roteiro da fala do professor, não o
  conteúdo completo. As suas anotações valem mais.
