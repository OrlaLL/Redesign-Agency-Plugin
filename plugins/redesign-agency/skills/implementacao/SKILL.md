---
name: implementacao
description: Prepara a implementação final do website a partir do protótipo refinado, preserva os destinos dos CTAs e executa QA proporcional às ferramentas disponíveis. Comando /implementacao.
argument-hint: [URL ou pasta do projeto]
---

# Implementação e QA final

Siga `project-governance` (veracidade, CTAs, leitura econômica, economia de capturas, status de verificação).

## Objetivo

Transformar o protótipo refinado em entrega funcional e rastreável, sem reinterpretar a direção de arte sem registro e justificativa.

## Pré-requisitos

`project-status.md`; `acceptance-criteria.md`; `art-direction.md` (contrato visual) e `design-tokens.css`; `refinement-log.md`; protótipo refinado e `prototype-spec.md`; `cta-map.csv`; `sitemap-proposed.md`. Sem protótipo refinado, informe o bloqueio e não apresente implementação improvisada como versão aprovada.

## Processo

### 1. Escopo técnico
Siga o stack aprovado. Para HTML autocontido: CSS no documento e JavaScript mínimo, sem bibliotecas desnecessárias. Sem dependências, serviços externos ou formulários que enviem dados sem necessidade e autorização.

### 2. Implementar com fidelidade
- Reproduza hierarquia, grid, tipografia, espaçamentos, imagens, estados e ritmo aprovados; não troque a direção por componentes padrão de framework.
- Mantenha as páginas internas do sitemap; navegação e CTAs conforme `cta-map.csv`.
- Preserve metadados e semântica planejados; foco por teclado; `alt` útil; `prefers-reduced-motion`.
- Otimize imagens e defina dimensões para evitar layout shift.

### 3. QA
Execute só o que houver ferramenta para executar; registre resultado e evidência com o status padrão.
- **Estrutura e conteúdo (via arquivo/DOM):** arquivos e rotas; conteúdo × `content-matrix.csv`; title, meta description e headings; ausência de placeholders.
- **Links e ações (via DOM):** destinos de links e CTAs; WhatsApp só se o número estiver confirmado; navegação, formulários e interações sem enviar dados reais.
- **Responsividade (capturas):** 375, 768 e 1440 px; outras larguras (360, 1024, 1280) só para investigar defeito. Overflow, texto cortado, imagens deformadas, menu mobile.
- **Fidelidade visual:** cada item AD-xx do checklist contra a implementação renderizada; divergências com severidade e motivo.
- **Qualidade:** imagens quebradas, console, Lighthouse/axe se disponíveis, contraste e teclado na medida possível.

Sem navegador, informe que a revisão foi estática e que a responsividade real não foi confirmada. Editor visual ou comparador só se fizerem parte do escopo e houver o necessário para funcionarem.

## Artefato

`07-implementacao/qa-report.md`: artefatos finais e caminhos; resumo das alterações; testes e resultados; diferenças entre protótipo e implementação; pendências; limitações do ambiente; recomendação de aprovação ou bloqueio.

## Critério de conclusão

Aprovada só com os critérios obrigatórios verificados. Com limitações, classifique como entrega parcial e liste o que falta.
