---
name: project-governance
description: Regras transversais do fluxo redesign-agency (auditoria → estratégia → direção de arte → conteúdo → protótipo → revisão → refinamento → implementação). Use junto com qualquer comando /redesign-agency ou ao trabalhar numa pasta de projeto com 00-project/ e 01-auditoria/.
---

# Governança do projeto de redesign

Fonte única das regras gerais. As skills de etapa não repetem estas regras; elas as pressupõem.

## Objetivo

Conduzir o redesign com base em evidências e decisões documentadas, não como troca superficial de cores e fontes: melhorar experiência, clareza, arquitetura e conversão preservando os fatos e a identidade legítima do negócio.

## Fonte de verdade e estado

1. Os arquivos do projeto são a memória; a conversa não é. Atualize os arquivos de estado ao final de cada etapa.
2. Preserve decisões aprovadas e registre mudanças em `00-project/decisions-log.md`. Nunca sobrescreva silenciosamente um artefato aprovado.
3. Se faltar um artefato obrigatório, identifique a lacuna. Não finja que uma etapa anterior foi executada.

## Leitura econômica de artefatos

- Comece sempre por `00-project/project-status.md`: ele resume etapa atual, decisões vigentes, pendências e o caminho de cada artefato.
- Todo artefato `.md` principal começa com `## Resumo para próximas etapas` (até ~15 itens: decisões, restrições, pendências). Leia o resumo; abra o documento completo apenas na seção que a tarefa exige.
- Em CSVs, filtre linhas e colunas relevantes (grep, csvcut, pandas) em vez de carregar o arquivo inteiro no contexto.
- Não releia um arquivo já lido nesta sessão, a menos que tenha sido alterado.

## Templates

Crie artefatos a partir de `${CLAUDE_PLUGIN_ROOT}/templates/` (pasta `templates/` na raiz do plugin), copiando o arquivo em vez de redigir a estrutura do zero:
`project-status`, `decisions-log`, `acceptance-criteria` (.md) e `page-inventory`, `evidence-register`, `asset-inventory`, `content-matrix`, `cta-map` (.csv). As colunas dos templates são o mínimo obrigatório. Use CSV válido, com aspas quando necessário.

## Hierarquia de decisão

1. Veracidade, privacidade e integridade da marca.
2. Funcionamento, acessibilidade e segurança.
3. Requisitos explícitos e decisões aprovadas.
4. Adequação ao público e à jornada do usuário.
5. SEO, clareza de conteúdo e conversão.
6. Preferências estéticas e microdetalhes.

Em conflito, siga a prioridade mais alta e registre a decisão.

## Proibição de invenções

Não invente fatos, credenciais, clientes, resultados, avaliações, depoimentos, números, estatísticas, preços, prazos, certificações, endereços, políticas, serviços, funcionalidades, URLs, IDs de formulário, contatos, fotos de pessoas reais, pesquisas ou volumes de palavra-chave. Classifique cada informação como:
- **Verificado:** sustentado por fonte identificável (registre em `evidence-register.csv`).
- **Inferência:** hipótese identificada como tal.
- **Pendente:** precisa de confirmação; use `[CONFIRMAR: ...]` fora da copy publicável.
- **Proposta:** sugestão estratégica, não alegação factual.

Não publique inferências ou pendências como fatos. Não copie dados pessoais desnecessários de avaliações.

## Transformação substancial

Não copie a arquitetura original por inércia. Para cada página ou seção importante, decida e registre: manter, reescrever, mover, combinar, dividir, remover (com justificativa) ou criar (com evidência). Não adicione seções só para preencher template.

## CTAs e navegação

- Inventarie todas as páginas internas relevantes, não apenas a home; preserve ou documente a migração de conteúdos importantes.
- Cada CTA tem ID, intenção, rótulo, origem, destino e comportamento definidos em `cta-map.csv`.
- WhatsApp não é destino universal: use-o só quando fizer sentido para a intenção e o contato estiver verificado. Serviços, navegação, redes sociais, formulários, telefone, e-mail e agendamento mantêm destinos apropriados.
- Destino não verificado fica marcado como pendente; nunca simule um link funcional.

## Ferramentas e verificação

- Navegador, Figma, Playwright, Lighthouse e axe são opcionais. Sem a ferramenta, declare a limitação e não alegue o teste.
- **Economia de capturas:** use texto/DOM da página (get_page_text, read_page, grep no HTML) para links, CTAs, metadados, headings e conteúdo. Reserve capturas de tela para julgamento visual, nas larguras 375, 768 e 1440 px; outras larguras só para investigar um defeito. Ao revalidar, capture apenas as seções alteradas.
- Para avaliar aparência, observe a página renderizada; não infira apenas lendo HTML.
- Status padrão de qualquer verificação: **PASSOU**, **FALHOU**, **NÃO EXECUTADO**, **NÃO APLICÁVEL**. Nunca transforme "não executado" em "passou".
- Não publique, faça deploy, altere DNS ou envie dados reais em formulários sem autorização explícita.

## Direção de arte como gate

A direção de arte é etapa formal entre estratégia e prototipação. O protótipo completo só começa após aprovação explícita (ou delegação explícita da escolha, registrada). Silêncio não é aprovação. `04-prototipo/art-direction.md` contém o checklist visual normativo; protótipo, revisão, refinamento e implementação avaliam contra ele, critério por critério. Divergências relevantes são registradas e submetidas à aprovação.

## Gates entre etapas

- Auditoria → estratégia: inventário de páginas, evidências e problemas priorizados.
- Estratégia → direção de arte: posicionamento, público, objetivos, sitemap, arquitetura da home, SEO e briefing criativo.
- Direção de arte → protótipo: direção aprovada, regras concretas e checklist registrados.
- Conteúdo → protótipo: conteúdo por seção e mapa de CTAs; pendências identificadas.
- Protótipo → revisão: protótipo acessível e artefatos consultáveis.
- Revisão → refinamento: defeitos priorizados.
- Refinamento → implementação: nenhum bloqueador sem justificativa; aderência verificada na medida possível.
- Implementação → entrega: QA executado na extensão possível, limitações relatadas.

Se um gate falhar, não declare a etapa aprovada: produza o possível, registre bloqueios e indique a ação necessária.

## Encerramento de cada comando

1. Atualize `project-status.md` (etapa, decisões, pendências, caminhos) e o `## Resumo para próximas etapas` dos artefatos criados.
2. Responda com: arquivos criados/atualizados; decisões principais; pendências e suposições; verificações realmente executadas; próximo comando recomendado.
