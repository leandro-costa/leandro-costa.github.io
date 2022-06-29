---
title: "GitHub Pages"
tags: [GitHub, GitHub Pages]
date: 2022-06-28
---

para criar o nosso site vamos seguir o passo a passo de [^githubpages]

# Com HTML
1. Criar um repositório
   
    Vá até o GitHub e crie um novo repositório público chamado **username.github.io**, onde username é seu nome de usuário (ou nome da organização) no GitHub.

    *Se a primeira parte do repositório não corresponder exatamente ao seu nome de usuário, não funcionará, portanto, certifique-se de acertar.*

    ![](https://pages.github.com/images/user-repo@2x.png)

2. Criar um arquivo de index.html

    Vá no repositório criado e clique no botão **Criar novo arquivo** 

    ![](https://pages.github.com/images/new-create-file@2x.png)

3. Nomeie o arquivo index.html e digite algum conteúdo HTML no editor.

    ![](https://pages.github.com/images/new-index-html@2x.png)

4. Confirme o arquivo

    Role até o final da página, escreva uma mensagem de confirmação e confirme o novo arquivo.

    ![](https://pages.github.com/images/new-commit-file@2x.png)

5. Configurações do repositório

    Clique na guia Configurações e role para baixo até a seção GitHub Pages.
    
    Em seguida, selecione a origem do branch principal e clique no botão **Salvar**.

    ![](https://pages.github.com/images/source-setting@2x.png)

6. Pronto!

    Abra um navegador e vá para **http://username.github.io/**    


ver [leandro-costa.github.io HTML](https://github.com/leandro-costa/leandro-costa.github.io/tree/gh-pages-p)
# Com Markdown

para criar o nosso site vamos seguir o passo a passo de [^githubpagesquickstart]


1. Criando seu site
   
   repete o passo 1 de [Com HTML](2022/06/28/github-pages#com-html)

   
1. No página  do seu repositório, clique em  `Configurações`.

    ![](https://docs.github.com/assets/cb-21851/images/help/repository/repo-actions-settings.png)

1. Clique `Pages`.
1. Clique Escolher um tema.

    ![](https://docs.github.com/assets/cb-62385/images/help/pages/choose-theme.png)

1. O seletor de temas será aberto. Pesquise os temas disponíveis e, em seguida, clique em Selecionar tema para selecionar um tema. É fácil mudar seu tema mais tarde. Portanto, se você não tiver certeza, basta escolher um por enquanto.

    ![](https://docs.github.com/assets/cb-180181/images/help/pages/select-theme.png)

1. Depois de selecionar um tema, o arquivo `README.md` do repositório será aberto no editor do arquivo. O arquivo README.md é onde você escreverá o conteúdo do seu site. Você pode editar o arquivo ou manter o conteúdo padrão por enquanto.
   - Esse conteúdo é em [Markdown](/2022/06/29/markdown) 
2. Ao terminar de editar o arquivo, clique em **Aplicar as alterações**.
3. Acesse `username.github.io` para ver seu novo site. 
   - podem ser necessários até 20 minutos para que as alterações no site sejam publicadas após o push delas no GitHub.

## Alterando o título e a descrição

Por padrão, o título do seu site é `username.github.io`. Você pode alterar o título editando o arquivo `_config.yml` no seu repositório. Você também pode adicionar uma descrição para o seu site.

1. Clique na aba Código do seu repositório.
1. Na lista de arquivos, clique em `_config.yml` para abrir o arquivo.
1. Clique em ✏️ para editar o arquivo.
1. O arquivo `_config.yml` já contém uma linha que especifica o tema para o seu site. Adicione uma nova linha com `title:` seguido do título que você deseja. Adicione uma nova linha com `description:` seguida da descrição que você deseja. Por exemplo:

    ```yml
    theme: jekyll-theme-minimal
    title: Octocat's homepage
    description: Bookmark this to keep an eye on my project updates!
    ```

1. Ao terminar de editar o arquivo, clique em **Aplicar as alterações**.

# Referências 

[^githubpages]: GitHub, Inc. GitHub Pages. Websites for you and your projects. [https://pages.github.com/](https://pages.github.com/).(Acessado em 28/06/2022)


[^githubpagesquickstart]: GitHub, Inc. GitHub Pages. Início rápido para o GitHub Pages. [https://docs.github.com/pt/pages/quickstart](https://docs.github.com/pt/pages/quickstart).(Acessado em 28/06/2022)

