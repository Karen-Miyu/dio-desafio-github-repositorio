# Criando e clonando repositório
Código usado na aula:
````
mkdir repo-local
cd repo-local
git init
````
inicializa a pasta como tipo git.
````
cd .git
ls
cat config
git clone 'link do repositório' 'nome opcional'
````
Cria um clone localmente com o nome que deseja, ou não.
````
cd repo-clonado
cat config
git remote -v
cd ..
git remote add origin 'link do repositório clonado'
cd .git
cat config
````
ou também é possível clonar apenas uma branch especifica:
`git clone 'URL' --branch feature-1 --single-branch`

## Informações adicionais sobre a criação de um novo repositório no GitHub
- READ ME -> serve para descrever o projeto, ou quais as ferramentas utilizadas no projeto;
- .gitignore -> Oculta os arquivos selecionados;
- license -> Você define como as pessoas vão poder mexer no seu código, principalmente se for público.
