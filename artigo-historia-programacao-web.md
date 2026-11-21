# História da programação web: das origens da Internet aos sites modernos

A programação web faz parte da rotina de milhões de pessoas. Quando acessamos uma página, fazemos uma compra online, assistimos a um vídeo ou enviamos uma mensagem, estamos usando tecnologias que foram desenvolvidas ao longo de várias décadas.

Mas como a web começou? O que são HTTP e HTML? Qual é a diferença entre Internet e Web? Como o navegador encontra um site? E como um arquivo de texto se transforma em uma página visual no computador ou no celular?

Neste artigo, você conhecerá essa história de forma didática e verá exemplos práticos usando HTML, CSS, JavaScript, HTTP e um pequeno servidor local.

O conteúdo foi preparado para quem está começando e não exige conhecimento anterior.

---

## 1. Internet e Web são a mesma coisa?

Não. Embora muitas pessoas usem as palavras como se fossem sinônimas, elas representam conceitos diferentes.

### Internet

A **Internet** é uma grande rede mundial de computadores conectados. Ela permite a comunicação entre dispositivos por meio de cabos, fibras ópticas, redes sem fio, satélites e outros equipamentos.

Na Internet funcionam diversos serviços, como:

- World Wide Web;
- e-mail;
- chamadas de voz e vídeo;
- transferência de arquivos;
- jogos online;
- mensagens instantâneas.

### World Wide Web

A **World Wide Web**, também chamada apenas de Web, é um sistema de documentos e aplicações acessados por meio da Internet.

A Web usa tecnologias como:

- URLs, para localizar recursos;
- HTTP ou HTTPS, para transportar informações;
- HTML, para estruturar documentos;
- CSS, para definir aparência;
- JavaScript, para adicionar comportamento.

Uma comparação simples:

```text
Internet = a infraestrutura de estradas
Web      = um dos serviços que utiliza essas estradas
```

---

## 2. Antes da Web: as origens das redes de computadores

Antes de existir a Web como conhecemos hoje, pesquisadores já trabalhavam em redes capazes de conectar computadores distantes.

Na década de 1960, projetos acadêmicos e militares estudavam como manter a comunicação entre computadores mesmo que parte da rede apresentasse problemas.

Um dos projetos mais conhecidos foi a **ARPANET**, criada nos Estados Unidos. Ela é considerada uma das importantes antecessoras da Internet moderna.

A ideia central era dividir uma mensagem em pequenos pacotes. Esses pacotes poderiam seguir caminhos diferentes pela rede e ser reunidos novamente no destino.

O conceito pode ser representado assim:

```text
Mensagem original
        ↓
[Pacote 1] [Pacote 2] [Pacote 3]
        ↓
  rede de computadores
        ↓
[Pacote 2] [Pacote 1] [Pacote 3]
        ↓
Mensagem reconstruída
```

Essa forma de comunicação ajudou a criar redes mais flexíveis e resistentes.

---

## 3. O nascimento da World Wide Web

A Web foi criada por **Tim Berners-Lee**, um cientista britânico que trabalhava no CERN, na Suíça.

No final da década de 1980 e início da década de 1990, ele propôs um sistema que facilitasse o compartilhamento de documentos entre pesquisadores.

Para que esse sistema funcionasse, três componentes eram fundamentais:

1. **HTML**: linguagem para estruturar documentos;
2. **HTTP**: protocolo para transferir documentos;
3. **URL**: endereço para localizar cada recurso.

Esses três elementos continuam sendo fundamentais na Web atual.

### O primeiro servidor e o primeiro navegador

Tim Berners-Lee também criou:

- um dos primeiros servidores web;
- o primeiro navegador web;
- a primeira página web;
- as primeiras especificações de HTML e HTTP.

A primeira página explicava o próprio projeto da World Wide Web. Na época, as páginas eram simples e formadas principalmente por textos e links.

---

## 4. O que é HTML?

**HTML** significa **HyperText Markup Language**, ou Linguagem de Marcação de Hipertexto.

Apesar de ser chamada de linguagem, o HTML não é uma linguagem de programação tradicional. Ele é uma linguagem de marcação usada para indicar a estrutura do conteúdo.

Com HTML, podemos indicar:

