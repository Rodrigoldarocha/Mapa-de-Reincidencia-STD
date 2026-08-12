# 📊 Mapa de Reincidência de Chamados

> 🔍 **Transformando dados de manutenção em decisões estratégicas.**

Ferramenta de análise que identifica **falhas recorrentes, problemas mal resolvidos e impactos financeiros** a partir de dados de chamados de manutenção.

---

## 🎯 Sobre o Projeto

O **Mapa de Reincidência** analisa históricos de chamados para encontrar padrões que normalmente passam despercebidos.

### 🔎 O que identifica

* 📍 Locais com maior reincidência
* 🔁 Problemas que voltam a acontecer
* ⚠️ Serviços potencialmente mal resolvidos
* 💸 Impacto financeiro das recorrências
* 🧠 Evidências textuais nas descrições dos chamados
* 📈 Tendências e concentração de problemas

**Resultado:** um ranking de criticidade que ajuda a transformar dados operacionais em **ações de manutenção**.

---

## 🧠 Lógica de Criticidade

O projeto combina reincidência, avaliação, custo e evidências textuais.

```python
score_base = reincidencias * (10 - nota_media)

score_avancado = (
    score_base
    * (1 + custo_acumulado / custo_maximo)
    * bonus_textual
)
```

### 🧠 Evidência textual

Um bônus de **20%** pode ser aplicado quando a descrição apresenta indícios explícitos de recorrência, como:

```text
"voltou"
"mesmo problema"
"não resolveu"
```

### 🚨 Por que isso importa?

| Problema                 | Impacto                |
| ------------------------ | ---------------------- |
| 🔁 Repetição de chamados | 💸 Custos duplicados   |
| 🛠️ Solução temporária   | 📉 Baixa qualidade     |
| ⚠️ Falhas recorrentes    | 🏭 Impacto operacional |
| ⏱️ SLA comprometido      | ⚖️ Risco contratual    |

---

## 📦 Resultados

O processamento gera:

### 📄 Excel

`resultado_reincidencia.xlsx`

Com:

* 📊 Resumo executivo
* 🥇 Ranking por local
* 🧠 Análise textual
* 🔤 Termos mais frequentes
* 🗂️ Dados enriquecidos

### 📈 Visualizações

* 🥇 Ranking Top N
* 🔥 Heatmap de reincidência
* 📊 Distribuição de criticidade
* 📅 Análise temporal
* 🧠 Comparativo temporal × textual
* 🔤 Frequência de termos

---

## 🛠️ Stack

* 🐍 **Python 3**
* 📊 **Pandas**
* 🔢 **NumPy**
* 📈 **Matplotlib**
* 🎨 **Seaborn**
* 📄 **OpenPyXL**
* 📓 **Jupyter Notebook**

---

## ▶️ Como executar

### 1. Instale as dependências

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

### 2. Execute o projeto

Coloque o arquivo CSV na pasta do projeto e abra o notebook:

```text
.ipynb
```

Depois:

```text
Run All ▶️
```

O arquivo Excel será gerado automaticamente ao final do processamento.

---

## ⚙️ Parâmetros

Os principais parâmetros podem ser ajustados no notebook:

```python
JANELA_REINCIDENCIA = 90  # dias
TOP_N = 15
NOTA_PADRAO = 7
```

---

## 📄 Dados de Entrada

O CSV deve conter os seguintes campos:

| Campo            | Obrigatório |
| ---------------- | ----------- |
| `Numero_Chamado` | ✅           |
| `Local_Nome`     | ✅           |
| `Tipo`           | ✅           |
| `Data_Criacao`   | ✅           |
| `Valor_Total`    | ✅           |
| `Nota_Inicial`   | ✅           |

---

## 📈 Qualidade

| Métrica             | Status        |
| ------------------- | ------------- |
| 🧪 Testes           | ✅ 10 passando |
| 🐛 Bugs críticos    | ✅ Corrigidos  |
| ⚡ Performance       | Otimizada     |
| 🧼 Manutenibilidade | Alta          |

---

## 🧩 Roadmap

* [ ] 📊 Dashboard interativo com Streamlit / Power BI
* [ ] 🔌 Integração com API de chamados
* [ ] 🚨 Alertas automáticos de reincidência
* [ ] 🤖 Machine Learning para previsão de falhas
* [ ] 📡 Monitoramento contínuo dos indicadores

---

## 🤝 Contribuição

Sugestões e melhorias são bem-vindas através de:

* 💡 Issues
* 🔀 Pull Requests
* 📝 Sugestões de melhoria

---

## 📌 Resumo

```text
📥 Dados brutos
      ↓
🔎 Diagnóstico
      ↓
🔁 Identificação de reincidências
      ↓
📊 Criticidade
      ↓
🎯 Priorização
      ↓
🛠️ Ação
```

> **O objetivo não é apenas identificar chamados repetidos, mas descobrir onde a manutenção está falhando e transformar essa informação em prioridade operacional.**
