+++
  title = "Zsh"
  type = "page"
  weight = 2
+++

O **Zsh** é um shell que busca ser mais poderoso e flexível que o Bash (o shell padrão do Ubuntu e do Fedora)
Ele permite a instalação de uma série de plugins de forma mais simplificada.

Vamos instalá-lo já pensando em utilizar seu framework de customização [**Oh My Zsh**](https://github.com/ohmyzsh/ohmyzsh).
Para instalar o Zsh, vamos seguir as instruções do [site](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH) do Oh My Zsh.

## Instalação

### Ubuntu e WSL

Execute o comando abaixo no terminal:

```bash
sudo apt install zsh
```

Verifique a instalação com o comando:

```bash
zsh --version
```

E então o defina como o shell padrão:

```bash
chsh -s $(which zsh)
```

### Fedora

Execute o comando abaixo no terminal:

```bash
sudo dnf install zsh
```

Verifique a instalação com o comando:

```bash
zsh --version
```

E então o defina como o shell padrão:

```bash
sudo lchsh $USER
```

### Windows

Infelizmente, o Zsh não é suportado nativamente no Windows.
Ainda assim, instalaremos alguns plugins no PowerShell para aprimorá-lo.

---

### Arquivo de configuração

Após instalar o Zsh, **feche** o terminal e abra-o novamente.
Se tudo correr bem, você verá o texto de boas-vindas.

<figure>
<img src="./welcome.png" />
<figcaption>Texto de boas-vindas do Zsh no Windows Terminal rodando o Ubuntu.</figcaption>
</figure>

O Zsh está pedindo para você criar um arquivo de configuração para ele.
O shell, assim como diversos outros programas no Linux utilizam arquivos de configuração para definir suas opções.

Pressione <kbd>0</kbd> para criar um arquivo vazio.
Não se preocupe, vamos preenchê-lo mais adiante.

O arquivo de configuração do Zsh é o `.zshrc`, assim mesmo, com ponto no começo e sem extensão.
Sua localização é na pasta do seu usuário.

## Oh My Zsh

O **Oh My Zsh** é um framework para gerenciar a configuração do zsh.
Ele é altamente _customizável_ e _extensível_, graças a uma grande quantidade de _plugins_ e _temas_ disponíveis.

Uma vez que ele depende do Zsh, sua instalação pode ser feita no Ubuntu, no Fedora e no WSL, mas não no PowerShell.

### Instalação

Suas instruções de instalação estão disponíveis no seu [repositório no GitHub](https://github.com/ohmyzsh/ohmyzsh?tab=readme-ov-file#basic-installation).

Execute o seguinte comando no terminal para instalar o Oh My Zsh:

```bash
sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Além de instalar o Oh My Zsh, o script de instalação também configura o arquivo `.zshrc` de forma a carregar o framework.

<figure>
<img src="./install_omz.png" />
<figcaption>Script de instalação do Oh My Zsh sendo executado no Ubuntu WSL.</figcaption>
</figure>

### Configuração

**Feche** e abra um novo terminal para que as alterações feitas no arquivo `.zshrc` tenham efeito.

Vamos usar um editor de texto para abrir o arquivo de configuração.
Como já instalamos o Visual Studio Code, podemos usá-lo.

Digite no terminal o seguinte comando:

```bash
code ~/.zshrc
```

O `~` é um atalho para a pasta do usuário, ou seja, `/home/gabriel` no meu caso.
Dentro dela, está o arquivo `.zshrc`.

<figure>
<img src="./zsh_code_initial.png" />
<figcaption>Arquivo de configuração do Zsh exibido no VSCode, com o aviso de arquivo modo restrito.</figcaption>
</figure>

Caso dentro do VSCode haja um aviso de que o arquivo está em modo restrito, clique em "Manage".
Então, na próxima página clique em "Trust".

<figure>
<img src="./code_trusted.png" />
<figcaption>Permitindo confiar no arquivo de configuração do Zsh no VSCode.</figcaption>
</figure>

Uou, realmente é um arquivo grande!
Mas não se preocupe, todas as linhas que começam com `#` são comentários e não são executadas.
Então, na verdade, não tem quase nada sendo definido no arquivo.

Por isso, vamos **apagar** tudo, e adicionar as seguintes linhas:

```bash
# Path to your Oh My Zsh installation.
export ZSH="$HOME/.oh-my-zsh"

# Shell configuration
ZSH_THEME="robbyrussell"

## Plugins
plugins=(git)

## User configuration
PATH=$PATH:~/.local/bin

## Source Oh my Zsh
source $ZSH/oh-my-zsh.sh
```

Por enquanto não definimos nada novo.
Vamos fazer isso no próximo subcapítulo.