- títulos;
- parágrafos;
- listas;
- links;
- imagens;
- tabelas;
- formulários;
- seções de uma página.

Exemplo simples:

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <title>Minha primeira página</title>
  </head>
  <body>
    <h1>Olá, Web!</h1>
    <p>Esta é uma página criada com HTML.</p>
  </body>
</html>
```

O navegador lê esse código e monta uma representação visual para o usuário.

---

## 5. Entendendo as tags HTML

As tags são palavras colocadas entre sinais de menor e maior:

```html
<p>Este é um parágrafo.</p>
```

Nesse exemplo:

- `<p>` é a tag de abertura;
- `Este é um parágrafo.` é o conteúdo;
- `</p>` é a tag de fechamento.

Algumas tags possuem uma estrutura diferente:

```html
<img src="foto.jpg" alt="Descrição da foto" />
```

### Estrutura básica de uma página

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Título exibido na aba</title>
  </head>
  <body>
    <header>
      <h1>Nome do site</h1>
    </header>

    <main>
      <p>Conteúdo principal da página.</p>
    </main>

    <footer>
      <p>Rodapé do site.</p>
    </footer>
  </body>
</html>
```

A organização semântica ajuda o navegador, os mecanismos de busca e as tecnologias assistivas a entenderem o conteúdo.

---

## 6. O que são hipertextos e links?

Um dos conceitos mais importantes da Web é o **hipertexto**. Ele permite conectar um documento a outro por meio de links.

Exemplo:

```html
<a href="https://www.example.com">Visitar o site</a>
```

A tag `<a>` cria uma âncora. O atributo `href` informa o endereço para onde o usuário será levado.

Também podemos criar links entre arquivos do mesmo projeto:

```html
<a href="sobre.html">Conheça nosso projeto</a>
```

Estrutura do projeto:

```text
meu-site/
├── index.html
└── sobre.html
```

O hipertexto transformou a Web em uma rede de documentos conectados.

---

## 7. O que é HTTP?

**HTTP** significa **HyperText Transfer Protocol**, ou Protocolo de Transferência de Hipertexto.

É o conjunto de regras usado para a comunicação entre clientes e servidores na Web.

Quando você acessa uma página, o navegador envia uma solicitação ao servidor. O servidor processa a solicitação e devolve uma resposta.

```text
Navegador                         Servidor
    |                                |
    | ---- solicitação HTTP ------>  |
    |                                |
    | <------- resposta HTTP ------- |
    |                                |
```

Uma solicitação HTTP pode pedir:

- uma página HTML;
- uma folha de estilos CSS;
- um arquivo JavaScript;
- uma imagem;
- dados de uma API.

---

## 8. Requisição e resposta HTTP na prática

Uma requisição HTTP pode ser representada assim:

```http
GET /index.html HTTP/1.1
Host: exemplo.com
Accept: text/html
```

Essa mensagem significa, de forma simplificada:

- `GET`: quero buscar um recurso;
- `/index.html`: o recurso solicitado;
- `HTTP/1.1`: versão do protocolo;
- `Host`: servidor que deve responder;
- `Accept`: tipo de conteúdo aceito pelo navegador.

A resposta pode ser parecida com esta:

```http
HTTP/1.1 200 OK
Content-Type: text/html; charset=UTF-8
Content-Length: 142

<!DOCTYPE html>
<html>
  <body>
    <h1>Página encontrada</h1>
  </body>
</html>
```

### Códigos de status

O servidor utiliza códigos para informar o resultado da solicitação:

| Código | Significado | Exemplo |
|---|---|---|
| `200` | Sucesso | Página carregada corretamente |
| `201` | Criado | Novo recurso criado |
| `301` | Redirecionamento permanente | Endereço mudou |
| `302` | Redirecionamento temporário | Recurso disponível em outro local |
| `400` | Requisição inválida | Dados enviados incorretamente |
| `401` | Não autenticado | Login necessário |
| `403` | Proibido | Acesso não permitido |
| `404` | Não encontrado | Página ou arquivo inexistente |
| `500` | Erro interno | Problema no servidor |

O famoso erro `404` significa que o servidor não encontrou o recurso solicitado.

---

