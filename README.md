# Git - Versionamento de Código.

# **O que é um repositório?**

<aside>
💡 Basicamente, um repositório é um local de armazenamento do nosso código-fonte. É nele que nossos códigos serão armazenados e versionados. Com o GIT, existem dois tipos de repositórios:

</aside>

<aside>
💡 Local: Um repositório onde os códigos são armazenados e versionados localmente, sem a necessidade de um serviço externo;

</aside>

<aside>
💡 Remoto: Um repositório onde os códigos são armazenados e versionados remotamente, utilizando serviços como Github, Bitbucket ou Gitlab (que serão vistos posteriormente).

</aside>

# **Estágios de um arquivo no .git:**

<aside>
💡 Um arquivo gerenciado pelo git possui três estados e o entendimento destes são fundamentais. Basicamente, os estados são: Modificado: Um arquivo possui o estado de modificado quando há alguma alteração, seja ele em seu conteúdo, adicionado ou removido; Preparado: Um arquivo possui o estado de preparado quando ele é adicionado ao versionamento utilizando o comando git add. É com este comando que adicionamos o arquivo e permitimos que o git o versione; Consolidado: Após serem modificados (adicionados, removidos ou alterados) e preparados (adicionados ao versionamento), o último passo de um arquivo é sua consolidação. Neste ponto, ao utilizamos o comando git commit, estamos salvando as alterações do arquivo e o versionando, mantendo um histórico de suas alterações.

</aside>

![os-3-estados-de-um-arquivo-no-git.png](https://www.ramon.pro.br/wp-content/uploads/2017/03/os-3-estados-de-um-arquivo-no-git.png)

---

# **Utilizando HTTPS para comunicação**

<aside>
💡 O protocolo HTTPS é o mais fácil e prático para ser utilizado no Github. Para isso, não há a necessidade de nenhuma configuração adicional. Apenas com o link do repositório é possível realizar esta comunicação, desde que você possua permissão de acesso ao repositório.

</aside>

# Git - Configuração do usuário

**Configurações do usuário do git:**

**Para que os commits feitos possuam nosso nome e e-mail em seu escopo, precisamos realizar esta configuração. Para isso, no terminal (macOS ou Linux) ou Git Bash (Windows), digite os seguintes comandos:**

```
git config --global user.name "seu_nome"
```
```
git config --global user.email "seu_email"
```
# Git - Comandos

**Inicia o arquivo (repositorio)".git/" para controlar a pasta:**

```
git init
```

**Verifica o status de todos os arquivos dentro do repositório e é responsável por validar os arquivos modificados dentro do projeto. Em vermelho ele mostra os arquivos modificados e em verde mostra os arquivos que foram adicionado pelo "git add":**

```
git status
```

**Ele é responsável por colocar o arquivo modificado em uma área segura:**

```
git add
```

**Ele é responsável por colocar todos os arquivos em uma área segura:**

```
git add .
```

**Ele é responsável por criar uma nova versão do projeto com as referências do criador:**

```
git commit -m "texto_da_modificação"
```

**Verificar histórico de modificações e comentários:**

```
git log
```

**Verificar histórico de modificações e comentários com informações mais resumidas:**

```
git log --oneline
```

**Cria uma nova branch ou ramo:**

```
git checkout -b <nome_da_branch>
```

**Muda de branch /ramo:**

```
git checkout <nome_da_branch>
```

**Consultar projeto com base nos commits passados:**

```
git checkout <ID-do-commit>
Ex: git checkout <b879020>
```

**Retornar para o último ponto dos commits:**

```
git checkout main
```

**Adiciona a branch atual o conteúdo de outra branch:**

```
git merge: <nome_de_branch>
```

**Baixa o projeto do repositório:**

```
git clone: <url>
```

**Baixa o projeto do repositório de uma branch específica:**

```
git clone -b <nome_da_branch> <url_do_repositório>
```

**Envia as alterações para o repositório:**

```
git push
```

**Puxa as alterações do repositório:**

```
git pull
```

**Puxa as alterações de um repositório especifico:**

```
git pull origin <branch>
```

**Envia o repositório local para o repositorio online do github. Este comado é quando você precisa fazer a ligação com o repositório online do github:**

```
git remote add origin "url" do repositório
```

**É utilizado quando queremos enviar a branch que criamos para o repositório remoto. Isso criará um “elo” entre o seu repositório local e o repositório remoto:**

```
git push origin "branch"
```

**Abri um repositório clonado diretamente no visual code através do terminal:**

```
code . <caminho-do-repositório>
```

**Ele cria um novo repositório caso não tenha nenhum criado**

```
echo "#nome_do_repositorio" >> README.md
```

**Ele lista os arquivos que possuem dentro do diretório:**

```
ls
```

**Ele lista detalhadamente mostrando hora, mês e data dos arquivos do repositório:**

```
ls -l
```

**Ele desfaz o que foi feito em um commit e cria um novo commit para o repositório, porén ele não exclui o commit desfeito do histórico.**

```
git revert <identificador do commit>
```

**Deleta o commit mas as alterações futuras do código ainda permanece, pois esse comando é utilizado quando há uma quantidade muito grande de commits feitos sem necessidade.**

```
git reset <identificador do commit>
```

**Deleta o commit e também as alterações feitas no código de forma parmanente, muito cuidado com essa opção, pois uma vez deltada por esse comando, não há possibilidade de recuperação.**

```
git reset <identificador do commit> --hard
```

**Ele é um editor de texto para terminal e consegue adicionar um arquivo um aquivo dentro do repositório.**

```
nano "index.html"
```

**Baixa o conteúdo remoto e não altera o estado do repositóri local.**

```
git fetch
```

**Entra em uma determinada pasta:**

```
cd <nomw_diretório>
```

**Apagar uma branch:**

```
git branch -d <branch>
```

**Ignorar arquivos ou pastas que contenham dados sensíveis é necessário criar um arquivo no repositório chamado “.gitignore”, dentro dele adicionando os nomes dos arquivos que você não quer que seja rastreado pelo .git:**

```
touch gitignore
```
