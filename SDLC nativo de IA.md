# Código rápido não significa projeto pronto

A inteligência artificial reduziu muito o tempo necessário para escrever código. Hoje, uma função que levaria horas para ser criada pode surgir em poucos minutos.

Isso parece resolver a parte mais difícil do desenvolvimento, mas apenas desloca o problema.

Quando escrever código fica mais rápido, o trabalho passa a se concentrar em outras perguntas:

- O problema foi entendido corretamente?
- A regra criada representa o processo real?
- O código pode alterar algo que não deveria?
- Quais situações podem causar erro?
- Como verificar se o resultado está correto?
- É possível desfazer a alteração?
- Quem assume a responsabilidade pela decisão?

O código pode ficar pronto em minutos. A confiança de que ele pode ser usado exige muito mais trabalho.

## A IA acelera a execução, não a compreensão

Uma IA consegue gerar funções, interfaces, fórmulas e testes. Porém, ela não conhece automaticamente a rotina em que a solução será utilizada.

Considere uma instrução simples:

```text
Crie uma automação para controlar medicamentos próximos do vencimento.
```

A IA consegue produzir algum código. No entanto, ainda faltam informações importantes:

- Onde está a data de validade?
- Existem várias abas?
- O que acontece quando a célula está vazia?
- O sistema pode exibir dias negativos?
- Como o saldo interfere no status?
- Quando uma perda é considerada evitada?
- Quem pode alterar os dados?
- Como recuperar a planilha se algo der errado?

Sem essas respostas, a IA precisa preencher as lacunas com suposições.

O código pode funcionar tecnicamente e ainda resolver o problema errado.

## O desenvolvimento começa antes do código

Antes de pedir uma implementação, é necessário transformar a necessidade em regras claras.

Esse trabalho pode ser dividido em cinco partes:

### 1. Problema

Descrever o que acontece atualmente e por que precisa mudar.

### 2. Resultado esperado

Definir o que a solução deve entregar quando estiver funcionando.

### 3. Regras

Explicar como cada situação precisa ser tratada.

### 4. Limites

Registrar o que o sistema pode e não pode alterar.

### 5. Validação

Determinar como o resultado será conferido.

Uma descrição útil não precisa ser um documento enorme. Ela precisa impedir interpretações diferentes.

```markdown
## Problema

O cálculo dos dias restantes depende de fórmulas manuais e pode apresentar resultados incorretos.

## Resultado esperado

A planilha deve calcular os dias automaticamente, tratar células vazias e atualizar os status relacionados.

## Limites

A automação não pode alterar colunas fora do escopo nem processar abas sem a estrutura esperada.

## Validação

O resultado automático será comparado com cálculos manuais em diferentes situações.
```

Com esse contexto, a IA deixa de adivinhar o processo e passa a trabalhar dentro de critérios definidos.

## Exemplo aplicado: Controle de Validade da Farmácia

O Controle de Validade começou com um problema real da rotina da farmácia.

A planilha usava fórmulas que precisavam ser arrastadas. Quando uma data estava ausente ou já havia passado, o resultado podia ficar incorreto. Além disso, acompanhar saldos, status e possíveis perdas exigia trabalho manual.

Uma função isolada poderia calcular a diferença entre duas datas:

```javascript
const dias = dataValidade - dataAtual;
```

Mas essa operação não representava a solução completa.

O projeto precisava entender diferentes estados:

```text
Sem data
→ não calcular

Data futura
→ mostrar os dias restantes

Data atual
→ mostrar zero

Data vencida
→ impedir contagem negativa

Saldo alterado
→ recalcular informações relacionadas

Falha durante a execução
→ preservar os dados existentes
```

O desafio principal não era subtrair datas. Era transformar a rotina da farmácia em regras que o sistema pudesse executar com segurança.

## A diferença entre uma função e uma solução

Uma função resolve uma operação específica.

Uma solução precisa considerar o processo inteiro.

| Função isolada | Solução aplicada |
| --- | --- |
| Calcula dias | Interpreta diferentes estados |
| Atualiza uma célula | Protege colunas fora do escopo |
| Funciona em um exemplo | Trata várias abas e linhas |
| Mostra um resultado | Verifica se o resultado faz sentido |
| Executa quando chamada | Define quando deve ser executada |
| Supõe dados corretos | Trata dados vazios ou inválidos |
| Altera a planilha | Cria meios de recuperação |

Essa diferença explica por que um código aparentemente simples pode exigir tantas decisões.

## O novo gargalo é a validação

Quando a IA produz código rapidamente, a quantidade de alterações aumenta.

Se cada nova versão precisar ser conferida manualmente sem nenhum método, o tempo economizado na escrita será gasto na revisão. Se a revisão for ignorada, os erros chegarão ao uso real.

O desenvolvimento precisa criar verificações junto com o código.

No Controle de Validade, alguns cenários essenciais são:

| Situação testada | Comportamento esperado |
| --- | --- |
| Data futura | Calcular os dias restantes |
| Data igual ao dia atual | Registrar zero |
| Data vencida | Não continuar abaixo de zero |
| Célula vazia | Manter o campo de resultado vazio |
| Data inválida | Não produzir cálculo incorreto |
| Nova linha | Aplicar as mesmas regras |
| Mudança de saldo | Atualizar os campos dependentes |
| Execução repetida | Não duplicar notificações |
| Aba incompatível | Não alterar sua estrutura |
| Erro durante o processo | Manter uma forma de recuperação |

A IA pode sugerir esses testes. Quem conhece a operação precisa confirmar se eles representam a realidade.

