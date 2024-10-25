+++
  title = "PowerShell"
  type = "page"
  weight = 1
+++

O **PowerShell** é uma ferramenta de linha de comando desenvolvida pela Microsoft, que é utilizada para automatizar tarefas e gerenciar configurações do sistema operacional.

Por padrão, o Windows vem com o **PowerShell 5.1** instalado.
No entanto, a versão mais recente é a [**PowerShell 7**](https://learn.microsoft.com/en-us/powershell/scripting/whats-new/migrating-from-windows-powershell-51-to-powershell-7), que traz diversas melhorias e novas funcionalidades.

Segundo a Microsoft, ambas as versões podem existir lado a lado no mesmo sistema, sem conflitos.
Neste capítulo, vamos mostrar como instalar o **PowerShell 7** no Windows.

## Instalando o PowerShell 7

O modo de instalação recomendado pela Microsoft é através do **WinGet**, que é um gerenciador de pacotes para o Windows.

Acesse o [guia de instalação](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.4#install-powershell-using-winget-recommended).

Segundo ele, o comando a ser executado é:

```powershell
winget install --id Microsoft.PowerShell --source winget
```

<figure>
<img src="./installing_7.png" />
<figcaption>Processo de instalação do PowerShell 7 pelo WinGet.</figcaption>
</figure>

Feche a abra o PowerShell para que as alterações tenham efeito.
Abra a lista de opções de shell do Windows Terminal.
Você verá que há uma nova entrada ao fim da lista, chamada simplesmente **PowerShell**.

<figure>
<img src="./options_list.png" />
<figcaption>Lista de opções de shell para o Windows Terminal.</figcaption>
</figure>

Para abrir essa opção por padrão ao iniciar o Windows Terminal, clique na opção de **Configurações**.

Então, na seção de **Inicialização**, defina a opção **Perfil padrão** como **PowerShell**.

<figure>
<img src="./default_profile.png" />
<figcaption>PowerShell 7 definido como o perfil padrão de inicialização do Windows Terminal.</figcaption>
</figure>

Salve, **feche** e abra o Windows Terminal novamente para que as alterações tenham efeito.
