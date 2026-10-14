---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um workflow do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para disponibilizá-lo publicamente. O Copilot pode preparar o workflow e orientar a publicação, mas você continua responsável por revisar as mudanças e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar uma publicação no GitHub Pages.
- revisar o workflow e o pull request antes de fazer o merge.
- acompanhar a publicação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma forma simples de experimentá-lo. Publicar o site de um único arquivo com o GitHub Pages o disponibiliza em uma URL pública sem adicionar um servidor nem uma dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um workflow do GitHub Actions que compile o site, se necessário, e o publique no GitHub Pages. Adicione um README que descreva o aplicativo e como executá-lo localmente, caso ainda não exista. Crie um pull request com essas mudanças e faça o merge depois que as verificações obrigatórias forem aprovadas. Acompanhe a publicação até ela ser concluída com sucesso e, então, informe a URL final do site ativo. Se você não tiver permissão para habilitar o Pages ou fazer o merge, diga exatamente o que preciso aprovar ou fazer; não informe que houve sucesso antes de o site estar no ar.
```

![Diagrama em três etapas: pull request de space-quiz mesclado; execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e faça o merge de um pull request e altere as configurações do Pages no repositório. Antes de continuar, revise o diff, as permissões de publicação e todos os pedidos de aprovação do GitHub.

## Revise o workflow e verifique a publicação

1. Confirme que o README foi adicionado somente se o repositório ainda não tinha um.
2. Revise as mudanças do pull request, incluindo as etapas de compilação e publicação do workflow.
3. Faça o merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de publicação do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou fazer o merge do pull request, siga as instruções específicas fornecidas. Não considere a tarefa concluída até que a publicação tenha sucesso e o site esteja no ar.

## Resumo e próximas etapas

Agora o Space Quiz está disponível em um site publicado, e você verificou a implantação em vez de confiar no relato do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
