<template>
    <button @click="action" :disable="disable">{{ text }}</button>
</template>

<script>
export default {
    props: {
        text: String,
        disable: {
            type: Boolean,
            default: false
        }
    },
    methods: {
        action(){
            // @action in BalanceAction
            this.$emit('action');
        },
    }
}
</script>