## 9. HTTPS: o HTTP com segurança

O **HTTPS** é a versão protegida do HTTP. O `S` vem de **Secure**.

Com HTTPS, os dados são transmitidos de forma criptografada entre o navegador e o servidor. Isso ajuda a proteger:

- senhas;
- dados pessoais;
- informações de pagamento;
- cookies;
- conteúdo enviado por formulários.

Um endereço seguro começa com:

```text
https://
```

Em vez de:

```text
http://
```

O HTTPS utiliza certificados digitais para ajudar a confirmar a identidade do site e proteger a comunicação.

---

## 10. O que é uma URL?

**URL** significa **Uniform Resource Locator**, ou Localizador Uniforme de Recursos.

É o endereço usado para localizar um recurso na Web.

Exemplo:

```text
https://www.exemplo.com.br/produtos/caderno?cor=azul#detalhes
```

Podemos dividir esse endereço:

```text
https://       protocolo
www.exemplo.com.br  domínio
/produtos/caderno   caminho
?cor=azul           parâmetro de consulta
#detalhes          fragmento
```

### Partes principais

#### Protocolo

Indica como a comunicação será feita:

```text
https://
```

#### Domínio

Identifica o site:

```text
www.exemplo.com.br
```

#### Caminho

Indica o recurso ou página:

```text
/produtos/caderno
```

#### Query string

Transporta parâmetros:

```text
?cor=azul
```

#### Fragmento

Aponta para uma parte específica da página:

```text
#detalhes
```

---

## 11. Como o navegador encontra um site?

Quando você digita um endereço, várias etapas acontecem.

### Passo 1: o navegador interpreta a URL

O navegador identifica o protocolo, o domínio e o caminho.

### Passo 2: consulta ao DNS

O **DNS**, ou Domain Name System, converte nomes de domínio em endereços IP.

Por exemplo:

```text
www.exemplo.com  →  203.0.113.10
```

Pessoas preferem usar nomes. Computadores e redes utilizam endereços IP para localizar servidores.

### Passo 3: conexão com o servidor

O navegador se conecta ao endereço IP encontrado.

### Passo 4: envio da requisição

O navegador solicita o recurso usando HTTP ou HTTPS.

### Passo 5: recebimento da resposta

O servidor envia HTML, CSS, JavaScript, imagens e outros recursos.

### Passo 6: renderização

O navegador interpreta os arquivos e desenha a página na tela.

Resumo:

```text
URL
 ↓
DNS encontra o IP
 ↓
Navegador conecta ao servidor
 ↓
Requisição HTTP
 ↓
Resposta do servidor
 ↓
Navegador renderiza a página
```

---

## 12. O crescimento da Web nos anos 1990

No início da Web, as páginas eram principalmente documentos com textos e links. Com o tempo, novos navegadores e tecnologias foram adicionados.

Durante a década de 1990:

- mais pessoas passaram a ter acesso à Internet;
- surgiram novos navegadores;
- as páginas começaram a usar imagens e tabelas;
- empresas começaram a criar sites institucionais;
- surgiram os primeiros mecanismos de busca;
- o comércio eletrônico começou a se desenvolver.

Nesse período, muitos sites misturavam estrutura e aparência no mesmo arquivo. Era comum usar tabelas para organizar visualmente o conteúdo.

Exemplo de uma técnica antiga:

```html
<table border="1">
  <tr>
    <td>Menu</td>
    <td>Conteúdo</td>
  </tr>
</table>
```

Hoje, essa organização normalmente seria feita com HTML semântico e CSS.

---

## 13. O surgimento do CSS

**CSS** significa **Cascading Style Sheets**, ou Folhas de Estilo em Cascata.

O CSS foi criado para separar o conteúdo da apresentação visual.

Antes do CSS, o HTML era frequentemente usado para controlar tanto a estrutura quanto a aparência. Com CSS, podemos colocar a estrutura no HTML e os estilos em um arquivo separado.

### HTML sem estilo

```html
<h1>Meu site</h1>
<p>Uma página simples.</p>
```

### CSS

```css
body {
  background: #f4f4f4;
  color: #222;
  font-family: Arial, sans-serif;
}

h1 {
  color: #2563eb;
}
```

