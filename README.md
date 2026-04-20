# 📊 Mapa de Reincidência de Chamados

> 🔍 Transformando dados de chamados em decisões estratégicas

---

## 🎯 Sobre o Projeto

O **Mapa de Reincidência** é uma ferramenta de análise que identifica padrões de falhas recorrentes em chamados de manutenção.

A partir de um arquivo CSV exportado do sistema, ele entrega:

- 📍 Locais com maior reincidência  
- 🔁 Problemas que voltam a acontecer  
- ⚠️ Serviços mal resolvidos  
- 💸 Impacto financeiro da recorrência  
- 🧠 Evidência textual de falhas recorrentes  

📦 **Saída final:** Excel completo + gráficos prontos para gestão

---

## 🧠 Lógica de Criticidade

```python
score_base = reincidencias * (10 - nota_media)

score_avancado = score_base * (1 + custo_acumulado / custo_maximo) * bonus_textual


Bônus textual (+20%) quando há recorrência explícita nas descrições:

"voltou", "mesmo problema", "não resolveu"

🚨 Por que usar?
Problema	Impacto
Repetição de chamados	💸 Custos duplicados
Solução temporária	📉 Baixa qualidade
Falhas recorrentes	🏭 Impacto operacional
SLA comprometido	⚖️ Risco contratual

👉 O projeto gera um ranking de criticidade acionável

📦 Output
📁 resultado_reincidencia.xlsx
📊 Resumo Executivo
🥇 Ranking por Local
🧠 Análise de Texto
🔤 Termos mais frequentes
🗂️ Dados brutos enriquecidos
📈 Gráficos
Ranking Top N
Heatmap de reincidência
Distribuição de criticidade
Comparativo temporal vs textual
Análise de termos

🛠️ Stack

🐍 Python 3
📊 pandas
📈 matplotlib / seaborn
📄 openpyxl
📓 Jupyter Notebook
▶️ Como rodar


1. Instalar dependências

pip install pandas numpy matplotlib seaborn openpyxl

2. Executar
Coloque o CSV na pasta do projeto
Abra o notebook .ipynb
Clique em Run All

✔️ O arquivo Excel será gerado automaticamente ao final

⚙️ Parâmetros

JANELA_REINCIDENCIA = 90  # dias
TOP_N = 15
NOTA_PADRAO = 7

📄 Estrutura do CSV
Campo	Obrigatório
Numero_Chamado	✅
Local_Nome	✅
Tipo	✅
Data_Criacao	✅
Valor_Total	✅
Nota_Inicial	✅

📈 Qualidade
Métrica	Status
Testes	✅ 10 passando
Bugs críticos	✅ 100% corrigidos
Performance	⚡ Otimizada
Manutenibilidade	🧼 Alta

🧩 Roadmap
 Dashboard interativo (Streamlit / Power BI)
 Integração com API de chamados
 Alertas automáticos de reincidência
 Machine Learning para previsão de falhas
🤝 Contribuição

Sugestões e melhorias são bem-vindas via:

Pull Requests
Issues
📌 Resumo

Dados brutos → Diagnóstico → Prioridade → Ação
