<div align="center">

  <img src="./.github/assets/git-process.png" alt="Logo" height="500">
  <h1 align="center" style="color:gray"><strong>Git Cheat Sheet </strong></h1>

</div>
<div align="center">
    <p>| <a href="https://git-scm.com/doc"> Git Documentation</a> |</p>                    
</div>


#### Areas de trabalho do git (ilustração)
	- 'untracked files': porta de entrada de novos recursos.
	- 'stage area': arquivos adicionados para compor o commit.
	- 'local repository': contem os commits do repositório.   
  

#### Comandos:

*Manual das funcionalidades do comando*

```
	git <comando> --help

	git help <comando>
``` 


*Iniciar git no projeto*

```
	git init
``` 


*Mostrar conteúdo da 'untracked' e da 'stage' areas*

```
	git status
``` 


*Adicionar atualizações para a 'stage' area*

```
	git add .

	git add <nome-do-arquivo>
``` 


*Commitar contribuições*

```
	git commit -m "<descrição>"

	git commit -am "<descrição>"

	git commit --amend -m "<adicionar nova msg ao commit>"
``` 


*Mostrar 'commits' no repositório local*

```
	git log

	git log --graph

	git log --decorate

	git reflog
``` 


*Mostrar modificações nos arquivos*

```
	git show

	git show <hash-code>

	git shortlog -sn
``` 


*Mostrar diferenças entre modificações 'untracked', 'staged' ou remota*

```
	git diff
	
	git diff HEAD

	git diff --name-only

	git diff main origin/main
``` 


*Trabalhar com branchs*

```
	git branch

	git branch -r 

	git checkout -b <nome-do-novo-branch>

	git checkout <acessar-um-branch-pelo-nome>

	git branch -d <nome-do-branch-para-deletar>

	git branch -D <nome-do-branch-para-deletar-forçado>
``` 


*Endereço remoto geralmente origin*

```
	git remote -v
	
	git remote add <nome-do-apontamento> <url-do-apontamento-remoto>

	git remote rm <remove-apontamento-pelo-nome>
```


*Clonar repositório remoto*

```
	git clone
	
	git clone <git@github.com:Nome-do-Usuario/repositorio.git> <nome-para-novo-diretorio-local>
``` 


*Atualizar repositório local com alterações do repositório remoto*

```
	git pull

	git pull <remote-origin> <branch-remoto>
``` 


*Enviar commits do repositório local para repositório remoto*

```
	git push

	git push <remote-origin> <branch-remoto>

	git push <nome-da-tag>

	git push --tags
``` 


*Armazenar alterações em um diretório de trabalho a parte*

```
	git stash

	git stash list

	git stash show

	git stash pop
``` 


*Desfazendo alterações em 'untracked files'*

```
	git restore <nome-arquivo>

	git checkout <nome-arquivo>
``` 


*Desfazendo alterações na 'stage area' (index)*

```
	git restore --staged <nome-arquivo> 

	git rm --cached <nome-arquivo>

	git reset <nome-pasta-ou-arquivo>

	git reset HEAD
``` 


*Desfazendo coisas no 'repositório local'*

```
	git reset --soft <hashcode-do-commit> 

	git reset --mixed <hashcode-do-commit> 

	git reset --hard <hashcode-do-commit> 

	git revert <hashcode-do-commit>
``` 


*Apagar branch ou tag de 'repositório remoto'*

```
	git push origin :<nome-da-branch-remota> 

	git push origin :<codigo-da-tag-remota> 
```


*Configurar git no projeto ou global*

```
	git config --list

	git config --list --show-options

	git config --list --show-origin

	cat ~/.gitconfig

	git config --global user.name "<user-name>"

	git config --global user.email "<user-email>"

	git config --global alias.s status

	git config --global http.proxy http://00.00.000.00:0000
	
	git config --global https.proxy http://00.00.000.00:0000

	echo $http_proxy
	
	unset http_proxy

	unset https
	
	git config --global --unset http.proxy
	
	reset http_proxy
``` 


*Trabalhando com tags*

``` 
	git tag

	git tag -a 1.0.1 -m "Mensagem da nova tag" 
	
	git push origin main --tags
	
	git tag -d <codigo-da-tag-local>
``` 

##### Observações Gerais:

- use o git diff antes de fazer um commit
- o git reset usa o 'HashCode' anterior ao commit que se quer retirar
- o revert serve para retirar o commit sem perder as alterações
- HEAD, HEAD~1, HEAD~2... aponta partindo do registro mais recente



#### Autor:  [LinkedIn](https://www.linkedin.com/in/andrp)