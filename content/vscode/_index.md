+++
  title = "Visual Studio Code"
  linkTitle = "VSCode"
  type = "chapter"
  weight = 2
+++

A fim de escrever código, você precisará de um editor de texto apropriado.
É interessante que ele seja voltado para o desenvolvimento de software, com funcionalidades como _syntax highlighting_, _code completion_, _debugging_, etc.

O **Visual Studio Code** é um editor de texto muito popular entre desenvolvedores.
Ele é leve, rápido e possui uma grande quantidade de extensões que facilitam o desenvolvimento de software.

Para este guia, vamos utilizar o Visual Studio Code e configurá-lo para compilar e depurar código em C e C++.

## Instalação

Apresento as formas ideias de instalar o Visual Studio Code nos três sistemas operacionais que estamos tratando neste guia: Windows, Ubuntu e Fedora.

### Windows

Você pode fazer o download do editor pelo [site oficial](https://code.visualstudio.com/Download).
Mesmo que você esteja usando o **WSL**, é necessário instalar o Visual Studio Code no Windows, pois é ele que irá gerenciar as extensões e configurações do editor.

<figure>
<img src="./download_options.png" />
<figcaption>Opções de download do Visual Studio Code, em que se seleciona o instalador do Windows.</figcaption>
</figure>

Execute o instalador e siga as instruções.
Quando chegar ao passo `Selecionar tarefas adicionais`, marque todas as opções na seção `Outros`.

<figure>
<img src="./other_options.png" />
<figcaption>Opções de download do Visual Studio Code, em que se selecionam todas as opções na seção Outros.</figcaption>
</figure>

### Ubuntu

Para instalar o Visual Studio Code no Ubuntu, e em outros sistemas que utilizam o gerenciador de pacotes `apt` (como Mint, Debian, Pop!\_OS, entre outros), podemos adicionar o repositório oficial do Visual Studio Code, o que o manterá atualizado automaticamente.

Para isso, utilize os seguintes comandos, conforme recomendado pelo [site oficial](https://code.visualstudio.com/docs/setup/linux#_debian-and-ubuntu-based-distributions).

```bash
sudo apt-get install wget gpg
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > packages.microsoft.gpg
sudo install -D -o root -g root -m 644 packages.microsoft.gpg /etc/apt/keyrings/packages.microsoft.gpg
echo "deb [arch=amd64,arm64,armhf signed-by=/etc/apt/keyrings/packages.microsoft.gpg] https://packages.microsoft.com/repos/code stable main" |sudo tee /etc/apt/sources.list.d/vscode.list > /dev/null
rm -f packages.microsoft.gpg
```

Em seguida, atualize a lista de pacotes e instale o Visual Studio Code:

```bash
sudo apt install apt-transport-https
sudo apt update
sudo apt install code
```

### Fedora

Para instalar o Visual Studio Code no Fedora, também podemos adicionar o repositório oficial do Visual Studio Code.

Utilize os seguintes comandos, conforme recomendado pelo [site oficial](https://code.visualstudio.com/docs/setup/linux#_rhel-fedora-and-centos-based-distributions):

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/yumrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" | sudo tee /etc/yum.repos.d/vscode.repo > /dev/null
```

Em seguida, instale o Visual Studio Code:

```bash
dnf check-update
sudo dnf install code
```

## Executando

Para abrir o Visual Studio Code, basta procurar por ele no menu de aplicativos do seu sistema operacional --- seja Windows, Ubuntu ou Fedora --- ou executar o comando `code` no terminal.

<figure>
<img src="./running_code_in_terminal.png" />
<figcaption>Executando o Visual Studio Code pelo Windows Terminal.</figcaption>
</figure>

Para abrir o VSCode no **WSL**, você pode prosseguir de duas formas abrir o Windows terminal pelo perfil do **WSL** e executar o comando `code`.

Ou então, pode abrir o VSCode normalmente, e selecionar o botão azul no canto inferior esquerdo, chamado `Open a Remote Window`.

<figure>
<img src="./remote_window.png" />
<figcaption>Botão para abrir uma conexão remota pelo Visual Studio Code.</figcaption>
</figure>

Então, selecione a opção `WSL` no menu que aparecer.

<figure>
<img src="./connections_menu.png" />
<figcaption>Opção WSL selecionada no menu de conexões remotas.</figcaption>
</figure>

Isso irá instalar a extensão do **WSL** no VSCode e atualizar sua janela para se conectar com o **Ubuntu**.

Algumas de suas extensões previamente instaladas manter-se-ão funcionando, mas algumas podem requerer que você clique em `Install in WSL: Ubuntu` para que funcionem corretamente.

<figure>
<img src="./extensions.png" alt="Seção de extensões do visual Studio Code, em que se vê a extensão 'WSL' instalada e sua descrição breve, além das extensões 'Error Lens' e 'vscode-pdf'. Também se veem as extensões 'AsciiDoc' e 'Brazilian Portuguese - Code Spell Checker' desabilitadas, nas quais aparece um botão escrito 'Install in WSL: Ubuntu'. No canto inferior esquerdo do aplicativo, o botão de conexões remotas agora mostra o texto 'WSL: Ubuntu'."/>
<figcaption>Seção de extensões do visual Studio Code, em que se vê a extensão WSL instalada.</figcaption>
</figure>

## Extensões

O Visual Studio Code possui uma grande quantidade de extensões que podem ser instaladas para adicionar funcionalidades ao editor.

Para instalar uma extensão no Visual Studio Code, clique no ícone de quadrados no canto esquerdo da janela, ou pressione `Ctrl+Shift+X`.

Então, pesquise pelo nome da extensão desejada e clique no botão `Install`.

Recomendo a instalação das seguintes:

- [Git Graph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [Error Lens](https://marketplace.visualstudio.com/items?itemName=usernamehw.errorlens)
- [Todo Tree](https://marketplace.visualstudio.com/items?itemName=Gruntfuggly.todo-tree)
- [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
- [Brazilian Portuguese - Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker-portuguese-brazilian)
- [vscode-pdf](https://marketplace.visualstudio.com/items?itemName=tomoki1207.pdf)
- [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
- [GitHub Copilot Chat](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot-chat)

Se você gostou do meu tema de cores, você pode instalá-lo também:

- [Catppuccin for VSCode](https://marketplace.visualstudio.com/items?itemName=Catppuccin.catppuccin-vsc)
- [Catppuccin Icons for VSCode](https://marketplace.visualstudio.com/items?itemName=Catppuccin.catppuccin-vsc)

Para cada uma dessas extensões, clique com o botão direito sobre e selecione **Apply Extensions to all Profiles**.

<figure>
<img src="./applying_extension_to_all_profiles.png" />
<figcaption>Aplicando a primeira extensão a todos os perfis do Visual Studio Code.</figcaption>
</figure>

Isso será importante mais tarde, quando criarmos perfis específicos para cada linguagem de programação.

## Configurações

Para configurar o Visual Studio Code, você pode acessar as configurações do editor clicando no ícone de engrenagem no canto inferior esquerdo da janela.

Alternativamente, você pode editar o arquivo `settings.json` diretamente.
Para isso, abra a paleta de comandos com `Ctrl+Shift+P` e digite `Preferences: Open User Settings (JSON)`.

<figure>
<img src="./opening_user_settings.png" />
<figcaption>Abrindo o arquivo de configurações pela paleta de comandos.</figcaption>
</figure>

Eu preparei um arquivo de configurações para o Visual Studio Code que inclui algumas definições úteis.

Copie o conteúdo do arquivo [`settings.json`](settings.json) deste capítulo e cole no arquivo `settings.json` do seu Visual Studio Code.

Sinta-se livre para alterar as configurações conforme sua preferência.
