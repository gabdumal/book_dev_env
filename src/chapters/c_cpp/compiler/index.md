# Compilador

A principal ferramenta para desenvolver em C e C++ é o compilador.
A função dele é transformar o código fonte escrito em um arquivo executável que pode ser rodado pelo sistema operacional.

Possivelmente, você já utilizou o compilador **GCC**.
Ele é muito popular em sistemas Linux, e também está disponível para Windows através do **MinGW**.
O GCC apenas compila projetos na linguagem C.

Para compilar projetos em C++, é comum utilizar outro compilador chamado **G++**.
Ele é do mesmo projeto do GCC, o [**GNU Compiler Collection**](https://gcc.gnu.org/).
Dessa forma, exibe um comportamento bastante similar, conseguindo compilar também códigos em C.

Existem, ainda, outros compiladores disponíveis, como o **Clang**.
Ele é um projeto do [**LLVM**](https://llvm.org/), que é uma infraestrutura para desenvolvimento de compiladores.
O Clang é conhecido por fornecer mensagens de erro mais claras para o usuário, e informações mais completas sobre o código para o processo de compilação.

Neste livro, vamos utilizar o **Clang** como compilador padrão para C e C++.
Sua instalação varia de acordo com o sistema operacional.
Vamos tratar separadamente a instalação no **Linux** (e **WSL**) e no **Windows**.

## Linux

<!-- TODO -->

## Windows

O **Microsoft Visual Studio** (MSVC) é uma IDE popular para desenvolvimento em C e C++ no Windows.
Muitas das suas funcionalidades são pagas, apesar de existir uma versão gratuita chamada **Community**.

Essa IDE é diferente do **Visual Studio _Code_**, o qual estamos utilizando neste livro.

Nós queremos apenas as ferramentas de compilação do **MSVC**.
Não é necessário instalar todo o Visual Studio.

Dessa forma, acesse a página de [downloads](https://visualstudio.microsoft.com/pt-br/downloads/#build-tools-for-visual-studio-2022) do Visual Studio e baixe a versão **Ferramentas de Build para Visual Studio 2022** (ou superior).

<figure>
<img src="download_options.png" />
<figcaption>Opções de download das ferramentas do Visual Studio, em que se seleciona a opção "Ferramentas de Build para Visual Studio 2022".</figcaption>
</figure>

Execute o instalador baixado e prossiga com a instalação.

<figure>
<img src="vs_installer.png" />
<figcaption>Instalação do gerenciador do Visual Studio.</figcaption>
</figure>

Na tela de seleção de cargas de trabalho, selecione apenas a opção **Desenvolvimento para desktop com C++**.

No menu lateral na esquerda, selecione as seguintes opções:

- Ferramentas de compilação MSVC v143 - VS 2022 C++ x64/x86 (mais recente)
- SDK do Windows 11 _(ou a opção selecionada para o seu sistema)_
- Ferramentas do CMake do C++ para Windows
- Recursos principais de ferramentas de teste --- Ferramentas de Build
- AddressSanitizer do C++
- ATL do C++ para as mais recentes ferramentas do build v143 (x86 e x64)
- MFC do C++ para as mais recentes ferramentas do build v143 (x86 e x64)
- Suporte do C++/CLI para as ferramentas do build v143 (Mais recente)
- Módulos do C++ para as ferramentas do build v143 (x86 e x64, experimental)

<figure>
<img src="installing_msvc.png" />
<figcaption>Tela de seleção de cargas de trabalho no gerenciador do Visual Studio.</figcaption>
</figure>

Clique em **Instalar** e aguarde o término da instalação.

Abra o menu de opções de perfis do Windows Terminal.
Você verá que duas novas entradas foram adicionadas:

- Developer Command Prompt for VS 2022
- Developer PowerShell for VS 2022

<figure>
<img src="options_list.png" />
<figcaption>Lista de opções de shell para o Windows Terminal.</figcaption>
</figure>

Para acessar as ferramentas instaladas, você deve utilizar o perfil **Developer PowerShell for VS 2022**.

Abra uma sessão nele e execute o comando `cl` para verificar se o compilador **Clang** foi instalado corretamente.

<figure>
<img src="testing_cl.png" />
<figcaption>Testando se a instalação do MSVC foi bem-sucedida.</figcaption>
</figure>

### Configurações do perfil

É interessante trocar a pasta inicial desse perfil para a pasta do seu usuário.
Acesse as configurações do perfil **Developer PowerShell for VS 2022**.
Abra a opção **Diretório inicial**, e troque o valor para `%USERPROFILE%`.
Então, **salve** as configurações.

<figure>
<img src="./initial_directory.png" />
<figcaption>Diretório de inicialização do perfil definido como a pasta do usuário.</figcaption>
</figure>

Se você deseja utilizar o **PowerShell 7** no perfil de desenvolvedor, você pode alterar o comando de inicialização do perfil.
Abra a opção **Linha de comando**.

O primeiro termo do comando é `powershell.exe`, que se refere à versão 5 do PowerShell.
Para utilizar o **PowerShell 7**, altere **apenas** este primeiro termo para `pwsh.exe`.

<figure>
<img src="init_ps_dev.png" />
<figcaption>Opção de inicialização do PowerShell para desenvolvimento do VS 2022 atualizada para usar o PowerShell 7.</figcaption>
</figure>

Então, **salve** as configurações.

### Configuração do terminal

Você pode também definir esse perfil como padrão, para que ele seja aberto automaticamente ao iniciar o Windows Terminal.

Faça isso na seção **Inicialização** e na opção **Perfil padrão**.

<figure>
<img src="./default_profile.png" />
<figcaption>"Developer PowerShell for VS 2022" definido como o perfil padrão de inicialização do Windows Terminal.</figcaption>
</figure>

**Salve** as configurações e **feche** o Windows Terminal.

<figure>
<img src="./new_terminal.png" />
<figcaption>Windows Terminal inicializado com o perfil de desenvolvimento.</figcaption>
</figure>

### Visual Studio Code

Para carregar as ferramentas de compilação no VSCode, é necessário primeiro abrir o Windows Terminal no perfil de desenvolvimento.

Então, execute o comando `code` para abrir o Visual Studio Code.
Se quiser abri-lo na pasta atual, utilize `code .`.

Para testar se a configuração foi bem-sucedida, abra o terminal integrado do VSCode e execute o comando `cl`.

<figure>
<img src="./opening_code.png" />
<figcaption>Abrindo o Visual Studio Code a partir do Windows Terminal, e executando o comando "cl" no terminal integrado.</figcaption>
</figure>

### Considerações

A instalação do **MSVC** utiliza o **Clang** como parte do seu conjunto de ferramentas.
Na verdade, o comando `cl` não é exatamente o compilador Clang, mas sim um wrapper que o chama.

Se você precisar do compilador Clang puro, você pode instalá-lo separadamente, junto com outras ferramentas do LLVM.
faremos isso no subcapítulo sobre o [depurador LLDB](/src/chapters/c_cpp/debugger/index.md).
