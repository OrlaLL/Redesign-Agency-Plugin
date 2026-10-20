---
name: estrategia
description: Converte a auditoria em estratégia de redesign, posicionamento, sitemap, jornada, arquitetura da home e requisitos de SEO. Comando /estrategia.
argument-hint: [URL ou pasta do projeto]
---

# Estratégia e arquitetura de website

Siga `project-governance` (veracidade, CTAs, leitura econômica, templates, status de verificação).

## Objetivo

Decidir o que o novo site precisa comunicar, quais páginas terá e qual função cada seção cumpre, e entregar um briefing criativo útil à direção de arte, sem escolher detalhes visuais.

## Pré-requisitos

`project-status.md`; resumo e seção de problemas priorizados de `audit-report.md`; `page-inventory.csv` e `evidence-register.csv` filtrados conforme a necessidade. Sem auditoria, peça `/redesign-agency:auditoria` ou faça uma auditoria limitada, explicitamente identificada.

## Processo

### 1. Sintetizar o diagnóstico
Selecione P0/P1 e oportunidades com evidência; identifique o que preservar; ligue cada oportunidade a uma decisão proposta. Não confunda preferência estética com problema de negócio.

### 2. Público e posicionamento
Segmentos e intenções; tarefas, dúvidas e barreiras de decisão; proposta de valor e diferenciais com evidência; tom de voz; pendências a validar com o cliente. Sem pesquisa de usuários, conclusões são hipóteses.

### 3. Objetivos e jornadas
Objetivo primário e secundários; jornadas principais da entrada à ação; CTA adequado a cada contexto (conhecer, comparar, consultar, agendar, comprar, ligar, mensagem).

### 4. Sitemap
Compare atual e proposto. Para cada URL: manter, renomear, consolidar, dividir, remover ou criar, com justificativa (público, conteúdo, intenção de busca, negócio). Considere conteúdo valioso, páginas por serviço, profundidade, links internos, redirecionamentos e redundância.

### 5. Arquitetura da home
Por seção: ordem; objetivo do usuário; pergunta respondida; conteúdo e evidência necessários; CTA e destino; razão de existir; critério de sucesso; relação com páginas internas. A home resume e orienta; não substitui as páginas de serviço.

### 6. Requisitos de SEO
Por página: intenção de busca; tópico principal (hipótese, sem dados de ferramenta); title, meta description e headings planejados; links internos; necessidade de conteúdo exclusivo; redirecionamentos a avaliar.

### 7. Briefing criativo
Em `strategic-brief.md`: atributos e percepção desejada; diferenciais comprovados; atributos visuais a evitar e por quê; expectativas do público quanto a confiança, clareza e personalidade; restrições e liberdade sobre a identidade atual; requisitos de acessibilidade, fotografia e ativos; referências do cliente (inspiração, não ordem de cópia).

### 8. Critérios de aceitação
Parta do template e acrescente condições observáveis: cobertura de conteúdo, navegação, clareza dos serviços, coerência dos CTAs, responsividade, SEO básico, fidelidade factual e requisitos do cliente.

## Artefatos

`02-estrategia/strategic-brief.md` (com resumo para próximas etapas e matriz de rastreabilidade achado → decisão → mudança → critério), `02-estrategia/sitemap-proposed.md`, `02-estrategia/homepage-architecture.md`, `00-project/acceptance-criteria.md`, `00-project/decisions-log.md`.

## Gate

Pronta quando: arquitetura da home definida; cada página existente com destino decidido ou pendência documentada; objetivos e públicos descritos; SEO registrado; decisões sem evidência marcadas como hipóteses. Recomende `/redesign-agency:direcao-de-arte` antes de `/redesign-agency:conteudo` (o conteúdo pode ser rascunhado em paralelo; o protótipo depende da direção aprovada).
