# Trabalhando com Branches: criando, mesclando, deletando e tratando conflitos
Código utilizado na aula:
````
git commit -m"commit 0"
git log
echo "#commit-0-branch-main" > commit-0-branch-main.txt
git add .
git commit -m"commit 1"
git log
echo "#commit-1-branch-main" > commit-1-branch-main.txt
git add .
git commit -m"commit 2"
git log
echo "#commit-2-branch-main" > commit-2-branch-main.txt
git add .
git checkout -b teste
````
alterna para essa nova branch chamada de _teste_.
````
echo "#commit-3-branch-main" > commit-3-branch-main.txt
git add .
git commit -m"commit 3"
git checkout main
````
retorna para a branch _main_, e as alterações feitas na branch teste não aparece aqui.
````
git branch -v
````
Mostra todos os últimos commits realizados nas branchs.
Se quiser mesclar duas branch você pode utilizar o seguinte comando: `git merge teste`, e caso queira deletar uma branch: `git branch -D teste`

## Conflito de versionamento
Ocorre quando alguém altera remotamente, e você também faz alterações localmente e tenta enviar para o remoto, mas não consegue devido ao conflito entre os dois commits.

````
git push origin main
````
Vai aparecer que está conflitando.
````
git pull
````
Abra o arquivo e veja as alterações feita remota e localmente. Isso permite escolha qual das alterações se deseja deixar.
````
git add .
git commit -m"commit após o conflito"
git push origin main
````
Já realizou as alterações no github.
