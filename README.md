# Comandos Git

O intuito deste repositório é servir como uma consulta de comandos Git que devem ser usados na manipulação de repositórios no GitHub. Sinta-se à vontade para realizar um fork e fazer comentários.

Verifique se o Git está instalado em sua máquina utilizando o comando `git --version`. Caso ainda não o tenha instalado, clique [aqui](https://git-scm.com/downloads).

## Configurando seu usuário

**Se possível, use o mesmo email e nome utilizados no github.com**

| Comando | Descrição |
| --- | --- |
| `git config --global user.name "Seu Nome"` | Configuração do nome |
| `git config --global user.email "SeuEmail@exemplo"` | Configuração do email |

## Manipulando um repositório

> Um repositório é um local onde todos os arquivos do projeto e o histórico completo de suas mudanças são armazenados. Ele contém todos os commits, branches, tags, e outros dados relacionados ao desenvolvimento do projeto.

| Comando | Descrição |
| --- | --- |
| `git clone <url>` | Clona um repositório por meio de sua URL |
| `git add .` | Prepara **todas** as mudanças feitas para commit |
| `git commit -m "mensagem"` | Cria um commit com uma mensagem descritiva das mudanças realizadas |
| `git push origin` | Envia o commit para o repositório remoto |
| `git pull origin` | Baixa os últimos commits do repositório remoto para a sua máquina |

## Manipulando Branches

Uma **branch** no Git funciona como uma ramificação do código principal, permitindo que você faça mudanças ou desenvolva novas funcionalidades sem afetar a linha principal do código (geralmente chamada de `main` ou `master`). Portanto, uma branch apresenta certas utilidades:

- **Desenvolvimento de Funcionalidades:** Permite desenvolver novas funcionalidades ou correções de bugs de forma isolada, sem interferir no código estável da `main`.
- **Trabalho em Equipe:** Diferentes membros da equipe podem trabalhar em diferentes branches, facilitando a integração de código e evitando conflitos.
- **Testes e Experimentações:** Permite testar novas ideias ou tecnologias sem o risco de comprometer a versão estável do projeto. Se algo der errado, basta descartar a branch.
- **Gestão de Releases:** Ajuda a gerenciar diferentes versões do software, por exemplo, branches para a versão de produção e para o desenvolvimento contínuo.
- **Correção de Bugs:** Se um bug crítico é encontrado na versão de produção, você pode criar uma branch a partir dessa versão para corrigir o bug, sem interromper o desenvolvimento contínuo.

**Comandos para criação de uma nova branch**

| Comando | Descrição |
| --- | --- |
| `git branch Nome-nova-Branch` | Cria uma nova branch |
| `git checkout Nome-Branch` | Muda para uma branch já existente |
| `git checkout -b Nome-nova-Branch` | Cria uma nova branch e muda para ela |

**Comandos para modificação de uma branch**

| Comando | Descrição |
| --- | --- |
| `git branch -m nome-antigo nome-novo` | Altera o nome da branch localmente |
| `git branch --set-upstream-to=origin/Repositorio-remoto Repositorio-local` | Conecta uma branch a outra, fazendo com que ambas compartilhem os mesmos dados |
| `git merge Nome-Branch` | Necessário estar na branch de destino para mesclar os arquivos de uma branch para outra |

**Comandos para excluir uma branch**

| Comando | Descrição |
| --- | --- |
| `git branch -d Nome-da-Branch` | Apaga a branch localmente sem forçá-la |
| `git branch -D Nome-da-Branch` | Força a branch a ser apagada localmente |
| `git push origin --delete Nome-da-Branch` | Remove a branch do repositório remoto |

**Comandos bônus**

| Comando | Descrição |
| --- | --- |
| `git branch` | Lista todas as branches locais |
| `git switch Nome-da-Branch` | Muda para a branch desejada, assim como o `git checkout Nome-da-Branch` |

## Recuperando commits antigos

> Esta seção é voltada para quando desejamos voltar em algum ponto no processo de produção devido a um erro, falha ou apenas para consulta.

| Comando | Descrição |
| --- | --- |
| `git log` | Mostra todos os commits feitos na branch |
| `git checkout <commit-hash>` | Muda todos os arquivos para o estado de um commit específico |

**Comandos `reset`**

Tenha como exemplo esta árvore de commits: `A -- B -- C -- D -- E (HEAD -> main) (as letras são os hashes dos commits)`

| Comando | Descrição |
| --- | --- |
| `git reset --soft <hash-code-C>` | A árvore de commits ficará como `A -- B -- C (HEAD -> main)`. Os commits realizados em `D` e `E` ainda estão presentes nos arquivos, prontos para serem commitados. |
| `git reset --mixed <hash-code-C>` | A árvore de commits ficará como `A -- B -- C (HEAD -> main)`. As mudanças feitas em `D` e `E` ainda estão presentes nos arquivos, mas não estão preparadas para commit (não estão no stage). |
| `git reset --hard <hash-code-C>` | A árvore de commits ficará como `A -- B -- C (HEAD -> main)`. As mudanças feitas em `D` e `E` são **apagadas permanentemente**. |

