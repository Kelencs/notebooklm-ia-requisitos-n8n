
# Prompts Reutilizáveis

## 1. História de Usuário + Critérios de Aceite

```text
Atue como Analista de Requisitos.

Extraia a História de Usuário e os Critérios de Aceite claros,
objetivos e verificáveis deste texto.

Não invente persona, benefício ou regra.

Quando faltar informação, escreva:
"Necessita validação".

Entrada:
Atualmente, os clientes precisam ligar para a central para cancelar um agendamento.

Queremos permitir que o cliente faça o cancelamento diretamente pelo aplicativo.

Acho que seria bom cobrar uma taxa quando a pessoa cancelar muito perto do horário.
```

## 2. Identificação de Ambiguidades

```text
Atue como Analista de Requisitos.

Liste exclusivamente os termos subjetivos e ambíguos presentes no requisito.

Não tente interpretá-los.
Não confunda informação ausente com ambiguidade.

Entrada:
O aplicativo deve permitir que qualquer cliente cancele facilmente qualquer agendamento, mesmo quando estiver muito perto do horário marcado.
```

## 3. Perguntas de Elicitação em Camadas

```text
Atue como Analista de Requisitos.

Identifique sugestões e hipóteses presentes na solicitação.

Gere primeiro perguntas de Nível 1 para confirmar se a regra de negócio
realmente deve existir.

Não detalhe valores, percentuais ou implementação antes da confirmação.

Entrada:
Queremos permitir o cancelamento de agendamentos pelo aplicativo.

Acho que seria bom cobrar uma taxa quando o cliente cancelar muito perto do horário.
```

## 4. Fatos x Sugestões x Lacunas

```text
Atue como Analista de Requisitos.

Classifique o texto em:

1. Fatos confirmados
2. Sugestões ou hipóteses
3. Informações ausentes

Para informações ausentes utilize:
"Necessita validação".

Não transforme sugestões em regras.

Entrada:
Atualmente, o cancelamento de agendamentos é realizado pela central de atendimento.

A empresa deseja permitir que o cliente faça o cancelamento pelo aplicativo.

Um stakeholder sugeriu que talvez seja interessante cobrar uma taxa quando o cancelamento acontecer muito perto do horário.

Ainda não foram definidos o prazo limite para cancelamento nem se a cobrança da taxa será realmente adotada.
```

## 5. Clareza e Testabilidade

```text
Atue como Analista de Requisitos.

Revise o requisito para torná-lo claro, objetivo e testável.

Preserve o significado original.
Não invente regras ou detalhes técnicos.

Quando faltar informação, marque:
"Necessita validação".

Indique que o resultado necessita revisão humana.

Entrada:
O sistema deve permitir que o cliente cancele qualquer agendamento facilmente pelo aplicativo e talvez cobrar uma taxa caso o cancelamento seja realizado muito perto do horário.
```
