Saber usar inteligência artificial não é apenas escrever bons prompts. Também é saber o que delegar, como explicar o trabalho, como avaliar o resultado e como usar a tecnologia com responsabilidade.

Essas quatro competências formam a estrutura dos **4Ds**:

1. **Delegação:** decidir o que a IA fará e o que continuará sob responsabilidade humana.
2. **Descrição:** explicar com clareza o problema, o contexto e o resultado esperado.
3. **Discernimento:** analisar criticamente o que a IA produziu.
4. **Diligência:** cuidar dos dados, das permissões e das consequências do uso da IA.

Os quatro pontos precisam funcionar juntos. Não adianta explicar perfeitamente uma tarefa que nunca deveria ter sido delegada. Também não adianta receber uma resposta convincente e colocá-la em uso sem testar.

## Três formas de trabalhar com IA

Antes de começar um projeto, preciso decidir qual será o papel da IA.

### Automação

A IA executa uma tarefa específica a partir das minhas instruções. Posso usá-la, por exemplo, para gerar uma estrutura inicial, revisar um código ou organizar informações.

### Aprimoramento

A IA trabalha comigo. Eu apresento o problema, avalio as opções e tomo as decisões. Ela ajuda a desenvolver ideias e acelerar a execução.

### Agência

A IA recebe um objetivo mais amplo e trabalha com mais independência. Nesse caso, preciso definir com cuidado os limites, as ferramentas permitidas, os critérios de conclusão e quais ações exigem minha aprovação.

Quanto maior a autonomia, maior precisa ser o controle sobre permissões, testes e possíveis impactos.

## Delegação: o que devo fazer e o que posso passar para a IA?

Delegar não significa entregar o projeto inteiro. Significa dividir o trabalho de forma consciente.

As decisões que dependem do contexto real continuam comigo. A IA não acompanha minha rotina, não conhece todos os envolvidos e não sente as consequências de uma decisão errada. Por isso, sou eu quem precisa identificar o problema, definir prioridades e estabelecer as regras.

A IA pode ajudar nas partes repetitivas ou técnicas, como:

- organizar os requisitos;
- sugerir caminhos possíveis;
- criar uma primeira versão do código;
- encontrar falhas na lógica;
- preparar testes e documentação.

## Descrição: a qualidade da resposta começa no contexto

Uma instrução curta pode funcionar para uma tarefa simples. Em um projeto, porém, a IA precisa entender mais do que o pedido final.

Preciso explicar:

- qual problema quero resolver;
- quem utilizará a solução;
- como o processo funciona atualmente;
- quais regras precisam ser respeitadas;
- o que já foi tentado;
- quais erros precisam ser evitados;
- como será possível saber que o projeto está pronto.

Descrever bem não é escrever muito. É fornecer as informações que realmente mudam a solução.

## Discernimento: a resposta parece certa ou está certa?

A IA pode escrever um código organizado e ainda assim interpretar uma regra de forma errada. Por isso, não devo avaliar apenas a aparência da resposta.

Preciso conseguir entender o que foi produzido, comparar com a documentação e testar situações diferentes. Se o resultado falhar, devo descobrir se o problema está na instrução, na lógica proposta ou na implementação.

Também preciso questionar soluções desnecessariamente complicadas. A melhor resposta não é a que utiliza mais recursos, mas a que resolve o problema com segurança e pode ser mantida depois.

## Diligência: a responsabilidade continua sendo humana

Usar IA não transfere a responsabilidade pelo projeto. Se eu decidir utilizar uma resposta, preciso assumir a revisão e as consequências dessa escolha.

Isso inclui:

- não compartilhar dados pessoais, internos ou sigilosos sem autorização;
- trocar informações reais por exemplos fictícios quando possível;
- conceder somente as permissões necessárias;
- testar alterações em uma cópia antes de usar no ambiente original;
- manter backup ou uma forma de desfazer a mudança;
- registrar o que foi alterado;
- reconhecer a participação da IA quando isso for relevante.

## Exemplo real: automação dias a vencer em uma planilha

Um exemplo de aplicação dos 4Ds foi uma automação criada para calcular os dias a vencer em uma planilha.

O problema já existia antes da IA: a fórmula precisava ser arrastada manualmente e apresentava resultados incorretos quando não havia uma data preenchida. Eu conhecia a rotina e sabia como o resultado deveria funcionar.

### Como apliquei a Delegação

Mantive comigo as decisões do processo:

