# Engenharia de prompts para Claude: como começar, testar e melhorar seus resultados

A engenharia de prompts é o processo de criar, testar e aperfeiçoar instruções para orientar um modelo de inteligência artificial a produzir respostas mais úteis e consistentes. No caso do Claude, a documentação oficial apresenta uma recomendação importante: antes de tentar “melhorar o prompt”, defina claramente o que significa sucesso e descubra como medir esse sucesso.

Esse ponto muda a forma de trabalhar com IA. Um prompt não deve ser considerado bom apenas porque parece detalhado ou porque produz uma resposta interessante em um teste isolado. Ele deve ser avaliado de acordo com critérios objetivos e repetíveis.

## O que é necessário antes de ajustar um prompt

A documentação do Claude recomenda começar com três elementos:

1. **Uma definição clara dos critérios de sucesso do caso de uso.**
2. **Formas de testar os resultados em relação a esses critérios.**
3. **Um primeiro rascunho do prompt que possa ser aprimorado.**

Sem esses elementos, é difícil saber se uma alteração realmente melhorou o sistema ou apenas produziu uma resposta diferente.

### 1. Defina o que é sucesso

Os critérios de sucesso devem descrever o resultado esperado de maneira observável. Dependendo da aplicação, eles podem incluir:

- precisão das informações;
- aderência a um formato específico;
- completude da resposta;
- tom de voz adequado;
- capacidade de seguir regras de negócio;
- redução de erros ou ambiguidades;
- consistência entre diferentes entradas;
- tempo de resposta e custo de execução.

Por exemplo, em um classificador de mensagens, sucesso pode significar classificar corretamente pelo menos 95% de um conjunto de exemplos avaliados. Em um gerador de respostas para atendimento, pode significar responder com clareza, não inventar informações e encaminhar corretamente os casos que exigem intervenção humana.

### 2. Crie uma forma de testar

Depois de definir os critérios, prepare exemplos que representem o uso real. Esses exemplos devem incluir tanto situações comuns quanto casos difíceis, ambíguos ou fora do padrão.

Um teste útil pode verificar se o Claude:

- respondeu ao que foi solicitado;
- respeitou as instruções de formato;
- usou somente as informações permitidas;
- reconheceu quando faltavam dados;
- evitou conclusões indevidas;
- manteve o tom esperado;
- produziu uma resposta semelhante em casos equivalentes.

A avaliação pode ser manual, automática ou uma combinação das duas. O essencial é comparar versões do prompt usando um conjunto de testes consistente.

### 3. Comece com um rascunho

Não é necessário criar um prompt perfeito antes de iniciar. Um primeiro rascunho serve como ponto de partida para observar o comportamento do modelo e identificar o que precisa ser corrigido.

Um rascunho simples pode ser:

> Leia a mensagem do cliente e classifique o assunto em uma das categorias disponíveis. Explique brevemente a decisão.

A partir dos primeiros resultados, podem surgir necessidades mais específicas: definir categorias, exigir um formato JSON, impedir que o modelo invente dados ou indicar como agir quando a mensagem não se encaixar em nenhuma opção.

## Quando a engenharia de prompts é a solução certa

Nem todo problema de uma aplicação de IA deve ser resolvido com um prompt mais elaborado. A documentação destaca que a engenharia de prompts é adequada para critérios que podem ser influenciados pelas instruções dadas ao modelo.

Antes de alterar o prompt, pergunte:

- O modelo entendeu mal a tarefa?
- A saída está no formato errado?
- Faltam exemplos ou contexto?
- As regras importantes não foram explicadas?
- O comportamento esperado não foi definido para casos ambíguos?

Se a resposta for sim, revisar o prompt pode ajudar.

Por outro lado, alguns problemas têm outra causa. Latência e custo, por exemplo, podem ser melhorados escolhendo um modelo diferente. Em determinadas situações, também pode ser necessário alterar a arquitetura da aplicação, melhorar os dados fornecidos ao modelo, mudar o fluxo de ferramentas ou criar uma etapa separada de validação.

A conclusão prática é: primeiro identifique a causa da falha; só depois decida se deve investir em engenharia de prompts.

## Técnicas de prompting para Claude

