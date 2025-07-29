<div align="center">

  <img src="./.github/assets/git-process.png" alt="Logo" height="500">
  <h1 align="center" style="color:red"><strong>Git Cheat Sheet</strong></h1>

</div>
<div align="center">
    <p>| <a href="https://git-scm.com/doc"> Git Documentation</a> |</p>                    
</div>


#### Setores
	- area de trabalho (untracked files) porta de entrada de novas funcionalidades no sistema.
	- 'stage area', arquivos adicionados(add) para compor o commit.
	- 'local repository', contem commits enviados e recebidos do repositório remoto.   


- commands: init, status, add, commit, log, diff, reset, branch, checkout, remote, pull, fetch, merge, remote, stash, shortlog, show, revert  

- properties: HEAD, HEAD~1, HEAD~2, --soft, --hard, --help, --decorate, --author="Nome", --graph, -sn, --name-only
 		  

#### Comandos:

	git commit -am ('para arquivos que já existiram no stage)

	git clone git@github.com:And-P/github-course.git new_dir
	git log --decorate (--author="Nome", --graph)

	git shortlog (-sn)
	
	git show "HashCode"
	git diff (--name-only)
	git checkout -b novo-branch
	git branch
	git stash (apply, list, show, drop, clear, create, store)
	git config --global alias.s status 
	
--- Desfazendo Coisas no Git 

	git checkout "Nome_Arquivo" (retira modifica��o do arquivo ainda na �rea de trabalho(unstaged file))
	git reset HEAD (retira o arquivo do stage-area, para depois usar o comando git checkout e retirar as altera��es indesej�veis) 
	git reset "HashCode"(--soft, --mixed, --hard) retira commits
	git revert "Hash-Code" (hash do commit a ser removido)
	
-- Branch
	
	git branch (lista os branchs disponíveis)
	git checkout -b novo-branch (cria novo-branch)
	git checkout novo-branch (entra em novo-branch)
	git branch -D nome-branch (deleta nome-branch)

-- Tag
	git tag (mostra tags geradas)
	git tag -a 1.0.1 -m "Mensagem link" (cria tag)
	git push origin master --tags

--- Repositorio Remoto - GitHub
	obs: antes, configurar a chave SSH 

	git remote add origin git@github.com:And-P/Projeto.git
	git remote -v ('lista os repositorios remotos dispon�veis')

	git push -u origin master ('remoto' - 'branch'- o -u crackeia o endere�o, depois � s� digitar git push como atalho)	

	git clone git@github.com:And-P/github-course.git Pasta_Clone

--- GitHub - Fork
	Fazer um fork(no GitHub) de projetos de outros dom�nios, traz uma c�pia do projeto para meu reposit�rio remoto. 

--- .gitignore 
   
	- criar um arquivo .gitignore
	
	O .gitignore � um arquivo de texto, onde anotamos o que deve ser ignorado pelo git. 
	- *.json (*.extensao-do-arquivo): ignora todos os arquivos com tal extens�o

	- nome_do_arquivo : ignora o arquivo especificado
	- um reposit�rio, no https://github.com/github/gitignore, especifica padr�es para desenvolvimento em varias plataformas(java, etc...) 

----- Apagando Tags e Branchs em Reposit�rios Remotos

	git tag -d cod-tag (ex. 1.0.1 - s� apaga local)
	git push origin :1.0.0 (apaga tag remota)
	git push origin :master (apaga branch remoto)


----- Observa��es Gerais:

- falando de diff: "sempre use o git diff antes de fazer um commit".
- git reset: "usa-se a HashCode anterior ao commit que se quer retirar"
- revert: "ele retira as altera��es, informa na log o revert e n�o apaga o commit de origem do problema da log - o revert serve pra resetar o arquivo sem perder as altera��es que foram feitas"


