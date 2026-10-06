<!-- ELUCENIA technical documentation · escore-mess · pt-BR · no clinical/professional/rights approval -->

# MESS (Mangled Extremity Severity Score)

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/escore-mess)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Lesão esquelética e de partes moles

`energia`

- `1` — Baixa energia (facada, fratura simples, projétil de arma curta)
- `2` — Média energia (fratura exposta ou múltipla, luxação)
- `3` — Alta energia (acidente em alta velocidade, projétil de fuzil)
- `4` — Muito alta energia (o anterior + contaminação grosseira)

### Isquemia do membro

`isquemia`

- `0` — Sem isquemia
- `1` — Pulso reduzido ou ausente, perfusão normal
- `2` — Sem pulso, parestesias, enchimento capilar lento
- `3` — Membro frio, paralisado, insensível

### Isquemia há mais de 6 horas?

`tempo`

- `0` — Não
- `1` — Sim

### Choque

`choque`

- `0` — PAS sempre \> 90 mmHg
- `1` — Hipotensão transitória
- `2` — Hipotensão persistente

### Idade

`idade`

- `0` — \< 30 anos
- `1` — 30 a 50 anos
- `2` — \> 50 anos

## Edição do método

MESS/Johansen 1990:4 domínios, isquemia dobrada\>6 h; sem ordem automática amputação

## Fórmula documentada

MESS = lesão esquelética/partes moles (1 a 4) + isquemia (0 a 3, dobrada se durar mais de 6 h) + choque (0 a 2) + idade (0 a 2).

## Limites e população

O MESS original foi derivado em pequenos grupos de trauma grave de membro inferior. A associação do corte ≥7 com amputação nesses grupos não estabelece uma regra universal nem uma indicação automática. Salvamento do membro depende de avaliação multidisciplinar e condições clínicas não resumidas no escore.

## Referências

- [Johansen K et al. Objective criteria accurately predict amputation following lower extremity trauma. J Trauma, 1990.](https://doi.org/10.1097/00005373-199005000-00007)

## Reproduzir os testes técnicos

Execute node test.cjs na pasta raiz deste repositório para repetir os casos sintéticos registrados. As entradas, expectativas e tolerâncias originais são preservadas. Testes técnicos não constituem validação clínica.

```sh
node test.cjs
```

tool.json contém fontes, edição e escopo de revisão. examples.json conserva as entradas e expectativas sintéticas; results.json registra os resultados obtidos.

[Ficha e referências](../tool.json) · [Código JavaScript](../calculator.js) · [Casos de referência](../examples.json) · [results.json](../results.json)

## Revisão e condições de uso

Revisão clínica independente não realizada.

Esta interface é uma tradução autoral, não uma edição oficial ou certificada. Revisão clínica independente, revisão linguística profissional e autorização de direitos de instrumentos não foram realizadas.

Resultado da fórmula ou classificação. Interpretação, conduta e aplicabilidade dependem da avaliação profissional e da fonte selecionada.

## Licença e atribuição

Apache-2.0 aplica-se somente ao código da ELUCENIA. Os instrumentos, publicações, traduções e dados mantêm os direitos dos respectivos titulares. Preserve LICENSE e NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Resultados documentados

As informações abaixo preservam as saídas do método para exemplos sintéticos. Não constituem validação clínica independente.

### 1

MESS < 7: faixa dos membros salvos na série original

| Detalhes do resultado | |
| --- | --- |
| Pontos de isquemia | 1 |

O MESS não decide sozinho: a indicação de amputação primária é da equipe (ortopedia, vascular e plástica), com o paciente estabilizado.


### 2

MESS ≥ 7: na série original, todos os membros com esse escore foram amputados

| Detalhes do resultado | |
| --- | --- |
| Pontos de isquemia | 4 (dobrados: isquemia > 6 h) |

O MESS não decide sozinho: a indicação de amputação primária é da equipe (ortopedia, vascular e plástica), com o paciente estabilizado.


### 3

MESS ≥ 7: na série original, todos os membros com esse escore foram amputados

| Detalhes do resultado | |
| --- | --- |
| Pontos de isquemia | 2 |

O MESS não decide sozinho: a indicação de amputação primária é da equipe (ortopedia, vascular e plástica), com o paciente estabilizado.