A documentação do Claude indica que as principais técnicas estão reunidas no guia de melhores práticas de prompting. Entre os temas citados estão:

- clareza nas instruções;
- uso de exemplos;
- estruturação com XML;
- prompting de papéis;
- orientação do raciocínio;
- encadeamento de prompts.

Essas técnicas não são receitas isoladas. A escolha depende do comportamento que você deseja obter e dos critérios usados para avaliar o resultado.

### Clareza nas instruções

Explique o objetivo, o contexto, o formato esperado e as restrições relevantes. Evite instruções vagas como “faça uma análise completa” quando você pode especificar o que a análise deve conter.

Em vez de:

> Analise este contrato.

Prefira algo como:

> Analise este contrato sob a perspectiva de uma pequena empresa. Resuma as obrigações principais, identifique cláusulas de renovação e destaque riscos que exigem revisão jurídica. Não faça afirmações sobre a validade legal definitiva do documento.

A segunda versão define o foco, o público e os limites da tarefa.

### Uso de exemplos

Exemplos ajudam o modelo a entender o padrão de entrada e saída esperado. Eles são especialmente úteis quando a tarefa envolve classificação, extração de dados, estilo ou regras que seriam difíceis de explicar apenas em texto.

Um exemplo pode mostrar:

- uma entrada;
- a resposta desejada;
- o formato exato;
- como lidar com uma exceção.

Se houver casos importantes que não devem ser esquecidos, inclua exemplos desses casos também.

### Estruturação com XML

A estruturação com tags XML pode separar instruções, contexto, documentos e critérios de resposta. Isso torna prompts longos mais legíveis e ajuda a indicar a função de cada trecho.

Por exemplo:

```xml
<instructions>
Classifique o feedback do cliente em uma categoria.
Responda somente com a categoria e uma justificativa de uma frase.
</instructions>

<categories>
- cobrança
- suporte técnico
- cancelamento
- elogio
- outro
</categories>

<customer_message>
O aplicativo fecha sempre que tento enviar uma foto.
</customer_message>
```

A estrutura não substitui instruções claras, mas pode ajudar a organizar informações com papéis diferentes.

### Prompting de papéis

Definir um papel pode fornecer contexto para a tarefa, principalmente quando o modelo precisa adotar uma perspectiva profissional, um público específico ou um padrão de comunicação.

Por exemplo:

> Você é um analista de suporte técnico que escreve para usuários não especialistas. Explique o problema sem jargão desnecessário e indique passos seguros para diagnóstico.

O papel deve servir ao objetivo da tarefa, e não ser usado apenas como decoração. O resultado ainda precisa ser avaliado pelos critérios definidos anteriormente.

### Orientação do raciocínio

Para tarefas complexas, pode ser útil pedir uma abordagem organizada, uma justificativa resumida ou uma verificação dos critérios. O objetivo é tornar o processo mais confiável e facilitar a avaliação da resposta.

Em vez de solicitar uma explicação extensa sem propósito, defina o que precisa ser conferido:

> Compare as duas propostas, liste os critérios usados, indique qual alternativa atende melhor a cada critério e finalize com uma recomendação. Sinalize qualquer informação que não esteja disponível.

A solicitação deve ser adequada ao caso de uso e ao formato que você realmente precisa receber.

### Encadeamento de prompts

Nem toda tarefa precisa ser resolvida em um único prompt. Quando o trabalho envolve etapas diferentes, pode ser mais confiável dividir o processo.

Um fluxo possível é:

1. extrair os dados relevantes;
2. verificar se os dados estão completos;
3. analisar as alternativas;
4. produzir a resposta final;
5. validar o resultado.

O encadeamento permite avaliar cada etapa separadamente e identificar onde ocorre uma falha. Também pode tornar o sistema mais fácil de ajustar do que um prompt único e excessivamente complexo.

## Como melhorar um prompt de forma sistemática

Um processo prático de melhoria pode seguir estas etapas:

### Etapa 1: registre o comportamento atual

Guarde o prompt inicial, os exemplos usados e as respostas produzidas. Sem esse registro, fica difícil comparar versões.

### Etapa 2: identifique a falha

Descreva o problema de maneira específica. “A resposta ficou ruim” é pouco útil. “O modelo omitiu o prazo em quatro de dez casos” fornece uma direção concreta.

