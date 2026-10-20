---
name: refinamento
description: Executa o refinamento visual e de interação do protótipo com base na revisão; corrige defeitos em vez de apenas listá-los. Comando /refinamento.
argument-hint: [URL ou pasta do projeto]
---

# Refinamento visual e de interação

Siga `project-governance` (veracidade, leitura econômica, economia de capturas, status de verificação).

## Objetivo

Implementar as correções da revisão no protótipo, não apenas recomendá-las, e registrar o que mudou.

## Pré-requisitos

`project-status.md`; `prototype-review.md` completo; `## Checklist visual` de `art-direction.md` (normativo); `prototype-spec.md`; arquivos do protótipo. Estratégia e conteúdo só quando uma correção os afetar. Correção que exija mudança estratégica: peça decisão ou registre como proposta.

## Processo

### 1. Lista de tarefas
Converta os achados em tarefas (ID do achado, prioridade, arquivo/seção, correção, critério de aceite, status). Bloqueadores e P1 primeiro.

### 2. Causas sistêmicas primeiro
Antes de microajustes, verifique se o problema vem de conceito inconsistente, tipografia sem hierarquia, composição repetitiva, imagens sem direção, paleta sem função, componentes iguais em excesso ou páginas internas achatadas. Corrija nos padrões compartilhados (tokens, componentes), não seção por seção. Se a própria direção for insuficiente, proponha revisão formal e peça aprovação antes de mudar o conceito.

### 3. Imagens e ativos
Priorize ativos reais e licenciados. Imagem nova necessária: registre finalidade, estilo, dimensões e fonte planejada. Verifique proporção, crop e resolução. Sem placeholders no resultado apresentado como final.

### 4. Movimento
Sem efeitos de scroll decorativos; movimento discreto, `prefers-reduced-motion` respeitado e conteúdo acessível sem animação.

### 5. Revalidar
Capture apenas as seções alteradas (375 e 1440 px); confira navegação e CTAs pelo DOM para detectar regressões. Atualize o resultado de cada item AD-xx afetado com o status padrão. Código alterado não significa qualidade visual validada.

## Artefatos

Arquivos do protótipo atualizados; `06-refinamento/refinement-log.md` (resumo para próximas etapas, tarefas e status, correções não executadas e por quê, checklist atualizado); `prototype-spec.md` se houver mudanças.

## Gate

Nenhum bloqueador sem justificativa explícita. Alterações estruturais ou de copy são comparadas à estratégia e registradas para aprovação. Recomende `/redesign-agency:implementacao`.
