# Cicatrizes e Testes do Projeto

## 1. Fontes Insuficientes

Na primeira criação do glossário, o NotebookLM indicou cobertura insuficiente para conceitos como requisito, rastreabilidade, regra de negócio, webhook e human-in-the-loop.

### Ação
Foram adicionadas fontes mais específicas: CPRE Glossary, AI4RE, IBM Business Rules e documentação do n8n.

### Aprendizado
> Melhorar apenas o prompt não resolve uma base documental incompleta.

## 2. Prompt Genérico

```text
Crie requisitos para um sistema de agendamento.
```

### Problema
O prompt permitia suposições sobre regras, permissões, pagamentos, notificações e exceções.

### Refinamento
Passou a exigir identificação de lacunas, separação entre fatos e suposições e uso de `Necessita validação`.

## 3. Cadeias de Suposições

Entrada:

```text
Quero que o aplicativo permita cancelar qualquer agendamento facilmente.
Acho que seria bom cobrar uma taxa quando a pessoa cancelar muito perto do horário.
```

### Falha
A IA começou a perguntar valor, percentual e forma de cobrança antes de confirmar se a taxa realmente existiria.

### Refinamento
Foi introduzida a regra de perguntas em camadas.

Primeiro:

```text
A cobrança de taxa será realmente adotada como regra de negócio?
```

## 4. Exceções Inventadas

A IA sugeriu falha de internet, indisponibilidade e meio de pagamento inválido sem evidência na entrada.

### Refinamento

```text
Preencha cenarios_excecao somente quando houver evidência direta.
Caso contrário, retorne [].
```

## 5. Teste Final

```json
{
  "necessidade": "Permitir o cancelamento de agendamentos pelo aplicativo",
  "persona": "Usuário do aplicativo",
  "objetivo": "Permitir o cancelamento de agendamentos pelo aplicativo",
  "beneficio_esperado": "Necessita validação",
  "regras_negocio": [],
  "ambiguidades": [
    "facilmente",
    "muito perto do horário",
    "qualquer agendamento"
  ],
  "informacoes_ausentes": [
    "Confirmação se a cobrança de taxa será adotada como regra de negócio",
    "Definição das condições de antecedência para cancelamento"
  ],
  "perguntas_stakeholders": [
    "A cobrança de taxa será realmente adotada como regra de negócio?",
    "Quais tipos de agendamento poderão ser cancelados pelo aplicativo?"
  ],
  "cenarios_excecao": [],
  "status": "NECESSITA_REVISAO_HUMANA"
}
```

## 6. Linha do Tempo

```text
Fontes insuficientes
→ Melhoria da curadoria
→ Prompt genérico
→ Prompt estruturado
→ System Prompt
→ Teste normal
→ Teste adversarial
→ Falhas identificadas
→ Refinamento
→ Teste final validado
```
