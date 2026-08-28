# Sobre a disciplina

## O que é Big Data, de verdade

A definição de manual fala em "grandes volumes de dados". É uma definição ruim,
porque não diz onde está a fronteira. A definição útil é operacional:

> **Big Data começa onde a ferramenta comum quebra.**

Uma planilha aguenta cerca de um milhão de linhas. Um banco relacional em um
servidor aguenta muito mais, até parar. Quando o dado não cabe mais na memória de
uma máquina, ou chega rápido demais para ser processado no ritmo em que chega, ou
vem em formatos que não entram numa tabela — aí você precisa de outra abordagem.
Essa abordagem é o conteúdo da disciplina.

## Os 5 Vs

O jeito clássico de descrever o problema. Os três primeiros são os originais; os
dois últimos foram acrescentados depois e são os que mais aparecem em prova.

| V | O que significa | Exemplo concreto |
| --- | --- | --- |
| **Volume** | Quantidade de dados além do que uma máquina processa | Todo o histórico de notas fiscais de um estado |
| **Velocidade** | Ritmo de chegada e de resposta exigido | Sensores de trânsito enviando posição a cada segundo |
| **Variedade** | Dados estruturados, semiestruturados e não estruturados juntos | Tabelas + PDFs + fotos + áudio de call center |
| **Veracidade** | O quanto se pode confiar no dado | Cadastro com CPF duplicado, campo preenchido "999999" |
| **Valor** | O retorno que a análise gera | Descobrir quais escolas precisam de reforço primeiro |

Cuidado com o mais comum dos erros: **Veracidade não é o mesmo que Valor**. O
primeiro é sobre qualidade do dado de entrada; o segundo, sobre utilidade do
resultado de saída. Dado veraz sem valor é desperdício; dado valioso sem
veracidade é uma decisão errada tomada com confiança.

## O que esta disciplina cobre

O curso vai do dado bruto até a decisão, nesta ordem:

| Bloco | Aulas | Pergunta que responde |
| --- | --- | --- |
| **Fundamentos** | 00–02 | O que é Big Data e que infraestrutura ele exige? |
| **Dados e processamento** | 03 | Como o dado sai do sistema operacional, é tratado e processado em escala? (banco operacional, ETL, MapReduce) |
| **Aplicação** | 04, 06–07 | Como se constrói uma interface que entrega esses dados a quem decide? (Observatório de Dados, cidades inteligentes) |
| **Casos reais** | 05, 08–09 | Como isso funciona fora da sala? (mineração de dados, dados de educação no Brasil, visão de mercado) |

O índice completo, com o material de cada aula, está em
[`../01-aulas/README.md`](../01-aulas/README.md).

## Os três conceitos que sustentam o resto

Se você entender bem estes três, o resto da disciplina encaixa.

**1. ETL (Extract, Transform, Load).** O caminho que o dado percorre do sistema
onde nasce até o lugar onde é analisado. *Extract*: puxar do banco operacional, da
API, do site. *Transform*: limpar, padronizar, juntar, agregar. *Load*: gravar no
destino analítico. É o assunto da aula 03, e o
[notebook dos gastões](../02-notebooks/README.md) é um ETL completo em miniatura —
extrai de um site, transforma com pandas, carrega num gráfico.

**2. MapReduce.** A ideia que tornou o Big Data possível: em vez de trazer o dado
até um computador grande, leve o processamento até onde o dado está, quebrado em
pedaços. *Map* aplica a mesma operação em cada pedaço, em paralelo e em máquinas
diferentes; *Reduce* junta os resultados parciais em um só. Contar palavras em um
bilhão de documentos vira contar em mil pedaços de um milhão e somar as contagens.

**3. Bancos operacionais × analíticos.** O banco que atende o sistema no dia a dia
(OLTP) é otimizado para escrever pouca coisa muitas vezes, rápido, sem erro. O
banco que responde às perguntas do negócio (OLAP) é otimizado para ler muita coisa
de uma vez. São desenhos opostos, e é por isso que o ETL existe: para mover o dado
de um mundo ao outro sem derrubar o sistema de produção.

## O que você deve saber fazer no final

- Explicar por que uma solução de Big Data é necessária em um caso concreto — e
  reconhecer quando **não** é (a resposta certa muitas vezes é "isso cabe num
  Postgres").
- Encontrar, baixar e avaliar a qualidade de uma base de dados pública.
- Fazer o ciclo ETL completo em Python: extrair, limpar, transformar, visualizar.
- Ler e escrever SQL para consultas analíticas.
- Explicar MapReduce com um exemplo próprio.
- Transformar uma análise em uma resposta que alguém que não é técnico consiga usar.

Esse último item é o que mais separa aluno de profissional, e é exatamente o que o
projeto de 60% da AV2 cobra.

## O que a disciplina não é

Não é um curso de Machine Learning — ML aparece como aplicação, não como foco (o
[e-book de ML](../05-recursos/ebook-machine-learning-codigos.pdf) está lá para quem
quiser ir além). Não é um curso de administração de clusters Hadoop. E não é um
curso de programação: espera-se que você já consiga ler Python básico. Se não
consegue, o roteiro em [`como-estudar.md`](como-estudar.md) diz por onde tapar
esse buraco antes que ele atrapalhe.
