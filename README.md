# MoGym

Aplicativo pessoal para gerenciamento de treinos de musculação e acompanhamento de desempenho ao longo do tempo.

O usuário poderá organizar sua rotina, registrar séries, cargas e repetições e comparar como seu desempenho varia entre sessões e períodos.

## Objetivo

Permitir que o usuário visualize como seu desempenho varia entre treinos, semanas e períodos.

O MoGym apresenta dados e tendências. Uma queda pode acontecer por fatores externos, mudança de rotina ou variação normal do treino. Por isso, o sistema não classifica automaticamente o resultado como evolução ou regressão.

## Fluxo principal

```text
Frequência semanal
        ↓
Divisão de treino
        ↓
Ficha de treino
        ↓
Exercícios
        ↓
Execução do treino
        ↓
Registro
        ↓
Histórico
        ↓
Comparação
        ↓
Relatório de desempenho
```

## Funcionalidades planejadas

- Informar quantos dias por semana pretende treinar.
- Escolher uma divisão de treino já cadastrada.
- Receber, se quiser, uma recomendação de divisão feita por regras do próprio sistema.
- Montar a ficha de treino, usando uma ficha pré-configurada ou uma ficha personalizada.
- Selecionar exercícios a partir do catálogo existente.
- Registrar carga, séries e repetições durante a execução do treino.
- Consultar o histórico de treinos.
- Comparar o desempenho entre sessões, semanas e períodos.
- Visualizar relatórios descritivos de como os indicadores variaram.

### Divisões de treino

O sistema terá divisões cadastradas. Exemplos previstos:

- Full Body
- Upper/Lower
- Push/Pull/Legs
- PPL + Upper/Lower

Outras divisões podem ser adicionadas depois.

A recomendação não usa inteligência artificial. Ela relaciona, por regras do sistema, a frequência semanal a um conjunto de divisões compatíveis. As regras concretas ainda serão definidas. A lógica deve poder mudar no futuro, sem ficar presa a uma estrutura rígida.

## Catálogo de exercícios

Os exercícios usados nos treinos precisam existir previamente no catálogo. O sistema não cria exercícios dinamicamente.

Cada exercício pode ter informações como:

- nome
- grupo muscular
- equipamento
- categoria
- descrição
- status ativo ou inativo

Outros dados podem ser incluídos depois, se fizerem sentido para o domínio. Ao personalizar um treino, o usuário seleciona exercícios desse catálogo.

## Fichas de treino

Depois de escolher a divisão, o usuário pode:

- utilizar uma ficha pré-configurada
- modificar uma ficha
- montar uma ficha personalizada com exercícios do catálogo

Uma ficha pode ter vários dias de treino. Cada dia pode ter vários exercícios, com uma ordem definida.

## Registro dos treinos

Durante a execução, o usuário registra o que foi realizado. As informações principais são:

- exercício
- carga
- número de repetições
- número de séries
- data e sessão

O registro previsto é por série. Exemplo:

**Supino reto**

- Série 1 → 70 kg × 10
- Série 2 → 70 kg × 9
- Série 3 → 70 kg × 8

Esses registros formam um histórico consultável.

## Acompanhamento de desempenho

Desempenho não depende somente do aumento de carga. Fazer mais ou menos repetições com a mesma carga também é uma variação.

Exemplo em que a carga permanece e as repetições mudam:

- Semana 1: 70 kg × 8
- Semana 2: 70 kg × 10

Exemplo em que a carga muda e as repetições também:

- Semana 3: 75 kg × 8
- Semana 4: 75 kg × 7

O sistema mostra a diferença. Ele não precisa classificá-la como regressão.

Indicadores previstos:

- carga utilizada
- repetições
- número de séries
- volume de treino
- frequência
- comparação entre sessões
- comparação entre semanas e períodos

Uma forma de calcular o volume é:

```text
volume = carga × repetições × séries
```

Volume descreve o que ocorreu no treino. Não é sinônimo direto de força ou de evolução.

## Relatórios

Os relatórios usam o histórico e apresentam os indicadores separadamente.

Exemplo:

**Supino reto**

- Semana anterior: 70 kg × 10
- Semana atual: 75 kg × 8
- Carga: +7,1%
- Repetições: −20%
- Volume: variação correspondente

A pergunta principal do relatório é: **como meu desempenho mudou?**

O relatório não resume o período em uma porcentagem única, como "você evoluiu 15%".

## Funcionalidades futuras

O que está nesta seção não faz parte da primeira versão.

No futuro, a sessão poderá receber contexto informado pelo usuário, como:

- horas de sono
- percepção de energia
- cansaço
- observações
- possíveis mudanças na rotina

Esses dados servem apenas como contexto. O sistema pode mostrar que uma sessão teve determinado desempenho e que, no mesmo dia, o usuário informou baixa energia. Ele não deve afirmar que uma coisa causou a outra.

Inteligência artificial não faz parte do núcleo do produto. O aplicativo deve funcionar sem ela. Um uso futuro de IA só será considerado se houver uma função em que ela realmente faça sentido, e essa decisão será avaliada à parte.

## Tecnologias

A stack ainda está em definição.

Ainda não foram escolhidos:

- linguagem
- framework
- banco de dados
- arquitetura
- estrutura definitiva do backend
- estrutura definitiva do frontend

## Status do projeto

Planejamento e desenvolvimento inicial.

Nesta etapa, o repositório descreve o projeto. Modelagem, APIs e implementação ainda serão definidas.

Conforme o projeto avançar, este README pode passar a incluir capturas de tela, instalação, arquitetura, endpoints, decisões técnicas, testes e roadmap.

## Objetivo de aprendizado

O MoGym também é um projeto de portfólio. A prioridade é um escopo menor e bem implementado, para praticar fundamentos de engenharia de software.

Ao longo do desenvolvimento, o código deve demonstrar principalmente:

- backend e APIs
- modelagem de domínio
- banco de dados
- regras de negócio
- autenticação
- histórico de dados
- cálculos
- testes
- organização de código
- Git
- Docker, se fizer sentido para o projeto
