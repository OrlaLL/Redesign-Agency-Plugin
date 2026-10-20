---
name: conteudo
description: Escreve a copy do novo website com base na auditoria e na arquitetura aprovada; organiza conteúdo por URL, seção e CTA. Comando /conteudo.
argument-hint: [URL ou pasta do projeto]
---

# Conteúdo e copywriting

Siga `project-governance` (veracidade, CTAs, leitura econômica, templates, status de verificação).

## Objetivo

Produzir conteúdo adequado à nova arquitetura, não polir frases do site antigo: reorganizar, reescrever, condensar ou expandir com intenção, preservando os fatos e registrando lacunas.

## Pré-requisitos

`project-status.md`; resumos de `strategic-brief.md` (tom de voz completo) e `art-direction.md`, se existir; `sitemap-proposed.md`; `homepage-architecture.md`; `page-inventory.csv` e `evidence-register.csv` filtrados por página. Sem arquitetura aprovada, sinalize o bloqueio; um rascunho é possível, rotulado como provisório.

## Processo

### 1. Inventário de conteúdo
Por página e seção: conteúdo original relevante; destino proposto; decisão (manter, reescrever, mover, combinar, dividir, remover, criar); justificativa; evidência; status. Conteúdo removido tem razão e destino alternativo registrados.

### 2. Escrever com propósito
Para cada seção, defina a pergunta do usuário e a resposta principal. Títulos informativos e específicos, parágrafos escaneáveis, listas só quando ajudam. Use o tom definido na estratégia. Evite clichês, copy intercambiável entre negócios, repetição de palavras-chave, falsa urgência e promessas de resposta rápida. Sem alegações médicas, financeiras, jurídicas ou de resultado não sustentadas.

### 3. CTAs contextuais
Preencha `cta-map.csv` (template) para cada CTA, incluindo mensagem predefinida quando aplicável e origem do contato. Escolha o destino pela intenção: página de serviço, formulário, agendamento, telefone, e-mail, rede social, WhatsApp ou âncora.

### 4. SEO e metadados
Title e meta description específicos por página; nome, serviço e localidade só quando verificados e relevantes. Escreva para pessoas.

### 5. Lacunas
Pendências usam `[CONFIRMAR: ...]` fora da copy publicável; nenhum placeholder no artefato final. Para seções dependentes de informação ausente, proponha omitir por ora, escrever sem a alegação ou pedir confirmação.

### 6. Alinhamento com a direção de arte
Identifique títulos, provas, números, citações e imagens que a composição aprovada exige e confirme se existem. Não force slogans, estatísticas, depoimentos ou textos decorativos para preencher layout.

## Artefatos

A partir dos templates: `03-conteudo/content-matrix.csv` e `03-conteudo/cta-map.csv`. Além deles: `03-conteudo/copy-home.md` e `03-conteudo/copy-inner-pages.md` (cada um com resumo para próximas etapas e metadados SEO por página).

## Checagem antes de entregar
Matriz comparada ao inventário original; todos os serviços com destino; CTAs com intenção e destino coerentes; nenhuma alegação sem fonte; páginas internas não reduzidas a CTAs genéricos; texto final separado de pendências.

## Gate

Recomende `/redesign-agency:prototipo` só se a direção de arte estiver aprovada; caso contrário, `/redesign-agency:direcao-de-arte`.
