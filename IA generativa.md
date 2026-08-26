# Como a IA generativa funciona na prática

A inteligência artificial generativa é capaz de criar um conteúdo novo a partir de padrões aprendidos durante o treinamento. Esse conteúdo pode ser um texto, uma imagem, um código, um áudio ou até a estrutura inicial de um projeto.

Isso não significa que a IA inventa tudo do zero da mesma forma que uma pessoa. Ela analisa o contexto recebido e calcula qual saída faz mais sentido com base nos padrões que aprendeu.

## IA generativa e IA tradicional

Nem todo sistema de inteligência artificial é generativo.

Um sistema tradicional pode analisar informações e classificá-las. Um filtro de e-mail, por exemplo, avalia uma mensagem e decide se ela é spam. Já uma IA generativa pode escrever um e-mail novo com base no objetivo, no destinatário e no tom informados pelo usuário.

| Tipo de sistema | O que faz | Exemplo prático |
| --- | --- | --- |
| Classificação | Separa informações em categorias | Identificar spam |
| Predição | Estima um resultado futuro | Prever a demanda de um produto |
| Recomendação | Seleciona itens relevantes | Recomendar filmes |
| Reconhecimento | Identifica padrões em dados | Extrair texto de uma imagem |
| IA generativa | Produz um conteúdo novo | Criar um texto, código ou imagem |

Essas funções também podem trabalhar juntas.

Um sistema pode usar reconhecimento óptico de caracteres para extrair informações de uma folha, classificar os dados encontrados e depois usar IA generativa para apresentar um resumo.

## O que é um LLM

Um **Grande Modelo de Linguagem**, conhecido pela sigla **LLM**, é um tipo de IA generativa especializado em processar e produzir linguagem.

Modelos como Claude e GPT recebem uma sequência de texto, analisam o contexto e calculam quais continuações são mais adequadas.

O nome pode ser dividido em três partes:

- **modelo:** estrutura matemática criada durante o treinamento;
- **linguagem:** principal tipo de informação processada;
- **grande:** referência à quantidade de parâmetros, dados e processamento envolvidos.

Os parâmetros são valores numéricos ajustados durante o treinamento. Eles determinam como o modelo reage aos padrões encontrados na entrada.

Um LLM não possui uma lista pronta com todas as perguntas e respostas possíveis. Ele gera cada resposta com base no contexto disponível naquele momento.

## O que tornou os modelos atuais possíveis

O avanço da IA generativa aconteceu pela combinação de três elementos: arquitetura, dados e capacidade de processamento.

## Arquitetura

As redes neurais existem há décadas, mas arquiteturas mais recentes permitiram trabalhar melhor com grandes sequências de texto.

Uma das principais é a arquitetura **Transformer**. Ela utiliza mecanismos de atenção para identificar quais partes de uma informação são mais relevantes entre si.

Considere a frase:

> O computador não acessava a internet porque o servidor DHCP não respondeu.

Para interpretar essa frase, o modelo precisa relacionar a falha de acesso à ausência de resposta do DHCP. O mecanismo de atenção ajuda a considerar essas relações mesmo quando os termos estão separados por várias palavras ou parágrafos.

Isso é importante em tarefas como:

- interpretar requisitos de um projeto;
- revisar códigos extensos;
- acompanhar uma conversa;
- resumir documentos;
- relacionar informações apresentadas em partes diferentes de um texto.

## Dados

Um modelo precisa analisar uma grande quantidade de exemplos para aprender padrões da linguagem.

Esses exemplos permitem reconhecer:

- estrutura de frases;
- relações entre conceitos;
- formatos de documentos;
- padrões de programação;
- estilos de escrita;
- formas comuns de responder a perguntas.

O modelo não recebe uma explicação manual para cada situação possível. Ele aprende regularidades presentes nos dados.

Por isso, a qualidade, a diversidade e a organização desses dados influenciam diretamente o comportamento final.

## Poder computacional

Treinar modelos grandes exige muitos cálculos.

Equipamentos especializados, como GPUs e TPUs, conseguem executar diversas operações matemáticas em paralelo. Vários equipamentos também podem trabalhar juntos em clusters.

Essa infraestrutura permite processar grandes conjuntos de dados e ajustar bilhões de parâmetros.

O treinamento de um modelo moderno, portanto, não depende apenas de um bom algoritmo. Também depende de infraestrutura, energia, armazenamento e capacidade de distribuir o processamento.

## Como acontece o treinamento

O desenvolvimento de um modelo de linguagem pode ser separado em duas etapas principais: pré-treinamento e pós-treinamento.

## Pré-treinamento

No pré-treinamento, o modelo aprende padrões gerais da linguagem.

O processo pode ser representado assim:

1. Um texto é dividido em unidades menores chamadas tokens.
2. Parte da sequência é apresentada ao modelo.
3. O modelo tenta prever qual token deve aparecer em seguida.
4. A previsão é comparada com o resultado esperado.
5. Os parâmetros são ajustados para reduzir o erro.
6. O processo se repete com muitos exemplos.

