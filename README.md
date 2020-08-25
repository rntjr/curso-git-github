# [Curso de Git e GitHub na pratica.](https://www.udemy.com/course/git-e-github-na-vida-real)

## Aula 3 - Inicializando o repositório

### Conteúdo da aula:

Crie uma pasta em qualquer local do computador, abre o Terminal ou Git Bash dentro dela. Você verá algo parecido com isso:
![Git Bash Aberto](images/aula_3_1.png)

Inicializando o repositório local com o comando `git init`, criando o arquivo `README.md` e adicionando conteúdo ao mesmo para a aula.
![Iniciando repositório local e criando o LEIA-ME](images/aula_3_2.png)

Também deve criar um repositório remoto no GitHub seguindo os seguintes passos:
![Criando repositorio no GitHub](images/aula_3_3.png)
![Criando repositorio no GitHub](images/aula_3_4.png)

Copie o URL grifado e digite o comando `git remote add origin URL-copiado`, exemplo:
`git remote add origin git@github.com:rntjr/curso-git-github.git`
![Configurando repositório remoto no local](images/aula_3_5.png)

Escreva algo dentro do arquivo README.md, digite no terminal `git add .` e depois `git commit -m "Commit Inicial do Projeto"`. O texto dentro de áspas pode ser qualquer coisa que preferir.