### Ligando o CSS ao HTML

```html
<link rel="stylesheet" href="style.css" />
```

Essa separação facilitou a manutenção e permitiu aplicar o mesmo estilo a várias páginas.

---

## 14. Criando uma página histórica com HTML e CSS

Vamos criar um exemplo prático sobre a própria história da Web.

Crie esta estrutura:

```text
historia-web/
├── index.html
└── style.css
```

### Arquivo `index.html`

```html
<!DOCTYPE html>
<html lang="pt-BR">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>História da Web</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header class="cabecalho">
      <h1>História da Web</h1>
      <p>Uma linha do tempo da programação web.</p>
    </header>

    <main class="linha-do-tempo">
      <article class="evento">
        <span class="ano">1969</span>
        <h2>ARPANET</h2>
        <p>
          Uma das redes precursoras da Internet começa a conectar computadores
          de instituições de pesquisa.
        </p>
      </article>

      <article class="evento">
        <span class="ano">1989</span>
        <h2>Proposta da Web</h2>
        <p>
          Tim Berners-Lee apresenta uma proposta para facilitar o
          compartilhamento de informações no CERN.
        </p>
      </article>

      <article class="evento">
        <span class="ano">1991</span>
        <h2>Primeiro site</h2>
        <p>
          A World Wide Web começa a ser disponibilizada ao público.
        </p>
      </article>

      <article class="evento">
        <span class="ano">Hoje</span>
        <h2>Aplicações modernas</h2>
        <p>
          A Web inclui lojas, redes sociais, jogos, sistemas empresariais e
          aplicações completas.
        </p>
      </article>
    </main>
  </body>
</html>
```

### Arquivo `style.css`

```css
* {
  box-sizing: border-box;
}

body {
  margin: 0;
  background: #eef2ff;
  color: #1f2937;
  font-family: Arial, sans-serif;
}

.cabecalho {
  padding: 3rem 1rem;
  background: #1e3a8a;
  color: #ffffff;
  text-align: center;
}

.linha-do-tempo {
  display: grid;
  gap: 1rem;
  width: min(90%, 760px);
  margin: 2rem auto;
}

.evento {
  padding: 1.5rem;
  border-left: 5px solid #2563eb;
  border-radius: 8px;
  background: #ffffff;
  box-shadow: 0 4px 12px rgb(0 0 0 / 10%);
}

.ano {
  color: #2563eb;
  font-weight: bold;
}
```

Abra o arquivo no navegador ou use uma extensão como Live Server no Visual Studio Code.

---

## 15. O surgimento do JavaScript

O **JavaScript** surgiu na década de 1990 para adicionar interatividade às páginas web.

Antes dele, muitas páginas eram documentos estáticos. O JavaScript permitiu responder a ações do usuário sem precisar recarregar toda a página.

Com JavaScript, podemos:

- alterar textos;
- abrir e fechar menus;
- validar formulários;
- responder a cliques;
- fazer cálculos;
- buscar dados de servidores;
- criar animações;
- desenvolver aplicações completas.

Exemplo:

```html
<button id="botao">Clique aqui</button>
<p id="mensagem"></p>

<script>
  const botao = document.querySelector('#botao');
  const mensagem = document.querySelector('#mensagem');

  botao.addEventListener('click', () => {
    mensagem.textContent = 'O JavaScript respondeu ao clique!';
  });
</script>
```

Nesse exemplo:

1. o HTML cria o botão e o parágrafo;
2. o JavaScript encontra esses elementos;
3. um evento de clique é registrado;
4. o texto do parágrafo é alterado.

---

## 16. Adicionando JavaScript ao projeto histórico

Crie um arquivo chamado `script.js`:

```text
historia-web/
├── index.html
├── style.css
└── script.js
```

Adicione ao final do `body`:

```html
<script src="script.js"></script>
```

No arquivo `script.js`, coloque:

```javascript
const eventos = document.querySelectorAll('.evento');

for (const evento of eventos) {
  evento.addEventListener('click', () => {
    evento.classList.toggle('destacado');
  });
}
```

Agora acrescente ao `style.css`:

```css
.evento {
  cursor: pointer;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.evento:hover,
.evento.destacado {
  transform: translateY(-4px);
  box-shadow: 0 8px 18px rgb(37 99 235 / 25%);
}
```

