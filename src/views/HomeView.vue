<template>
  <div class="home">
    <p ref="p">my name is {{ name }} and my age is{{ age }} </p>
    <button @click="handleClick">click me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name">
  </div>
</template>

<script>
import { ref } from 'vue'

export default {
  name: 'Home',
  // mounted(){
  //   console.log('mounted')},
  // created(){
  //   console.log('created')},
  setup(){                  //setup runs before anything else!
    console.log('setup')

    const p = ref(null)

    let name = ref('samara')
    let age = ref(30)

    const handleClick = () => {
      // console.log('you clicked')
      console.log(p, p.value)
      // p.value.classList.add('test')
      // p.value.textContent = 'hello, ninjaasss'
      name.value = 'Sohaima'
      name.age = 25
    }

    return{name: name , age:age, handleClick, p}
  }
}
</script>
