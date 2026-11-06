# ☁️ SalesFlow CRM

## 📌 Sobre o projeto

O SalesFlow CRM é um projeto prático desenvolvido na plataforma Salesforce para simular a gestão de clientes e propostas comerciais, com foco em automação de processos, organização de dados e análise comercial.

O projeto faz parte do meu portfólio de estudos e desenvolvimento profissional em Salesforce Administration.

## 🚀 Funcionalidades desenvolvidas

- Cadastro e gerenciamento de clientes.
- Cadastro de propostas comerciais.
- Relacionamento Lookup entre Cliente e Proposta Comercial.
- Automação com Salesforce Flow para criação de tarefa de acompanhamento três dias após o cadastro de uma proposta.
- Relatório de propostas comerciais.
- Dashboard Comercial com três componentes para acompanhamento dos resultados.

## 🛠️ Tecnologias e ferramentas

- Salesforce Platform
- Salesforce Flow Builder
- Salesforce Object Manager
- Salesforce Reports & Dashboards
- Git e GitHub para documentação e versionamento

## 📊 Dashboard Comercial

O dashboard apresenta indicadores de valor total das propostas, quantidade de propostas e distribuição por status.

![Dashboard Comercial do SalesFlow CRM](images/dashboard-comercial.png)

## ⚙️ Automação Salesforce Flow

### Criação automática de tarefa de acompanhamento

Foi desenvolvido um Flow acionado por registro (Record-Triggered Flow) para automatizar o acompanhamento das propostas comerciais.

**Funcionamento:**

1. O usuário cadastra uma nova Proposta Comercial.
2. O Salesforce executa automaticamente o Flow após a criação do registro.
3. O Flow cria uma tarefa com o assunto "Acompanhar proposta comercial".
4. A data de vencimento da tarefa é calculada por meio de uma fórmula, considerando três dias corridos após a execução.

**Configurações técnicas:**

- Tipo: Record-Triggered Flow.
- Objeto de origem: Proposta Comercial.
- Evento: criação de registro.
- Execução: após salvar o registro.
- Elemento: Create Records (Criar tarefa de acompanhamento).
- Objeto de destino: Task (Tarefa).
- Recurso de fórmula: `Data_Vencimento_Tarefa`.
- Fórmula: `TODAY() + 3`.

**Observação:** a tarefa é criada imediatamente, com vencimento previsto para três dias depois. O Flow não aguarda três dias para executar.

### Estrutura da automação

![Fluxo de acompanhamento de propostas comerciais](images/flow-acompanhamento.png)

## 🎯 Objetivo

Demonstrar conhecimentos práticos em modelagem de dados, automação declarativa e análise de informações comerciais utilizando Salesforce.

## 🔜 Próximas melhorias

- Adicionar capturas de tela das funcionalidades.
- Expandir os relatórios e indicadores comerciais.
- Documentar os metadados do Salesforce e versioná-los no GitHub.

## 👩‍💻 Autora

Paula Canalle

Projeto desenvolvido para estudos e portfólio profissional em Salesforce.
