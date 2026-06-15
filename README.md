# IMT_CD_PROJETO_1

Repositório do **Projeto 1** da disciplina **ECM514 — Ciência dos Dados**  
Instituto Mauá de Tecnologia — 2025

> **Nota:** Em relação à entrega do vídeo, optamos por realizar dois vídeos de até 5 minutos cada, uma para a Parte A (Pesquisa de Opinião) e outra para a Parte B (Séries Temporais).

---

## 👥 Integrantes

| Nome | RA |
|------|----|
| Felipe Kenzo Ohara Sakae | 22.00815-2 |
| Guilherme Martins Souza Paula | 22.00006-2 |
| Lucas Gozze Crapino | 22.00667-2 |
| Murillo Penha Strina | 22.00730-0 |
| Pedro Campos Dec | 22.00787-3 |
| Vinicius Garcia Imendes Dechechi | 22.01568-0 |

---

## 📁 Estrutura do Repositório

```
IMT_CD_PROJETO_1/
│
├── README.md
│
├── apresentacao/
│   └── apresentacao_CD.pptx
│
├── parte_a_pesquisa_opiniao/
│   ├── notebook_parte_a.ipynb
│   └── dados/
│       ├── 04829.SAV
│       └── dados_externos/
│           ├── tabela10374.csv
│           ├── tabela10372.csv
│           ├── tabela10361.xlsx
│           └── consulta_cand_2022_BRASIL.csv
│
└── parte_b_series_temporais/
    ├── notebook_parte_b.ipynb
    └── dados/
```

---

## 📊 Parte A — Pesquisa de Opinião: Racismo no Brasil

**Tema:** Percepção dos Brasileiros sobre o Racismo no Brasil  
**Fonte:** CESOP/IPEC — Pesquisa 04829 (abril de 2023, n = 2.000)

### Bases externas utilizadas

| Base | Fonte | Ano | Conexão com a pesquisa |
|------|-------|-----|------------------------|
| PNAD Contínua — Rendimento por raça e UF | IBGE / SIDRA (Tab. 10374) | 2023 | Desigualdade salarial real vs. percepção de racismo |
| PNAD Contínua — Horas trabalhadas por raça | IBGE / SIDRA (Tab. 10372) | 2023 | Gap de rendimento por hora trabalhada |
| PNAD Contínua — Informalidade por raça | IBGE / SIDRA (Tab. 10361) | 2023 | Mercado de trabalho e desigualdade estrutural |
| Candidatos e eleitos por raça | TSE — Repositório Eleitoral | 2022 | Representatividade real vs. percebida (P20) |
| Composição racial do Judiciário | CNJ — DataJud | 2023 | Pirâmide de exclusão institucional |

### Análises desenvolvidas

1. **Paradoxo da Consciência Racial** — gap entre reconhecer o racismo estrutural e assumir responsabilidade individual, por raça
2. **Distância Social do Racismo** — declínio da percepção conforme a afirmação se aproxima da esfera pessoal
3. **Anatomia do Apoio às Cotas** — hierarquia de apoio (PcD > Social > Racial > Mulheres > LGBTQIA+) por raça e posição política
4. **Motor das Desigualdades** — raça vs. classe social como explicação das desigualdades, por renda e escolaridade
5. **Definição Popular de Racismo** — adoção de definição estrutural vs. restrita, por escolaridade
6. **Percepção do Racismo Policial** — afirmações P19 por raça e posição política
7. **Correlação PNAD 2023** — gap salarial real por UF vs. percepção de racismo (paradoxo da normalização)
8. **Correlação TSE 2022** — representatividade real dos eleitos vs. percepção de sub-representação
9. **Correlação CNJ 2023** — pirâmide de exclusão (28% negros entre servidores → 15% juízes → 11% desembargadores)
10. **PCA** — dimensões latentes na percepção do racismo (itens P5)

### Entregas

