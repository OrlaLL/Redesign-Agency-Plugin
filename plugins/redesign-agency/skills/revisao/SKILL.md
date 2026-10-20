---
name: revisao
description: Faz revisão crítica do protótipo contra auditoria, estratégia, conteúdo e critérios de aceitação; identifica falhas e recomendações priorizadas. Comando /revisao.
argument-hint: [URL ou pasta do projeto]
---

# Revisão crítica do protótipo

Siga `project-governance` (veracidade, CTAs, leitura econômica, economia de capturas, status de verificação).

## Objetivo

Atuar como diretor de arte, revisor de UX e responsável por qualidade, não como autor defendendo o próprio design. Encontrar desvios antes da implementação.

## Pré-requisitos

`project-status.md`; `acceptance-criteria.md`; `## Checklist visual` de `art-direction.md`; `prototype-spec.md`; arquivos do protótipo; matriz de rastreabilidade de `strategic-brief.md`; `cta-map.csv`. Demais artefatos pelo resumo, abrindo seções só para verificar um achado. Registre artefatos ausentes como limitação.

## Processo

### 1. Rastreabilidade
Para cada P0/P1 da auditoria e cada decisão estratégica: resolvido, parcial, não resolvido ou não aplicável (com justificativa).

### 2. Estrutura e conteúdo
Arquitetura corresponde ao sitemap? Serviços acessíveis? Conteúdo original preservado ou com destino documentado? Páginas internas têm função própria? Títulos explicam a proposta de valor? Há texto genérico, repetido, sem evidência ou pendência apresentada como fato?

### 3. CTAs e navegação (via DOM, sem capturas)
Cada CTA confere com `cta-map.csv` e com a intenção da seção? Links internos funcionam? Menu e rodapé são úteis? O usuário consegue explorar antes de contatar? Houve concentração indevida em WhatsApp?

### 4. Direção visual
Avalie o protótipo renderizado contra cada item do `## Checklist visual` (AD-xx): conformidade, desvio, evidência/localização e correção. Justifique pelo briefing e pela função do conteúdo, não por gosto pessoal. Capturas em 375, 768 e 1440 px.

### 5. Requisitos técnicos observáveis
Âncoras, recursos ausentes, overflow, semântica e acessibilidade aparente, mobile, estados interativos, erros de console (se disponível).

### 6. Priorização
**Bloqueador** (impede avaliação ou navegação, ou contradiz fatos críticos), **P1** (quebra requisito estratégico ou compromete UX/conversão), **P2** (problema visual, editorial ou funcional relevante), **P3** (acabamento). Cada item: ID, evidência/localização, impacto, correção sugerida e critério de resolução.

## Artefato

`05-revisao/prototype-review.md`:
0. Resumo para próximas etapas.
1. Status: aprovado, aprovado com ressalvas ou reprovado.
2. Cobertura e limitações.
3. Rastreabilidade auditoria → estratégia → protótipo.
4. Resultado do checklist visual (AD-xx).
5. Achados priorizados.
6. Pontos fortes a preservar.
7. Questões que exigem decisão do usuário.

Não aprove com bloqueadores ou violações factuais. Não reescreva o briefing. Recomende `/redesign-agency:refinamento` se houver correções; se aprovado, explique por que o refinamento pode ser leve.
