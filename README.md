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

git add . <br>
git add --all <br>
git add -A <br>
git status


<h3>Aula 4: Desfazendo mudanças-</h3>

git rm --cached *arquivo* : <b>remover da área de preparação</b> <br>
git rm --cached -r .


<h3>Aula 5: Salvando mudanças-</h3>

git commit -m "mensagem de commit"


<h3>Aula 6: Visualizando alterações-</h3>

git diff : compara arquivo já rastreado com o modificado <br>
git diff --cached : compara a área de preparação (add) com a commitada


<h3>Aula 7: Visualiazando histórico de commits</h3>

git log 
git log --oneline : mostra hash e mensagem do commit <br>
git log -1 : mostra a quantidade de commits que deseja mostrar <br>
git log --oneline -1 <br>
git log -p : mostra as mudanças de cada commit <br>
git log --stat : mostra os arquivos que foram modificados de cada commit <br>
git log --shortstat : mostra resumidamente os arquivos modificados


<h3>Aula 8: Alterando um commit- </h3>

git commit --amend -m "mensagem" : substitui o ultimo commit e modifica a mensagem <br>
git commit --amend --no-edit : substitui o ultimo commit e não modifica a mensagem <br>
git commit --amend : abre o editor de texto esperando uma mensagem


<h3>Aula 9: Alterando editor de texto padrão-</h3>

git config --global core.editor "code --wait" : configurando o Visual Studio Code como exemplo <br>
code *arquivo* <br>
code .


<h3>Aula 10: Usando commits anteriores-</h3>

git checkout *hash do commit* : repositório vai assumir a versão desse commit <br>
git checkout main/master : volta normalmente pra branch principal


<h3>Aula 11: Desfazendo mudanças </h3>

git checkout *arquivo* : reverte mudanças de arquivos rastreados/mofificados para a ultima versão que o git conhece <br>
git clean -f : remove arquivos não rastreados <br>
git restore --staged *arquivo* : reverte mudanças de arquivos ratreados/preparados se já existe um commit feito <br>
git rm --cached *arquivo* : reverte mudanças de arquivos ratreados/preparados se já tiver ou não um commit feito


<h3>Aula 12: .gitignore-</h3>

git update-index --skip-worktree *arquivo* : faz com que arquivos que já foram commitados serem ignorados <br>
git update-index --no-skip-worktree *arquivo* : desfaz a ultima alteração


<h3>Aula 13: Clonando repositório-</h3>

git clone *caminho do repositório*


<h3>Aula 14: Github - Endereço de repositório - </h3>

git remote -v : mostra o repositório remoto associado <br>
git remote add origin *caminho do repositório* : associar repositório local com remoto <br>
git remote set-url origin *caminho do repositório* : muda endereço do repositório

