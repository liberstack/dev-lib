# Visual Studio Code: instalação e configuração para iniciantes

Aprender a programar fica muito mais fácil quando usamos uma ferramenta confortável, organizada e com bons recursos. O **Visual Studio Code**, também conhecido como **VS Code**, é um editor de código gratuito, leve e disponível para Windows, macOS e Linux.

Neste tutorial, você vai aprender, passo a passo, como:

- instalar o Visual Studio Code;
- conhecer a interface principal;
- criar e abrir uma pasta de projeto;
- instalar extensões básicas;
- configurar o Live Server;
- formatar arquivos automaticamente;
- criar um exemplo simples com HTML, CSS e JavaScript;
- resolver problemas comuns.

O conteúdo foi escrito para quem está começando e não exige experiência anterior.

---

## 1. O que é o Visual Studio Code?

O Visual Studio Code é um editor de texto especializado em programação. Diferentemente de um editor comum, ele oferece recursos como:

- destaque de cores para diferentes partes do código;
- sugestões automáticas;
- navegação entre arquivos;
- terminal integrado;
- extensões para adicionar funcionalidades;
- integração com Git;
- depuração de programas;
- formatação automática.

É importante não confundir **Visual Studio Code** com **Visual Studio**. O Visual Studio é uma IDE maior, muito usada em projetos com .NET e C#. Já o VS Code é mais leve e flexível, sendo bastante utilizado para desenvolvimento web, Python, JavaScript, Java, PHP e muitas outras tecnologias.

---

## 2. Requisitos básicos

Antes de instalar o VS Code, verifique se você tem:

- um computador com Windows, macOS ou Linux;
- acesso à internet;
- permissão para instalar programas;
- pelo menos uma pasta disponível para guardar seus projetos.

O VS Code funciona sem que você precise instalar uma linguagem de programação. Porém, para executar determinados projetos, talvez seja necessário instalar ferramentas adicionais, como:

- Node.js, para JavaScript e TypeScript;
- Python, para programas em Python;
- Java, para projetos Java;
- PHP, para aplicações PHP.

Neste tutorial, usaremos HTML, CSS e JavaScript, que podem ser testados diretamente no navegador.

---

## 3. Como baixar o Visual Studio Code

Acesse o site oficial:

