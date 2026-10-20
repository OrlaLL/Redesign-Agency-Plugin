---
name: auditoria
description: Audita um website existente por completo antes do redesign: páginas, conteúdo, público, UX, visual, SEO, tecnologia e oportunidades. Comando /auditoria.
argument-hint: <URL do site> [pasta do projeto]
---

# Auditoria de website existente

Siga `project-governance` (veracidade, CTAs, leitura econômica, templates, status de verificação).

## Objetivo

Construir uma visão confiável do site atual e do negócio antes de propor soluções. Não redesenhe nesta etapa: diagnostique, documente evidências e priorize.

## Entrada

URL, domínio, nome da empresa e/ou pasta de projeto. Se a URL faltar e for essencial, faça uma pergunta direta. Se o projeto já existir, comece por `00-project/project-status.md`.

## Processo

### 1. Acesso e escopo
Abra o site; registre data, URLs acessíveis, bloqueios e limites de coleta. Inclua todas as URLs fornecidas pelo usuário.

### 2. Inventário do site inteiro
- Use navegação global, menus, rodapé, links internos, sitemap XML e robots.txt.
- Registre páginas encontradas, esperadas mas inacessíveis e possivelmente duplicadas.
- Não faça crawling agressivo nem contorne autenticação ou bloqueios.
- Prefira extrair texto/links (WebFetch, get_page_text) a capturas de tela.

### 3. Diagnóstico por página — com amostragem
Todas as páginas entram no inventário. Diagnóstico detalhado: home, uma página representativa por tipo (serviço, sobre, contato, blog…) e qualquer página com problema P0/P1. Páginas do mesmo tipo herdam o diagnóstico; registre apenas suas diferenças.

Para cada página detalhada: objetivo provável; público/intenção; seções e conteúdo principal; CTAs e destinos verificáveis; elementos de confiança; ativos relevantes; problemas de hierarquia, legibilidade, navegação e mobile; oportunidades de SEO e links internos; conteúdo a preservar, atualizar, mover ou questionar.

### 4. Marca e público
Registre sinais verificáveis de posicionamento, tom de voz, diferenciais e estilo visual. Hipóteses de público são marcadas como hipóteses (não como personas de pesquisa). Lacunas viram perguntas de descoberta.

### 5. Dimensões de qualidade
Avalie com evidência: proposta de valor; arquitetura e navegação; copy; UX, acessibilidade observável e responsividade; design visual; SEO on-page; desempenho/tecnologia apenas se observável; conversão e CTAs; confiança e prova social. Nota qualitativa só com critério, evidência e nível de confiança; sem pontuações métricas inventadas.

### 6. Ativos
Para logos, fotos, ilustrações, vídeos e ícones relevantes: URL/local, contexto, relevância, qualidade, uso recomendado, direitos/limitações. Não baixe nem reutilize fora das permissões.

### 7. Priorização (justificada)
- P0: bloqueio crítico de funcionamento, confiança ou acesso.
- P1: impacto alto em compreensão, navegação, conteúdo ou conversão.
- P2: melhoria importante de experiência, SEO ou consistência.
- P3: refinamento cosmético.

## Artefatos

A partir dos templates: `00-project/project-status.md`, `01-auditoria/page-inventory.csv`, `01-auditoria/evidence-register.csv`, `01-auditoria/asset-inventory.csv`. Além deles, `01-auditoria/audit-report.md` com:
0. Resumo para próximas etapas.
1. Resumo executivo.
2. Escopo e limitações.
3. Inventário de URLs (referência ao CSV, sem duplicá-lo).
4. Diagnóstico por página/tipo.
5. Pontos fortes a preservar.
6. Problemas priorizados com evidências.
7. Hipóteses de público e perguntas abertas.
8. Oportunidades.
9. Informações que precisam de confirmação.

## Gate

Se só a home foi analisada e há páginas internas relevantes, chame o resultado de auditoria parcial e liste o que falta. Com inventário e evidências suficientes, recomende `/redesign-agency:estrategia`.
