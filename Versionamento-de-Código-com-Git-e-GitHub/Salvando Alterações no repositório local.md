# Salvando Alterações no Repositório local 
Código utilizado durante a aula:
````
mkdir dio-resumos-git-e-github
cd dio-resumos-git-e-github
git init
git status
````
mostra a área de trabalho e a área de preparação.
````
touch README.md
````
cria um arquivo vazio.
````
git add README.md
````
coloca o arquivo na área de preparação (ainda não foi salvo no github).
````
git status
git commit -m"commit inicial"
````
salva o commit.
````
git log
````
mostra a realização do commit, com informações do autos e a data.
````
clear
````
limpa o terminal.
````
git status
````
mostra que está vazio.
````
touch resumos/resumo-aula1.md
git status
````
agora mostra que tem alguma coisa aqui.
````
echo resumos/>.gitignore
````
a pasta de resumo não é mais conhecida.
````
git status
echo >.gitignore
````
Retira a pasta resumos do gitignore.
````
git status
````
mostra de volta a pasta de resumos.

````
mkdir aulas
touch aulas/.gitkeep
````
para que o git reconheça os arquivos vazios.
````
git add .
````
adciona todos os arquivos na área de preparação.
````
git commit -m"----"
git log
````
mostra o que estiver em cima é o commit mais recente.

## Agora sobre modificações dos arquivos já comitados
Alterando o arquivo README.md
````
git status
````
Irá aparecer que o arquivo README.md foi modificado. E se você voltar com o arquivo antes da modificação, então o `git status` indicará que está tudo em ordem.
