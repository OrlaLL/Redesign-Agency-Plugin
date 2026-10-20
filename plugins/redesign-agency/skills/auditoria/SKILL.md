---
name: auditoria
description: Audita um website existente por completo antes do redesign: páginas, conteúdo, público, UX, visual, SEO, tecnologia e oportunidades. Comando /auditoria.
argument-hint: <URL do site> [pasta do projeto]
---

# Auditoria de website existente

## Objetivo

Construir uma visão confiável do site atual e do negócio antes de propor soluções. Não redesenhe a página durante esta etapa. Diagnostique, documente evidências e priorize oportunidades.

## Entrada

Aceite URL, domínio, nome da empresa e/ou pasta de projeto. Se a URL estiver ausente e for essencial, faça uma pergunta direta. Se já houver projeto, leia os documentos antes de começar.

## Processo obrigatório

### 1. Confirmar acesso e escopo
- Tente abrir o site no navegador disponível.
- Registre a data da auditoria, URLs acessíveis, bloqueios de acesso e limites de coleta.
- Não afirme que analisou páginas que não conseguiu abrir.
- Se o usuário fornecer várias URLs, inclua todas no escopo.

### 2. Inventariar o site inteiro
- Explore navegação global, menus, rodapé, links internos e páginas de serviços.
- Recolha URLs internas relevantes; não limite a auditoria à home.
- Se houver sitemap XML, robots.txt ou links de navegação acessíveis, use-os como fontes auxiliares.
- Registre páginas encontradas, páginas esperadas mas inacessíveis e páginas possivelmente duplicadas.
- Não faça crawling agressivo nem contorne autenticação ou bloqueios.

### 3. Examinar cada página
Para cada URL relevante, registre:
- objetivo provável da página;
- público e intenção atendidos;
- seções e conteúdo principal;
- CTA principal e CTAs secundários;
- destino real dos links que puder verificar;
- elementos de confiança e prova;
- ativos visuais relevantes;
- problemas de hierarquia, legibilidade, navegação e mobile;
- oportunidades de SEO e links internos;
- conteúdo importante a preservar, atualizar, mover ou questionar.

### 4. Analisar a marca e o público
- Identifique sinais verificáveis de posicionamento, tom de voz, nível de formalidade, diferenciais e estilo visual.
- Separe evidências do site de hipóteses sobre o público.
- Não apresente personas especulativas como pesquisa real. Use hipóteses de público e marque-as como tais.
- Se a informação for insuficiente, registre perguntas de descoberta.

### 5. Avaliar dimensões de qualidade
Avalie com justificativas e evidências:
- estratégia e clareza da proposta de valor;
- arquitetura da informação e navegação;
- conteúdo e copywriting;
- UX, acessibilidade observável e responsividade;
- design visual e consistência;
- SEO on-page e arquitetura de links;
- desempenho/tecnologia apenas na medida em que puder ser observado ou medido;
- conversão e coerência dos CTAs;
- confiança, credenciais e prova social.

Não invente pontuações métricas. Uma nota qualitativa pode ser usada se cada nota vier acompanhada de critério, evidência e nível de confiança. Diferencie problemas observados de itens não testados.

### 6. Inventariar ativos
Registre logos, fotos, ilustrações, vídeos, ícones e outros ativos relevantes. Para cada um, informe URL/local, contexto, relevância, qualidade aparente, uso recomendado e limitações. Não baixe ou reutilize material fora das permissões disponíveis.

### 7. Priorizar oportunidades
Classifique cada achado:
- P0: bloqueio crítico de funcionamento, confiança ou acesso;
- P1: impacto alto na compreensão, navegação, conteúdo ou conversão;
- P2: melhoria importante de experiência, SEO ou consistência;
- P3: refinamento cosmético.

A prioridade deve ser justificada; não use pontuação de impacto fictícia.

## Artefatos

Crie/atualize:
- `00-project/project-status.md`
- `01-auditoria/audit-report.md`
- `01-auditoria/page-inventory.csv`
- `01-auditoria/evidence-register.csv`
- `01-auditoria/asset-inventory.csv`

O relatório deve conter:
1. Resumo executivo.
2. Escopo e limitações.
3. Inventário de URLs.
4. Diagnóstico por página.
5. Pontos fortes que devem ser preservados.
6. Problemas priorizados com evidências.
7. Hipóteses de público e perguntas abertas.
8. Recomendações de oportunidade.
9. Lista de informações que não devem ser inventadas e que precisam de confirmação.

### Colunas mínimas dos CSVs

`page-inventory.csv`: `url_original,page_title,page_type,primary_goal,main_cta,cta_destination,content_to_preserve,observed_issues,review_status,notes`

`evidence-register.csv`: `id,claim_or_finding,source_url,source_type,observed_at,evidence_or_excerpt,confidence,status,notes`

`asset-inventory.csv`: `asset_id,asset_type,source_url,location_on_page,description,relevance,quality_assessment,recommended_use,rights_or_access_notes`

Use CSV válido, com campos entre aspas quando necessário. Não inclua vírgulas que quebrem colunas.

## Gate de conclusão

Não finalize como “auditoria completa” se a home foi a única página analisada e o site possui páginas internas relevantes. Se não foi possível mapear o site inteiro, chame o resultado de auditoria parcial, liste as URLs verificadas e explique o que falta.

Conclua indicando `/redesign-agency:estrategia` como próximo passo quando o inventário e as evidências forem suficientes.
