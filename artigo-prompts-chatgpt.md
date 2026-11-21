# Como escrever prompts melhores para o ChatGPT: um guia prático baseado na documentação oficial

Escrever um bom prompt não significa decorar fórmulas complexas. Na maioria das situações, basta explicar com clareza o que você precisa, fornecer o contexto relevante e indicar como pretende usar o resultado.

A documentação oficial resume essa abordagem em quatro elementos principais:

- **Objetivo:** o que o ChatGPT deve fazer;
- **Contexto:** quais informações, arquivos ou fontes podem influenciar o resultado;
- **Saída:** qual formato, tamanho, público ou nível de detalhe você espera;
- **Limites:** o que deve ser preservado, evitado ou submetido à sua revisão.

Você não precisa usar todos esses elementos em todo prompt. Uma pergunta simples pode ser suficiente. Porém, quanto mais importante ou complexa for a tarefa, mais útil será explicitar esses pontos.

## 1. Comece pelo resultado desejado

Em vez de descrever uma longa sequência de passos, comece dizendo qual resultado você quer obter. O ChatGPT pode ajudar a organizar a abordagem, comparar alternativas e decidir quais etapas são necessárias.

Também informe o público e o formato quando esses fatores alterarem a resposta.

### Exemplo fraco

> Analise estas anotações e faça algumas mudanças.

### Exemplo melhor

> Transforme estas anotações de reunião em uma atualização curta para a equipe do projeto. Coloque as decisões e os próximos passos no início.

O segundo exemplo esclarece o produto final e a prioridade editorial, sem controlar cada detalhe do processo.

## 2. Adicione apenas o contexto que muda a resposta

Contexto é tudo aquilo que pode alterar a qualidade ou a direção do resultado. Inclua as informações relevantes, mas evite despejar material que não tenha relação com a tarefa.

Você pode fornecer contexto de várias formas:

- anexando documentos, planilhas, apresentações ou PDFs;
- enviando uma captura de tela, imagem ou diagrama;
- indicando quais partes de um arquivo devem ser consideradas;
- solicitando pesquisa na web quando a resposta depender de informações atuais;
- usando um projeto para reunir conversas, arquivos e fontes relacionadas.

Ao anexar uma fonte, explique o que o ChatGPT deve extrair dela. Por exemplo:

> Use o relatório trimestral anexo para identificar os três principais riscos e cite a página de onde cada dado foi extraído.

Isso é mais útil do que apenas dizer “analise o arquivo”, porque define o foco da análise.

## 3. Especifique fontes conectadas e informações atuais

Quando a tarefa depender de fontes externas ou conectadas, indique onde o ChatGPT deve procurar e o que precisa encontrar. Não é necessário descrever cada busca individual.

Por exemplo:

> Use o plano mais recente do projeto no Drive e as decisões publicadas no canal do Slack da equipe para preparar uma atualização de status.

Se o assunto for atual — como preços, legislação, concorrentes, notícias ou versões de produtos — peça explicitamente uma pesquisa na web e solicite links ou fontes para conferência.

Sempre diferencie fatos fornecidos pelas fontes de interpretações ou recomendações produzidas pelo modelo. Essa separação facilita a revisão e reduz o risco de tratar uma análise como se fosse um dado comprovado.

## 4. Defina limites para evitar problemas reais

Limites são as poucas instruções que impedem alterações indesejadas ou ações não planejadas. Eles são especialmente importantes quando um detalhe errado pode inutilizar o resultado ou quando outras pessoas podem ser afetadas.

Exemplos de limites úteis:

- Mantenha inalteradas as datas aprovadas e os valores do orçamento.
- Use somente as fontes fornecidas e sinalize informações ausentes em vez de adivinhar.
- Mantenha as recomendações dentro do orçamento indicado.
- Prepare a mensagem como rascunho; não a envie.
- Não publique nem altere informações sem minha aprovação.

Concentre-se em uma ou duas restrições realmente importantes. Tentar controlar cada passo do trabalho costuma deixar o prompt mais pesado sem necessariamente melhorar o resultado.

## 5. Diga como o resultado será usado

O uso final ajuda o ChatGPT a escolher o tamanho, o nível de detalhe e a organização adequados.

Compare estas instruções:

> Resuma o relatório.

> Faça um resumo de uma página para um diretor consultar antes da reunião. Coloque a decisão necessária e os próximos passos no início.

A segunda versão fornece um critério editorial claro. Outros exemplos:

- Transforme estas anotações em um e-mail de acompanhamento com decisões, responsáveis e prazos.
- Crie uma tabela comparando gastos planejados e reais e destaque diferenças superiores a 10%.
- Prepare um memorando de recomendação com links, premissas e perguntas que precisam ser respondidas antes da contratação.

Para trabalhos importantes, peça também uma verificação final. Você pode solicitar que o ChatGPT confirme se cada ação tem responsável e prazo, sinalize dados não verificados ou confira se dois documentos estão consistentes entre si.

## 6. Refine a resposta em vez de recomeçar

O primeiro prompt não precisa ser perfeito. Uma das vantagens de trabalhar em uma conversa é poder analisar o resultado e pedir alterações específicas.

Exemplos de mensagens de acompanhamento:

- Torne a abertura mais direta, preserve as evidências e mova a recomendação para antes do contexto.
- Reduza o texto para 120 palavras e mantenha um tom cordial.
- Transforme a seção de comparação em uma tabela.
- Inclua os responsáveis e os prazos que aparecem nas anotações.
- Apresente uma alternativa mais conservadora e explique o principal compromisso envolvido.

Pedidos de refinamento funcionam melhor quando indicam exatamente o que deve mudar e o que deve ser preservado.

## 7. Um modelo simples de prompt

