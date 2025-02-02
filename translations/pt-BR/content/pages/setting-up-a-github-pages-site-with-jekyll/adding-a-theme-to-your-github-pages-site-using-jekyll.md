---
title: Adicionar um tema ao site do GitHub Pages usando Jekyll
intro: É possível personalizar o site do Jekyll adicionando e personalizando um tema.
redirect_from:
  - /articles/customizing-css-and-html-in-your-jekyll-theme
  - /articles/adding-a-jekyll-theme-to-your-github-pages-site
  - /articles/adding-a-theme-to-your-github-pages-site-using-jekyll
  - /github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-using-jekyll
  - /pages/getting-started-with-github-pages/adding-a-theme-to-your-github-pages-site-with-the-theme-chooser
product: '{% data reusables.gated-features.pages %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pages
shortTitle: Add theme to Pages site
ms.openlocfilehash: 33969695e96aa0629b2811e2742ca3093e58139a
ms.sourcegitcommit: 47bd0e48c7dba1dde49baff60bc1eddc91ab10c5
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/05/2022
ms.locfileid: '147644792'
---
Pessoas com permissões de gravação para um repositório podem adicionar um tema a um site do {% data variables.product.prodname_pages %} usando Jekyll.

{% data reusables.pages.test-locally %}

## Adicionar um tema

{% data reusables.pages.navigate-site-repo %} {% data reusables.pages.navigate-publishing-source %}
2. Procure *_config.yml*.
{% data reusables.repositories.edit-file %}
4. Adicione uma nova linha ao arquivo para o nome do tema.
   - Para usar um tema com suporte, digite `theme: THEME-NAME`, substituindo _THEME-NAME_ pelo nome do tema, conforme mostrado no LEIAME do repositório do tema. Para ver a lista de temas com suporte, confira "[Temas com suporte](https://pages.github.com/themes/)" no site do {% data variables.product.prodname_pages %}.
   ![Tema com suporte no arquivo de configuração](/assets/images/help/pages/add-theme-to-config-file.png)
   - Para usar qualquer outro tema do Jekyll hospedado no {% data variables.product.prodname_dotcom %}, digite `remote_theme: THEME-NAME`, substituindo THEME-NAME pelo nome do tema, conforme mostrado no LEIAME do repositório do tema.
   ![Tema sem suporte no arquivo de configuração](/assets/images/help/pages/add-remote-theme-to-config-file.png) {% data reusables.files.write_commit_message %} {% data reusables.files.choose-commit-email %} {% data reusables.files.choose_commit_branch %} {% data reusables.files.propose_file_change %}

## Personalizar o CSS do tema

{% data reusables.pages.best-with-supported-themes %}

{% data reusables.pages.theme-customization-help %}

{% data reusables.pages.navigate-site-repo %} {% data reusables.pages.navigate-publishing-source %}
1. Crie um arquivo chamado _/assets/css/style.scss_.
2. Adicione o seguinte conteúdo ao topo do arquivo:
  ```scss
  ---
  ---

  @import "{% raw %}{{ site.theme }}{% endraw %}";
  ```
3. Adicione qualquer CSS ou Sass personalizado que desejar (incluindo as importações) imediatamente após a linha `@import`.

## Personalizar o layout HTML do tema

{% data reusables.pages.best-with-supported-themes %}

{% data reusables.pages.theme-customization-help %}

1. No {% data variables.product.prodname_dotcom %}, navegue até o repositório de origem do tema. Por exemplo, o repositório de origem do Minima é https://github.com/jekyll/minima.
2. Na pasta *_layouts*, procure o arquivo _default.html_ do tema.
3. Copie o conteúdo do arquivo.
{% data reusables.pages.navigate-site-repo %} {% data reusables.pages.navigate-publishing-source %}
6. Crie um arquivo chamado *_layouts/default.html*.
7. Cole o conteúdo do layout padrão que você copiou anteriormente.
8. Personalize o layout como desejado.

## Leitura adicional

- "[Como criar arquivos](/articles/creating-new-files)"
