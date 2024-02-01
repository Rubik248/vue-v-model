<template>
    <input 
        type="text"
        :placeholder='placeholder'
        :value="modelValue"
        @input="$emit('update:modelValue', $event.target.value)"
    >
</template>


<script>
export default {
    props: {
        modelValue: {
            type: String
        },
        placeholder: 'placeholder'
    }
}
</script>



<style scoped>
    input {
        font-family: DM Sans, sans-serif;
        font-size: 18px;
        font-weight: 400;
        text-align: left;
        color: rgba(111, 108, 144, 1);
        border: none;
        padding: 16px 18px;
        border-radius: 20px;
    }
</style>