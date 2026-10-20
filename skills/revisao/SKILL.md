---
name: revisao
description: Faz revisão crítica do protótipo contra auditoria, estratégia, conteúdo e critérios de aceitação; identifica falhas e recomendações priorizadas. Comando /revisao.
argument-hint: [URL ou pasta do projeto]
---

# Revisão crítica do protótipo

## Objetivo

Atuar como diretor de arte, UX reviewer e responsável por qualidade, não como autor que tenta justificar o próprio design. Encontrar desvios e problemas antes da implementação final.

## Pré-requisitos

Leia:
- relatório de auditoria;
- briefing estratégico;
- sitemap e arquitetura da home;
- matriz de conteúdo e mapa de CTAs;
- direção de arte;
- especificação e arquivos do protótipo;
- critérios de aceitação.

Se um desses artefatos não existir, registre a limitação.

## Processo de revisão

### 1. Conferir rastreabilidade
Para cada problema prioritário da auditoria, verifique se foi:
- resolvido;
- parcialmente resolvido;
- não resolvido;
- considerado não aplicável, com justificativa.

Para cada decisão estratégica, verifique se o protótipo a representa.

### 2. Revisar estrutura e conteúdo
- A arquitetura corresponde ao sitemap aprovado?
- Os serviços importantes continuam acessíveis?
- Conteúdo relevante das páginas originais foi preservado ou teve seu destino documentado?
- As páginas internas têm função própria ou tudo virou uma seção da home?
- Os títulos explicam a proposta de valor?
- A hierarquia da informação atende às perguntas do público?
- Há texto repetido, genérico, excessivo ou sem evidência?
- Há conteúdo pendente apresentado como fato?

### 3. Revisar CTAs e navegação
- Cada CTA corresponde à intenção da seção?
- Os links levam a destinos coerentes?
- Serviços apontam para páginas de serviço quando esse é o fluxo aprovado?
- O menu e o rodapé são úteis?
- Os links internos funcionam?
- Todos os CTAs foram indevidamente apontados para WhatsApp?
- O usuário consegue explorar antes de entrar em contato?

### 4. Revisar direção visual
Observe a página renderizada quando possível:
- clareza do hero;
- hierarquia tipográfica;
- equilíbrio entre texto e imagem;
- consistência do grid;
- quantidade e largura das colunas;
- ritmo e diferenciação das seções;
- alinhamento, espaçamento e densidade;
- qualidade, pertinência e proporção das imagens;
- contraste e legibilidade;
- responsividade;
- estados de interação;
- coerência com a personalidade da marca;
- padrões genéricos ou repetitivos que não agregam valor.

Não exija uma preferência estética pessoal. Justifique as observações com o briefing e a função do conteúdo.

### 5. Revisar requisitos técnicos observáveis
- links e âncoras;
- imagens e recursos ausentes;
- overflow;
- semântica e acessibilidade aparente;
- comportamento mobile;
- estados interativos;
- problemas que possam ser observados no navegador/console, se disponíveis.

Não declare resultados de Lighthouse, axe ou testes automatizados se não foram executados.

### 6. Priorizar defeitos
Classifique:
- **Bloqueador:** impede avaliação, navegação ou contradiz fatos críticos.
- **P1:** quebra um requisito estratégico ou compromete fortemente UX/conversão.
- **P2:** problema visual, editorial ou funcional relevante.
- **P3:** acabamento e melhoria opcional.

Para cada item, inclua evidência/localização, impacto, correção sugerida e critério para considerar resolvido.

## Artefato

Crie `05-revisao/prototype-review.md` com:
1. Resumo e status: aprovado, aprovado com ressalvas ou reprovado.
2. Cobertura da revisão e limitações.
3. Matriz de rastreabilidade auditoria → estratégia → protótipo.
4. Achados priorizados.
5. Pontos fortes a preservar.
6. Lista objetiva de correções.
7. Questões que exigem decisão do usuário.

Não aprove o protótipo se houver defeitos bloqueadores ou violações factuais. Não reescreva silenciosamente o briefing.

Finalize recomendando `/redesign-agency:refinamento` se houver correções; se aprovado, explique por que o refinamento pode ser leve.
