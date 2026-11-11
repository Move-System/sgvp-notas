# AGENTS.md

## Fonte oficial de conhecimento (knowledge/) — leia antes de qualquer tarefa

Este repositório consome o Knowledge Workspace da Move System como **submodule em `knowledge/`**.
Pasta vazia? `git submodule update --init`. Docs novas? `git -C knowledge pull origin main`.

O produto ao qual este repo pertence **ainda não consta** em `knowledge/governance/indexes/Mapa_Repos_Produtos.md` — pendente de mapear.
Stack: HTML estático (sem perfil de stack no knowledge).
A ordem de leitura obrigatória está em `knowledge/AGENTS.md`. Atalhos:

- `knowledge/governance/indexes/Mapa_Repos_Produtos.md` — o mapa dos repositórios
- `knowledge/engineering/stacks/README.md` — perfis de stack disponíveis (não aplique padrão de outra stack)
- `knowledge/governance/knowledge-architecture/Dicionario_Siglas.md` — siglas (ADR, PRD, spec…)

### Regras anti-alucinação (Claude Code, Codex, Cursor — qualquer agente)

1. **Não invente** regra de negócio, contrato de API, endpoint, campo ou nome de entidade: verifique no `knowledge/` e no código antes de afirmar.
2. Não encontrou nem na doc nem no código? **Diga "não está documentado" e pergunte** — nunca presuma.
3. Toda decisão relevante **cita o documento que a governou** (ADR, spec, glossário).
4. Conflito entre doc local deste repo e o `knowledge/`? **O `knowledge/` prevalece** — sinalize a divergência em vez de escolher em silêncio.
5. Decisão nova tomada durante a tarefa → **registrar no `knowledge/`** (ADR ou spec), não só no código.

Convenções completas do repositório: ver `CLAUDE.md` (se existir) e o perfil de stack no `knowledge/`.
