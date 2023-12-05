# CursoGit
Aprendendo a usar Git: Passo a passo simples e direto a respeito das funcionalidades do Git com exemplos fáceis e eficientes!

Aula 1: Identificação- 

git config --global user.name ""
git config --global user.email ""
git config --list
git config --global init.defaultBranch master/main


Aula 2: Criando repositório local-

git init


Aula 3: Adicionando/rastreando mudanças-

git add .
git add --all
git add -A
git status


Aula 4: Desfazendo mudanças-

git rm --cached *arquivo*
git rm --cached -r .


Aula 5: Salvando mudanças-

git commit -m "mensagem de commit"


Aula 6: Visualizando alterações-

git diff : compara arquivo já rastreado com o modificado
git diff --cached : compara a área de preparação (add) com a commitada


Aula 7: Visualiazando histórico de commits

git log 
git log --oneline : mostra hash e mensagem do commit
git log -1 : mostra a quantidade de commits que deseja mostrar
git log --oneline -1
git log -p : mostra as mudanças de cada commit
git log --stat : mostra os arquivos que foram modificados de cada commit
git log --shortstat : mostra resumidamente os arquivos modificados


Aula 8: Alterando um commit- 

git commit --amend -m "mensagem" : substitui o ultimo commit e modifica a mensagem
git commit --amend --no-edit : substitui o ultimo commit e não modifica a mensagem
git commit --amend : abre o editor de texto esperando uma mensagem


Aula 9: Alterando editor de texto padrão-

git config --global core.editor "code --wait" : configurando o Visual Studio Code como exemplo
code *arquivo* 
code .


Aula 10: Usando commits anteriores-

git checkout *hash do commit* : repositório vai assumir a versão desse commit 
git checkout main/master : volta normalmente pra branch principal


Aula 11: Desfazendo mudanças 

git checkout *arquivo* : 


