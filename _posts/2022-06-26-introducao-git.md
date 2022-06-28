---
title: "Introdução ao Git"
tags: [Git]
date: 2022-06-26
---

# Controle de Versão


O controle de versão é a prática de rastrear e gerenciar alterações. Essas alterações podem ser em qualquer arquivo digital.[^atlassian]

Você já salvou diferentes versões de um arquivo? Algo assim:

- trabalho.doc
- trabalho-v2.doc
- trabalho-final.doc
- trabalho-final-final.doc

Os sistemas de controle de versão são ferramentas de software que ajudam a gerenciar as alterações ao longo do tempo.

O controle de versão é um sistema que registra alterações em um arquivo ou conjunto de arquivos ao longo do tempo para que você possa recuperar versões específicas posteriormente.[^git-scm]

Se você é um designer gráfico ou web e deseja manter todas as versões de uma imagem ou layout (o que você certamente deseja), um sistema de controle de versão (VCS) é uma coisa muito sábia de usar. Ele permite reverter arquivos selecionados de volta a um estado anterior, reverter todo o projeto de volta a um estado anterior, comparar alterações ao longo do tempo, ver quem modificou pela última vez algo que pode estar causando um problema, quem introduziu um problema e quando e muito mais. Usar um SCV também geralmente significa que, se você estragar tudo ou perder arquivos, poderá recuperar facilmente. Além disso, você obtém tudo isso por muito pouco trabalho.


## Principais vantagens

As principais vantagens de se utilizar um sistema de controle de versão para rastrear as alterações feitas durante o desenvolvimento de software ou o desenvolvimento de um documento de texto qualquer são:[^wikiscv]

- **Controle do histórico**: facilidade em desfazer e possibilidade de analisar o histórico do desenvolvimento, como também facilidade no resgate de versões mais antigas e estáveis. A maioria das implementações permitem analisar as alterações com detalhes, desde a primeira versão até a última.
- **Trabalho em equipe**: um sistema de controle de versão permite que diversas pessoas trabalhem sobre o mesmo conjunto de documentos ao mesmo tempo e minimiza o desgaste provocado por problemas com conflitos de edições. É possível que a implementação também tenha um controle sofisticado de acesso para cada usuário ou grupo de usuários.
- **Marcação e resgate de versões estáveis**: a maioria dos sistemas permite marcar onde é que o documento estava com uma versão estável, podendo ser facilmente resgatado no futuro.
- **Ramificação de projeto**: a maioria das implementações possibilita a divisão do projeto em várias linhas de desenvolvimento, que podem ser trabalhadas paralelamente, sem que uma interfira na outra.
- **Segurança**: Cada software de controle de versão usa mecanismos para evitar qualquer tipo de invasão de agentes infecciosos nos arquivos. Além do mais, somente usuários com permissão poderão mexer no código.
- **Rastreabilidade**: Com a necessidade de sabermos o local, o estado e a qualidade de um arquivo; o controle de versão traz todos esses requisitos de forma que o usuário possa se embasar do arquivo que deseja utilizar.
- **Organização**: Alguns softwares disponibilizam uma interface visual onde podem ser vistos todos os arquivos controlados, desde a origem até o projeto por completo.
- **Confiança**: O uso de repositórios remotos (na nuvem) ajuda a não perder arquivos por eventos inesperados. Além disso, e possível fazer novos projetos sem danificar o desenvolvimento do atual.

as equipes de software a gerenciar as alterações no código-fonte ao longo do tempo. À medida que os ambientes de desenvolvimento se aceleram, os sistemas de controle de versão ajudam as equipes de software a trabalhar de forma mais rápida e inteligente. Eles são especialmente úteis para equipes de DevOps , pois os ajudam a reduzir o tempo de desenvolvimento e aumentar as implantações bem-sucedidas.

## Tipos de Sistema de Controle de Versão

### Sistemas de Controle de Versão Local

O método de controle de versão preferido de muitas pessoas é copiar arquivos para outro diretório (talvez um diretório com carimbo de data/hora, se forem inteligentes). Essa abordagem é muito comum porque é muito simples, mas também é incrivelmente propensa a erros. É fácil esquecer em qual diretório você está e acidentalmente gravar no arquivo errado ou copiar arquivos indesejados.

