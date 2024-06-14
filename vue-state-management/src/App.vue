<script setup>
import { reactive,ref } from 'vue'

// const red = ref(0)
// const green = ref(0)
// const blue = ref(0)

// function generateColor() {
//   red.value = Math.floor(Math.random() * 255)
//   green.value = Math.floor(Math.random() * 255)
//   blue.value = Math.floor(Math.random() * 255)
// }

// const color = ref({
//     red:0,
//     green:0,
//     blue:0,
//   })
  
  // //atau bisa memanfaatkan ini juga jika berupa object datanya
  const color = reactive({
    red:0,
    green:0,
    blue:0,
  })

  function generateColor() {
  color.red = Math.floor(Math.random() * 255)
  color.green = Math.floor(Math.random() * 255)
  color.blue = Math.floor(Math.random() * 255)
}

//perbedaan asign value pada ref dengan reactive
// const refValue = ref('Hello')
// const reactiveValue = reactive({
//   greeting:'world',
// })

//mencoba men asign ulang nilai yg sudah di asign diatas
// refValue.value = true
// reactiveValue=  false;
</script>

<template>
  <main :style="{ backgroundColor: `rgb(${color.red}, ${color.green}, ${color.blue})`}">
    <div>
      <input type="number" placeholder="red" v-model="color.red" id="">
      <input type="number" placeholder="green" v-model="color.green" id="">
      <input type="number" placeholder="blue" v-model="color.blue" id="">
      <button @click="generateColor()">Generate</button>
    </div>
  </main>
</template>

<style scoped>
main {
	background-color: rgb(122, 50, 255);
	height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
}

div {
	display: flex;
	flex-direction: column;
}
</style>
