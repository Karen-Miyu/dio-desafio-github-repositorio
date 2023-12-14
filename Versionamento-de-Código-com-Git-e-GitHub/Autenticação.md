# Autenticação
Código visto na aula:
````
git config --global user.name "nome do github"
git config --global user.email "email utilizado no github"
git config init.defaultBranch main
````
retorna para Branch (branching é a duplicação de um objeto sob controle de versão. [Fonte]( https://en.wikipedia.org/wiki/Branching_(version_control))) padrão.
````
git config --global --list
````
Vê as informações que você modificou.

````
git config credential.helper store
git config --global credential.helper
````
Para saber como suas credenciais estão armazenadas.
````
git config --global --show-origin credential.helper
````
Mostra aonde as credenciais estão armazenadas.
````
cat.gitconfig
````
Mostra os conteúdos dos seus arquivos.
````
cat .git-credentials
````
Mostra as credenciais armazenadas. 

## Autenticando via chave SSH
A chave SSH cria uma chave privata com a senha e outra chave pública.

````
.ls -a ~/.ssh
````
- ls - listas os arquivos;
- -a -retorna todos os arquivos;
- .ssh - é aonde se encontra a chave.
````
ssh -keygen -t ed25519 -C "user.email"
file:'enter' passphrase: 'Digite uma senha'
eval "$(ssh-agent -s)"
ssh -add ~/.ssh/id_ed25519
````
Feito isso já adicionou a chave privata a chave SSH agent.
````
cd ~/.ssh
ls
````
Lista as chaves privatas e públicas, respectivamente.
````
cat id_ed25519.pub
````
Mostrará o conteúdo da chave pública, permitindo copiar e colar lá, que gerará uma nova chave SSH no GitHub.

## 🔎Links
[Mais informações sobre Git](https://git-scm.com/doc)
