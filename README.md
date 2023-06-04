README.md

Módulo de Git/Github e o material criado a partir das aulas:

<h4>#1
O que é, para que serve, como funciona?</h4>

O Github surgiu a partir de uma necessidade do programador conseguir identificar as alterações realizadas, facilitando a visualização de erros e recuperação do código antes disso acontecer.

Possibilitar que um ou mais programadores atuem no mesmo código em locais diferentes e ao mesmo tempo.


<h4>#2
Instalando o GIT</h4>

git --version 
Exibe a versão do git instalado no pc.


<h4>#3
Configurando o GIT</h4>

Alterando nome no GIT

git config --global user.name "Nome desejado"

Definindo e-mail

git config --global user.email "informar o e-mail desejado"


Indicar editor utilizado

git config --global core.editor editor utilizado


Comando para exibir os dados cadastrados:

git config user.name

git config user.email

git config core.editor

Como trazer todas as informações cadastradas:

git config --list


<h4>#4
Iniciando um repositório</h4>

Comandos básicos para uso no prompt de comando:

Acessar pastas - 
Identifique a pasta desejada e insira o comando --> cd Nome da pasta/

Verificar quais itens existem dentro da pasta -
	- dir 
	- tree/f

Retornando as pastas -
"cd .."


Criando uma pasta via prompt -
mkdir nome da pasta


Criando um repositório -
git init



<h4>#5
Branch, README e Commit</h4>

Commit - ação que consiste em atualizar o código com novas informações é indicar através de comentários qual foi a modificação realizada.

README - local onde se resume o projeto e o que foi realizado. Geralmente acompanha instruções, comentários e etc.

git status - traz informações sobre as últimas atualizações e modificações realizadas dentro da pasta.



Git add -A - ao fazer isso o arquivo passa a ser reconhecido dentro do terminal:


Como fazer o commit:

Terminal --> git commit -m "Inserir o comentário sobre o que foi feito";

Git log - traz o autor e data do commit e o comentário que foi inserido.


<h4>#6 Revertendo alterações
</h4>

Git branch - mostra em qual branch está no momento.

Para reverter modificações utiliza-se o git reset. Existem e possibilidades de resetar:

	- Soft: retorna para o commit indicado, mas preserva os arquivos criados anteriormente no caso de querer utilizá-lo futuramente (mais recomendado trabalhando em equipe).

	- Mixed: faz o mesmo do soft, mas será necessário commitar novamente os arquivos.
	
	- Hard: apagará tudo o que foi feito no arquivo commitado.


Comando:

git reset --resetar desejado [copiar o commit que deseja realizar a ação]


<h4>#7 
Trabalhando com diferentes Branches
</h4>

Como criar uma branch?

"git branch [nome da nova branch desejada]"


Como alternar entre as branchs?

"git checkout [nome da branch desejada]"



<h4>>#8 
Diferença entre arquivos</h4>

	- git diff > irá detalhar onde e quais alterações foram realizadas;

	- git diff --name-only > trará apenas as pastas onde houveram modificações;

	- git diff "nome do arquivo" > trará apenas as modificações realizadas no arquivo indicado;

	- git checkout HEAD -- "nome do arquivo" > irá desconsiderar as alterações que foram feitas na pasta;



<h4>>#9
Criando um repositório no GitHub</h4>

Aula de instruções para acessar o Github.

<h4>#10
Conectando repositório local ao remoto</h4>

Ao seu criar o repositório no github, a própria plataforma dará algumas opções. 
No caso de um repositório já existente, indica-se o seguinte comando:

"git remote add origin https://github.com/brianmduarte/modulogit.git"


Para visualizar se o processo funcionou:

"git remote" 

Para mais detalhes:
"git remote -v"

Trará duas opções:

Fetch - puxar as informações do servidor remoto e os leva para o repositório local (gitHub)
Push - levar as informações do repositório local para o servidor remoto(gitHub)



Exemplo de push:

Git push "nome dado ao arquivo" "branch desejada"

No exemplo da aula, foi feito da seguinte maneira - git push origin master

 
<h4>#12
Ignorando arquivos do repositório (gitignore)
</h4>

Esse processo consiste em preservar alguns arquivos aos quais o programador não quer que vá para o repositório. Para isso, é necessário criar um arquivo chamado ".gitignore" e dentro dele inserir quais arquivos não serão exibidos no repositório.

Exemplo:


<h4>#13
Revertendo sem perder o código (Revert)
</h4>
Essa funcionalidade permite reverter as inclusões realizadas revertendo a ação feita. A sua estrutura funciona da seguinte maneira:

git revert --no-edit [chave do commit de alteração] 3ddc5755a7754e70aefb3b3a38f1ff29644f5d5a

Feito isso, o terminal trará o processo reverso e indicará qual foi a mudança.


<h4>#14
Deletando branches locais e remotos</h4>

Para adicionar branches remotamente:

git push origin (ou outro nome dado) nome da branche desejada


Para deletar uma branche remotamente é necessário inserir a seguinte estrutura:

git push origin (ou outro nome dado) :nome da branche desejada


Para deletar uma branch local:

git branch -d "nome da branch a ser excluída"

<h4>#15
Puxando alterações de outras pessoas (pull)</h4>

Para trazer alterações ou inclusões do repositório, utiliza-se o "pull". 

Igualmente ao push, o pull possui a mesma estrutura:

"git pull origin master"



<h4>#16
Clonando repositórios remotos</h4>


Estrutura para clonar repositórios (geralmente utilizado para clonar repositório próprio):

git clone [url de onde o repositório se encontra]

Importante: apesar de ser possível clonar o repositório, não é possível fazer alterações diretas, apenas contribuições que poderão ser aceitas ou não pelo autor.

<h4>#17
Contribuindo com outros repositórios (fork / pull)</h4>


Fork - permite copiar um repositório de outro autor para realizar contribuições. Essa opção está disponível dentro do próprio Github, basta procurar o projeto ao qual se deseja contribuir. 


Após realizar as alterações desejadas, o processo é o mesmo; adicionar as mudanças, fazer o commit, fazer o push para o repositório. 

Feito isso, deve-se solicitar a opção "New pull request". Essa funcionalidade enviará as mudanças para que o autor original aceite ou não tais modificações.
