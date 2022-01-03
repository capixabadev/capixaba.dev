---
layout: post
title: Instalando o Fish Shell no Fedora Linux
author: Douglas Gusson
tags: [fish, shell, fedora]
comments: true
---

Olá, pessoas. Neste tutorial veremos como instalar o Fish Shell no Fedora e como torná-lo o seu interpretador padrão.

## Fish

Uma breve definição do Fish extraída do site do projeto: 

> "**The user-friendly command line shell**. fish is a smart and user-friendly command line shell for macOS, Linux, and the rest of the family. fish includes features like syntax highlighting, autosuggest-as-you-type, and fancy tab completions that just work, with no configuration required." - [fish-shell](https://github.com/fish-shell/fish-shell)

Como pôde ser observado no trecho acima o Fish tem uma proposta de ser um interpretador shell inteligente e amigável, incluindo recursos como destaque de sintaxe, auto-sugestão enquanto você digita e preenchimentos sofisticados que funcionam sem a necessidade de configuração.

### Instalação

No caso do Fedora, para instalar o Fish, basta rodar um `dnf install <nome_do_pacote>`:

```bash
sudo dnf install fish
```

Eu outras distribuições será bem parecido, podendo mudar apenas o comando do gerenciador de pacotes. Verifique se a sua distribuição possui suporte e os passos da instalação diretamente no site do [Fish](https://fishshell.com/).

Após instalar, podemos chamá-lo diretamento pelo terminal executando o comando `fish`.

### Tornando o Fish o Shell padrão

Para torna o Fish o nosso interpretador padrão, precisamos do `chsh` (_change shell_), ele está disponível no pacote `util-linux-user`:

```bash
sudo dnf install util-linux-user
```

Após instalado, podemos executar o seguinte comando para tornar o fish nosso shell padrão:

```bash
chsh -s $(which fish)
```

Com isso quando a gente reiniciar a máquina o Fish estará habilitado por padrão.


## Links úteis

* https://fishshell.com/
* https://fedoramagazine.org/fish-a-friendly-interactive-shell/
* http://fishshell.com/docs/current/faq.html#faq-greeting
