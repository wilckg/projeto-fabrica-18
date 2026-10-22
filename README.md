# ✅ Boletim em Dados — a turma conta a verdade

Uma **escola** quer entender o desempenho dos alunos além da média simples.

Você foi convidado(a) por uma **escola do seu bairro** para investigar as notas de 80 alunos em 4 disciplinas e transformar números em **decisões**.

A missão é direta e útil: **importar**, **limpar**, **analisar** e **visualizar** um dataset — tudo em **Google Colab**, usando **NumPy, Pandas, Matplotlib e Seaborn**.

Projeto pensado para **jovens de 14 a 18 anos**: linguagem técnica, mas acessível, e um toque de design para ficar gostoso de ler. ✨

> 🎯 **Nível:** conclusão do curso *Ciência de Dados com Python* (40h) — Aula 10, Projeto Integrador.
> 🚫 **Não usar:** machine learning, Scikit-learn, web ou banco de dados. Só as 4 bibliotecas do curso.

---

## 🎬 Enunciado — A missão do(a) cientista de dados

A coordenação quer saber **onde a turma vai bem e onde precisa de reforço**. O dataset traz as notas de cada aluno por disciplina, com faltas e turma.

Sua missão: mostrar **qual disciplina é a mais difícil**, se faltas derrubam notas e quem precisa de ajuda — tudo com gráficos que qualquer professor entenda.

### 📊 O dataset

Arquivo `boletim.csv` (80 linhas × 7 colunas) com os seguintes campos:

| Coluna | Tipo | Significado |
|---|---|---|
| `aluno` | str | nome do aluno |
| `turma` | str | A ou B |
| `matematica` | float | nota 0 a 10 |
| `portugues` | float | nota 0 a 10 |
| `ciencias` | float | nota 0 a 10 |
| `historia` | float | nota 0 a 10 |
| `faltas` | int | total de faltas no bimestre |

> **Obs. didática:** os dados são **ilustrativos/simulados** para fins de estudo. Se quiser, troque por um dataset público do mesmo tema.

### O que o projeto deve conter (as 14 etapas)

1. **Importar** o CSV com `pd.read_csv`
2. **Explorar** com `head`, `shape`, `info` e `describe`
3. **Identificar** o que cada coluna significa
4. **Conferir os tipos** de cada coluna (`dtypes`) — estão certos?
5. **Tratar valores ausentes** — `dropna` ou `fillna` (justifique)
6. **Remover duplicados** — `duplicated()` e `drop_duplicates()`
7. **Responder 2 perguntas com filtros** — `df[df['col'] > x]`
8. **Criar 1 coluna nova** — calculada ou com `apply`
9. **Agrupar** com `groupby` por pelo menos 1 categoria
10. **Calcular medidas** com NumPy — `np.array`, `mean`, `max`, `min`, filtros booleanos
11. **Criar 4 gráficos** — Matplotlib e Seaborn, cada um com uma pergunta
12. **Interpretar** cada gráfico com 1 frase
13. **Escrever 3 descobertas** — frases completas, com números
14. **Apresentar 1 conclusão** — o que você recomendaria com base nos dados?

---

## 🔎 Perguntas-guia do projeto

| # | Pergunta | Pista de código |
|---|---|---|
| 1 | Qual disciplina tem a menor média? | `groupby` ou média por coluna |
| 2 | Quantos alunos ficaram abaixo de 6 em cada matéria? | filtros booleanos + `len()` |
| 3 | Faltas influenciam nas notas? | `sns.scatterplot(x='faltas', y='matematica')` |
| 4 | Turma A e B têm desempenho diferente? | `sns.boxplot(x='turma', y=...)` |
| 5 | Qual a média geral da turma? | `np.array` + `mean` |

---

## 💻 Como rodar

**Pré-requisito:** uma conta Google (para o Colab) — nada mais.

```
1) Acesse colab.research.google.com
2) Envie o arquivo boletim.csv pela aba de arquivos (📁)
3) Abra um novo notebook e siga as 14 etapas
4) Rode tudo com Shift + Enter e confira se não há erros
5) Exporte: Arquivo → Fazer download → .ipynb
```

Checklist antes de subir no GitHub:

- [ ] notebook roda do início ao fim **sem erros**
- [ ] dataset (`boletim.csv`) na pasta `data/`
- [ ] pelo menos **4 gráficos** com título e eixos nomeados
- [ ] **3 descobertas** com números + **1 conclusão** final
- [ ] README preenchido com o que você descobriu

---

## 🧠 Conceitos trabalhados

- **NumPy:** arrays, `mean`/`max`/`min`, filtros booleanos
- **Pandas:** `read_csv`, `head`/`info`/`describe`, `loc`/`iloc`, filtros, `dropna`/`fillna`, `drop_duplicates`, colunas calculadas, `apply`, `groupby` + `agg`
- **Matplotlib:** linha, barras, histograma, dispersão (`plt.plot`, `plt.bar`, `plt.hist`, `plt.scatter`)
- **Seaborn:** `countplot`, `barplot`, `histplot`, `boxplot`, `scatterplot`, `heatmap` (correlação)
- **Boas práticas:** explorar antes de analisar · gráfico certo para cada pergunta · correlação não é causa

---

## 🚀 Próximos passos

- Criar a coluna `media_geral` com a média das 4 notas
- Criar `situacao` com `apply`: Aprovado (≥7), Recuperação (5–7), Reprovado (<5)
- Comparar a distribuição das notas com `sns.histplot` por disciplina
- Heatmap de correlação: as notas das matérias andam juntas?

---

## 📂 Estrutura

```
projeto-boletim-em-dados/
├─ README.md            ← este arquivo
├─ notebooks/
│  └─ analise.ipynb     ← seu notebook no Colab
├─ data/
│  └─ boletim.csv         ← o dataset
├─ img/                 ← prints dos gráficos
│  └─ grafico1.png
└─ LICENSE              ← MIT
```

---

## 📋 Rubrica de avaliação (0 a 10)

| Critério | Pontos |
|---|---|
| Importação e organização dos dados | 1,0 |
| Exploração inicial (`head`, `shape`, `info`, `describe`) | 1,0 |
| Limpeza (ausentes e duplicados) | 1,5 |
| Manipulação com Pandas (filtros, colunas, `groupby`) | 2,0 |
| Uso de NumPy | 1,0 |
| Visualizações (4 gráficos com propósito) | 2,0 |
| Interpretação (3 descobertas) | 1,0 |
| Apresentação (5–10 min) | 0,5 |
| **TOTAL** | **10,0** |

---

## 📝 Licença

Projeto sob **MIT** — use, adapte e compartilhe. ✅
