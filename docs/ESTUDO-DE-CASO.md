# Estudo de Caso — Cancelamento de Agendamentos

## 1. Solicitação

```text
Quero que o aplicativo permita cancelar qualquer agendamento facilmente.
Acho que seria bom cobrar uma taxa quando a pessoa cancelar muito perto do horário.
```

## 2. Ambiguidades

- `facilmente`
- `muito perto do horário`
- `qualquer agendamento`

## 3. Sugestão não confirmada

```text
Acho que seria bom cobrar uma taxa...
```

Isso não representa uma regra de negócio confirmada.

## 4. Resultado Estruturado

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

## 5. Perguntas em Camadas

### Nível 1
```text
A cobrança de taxa será realmente adotada como regra de negócio?
```

### Nível 2
Somente se a resposta for positiva:

```text
Em quais situações a taxa será aplicada?
```

### Nível 3
Somente depois:

```text
Qual valor ou fórmula será utilizada?
```

## 6. O que a IA não deve fazer

- inventar valor;
- inventar percentual;
- inventar meio de pagamento;
- inventar integrações;
- assumir que a taxa existirá;
- criar cenários de exceção sem evidência.

## 7. Conclusão

> Hipótese não é regra. Sugestão não é requisito aprovado.

