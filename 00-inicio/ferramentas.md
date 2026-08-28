# Ferramentas

## Comece pelo mínimo

Você não precisa instalar nada para acompanhar a disciplina. Um navegador e uma
conta Google bastam para as primeiras aulas.

| Prioridade | Ferramenta | Por quê |
| --- | --- | --- |
| **1. Agora** | [Google Colab](https://colab.research.google.com) | Roda Python no navegador, sem instalar nada, com pandas e matplotlib já prontos. É onde vivem os [notebooks da disciplina](../02-notebooks/) |
| **2. Agora** | Conta no [GitHub](https://github.com) | Onde este repositório está e onde seu portfólio vai morar |
| **3. Logo** | Um cliente SQL | Para praticar o [schema da aula 03](../01-aulas/aula-03-exemplo-schema.sql) |
| **4. Depois** | Python local + VS Code | Quando o Colab começar a limitar você |
| **5. No projeto** | Power BI ou Looker Studio | Para dashboards do seminário |

## A stack da área, em camadas

Entender onde cada tecnologia se encaixa evita a sensação de que são cem coisas
desconexas. São cinco camadas, e cada aula da disciplina mora em uma delas.

```
  COLETA        →   ARMAZENAMENTO   →   PROCESSAMENTO   →   ANÁLISE      →   APRESENTAÇÃO
  APIs, scraping    Data lake, DW       Spark, MapReduce    SQL, pandas      BI, Observatório
  Kafka (streaming) HDFS, S3            ETL / ELT           ML               dashboards
  ───────────────   ───────────────     ───────────────     ────────────     ───────────────
  aula 02           aulas 02–03         aula 03             aulas 05, 08     aulas 04, 06–07
```

## O que aprender, em ordem

**SQL — primeiro, sempre.** É o que mais aparece em entrevista e o que menos muda
com o tempo. O [minicurso da disciplina](../05-recursos/minicurso-de-sql.pdf) cobre
o necessário. Meta: `SELECT`/`WHERE`, `JOIN`, `GROUP BY` com agregações, e
subconsultas.

**Python + pandas — segundo.** A dupla que faz o trabalho diário de tratamento de
dados. Cinco operações resolvem a maior parte dos casos: ler arquivo, filtrar,
selecionar colunas, agrupar/agregar, ordenar. O
[notebook dos gastões](../02-notebooks/README.md) usa todas.

**Visualização — junto com pandas.** `matplotlib` para o básico, `seaborn` quando
quiser algo mais apresentável sem esforço. A regra que importa não é técnica: todo
gráfico precisa de título, eixos rotulados e unidade.

**Git — em paralelo, desde já.** `clone`, `add`, `commit`, `push`, `pull`, `branch`
e como resolver um conflito. Pratique neste próprio repositório.

**Depois, conforme o rumo que você escolher:**

| Ferramenta | O que é | Quando faz sentido |
| --- | --- | --- |
| **Apache Spark** | Processamento distribuído em memória; o sucessor prático do MapReduce | Quando o dado não cabe mais em uma máquina |
| **Apache Kafka** | Fila de mensagens para dados em tempo real ([download](https://kafka.apache.org/community/downloads/)) | Quando os dados chegam continuamente, não em lotes |
| **Hadoop / HDFS** | O sistema de arquivos distribuído original | Mais para entender o conceito e a prova do que para usar hoje |
| **Airflow** | Orquestrador — agenda e monitora pipelines | Quando você tem vários ETLs que dependem uns dos outros |
| **dbt** | Transformação de dados escrita em SQL, versionada e testada | Caminho de analytics engineer |
| **Power BI / Looker Studio** | Dashboards | No projeto do seminário, e em qualquer vaga de analista |
| **AWS / GCP / Azure** | Nuvem, onde quase tudo acima roda de verdade | Quando for buscar vaga de engenharia de dados |

Uma observação que vale a prova e a vida profissional: **MapReduce hoje se estuda
mais como conceito do que como ferramenta**. Quase ninguém escreve MapReduce à mão
em 2026 — usa-se Spark, que faz o mesmo de forma mais rápida e com código mais
simples. Mas Spark é uma implementação da ideia do MapReduce, e por isso entender o
original continua sendo o que faz o resto fazer sentido.

## Montando o ambiente local

Quando o Colab ficar apertado:

```bash
# Python 3 já vem na maioria das distribuições Linux
python3 --version

# Ambiente isolado por projeto — evita conflito de versões
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# O básico da análise de dados
pip install pandas matplotlib jupyter requests beautifulsoup4 seaborn
```

Para rodar os notebooks localmente: `jupyter notebook`.

Sempre use ambiente virtual (`venv`). Instalar pacotes no Python do sistema é a
forma mais rápida de quebrar o ambiente e passar uma tarde consertando.

## Onde buscar dados

As fontes usadas na disciplina, com o que cada uma serve, estão em
[`../05-recursos/datasets.md`](../05-recursos/datasets.md).
