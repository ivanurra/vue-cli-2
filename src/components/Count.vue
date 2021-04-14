<template>
    <h3>Count name: {{ count }}</h3>
    <h3>Qty: {{ balance }}</h3>
    <h3>Status: {{ status ? 'Active' : 'Closed'}}</h3>
    <div v-for="(item, index) in services" :key="index">
        {{index + 1}} - {{ item }}
    </div>
    <BalanceAction 
        text="add balance"
        @action="add"
    />
    <BalanceAction
        text="remove balance"
        @action="remove"
        :disable="disable"
    />
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
            disable: false,
        }
    },
    methods: {
        add() {
            this.balance = this.balance + 100
            this.disable = false
        },
        remove() {
            if (this.balance === 0) {
                this.disable = true
                alert('Zero Qt')
            } else {
                this.balance = this.balance - 100
            }
        },
    },
}
</script>
