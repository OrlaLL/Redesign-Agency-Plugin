---
name: refinamento
description: Executa o refinamento visual e de interação do protótipo com base na revisão; corrige defeitos em vez de apenas listá-los. Comando /refinamento.
argument-hint: [URL ou pasta do projeto]
---

# Refinamento visual e de interação

## Objetivo

Aplicar melhorias concretas ao protótipo com base na revisão aprovada. Não se limite a produzir recomendações; implemente as correções possíveis e registre o que foi alterado.

## Pré-requisitos

Leia `prototype-review.md`, `art-direction.md`, `prototype-spec.md`, os arquivos do protótipo e os documentos de estratégia/conteúdo. Respeite as decisões aprovadas. Se uma correção exigir mudança estratégica, peça decisão ou registre-a como proposta, sem alterar silenciosamente o escopo.

## Processo

### 1. Transformar revisão em tarefas
Crie uma lista com ID, prioridade, arquivo/seção afetada, problema, correção, critério de aceite e status. Resolva primeiro bloqueadores e P1.

### 2. Refinar o design com intenção
Exemplos de problemas a procurar e corrigir:
- depoimentos sem contexto visual suficiente ou sem avatar/ilustração apropriada; não invente fotos de usuários nem apresente avatar ilustrativo como pessoa real;
- números ou estatísticas que perdem hierarquia;
- grids com número de colunas inadequado ao tipo e volume do conteúdo;
- cards repetitivos que não ajudam a comparar;
- imagens genéricas, mal recortadas ou com proporção incorreta;
- seções sem ritmo visual ou que parecem pertencer a outro site;
- tipografia, espaçamento e alinhamento inconsistentes;
- contraste insuficiente;
- estados de hover/foco ausentes;
- animações que não explicam nem melhoram a experiência;
- transições no scroll excessivas, pesadas ou inacessíveis;
- botões sem destino claro;
- responsividade quebrada.

Não adicione efeitos de scroll apenas por decoração. Prefira movimento discreto, respeite `prefers-reduced-motion` e garanta que o conteúdo continue acessível sem animação.

### 3. Refinar imagens e ativos
- Priorize ativos reais do cliente e imagens licenciadas/autorizadas.
- Se for necessária imagem nova, registre a necessidade, finalidade, estilo, dimensões e fonte planejada.
- Não invente provas sociais, fotografias de equipe, instalações ou clientes.
- Evite placeholders no resultado que será apresentado como final.
- Verifique proporção, crop, resolução e contexto.

### 4. Validar após alterações
Se navegador disponível:
- inspecione desktop e mobile;
- verifique as correções contra os critérios de aceite;
- confirme que navegação/CTAs não regrediram;
- faça nova captura para comparação, se possível.

Não afirme que o resultado está visualmente validado sem inspeção visual.

## Artefatos

- Atualize os arquivos do protótipo.
- Crie/atualize `06-refinamento/refinement-log.md`.
- Atualize `04-prototipo/prototype-spec.md` se houver mudanças.
- Registre correções não executadas e por quê.

## Gate

Nenhum bloqueador deve permanecer sem justificativa explícita. Se houver alterações estruturais ou de copy, compare com a estratégia e registre a aprovação necessária.

Finalize recomendando `/redesign-agency:implementacao`.
