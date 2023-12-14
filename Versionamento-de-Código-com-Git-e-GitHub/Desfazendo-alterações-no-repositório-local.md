# Desfazendo alterações no repositório local
Código utilizado durante a aula:
````
git init
rm -rf .git
````
remove do repositório tipo git.
````
git status
````
mostra que não tem nenhum arquivo no git.

- Para restaurar para a área de trabalho:
Se você modifica o arquivo localmente, por exemplo apaga todo o conteúdo do arquivo README.md e salva, 
você pode usar o comando 'git restore README.md', que irá restaurar deste a última modificação salva no git.

- Para alterar os dados do último commit:
Serve para alterar o nome do último commit.
````
git log
git commit -amend -m"Nome do commit"
````
Aqui realiza a alteração do nome do commit.
````
git commit --amend
````
Entra no editor para fazer alterações no commit de forma ampla. E para começar a editar pule a primeira linha do código, e caso deseje sair aperte o `esc` + `:` e digite __exit__ e pressione o enter.

- Para desfazer a mensagem do último commit:
temos três opções:
1. `git reset --soft`, coloca o commit na área de preparação;
2. `git reset --mixed`, reseta o arquivo para a área de trabalho;
3. `git reset --hard`, fará com que o arquivo seja apagado do commit, tanto da área de trabalho, quanto da área de preparação;

 `git reflog`, mostra o histórico das alterações.

Podemos também utilizar o comando `git reset 'nome da pasta/nome do arquivo'`, ou `git restore --staged 'nome da pasta/nome do arquivo'` para remover.