Ao clicar em um evento, ele ficará destacado.

Esse exemplo mostra a divisão das três principais tecnologias do front-end:

```text
HTML       = estrutura
CSS        = aparência
JavaScript = comportamento
```

---

## 17. O modelo cliente-servidor

A Web funciona principalmente com base no modelo **cliente-servidor**.

### Cliente

O cliente é o programa que faz a solicitação. Normalmente, é um navegador como:

- Chrome;
- Firefox;
- Safari;
- Edge.

### Servidor

O servidor é o computador ou sistema que recebe a solicitação e fornece recursos ou serviços.

```text
Cliente: "Quero a página inicial."
                 ↓
Servidor: "Aqui está o HTML, o CSS e o JavaScript."
```

Exemplo de uma requisição feita pelo navegador:

```http
GET /produtos HTTP/1.1
Host: loja.exemplo
```

O servidor pode responder com HTML:

```html
<h1>Produtos disponíveis</h1>
```

Ou com dados em JSON:

```json
{
  "produto": "Caderno",
  "preco": 25.9
}
```

---

## 18. Criando um servidor local simples

Um arquivo HTML pode ser aberto diretamente pelo navegador usando um endereço `file://`. Porém, muitos recursos funcionam melhor quando a página é servida por um servidor local.

Se você tiver Python instalado, entre na pasta do projeto e execute:

```bash
python -m http.server 8000
```

No Windows, também pode ser necessário usar:

```bash
py -m http.server 8000
```

Depois, abra no navegador:

```text
http://localhost:8000
```

O servidor local fará com que os arquivos da pasta sejam disponibilizados por HTTP.

Para parar o servidor, volte ao terminal e pressione:

```text
Ctrl + C
```

### O que aconteceu?

```text
Navegador
    ↓
http://localhost:8000
    ↓
Servidor Python local
    ↓
index.html
```

O endereço `localhost` aponta para o próprio computador.

---

## 19. Testando HTTP pelo terminal com `curl`

O comando `curl` permite fazer requisições pela linha de comando.

Com um servidor local em execução, abra outro terminal e execute:

```bash
curl http://localhost:8000
```

O terminal mostrará o conteúdo retornado pelo servidor.

Para ver também os cabeçalhos da resposta:

```bash
curl -i http://localhost:8000
```

Um resultado possível:

```http
HTTP/1.0 200 OK
Server: SimpleHTTP/0.6 Python/3.x
Content-type: text/html

<!DOCTYPE html>
<html lang="pt-BR">
  ...
</html>
```

Esse exercício ajuda a perceber que uma página web é uma resposta enviada por um servidor ao cliente.

---

## 20. Sites estáticos e aplicações dinâmicas

### Site estático

Um site estático entrega arquivos que já existem, como:

- HTML;
- CSS;
- JavaScript;
- imagens.

Exemplo:

```text
servidor → index.html
servidor → style.css
servidor → script.js
```

Isso não significa que o site não tenha interações. Um site estático pode usar JavaScript no navegador.

### Aplicação dinâmica

Uma aplicação dinâmica pode gerar respostas com base em:

- usuário conectado;
- banco de dados;
- data e hora;
- produtos disponíveis;
- permissões;
- dados enviados por formulários.

Exemplo:

```text
usuário solicita sua conta
          ↓
servidor consulta o banco de dados
          ↓
servidor monta uma resposta personalizada
          ↓
navegador mostra os dados
```

Tecnologias de back-end podem incluir Node.js, Python, PHP, Java, Ruby, C# e outras.

---

## 21. O que é back-end?

O **back-end** é a parte da aplicação que roda no servidor. Ele normalmente cuida de:

- regras de negócio;
- autenticação;
- acesso a bancos de dados;
- processamento de pagamentos;
- envio de e-mails;
- criação de APIs;
- validações de segurança.

Um exemplo simplificado em JavaScript usando Node.js seria:

```javascript
const http = require('http');

const servidor = http.createServer((requisicao, resposta) => {
  resposta.writeHead(200, { 'Content-Type': 'text/plain; charset=utf-8' });
  resposta.end('Resposta enviada pelo servidor!');
});

servidor.listen(3000, () => {
  console.log('Servidor em http://localhost:3000');
});
```

