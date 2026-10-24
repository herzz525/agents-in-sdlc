---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar a solicitação de pull e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que qualquer pessoa possa acessá-lo. O Copilot pode preparar o fluxo de trabalho e orientar a implantação, mas cabe a você revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar a implantação no GitHub Pages.
- revisar o fluxo de trabalho e a solicitação de pull antes de mesclá-la.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma forma simples de experimentá-lo. A publicação do site de arquivo único com o GitHub Pages o disponibiliza em uma URL pública sem adicionar um servidor ou dependência de runtime.

## Peça ao Copilot para implantar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um fluxo de trabalho do GitHub Actions que compile o site, se necessário, e o implante no GitHub Pages. Se ainda não houver um README, adicione um que descreva o aplicativo e como executá-lo localmente. Crie uma solicitação de pull com essas alterações e faça o merge depois que as verificações obrigatórias forem aprovadas. Monitore a implantação até que ela seja concluída com sucesso e, então, informe a URL final do site no ar. Se você não tiver permissão para habilitar o Pages ou fazer o merge, diga exatamente o que preciso aprovar ou fazer; não informe que houve sucesso até que o site esteja no ar.
```

![Diagrama em três etapas: uma solicitação de pull do space-quiz mesclada; uma execução bem-sucedida de Deploy website no GitHub Actions com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz no ar em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e faça o merge de uma solicitação de pull e altere as configurações do Pages no repositório. Revise o diff, as permissões de implantação e todas as solicitações de aprovação do GitHub antes de continuar.

## Revise o fluxo de trabalho e verifique a implantação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as alterações da solicitação de pull, incluindo as etapas de compilação e implantação do fluxo de trabalho.
3. Faça o merge somente depois que as verificações obrigatórias da solicitação de pull forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou fazer o merge da solicitação de pull, siga as instruções específicas fornecidas. Não considere a tarefa concluída até que a implantação seja bem-sucedida e o site no ar carregue.

## Resumo e próximas etapas

Agora o Space Quiz está disponível como um site no ar, e você verificou a implantação em vez de confiar no relato do agente. Continue para a [Lição 13: Revisão e próximas etapas][next-lesson].

[next-lesson]: ../13-review/
