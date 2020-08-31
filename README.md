# [Curso de Git e GitHub na pratica.](https://www.udemy.com/course/git-e-github-na-vida-real)

# Seção 2: Utilizando o Git numa interface gráfica com Visual Studio Code

## Aula 3 - Inicializando o repositório

### Conteúdo da aula:

Crie uma pasta em qualquer local do computador, abre o Terminal ou Git Bash dentro dela.
Inicialize o repositório local com o comando `git init`, criando o arquivo `README.md` e adicionando conteúdo ao mesmo para a aula.<br>

Também deve criar um repositório remoto no GitHub seguindo os seguintes passos:<br>
![Criando repositorio no GitHub](images/aula_3_3.png)
![Criando repositorio no GitHub](images/aula_3_4.png)

Copie o URL grifado e digite o comando `git remote add origin URL-copiado`, exemplo:
`git remote add origin git@github.com:rntjr/curso-git-github.git`<br>
![Configurando repositório remoto no local](images/aula_3_5.png)

Escreva algo dentro do arquivo README.md, digite no terminal `git add .` e depois `git commit -m "Commit Inicial do Projeto"`. O texto dentro de áspas pode ser qualquer coisa que preferir.<br>

## Aula 4 - Fazendo mudanças, vendo o diff e commitando

### Conteúdo da aula:

Toda e qualquer alteração realizada dentro de algum arquivo no repositório, você poder salvar seu estado de maneira individual (arquivo por arquivo) ou salvar seu conjunto, selecionando varios.
Para fazer isso no VSCode por exemplo, vá até a aba Source Controll e clique no + em cada arquivo, o mesmo será enviado para um novo detalhamento chamado `Staged Changes`.

É possivel visualizar o que foi alterado antes de commitar o arquivo. Basta na mesma aba selecionar o arquivo em `Staged Changes` e você verá do lado esquerda o ANTES e do lado direito o DEPOIS.

Após o commit, é possivel visualizar o que foi alterado no mesmo. Basta digitar `git diff codigo_commit`.

## Aula 5 - Trabalhando com Branches

### Conteúdo da aula:

A `Branch` é como um estado unico do projeto, que salva todos os arquivos e commits atuais. Você pode gera-lo a partir de uma branch especifica ou da branch atual que você está.

Para criar uma `Branch` com as mesmas caracteristicas que a sua atual, basta usar o comando `git branch -c nova-branch` ou `git checkout -b nova_branch`.

Para criar uma `Branch` através de outra em que você não esteja, baste usar o comando `git branch -C master nova-branch` ou `git checkout -b master nova_branch`.

**ATENÇÂO**: Com o `git checkout -b` você cria a branch caso não exista e automaticamente seleciona ela para trabalhar.

## Aula 6 - Adicionando um repositório remoto e subindo o código

### Conteúdo da aula:

Revisão do que foi ensinado na [Aula 3](#aula-3---inicializando-o-repositório) como criar repositório remoto.

Para subir todas as alterações salvas, basta usar o comando `git push -u origin branch`, e no lugar do branch, troque para o que vc está enviando.

## Aula 7 - Sincronizando com o repositório remoto

### Conteúdo da aula:

Para sincronizarmos o codigo da nossa branch atual com a branch remota, caso houver atualizações de novos commits, basta usar o comando `git pull -f origin branch`. Ou você pode clicar no icone loop ao lado da branch no canto inferior esquerdo do VSCode.

## Aula 8 - Vendo o Histórico de commits

### Conteúdo da aula:

Baixado a extensão [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory). Abra o painel de busca com `Ctrl + P` e digite `Git: View History (git log)`.

A extensão mostra o historico dos commits dentro do repositório local e remoto.

## Aula 9 - Merge na Pratica

### Conteúdo da aula:

Crie uma nova branch usando como referencia sua branch principal (master), selecione-a e modifique algum arquivo. Logo prossiga com as mesmas instruções da [Aula 3](#aula-3---inicializando-o-repositório) e commit. 

O merge funciona da seguinte forma. Você deve estar em uma branch e trazer os novos commits para ele. Sendo assim, vamos fazer:
Selecione a branch principal (master) `git checkout master` e execute o comando `git merge branch-nova`. 

Após o merge, os commits feitos na branch-nova serão lançados no master. Logo após você pode visualizar no [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory) a sequencia dos commits.

Depois do merge feito localmente, apenas realize o push como a [Aula 6](#aula-6---adicionando-um-repositório-remoto-e-subindo-o-código) ensina.

## Aula 10 - Rebase na Pratica

### Conteúdo da aula:

O merge sempre gera um novo commit no historico da branch. Já o rebase deixa o histórico linear e mais simples, mas alguns commits são reescritos.

Um otimo workflow para utilzar o rebase seria atualizar os dados da sua master `$ git checkout master` `$ git pull --rebase origin master`. Os commits locais da master irão ficar linearizados.
Logo então você irá mudar para a sua branch `$ git checkout sua-branch` `$ git pull --rebase origin sua-branch` caso a branch já exista.
Então mesclar com rebase a master na sua branch
`$ git rebase master`.

# Seção 3: Soluções e comandos do cotidiano

## Aula 12 - Rebase na Pratica

### Conteúdo da aula: