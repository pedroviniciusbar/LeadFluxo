# LeadFluxo — Portal de Documentação para Clientes

## What This Is

O LeadFluxo terá um portal GitBook próprio, em português, para orientar clientes no uso diário da plataforma: atendimento, canais, gestão da equipe, automações, Kanban e integrações aprovadas. O conteúdo parte da documentação Whazing existente, mas será curado, reescrito e publicado em um repositório exclusivo do LeadFluxo, sem páginas operacionais, administrativas ou de infraestrutura.

## Core Value

Cada cliente deve encontrar instruções confiáveis para usar o LeadFluxo sem jamais ter acesso a conteúdo de SaaS, gestão interna do sistema, instalação, atualizações ou infraestrutura.

## Requirements

### Validated

<!-- Shipped and confirmed valuable. -->

(None yet — ship to validate)

### Active

<!-- Current scope. Building toward these. -->

- [ ] Criar uma fonte publicada exclusiva do LeadFluxo que contenha apenas páginas e assets aprovados para clientes.
- [ ] Definir uma matriz de curadoria para classificar cada fonte como publicar, adaptar ou bloquear.
- [ ] Publicar uma navegação orientada ao cliente para canais, atendimento, gestão, automação, Kanban, integrações, ajuda e suporte.
- [ ] Remover ou adaptar toda menção pública a Whazing, domínios e contatos antigos; usar a marca LeadFluxo e o suporte oficial `(31) 9964-5781`.
- [ ] Impedir a publicação de conteúdo SaaS, instalação, VPS, atualizações, servidor, banco de dados e administração interna.
- [ ] Criar verificações automatizadas de escopo, marca, contatos, links e assets antes de uma publicação.
- [ ] Manter um fluxo de atualização do upstream Whazing que gere uma PR revisada antes de qualquer publicação LeadFluxo.
- [ ] Configurar o GitBook para sincronizar somente a fonte documental aprovada do LeadFluxo.

### Out of Scope

- Módulo SaaS, planos, financeiro, afiliados e administração de plataforma — são exclusivos da operação interna e não podem chegar aos clientes.
- Instalação, VPS, Docker, banco de dados, proxy, atualizações, logs e manutenção de servidor — são responsabilidades técnicas internas, não documentação do cliente.
- Publicação automática de alterações do upstream — uma revisão humana é obrigatória para impedir vazamentos e conteúdo incorreto.
- Alterar o produto SaaS ou a infraestrutura do LeadFluxo — este projeto trata somente da documentação e do seu processo de publicação.

## Context

- A fonte atual é um repositório GitBook clássico, com `README.md` e `SUMMARY.md`, originalmente conectado ao Whazing.
- O repositório possui conteúdo útil para clientes em funcionalidades, canais e integrações, mas também inclui páginas SaaS, instalação e suporte de infraestrutura.
- A documentação de origem muda ao longo do tempo; a curadoria deve tornar a incorporação de alterações incrementais e auditáveis.
- Alguns documentos de uso misturam instruções de cliente com passos administrativos ou técnicos. A classificação deve ser feita por página e, quando necessário, por uma versão adaptada da página.
- Screenshots e assets também podem exibir a marca Whazing, portanto a revisão precisa ser visual além de textual.

## Constraints

- **Segurança de conteúdo**: o repositório sincronizado com o GitBook público deve conter somente conteúdo aprovado — esconder links no `SUMMARY.md` não é uma proteção suficiente.
- **Marca**: a documentação publicada deve usar LeadFluxo e o número oficial `(31) 9964-5781`, com link de WhatsApp `https://wa.me/5531999645781` quando aplicável.
- **Atualizações**: alterações do Whazing entram por uma PR de curadoria, nunca por publicação direta.
- **Rastreabilidade**: cada página publicada deve ter origem, status e justificativa na matriz de curadoria.
- **Compatibilidade**: a documentação deve continuar compatível com GitBook Git Sync e Markdown existente.
- **Direitos de uso**: a publicação pressupõe autorização do titular para reutilizar e rebrandear o conteúdo Whazing; isso deve ser confirmado antes da abertura pública.

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Publicar em repositório exclusivo do LeadFluxo | Garante que clientes não recebam arquivos internos por engano. | — Pending |
| Manter o Whazing como upstream de referência | Permite detectar melhorias da fonte sem misturar seu conteúdo ao portal publicado. | — Pending |
| Incorporar atualizações por PR revisada | Protege contra vazamentos de SaaS, infraestrutura, marca antiga e instruções incompatíveis. | — Pending |
| Usar LeadFluxo e `(31) 9964-5781` como identidade de suporte | Padroniza a experiência pública e remove os contatos Whazing. | — Pending |
| Usar allowlist e validações automatizadas | A proibição de conteúdo interno precisa ser verificável, não apenas editorial. | — Pending |

## Evolution

This document evolves at phase transitions and milestone boundaries.

**After each phase transition** (via `$gsd-transition`):
1. Requirements invalidated? → Move to Out of Scope with reason
2. Requirements validated? → Move to Validated with phase reference
3. New requirements emerged? → Add to Active
4. Decisions to log? → Add to Key Decisions
5. "What This Is" still accurate? → Update if drifted

**After each milestone** (via `$gsd-complete-milestone`):
1. Full review of all sections
2. Core Value check — still the right priority?
3. Audit Out of Scope — reasons still valid?
4. Update Context with current state

---
*Last updated: 2026-08-16 after initialization*
