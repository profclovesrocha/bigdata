# 02 — Notebooks

Código escrito em sala. Todos abrem direto no Google Colab pelo badge no topo do
notebook, sem instalar nada.

| Notebook | Aula | Tema |
| --- | --- | --- |
| [`gastoes-congresso.ipynb`](gastoes-congresso.ipynb) | 17/09/2025 | Web scraping + análise de dados abertos com pandas |

---

## `gastoes-congresso.ipynb` — Os 10 maiores gastões do Senado

Pipeline completo de dados públicos, do HTML bruto ao gráfico. É o exemplo prático
das etapas de **extração → transformação → visualização** vistas na
[aula 03 (ETL)](../01-aulas/aula-03-banco-de-dados-operacional-etl-e-mapreduce.pdf).

**Fonte:** <http://meucongressonacional.com/senador>

**Bibliotecas:** `pandas`, `requests`, `BeautifulSoup` (bs4), `matplotlib`

### Passo a passo

| Etapa | O que faz |
| --- | --- |
| 1. Extração | `requests.get()` baixa o HTML da página de senadores |
| 2. Parsing | `BeautifulSoup` localiza a tabela (`soup.find(name='table')`) |
| 3. Carga | `pd.read_html()` converte a tabela HTML em DataFrame |
| 4. Ordenação | `sort_values(by='R$/dia')` ordena pelo gasto diário, do maior para o menor |
| 5. Limpeza | renomeia colunas e descarta a coluna `Gastos` |
| 6. Recorte | mantém apenas as 10 primeiras linhas |
| 7. Visualização | gráfico de barras horizontais com `matplotlib` |

### Erros conhecidos no código original

O notebook foi digitado ao vivo em aula e **não roda de ponta a ponta como está**.
Corrigir estes pontos é um bom exercício de leitura de código:

1. **Célula 2** — o import é `import requests as rq`, mas a chamada usa
   `requests.get(...)`. Use `rq.get(...)` (ou troque o import por `import requests`).
2. **Célula 2 → 4** — a resposta do `get()` nunca é guardada em variável, e a
   célula 4 usa `content`, que não existe. Faça
   `resposta = rq.get(url)` e depois `BeautifulSoup(resposta.content, 'html.parser')`.
3. **Célula 6** — `ascending=[False]` passa uma lista onde `by` é um único nome de
   coluna. Use `ascending=False`.
4. **Célula 11** — o gráfico usa `Senador` e `Gasto_dia` soltos, que são nomes de
   colunas e não variáveis. Use `df_ordenado3['Senador']` e
   `df_ordenado3['Gasto_dia']`.
5. **Célula 7** — o `rename` por atribuição direta em `.columns` depende de a tabela
   ter exatamente 5 colunas. Se o site mudar o layout, confira com `df.columns`
   antes de renomear.
