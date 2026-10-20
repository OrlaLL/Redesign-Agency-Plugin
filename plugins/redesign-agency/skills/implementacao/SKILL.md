---
name: implementacao
description: Prepara a implementação final do website a partir do protótipo refinado, preserva os destinos dos CTAs e executa QA proporcional às ferramentas disponíveis. Comando /implementacao.
argument-hint: [URL ou pasta do projeto]
---

# Implementação e QA final

## Objetivo

Transformar o protótipo refinado em uma entrega funcional e rastreável. Não reinterprete a direção de arte durante a codificação sem registrar e justificar as mudanças.

## Pré-requisitos

Leia:
- briefing e critérios de aceitação;
- sitemap;
- conteúdo e mapa de CTAs;
- direção de arte;
- revisão e log de refinamento;
- especificação do protótipo.

Se não houver protótipo refinado, informe o bloqueio e não apresente uma implementação improvisada como se fosse a versão aprovada.

## Processo

### 1. Definir escopo técnico
Respeite o requisito definido para o projeto. Se o escopo for HTML autocontido, use CSS no documento e JavaScript mínimo, sem bibliotecas desnecessárias. Se houver outro stack aprovado, siga-o.

Não introduza dependências, serviços externos ou formulários que enviem dados sem necessidade e autorização.

### 2. Implementar com fidelidade
- Reproduza a hierarquia, o grid, a tipografia, os espaçamentos, as imagens e os estados aprovados.
- Mantenha páginas internas que fazem parte do sitemap; não converta tudo em CTAs genéricos.
- Implemente navegação e CTAs conforme `cta-map.csv`.
- Use URLs reais e verificadas; marque destinos pendentes sem simular funcionamento.
- Preserve metadados e semântica planejados.
- Inclua estados de foco por teclado e texto alternativo útil nas imagens.
- Respeite `prefers-reduced-motion`.
- Otimize imagens e evite dimensões que provoquem layout shift quando possível.
- Não publique, faça deploy ou altere sistemas externos sem autorização explícita.

### 3. Testes mínimos
Execute somente testes para os quais exista ferramenta disponível. Registre resultados e evidências.

**Estrutura e conteúdo**
- verificar arquivos e rotas esperados;
- comparar conteúdo com a matriz;
- verificar título, meta description e hierarquia de headings;
- verificar ausência de placeholders.

**Links e ações**
- validar destinos de links e CTAs;
- verificar número/URL do WhatsApp apenas se fornecido e confirmado;
- testar navegação, formulários e interações implementadas;
- não enviar dados reais em formulários de teste.

**Responsividade**
- conferir, quando possível, 360, 375, 768, 1024, 1280 e 1440 px;
- verificar overflow, texto cortado, imagens deformadas e grids inadequados;
- inspecionar estados relevantes de menu mobile.

**Qualidade**
- verificar imagens quebradas;
- observar erros de console se a ferramenta permitir;
- usar Lighthouse/axe se estiverem disponíveis;
- verificar contraste e navegação por teclado na medida possível;
- abrir editor e comparador somente se forem parte do escopo solicitado.

### 4. Relatar honestamente
Para cada teste, use:
- PASSOU;
- FALHOU;
- NÃO EXECUTADO;
- NÃO APLICÁVEL.

Não transforme “não executado” em “passou”. Se não houver navegador, informe que a revisão foi estática e que a responsividade real não foi confirmada.

### 5. Entrega
Produza `07-implementacao/qa-report.md` com:
- artefatos finais e seus caminhos;
- resumo das alterações;
- testes executados e resultados;
- problemas pendentes;
- diferenças entre protótipo e implementação;
- limitações do ambiente;
- recomendação de aprovação ou bloqueio.

Se o projeto exigir editor visual ou comparador, só os crie se as especificações e os arquivos necessários estiverem disponíveis. Não finja que arquivos auxiliares funcionam apenas porque existem.

## Critério de conclusão

A entrega só pode ser marcada como aprovada se os critérios obrigatórios estiverem verificados. Se houver limitações, classifique como entrega parcial e liste o que falta.
