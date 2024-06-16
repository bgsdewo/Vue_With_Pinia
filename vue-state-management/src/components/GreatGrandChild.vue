<script setup>
// import { inject } from 'vue'
import { useNumbers } from '../stores/numbers'

const { numbers } = useNumbers()
// const numbers  = inject('numbers')
</script>

<template>
    <div>
        <h1>GreatGrandChild</h1>
        {{ numbers }}
    </div>
</template>