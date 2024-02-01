<template lang="">
    <input @click="getData" type="submit" placeholder="Submit">
</template>


<script>
export default {
    methods: {
        getData() {
            this.$emit('getData')
        }
    }
}
</script>



<style scoped>
    input {
        background: linear-gradient(rgba(158, 150, 242, 1), rgba(236, 49, 240, 1));
        border: none;
        padding: 20px 24px;
        border-radius: 26px;
        font-family: "Poppins" ,sans-serif;
        font-size: 24px;
        font-weight: 700;
        text-align: center;
        color: white;
    }
    input:hover {
        background: linear-gradient(rgb(108, 104, 161), rgb(149, 32, 151));
    }
</style>