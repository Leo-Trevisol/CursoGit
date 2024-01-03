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
git log --shortstat : mostra resumidamente os arquivos modificados <br>
git log *nome da branch* --oneline : mostra histórico de uma branch


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


<h3>Aula 15: Salvando e baixando mudanças no servidor-</h3>

git push <br>
git pull <br>


<h3>Aula 16: Gerar chave ssh-</h3>

ssh-keygen <br>
cd ~/.ssh/ <br>
start . <br>
eval $(ssh-agent) <br>
ssh-add ~/.ssh/*chave* : referenciar/adicionar chave


<h3>Aula 17: Criando branch local-</h3>

git branch / git branch --list <br>
git branch *nome da branch* <br>
git checkout *nome da branch* <br>
git checkout -b *nome da branch* : criar e já mudar pra branch <br>
git switch - muda pra ultima branch checkada <br>
git switch -c *nome da branch* : criar e já mudar pra branch <br>
git checkout -f *nome da branch* : muda de branch e descarta alterações não rastreadas


<h3>Aula 18: Detached head-</h3>

git checkout *hash do commit* : navegar e fazer mudanças em um commit


<h3>Aula 19: Enviando/removendo branch local/remota-</h3>

git push --set-upstream origin *nome da branch* : enviar para o repositorio remoto <br>
git push -u origin *nome da branch* : enviar para o repositorio remoto <br>
git branch -d *nome da branch* : remover branch local <br>
git push --delete origin *nome da branch* : remover branch remota

<h3>Aula 20: Renomeando branch-</h3>

git branch -m *novo nome* : renomear branch checkada no momento <br>
git branch -m *nome da branch* *nome da nova branch* : renomear branch não checkada 


<h3>Aula 21: Criando merge-</h3>

git merge *nome da branch* : mescla a branch na branch checkada <br>
git brach --no-merged : mostra as branchs não mescladas com a branch checkada <br>
git branch --merged : mostra as branchs mescladas com a branch checkada


<h3>Aula 22: Resolvendo conflitos de merges-</h3>

git merge --abort : cancelar um merge


<h3>Aula 23: Criando tags-</h3>

git tag *nome da tag* : cria tag no exato ponto checkado <br>
git tag -a -m "mensagem" *nome da tag* : cria tag com descrição e marca quem fez <br>
git show *nome da tag* : mostra as informações da tag <br>
git tag / git tag -l / git tag --list <br>  
git tag -n : mostra a descrição das tags <br>
git tag *nome da tag* *hash do commit* : cria tag no commit especifico <br>
git tag -a -m "mensagem" *nome da tag* *hash do commit* <br>  
git push origin *nome da tag* : envia tag citada para o servidor <br>
git push --tags : envia todas as tags para o servidor <br>
git checkout *nome da tag* : navega para a tag <br>
git diff *nome da tag* *nome da tag* : mostra as diferenças entre duas tags <br>
git tag -d *nome da tag* : remove tag local <br>
git push --delete origin *nome da tag* : remove tag no servidor


<h3>Aula 24: Criando stash-</h3>

git stash : salva as ultimas mudanças de arquivos rastreados e limpa a branch <br>
git stash list <br>
git stash apply : aplica as mudanças do primeiro stash da lista de stashs <br>
git stash apply stash@{*numero do stash*} <br>
git stash pop : aplica e exclui mudanças do primeiro stash da lista de stashs <br>
git stash pop stash@{*numero do stash*} <br>
git stash drop : exclui o primeiro stash da lista de stashs <br>
git stash drop stash@{*numero do stash*} <br>
git stash branch *nome da branch* : cria branch a partir do primeiro stash da lista da stashs <br>
git stash branch *nome da branch* stash@{*numero do stash*}


<h3>Aula 25: Revertendo commits-</h3>

git revert HEAD : adiciona um novo commit que desfaz as alterações introduzidas pelo commit especificado <br>
git revert *hash do commmit* <br>
git revert HEAD --no-edit : Isso criará automaticamente um novo commit de reversão sem solicitar que você insira uma mensagem de commit


<h3>Aula 26: Desfazendo commits-</h3>

git reset --hard HEAD : desfaz todas as alterações e assume a HEAD <br>
git reset --hard HEAD~*numero de commits* : desfaz todas as alterações e assume o número do commit informado (informar quantos commits devem voltar) <br>
git commit -a -m "mensagem" : adiciona arquivos na area de preparação e já commita <br>
git reset --mixed HEAD : mantém as alterações na área de modificadas e assume a HEAD <br>


<h3> Aula 27: Forçando envio de mudanças-</h3>

git push --force : força mudança no repositório remoto pra ele ficar igual ao local <br>
git push --force-with-lease : força mudança no repositório remoto pra ele ficar igual ao local caso mudanças no remoto não sejam perdidas


<h3>Aula 28: Rebase-</h3>

git rebase *nome da branch* : reorganizar ou rebase commits locais no topo dos commits mais recentes do repositório remoto, em vez de fazer uma fusão padrão. O objetivo é manter um histórico linear e mais limpo <br>
git rebase --abort : cancela o rebase caso de algum conflito <br>
git rebase --continue : continua o rebase após tratar os conflitos <br> 
git pull --rebase : busca as alterações do repositório remoto e reorganiza seus commits locais no topo dessas alterações, em vez de criar um novo commit de mesclagem 


<h3>Aula 29: Rebase squash-</h3>

git rebase -i/ git rebase --interactive : pega os ultimos commits não mandados para o servidor e abre o editor, que vai dar a opção de dar um squash, que seria juntar os commits em 1 só


<h3> Aula 30: crerry-pick- </h3>

git cherry-pick *hash do commit da outra branch* : traz o commit de uma branch para outra


<h3> Aula 31: Bisect- </h3>

git bisect start : inicia uma verificação que ajuda a encontrar o commit específico que introduziu um bug ou problema no repositório <br> 
git bisect bad *hash do commit* : indicar o commit onde o bug está presente. Isso é geralmente o commit mais recente onde você sabe que o código está com problemas <br> 
git bisect bad *commit-hash* : indicar o commit onde o código está livre do bug <br> 
Revisar Commits Automaticamente:

<b>O Git agora irá automaticamente selecionar um commit no meio do intervalo entre o commit bom e o commit ruim.
Você revisa esse commit para determinar se o bug está presente ou não.
Com base na revisão, você marca o commit como "bom" ou "ruim" usando os comandos git bisect good ou git bisect bad.
Repetir até Encontrar o Commit Problemático:

O Git continuará dividindo o intervalo pela metade até encontrar o commit que introduziu o bug.
Finalizar o Processo de Bissecção:

Uma vez que o Git encontre o commit problemático, você pode finalizar o processo de bissecção.<b> <br> 

git bisect reset