| Artefato | Link |
|----------|------|
| 📓 Notebook (Colab) | [`parte_a_pesquisa_opiniao/notebook_parte_a.ipynb`](parte_a_pesquisa_opiniao/notebook_parte_a.ipynb) |
| 🗂 Dados | [`parte_a_pesquisa_opiniao/dados/`](parte_a_pesquisa_opiniao/dados/) |
| 🎥 Vídeo (YouTube) | [Assistir apresentação — Parte A](https://www.youtube.com/watch?v=D47b2_NHeZw) |
| 📑 Slides | [`apresentacao/apresentacao_CD.pptx`](apresentacao/apresentacao_CD.pptx) |

---

## 📈 Parte B — Séries Temporais: Inadimplência no Brasil

**Tema:** Evolução da Inadimplência de Pessoas Físicas e Jurídicas (2012–2024)  
**Fonte principal:** Banco Central do Brasil — API SGS

### Séries utilizadas

| Série | Código SGS | Descrição |
|-------|-----------|-----------|
| Inadimplência PF | 21082 | Taxa total — Pessoas Físicas |
| Inadimplência PJ | 21083 | Taxa total — Pessoas Jurídicas |
| Inadimplência Total | 21084 | Taxa geral do sistema |
| Crédito Pessoal PF | 20400 | Inadimplência — crédito pessoal |
| Selic acumulada mês | 4189 | Taxa Selic (% a.m.) |
| IPCA mensal | 433 | Variação mensal de preços |
| Desemprego PNAD | 24369 | Taxa de desocupação |
| Endividamento das famílias | 29037 | % famílias endividadas |
| PIB trimestral | 4380 | Variação trimestral do PIB |

### Análises desenvolvidas

1. **PF vs. PJ** — comportamentos distintos ao longo dos ciclos econômicos
2. **Decomposição por modalidade** — crédito pessoal, cartão, veículos, habitação
3. **Ciclos econômicos e choques** — recessão 2015-16, pandemia 2020, ciclo Selic 2021-23
4. **Correlação com Selic e IPCA** — scatter com diferentes defasagens (0, 3 e 6 meses)
5. **Correlação com Desemprego e PIB** — matriz de correlação entre todas as variáveis
6. **Endividamento vs. Inadimplência** — scatter colorido por período histórico
7. **Decomposição STL** — tendência, sazonalidade e resíduo para PF e PJ
8. **Cross-Correlation (CCF)** — defasagem de transmissão dos choques para a inadimplência

### Entregas

| Artefato | Link |
|----------|------|
| 📓 Notebook (Colab) | [`parte_b_series_temporais/notebook_parte_b.ipynb`](parte_b_series_temporais/notebook_parte_b.ipynb) |
| 🗂 Dados | [`parte_b_series_temporais/dados/`](parte_b_series_temporais/dados/) |
| 🎥 Vídeo (YouTube) | [Assistir apresentação — Parte B](https://www.youtube.com/watch?v=fvffIDevyAM) |
| 📑 Slides | [`apresentacao/apresentacao_CD.pptx`](apresentacao/apresentacao_CD.pptx) |

---

## 🤖 Uso de Inteligência Artificial

Este projeto foi desenvolvido **com auxílio de Inteligência Artificial** (Claude, Anthropic).  
O uso de IA incluiu sugestão de análises, geração e refinamento de código e diagnóstico de bugs.  
Todo o código foi **revisado, executado e validado pela equipe**.  
As interpretações e conclusões são de **responsabilidade dos autores**.

---

## 📚 Referências

- CESOP/IPEC (2023). *Pesquisa 04829 — Percepção dos Brasileiros sobre o Racismo no Brasil*. Unicamp.
- IBGE (2023). *PNAD Contínua Anual*. https://sidra.ibge.gov.br
- TSE (2022). *Repositório de Dados Eleitorais*. https://dadosabertos.tse.jus.br
- CNJ (2023). *DataJud / Censo do Poder Judiciário*. https://www.cnj.jus.br
- Banco Central do Brasil (2024). *Sistema Gerenciador de Séries Temporais (SGS)*. https://www3.bcb.gov.br/sgspub