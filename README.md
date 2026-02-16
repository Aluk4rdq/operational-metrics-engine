# Operational Metrics Engine (Google Sheets + Apps Script)

A plug-and-play Google Sheets + Apps Script template that turns a raw dataset into a team-ready operational board with:

- Persistent **HISTORY** by unique record ID  
- A protected **TEAM_BOARD** with editable fields, validations, and conditional formatting  
- Optional **monthly snapshot** to freeze “previous period” metrics  
- A simple **DASHBOARD** and execution **LOGS**  

This template is designed for operational teams that need a lightweight workflow without a full BI stack.

## Typical use cases
- Sales / SDR operations (leads)
- Customer Support (tickets)
- Customer Success (portfolio)
- Collections (accounts)
- Backoffice operations (tasks/orders)

## How it works (pipeline)
1) Paste/import your data into **INPUT_DATA**  
2) Configure mappings and rules in **CONFIG**  
3) Run **Operational Engine → Daily Update**  
4) The team works on **TEAM_BOARD** (edits sync back to **HISTORY**)  
5) Optional: run **Monthly Snapshot** to freeze previous-period metrics

## Sheets included
- `ABOUT` — quick instructions + author/license
- `CONFIG` — mappings and rules
- `INPUT_DATA` — raw input dataset
- `HISTORY` — persistent operational state
- `TEAM_BOARD` — team-facing board (editable + protected)
- `DASHBOARD` — basic KPI view (expandable)
- `LOGS` — execution audit trail

## Configuration (the core of customization)
Edit the **CONFIG** sheet:

**Column mappings**
- `MAP_ID` — unique identifier column name (e.g., `CNPJ`, `lead_id`, `ticket_id`)
- `MAP_OWNER` — owner/assignee column name
- `MAP_SUBJECT` — subject/name column
- `MAP_CREATED_AT` — created date column
- `MAP_PRIORITY` — priority/score column (0–4 recommended)

**Operational behavior**
- `EDITABLE_FIELDS` — fields the team can edit (semicolon-separated)
- `STATUS_OPTIONS` — allowed values for STATUS (semicolon-separated)
- `PROTECT_NON_EDITABLE` — `YES/NO`
- `DAILY_OVERWRITE_OWNER` — `YES/NO`

**Essentials**
- `ESSENTIAL_COLUMNS` — extra columns to include (semicolon-separated)
- `ESSENTIAL_BY_HEADER_COLOR` — `YES/NO` (detect “important” columns by header color)
- `ESSENTIAL_COLOR_HEX`, `COLOR_TOLERANCE`

## License
This project is dual-licensed:
- **AGPL-3.0** for open-source use (see `LICENSE`)
- **Commercial license** for proprietary/closed-source distribution (see `COMMERCIAL_LICENSE.md`)

## Author
Eduardo Sousa

---

# Motor de Métricas Operacionais (Google Sheets + Apps Script)

Um template “plug-and-play” em Google Sheets + Apps Script que transforma uma base crua em um board operacional pronto para time, com:

- **HISTORY** persistente por ID único  
- **TEAM_BOARD** com campos editáveis, validações, travas e formatação condicional  
- **Snapshot mensal (opcional)** para congelar métricas do “período anterior”  
- **DASHBOARD** simples e **LOGS** de execução  

Ideal para equipes operacionais que precisam de fluxo leve, sem depender de uma stack completa de BI.

## Casos de uso comuns
- Operação Comercial / SDR (leads)
- Suporte (tickets)
- Customer Success (carteira)
- Cobrança (contas)
- Operações / Backoffice (tarefas/ordens)

## Como funciona (pipeline)
1) Cole/importe os dados em **INPUT_DATA**  
2) Configure mapeamentos e regras em **CONFIG**  
3) Rode **Operational Engine → Daily Update**  
4) O time opera em **TEAM_BOARD** (as edições sincronizam para **HISTORY**)  
5) Opcional: rode **Monthly Snapshot** para congelar métricas do período anterior

## Abas incluídas
- `ABOUT` — instruções rápidas + autor/licença
- `CONFIG` — mapeamentos e regras
- `INPUT_DATA` — base crua
- `HISTORY` — estado persistente operacional
- `TEAM_BOARD` — frente do time (editável + travada)
- `DASHBOARD` — visão básica de indicadores (expandível)
- `LOGS` — auditoria de execuções

## Configuração (coração da personalização)
Edite a aba **CONFIG**:

**Mapeamento de colunas**
- `MAP_ID` — coluna do ID único (ex.: `CNPJ`, `lead_id`, `ticket_id`)
- `MAP_OWNER` — responsável/dono
- `MAP_SUBJECT` — nome/assunto
- `MAP_CREATED_AT` — data de criação
- `MAP_PRIORITY` — prioridade/score (recomendado 0–4)

**Comportamento operacional**
- `EDITABLE_FIELDS` — campos editáveis (separados por `;`)
- `STATUS_OPTIONS` — valores do STATUS (separados por `;`)
- `PROTECT_NON_EDITABLE` — `YES/NO`
- `DAILY_OVERWRITE_OWNER` — `YES/NO`

**Essenciais**
- `ESSENTIAL_COLUMNS` — colunas extras no board (separadas por `;`)
- `ESSENTIAL_BY_HEADER_COLOR` — `YES/NO` (detectar colunas importantes pela cor do header)
- `ESSENTIAL_COLOR_HEX`, `COLOR_TOLERANCE`

## Licença
Licença dupla:
- **AGPL-3.0** para uso open-source (ver `LICENSE`)
- **Licença comercial** para distribuição proprietária/fechada (ver `COMMERCIAL_LICENSE.md`)

## Autor
Eduardo Sousa
