<template>
    <div class="card">
        <DataTable :value="products" removableSort tableStyle="min-width: 50rem">
            <Column field="code" header="Code" sortable style="width: 14%"></Column>
            <Column field="name" header="Name" sortable style="width: 16%"></Column>
            <Column field="PL" header="P/L" sortable style="width: 14%"></Column>
            <Column field="PVP" header="P/PV" sortable style="width: 14%"></Column>
            <Column field="cagr_lucros_5_anos" header="CAGR LUCROS 5 ANOS" sortable style="width: 14%"></Column>
            <Column field="margem_liquida" header="MARGEM LÍQUIDA" sortable style="width: 14%"></Column>
            <Column field="divida_liquida_ebit" header="DÍVIDA LÍQUIDA / EBIT" sortable style="width: 14%"></Column>
        </DataTable>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
const products = ref();

const ProductService = () => {
    const getProductsMini = () => {
        const response = [
            { 
                code: 'MGLU3',
                name: 'Magazine Luiza',
                PL: -31.78,
                PVP: 1.33,
                cagr_lucros_5_anos: '13.08%',
                margem_liquida: '4.5%',
                divida_liquida_ebit: 4.5
            },
            {
                code: 'ABEV3',
                name: 'Ambev',
                PL: 12.79,
                PVP: 2.14,
                cagr_lucros_5_anos: '15.72%',
                margem_liquida: '18.29%',
                divida_liquida_ebit: -0.75
            },
            {
                code: 'PETR4',
                name: 'Petrobas',
                PL: 3.65,
                PVP: 1.29,
                cagr_lucros_5_anos: '25,03%',
                margem_liquida: '25.53%',
                divida_liquida_ebit: 1.2
            },
            {
                code: 'HAPV3',
                name: 'Hapvida',
                PL: -29.15,
                PVP: 0.61,
                cagr_lucros_5_anos: '37.19%',
                margem_liquida: '-2.7%',
                divida_liquida_ebit: 6.64
            },
            {
                code: 'B3SA3',
                name: 'B3',
                PL: 16.4,
                PVP: 3.34,
                cagr_lucros_5_anos: '8.78%',
                margem_liquida: '41.65%',
                divida_liquida_ebit: -0.38
            },
            {
                code: 'ITUB4',
                name: 'Itaú Unibanco',
                PL: 9.69,
                PVP: 1.69,
                cagr_lucros_5_anos: '4.02%',
                margem_liquida: '10.57%',
                divida_liquida_ebit: ''
            },
            {
                code: 'COGN3',
                name: 'Cogna',
                PL: -8.53,
                PVP: 0.35,
                cagr_lucros_5_anos: '',
                margem_liquida: '-8,48%',
                divida_liquida_ebit: 8.17
            },
            {
                code: 'BBDC4',
                name: 'Banco Bradesco',
                PL: 10.80,
                PVP: 0.93,
                cagr_lucros_5_anos: '-8,48%',
                margem_liquida: '6,37%',
                divida_liquida_ebit: ''
            },
            {
                code: 'ITSA4',
                name: 'Itaúsa',
                PL: 7.66,
                PVP: 1.24,
                cagr_lucros_5_anos: '5,75%',
                margem_liquida: '182,39%',
                divida_liquida_ebit: 0.19
            },
            {
                code: 'EQTL3',
                name: 'Equatorial Energia',
                PL: 17.60,
                PVP: 1.73,
                cagr_lucros_5_anos: '1,16%',
                margem_liquida: '5,06%',
                divida_liquida_ebit: 4.47
            },
        ];
        return response;
    };

    return { getProductsMini };
};

onMounted(() => {
    products.value = ProductService().getProductsMini();
});



</script>