# Trabalhando com Branches: Comandos úteis no dia a dia
Códigos utilizados na aula:

Para baixar arquivos remotos:
- `git fetch origin main`, baixa as alterações.
- `git diff main origin/main`, análisa as diferenças entre os arquivos já existente com o do remoto.
- `git merge origin/main`, traz as modificações do remoto para localmente.

> Para baixar apenas uma das branchs
````
git clone 'url' --branch teste --single branch
cd repo-remote
````
> suponhamos que você deletou um arquivo dentro da branch teste.
````
git stash
````
arquiva as mudanças, e os arquivos deletados reaparecem.
````
git stash list
git checkout -b teste-2
````
cria uma nova branch chamada de _teste-2_
````
git checkout teste
````
retorna para a branch _teste_.
- `git stash pop`, traz as alterações aqui e exclui as mais recentes, ou 
- `git stash apply`, mantém a alteração da lista para o uso posterior.