Nesse exemplo, o servidor responde com texto quando alguém acessa a porta `3000`.

---

## 22. O que é front-end?

O **front-end** é a parte com a qual o usuário interage diretamente.

Ele inclui:

- conteúdo exibido na tela;
- botões;
- menus;
- formulários;
- cores;
- fontes;
- animações;
- comportamento no navegador.

As tecnologias fundamentais são:

```text
HTML       → estrutura do conteúdo
CSS        → aparência e layout
JavaScript → interações e lógica no navegador
```

Uma aplicação completa normalmente combina front-end e back-end:

```text
Navegador
  ├── HTML
  ├── CSS
  └── JavaScript
          ↓ HTTP/HTTPS
Servidor
  ├── regras da aplicação
  ├── banco de dados
  └── APIs
```

---

## 23. APIs e JSON

Uma **API** permite que sistemas diferentes se comuniquem.

Em aplicações web, é comum uma API responder com JSON.

Exemplo:

```json
{
  "nome": "Ana",
  "idade": 28,
  "cidade": "Recife"
}
```

O JavaScript pode buscar dados de uma API usando `fetch`:

```javascript
fetch('https://api.exemplo.com/usuarios/1')
  .then((resposta) => resposta.json())
  .then((dados) => {
    console.log(dados.nome);
  })
  .catch((erro) => {
    console.error('Não foi possível buscar os dados:', erro);
  });
```

Em aplicações modernas, o navegador pode carregar uma estrutura inicial e depois buscar dados sem recarregar a página inteira.

---

## 24. Da Web de documentos à Web de aplicações

No início, a Web era principalmente uma coleção de documentos interligados. Com o passar do tempo, tornou-se uma plataforma para aplicações completas.

Hoje podemos usar a Web para:

- editar documentos;
- assistir a vídeos;
- realizar videoconferências;
- comprar produtos;
- estudar;
- usar bancos;
- jogar;
- trabalhar em equipe;
- armazenar arquivos.

A evolução aconteceu graças à combinação de:

- conexões mais rápidas;
- navegadores mais capazes;
- JavaScript moderno;
- padrões web;
- servidores e bancos de dados;
- dispositivos móveis;
- computação em nuvem.

---

## 25. Web responsiva e dispositivos móveis

Com a popularização dos celulares, surgiu a necessidade de criar páginas que se adaptassem a diferentes tamanhos de tela.

Uma parte essencial é a meta tag `viewport`:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Também usamos CSS responsivo:

```css
.container {
  width: min(90%, 900px);
  margin: 0 auto;
}

@media (max-width: 600px) {
  h1 {
    font-size: 1.7rem;
  }
}
```

Esse recurso permite aplicar estilos específicos quando a tela é menor.

---

## 26. A importância dos padrões web

A Web é formada por tecnologias e padrões que permitem que diferentes navegadores e dispositivos interpretem os mesmos documentos.

Padrões ajudam a garantir:

- compatibilidade;
- acessibilidade;
- previsibilidade;
- interoperabilidade;
- manutenção do código.

Uma boa prática é utilizar HTML semântico:

```html
<header>Topo da página</header>
<nav>Menu de navegação</nav>
<main>Conteúdo principal</main>
<aside>Conteúdo complementar</aside>
<footer>Rodapé</footer>
```

Em vez de usar apenas vários elementos genéricos:

```html
<div>Topo</div>
<div>Menu</div>
<div>Conteúdo</div>
<div>Rodapé</div>
```

O HTML semântico melhora a compreensão da página por navegadores, mecanismos de busca e leitores de tela.

---

## 27. Linha do tempo resumida

```text
Década de 1960  → pesquisas com redes de computadores
1969            → ARPANET começa a conectar instituições
Década de 1980  → expansão dos protocolos de rede
1989            → proposta da World Wide Web
1990            → criação das primeiras ferramentas da Web
1991            → Web começa a ser disponibilizada publicamente
Década de 1990  → popularização de navegadores e sites
Anos 2000       → Web 2.0, redes sociais e aplicações interativas
Anos 2010       → crescimento do mobile, APIs e aplicações web
Hoje            → aplicações completas, nuvem, streaming e serviços online
```

