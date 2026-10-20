---
name: conteudo
description: Escreve a copy do novo website com base na auditoria e na arquitetura aprovada; organiza conteúdo por URL, seção e CTA. Comando /conteudo.
argument-hint: [URL ou pasta do projeto]
---

# Conteúdo e copywriting

## Objetivo

Produzir conteúdo realmente adequado à nova arquitetura, não apenas polir frases do site antigo. Reorganize, reescreva, condense ou expanda com intenção, preservando os fatos e registrando lacunas.

## Pré-requisitos

Leia:
- auditoria e inventário de páginas;
- briefing estratégico;
- sitemap proposto;
- arquitetura da home;
- critérios de aceitação;
- registro de evidências.

Se não houver arquitetura aprovada, sinalize o bloqueio antes de escrever uma versão final. É possível produzir um rascunho exploratório, mas rotule-o como provisório.

## Processo

### 1. Criar inventário de conteúdo
Para cada página e seção:
- conteúdo original relevante;
- destino proposto;
- decisão: manter, reescrever, mover, combinar, dividir, remover ou criar;
- justificativa;
- fonte/evidência;
- estado de aprovação.

Não elimine silenciosamente informação importante. Quando remover conteúdo, registre a razão e o destino alternativo, se houver.

### 2. Escrever com propósito
Para cada seção, determine a pergunta do usuário e a resposta principal. Escreva títulos informativos e específicos, parágrafos escaneáveis e listas apenas quando ajudarem a compreensão.

- Não use clichês sem evidência.
- Não invente benefícios, diferenciais, serviços, garantias, credenciais, preços ou resultados.
- Não crie falsa urgência nem promessas de resposta rápida.
- Não transforme inferências em afirmações factuais.
- Evite repetição de palavras-chave e copy genérica intercambiável entre negócios.
- Use o tom de voz definido na estratégia.
- Não faça alegações médicas, financeiras, jurídicas ou de resultados que não estejam sustentadas.

### 3. Criar CTAs contextuais
Para cada CTA, documente:
- ID;
- página/seção;
- rótulo;
- intenção;
- destino;
- comportamento;
- mensagem predefinida, se aplicável;
- origem da URL/contato;
- status de verificação.

Exemplos de destinos possíveis: página de serviço, formulário, agendamento, telefone, e-mail, rede social, WhatsApp ou âncora interna. Escolha de acordo com a intenção. Não use WhatsApp como destino universal.

Não invente número, endereço, URL de agendamento nem link. Se o destino não for verificável, marque como pendente e não simule um link funcional.

### 4. SEO e metadados
Proponha title e meta description específicos para cada página, com nome da empresa, serviço e localidade somente quando verificados e relevantes. Escreva para pessoas; não force termos.

### 5. Gerenciar lacunas
Use marcadores de pendência fora da copy publicável, como `[CONFIRMAR: horário de atendimento]`. Nunca deixe placeholders no artefato apresentado como final.

Quando uma seção depende de informação não encontrada, proponha:
- omitir por enquanto;
- escrever sem a alegação pendente;
- solicitar confirmação do cliente.

## Artefatos

Crie/atualize:
- `03-conteudo/content-matrix.csv`
- `03-conteudo/cta-map.csv`
- `03-conteudo/copy-home.md`
- `03-conteudo/copy-inner-pages.md`
- metadados SEO por página, no mesmo documento ou arquivo dedicado.

Colunas mínimas de `content-matrix.csv`:
`source_url,proposed_url,section,original_content_summary,proposed_content,decision,rationale,evidence_ids,status,open_questions`

Colunas mínimas de `cta-map.csv`:
`cta_id,page_url,section,label,intent,destination_url,destination_type,verified,status,notes`

## Revisão antes de entregar
- Compare a matriz com o inventário original.
- Confirme que todos os serviços relevantes têm destino definido.
- Confirme que cada CTA possui intenção e destino coerentes.
- Verifique se há alegações sem fonte.
- Confirme que as páginas internas não foram reduzidas a CTAs genéricos.
- Diferencie texto final de pendências.

Finalize recomendando `/redesign-agency:prototipo`.
