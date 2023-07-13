# Anotações de Git
Este repositório contém alguns comandos do Git, que são utilizados no dia-a-dia.

## Adicionar usuário e e-mail na config global

`git config --global user.name "Nome de usuário"`

`git config --global user.email emaildousuario@exemplo.br`

## Salvar dados do usuário github definitivamente

`git config --global credential.helper cache`
> Esse comando permite que o usuário github fique salvo e, assim, não fique solicitando sempre o usuário e senha para fazer commits.

## Remover arquivo do controle de versão

`git rm --cached NOME_DO_ARQUIVO`
> Alterar **NOME_DO_ARQUIVO** por arquivo desejado.

## Criar uma branch nova

`git checkout -b NOME_DA_BRANCH`
> Alterar **NOME_DA_BRANCH** por nome do branch desejado.

## Alterar branch em que esta e ir para outra

`git checkout NOME_DA_BRANCH`
> Exemplo: git checkout master volta para o master

## Verificar status dos arquivos 
`git status`

## Adicionar um arquivo ao controle de versão
`git add NOME_DO_ARQUIVO`

## Commitar uma mudança
`git commit -m "MENSAGEM_DO_COMMIT"`

## Push para branch não master

`git push origin NOME_DO_BRANCH`
> Exemplo: git push origin dev

## Desfazer um commit errado em uma branch errada

> Muda para a branch errada (onde o commit foi feito) e mostra o log, assim você identifica o commit e pega o id do commit 

`git checkout branch-errada`

`git log`

> Muda para a branch certa ( onde o commit deveria estar) e copia o commit para a branch atual

`git checkout branch-certa`

`git cherry-pick <id-do-commit>`

> Muda para a branch errada e aplica o revert no commit indesejado, assim a branch segue sem essas alterações

`git checkout branch-errada`

`git revert <id-do-commit>`

## Salvar alterações para uso posterior
> Salva as alterações sem precisar dar commit, isso permite que você possa ir para outra branch ou trabalhar em outras alterações, sem que perca as alterações que já foram feitas.

`git stash`

> Esse comando tira o stash da pilha e aplica as mudanças que você guardou ao utilizar o camando anterior.

`git stash pop`
