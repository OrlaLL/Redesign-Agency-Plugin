---
name: prototipo
description: Cria um protótipo navegável para avaliar a direção visual e a experiência antes da implementação final. Comando /prototipo.
argument-hint: [URL ou pasta do projeto]
---

# Prototipação de website

Siga `project-governance` (veracidade, CTAs, leitura econômica, economia de capturas, status de verificação).

## Objetivo

Transformar estratégia, conteúdo e direção de arte aprovada em um protótipo navegável que represente decisões reais do projeto, não um template genérico com o conteúdo antigo.

## Pré-requisitos

`project-status.md`; `art-direction.md` completo (é o contrato visual) e `design-tokens.css`, se existir; `homepage-architecture.md`; `sitemap-proposed.md`; `copy-home.md` e `copy-inner-pages.md`; `cta-map.csv`. Os demais artefatos só pelo resumo. A direção precisa estar aprovada no log. Se estiver ausente, não aprovada ou vaga demais, interrompa e recomende `/redesign-agency:direcao-de-arte`; um wireframe estrutural exploratório só se for útil e solicitado.

## Processo

### 1. Aplicar a direção aprovada
Não crie direção nova nem edite `art-direction.md`. Use o `## Checklist visual` dele como guia de construção; registre conflitos em `prototype-spec.md`. Divergência relevante exige registro de motivo, impacto e alternativa, e aprovação.

### 2. Planejar a experiência
Antes de codificar: composição do hero; ordem e ritmo das seções com variação intencional; hierarquia dos serviços; prova social só se real; imagens com propósito; navegação entre páginas; estados de hover, foco, erro e sucesso; comportamento mobile. Número de colunas segue a natureza do conteúdo; carrossel ou animação só com motivo funcional.

### 3. Construir
Padrão: HTML/CSS/JS autocontido e navegável, salvo indicação de Figma ou outra ferramenta (com Figma MCP disponível; não declare uso se não houve).
- Prototipe as páginas internas críticas do sitemap ou documente quais ficaram fora do escopo.
- Navegação leva à página/âncora correspondente; CTAs seguem `cta-map.csv`.
- Use ativos do cliente quando apropriado; registre placeholders e ativos ausentes.
- Foco em composição e hierarquia; não precisa estar otimizado para produção.

### 4. Verificação mínima
Com navegador: links e CTAs pelo DOM; capturas em 375 e 1440 px para hierarquia, overflow e imagens quebradas. Sem navegador: validação estática, declarando que a inspeção visual não foi feita.

## Artefatos

`04-prototipo/prototype/` (arquivos do protótipo) e `04-prototipo/prototype-spec.md` (resumo para próximas etapas; mapa seção do protótipo → arquitetura aprovada; origem de cada ativo importante; conflitos com a direção).

## Gate

Pronto para revisão quando estrutura, hierarquia, ativos, destinos de navegação e principais comportamentos podem ser avaliados. "Arquivo HTML criado" não é "protótipo validado". Recomende `/redesign-agency:revisao` e declare se a inspeção foi renderizada ou apenas estática.
