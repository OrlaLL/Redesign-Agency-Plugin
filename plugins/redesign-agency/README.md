# Redesign Agency — Plugin POC para Claude Cowork

Plugin experimental para conduzir redesigns de websites por etapas, com entregáveis verificáveis e passagem explícita de contexto entre skills.

## Comandos

Use os comandos slash no Claude Cowork. A sintaxe exata exibida pode incluir o prefixo do plugin:

- `/redesign-agency:auditoria https://site-do-cliente.com.br`
- `/redesign-agency:estrategia [URL ou nome da pasta do projeto]`
- `/redesign-agency:conteudo [URL ou nome da pasta do projeto]`
- `/redesign-agency:prototipo [URL ou nome da pasta do projeto]`
- `/redesign-agency:revisao [URL ou nome da pasta do projeto]`
- `/redesign-agency:refinamento [URL ou nome da pasta do projeto]`
- `/redesign-agency:implementacao [URL ou nome da pasta do projeto]`

O Claude pode exibir os nomes sem o prefixo em algumas superfícies. Use o nome que aparecer no menu de comandos.

## Instalação

1. Descompacte o arquivo ZIP, se necessário.
2. No Claude, abra **Customize → Plugins** (no Cowork, entre primeiro na área Cowork).
3. Escolha a opção para enviar/adicionar um plugin personalizado e selecione o arquivo `.plugin` ou ZIP aceito pela interface.
4. Instale o plugin e abra uma tarefa no Cowork.
5. Digite `/` e confirme se os sete comandos aparecem.

A interface e as opções de importação podem variar conforme a versão do Claude. Este pacote contém o manifesto e as skills; não inclui conectores MCP externos.

## Fluxo recomendado para a POC

1. Execute `auditoria`.
2. Revise o relatório de auditoria e confirme que as páginas relevantes foram inventariadas.
3. Execute `estrategia`.
4. Aprove a arquitetura e os objetivos das páginas.
5. Execute `conteudo`.
6. Revise a matriz de conteúdo e o mapa de CTAs.
7. Execute `prototipo`.
8. Execute `revisao`; se houver bloqueios, corrija antes de avançar.
9. Execute `refinamento`.
10. Execute `implementacao` e revise o relatório de QA.

Não é obrigatório concluir todas as etapas numa única conversa. Os artefatos do projeto são a fonte de verdade entre etapas.

## Estrutura de arquivos esperada no projeto de cada cliente

Por padrão, as skills propõem criar/atualizar uma pasta `redesign-project/` dentro da pasta de trabalho selecionada. Se o usuário indicar outro local, respeite-o.

- `00-project/project-status.md`
- `00-project/decisions-log.md`
- `01-auditoria/audit-report.md`
- `01-auditoria/page-inventory.csv`
- `01-auditoria/evidence-register.csv`
- `01-auditoria/asset-inventory.csv`
- `02-estrategia/strategic-brief.md`
- `02-estrategia/sitemap-proposed.md`
- `02-estrategia/homepage-architecture.md`
- `03-conteudo/content-matrix.csv`
- `03-conteudo/cta-map.csv`
- `03-conteudo/copy-home.md`
- `04-prototipo/art-direction.md`
- `04-prototipo/prototype-spec.md`
- `05-revisao/prototype-review.md`
- `06-refinamento/refinement-log.md`
- `07-implementacao/qa-report.md`

Os nomes são uma convenção recomendada. Se já houver estrutura equivalente, reutilize-a em vez de duplicar documentos.

## Limites e segurança operacional

- Não invente informações do cliente, métricas, depoimentos, credenciais, preços, avaliações ou promessas.
- Não declare que uma página, URL, ferramenta, integração ou teste foi verificado se não foi efetivamente verificado.
- Se o navegador, o Figma, Playwright, arquivos de referência ou acesso ao site não estiverem disponíveis, declare a limitação e produza apenas o trabalho possível.
- Não execute ações destrutivas, publique um site, altere DNS ou envie conteúdo a produção sem autorização explícita.
- Não copie dados pessoais desnecessários de avaliações. Se usar citações públicas, mantenha-as fiéis e registre a fonte.
- O protótipo é um artefato de avaliação, não a aprovação automática da implementação final.

## Sobre esta POC

Esta primeira versão prioriza processo e qualidade das decisões. Ela não configura por si só Playwright, Figma MCP, Git, analytics ou crawler. Essas integrações devem ser adicionadas após validar o fluxo em um ou dois sites reais.
