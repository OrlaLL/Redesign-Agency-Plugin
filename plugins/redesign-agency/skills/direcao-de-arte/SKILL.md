---
name: direcao-de-arte
description: Define e submete à aprovação o conceito criativo, a linguagem visual e o design system antes da prototipação. Comando /direcao-de-arte.
argument-hint: [URL ou pasta do projeto]
---

# Direção de arte e design system

Siga `project-governance` (veracidade, leitura econômica, gate de aprovação).

## Objetivo

Converter a estratégia em uma direção visual específica, justificável e verificável, que reflita posicionamento, público, categoria, ativos reais e objetivos. A meta não é tornar todo site "premium" ou minimalista, nem imitar uma referência.

## Pré-requisitos

`project-status.md`; resumos de `audit-report.md` e `strategic-brief.md` e a seção de briefing criativo completa; `asset-inventory.csv` filtrado; sitemap; arquitetura da home; critérios de aceitação. Se faltar estratégia, liste o que falta e marque a exploração como provisória.

## Processo

### 1. Traduzir estratégia em requisitos visuais
Percepção desejada e por quê; personalidade em 3–5 atributos; atributos a evitar; contextos de decisão do público; diferenciais verificados que merecem expressão visual; restrições de identidade, acessibilidade, conteúdo e ativos; tensão entre diferenciação, clareza, confiança e usabilidade. Converta adjetivos ("moderno", "elegante", "acolhedor") em decisões observáveis.

### 2. Explorar 2–3 direções distintas
Diferenças reais de composição, tipografia, cor, fotografia e personalidade, não variações de paleta. Por rota: conceito; posicionamento comunicado; paleta preliminar; tipografia; composição e ritmo; fotografia; componentes; referências verificáveis; benefícios; riscos; aderência à estratégia e aos ativos. Sem navegação ou moodboard, descreva com clareza e declare a limitação.

### 3. Recomendar e aguardar aprovação
Recomende uma rota justificada. Peça para aprovar, escolher com alterações ou pedir novas opções. **Não finalize a direção nem inicie o protótipo sem aprovação explícita.** Se a escolha for delegada explicitamente, escolha a mais sustentada e registre a delegação. Registre a decisão no log.

### 4. Especificar a direção aprovada
`04-prototipo/art-direction.md`, começando pelo resumo para próximas etapas: conceito e decisão; personalidade; princípios inegociáveis; paleta HEX com função semântica; tipografia, hierarquia e pesos; grid, largura, espaçamento, ritmo, densidade e hero; fotografia (proporções, origem/licença, lacunas); componentes e estados; movimento e `prefers-reduced-motion`; regras responsivas; padrões a evitar; referências (o que aprender e o que não copiar); pendências. Tokens CSS quando útil.

### 5. Checklist visual normativo (fonte única)
Ao final de `art-direction.md`, inclua `## Checklist visual` com IDs (AD-01, AD-02…), cada critério observável e ligado a estratégia, público ou requisito de UX. Cubra no mínimo: hero com hierarquia e composição intencional; consistência de tipografia, cores, espaçamento e componentes; ritmo variado sem repetição mecânica de cards; imagens pertinentes, bem recortadas e proporcionais; páginas internas coerentes e com hierarquia própria; contraste, legibilidade, foco e responsividade; estados de interação; movimento com propósito; originalidade sem cópia de referências; nenhuma prova visual inventada. Protótipo, revisão, refinamento e implementação usam este checklist; não o duplique em outros arquivos.

## Artefatos

Antes da aprovação: `04-prototipo/creative-directions.md`, status e log. Após: `04-prototipo/art-direction.md`, `04-prototipo/design-tokens.css` (se aplicável) e referência ao checklist em `00-project/acceptance-criteria.md`.

## Gate

Concluída só com direção aprovada (ou delegada), regras específicas, origens e limitações de referências e ativos registradas, checklist criado e decisão documentada. Depois, recomende `/redesign-agency:conteudo` se o conteúdo não estiver pronto; senão, `/redesign-agency:prototipo`.
