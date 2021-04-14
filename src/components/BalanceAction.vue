<template>
    <button @click="action">{{ text }}</button>
</template>

<script>
export default {
    props: {
        text: String,
    },
    methods: {
        action(){
            // @action in BalanceAction
            this.$emit('action');
        },
    }
}
</script>
