<!-- ELUCENIA technical documentation · das28 · pt-BR · no clinical/professional/rights approval -->

# DAS28 (VHS e PCR)

[condições, fontes e permissões](https://elucenia.org/pt-br/ferramentas/das28)

## Como usar

Use a ferramenta no portal ou abra index.html em um servidor HTTP local. Selecione o idioma, preencha os campos e calcule.

## Entradas e unidades

### Articulações dolorosas (de 28)

`tjc`

intervalo: 0–28

### Articulações edemaciadas (de 28)

`sjc`

intervalo: 0–28

### Avaliação global de saúde pelo paciente (escala visual)

`gh`

mm · intervalo: 0–100

### VHS

`vhs`

mm/h · opcional · intervalo: 1–150

### PCR

`pcr`

mg/L · opcional · intervalo: 0–300

## Edição do método

DAS 28 VHS/Prevoo 1995 e DAS 28 PCR/Wells 2009; 28 articulações; PCR comintercepto 0,96

## Fórmula documentada

DAS28-VHS = 0,56 × √(dolorosas) + 0,28 × √(edemaciadas) + 0,70 × ln(VHS) + 0,014 × avaliação global.

DAS28-PCR = 0,56 × √(dolorosas) + 0,28 × √(edemaciadas) + 0,36 × ln(PCR + 1) + 0,014 × avaliação global + 0,96 (PCR em mg/L).

## Limites e população

O DAS28 de 1995 foi desenvolvido para atividade da artrite reumatoide, utilizando contagem de 28 articulações e comparações com avaliação clínica de reumatologistas. A variante por PCR não é automaticamente equivalente à variante por VHS; fórmula, unidades e cortes precisam corresponder à fonte e à edição utilizadas.

## Referências

- [Prevoo MLL et al. Modified disease activity scores that include twenty-eight-joint counts: development and validation in a prospective longitudinal study of patients with rheumatoid arthritis. Arthritis Rheum, 1995.](https://doi.org/10.1002/art.1780380107)

- [Wells G et al. Validation of the 28-joint Disease Activity Score (DAS28) and European League Against Rheumatism response criteria based on C-reactive protein against disease progression in patients with rheumatoid arthritis, and comparison with the DAS28 based on erythrocyte sedimentation rate. Ann Rheum Dis, 2009.](https://doi.org/10.1136/ard.2007.084459)

- [England BR et al. 2019 Update of the American College of Rheumatology Recommended Rheumatoid Arthritis Disease Activity Measures. Arthritis Care Res, 2019.](https://doi.org/10.1002/acr.24042)

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
