
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
[COLE A SOLICITAÇÃO]
```

## 2. Identificação de Ambiguidades

```text
Atue como Analista de Requisitos.

Liste exclusivamente os termos subjetivos e ambíguos presentes no requisito.

Não tente interpretá-los.
Não confunda informação ausente com ambiguidade.

Entrada:
[COLE O REQUISITO]
```

## 3. Perguntas de Elicitação em Camadas

```text
Atue como Analista de Requisitos.

Identifique sugestões e hipóteses presentes na solicitação.

Gere primeiro perguntas de Nível 1 para confirmar se a regra de negócio
realmente deve existir.

Não detalhe valores, percentuais ou implementação antes da confirmação.

Entrada:
[COLE A SOLICITAÇÃO]
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
[COLE O TEXTO]
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
[COLE O REQUISITO]
```
