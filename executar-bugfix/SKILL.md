---
name: executar-bugfix
description: Corrige os bugs documentados em uma funcionalidade, cria testes de regressão e registra as correções. Use quando o usuário pedir para executar um bugfix ou corrigir bugs descritos em tasks/prd-*/bugs.md.
---

# Executar Bugfix

Corrija todos os bugs documentados para a funcionalidade solicitada, preservando os requisitos do PRD, as decisões da TechSpec e as regras do repositório.

## Arquivos da funcionalidade

Localize os arquivos em `tasks/prd-[nome-da-funcionalidade]/`:

- `bugs.md`: bugs a corrigir.
- `prd.md` e `techspec.md`: requisitos e decisões técnicas.
- `tasks.md`: tarefas relacionadas, quando existir.
- `qa.md` e `evidences/`: contexto e evidências, quando existirem.
- `bugfixes.md`: relatório final das correções.

## Fluxo

1. Leia `bugs.md` por completo e identifique todos os bugs. Leia o PRD, a TechSpec, as tarefas relacionadas, as evidências disponíveis e as instruções do projeto.
2. Para cada bug, rastreie o fluxo afetado e determine a causa raiz antes de alterar o código.
3. Corrija o comportamento e crie um teste de regressão que reproduza o cenário original e falhe se a correção for removida. Inclua casos de limite relevantes.
4. Execute as verificações adequadas ao projeto, incluindo testes existentes e verificação de tipos. Relate claramente qualquer verificação que não pôde ser executada ou que falhou.
5. Para bugs visuais ou de frontend, valide o fluxo na aplicação com a ferramenta de navegador disponível e registre evidências. Se a automação de navegador não estiver disponível, informe essa limitação e faça as verificações restantes.
6. Atualize cada bug em `bugs.md` com:

   - **Status:** Corrigido
   - **Correção aplicada:** resumo breve
   - **Testes de regressão:** testes criados

7. Crie ou atualize `bugfixes.md` com o resumo, totais, estado por bug e resultados reais dos testes, tipagem e validação visual. Não declare verificações como aprovadas sem executá-las.

## Relatório

Use uma tabela por bug com ID, severidade, status, correção e testes criados. Inclua totais de bugs documentados, corrigidos e testes de regressão criados, além dos resultados e limitações das verificações.
