# Glossário

Os termos que aparecem nas aulas, em uma frase cada. Boa parte da dificuldade
inicial em Big Data é vocabulário — deixe este arquivo aberto durante as aulas.

## Conceitos gerais

**Big Data** — Conjunto de abordagens para dados que ultrapassam a capacidade das
ferramentas convencionais, em volume, velocidade ou variedade.

**5 Vs** — Volume, Velocidade, Variedade, Veracidade e Valor. Ver
[`sobre-a-disciplina.md`](sobre-a-disciplina.md#os-5-vs).

**Dado estruturado** — Cabe numa tabela com colunas definidas: um banco relacional,
uma planilha.

**Dado semiestruturado** — Tem organização, mas não em formato de tabela: JSON,
XML, logs.

**Dado não estruturado** — Sem formato prévio: texto livre, imagem, áudio, vídeo. É
a maior parte dos dados existentes, e a mais difícil de usar.

**Metadado** — Dado sobre o dado: quando foi coletado, por quem, em que unidade, o
que significa cada coluna. Sem isso, dado é número solto.

**Governança de dados** — As regras sobre quem pode acessar o quê, como se garante
qualidade e como se atende à LGPD.

**LGPD** — Lei Geral de Proteção de Dados. Regula o tratamento de dados pessoais no
Brasil; determina o que você pode coletar, por quanto tempo guarda e o que precisa
anonimizar.

## Armazenamento

**OLTP** (*Online Transaction Processing*) — O banco que roda o sistema no dia a
dia. Otimizado para escritas pequenas e frequentes, com consistência. O "banco
operacional" da aula 03.

**OLAP** (*Online Analytical Processing*) — O banco voltado à análise. Otimizado
para ler muitos registros de uma vez e agregar.

**Data Warehouse (DW)** — Repositório central com dados já limpos e modelados para
análise. Estruturado antes de gravar (*schema-on-write*).

**Data Lake** — Repositório que guarda dados brutos em qualquer formato; a estrutura
é aplicada só na hora de ler (*schema-on-read*). Mais flexível, mais fácil de virar
bagunça.

**Data Lakehouse** — Tentativa de juntar os dois: a flexibilidade do lake com a
confiabilidade e o desempenho do warehouse.

**HDFS** (*Hadoop Distributed File System*) — Sistema de arquivos que espalha
arquivos grandes em blocos por várias máquinas, com réplicas.

**Modelagem dimensional** — Organização do DW em tabelas *fato* (os eventos, os
números) e *dimensão* (o contexto: tempo, lugar, produto). É o desenho "estrela".

## Processamento

**ETL** (*Extract, Transform, Load*) — Extrair do sistema de origem, transformar e
carregar no destino. Transforma antes de carregar.

**ELT** — A variação moderna: carrega o dado bruto primeiro e transforma já dentro
do destino, aproveitando o poder de processamento da nuvem.

**Pipeline de dados** — O caminho automatizado que leva o dado da origem ao
destino, incluindo o ETL e o que mais for necessário.

**MapReduce** — Modelo de processamento distribuído em duas etapas: *Map* aplica a
mesma operação a pedaços do dado em paralelo, *Reduce* combina os resultados
parciais.

**Apache Spark** — Motor de processamento distribuído que executa em memória; o
sucessor prático do MapReduce, muito mais rápido para a maioria dos casos.

**Processamento em lote** (*batch*) — Processa um volume acumulado de uma vez, em
horários definidos. Ex.: fechamento diário às 3h da manhã.

**Processamento em tempo real** (*streaming*) — Processa cada evento conforme ele
chega. Ex.: detectar fraude no momento da transação.

**Apache Kafka** — Plataforma de streaming que funciona como fila entre quem produz
e quem consome os dados.

**Escalabilidade horizontal** — Aguentar mais carga acrescentando máquinas. É o
modelo do Big Data.

**Escalabilidade vertical** — Aguentar mais carga colocando uma máquina maior.
Mais simples, mas esbarra num teto físico e de preço.

**Cluster** — Conjunto de máquinas trabalhando como se fossem uma só.

## Análise

**Mineração de dados** (*data mining*) — Buscar padrões e relações não óbvias em
grandes volumes de dados. Tema da aula 05.

**Web scraping** — Extrair dados de páginas web pelo HTML, quando não há API.
Técnica do [notebook dos gastões](../02-notebooks/README.md).

**API** (*Application Programming Interface*) — Ponto de acesso pelo qual um sistema
entrega dados a outro de forma estruturada. Sempre prefira a API ao scraping,
quando existir.

**Machine Learning** — Algoritmos que aprendem padrões a partir de dados, em vez de
seguir regras escritas à mão.

**Análise descritiva / preditiva / prescritiva** — O que aconteceu / o que deve
acontecer / o que fazer a respeito. Em ordem crescente de dificuldade e de valor.

**Correlação × causalidade** — Duas variáveis se moverem juntas não significa que
uma cause a outra. O erro mais comum e mais caro da área.

**KPI** (*Key Performance Indicator*) — O número escolhido para medir se algo está
indo bem. A escolha do KPI é uma decisão de negócio, não técnica.

## Aplicação

**Dados abertos** (*open data*) — Dados públicos disponibilizados livremente para
uso e redistribuição. Base dos desafios da disciplina.

**Cidade inteligente** (*smart city*) — Cidade que usa dados e tecnologia para
melhorar serviços públicos e qualidade de vida. Tema das aulas 04, 06 e 07.

**Observatório de Dados** — Plataforma que reúne, trata e publica indicadores de um
território para apoiar decisões públicas e o controle social.

**Dashboard** — Painel visual com os indicadores acompanhados de forma contínua.

**Business Intelligence (BI)** — O conjunto de práticas e ferramentas que
transforma dados em relatórios e painéis para decisão.
