<template>
    <div class="card">
        <Fieldset legend="P/L" :toggleable="true">
            <p class="m-0">
                Benjamin Graham - O P/L máximo que paga em uma empresa é de 15. Superior a 15 quer fizer que a empresa está cara.
            </p>
        </Fieldset>
        <Fieldset legend="P/PV" :toggleable="true">
            <p class="m-0">
                Se estiver 1 quer dizer a empresa está sendo negociada no valor justo. Acima de 1 quer dizer que a empresa está cara. Menor que 1 quer dizer que a empresa está barata.
                Benjamin Graham - Compra a empresa até 1.5. Fórmula: P/L * P/V <= 22.5
            </p>
        </Fieldset>
        <Fieldset legend="CAGR LUCROS 5 ANOS" :toggleable="true">
            <p class="m-0">
                Média de crescimento anual dos lucros da empresa nos últimos 5 anos.
            </p>
        </Fieldset>
        <Fieldset legend="MARGEM LÍQUIDA" :toggleable="true">
            <p class="m-0">
                Margem líquida é o lucro líquido dividido pela receita líquida. É a porcentagem de lucro que a empresa obteve em relação ao seu faturamento.
                Não é indicado investir em empresas com margem líquida negativa ou muito baixa (1, 2, 3%).
            </p>
        </Fieldset>
        <Fieldset legend="DÍVIDA LÍQUIDA / EBIT" :toggleable="true">
            <p class="m-0">
                Dívida líquida é a diferença entre o total de dívidas e o total de caixa e equivalentes de caixa. O EBIT é o lucro antes dos juros, impostos, depreciação e amortização.
                Quanto menor o índice, melhor. Empresas com índice negativo são as melhores.
                Até 4 é considerado bom. Acima de 4 é considerado ruim.
            </p>
        </Fieldset>
    </div>
</template>

<script setup lang="ts">

</script>