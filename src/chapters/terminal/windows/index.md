# Windows Terminal

Este subcapítulo aborda o **Windows Terminal**, um emulador de terminal moderno para usuários do Windows.

Ele é instalado por padrão no Windows 11.
Para o Windows 10, você pode baixá-lo na [Microsoft Store](https://www.microsoft.com/store/productId/9N0DX20HK701?ocid=pdpshare).

## Atalho de teclado

Vamos criar um atalho de teclas para abrir o Windows Terminal.
Abra o `Executar` com <kbd>Win + R</kbd>, digite `shell:AppsFolder`, e pressione <kbd>Enter</kbd>.

<figure>
<img src="./open_folder.png" />
<figcaption>Abrindo a pasta de aplicativos pelo Executar.</figcaption>
</figure>

Encontre o ícone do Windows Terminal, clique com o botão direito do mouse e selecione `Criar atalho`.

<figure>
<img src="./select_terminal.png" />
<figcaption>Criando um atalho para o Windows Terminal.</figcaption>
</figure>

Clique em `Sim` para criar o atalho na área de trabalho.

<figure>
<img src="./confirm.png" />
<figcaption>Confirmação da criação do atalho na área de trabalho.</figcaption>
</figure>

Agora, clique com o botão direito do mouse no atalho criado na área de trabalho e selecione `Propriedades`.

<figure>
<img src="./edit_shortcut.png" />
<figcaption>Confirmação da criação do atalho na área de trabalho.</figcaption>
</figure>

Clique sobre a caixa de texto `Tecla de atalho` e pressione a combinação de teclas <kbd>Ctrl + Alt + T</kbd>.

<figure>
<img src="./set_keybinding.png" />
<figcaption>Confirmação da criação do atalho na área de trabalho.</figcaption>
</figure>

## Perfis

O Windows Terminal permite a criação de perfis, que são configurações personalizadas para o terminal.

Para acessar as configurações, clique no ícone de seta para baixo no canto superior direito da janela e selecione `Configurações`.

<figure>
<img src="./open_configurations.png" />
<figcaption>Menu de abertura das configurações do Windows Terminal.</figcaption>
</figure>

As configurações são divididas em seções, que permitem configurar o tema, as fontes, os atalhos de teclado, os perfis e outros aspectos do terminal.

<figure>
<img src="./initial_configs.png" />
<figcaption>Tela inicial das configurações do Windows Terminal.</figcaption>
</figure>

Eu gosto de usar o tema claro no terminal, o que eu posso fazer pela seção `Aparência`.
Então, posso selecionar a definição `Tema do Aplicativo` como `Claro`.

<figure>
<img src="./light_theme.png" />
<figcaption>Tela inicial das configurações do Windows Terminal.</figcaption>
</figure>

Entretanto, essa definição apenas muda o tema do aplicativo.
Para configurar a cor de fundo, as cores do texto, fonte, e aspectos relacionados, é necessário editar um perfil.

Para aplicar a mesma configuração a todos os perfis, selecione a seção `Padrões` dentro de `Perfis` no menu lateral.
Então selecione a opção `Aparência` no fim do menu.

Eu defini o tema como `One Half Light` e o tamanho da fonte como 16.

<figure>
<img src="./default_profile.png" />
<figcaption>Definições do perfil padrão.</figcaption>
</figure>

Toda essa interface apenas edita um arquivo de configuração, que pode ser acessado diretamente pelo botão `Abrir JSON`.

<figure>
<img src="./json_file.png" />
<figcaption>Arquivo JSON de definições do Windows Terminal.</figcaption>
</figure>

Eu gosto de usar um tema bastante popular chamado `Catppuccin`.
Ele é um projeto que oferece personalização para uma série de programas.
Você pode optar entre quatro variantes: Latte, Frappé, Macchiato e Mocha.

Para aplicar o tema ao Windows Terminal, acesse o [repositório da implementação](https://github.com/catppuccin/windows-terminal).
Decida qual das variantes você deseja usar.

Eu prefiro a variante `Latte`.
Para aplicar o tema, abra o arquivo `latte.json` do repositório do GitHub (ou o correspondente à variante que você escolheu) e copie o conteúdo.

Então, abra o arquivo de configuração do Windows Terminal e cole o conteúdo copiado dentro da seção `schemes`.

<figure>
<img src="./schemes.png" />
<figcaption>Tema Catppuccin Latte sendo aplicado no atributo "schemes".</figcaption>
</figure>

Depois, copie o conteúdo do arquivo `latteTheme.json` do repositório (ou o correspondente à variante que você escolheu) e cole dentro da seção `themes`.

<figure>
<img src="./themes.png" />
<figcaption>Tema Catppuccin Latte sendo aplicado no atributo "themes".</figcaption>
</figure>

Salve o arquivo de configuração e feche o Windows Terminal.
Abra o terminal novamente.
Agora, você verá que o esquema de cores `Catppuccin Latte` está disponível na lista de temas.

<figure>
<div style="display:flex;align-items:center;gap:1rem;">
<img src="./schemes_list.png" style="height:320px;"/>
<img src="./themes_list.png" style="height:320px;"/>
</div>
<figcaption>Tema Catppuccin Latte disponível nas listas de esquema de cores e temas.</figcaption>
</figure>

Você pode aplicar o tema da mesma forma como selecionamos o tema claro e o `One Half Light` anteriormente.