[https://code.visualstudio.com/](https://code.visualstudio.com/)

Na página inicial, escolha a versão correspondente ao seu sistema operacional.

> Baixe o programa sempre pelo site oficial ou por uma fonte confiável. Evite instaladores encontrados em páginas desconhecidas.

---

## 4. Instalação no Windows

### Passo 1: abrir o instalador

Depois de baixar o arquivo `.exe`, abra-o com um duplo clique.

### Passo 2: aceitar a licença

Leia os termos de licença e marque a opção para aceitar o contrato. Em seguida, clique em **Próximo**.

### Passo 3: escolher o local de instalação

Na maioria dos casos, você pode manter a pasta sugerida pelo instalador. Clique em **Próximo**.

### Passo 4: selecionar tarefas adicionais

Durante a instalação, é recomendável marcar opções semelhantes a estas:

- **Adicionar “Abrir com Code” ao menu de contexto de arquivos**;
- **Adicionar “Abrir com Code” ao menu de contexto de diretórios**;
- **Adicionar o VS Code ao PATH**;
- criar um atalho na área de trabalho, se desejar.

A opção **PATH** permite abrir o VS Code pelo terminal usando o comando `code`.

### Passo 5: concluir

Clique em **Instalar** e aguarde. Ao final, marque a opção para iniciar o Visual Studio Code e clique em **Concluir**.

---

## 5. Instalação no macOS

No macOS, baixe o arquivo apropriado no site oficial. Depois:

1. abra o arquivo `.zip` baixado;
2. arraste o aplicativo **Visual Studio Code** para a pasta **Applications**;
3. abra o VS Code pelo Launchpad ou pelo Finder;
4. confirme a abertura caso o sistema solicite.

Para usar o comando `code` no terminal:

1. abra o VS Code;
2. pressione `Command + Shift + P`;
3. procure por `Shell Command: Install 'code' command in PATH`;
4. selecione essa opção;
5. feche e abra novamente o terminal.

Depois, teste com:

```bash
code .
```

Esse comando abre no VS Code a pasta atual do terminal.

---

## 6. Instalação no Linux

Em distribuições Linux, a forma de instalação varia. Consulte a página oficial de download para escolher o método adequado à sua distribuição.

Em sistemas baseados em Debian ou Ubuntu, por exemplo, é comum baixar um pacote `.deb` e instalá-lo pelo gerenciador de aplicativos. Também pode ser possível instalar pela loja de aplicativos da distribuição.

Após instalar, abra o terminal e teste:

```bash
code --version
```

Se o comando funcionar, o terminal exibirá a versão instalada.

---

## 7. Conhecendo a interface do VS Code

Ao abrir o VS Code pela primeira vez, você verá algumas áreas importantes.

### 7.1 Barra lateral de atividades

Fica no lado esquerdo e contém atalhos para:

- **Explorer**: arquivos e pastas do projeto;
- **Search**: pesquisa dentro dos arquivos;
- **Source Control**: controle de versão com Git;
- **Run and Debug**: execução e depuração;
- **Extensions**: instalação de extensões.

### 7.2 Explorador de arquivos

O Explorer mostra as pastas e os arquivos abertos no projeto atual.

### 7.3 Área do editor

É a região central onde você escreve e modifica o código.

### 7.4 Painel inferior

Pode exibir:

- terminal;
- problemas encontrados;
- saída de extensões;
- mensagens de depuração.

Para abrir ou fechar o terminal integrado, use:

```text
Ctrl + `
```

No macOS, normalmente:

```text
Control + `
```

---

## 8. Criando a primeira pasta de projeto

Organizar cada projeto em uma pasta própria é uma boa prática.

Crie uma pasta chamada `meu-primeiro-site` em um local fácil de encontrar. Depois, no VS Code:

1. clique em **File** ou **Arquivo**;
2. selecione **Open Folder** ou **Abrir Pasta**;
3. escolha a pasta `meu-primeiro-site`;
4. confirme a abertura.

O VS Code perguntará se você confia nos arquivos da pasta. Se a pasta foi criada por você, escolha a opção de confiar.

### Abrindo pelo terminal

Você também pode abrir a pasta pelo terminal. Entre na pasta e execute:

```bash
cd caminho/para/meu-primeiro-site
code .
```

No Windows, um exemplo seria:

```powershell
cd C:\Users\SeuNome\Documents\meu-primeiro-site
code .
```

---

## 9. Extensões: o que são?

Extensões são pequenos complementos que adicionam recursos ao VS Code. Elas podem ajudar a:

- formatar código;
- criar servidores locais;
- destacar cores;
- trabalhar com linguagens específicas;
- validar erros;
- melhorar a produtividade.

Para instalar uma extensão:

1. clique no ícone de extensões na barra lateral;
2. pesquise pelo nome;
3. confira o nome do autor e a quantidade de instalações;
4. clique em **Install** ou **Instalar**.

> Instale extensões de fontes confiáveis e evite instalar muitas extensões sem necessidade. Extensões desnecessárias podem deixar o editor mais lento.

---

## 10. Extensões básicas recomendadas

### 10.1 Live Server

A extensão **Live Server**, geralmente associada ao autor Ritwick Dey, cria um servidor local para visualizar páginas HTML no navegador.

Depois de instalar:

1. abra um arquivo HTML;
2. clique com o botão direito no editor;
3. selecione **Open with Live Server**;
4. o navegador será aberto automaticamente.

Outra opção é clicar no botão **Go Live**, geralmente exibido no canto inferior direito.

Quando você salvar uma alteração, o navegador poderá atualizar a página automaticamente.

### 10.2 Prettier - Code formatter

O **Prettier** organiza automaticamente a formatação de arquivos como:

- HTML;
- CSS;
- JavaScript;
- JSON;
- Markdown.

Depois de instalar, clique com o botão direito em um arquivo e escolha **Format Document**.

Atalho comum:

```text
Shift + Alt + F
```

No macOS:

```text
Shift + Option + F
```

### 10.3 Auto Rename Tag

O **Auto Rename Tag** altera automaticamente a tag de fechamento quando você muda a tag de abertura.

Por exemplo, se você trocar:

```html
<h1>Título</h1>
```

para:

```html
<h2>Título</h1>
```

A extensão poderá atualizar o fechamento para:

```html
<h2>Título</h2>
```

### 10.4 Auto Close Tag

Essa extensão fecha automaticamente tags HTML. Ao digitar:

```html
<p>
```

ela pode completar o código como:

```html
<p></p>
```

### 10.5 Error Lens

O **Error Lens** mostra erros e avisos diretamente na linha do código, facilitando a identificação de problemas.

### 10.6 Material Icon Theme

O **Material Icon Theme** altera os ícones de arquivos e pastas no Explorer. Não é obrigatório, mas pode deixar a visualização mais organizada.

### 10.7 GitLens

O **GitLens** adiciona informações úteis para quem usa Git, como histórico de alterações e autoria das linhas.

Para começar, você não precisa instalar todas essas extensões. Uma combinação simples seria:

- Live Server;
- Prettier;
- Auto Rename Tag;
- Material Icon Theme.

---

## 11. Criando um site de exemplo

Dentro da pasta do projeto, crie três arquivos:

```text
meu-primeiro-site/
├── index.html
├── style.css
└── script.js
```

### 11.1 Arquivo `index.html`

Crie o arquivo `index.html` com este conteúdo:

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Meu primeiro site</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <main class="container">
      <h1>Olá, mundo!</h1>
      <p>Este é o meu primeiro site criado no Visual Studio Code.</p>
      <button id="botaoMensagem">Clique aqui</button>
      <p id="mensagem"></p>
    </main>

    <script src="script.js"></script>
  </body>
</html>
```

### 11.2 Arquivo `style.css`

Agora, adicione o estilo:

```css
* {
  box-sizing: border-box;
}

body {
  display: grid;
  min-height: 100vh;
  margin: 0;
  place-items: center;
  background: #f2f4f8;
  color: #1f2937;
  font-family: Arial, sans-serif;
}

.container {
  width: min(90%, 520px);
  padding: 2rem;
  border-radius: 12px;
  background: #ffffff;
  text-align: center;
  box-shadow: 0 8px 24px rgb(0 0 0 / 10%);
}

button {
  padding: 0.75rem 1rem;
  border: 0;
  border-radius: 8px;
  background: #2563eb;
  color: #ffffff;
  cursor: pointer;
  font-size: 1rem;
}

button:hover {
  background: #1d4ed8;
}

#mensagem {
  min-height: 1.5rem;
  font-weight: bold;
}
```

### 11.3 Arquivo `script.js`

Por fim, adicione a interação:

```javascript
const botaoMensagem = document.querySelector('#botaoMensagem');
const mensagem = document.querySelector('#mensagem');

