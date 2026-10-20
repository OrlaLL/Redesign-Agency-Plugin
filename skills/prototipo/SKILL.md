---
name: prototipo
description: Cria um protótipo navegável para avaliar a direção visual e a experiência antes da implementação final. Comando /prototipo.
argument-hint: [URL ou pasta do projeto]
---

# Prototipação de website — Modelo C

## Objetivo

Transformar estratégia e conteúdo em um protótipo visual navegável para revisão. O protótipo deve representar decisões reais do projeto, não ser um template genérico com o conteúdo antigo.

## Pré-requisitos

Leia estratégia, sitemap, arquitetura da home, conteúdo e mapa de CTAs. Se faltar material, liste as lacunas. Não preencha informações comerciais com invenções.

## Processo

### 1. Preparar direção de arte
Crie `04-prototipo/art-direction.md` com:
- personalidade visual e razões;
- relação com a marca original;
- público e contexto de decisão;
- referências visuais (se fornecidas ou pesquisadas, registre origem);
- paleta proposta e contraste;
- tipografia;
- grid, escala de espaçamento e largura de conteúdo;
- tratamento de imagens;
- comportamento responsivo;
- componentes e estados de interação;
- elementos que diferenciam a página de um template genérico.

Não force uma estética fixa (por exemplo, serifas elegantes e neutros quentes) em todas as marcas. O design deve responder ao briefing.

### 2. Desenhar a experiência
Antes de codificar, planeje:
- composição do hero;
- ordem e ritmo das seções;
- variação intencional entre blocos;
- hierarquia dos serviços;
- prova social apenas se real;
- uso de imagens com propósito;
- navegação entre páginas;
- estados de hover, foco, erro e sucesso quando aplicáveis;
- comportamento mobile.

A quantidade de colunas deve corresponder à natureza do conteúdo. Não use uma grade só porque cabe. Não inclua carrossel ou animação sem motivo funcional.

### 3. Construir o protótipo
Preferência da POC: HTML/CSS/JS autocontido e navegável, salvo se o usuário indicar Figma ou outra ferramenta. Se houver Figma MCP e permissões adequadas, ele pode ser usado para criar/editar frames e componentes. Não declare que o Figma foi utilizado se não foi.

- Crie uma página que possa ser aberta e inspecionada.
- Se o sitemap inclui páginas internas, não reduza tudo a uma home com botões para contato. Prototipe as páginas críticas ou documente claramente quais ficaram fora do escopo.
- Links de navegação devem levar à página/âncora correspondente quando disponível.
- CTAs devem respeitar `cta-map.csv`.
- Use ativos do cliente quando disponíveis e apropriados; registre placeholders e ativos ausentes.
- Não invente depoimentos, logos de clientes ou fotos que pareçam representar pessoas reais do negócio.
- O protótipo deve permitir avaliar composição e hierarquia, não precisa ainda ser otimizado para produção.

### 4. Entregáveis
Crie/atualize:
- `04-prototipo/art-direction.md`
- `04-prototipo/prototype-spec.md`
- arquivos do protótipo dentro de `04-prototipo/prototype/`

O `prototype-spec.md` deve mapear cada seção do protótipo para a arquitetura aprovada e identificar a origem de cada ativo importante.

### 5. Verificação mínima
Se houver navegador:
- abra o protótipo;
- capture ou inspecione desktop e mobile;
- teste navegação e CTAs principais;
- observe overflow, imagens quebradas e hierarquia visual.

Se não houver navegador, valide o código estático na medida possível e declare que a inspeção visual não foi executada.

## Gate

O protótipo está pronto para revisão quando é possível avaliar a estrutura, a hierarquia, os ativos, os destinos de navegação e os principais comportamentos. Não confunda “arquivo HTML criado” com “protótipo validado”.

Finalize recomendando `/redesign-agency:revisao`.