- qual coluna continha a data;
- onde o resultado deveria aparecer;
- quais páginas precisavam ser atualizadas;
- como tratar células vazias;
- o que fazer quando o cálculo chegasse a zero;
- quando a atualização deveria acontecer.

Usei a IA para ajudar a transformar essas regras em Apps Script, revisar a lógica e corrigir os erros encontrados.

### Como apliquei a Descrição

Em vez de pedir apenas um script para calcular datas, expliquei a estrutura da planilha, as colunas envolvidas, o comportamento esperado e as exceções.

Uma descrição adequada seria:

> Preciso de um Apps Script para uma planilha com várias páginas que seguem a mesma estrutura. A data está na coluna 8 e o resultado deve aparecer na coluna 10. Células sem data precisam continuar vazias e o cálculo não pode gerar valores negativos. A atualização deve funcionar em todas as páginas.

### Como apliquei o Discernimento

Não considerei o código pronto apenas porque ele foi executado. Testei situações diferentes:

- célula com uma data válida;
- célula sem data;
- resultado igual a zero;
- data já vencida;
- várias páginas da planilha;
- inclusão e alteração de datas.

Foi durante esse processo que apareceram regras que precisavam ser ajustadas. O teste ajudou a transformar uma resposta inicial em uma solução adequada à rotina real.

### Como apliquei a Diligência

O código foi testado antes de ser aplicado à planilha utilizada no trabalho. Informações reais não precisavam ser enviadas para a IA, pois a estrutura podia ser explicada com exemplos. A decisão de usar o script continuou dependendo de validação humana.

Nesse projeto, a IA não identificou o problema e não definiu as regras. Ela acelerou a transformação de uma necessidade real em uma solução testável.

## Perguntas para aplicar os 4Ds em qualquer projeto

Antes de iniciar um novo projeto com IA, posso usar este checklist.

### Delegação

- [ ] Qual problema estou tentando resolver?
- [ ] A IA realmente é necessária para este trabalho?
- [ ] O que depende do meu conhecimento e precisa continuar comigo?
- [ ] Quais tarefas posso delegar à IA?
- [ ] Quais partes serão construídas em colaboração?
- [ ] Quanto de autonomia a IA precisa receber?
- [ ] Quais ações precisam da minha aprovação antes de continuar?

### Descrição

- [ ] Expliquei o contexto do problema?
- [ ] Informei quem utilizará o resultado?
- [ ] Descrevi o processo atual?
- [ ] Defini o resultado esperado?
- [ ] Listei as regras, limites e exceções?
- [ ] Mostrei o que já foi tentado e quais erros aconteceram?
- [ ] Informei o formato da entrega?
- [ ] Defini como reconhecer que o trabalho está concluído?

### Discernimento

- [ ] Consigo entender e explicar o resultado?
- [ ] Os fatos foram conferidos em fontes confiáveis?
- [ ] O código foi revisado antes de ser executado?
- [ ] Testei situações normais, limites e possíveis erros?
- [ ] A resposta resolve o problema original?
- [ ] Existe uma solução mais simples, segura ou fácil de manter?
- [ ] Registrei as limitações que ainda existem?

### Diligência

- [ ] Tenho autorização para usar os dados e sistemas envolvidos?
- [ ] Removi informações pessoais, sigilosas ou internas?
- [ ] Concedi somente as permissões necessárias?
- [ ] Existe uma cópia de teste, um backup ou uma forma de desfazer a alteração?
- [ ] O resultado será revisado antes de entrar em produção?
- [ ] Está claro quem assume a responsabilidade pela decisão final?
- [ ] Preciso informar que houve participação de IA?

## Modelo rápido para novos projetos

```markdown
# Nome do projeto

## Problema

Qual problema real precisa ser resolvido?

## Resultado esperado

O que precisa existir ou funcionar ao final?

## Delegação

- Responsabilidade humana:
- Responsabilidade da IA:
- Trabalho colaborativo:
- Ações que exigem aprovação:

## Descrição

- Contexto:
- Usuários envolvidos:
- Regras e exceções:
- Restrições:
- Formato da entrega:
- Critérios de conclusão:

## Discernimento

- Testes necessários:
- Fontes para verificação:
- Limitações conhecidas:
- Critérios de aprovação:

## Diligência

- Dados que não podem ser compartilhados:
- Permissões necessárias:
- Estratégia de backup ou reversão:
- Responsável pela validação final:
```