### Etapa 3: altere uma coisa por vez

Sempre que possível, mude apenas um aspecto do prompt: uma instrução, um exemplo, o formato ou uma regra. Isso ajuda a entender qual alteração produziu o efeito observado.

### Etapa 4: execute novamente os testes

Avalie a nova versão no mesmo conjunto de exemplos. Verifique não apenas se o caso que falhou foi corrigido, mas também se outras respostas pioraram.

### Etapa 5: compare qualidade, custo e latência

Uma alteração pode melhorar a precisão, mas aumentar muito o tamanho da resposta ou o tempo de execução. O melhor prompt é aquele que atende aos critérios relevantes do produto, não necessariamente aquele que gera a resposta mais longa.

### Etapa 6: mantenha a versão aprovada

Quando uma versão apresentar resultados melhores e consistentes, registre o prompt, os testes e as limitações conhecidas. Isso facilita futuras mudanças e evita regressões.

## Recursos oficiais para continuar aprendendo

A documentação apresenta diferentes caminhos de estudo:

- **Guia de melhores práticas de prompting:** referência principal para técnicas específicas dos modelos mais recentes do Claude.
- **Postagem sobre melhores práticas de engenharia de prompts:** visão mais geral sobre o processo de criação e aperfeiçoamento de prompts.
- **Tutorial interativo no GitHub:** material com exemplos sobre fundamentos de engenharia de prompts. A documentação observa que ele foi escrito para modelos Claude 3; quando houver divergência, deve-se priorizar o guia atualizado de melhores práticas.
- **Tutorial interativo no Google Sheets:** versão mais leve do tutorial, organizada em formato de planilha.
- **Notebook gerador de prompts:** recurso do Claude Cookbook para quem ainda não possui um primeiro rascunho e deseja gerar uma base inicial usando uma abordagem de metaprompt.
- **Guia sobre critérios de sucesso e avaliações:** referência para definir como medir o desempenho antes de começar os ajustes.

## Checklist para avaliar um prompt

Antes de considerar um prompt pronto, verifique:

- O objetivo está claro?
- Os critérios de sucesso são observáveis?
- Existe um conjunto de exemplos para teste?
- O prompt informa o formato e o nível de detalhe esperados?
- As restrições importantes estão explícitas?
- Há instruções para lidar com informações ausentes ou ambiguidades?
- Os exemplos representam casos comuns e casos difíceis?
- O resultado será avaliado em mais de uma entrada?
- A alteração melhorou o resultado sem elevar excessivamente custo ou latência?
- Existe uma forma de detectar regressões depois?

## Conclusão

A engenharia de prompts para Claude deve começar antes da escolha das palavras exatas. Primeiro, defina o que significa sucesso, crie uma forma de testar e prepare um rascunho. Em seguida, use técnicas como clareza, exemplos, estruturação com XML, definição de papéis, orientação do raciocínio e encadeamento de prompts conforme a necessidade.

Também é importante reconhecer quando o prompt não é o problema principal. Se a falha estiver relacionada a custo, latência, modelo, dados ou arquitetura, uma simples reformulação pode não resolver a situação.

O melhor processo é experimental e mensurável: formular uma hipótese, alterar o prompt, testar os resultados, comparar os efeitos e registrar o que funcionou. Dessa forma, a engenharia de prompts deixa de ser tentativa e erro e passa a fazer parte de um processo confiável de desenvolvimento de aplicações com IA.

### Referências da documentação fornecida

- [Visão geral da engenharia de prompts](https://platform.claude.com/docs/pt-BR/build-with-claude/prompt-engineering/overview)
- [Melhores práticas de prompting](https://platform.claude.com/docs/pt-BR/build-with-claude/prompt-engineering/claude-prompting-best-practices)
- [Defina critérios de sucesso e crie avaliações](https://platform.claude.com/docs/pt-BR/test-and-evaluate/develop-tests)
- [Tutorial interativo no GitHub](https://github.com/anthropics/prompt-eng-interactive-tutorial)
- [Notebook gerador de prompts](https://colab.research.google.com/github/anthropics/claude-cookbooks/blob/main/misc/metaprompt.ipynb)