A história não é uma sequência de tecnologias que substituem totalmente as anteriores. HTML, HTTP e URLs continuam sendo usados, mas evoluíram junto com novos recursos.

---

## 28. Exercício prático: observar uma página no navegador

Você pode investigar qualquer página usando as ferramentas de desenvolvedor do navegador.

### Passo 1: abrir as ferramentas

No navegador, pressione:

```text
F12
```

Ou use:

```text
Ctrl + Shift + I
```

No macOS:

```text
Command + Option + I
```

### Passo 2: observar o HTML

Na aba **Elements** ou **Inspector**, você verá a estrutura HTML da página.

### Passo 3: observar as requisições

Na aba **Network**, recarregue a página e observe:

- documentos HTML;
- arquivos CSS;
- arquivos JavaScript;
- imagens;
- códigos de status;
- tempo de carregamento.

### Passo 4: selecionar uma requisição

Ao selecionar um recurso, você poderá observar informações como:

- URL;
- método HTTP;
- cabeçalhos;
- resposta;
- status `200`, `404` ou outro;
- tempo de resposta.

Esse exercício conecta a teoria com o que realmente acontece quando uma página é carregada.

---

## 29. Exercício prático: criar uma requisição com formulário

O HTML também permite enviar dados ao servidor.

```html
<form action="/cadastro" method="post">
  <label for="nome">Nome:</label>
  <input id="nome" name="nome" type="text" required />

  <label for="email">E-mail:</label>
  <input id="email" name="email" type="email" required />

  <button type="submit">Cadastrar</button>
</form>
```

Nesse exemplo:

- `action` indica para onde os dados serão enviados;
- `method="post"` indica o método HTTP;
- `name` identifica cada campo;
- `required` exige o preenchimento.

Um servidor poderia receber esses dados e armazená-los em um banco de dados.

---

## 30. O que estudar depois?

Depois de entender os fundamentos, uma sequência possível de estudos é:

1. HTML semântico;
2. CSS básico;
3. Flexbox;
4. CSS Grid;
5. design responsivo;
6. JavaScript básico;
7. manipulação do DOM;
8. eventos;
9. requisições com `fetch`;
10. Git e GitHub;
11. criação de APIs;
12. bancos de dados;
13. segurança web;
14. frameworks front-end ou back-end.

Não é necessário aprender tudo de uma vez. A melhor estratégia é criar projetos pequenos e aumentar a dificuldade gradualmente.

---

## 31. Checklist de revisão

Verifique se você consegue explicar:

- [ ] a diferença entre Internet e Web;
- [ ] o que é HTML;
- [ ] o que é CSS;
- [ ] o que é JavaScript;
- [ ] o que é HTTP;
- [ ] o que é HTTPS;
- [ ] o que é uma URL;
- [ ] para que serve o DNS;
- [ ] o que é cliente;
- [ ] o que é servidor;
- [ ] o que é front-end;
- [ ] o que é back-end;
- [ ] o significado do código HTTP `404`;
- [ ] como iniciar um servidor local;
- [ ] como observar requisições nas ferramentas do navegador.

---

## Conclusão

A programação web nasceu da combinação de uma necessidade simples: compartilhar informações entre computadores de forma organizada.

A partir dessa ideia surgiram o HTML, o HTTP e as URLs. Com o tempo, o CSS trouxe recursos visuais, o JavaScript adicionou interatividade e os servidores passaram a processar dados, usuários e regras de negócio.

Hoje, a Web é muito mais do que um conjunto de páginas. Ela é uma plataforma completa para documentos, comunicação, comércio, educação, entretenimento e aplicações empresariais.

Mesmo com todas as tecnologias modernas, o funcionamento básico continua baseado em uma ideia fundamental:

```text
um cliente solicita um recurso
        ↓
um servidor processa a solicitação
        ↓
uma resposta retorna pela rede
        ↓
o navegador apresenta o resultado
```

Ao entender esse ciclo, fica muito mais fácil estudar HTML, CSS, JavaScript, servidores, APIs e qualquer outra tecnologia relacionada ao desenvolvimento web.