botaoMensagem.addEventListener('click', () => {
  mensagem.textContent = 'Você clicou no botão!';
});
```

Salve os três arquivos usando `Ctrl + S` ou `Command + S` no macOS.

---

## 12. Visualizando o projeto com Live Server

Para abrir o site:

1. abra o arquivo `index.html`;
2. clique com o botão direito no editor;
3. selecione **Open with Live Server**;
4. aguarde o navegador abrir.

Normalmente, o endereço será semelhante a:

```text
http://127.0.0.1:5500/index.html
```

O endereço pode variar conforme a configuração e a porta disponível.

Agora altere o texto do título em `index.html`, salve o arquivo e observe o navegador. Se o Live Server estiver funcionando, a página será atualizada automaticamente.

---

## 13. Configurando o Prettier como formatador padrão

Para definir o Prettier como formatador padrão:

1. abra a paleta de comandos com `Ctrl + Shift + P`;
2. procure por `Format Document With...`;
3. escolha `Configure Default Formatter`;
4. selecione `Prettier - Code formatter`.

Também é possível ativar a formatação ao salvar.

Abra as configurações usando:

```text
Ctrl + ,
```

Pesquise por:

```text
Format On Save
```

Ative a opção **Editor: Format On Save**.

A partir daí, o VS Code tentará formatar o arquivo sempre que você salvá-lo.

---

## 14. Configuração usando `settings.json`

Usuários que preferem editar configurações diretamente podem abrir o arquivo JSON:

1. pressione `Ctrl + Shift + P`;
2. procure por `Preferences: Open User Settings (JSON)`;
3. adicione configurações como estas:

```json
{
  "editor.formatOnSave": true,
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.wordWrap": "on",
  "files.autoSave": "afterDelay",
  "files.autoSaveDelay": 1000,
  "editor.bracketPairColorization.enabled": true,
  "editor.minimap.enabled": false
}
```

### O que cada configuração faz?

- `editor.formatOnSave`: formata o arquivo ao salvar;
- `editor.tabSize`: define o tamanho visual da indentação;
- `editor.insertSpaces`: usa espaços em vez de tabulações;
- `editor.wordWrap`: quebra linhas longas visualmente;
- `files.autoSave`: salva automaticamente depois de um pequeno intervalo;
- `editor.minimap.enabled`: oculta o minimapa lateral;
- `editor.bracketPairColorization.enabled`: diferencia visualmente pares de chaves e parênteses.

> Se o seu arquivo já tiver outras configurações, não apague tudo. Acrescente as novas propriedades respeitando a sintaxe JSON.

---

## 15. Atalhos importantes

| Ação | Windows/Linux | macOS |
|---|---|---|
| Salvar arquivo | `Ctrl + S` | `Command + S` |
| Abrir arquivo rapidamente | `Ctrl + P` | `Command + P` |
| Abrir configurações | `Ctrl + ,` | `Command + ,` |
| Abrir paleta de comandos | `Ctrl + Shift + P` | `Command + Shift + P` |
| Abrir terminal | `Ctrl + ` | `Control + ` |
| Formatar documento | `Shift + Alt + F` | `Shift + Option + F` |
| Comentar linha | `Ctrl + /` | `Command + /` |
| Duplicar linha | `Shift + Alt + Down` | `Shift + Option + Down` |
| Pesquisar no projeto | `Ctrl + Shift + F` | `Command + Shift + F` |

O atalho mais importante para iniciantes é a **Paleta de Comandos**. Ela permite pesquisar praticamente qualquer ação do VS Code sem precisar decorar todos os menus.

---

## 16. Terminal integrado

O terminal integrado permite executar comandos sem sair do VS Code.

Para abri-lo, use:

```text
Ctrl + `
```

