<script setup>
import GreatGrandChild from './GreatGrandChild.vue'
import useNumbers from '../composable/useNumbers'


const { numbers } = useNumbers()
</script>
<template>
    <div>
        <h1>GrandChild</h1>
        {{ numbers }}
        <div class="line"></div>
        <GreatGrandChild />
    </div>
</template>