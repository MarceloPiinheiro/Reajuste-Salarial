# Lógica de Folha

Ferramenta de reajuste salarial em lote criada por Marcelo Pinheiro, a partir da experiência na rotina de Departamento Pessoal.

O projeto permite transformar uma lista de funcionários e salários em uma tabela de reajustes, facilitando a conferência dos valores e do impacto mensal.

## Funcionalidades

- Entrada de funcionários e salários por texto ou colagem de duas colunas do Excel.
- Aplicação de um percentual único ao lote.
- Exibição do salário atual, percentual, diferença e novo salário de cada funcionário.
- Totalização da base salarial e do impacto mensal.
- Identificação opcional da empresa e da vigência.
- Validação das linhas e aviso quando o resultado precisa ser recalculado.
- Cópia da tabela e exportação em CSV.
- Layout adaptável a celular e computador.

## Tecnologias

HTML5, CSS3 e JavaScript, sem frameworks ou dependências externas.

## Como executar

1. Baixe e extraia os arquivos deste projeto.
2. Mantenha `index.html`, `styles.css` e `app.js` na mesma pasta.
3. Abra `index.html` no navegador.
4. Clique em **Usar exemplo fictício** e depois em **Calcular reajuste** para experimentar.

A cópia para a área de transferência depende das permissões e do contexto de segurança do navegador. Se estiver indisponível, utilize o CSV.

## Formato de entrada

Uma pessoa por linha, sem cabeçalho:

```text
Ana Silva; 2.000,00
Bruno Souza; 2.500,00
Carla Santos; 3.000,00
```

Também é possível colar duas colunas separadas por tabulação, copiadas de uma planilha. O percentual aceita vírgula ou ponto decimal, com até duas casas.

## Exemplo de conferência

Com os salários acima e reajuste de 5%:

| Funcionário | Salário atual | Diferença | Novo salário |
| --- | ---: | ---: | ---: |
| Ana Silva | R$ 2.000,00 | R$ 100,00 | R$ 2.100,00 |
| Bruno Souza | R$ 2.500,00 | R$ 125,00 | R$ 2.625,00 |
| Carla Santos | R$ 3.000,00 | R$ 150,00 | R$ 3.150,00 |
| **Total** | **R$ 7.500,00** | **R$ 375,00** | **R$ 7.875,00** |

## Critério do cálculo

A diferença é calculada por funcionário e arredondada para centavos. O novo salário corresponde ao salário atual somado à diferença. Os totais somam os valores individuais arredondados.

O escopo considera somente o reajuste direto. Não inclui encargos, reflexos, retroativos, pisos ou regras de convenção coletiva. A vigência é uma identificação do cálculo e não gera retroativos.

## Dados

O cálculo acontece no navegador. Os nomes e salários não são enviados a um servidor nem persistidos pela aplicação. Recarregar ou fechar a página apaga a lista.

## Autoria

**Marcelo Pinheiro** · [GitHub](https://github.com/MarceloPiinheiro)

Projeto idealizado a partir da experiência em Departamento Pessoal.
