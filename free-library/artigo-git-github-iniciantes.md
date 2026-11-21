# Git e GitHub para iniciantes: instalação, configuração e primeiro commit

O **Git** é uma ferramenta usada para controlar versões de arquivos. Com ele, podemos acompanhar alterações, recuperar versões antigas e trabalhar com segurança em projetos de programação.

O **GitHub** é uma plataforma online que armazena repositórios Git e facilita o compartilhamento, a colaboração e o backup de projetos.

Neste tutorial, você aprenderá passo a passo a:

- instalar o Git;
- abrir e usar o Git Bash;
- configurar seu nome e e-mail;
- entender os principais conceitos do Git;
- criar um repositório local;
- fazer o primeiro commit;
- criar um repositório no GitHub;
- conectar o projeto local ao GitHub;
- enviar arquivos com `push`;
- baixar alterações com `pull`;
- clonar projetos;
- usar um arquivo `.gitignore`;
- corrigir erros comuns.

O conteúdo foi preparado para pessoas que nunca usaram Git ou GitHub.

---

## 1. Git e GitHub são a mesma coisa?

Não. Eles são ferramentas diferentes, mas trabalham muito bem juntas.

### Git

O Git é um programa instalado no computador. Ele controla as versões dos arquivos de um projeto, mesmo quando você está trabalhando sem internet.

Com o Git, você pode:

- registrar alterações;
- criar pontos de restauração;
- comparar versões;
- criar ramificações para testar ideias;
- desfazer alterações;
- colaborar com outras pessoas.

### GitHub

O GitHub é um serviço online. Ele pode armazenar seus repositórios Git na nuvem e disponibilizá-los para você ou para sua equipe.

Com o GitHub, você pode:

- guardar projetos online;
- compartilhar código;
- trabalhar em equipe;
- abrir solicitações de alteração, chamadas de pull requests;
- acompanhar problemas, chamados de issues;
- criar um portfólio público.

Uma forma simples de entender é:

```text
Git    = ferramenta de controle de versões no computador
GitHub = plataforma online para hospedar repositórios Git
```

---

## 2. O que é um repositório?

Um **repositório** é uma pasta controlada pelo Git.

Dentro dela ficam:

- os arquivos do projeto;
- o histórico de alterações;
- as informações de configuração do Git;
- os commits realizados.

Podemos ter dois tipos principais:

### Repositório local

Fica no seu computador.

```text
Seu computador
└── projeto-meu-site
    ├── index.html
    ├── style.css
    └── histórico Git
```

### Repositório remoto

Fica em um serviço online, como o GitHub.

```text
Internet
└── github.com/seu-usuario/projeto-meu-site
```

O fluxo mais comum é:

```text
editar arquivos
      ↓
git add
      ↓
git commit
      ↓
git push
      ↓
GitHub
```

---

## 3. Instalando o Git no Windows

Acesse o site oficial:

