# Javascript

Javascript é uma linguagem de programação de alto nível, interpretada, imperativa e prototipada.
Tem muitos usos no desenvolvimento web, como a criação de páginas web dinâmicas, jogos, aplicativos móveis e servidores.
Além disso, uma série de ferramentas dependem do Javascript, de seus gerenciadores de pacotes e de seus ambientes de execução.

Neste capítulo vamos aprender a instalar e configurar as seguintes ferramentas:

- [**PNPM**](https://pnpm.io/)
- [**Node**](https://nodejs.org/)
- [**Typescript**](https://www.typescriptlang.org/)

## PNPM

O **PNPM** é um gerenciador de pacotes para Javascript que visa ser mais rápido e resolver problemas comuns em gerenciadores de pacotes como o **NPM** e o **Yarn**.
Uma das vantagens dele é que ele gerencia também versões do **Node**, como veremos adiante.

### Instalação

A instalação do **PNPM** é feita através de um script que pode ser baixado e executado diretamente no terminal.

#### Windows

Para instalar o PNPM no Windows, execute o seguinte comando no **PowerShell**:

```powershell
Invoke-WebRequest https://get.pnpm.io/install.ps1 -UseBasicParsing | Invoke-Expression
```

<figure>
<img src="./install_pnpm.png" />
<figcaption>Instalação do PNPM para Windows.</figcaption>
</figure>

Para verificar se a instalação foi bem sucedida, execute o comando `pnpm --version`.

O resultado deve ser algo como `9.12.2` ou mais recente.

##### Alias

Apesar das vantagens, o **NPM** ainda é bem mais popular que o PNPM.
Muitos guias e tutoriais que você pode encontrar usam os comandos do NPM.

Para facilitar a transição, você pode criar um alias para o PNPM.
Isto é, um "apelido" para que, quando você digitar `npm`, o terminal entenda que você quer dizer `pnpm`.

Para definir isso, abra o arquivo de configuração do PowerShell digitando `code $PROFILE` no terminal.

Então, adicione o seguinte bloco ao **final** do arquivo:

```powershell
# User configuration

## Aliases

### PNPM
Set-Alias -Name npm -Value 'pnpm'
Function npx {
  pnpm dlx $args
}
```

Então, **salve** o arquivo de configuração e feche o editor.

## Node

O **Node** é um ambiente de execução para Javascript que permite rodar códigos Javascript fora do navegador.

Utilizando o PNPM, é possível instalar versões específicas do Node, e trocar entre elas para diferentes projetos.

### Instalação

O processo de instalação é o mesmo em todos os sistemas operacionais tratados por este livro.

Abra o terminal e execute o seguinte comando:

```powershell
pnpm env use --global lts
```

Isso instalará a versão mais recente do Node que é considerada estável.

<figure>
<img src="./install_node.png" />
<figcaption>Instalação do NODE.</figcaption>
</figure>

Para verificar se a instalação foi bem sucedida, execute o comando `node --version`.

O resultado deve ser algo como `20.18.0` ou mais recente.