Considere a frase incompleta:

> Antes de alterar o código, preciso criar um...

Dependendo do contexto, palavras como `backup`, `teste` ou `plano` podem ser continuações prováveis.

O modelo calcula probabilidades para essas possibilidades. Durante o treinamento, ele ajusta seus parâmetros para melhorar essas previsões.

Ao repetir esse processo em grande escala, o modelo aprende muito mais do que completar frases simples. Ele identifica estruturas, relações, padrões de código e formas de organizar ideias.

Mesmo assim, seu mecanismo básico continua sendo a previsão de tokens.

## Pós-treinamento

Depois do pré-treinamento, o modelo sabe produzir texto, mas ainda precisa aprender a funcionar como assistente.

No pós-treinamento, ele pode ser ajustado para:

- seguir instruções;
- respeitar formatos;
- responder de forma mais útil;
- recusar solicitações inadequadas;
- reconhecer limites;
- reduzir comportamentos prejudiciais;
- adaptar o tom da resposta.

Esse processo pode utilizar exemplos de respostas, avaliações humanas, princípios de segurança e diferentes formas de aprendizado por reforço.

Por isso, dois modelos construídos sobre tecnologias parecidas podem apresentar comportamentos muito diferentes.

## Como uma resposta é criada

Quando o modelo já está treinado e recebe uma solicitação, começa a etapa chamada **inferência**.

A entrada é dividida em tokens. O modelo analisa esses tokens e calcula uma distribuição de probabilidades para o próximo.

Depois que um token é escolhido, ele é adicionado à sequência. O modelo repete o cálculo até concluir a resposta.

O fluxo simplificado é:

```text
Instrução do usuário
        ↓
Divisão em tokens
        ↓
Análise do contexto
        ↓
Cálculo do próximo token
        ↓
Token adicionado à sequência
        ↓
Repetição até concluir a resposta
```

Isso explica por que a mesma pergunta pode gerar respostas diferentes.

A saída depende de fatores como:

- contexto disponível;
- forma como a pergunta foi escrita;
- exemplos fornecidos;
- instruções do sistema;
- ferramentas conectadas;
- configuração utilizada para selecionar os tokens.

## Por que a IA pode errar com confiança

O modelo tenta produzir uma continuação coerente. Ele não possui, em seu funcionamento básico, um mecanismo que garanta a verdade de cada frase.

Uma resposta pode estar:

- bem escrita;
- organizada;
- tecnicamente convincente;
- completamente errada.

Isso acontece porque coerência e verdade não são a mesma coisa.

Se eu pedir um código para Apps Script, o modelo pode escrever uma função válida, mas interpretar de forma errada qual coluna deve ser atualizada.

Se eu perguntar sobre uma configuração de rede, ele pode sugerir um comando real que não se aplica ao meu sistema operacional.

Por isso, a resposta precisa passar por testes e validação humana.

## O modelo não pesquisa automaticamente

Um LLM não acessa automaticamente a internet, um banco de dados ou os arquivos do computador.

Sem ferramentas externas, ele responde com base em:

- padrões aprendidos durante o treinamento;
- instruções recebidas;
- conteúdo disponível na conversa.

Porém, uma aplicação pode conectar o modelo a ferramentas como:

- busca na internet;
- arquivos;
- banco de dados;
- APIs;
- calculadora;
- terminal;
- editor de código;
- sistemas empresariais.

Essa diferença é importante.

Quando o modelo responde apenas com seu conhecimento interno, a informação pode estar desatualizada. Quando utiliza uma ferramenta de busca, ele pode consultar uma fonte atual. Mesmo assim, ainda é necessário verificar se interpretou a fonte corretamente.

## Exemplo prático: criar uma automação com Apps Script

Imagine que preciso automatizar uma planilha que calcula quantos dias faltam para o vencimento de um item.

Se eu enviar apenas:

> Crie um script para calcular os dias.

O modelo terá que adivinhar grande parte do processo.

Ele não sabe:

- em qual coluna está a data;
- onde deve escrever o resultado;
- se existem várias páginas;
- como tratar células vazias;
- se valores negativos são permitidos;
- quando o script deve ser executado.

Uma instrução mais completa seria:

> Crie um Apps Script para uma planilha com várias páginas que seguem a mesma estrutura. A data de validade está na coluna 8 e o resultado deve aparecer na coluna 10. Quando não houver data, a célula do resultado deve permanecer vazia. O valor não pode ficar negativo e a atualização precisa funcionar em todas as páginas.

O modelo continua podendo errar, mas agora possui contexto suficiente para gerar uma solução mais próxima do processo real.

Depois disso, ainda preciso testar:

- uma data futura;
- uma data já vencida;
- uma célula vazia;
- o resultado igual a zero;
- diferentes páginas da planilha;
- alteração de uma data existente;
- inclusão de uma nova linha.

A IA acelera a criação do código. Ela não substitui o conhecimento do processo nem a validação.

## Janela de contexto

A **janela de contexto** representa a quantidade de informação que o modelo consegue considerar durante uma interação.