[https://git-scm.com/](https://git-scm.com/)

Baixe o instalador para Windows e execute o arquivo baixado.

Durante a instalação, você pode manter as opções padrão. Para iniciantes, é recomendável observar principalmente estas opções:

- usar o Git pelo Git Bash e pelo terminal do Windows;
- manter o editor padrão sugerido ou escolher o Visual Studio Code;
- usar o nome padrão da branch inicial;
- permitir que o Git ajuste os finais de linha automaticamente.

Na maioria dos casos, basta clicar em **Next** até a instalação ser concluída.

Depois, abra o menu Iniciar e procure por:

```text
Git Bash
```

Se o Git Bash abrir, a instalação foi concluída.

Para conferir a versão instalada, execute:

```bash
git --version
```

Um resultado possível é:

```text
git version 2.45.0
```

O número pode ser diferente conforme a versão instalada.

---

## 4. Instalando o Git no macOS

Você pode baixar o Git pelo site oficial ou instalar ferramentas de desenvolvimento da Apple.

Depois da instalação, abra o aplicativo **Terminal** e execute:

```bash
git --version
```

Se o macOS solicitar a instalação de ferramentas adicionais, confirme e aguarde a conclusão.

---

## 5. Instalando o Git no Linux

Em distribuições baseadas em Ubuntu ou Debian, abra o terminal e execute:

```bash
sudo apt update
sudo apt install git
```

Depois, verifique a instalação:

```bash
git --version
```

Em outras distribuições, use o gerenciador de pacotes correspondente.

---

## 6. Conhecendo o Git Bash

O **Git Bash** é um terminal instalado junto com o Git no Windows. Ele permite usar comandos do Git e vários comandos tradicionais de sistemas Linux e macOS.

Ao abrir o Git Bash, você verá uma linha parecida com esta:

```text
usuario@computador MINGW64 ~
$
```

O símbolo `$` indica que o terminal está esperando um comando.

### Comandos básicos do terminal

#### Mostrar a pasta atual

```bash
pwd
```

#### Listar arquivos e pastas

```bash
ls
```

Para mostrar também arquivos ocultos:

```bash
ls -la
```

#### Criar uma pasta

```bash
mkdir meu-projeto
```

#### Entrar em uma pasta

```bash
cd meu-projeto
```

#### Voltar uma pasta

```bash
cd ..
```

#### Criar um arquivo vazio

```bash
touch README.md
```

#### Limpar a tela

```bash
clear
```

No Windows, o comando abaixo também pode ser usado para limpar a tela:

```bash
cls
```

#### Voltar para a pasta pessoal

```bash
cd ~
```

> Os comandos do terminal diferenciam letras maiúsculas de minúsculas em muitos sistemas. Por isso, `Projeto` e `projeto` podem ser nomes diferentes.

---

## 7. Configurando o Git pela primeira vez

Antes de fazer commits, configure seu nome e seu e-mail. Essas informações ficam associadas aos registros que você criar.

Use um nome que identifique você:

```bash
git config --global user.name "Seu Nome"
```

Depois, informe seu e-mail:

```bash
git config --global user.email "seu-email@exemplo.com"
```

Exemplo:

```bash
git config --global user.name "Maria Silva"
git config --global user.email "maria@example.com"
```

Confira as configurações:

```bash
git config --global --list
```

Para verificar somente o nome:

```bash
git config --global user.name
```

Para verificar somente o e-mail:

```bash
git config --global user.email
```

### Sobre o e-mail usado nos commits

Você pode usar o mesmo e-mail da sua conta do GitHub. Isso ajuda o GitHub a associar os commits ao seu perfil.

Se preferir não expor seu e-mail pessoal, o GitHub oferece um endereço de e-mail `noreply`. Nesse caso, configure no Git o endereço fornecido pelas configurações da sua conta GitHub.

---

## 8. Escolhendo o nome da branch principal

A branch principal costuma ser chamada de `main`. Para usar esse nome como padrão em novos repositórios, execute:

```bash
git config --global init.defaultBranch main
```

Isso faz com que o comando `git init` crie a branch inicial com o nome `main`.

---

## 9. Criando um projeto de exemplo

Vamos criar um pequeno site para praticar.

No Git Bash, execute:

```bash
mkdir meu-primeiro-repositorio
cd meu-primeiro-repositorio
```

Crie um arquivo chamado `index.html`:

```bash
touch index.html
```

Se o comando `touch` não funcionar no seu ambiente, crie o arquivo pelo Visual Studio Code ou pelo Explorador de Arquivos.

Abra a pasta no VS Code, caso ele esteja instalado:

```bash
code .
```

Coloque este conteúdo em `index.html`:

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Meu primeiro repositório</title>
  </head>
  <body>
    <h1>Meu primeiro projeto com Git</h1>
    <p>Estou aprendendo a controlar versões.</p>
  </body>
</html>
```

Salve o arquivo.

---

## 10. Criando um repositório local com `git init`

Dentro da pasta do projeto, execute:

```bash
git init
```

O Git exibirá uma mensagem informando que um repositório vazio foi criado.

Esse comando cria uma pasta oculta chamada `.git`. Ela guarda o histórico e as configurações do projeto.

Confira os arquivos ocultos:

```bash
ls -la
```

Você verá algo parecido com:

```text
.
..
.git
index.html
```

Não edite manualmente os arquivos dentro da pasta `.git`. O Git gerencia esses arquivos automaticamente.

---

## 11. Consultando o estado com `git status`

O comando mais importante para iniciantes é:

```bash
git status
```

Ele mostra o estado atual do repositório.

Como ainda não fizemos um commit, o resultado poderá indicar que o arquivo `index.html` não está sendo acompanhado pelo Git.

A expressão **untracked files** significa **arquivos não rastreados**.

```text
Untracked files:
  index.html
```

Isso não significa que o arquivo está com problema. Significa apenas que o Git ainda não foi instruído a acompanhá-lo.

---

## 12. A área de preparação e o comando `git add`

O Git usa uma área intermediária chamada **staging area** ou **área de preparação**.

Antes de criar um commit, você escolhe quais alterações deseja incluir.

Para adicionar um arquivo específico:

```bash
git add index.html
```

Para adicionar todos os arquivos modificados e novos da pasta atual:

```bash
git add .
```

Depois, confira o estado novamente:

```bash
git status
```

O arquivo deverá aparecer em uma seção parecida com:

```text
Changes to be committed:
  new file:   index.html
```

### Qual é a diferença entre `git add index.html` e `git add .`?

O primeiro adiciona apenas o arquivo indicado:

```bash
git add index.html
```

O segundo adiciona todos os arquivos da pasta atual:

```bash
git add .
```

Para iniciantes, `git add .` é prático, mas sempre confira o resultado de `git status` antes de fazer o commit. Assim, você evita incluir arquivos que não deveriam ser enviados.

---

## 13. Criando o primeiro commit

Um **commit** é um registro de alterações. Ele funciona como um ponto salvo no histórico do projeto.

Depois de adicionar o arquivo à área de preparação, execute:

```bash
git commit -m "Cria a página inicial"
```

A opção `-m` permite informar uma mensagem para descrever o commit.

Exemplos de boas mensagens:

```bash
git commit -m "Adiciona estrutura HTML inicial"
git commit -m "Corrige texto do título"
git commit -m "Adiciona estilos da página"
```

Evite mensagens vagas como:

```bash
git commit -m "Alterações"
git commit -m "Coisas"
```

Uma mensagem deve explicar o que foi feito.

Depois do commit, execute:

```bash
git status
```

Se tudo estiver correto, aparecerá uma mensagem semelhante a:

```text
nothing to commit, working tree clean
```

Isso significa que não há alterações pendentes.

---

## 14. Visualizando o histórico com `git log`

Para ver os commits realizados:

```bash
git log
```

O resultado mostra informações como:

- identificador do commit;
- autor;
- data;
- mensagem.

Para uma visualização resumida:

```bash
git log --oneline
```

Exemplo:

```text
8a31f4c Cria a página inicial
```

Para mostrar um histórico mais visual:

```bash
git log --oneline --graph --decorate --all
```

---

## 15. Criando uma conta no GitHub

Acesse:

[https://github.com/](https://github.com/)

Clique em **Sign up** e siga o cadastro.

Escolha um nome de usuário que você goste, pois ele poderá fazer parte do endereço dos seus projetos.

Exemplo de endereço de perfil:

```text
https://github.com/seu-usuario
```

Depois de criar a conta, confirme seu e-mail se o GitHub solicitar.

---

## 16. Criando um repositório no GitHub

Depois de entrar na sua conta:

1. clique no botão `+` no canto superior direito;
2. escolha **New repository**;
3. informe o nome do repositório;
4. escreva uma descrição opcional;
5. escolha se ele será público ou privado;
6. clique em **Create repository**.

Para este exemplo, use o nome:

```text
meu-primeiro-repositorio
```

### Não marque a opção de criar README neste momento

Como já criamos um projeto local, deixe desmarcada a opção de adicionar README automaticamente.

Isso evita criar um histórico remoto separado do histórico local. Para o primeiro envio, é mais simples criar o repositório remoto vazio e conectá-lo ao projeto local.

Depois de criar o repositório, o GitHub mostrará uma página com instruções para conectá-lo.

---

## 17. Conectando o repositório local ao GitHub

No Git Bash, dentro da pasta do projeto, adicione o endereço remoto:

```bash
git remote add origin https://github.com/seu-usuario/meu-primeiro-repositorio.git
```

Substitua `seu-usuario` pelo seu nome de usuário real.

Confira o endereço configurado:

```bash
git remote -v
```

O resultado será parecido com:

```text
origin  https://github.com/seu-usuario/meu-primeiro-repositorio.git (fetch)
origin  https://github.com/seu-usuario/meu-primeiro-repositorio.git (push)
```

### O que significa `origin`?

`origin` é um apelido tradicional para o repositório remoto principal. Em vez de digitar a URL completa toda vez, usamos apenas o nome `origin`.

---

## 18. Enviando o primeiro commit com `git push`

Para enviar a branch `main` ao GitHub, execute:

```bash
git push -u origin main
```

A opção `-u` cria uma ligação entre a branch local `main` e a branch remota `origin/main`.

Depois do primeiro envio, normalmente será possível usar apenas:

```bash
git push
```

Ao acessar a página do repositório no GitHub, você verá o arquivo `index.html`.

O fluxo completo realizado até aqui foi:

```bash
mkdir meu-primeiro-repositorio
cd meu-primeiro-repositorio
git init
# criar ou copiar os arquivos
git add .
git commit -m "Cria a página inicial"
git remote add origin https://github.com/seu-usuario/meu-primeiro-repositorio.git
git push -u origin main
```

---

## 19. Login e autenticação no GitHub

Ao fazer `git push` por HTTPS, o GitHub pode solicitar autenticação.

O GitHub não aceita mais a senha comum da conta para operações Git via HTTPS. As opções mais usadas são:

- Git Credential Manager;
- token de acesso pessoal;
- chave SSH.

### Git Credential Manager

Nas instalações atuais do Git para Windows, o Git Credential Manager costuma ser incluído. Ele pode abrir uma janela do navegador para você entrar na conta do GitHub.

Depois que a autenticação for concluída, as credenciais podem ser armazenadas de maneira segura para usos futuros.

### Token de acesso pessoal

Um token funciona como uma senha específica para operações autorizadas. Nunca publique o token em arquivos, mensagens, screenshots ou repositórios.

Se você usar um token no terminal, trate-o como uma senha:

- não compartilhe;
- não coloque dentro do código;
- revogue-o se houver suspeita de exposição;
- crie apenas as permissões necessárias.

### Chave SSH

Outra opção é configurar uma chave SSH. Esse método evita digitar credenciais repetidamente e é bastante usado por quem trabalha frequentemente com GitHub.

Para iniciantes, HTTPS com o gerenciador de credenciais costuma ser a opção mais simples.

---

## 20. Fazendo uma nova alteração

Agora abra o arquivo `index.html` e altere o parágrafo:

```html
<p>Estou aprendendo Git e GitHub passo a passo.</p>
```

Salve o arquivo e consulte o status:

```bash
git status
```

O Git indicará que `index.html` foi modificado.

Veja exatamente o que mudou:

```bash
git diff
```

O comando `git diff` mostra as diferenças entre a versão atual e a última versão registrada.

Depois, registre a alteração:

```bash
git add index.html
git commit -m "Atualiza mensagem da página"
git push
```

Agora a nova versão também estará disponível no GitHub.

---

## 21. Baixando alterações com `git pull`

O comando `git pull` busca alterações do repositório remoto e tenta incorporá-las ao seu projeto local.

```bash
git pull
```

Use esse comando antes de começar a trabalhar em um projeto compartilhado, especialmente quando outras pessoas também fazem alterações.

Um fluxo comum é:

```bash
git pull
# editar arquivos
git add .
git commit -m "Descreve a alteração"
git push
```

---

## 22. Clonando um projeto existente

Se o projeto já existe no GitHub e você quer baixá-lo para o computador, use `git clone`.

```bash
git clone https://github.com/seu-usuario/meu-primeiro-repositorio.git
```

O Git criará uma pasta com o nome do repositório.

Para escolher outro nome de pasta:

```bash
git clone https://github.com/seu-usuario/meu-primeiro-repositorio.git meu-site
```

Depois, entre na pasta:

```bash
cd meu-primeiro-repositorio
```

Confira o estado:

```bash
git status
```

Você também pode abrir o projeto no VS Code:

```bash
code .
```

---

## 23. Criando um arquivo `README.md`

O README explica o que é o projeto e como executá-lo.

Crie o arquivo:

```bash
touch README.md
```

Adicione este conteúdo:

```markdown
# Meu primeiro repositório

Este é um projeto criado para aprender Git e GitHub.

## Como visualizar

Abra o arquivo `index.html` em um navegador ou use o Live Server no Visual Studio Code.

## Tecnologias

- HTML
- Git
- GitHub
```

Depois, registre o arquivo:

```bash
git add README.md
git commit -m "Adiciona documentação do projeto"
git push
```

---

## 24. Usando o arquivo `.gitignore`

O arquivo `.gitignore` informa ao Git quais arquivos e pastas não devem ser enviados para o repositório.

Ele é útil para ignorar:

- arquivos temporários;
- configurações pessoais;
- pastas de dependências;
- arquivos com senhas;
- arquivos gerados automaticamente;
- logs.

Crie o arquivo:

```bash
touch .gitignore
```

Exemplo de conteúdo para um projeto web:

```gitignore
# Dependências do Node.js
node_modules/

# Arquivos de ambiente
.env
.env.local

# Logs
*.log

# Arquivos do sistema operacional
.DS_Store
Thumbs.db

# Configurações locais de editores
.vscode/settings.json
```

Depois, adicione e envie o arquivo:

```bash
git add .gitignore
git commit -m "Adiciona arquivos ignorados"
git push
```

> Nunca coloque senhas, tokens, chaves privadas ou outras informações secretas no GitHub.

### Arquivo que já foi enviado por engano

Adicionar um nome ao `.gitignore` não remove automaticamente um arquivo que já foi registrado pelo Git. Para retirar um arquivo do controle de versão, mantendo-o no computador, use:

```bash
git rm --cached nome-do-arquivo
```

Depois, faça um novo commit:

```bash
git commit -m "Remove arquivo local do controle de versão"
git push
```

Se uma senha ou token já foi publicado, apenas apagar o arquivo em um novo commit pode não ser suficiente. Revogue ou troque a credencial imediatamente.

---

## 25. Branches: trabalhando em ramificações

Uma **branch** é uma linha independente de desenvolvimento. Ela permite experimentar alterações sem modificar diretamente a branch principal.

Para criar uma branch chamada `nova-pagina`:

```bash
git branch nova-pagina
```

Para mudar para ela:

```bash
git switch nova-pagina
```

Também é possível criar e mudar para a branch em um único comando:

```bash
git switch -c nova-pagina
```

Confira em qual branch você está:

```bash
git branch
```

A branch atual aparecerá com um asterisco:

```text
* nova-pagina
  main
```

Depois de fazer alterações, crie um commit:

```bash
git add .
git commit -m "Adiciona nova página"
```

Para enviar a branch ao GitHub:

```bash
git push -u origin nova-pagina
```

Para voltar à branch principal:

```bash
git switch main
```

---

## 26. Mesclando uma branch na `main`

Depois de testar as alterações, volte para a branch principal:

```bash
git switch main
```

Atualize a branch:

```bash
git pull
```

Mescle a branch de trabalho:

```bash
git merge nova-pagina
```

Envie o resultado ao GitHub:

```bash
git push
```

Em projetos de equipe, esse processo geralmente é feito por meio de uma **Pull Request** no GitHub, permitindo que outras pessoas revisem o código antes da integração.

---

## 27. Desfazendo alterações ainda não salvas em um commit

Se você alterou um arquivo, mas quer voltar ao estado do último commit, use:

```bash
git restore nome-do-arquivo
```

Exemplo:

```bash
git restore index.html
```

> Atenção: esse comando descarta as alterações locais do arquivo. Use somente quando tiver certeza de que não precisa delas.

Para retirar um arquivo da área de preparação, mas manter suas alterações:

```bash
git restore --staged nome-do-arquivo
```

Exemplo:

```bash
git restore --staged index.html
```

---

## 28. Alterando a mensagem do último commit

Se você acabou de criar um commit e percebeu que a mensagem está errada, use:

```bash
git commit --amend -m "Nova mensagem correta"
```

Isso altera o último commit local.

Evite alterar commits que já foram enviados e utilizados por outras pessoas sem entender as consequências. Alterar o histórico compartilhado pode causar conflitos.

---

## 29. Resolvendo conflitos de merge

Um conflito acontece quando duas alterações diferentes foram feitas na mesma parte de um arquivo e o Git não consegue escolher automaticamente qual manter.

O arquivo poderá apresentar marcações como:

```text
<<<<<<< HEAD
Texto da branch atual
=======
Texto da outra branch
>>>>>>> outra-branch
```

Para resolver:

1. abra o arquivo;
2. escolha o conteúdo correto;
3. remova as marcações `<<<<<<<`, `=======` e `>>>>>>>`;
4. salve o arquivo;
5. adicione o arquivo novamente;
6. conclua o merge.

```bash
git add nome-do-arquivo
git commit -m "Resolve conflito de merge"
```

Depois, envie ao GitHub:

```bash
git push
```

---

## 30. Comandos essenciais para memorizar

| Comando | Função |
|---|---|
| `git --version` | Mostra a versão do Git |
| `git config --global user.name` | Configura ou consulta o nome |
| `git config --global user.email` | Configura ou consulta o e-mail |
| `git init` | Cria um repositório local |
| `git status` | Mostra o estado do projeto |
| `git add .` | Adiciona alterações à preparação |
| `git commit -m "mensagem"` | Registra alterações |
| `git log --oneline` | Mostra o histórico resumido |
| `git diff` | Mostra diferenças não registradas |
| `git remote -v` | Mostra repositórios remotos |
| `git push` | Envia commits ao GitHub |
| `git pull` | Baixa e incorpora alterações |
| `git clone URL` | Copia um repositório remoto |
| `git branch` | Lista branches |
| `git switch nome` | Troca de branch |
| `git restore arquivo` | Descarta alterações locais |

---

## 31. Fluxo básico de trabalho

Para um projeto já conectado ao GitHub, o fluxo mais comum é:

```bash
# 1. Atualizar a cópia local
git pull

# 2. Conferir o estado
git status

# 3. Editar os arquivos

# 4. Ver o que mudou
git diff

# 5. Adicionar as alterações
git add .

# 6. Criar um commit
git commit -m "Descreve o que foi feito"

# 7. Enviar para o GitHub
git push
```

Uma versão ainda mais curta seria:

```bash
git add .
git commit -m "Atualiza projeto"
git push
```

Mesmo usando a versão curta, consulte o `git status` regularmente.

---

## 32. Erros comuns e como resolver

### `Author identity unknown`

Esse erro aparece quando o nome e o e-mail ainda não foram configurados.

Execute:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu-email@exemplo.com"
```

### `not a git repository`

Você executou um comando Git fora de uma pasta que possui um repositório.

Entre na pasta correta:

```bash
cd caminho/para/seu-projeto
```

Ou inicialize um novo repositório:

```bash
git init
```

### `nothing to commit, working tree clean`

Esse não é um erro. Significa que não há alterações novas para registrar.

### `remote origin already exists`

O repositório já possui um remoto chamado `origin`.

Veja a URL atual:

```bash
git remote -v
```

Para trocar a URL:

```bash
git remote set-url origin https://github.com/seu-usuario/seu-repositorio.git
```

### `rejected - non-fast-forward`

Isso geralmente significa que o GitHub tem commits que ainda não existem no seu computador.

Primeiro, baixe as alterações:

```bash
git pull
```

Depois, resolva possíveis conflitos, faça o commit e tente novamente:

```bash
git push
```

### `src refspec main does not match any`

Esse problema pode acontecer quando ainda não existe um commit ou quando a branch tem outro nome.

Verifique o histórico:

```bash
git log --oneline
```

Se não houver commit, crie um:

```bash
git add .
git commit -m "Primeiro commit"
```

Confira o nome da branch:

```bash
git branch
```

---

## 33. Cuidados importantes de segurança

Nunca envie para um repositório público:

- senhas;
- tokens de acesso;
- chaves de API;
- chaves privadas SSH;
- arquivos `.env` com informações reais;
- dados pessoais desnecessários;
- arquivos de configuração com credenciais.

Use o `.gitignore` para evitar o envio acidental:

```gitignore
.env
.env.*
*.pem
*.key
secrets/
```

Antes de fazer um `git push`, confira os arquivos preparados:

```bash
git status
```

E, se necessário, veja as diferenças:

```bash
git diff --cached
```

Esse comando mostra o que será incluído no próximo commit.

---

## 34. Checklist do primeiro projeto

Use este checklist para confirmar que tudo foi feito corretamente:

- [ ] O Git foi instalado.
- [ ] O comando `git --version` funciona.
- [ ] O nome foi configurado.
- [ ] O e-mail foi configurado.
- [ ] Uma pasta de projeto foi criada.
- [ ] O comando `git init` foi executado.
- [ ] Um arquivo de projeto foi criado.
- [ ] O comando `git status` foi compreendido.
- [ ] O arquivo foi adicionado com `git add`.
- [ ] O primeiro commit foi criado.
- [ ] Uma conta no GitHub foi criada.
- [ ] Um repositório remoto foi criado.
- [ ] O remoto `origin` foi configurado.
- [ ] O primeiro `git push` foi realizado.
- [ ] O projeto aparece no GitHub.
- [ ] Um arquivo `.gitignore` foi criado quando necessário.

---

## Conclusão

Git e GitHub podem parecer complicados no começo, mas o fluxo básico é simples:

```text
editar
  ↓
git status
  ↓
git add
  ↓
git commit
  ↓
git push
```

O Git cuida do histórico local e o GitHub permite armazenar e compartilhar esse histórico online.

Comece com projetos pequenos. Pratique a criação de commits claros, confira o resultado de `git status` e faça alterações gradualmente. Com o tempo, comandos como `git pull`, `git push`, `git branch` e `git clone` se tornarão parte natural do seu trabalho.

O mais importante é não ter medo dos comandos. Leia as mensagens exibidas pelo Git, faça cópias de segurança e use o histórico para entender como seu projeto evolui.
