<template>
    <h3>Count name: {{ count }}</h3>
    <h3>Qty: {{ balance }}</h3>
    <h3>Status: {{ status ? 'Active' : 'Closed'}}</h3>
    <div v-for="(item, index) in services" :key="index">
        {{index + 1}} - {{ item }}
    </div>
</template>

<script>
export default {
    data() {
        return {
            balance: 1000,
            count: 'Master',
            status: false,
            services: ['Transaction', 'Payment', 'Search'],
        }
    },
}
</script>
