---
name: project-governance
description: Regras transversais para projetos de redesign de websites. Use quando uma tarefa envolver auditoria, estratégia, conteúdo, prototipação, revisão, refinamento ou implementação de um site existente.
---

# Governança do projeto de redesign

## Objetivo

Conduzir o redesign como um processo baseado em evidências e decisões documentadas, não como uma troca superficial de cores e fontes. O objetivo é melhorar a experiência, a clareza, a arquitetura e a conversão preservando os fatos e a identidade legítima do negócio.

## Fonte de verdade

1. Leia os artefatos já existentes no projeto antes de começar.
2. Preserve decisões aprovadas e registre mudanças no `00-project/decisions-log.md`.
3. Não trate a conversa como única memória do projeto: atualize os arquivos de estado.
4. Nunca sobrescreva silenciosamente um artefato aprovado. Registre a mudança e seu motivo.
5. Se faltarem artefatos obrigatórios, identifique a lacuna. Não finja que uma etapa anterior foi executada.

## Hierarquia de decisão

1. Veracidade, privacidade e integridade da marca.
2. Funcionamento, acessibilidade e segurança.
3. Requisitos explícitos e decisões aprovadas.
4. Adequação ao público e à jornada do usuário.
5. SEO, clareza de conteúdo e conversão.
6. Preferências estéticas e microdetalhes.

Se duas instruções entrarem em conflito, siga a prioridade mais alta e registre a decisão.

## Proibição de invenções

Não invente fatos, credenciais, clientes, resultados, avaliações, números, preços, prazos de resposta, certificações, endereços, políticas, serviços ou funcionalidades. Separe:
- **Verificado:** sustentado por fonte identificável.
- **Inferência:** interpretação plausível, identificada como hipótese.
- **Pendente:** precisa de confirmação.
- **Proposta:** sugestão de estratégia, não uma alegação factual.

Não publique inferências ou pendências como fatos.

## Transformação substancial

Não copie automaticamente a arquitetura original. Para cada página ou seção importante, decida e registre se deve ser:
- manter;
- reescrever;
- mover;
- combinar;
- dividir;
- remover, com justificativa;
- criar, indicando a oportunidade e a evidência que a sustenta.

Uma seção nova deve resolver uma necessidade real do usuário ou do negócio. Não adicione seções apenas para preencher um template.

## Integridade do conteúdo e navegação

- Inventarie todas as páginas internas relevantes, não apenas a home.
- Preserve o destino de conteúdos importantes ou registre sua migração.
- Cada CTA deve ter intenção, rótulo, origem, destino e comportamento definidos.
- Não direcione todos os links para WhatsApp por conveniência.
- Use WhatsApp somente quando fizer sentido para a intenção e quando o contato real estiver verificado.
- Links de serviços, navegação, redes sociais, formulários, telefone, e-mail e agendamento devem manter destinos apropriados.
- Nunca invente URLs, IDs de formulário ou destinos funcionais.

## Uso de ferramentas

Use navegador ou ferramentas de inspeção se estiverem disponíveis. Para testes visuais, prefira observar a página renderizada, não apenas inferir aparência lendo HTML. O Figma é opcional. Playwright e Lighthouse são opcionais, mas, se não estiverem disponíveis, não declare que seus testes foram executados.

Diferencie sempre:
- testado e aprovado;
- testado e reprovado;
- não testado;
- impossível de verificar com os recursos atuais.

## Critérios de passagem entre etapas

- Auditoria → estratégia: inventário de páginas, evidências e problemas prioritários disponíveis.
- Estratégia → conteúdo: posicionamento, sitemap, arquitetura da home e objetivos das páginas definidos.
- Conteúdo → protótipo: conteúdo por seção e mapa de CTAs disponíveis; pendências identificadas.
- Protótipo → revisão: protótipo acessível e artefatos da estratégia/conteúdo consultáveis.
- Revisão → refinamento: defeitos e recomendações priorizados.
- Refinamento → implementação: design refinado e pendências de conteúdo/funcionalidade documentadas.
- Implementação → entrega: QA executado na extensão possível, limitações relatadas e arquivos finais identificados.

Se um gate falhar, não declare a etapa aprovada. Produza o trabalho possível, registre os bloqueios e indique a ação necessária.

## Relatório ao final de cada comando

Sempre termine com:
1. Arquivos criados ou atualizados.
2. Decisões principais.
3. Questões pendentes e suposições.
4. Verificações realmente executadas.
5. Próximo comando recomendado.
