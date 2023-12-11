# CursoGit
<h2> Aprendendo a usar Git: Passo a passo simples e direto a respeito das funcionalidades do Git com exemplos fáceis e eficientes! </h2>

<h3> Aula 1: Identificação- </h3>

git config --global user.name ""
git config --global user.email ""
git config --list
git config --global init.defaultBranch master/main


<h3>Aula 2: Criando repositório local-</h3>

git init


<h3>Aula 3: Adicionando/rastreando mudanças-</h3>

git add .
git add --all
git add -A
git status


<h3>Aula 4: Desfazendo mudanças-</h3>

git rm --cached *arquivo* : <b>remover da área de preparação</b>
git rm --cached -r .


<h3>Aula 5: Salvando mudanças-</h3>

git commit -m "mensagem de commit"


<h3>Aula 6: Visualizando alterações-</h3>

git diff : compara arquivo já rastreado com o modificado
git diff --cached : compara a área de preparação (add) com a commitada


<h3>Aula 7: Visualiazando histórico de commits</h3>

git log 
git log --oneline : mostra hash e mensagem do commit
git log -1 : mostra a quantidade de commits que deseja mostrar
git log --oneline -1
git log -p : mostra as mudanças de cada commit
git log --stat : mostra os arquivos que foram modificados de cada commit
git log --shortstat : mostra resumidamente os arquivos modificados


<h3>Aula 8: Alterando um commit- </h3>

git commit --amend -m "mensagem" : substitui o ultimo commit e modifica a mensagem
git commit --amend --no-edit : substitui o ultimo commit e não modifica a mensagem
git commit --amend : abre o editor de texto esperando uma mensagem


<h3>Aula 9: Alterando editor de texto padrão-</h3>

git config --global core.editor "code --wait" : configurando o Visual Studio Code como exemplo
code *arquivo* 
code .


<h3>Aula 10: Usando commits anteriores-</h3>

git checkout *hash do commit* : repositório vai assumir a versão desse commit 
git checkout main/master : volta normalmente pra branch principal


<h3>Aula 11: Desfazendo mudanças </h3>

git checkout *arquivo* : reverte mudanças de arquivos rastreados/mofificados para a ultima versão que o git conhece 
git clean -f : remove arquivos não rastreados
git restore --staged *arquivo* : reverte mudanças de arquivos ratreados/preparados se já existe um commit feito
git rm --cached *arquivo* : reverte mudanças de arquivos ratreados/preparados se já tiver ou não um commit feito




