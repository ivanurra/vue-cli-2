<template>
    <h3>Count name: {{ count }}</h3>
    <h3>Qty: {{ balance }}</h3>
    <h3>Status: {{ status ? 'Active' : 'Closed'}}</h3>
    <div v-for="(item, index) in services" :key="index">
        {{index + 1}} - {{ item }}
    </div>
    <BalanceAction text="add balance"/>
    <BalanceAction text="remove balance"/>
</template>

<script>
import BalanceAction from './BalanceAction.vue'

export default {
    components: { 
      BalanceAction 
    },
    data() {
        return {
            balance: 1000,
            count: 'Master',
            status: false,
            services: ['Transaction', 'Payment', 'Search'],
        }
    },
    methods: {
        add() {
            this.balance = this.balance + 100
        },
        remove() {
            this.balance = this.balance - 100
        },
    },
}
</script>
