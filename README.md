# Relatório Final – Análise de Evasão de Clientes na TelecomX_BR

---

## 📌 Relatório Final – Análise de Evasão de Clientes na TelecomX_BR

### 1. Introdução

A evasão de clientes, conhecida como **churn**, é um dos maiores desafios enfrentados por empresas do setor de telecomunicações. Este relatório tem como objetivo identificar padrões comportamentais que influenciam a decisão dos clientes de cancelarem os serviços da **TelecomX_BR**, utilizando técnicas de análise exploratória de dados para apoiar ações estratégicas de retenção.

---

### 2. Limpeza e Tratamento de Dados

Durante a etapa de preparação, foram realizados os seguintes procedimentos:

- **Importação do dataset original** com informações brutas dos clientes.
- **Remoção da coluna “ID do Cliente”**, por não agregar valor analítico.
- **Tradução dos valores categóricos do inglês para o português**, mantendo consistência na linguagem.
- **Conversão de tipos de dados**:
  - Colunas categóricas transformadas em `category`
  - Colunas financeiras convertidas para `float64`
- **Padronização de valores binários**, como “Sim”/“Não”, em `1`/`0`
- **Criação da variável derivada `Contas_Diarias`**, representando o custo médio diário do cliente.

---

### 3. Análise Exploratória de Dados

Foram geradas visualizações e estatísticas descritivas com o objetivo de compreender o comportamento da base de clientes.

#### 🔍 Distribuição do Cancelamento

- Gráficos indicaram que aproximadamente **26,5% dos clientes cancelaram os serviços**, enquanto 73,5% permaneceram.

#### 📊 Cancelamento por Variáveis Categóricas

- **Tipo de contrato**: Clientes com plano "Mês a mês" apresentaram alta taxa de churn.
- **Método de pagamento**: Cancelamentos foram mais frequentes entre clientes que utilizam **boleto eletrônico**.
- **Gênero e dependentes**: Não houve diferença significativa entre homens e mulheres, porém, clientes com **dependentes** tendem a permanecer mais tempo.

#### 📈 Cancelamento por Variáveis Numéricas

- **Cobrança total**: Clientes que cancelam frequentemente possuem **faturamento total baixo**, indicando abandono precoce do serviço.
- **Tempo de permanência**: Canceladores estão concentrados entre os **primeiros 10 meses de contrato**.
- **Contas diárias**: Quanto maior o gasto diário, maior a chance de evasão (especialmente acima de R$ 3,00/dia).

---

### 4. Conclusões e Insights

- **Planos mensais** e **métodos de pagamento eletrônicos** estão fortemente associados à evasão.
- Clientes que abandonam o serviço costumam gerar **receita baixa**, o que representa **perda precoce do ciclo de valor**.
- **Clientes com perfil familiar** (dependentes ou parceiro) demonstram menor risco de churn.

---

### 5. Recomendações

1. **Criar incentivos para contratos anuais**, como descontos graduais.
2. **Focar campanhas de retenção nos primeiros meses de vida do cliente**, com acompanhamento proativo.
3. **Oferecer benefícios para clientes que utilizam boletos eletrônicos migrarem para débito automático.**
4. **Segmentar clientes por gasto diário** e adotar ações específicas para aqueles com alta sensibilidade ao preço.
5. **Investir em melhorias de serviço para clientes com menor tempo de casa**, que são mais propensos a sair.