Alguns comandos úteis:

```bash
# Exibir a pasta atual
pwd

# Listar arquivos e pastas
ls

# Entrar em uma pasta
cd nome-da-pasta
```

No Windows PowerShell, você também pode usar:

```powershell
# Exibir a pasta atual
Get-Location

# Listar arquivos e pastas
Get-ChildItem

# Entrar em uma pasta
Set-Location nome-da-pasta
```

O terminal permite instalar pacotes, iniciar servidores, usar Git e executar programas.

---

## 17. Usando o Git no VS Code

O Git é um sistema de controle de versão. Ele ajuda a acompanhar alterações e recuperar versões anteriores dos arquivos.

Depois de instalar o Git no computador, abra uma pasta de projeto e execute:

```bash
git init
```

Veja os arquivos modificados:

```bash
git status
```

Adicione os arquivos:

```bash
git add .
```

Crie o primeiro registro de alteração:

```bash
git commit -m "Cria o primeiro site"
```

A seção **Source Control** do VS Code também permite visualizar alterações e criar commits por uma interface gráfica.

---

## 18. Problemas comuns e soluções

### O botão “Go Live” não aparece

Verifique se:

1. a extensão Live Server está instalada;
2. você abriu uma pasta no VS Code;
3. existe um arquivo com extensão `.html` aberto;
4. o VS Code foi reiniciado depois da instalação da extensão.

