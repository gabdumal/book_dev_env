# Rust

**Rust** é uma linguagem de programação recente, desenvolvida inicialmente pela **Mozilla Research** e atualmente mantida pela **Rust Foundation**.
Ela é focada em segurança, concorrência e performance, permitindo escrever código de baixo nível evitando acesso direto à memória e bugs comuns em linguagens como C e C++.

O Rust, em vez de utilizar um coletor de lixo, implementa as ideias de **ownership** e **borrowing**.
Isso significa que a linguagem controla o tempo de vida das variáveis e garante que não haja referências inválidas ou acesso à memória que não deveria ser feito.

Uma vez que boa parte do gerenciamento é feito em tempo de compilação, os programas escritos em Rust tendem a ser muito rápidos e seguros.

## Instalação

A forma recomendada de instalar o Rust é utilizando o [**rustup**](https://rust-lang.github.io/rustup/installation/index.html), um gerenciador de versões da linguagem.

### Ubuntu e Fedora

### WSL

### Windows

O Rust para Windows depende do **MSVC** (Microsoft Visual Studio Build Tools) para compilar código nativo.
Acesse o capítulo sobre o [compilador para C e C++](/src/chapters/c_cpp/compiler/index.md#windows) para aprender a instalar o MSVC.

Para instalar o rustup no Windows, acesse o [site oficial](https://www.rust-lang.org/tools/install) da linguagem e baixe o instalador referente à sua arquitetura.
Para a grande maioria dos casos, o instalador de **64 bits** é o mais adequado.

<figure>
<img src="./download_options_windows.png" />
<figcaption>Opções de download do rustup para Windows.</figcaption>
</figure>

O instalador abre uma janela de terminal que guiará você pelo processo de instalação.

<figure>
<img src="./windows_installer.png" />
<figcaption>Instalador do rust para Windows.</figcaption>
</figure>

Pressione a tecla <kbd>1</kbd> e <kbd>Enter</kbd> para instalar o Rust e suas ferramentas.

<figure>
<img src="./windows_installed.png" />
<figcaption>Finalização da instalação do rust para Windows.</figcaption>
</figure>

Para verificar se a instalação foi bem-sucedida, abra um terminal e execute o comando `rustc --version`.
O resultado deve ser algo como `rustc 1.82.0 (f6e511eec 2024-10-15)` ou mais recente.

Então, verifique se o **cargo**, o gerenciador de pacotes do Rust, também foi instalado corretamente com o comando `cargo --version`.
O resultado deve ser algo como `cargo 1.82.0 (8f40fc59f 2024-08-21)` ou mais recente.
