# Sequência de Comandos e instruções

## Criar SSH para GitHub em cada máquina:

### digitando no gitbash:

ssh-keygen -t ed25519 -C bftcorporations@gmail.com
cd /c/Users/YourUser/.ssh/
ls
cat id_ed25519.pub

Copie o texto gerado >> abra o github >>
No seu perfil clique em settings >> 
clique em ssh and gpg >> Clique em "New SSH" >>
Crie um título da chave >> Cole o texto da chave
que você copiou >> clique em "add ssh", pronto!

### Novamente no gitbash, digite:

ssh-add id_ed25519
eval $(ssh-agent -s)


## Comandos para trabalhar com repos locais:

git init  : Inicializa o git
git status : Verifica estado atual
git add <file> ou git add * : Adiciona arquivos
git status : Verifica estado atual
git commit -m "msg..." : Commita arquivos
git status : Verifica estado atual

## Comandos para subir ao servidor remoto (GitHub):

git remote add origin git@github.com:[LINK SSH]
git branch -M main
git push -u origin main

ou...

git remote add origin git@github.com:[LINK SSH]
git push origin master

git remote -v

## Para adicionar um email e username ao git:

git config --global user.email "[SEU EMAIL]"
git config --global user.name "[SEU USERNAME]"
git config --list : para ver as configurações