## Segurança precisa nascer com a automação

Adicionar segurança somente depois que o sistema está pronto cria retrabalho.

No projeto, algumas decisões de segurança fazem parte da própria solução:

- criar cópias de segurança;
- limitar as colunas alteradas;
- impedir valores inválidos;
- evitar notificações repetidas;
- registrar falhas;
- validar a estrutura antes de processar uma aba;
- permitir conferência humana;
- testar antes de aplicar mudanças amplas.

Quanto maior o impacto de um erro, menor deve ser a liberdade da automação para agir sem verificação.

## Nem toda mudança exige o mesmo cuidado

O nível de controle deve acompanhar o risco.

| Alteração | Risco | Cuidado necessário |
| --- | --- | --- |
| Corrigir um texto da interface | Baixo | Revisão visual |
| Alterar uma cor de status | Baixo | Conferir legibilidade |
| Modificar o cálculo dos dias | Médio | Testar várias datas |
| Mudar a regra de saldo | Alto | Comparar com casos reais |
| Calcular perda financeira | Alto | Revisão dos valores e das condições |
| Apagar registros | Crítico | Bloqueio, backup e autorização |

Essa classificação ajuda a decidir quando a IA pode avançar e quando precisa parar para receber aprovação.

## Documentação como memória do projeto

Durante o desenvolvimento, várias decisões são tomadas:

- uma regra é acrescentada;
- outra é descartada;
- um erro revela um caso que não havia sido previsto;
- um usuário pede uma mudança;
- um teste mostra que a primeira solução não serve.

Se essas decisões permanecem apenas na conversa com a IA, parte do contexto pode se perder.

A documentação funciona como memória externa.

Uma estrutura simples pode conter:

```text
controle-validade/
├── README.md
├── docs/
│   ├── problema.md
│   ├── regras.md
│   ├── decisoes.md
│   ├── testes.md
│   └── erros-encontrados.md
└── codigo/
    └── apps-script.gs
```

### `problema.md`

Explica por que o projeto existe.

### `regras.md`

Registra como cada situação deve ser tratada.

### `decisoes.md`

Guarda escolhas importantes e seus motivos.

### `testes.md`

Lista cenários, resultados esperados e resultados encontrados.

### `erros-encontrados.md`

Documenta falhas e como elas foram corrigidas.

Quando a IA recebe esses arquivos, ela trabalha com o estado real do projeto em vez de depender apenas do histórico da conversa.

## O projeto não termina quando funciona uma vez

Uma automação pode funcionar durante o teste e falhar depois.

Isso pode acontecer porque:

- surgiu uma nova aba;
- alguém mudou o nome de uma coluna;
- uma célula recebeu um formato inesperado;
- o gatilho executou duas vezes;
- uma regra da operação mudou;
- uma nova necessidade apareceu.

Por isso, manutenção não significa apenas corrigir erros. Significa acompanhar se a solução continua adequada ao processo.

No Controle de Validade, novas necessidades ampliaram o projeto:

- acompanhamento do saldo atual;
- atualização automática de status;
- registro de valores financeiros;
- controle de perdas;
- data de zeragem;
- histórico do saldo no vencimento;
- notificações;
- base de medicamentos.

Cada mudança precisa voltar às perguntas iniciais:

```text
O que mudou?
      ↓
Qual regra nova surgiu?
      ↓
Quais partes serão afetadas?
      ↓
Como testar?
      ↓
Qual é o risco?
      ↓
Como desfazer se falhar?
```

O desenvolvimento passa a ser um ciclo de melhoria, não uma entrega única.

## Como trabalhar com IA sem perder o controle

Um fluxo prático pode seguir esta ordem:

### Entender

Descrever o problema com base na rotina real.

### Modelar

Transformar o processo em dados, estados e regras.

### Limitar

Definir o que a automação pode acessar e alterar.

### Construir

Usar a IA para acelerar código, documentação e casos de teste.

### Verificar

Executar cenários normais, extremos e inválidos.

### Aplicar

Liberar a solução gradualmente e manter uma forma de reversão.

### Aprender

Registrar erros, pedidos e mudanças para orientar a próxima versão.

```text
Rotina real
    ↓
Problema entendido
    ↓
Regras documentadas
    ↓
Implementação com IA
    ↓
Testes e proteção
    ↓
Uso controlado
    ↓
Aprendizado registrado
    ↓
Próxima versão
```

## O que deve ser medido

Contar linhas de código não mostra se a solução ficou melhor.

Indicadores mais úteis seriam:

- tarefas manuais removidas;
- erros encontrados antes do uso;
- falhas depois da liberação;
- tempo necessário para conferir resultados;
- quantidade de retrabalho;
- segurança para recuperar os dados;
- clareza das regras;
- facilidade de manutenção;
- confiança dos usuários;
- tempo entre a identificação do problema e a solução validada.

A IA pode aumentar a produção de código sem melhorar nenhum desses resultados.

Produtividade real significa entregar uma solução correta, compreensível e segura em menos tempo.

## Conclusão

A principal mudança trazida pela IA não é apenas escrever código mais rápido. É obrigar o desenvolvimento a valorizar mais tudo o que existe ao redor dele.

No Controle de Validade, calcular dias foi a parte simples. O trabalho real apareceu ao entender a rotina, transformar situações em regras, tratar dados incompletos, proteger a planilha, testar resultados e acompanhar novas necessidades.

A IA acelerou a construção. O conhecimento da operação definiu o que precisava ser construído.

Quando o código fica barato e rápido, entendimento, validação e responsabilidade passam a ter ainda mais valor.
