# Desafio-Dio.me
## _Criando uma chave ssh_


Com o Github instalado acesse o gitbash no windows

Comandos :ssh-keygen -t ed25519 -C "e-mail que usa no github" enter

$ ssh-keygen -t ed25519 -C "e-mail que usa no github"

Generating public/private ed25519 key pair.

Enter file in which to save the key (/c/Users/nome usuario/.ssh/id_ed25519): enter (local onde a chave vai ser gerada)

Created directory '/c/Users/nome usuario/.ssh'.

Enter passphrase (empty for no passphrase): criar uma senha (Quando digita a senha não aparece no comando é normal)

Enter same passphrase again:

Após criar a senha vai mostrar a mensagem abaixo


Your identification has been saved in /c/Users/nome usuario/.ssh/id_ed25519

Your public key has been saved in /c/Users/nome usuario/.ssh/id_ed25519.pub

The key fingerprint is:

SHA256:QPLdlKPVwRbFw30W6P6Q2JrYqE/f3AUJHbIADSTlU1E e seu e-mail

The key's randomart image is:
+--[ED25519 256]--+

|    . oo=+=*E*+o.|

|     + + +=.+=+.+|

|      o +o.o+ .o.|

|       ...   o . |

|        S   + +  |

|           . = . |

|         .+ o o .|

|        .o.+o ...|

|       .o. . o . |

+----[SHA256]-----+

Mostra onde a chave foi salva

Your public key has been saved in /c/Users/nome usuario/.ssh/id_ed25519.pub

No comando

Usuário@Usuário MINGW64 ~/Desktop 

digite esse comando: $ cd '/c/Users/Usuário/.ssh/' enter

imprime esse comando Usuário@Usuário MINGW64 ~/.ssh

$ Usuário@Usuário MINGW64 ~/.ssh

$ ls (digitando esse comando mostra a chave criada publica e privada)

id_ed25519  id_ed25519.pub

comando  cat  visualiza conteudo dessas chaves

Usuário@UsuárioMINGW64 ~/.ssh

$ cat id_ed25519.pub 

Irá aparecer uma chave com seguencia enorme de numeros e letras mais o email cadastrado ssh-ed25519 (....)+e-mail (essa chave publica)

Logado no site do Github:
 
 Na aba SSG  ad GPG KEYS; new ssh; sshkey/add; coloque o title onde a chave foi originada; e cole a chave 

Ainda git windows

Usuário@Usuário MINGW64 ~/.ssh

Comando pwd mostra o caminho completo que fizemos

Usuário@Usuário MINGW64 ~/.ssh

$ eval "$(ssh-agent -s)"

Agent pid 320(esse numero costuma variar)

Usuário@Usuário MINGW64 ~/.ssh

$ ssh-add id_ed25519

Enter passphrase for id_ed25519:  ( tem que digitar a senha criada aqui)

Identity added: id_ed25519 (e-mail)

### Clonar repositorio

Usuário@Usuário MINGW64 ~/workspace/teste

$ git clone (cole após esse comando o code em formato ssh na aba code do repositorio) enter

Cloning into 'aprendiz-de-tecnologia'...

Enter passphrase for key '/c/Users/usuario/.ssh/id_ed25519':

Enter passphrase for key '/c/Users/usuario/.ssh/id_ed25519':

remote: Enumerating objects: 6, done.

remote: Counting objects: 100% (6/6), done.

remote: Compressing objects: 100% (3/3), done.

remote: Total 6 (delta 0), reused 0 (delta 0), pack-reused 0

Receiving objects: 100% (6/6), done.

### Observação: consegui clonar na máquina mas solicitou a senha. Tenho que estudar mais.

 
### _Algumas anotações importantes:_

Quando ja tem uma chave criada na sua maquina, vc não poderar simplesmente copiar um link e usar o git clone(urls). Quando tem um ssh fixo na maquina
tem que usar o caminho ssh no git

Passar pro agent a chave privada: toda vez que chegar uma criptografia com essa chave ele vai usar a nossa chave privada para criptografar
lembrar de criar uma pasta no sistema gif bash.

Token de acesso pessoal: gera um token no github e guarda lo na maquina : no github na guia developper settings, personal acess tokens,generetion new token, pode
colocar uma data de validade, opçao repo,generation token. vai ser criada uma chave deve copia la em um lugar seguro.

### Curso feito na Dio.me com os professores Venilton Falvo Jr. e Otavio Reis Perkles

## links úteis

[sintaxe basica markdown](https://www.dio.me/)



