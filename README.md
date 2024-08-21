# Comandos Git

O intuito deste repositorio é a consulta de comandos gits que devem ser usados na manipulação de repositorios dentro do github. Sinta-se a vontade para realizar um fork e fazer comentários.

Verifique se o Git está installado em sua máquina utilizando o ``` git --version ```. Caso ainda não o tenha instalado clique [aqui](https://git-scm.com/downloads).

## Configurando seu usuário
**Se possível use o mesmo email e nome utilizados no github.com**


| Comando | Descrição |
| --- | --- |
|``` git config --global user.name "Seu Nome"```| Configuração do nome |
|``` git config --global user.email "SeuEmail@exemplo" ```| Configuração do email |

## Trabalhando com um repositório
> Os comandos a seguir são para que se possa clonar um repositório pessoal e realizar os comandos básicos de commit, push e pull. Siga o passo a passo.

| Comando | Descrição |
| --- | --- |
| ``` git clone <url> ```| Clona um repositório por meio de sua URL |
| ``` git add . ```| Prepara **todas** as mudanças feitas para commit |
| ``` git commit -m "mensagem" ```| Cria um commit com uma mensagem descritiva das mudanças realizadas |
| ``` git push origin ```| Envia o commit para o repositório remoto |
| ``` git pull origin ```| Baixa os últimos commits do repositório remoto para a sua máquina |

