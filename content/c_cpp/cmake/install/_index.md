+++
  title = "Instalação"
  type = "page"
  weight = 1
+++

A instalação do **CMake** é simples e pode ser feita de várias formas, dependendo do sistema operacional.

Vamos também instalar o **Ninja**, um gerador de build que é mais rápido que o **Make**.

## Linux

<!-- TODO -->

## Windows

Para instalar o **CMake** no Windows, acesse a página de [downloads](https://cmake.org/download/) do CMake.

Então, selecione a opção do instalador para Windows x64 mais recente.

<figure>
<img src="./download_options.png" />
<figcaption>Opções de download do CMake.</figcaption>
</figure>

Execute o instalador e siga as instruções.
Na página **Install Options**, selecione a opção **Add CMake to the PATH environment variable**.
Então prossiga com a instalação.

<figure>
<img src="./installing_windows.png" />
<figcaption>Instalando o CMake no Windows.</figcaption>
</figure>

Para verificar se a instalação foi bem-sucedida, abra o PowerShell e execute o comando `cmake`.

<figure>
<img src="./checking_installation_windows.png" />
<figcaption>Verificando se a instalação do CMake no Windows foi bem-sucedida.</figcaption>
</figure>

### Ninja

Para instalar o **Ninja**, acesse a página de [downloads](https://github.com/ninja-build/ninja/releases).

Selecione a opção para Windows na versão mais recente, marcada como **latest**.

<figure>
<img src="./ninja_download_options.png" />
<figcaption>Opções de download do Ninja.</figcaption>
</figure>

Extraia o arquivo Zip baixado.
Então rode o executável `ninja.exe`.

<!-- TODO: continuar -->
