function calcularEconomiaParaMeta(meta, taxaDeRetorno, prazoEmAnos) {
    // Converter a taxa de retorno para decimal
    taxaDeRetornoDecimal = taxaDeRetorno / 100;

    // Calcular o valor futuro da meta
    const valorFuturo = meta * Math.pow((1 + taxaDeRetornoDecimal), prazoEmAnos);

    // Calcular a economia necessária periodicamente
    const economiaPeriodica = (valorFuturo / (prazoEmAnos * 12)).toFixed(2);

    return economiaPeriodica;
}

// Exemplo de uso:
const metaFinanceira = 100000; // Meta financeira desejada
const taxaDeRetornoAnual = 8; // Taxa de retorno anual esperada (em porcentagem)
const prazoDeAnos = 10; // Prazo em anos

const economiaMensalNecessaria = calcularEconomiaParaMeta(metaFinanceira, taxaDeRetornoAnual, prazoDeAnos);
console.log(`Para alcançar uma meta de $${metaFinanceira} em ${prazoDeAnos} anos, você precisa economizar aproximadamente $${economiaMensalNecessaria} por mês.`);
