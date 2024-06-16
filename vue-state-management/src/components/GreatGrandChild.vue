<script setup>
const {numbers} = defineProps(['numbers'])
</script>

<template>
    <div>
        <h1>GreatGrandChild</h1>
        {{ numbers }}
    </div>
</template>