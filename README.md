# Comandos Git

O intuito deste repositorio é a consulta de comandos gits que devem ser usados na manipulação de repositorios dentro do github. Sinta-se a vontade para realizar um fork e fazer comentários.

Verifique se o Git está installado em sua máquina utilizando o ``` git --version ```. Caso ainda não o tenha instalado clique [aqui](https://git-scm.com/downloads).

## Configurando seu usuário
**Se possível use o mesmo email e nome utilizados no github.com**


| Comando | Descrição |
| --- | --- |
|` git config --global user.name "Seu Nome"`| Configuração do nome |
|` git config --global user.email "SeuEmail@exemplo" `| Configuração do email |

## Manipulando um repositório
> Um repositório é um local onde todos os arquivos do projeto e o histórico completo de suas mudanças são armazenados. Ele contém todos os commits, branches, tags, e outros dados relacionados ao desenvolvimento do projeto.

| Comando | Descrição |
| --- | --- |
| ` git clone <url> `| Clona um repositório por meio de sua URL |
| ` git add . `| Prepara **todas** as mudanças feitas para commit |
| ` git commit -m "mensagem" `| Cria um commit com uma mensagem descritiva das mudanças realizadas |
| ` git push origin `| Envia o commit para o repositório remoto |
| ` git pull origin `| Baixa os últimos commits do repositório remoto para a sua máquina |

## Manipulando Branchs (galhos)

Uma **branch** no Git funciona como uma ramificação do código principal, permitindo que você faça mudanças ou desenvolva novas funcionalidades sem afetar a linha principal do código (geralmente chamada de `main` ou `master`). Portanto uma branch apresenta certas serventias:

* **Desenvolvimento de Funcionalidades:** Desenvolver novas funcionalidades ou correções de bugs de forma isolada sem interferirá no código estável da main.

* **Trabalho em Equipe:** Diferentes membros da equipe podem trabalhar em diferentes branches, o que facilita a integração de código e evita conflitos.

* **Testes e Experimentações:** Teste de novas ideias ou tecnologias sem o risco de comprometer a versão estável do projeto. Se algo der errado, basta descartar a branch.

* **Gestão de Releases:** Gerenciar diferentes versões do software. Por exemplo, branchs para a versão de produção e para o desenvolvimento contínuo.

* **Correção de Bugs:** Se um bug crítico é encontrado na versão de produção, você pode criar uma branch a partir da versão de produção para corrigir o bug, sem interromper o desenvolvimento contínuo.

**Comandos para criação de uma nova branch**

| Criação | Descrição |
| --- | --- |
| ` git branch Nome-nova-Branch `| Criar uma nova branch |
| ` git checkout Nome-Branch" `| Mudar para uma branch já existente |
| ` git checkout -b Nome-nova-Branch `| Cria uma nova branch e mudar para a mesma |


**Comandos para modificação de uma branch**
| Modificação | Descrição |
| --- | --- |
|` git branch -m nome-antigo nome-novo `| Altera o nome da branch localmente|
|` git branch --set-upstream-to=origin/Repositorio-remoto Repositorio-local `| Conecta uma branch a outra, fazendo assim que ambas compartilhem os mesmos dados|


**Comandos para excluir uma branch**
| Deletar | Descrição |
| --- | --- |
| ` git branch -d Nome-da-Branch `| Apaga a branch localmente sem força-la |
| ` git branch -D Nome-da-Branch`| Força a branch a ser apagada localmente |
| ` git push origin --delete Nome-da-Branch`| Remove a branch do repositório remoto |


**Comandos bônus**
| Bônus | Descrição |
| --- | --- |
| ` git branch `| Lista todas as branch locais |
| ` git switch Nome-da-Branch`| Muda para a branch desejada assim como o ` git checkout Nome-da-Branch` |

