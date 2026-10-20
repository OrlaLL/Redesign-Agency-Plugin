---
name: estrategia
description: Converte a auditoria em estratégia de redesign, posicionamento, sitemap, jornada, arquitetura da home e requisitos de SEO. Comando /estrategia.
argument-hint: [URL ou pasta do projeto]
---

# Estratégia e arquitetura de website

## Objetivo

Decidir o que o novo website precisa comunicar, quais páginas deve ter e qual função cada seção desempenha. Não comece pelo visual nem copie a arquitetura original por inércia.

## Pré-requisitos

Leia `audit-report.md`, `page-inventory.csv` e `evidence-register.csv`. Se não existirem, peça ao usuário para executar `/redesign-agency:auditoria` ou faça uma auditoria limitada explicitamente identificada. Não trate informações ausentes como fatos.

## Processo

### 1. Sintetizar o diagnóstico
- Selecione os problemas P0/P1 e as oportunidades com evidência.
- Identifique o que funciona e deve ser preservado.
- Relacione cada oportunidade a uma decisão estratégica proposta.
- Não confunda preferências estéticas com problemas de negócio.

### 2. Definir público e posicionamento
Documente:
- segmentos de público plausíveis e suas intenções;
- tarefas, dúvidas e barreiras de decisão;
- proposta de valor e diferenciais sustentados por evidência;
- tom de voz e personalidade da marca;
- informações pendentes que exigem validação do cliente.

Se não houver pesquisa de usuários, identifique as conclusões como hipóteses a validar. Não invente pesquisas, estatísticas ou insights de entrevistas.

### 3. Definir objetivos e jornadas
- Defina o objetivo primário e os objetivos secundários do site.
- Mapeie as jornadas mais importantes, desde a entrada até a ação.
- Determine qual CTA faz sentido em cada contexto.
- Diferencie intenção de conhecer, comparar, consultar, agendar, comprar, ligar ou enviar uma mensagem.
- Não determine que todos os caminhos terminem no WhatsApp.

### 4. Propor sitemap
Compare arquitetura atual e proposta. Para cada URL, decida manter, renomear, consolidar, dividir, remover ou criar. Justifique a decisão com base no público, conteúdo, intenção de busca e negócio.

Considere:
- preservação de conteúdo valioso;
- necessidade de páginas específicas para serviços;
- profundidade de navegação;
- links internos;
- URLs e redirecionamentos, se aplicáveis;
- prevenção de páginas redundantes.

Não crie páginas apenas para aumentar o número de páginas.

### 5. Definir a arquitetura da home
Para cada seção, especifique:
- ordem;
- objetivo do usuário;
- pergunta que responde;
- conteúdo necessário;
- evidência ou fonte necessária;
- CTA e destino, se houver;
- razão para incluir a seção;
- critério de sucesso;
- relação com páginas internas.

A home deve resumir e orientar, não substituir automaticamente todas as páginas de serviços.

### 6. Definir requisitos de SEO
- Intenção de busca provável por página.
- Palavra-chave/tópico principal como hipótese, quando não houver pesquisa de palavras-chave.
- Title, meta description e hierarquia semântica planejados.
- Links internos e relação entre páginas.
- Necessidade de conteúdo exclusivo por serviço.
- Redirecionamentos a avaliar se URLs forem alteradas.
Não alegue volume, dificuldade ou posição de palavras-chave sem ferramenta/dados.

### 7. Registrar critérios de aceitação
Defina condições observáveis para avaliar o redesign, incluindo:
- cobertura do conteúdo relevante;
- arquitetura e navegação;
- clareza dos serviços;
- coerência dos CTAs;
- requisitos responsivos;
- SEO básico;
- fidelidade factual;
- requisitos específicos do cliente.

## Artefatos

Crie/atualize:
- `02-estrategia/strategic-brief.md`
- `02-estrategia/sitemap-proposed.md`
- `02-estrategia/homepage-architecture.md`
- `00-project/acceptance-criteria.md`
- `00-project/decisions-log.md`

Inclua uma matriz de rastreabilidade: achado da auditoria → decisão estratégica → mudança proposta → critério de aceitação.

## Gate

A etapa só está pronta para conteúdo quando:
- a arquitetura da home está definida;
- as páginas existentes têm destino decidido ou pendência documentada;
- objetivos e públicos estão descritos;
- requisitos de SEO estão registrados;
- decisões sem evidência estão marcadas como hipóteses.

Finalize recomendando `/redesign-agency:conteudo`.