Ela pode incluir:

- instruções do sistema;
- mensagens anteriores;
- arquivos enviados;
- resultados de buscas;
- respostas de ferramentas;
- código do projeto;
- resposta que está sendo gerada.

A janela de contexto funciona como um espaço de trabalho temporário.

Em uma conversa curta, o modelo pode acompanhar facilmente as decisões anteriores. Em um projeto muito longo, informações antigas podem ser resumidas ou deixar de estar disponíveis.

Isso explica por que projetos extensos precisam de documentação.

Em vez de depender apenas da conversa, posso manter arquivos com:

- objetivo do projeto;
- arquitetura;
- regras de negócio;
- decisões aprovadas;
- estrutura de pastas;
- testes;
- limitações;
- próximos passos.

Quando necessário, esses arquivos são fornecidos novamente ao modelo.

## Aprendizado em contexto

Um LLM consegue adaptar sua resposta aos exemplos e às regras presentes na conversa sem precisar ser treinado novamente.

Se eu fornecer um padrão de documentação, o modelo pode seguir esse formato nas próximas respostas.

Se eu mostrar um código e explicar como os arquivos estão organizados, ele pode continuar trabalhando dentro daquela estrutura.

Esse comportamento é chamado de **aprendizado em contexto**.

| Aprendizado em contexto | Treinamento |
| --- | --- |
| Acontece durante a interação | Acontece durante o desenvolvimento do modelo |
| Usa instruções e exemplos da conversa | Usa grandes conjuntos de dados |
| Não altera permanentemente os parâmetros | Ajusta os parâmetros |
| Geralmente é temporário | Pode alterar o comportamento de forma persistente |
| Pode acontecer em segundos | Exige infraestrutura e processamento |

O modelo não aprende permanentemente tudo o que o usuário escreve. Ele adapta o comportamento enquanto possui acesso ao contexto fornecido.

## Escala e novas capacidades

O desempenho dos modelos tende a melhorar quando existe equilíbrio entre:

- quantidade de dados;
- qualidade dos dados;
- número de parâmetros;
- capacidade computacional;
- tempo de treinamento;
- arquitetura utilizada.

Aumentar apenas um desses elementos não garante um resultado melhor.

Com o crescimento dos modelos, também começaram a aparecer comportamentos que não foram programados como regras individuais.

Entre eles estão:

- adaptação a tarefas novas;
- geração de código;
- tradução;
- uso de exemplos;
- organização de problemas em etapas;
- combinação de conhecimentos de áreas diferentes.

Esses comportamentos são chamados de capacidades emergentes.

Isso não significa que o modelo desenvolveu consciência ou compreensão humana. Significa apenas que determinadas habilidades passaram a ser observadas conforme o sistema ganhou escala e recebeu condições adequadas.

## O que muda na forma de usar IA

Compreender o funcionamento básico da IA generativa muda a maneira de trabalhar com ela.

## O prompt não é apenas uma pergunta

Uma boa instrução pode conter:

- objetivo;
- contexto;
- público;
- regras;
- restrições;
- exemplos;
- formato esperado;
- critérios de sucesso.

Quanto menos contexto eu fornecer, mais decisões o modelo precisará assumir sozinho.

## A resposta é uma proposta

O resultado da IA deve ser tratado como algo a analisar, não como uma decisão automática.

Em um projeto, preciso perguntar:

- A solução resolve o problema original?
- O código pode ser explicado?
- Os casos de erro foram considerados?
- Existe uma opção mais simples?
- As informações estão corretas?
- Quais limitações ainda existem?

## Ferramentas aumentam capacidade e risco

Um modelo que apenas responde textos possui um alcance limitado.

Quando recebe acesso a arquivos, navegador, terminal ou banco de dados, ele consegue realizar tarefas mais complexas. Ao mesmo tempo, aumenta o impacto de um erro.

Por isso, as permissões devem ser proporcionais à tarefa.

Uma IA que precisa apenas analisar um arquivo não precisa receber autorização para excluir pastas. Um agente que deve revisar um código não precisa publicar automaticamente em produção.

## Documentação preserva o contexto

Em projetos longos, a documentação funciona como uma memória externa.

Ela evita que regras importantes dependam apenas do histórico da conversa e permite que diferentes pessoas ou sistemas entendam o trabalho.

## Verificação continua sendo necessária

A IA pode acelerar pesquisa, escrita, programação e análise. Porém, o resultado precisa ser verificado de acordo com o risco.

Um texto para estudo exige revisão de conceitos. Um código exige testes. Uma orientação médica, jurídica ou financeira exige fontes confiáveis e avaliação profissional.

Quanto maior o impacto do erro, maior deve ser o nível de validação.

## Modelo mental

Uma forma simples de entender todo o processo é:

```text
Dados + arquitetura + computação
              ↓
        Pré-treinamento
              ↓
      Modelo de linguagem
              ↓
        Pós-treinamento
              ↓
   Instrução + contexto + ferramentas
              ↓
       Geração da resposta
              ↓
      Teste e validação humana
```