![scv local](https://git-scm.com/book/en/v2/images/local.png)[^git-scm]

### Sistemas de Controle de Versão Centralizados

O próximo grande problema que as pessoas encontram é que elas precisam colaborar com desenvolvedores em outros locais. Para lidar com este problema, foram desenvolvidos Sistemas de Controle de Versão Centralizados

![scv centralized](https://git-scm.com/book/en/v2/images/centralized.png)[^git-scm]


### Sistemas Distribuídos de Controle de Versão

É aqui que entram os Sistemas de Controle de Versão Distribuído (SCVD). Em um SCVD (como Git, Mercurial, Bazaar ou Darcs), os clientes não apenas verificam o último instantâneo dos arquivos; em vez disso, eles espelham totalmente o repositório, incluindo seu histórico completo. Assim, se algum servidor morrer e esses sistemas estiverem colaborando por meio desse servidor, qualquer um dos repositórios do cliente poderá ser copiado de volta para o servidor para restaurá-lo. Cada clone é realmente um backup completo de todos os dados.

![scv distributed](https://git-scm.com/book/en/v2/images/distributed.png)[^git-scm]


# Uma Breve História do Git

[^git-scm]

O kernel Linux é um projeto de software de código aberto de escopo bastante grande. Durante os primeiros anos da manutenção do kernel do Linux (1991–2002), as mudanças no software foram passadas como patches e arquivos arquivados. Em 2002, o projeto do kernel Linux começou a usar um SCVD proprietário chamado BitKeeper.

Em 2005, o relacionamento entre a comunidade que desenvolveu o kernel Linux e a empresa comercial que desenvolveu o BitKeeper quebrou, e o status gratuito da ferramenta foi revogado. Isso levou a comunidade de desenvolvimento do Linux (e em particular Linus Torvalds, o criador do Linux) a desenvolver sua própria ferramenta com base em algumas das lições que aprenderam ao usar o BitKeeper. Alguns dos objetivos do novo sistema foram os seguintes:

- Velocidade
- Design simples
- Forte suporte para desenvolvimento não linear (milhares de ramificações paralelas)
- Totalmente distribuído
- Capaz de lidar com grandes projetos como o kernel Linux de forma eficiente (velocidade e tamanho dos dados)

Desde o seu nascimento em 2005, o Git evoluiu e amadureceu para ser fácil de usar e ainda manter essas qualidades iniciais. É incrivelmente rápido, muito eficiente com projetos grandes e possui um sistema de ramificação incrível para desenvolvimento não linear


## Adoção

[^wikigit]

A Eclipse Foundation relatou em sua pesquisa anual da comunidade que, em maio de 2014, o Git é a ferramenta de gerenciamento de código-fonte mais usada, com 42,9% dos desenvolvedores de software profissionais relatando que usam o Git como seu principal sistema de controle de versão comparado com 36,3% em 2013, 32% em 2012.

O Stack Overflow incluiu o controle de versão em sua pesquisa anual de desenvolvedores em 2015 (16.694 respostas), 2017 (30.730 respostas), 2018 (74.298 respostas) e 2022 (71.379 respostas). O Git foi o favorito dos desenvolvedores que responderam nessas pesquisas, relatando até 93,9% em 2022.

Sistemas de controle de versão usados pelos desenvolvedores que responderam as pesquisas:

| Name                | 2015  | 2017  | 2018  | 2022  |
| ------------------- | :---: | :---: | :---: | :---: |
| Git                 | 69.3% | 69.2% | 87.2% | 93.9% |
| Subversion          | 36.9% | 9.1%  | 16.1% | 5.2%  |
| None                | 9.3%  | 4.8%  | 4.8%  | 4.3%  |
| Mercurial           | 7.9%  | 1.9%  | 3.6%  | 1.13% |
| ClearCase           | -     | 0.4%  | -     | -     |
| CVS                 | 4.2%  | -     | -     | -     |
| Other               | 5.8%  | 3.0%  | -     | -     |
| Perforce            | 3.3%  | -     | -     | -     |
| Raw network sharing | -     | 1.7%  | 7.9%  | -     |
| TFVC                | 12.2% | 7.3%  | 10.9% | -     |
| VSS                 | -     | 0.6%  | -     | -     |
| Zip file backups    | -     | 2.0%  | 7.9%  | -     |

# Referências 

[^atlassian]:Atlassian. What is Version Control [https://www.atlassian.com/git/tutorials/what-is-version-control](https://www.atlassian.com/git/tutorials/what-is-version-control).(Acessado em 28/06/2022)

[^wikiscv]: Wikipedia. Sistema de controle de versões [https://pt.wikipedia.org/wiki/Sistema_de_controle_de_vers%C3%B5es](https://pt.wikipedia.org/wiki/Sistema_de_controle_de_vers%C3%B5es).(Acessado em 28/06/2022)

[^git-scm]: Scott Chacon and Ben Straub. Git - About Version Control[https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control).(Acessado em 28/06/2022)

[^wikigit]: Wikipedia. Git [httpsGit/Git](https://en.wikipedia.org/wiki/Git).(Acessado em 28/06/2022)