### O Prettier não formata o arquivo

Confira se:

- o Prettier está instalado;
- o arquivo possui uma linguagem compatível;
- o Prettier foi selecionado como formatador padrão;
- não existe um erro de sintaxe no arquivo;
- a opção `editor.formatOnSave` está ativada.

### O CSS não funciona

Confira se o HTML contém esta linha dentro de `<head>`:

```html
<link rel="stylesheet" href="style.css" />
```

Também confirme se `style.css` está na mesma pasta que `index.html`.

### O JavaScript não funciona

Confira se o HTML contém esta linha antes do fechamento de `</body>`:

```html
<script src="script.js"></script>
```

Verifique também o nome do arquivo. `script.js` e `Script.js` podem ser considerados nomes diferentes em alguns sistemas.

### A página não atualiza automaticamente

Tente:

1. salvar o arquivo manualmente;
2. fechar e abrir o Live Server;
3. atualizar o navegador com `Ctrl + R`;
4. verificar se o navegador não bloqueou a página;
5. verificar se a extensão está habilitada.

### O terminal diz que `code` não existe

Isso significa que o comando ainda não foi adicionado ao PATH. Reinstale o VS Code ativando a opção correspondente ou configure o comando de acordo com o seu sistema operacional.

---

## 19. Boas práticas para iniciantes

Para aproveitar melhor o VS Code:

1. mantenha cada projeto em uma pasta própria;
2. use nomes claros para arquivos e pastas;
3. salve os arquivos com frequência;
4. formate o código regularmente;
5. evite instalar extensões em excesso;
6. leia as mensagens de erro com calma;
7. faça pequenas alterações e teste cada uma;
8. use o Git para projetos importantes;
9. não copie códigos sem entender o que eles fazem;
10. aprenda os atalhos aos poucos.

Uma boa organização para um site simples pode ser:

```text
meu-projeto/
├── index.html
├── style.css
├── script.js
├── imagens/
│   └── logo.png
└── README.md
```

---

## 20. Checklist final

Antes de começar a estudar ou desenvolver, confirme:

- [ ] O VS Code está instalado.
- [ ] Você consegue abrir uma pasta de projeto.
- [ ] O terminal integrado está funcionando.
- [ ] A extensão Live Server está instalada.
- [ ] O Prettier está configurado.
- [ ] A formatação ao salvar está ativada.
- [ ] Você criou um arquivo `index.html`.
- [ ] O site abre no navegador.
- [ ] O CSS está sendo aplicado.
- [ ] O JavaScript responde ao clique do botão.

---

## Conclusão

O Visual Studio Code pode parecer cheio de opções no início, mas você não precisa aprender tudo de uma vez. Comece instalando o editor, criando uma pasta de projeto e aprendendo a usar quatro recursos principais: **Explorer**, **terminal**, **extensões** e **Live Server**.

Com o Prettier configurado e algumas extensões básicas, seu ambiente já estará preparado para estudar HTML, CSS e JavaScript com mais organização e produtividade.

O mais importante é praticar. Crie pequenos projetos, altere os exemplos deste tutorial e observe o resultado no navegador. Com o tempo, os atalhos, menus e ferramentas do VS Code se tornarão parte natural da sua rotina de programação.