Você pode usar o seguinte modelo como ponto de partida:

> **Objetivo:** [o que deve ser feito]
>
> **Contexto:** [informações, arquivos ou fontes relevantes]
>
> **Resultado:** [formato, público, extensão e nível de detalhe]
>
> **Limites:** [o que deve ser preservado, evitado ou revisado antes de qualquer ação]
>
> **Verificação:** [o que deve ser conferido antes da conclusão]

### Exemplo completo

> Prepare uma atualização de status de uma página para a reunião de liderança de segunda-feira. Use o plano mais recente do projeto no Drive e as decisões e atualizações relevantes do canal do Slack.
>
> Comece pelas decisões que a liderança precisa tomar e pelos próximos passos. Resuma progresso, riscos, responsáveis e prazos. Mantenha inalterados os valores aprovados do orçamento e as datas já confirmadas. Sinalize informações conflitantes ou ausentes e não envie nem publique nada.
>
> Antes de concluir, verifique se todo próximo passo tem um responsável e uma data de vencimento.

Esse prompt combina objetivo, contexto, formato, limites e verificação sem impor uma lista desnecessária de etapas.

## 8. Escolha a ferramenta de acordo com a tarefa

A documentação também diferencia tipos de trabalho.

### Chat para tarefas rápidas

Use o ChatGPT para perguntas, ideias, pequenas reescritas, comparações e rascunhos leves. Exemplos:

> Explique como funciona o juro composto para alguém que nunca investiu. Use um exemplo concreto e defina os termos financeiros.

> Compare estes dois planos de celular para uma pessoa que viaja ao exterior duas vezes por ano. Mostre as diferenças importantes em uma tabela e recomende um deles, explicando o compromisso envolvido.

### Trabalho com várias fontes ou etapas

Para tarefas que usam múltiplos arquivos, ferramentas ou fontes, envolvem pesquisa, criam documentos maiores ou exigem uma sequência de etapas, descreva o resultado final, forneça o material de origem e indique como o trabalho deverá ser revisado.

Um exemplo:

> Use os relatórios trimestrais anexos para criar um briefing executivo e uma apresentação de seis slides. O público é a diretoria. Comece pelas três decisões que precisam ser tomadas, diferencie fatos reportados de análises, cite cada número com seu arquivo de origem e confirme que o briefing e os slides estão consistentes antes de concluir.

Para tarefas recorrentes, refine primeiro o prompt em uma conversa normal. Quando o resultado estiver confiável, transforme o fluxo em uma tarefa agendada, se essa função estiver disponível.

## 9. Prompts para programação e Codex

Em tarefas de código, um prompt eficaz deve incluir o comportamento desejado, o contexto técnico relevante, os passos para reproduzir o problema, as restrições e a forma de verificação.

### Explicar uma base de código

> Explique como uma requisição percorre o código selecionado. Inclua um resumo das responsabilidades de cada módulo, indique onde os dados são validados e liste dois pontos de atenção para futuras alterações. Depois, resuma o fluxo em uma lista numerada e informe os arquivos envolvidos.

### Corrigir um bug

> Bug: clicar em “Salvar” na tela de configurações mostra “Salvo”, mas a alteração não persiste.
>
> Reprodução:
> 1. Execute `npm run dev`.
> 2. Acesse `/settings`.
> 3. Ative “Habilitar alertas”.
> 4. Clique em “Salvar”.
> 5. Atualize a página; a opção volta ao estado anterior.
>
> Restrições: não altere o formato da API, mantenha a correção mínima e adicione um teste de regressão se for viável. Comece reproduzindo o problema, proponha o patch e execute as verificações relevantes.

### Criar um teste

> Adicione um teste para a função `invert_list` em `transform.ts`. Cubra o caso normal e os casos extremos, seguindo as convenções dos testes existentes.

### Alterar uma interface a partir de uma imagem

> Crie uma nova página de configurações usando a imagem anexada como referência visual. Siga os padrões de design já existentes no projeto. Use React, Vite, Tailwind e TypeScript. Inclua os estados de validação, interação por teclado e comportamento responsivo que não aparecem na imagem. Ao terminar, informe a rota local para visualizar o protótipo e como executá-lo.

Sempre peça uma forma concreta de verificação: executar os testes, reproduzir o bug novamente, rodar lint, iniciar o servidor ou explicar como conferir a mudança na interface.

## 10. Checklist antes de enviar um prompt

Antes de enviar, faça estas perguntas:

1. Deixei claro qual resultado quero?
2. Forneci apenas o contexto que pode alterar a resposta?
3. Expliquei o formato, o público ou o nível de detalhe necessário?
4. Indiquei o que deve permanecer inalterado?
5. Pedi para sinalizar lacunas em vez de adivinhar?
6. Solicitei fontes quando a informação precisar ser verificada?
7. Defini uma revisão final para tarefas importantes?
8. Evitei controlar etapas que não são relevantes?

Se as respostas forem “sim” para os itens importantes, o prompt provavelmente já está suficientemente claro.

## Conclusão

Prompts eficazes são instruções claras, não fórmulas rígidas. Comece pelo resultado, adicione contexto relevante, estabeleça os limites essenciais e explique como o material será usado. Depois, revise a primeira resposta e faça pedidos específicos de melhoria.

O princípio mais importante é simples: não tente escrever o prompt perfeito de primeira. Use a conversa para orientar, corrigir e validar o trabalho. Para tarefas maiores, combine essa abordagem com fontes bem escolhidas, critérios de verificação e aprovação humana antes de enviar, publicar ou alterar algo que afete outras pessoas.

*Baseado na documentação oficial de prompting fornecida pelo usuário. Consulte a versão original para detalhes de disponibilidade de recursos, planos e interfaces.*
