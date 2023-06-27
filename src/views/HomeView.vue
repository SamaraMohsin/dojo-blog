<template>
  <div class="home">
    <p ref="p">my name is {{ name }} and my age is{{ age }} </p>
    <button @click="handleClick">click me</button>
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

    let name = 'samara'
    let age = 23

    const handleClick = () => {
      // console.log('you clicked')
      console.log(p, p.value)
      p.value.classList.add('test')
      p.value.textContent = 'hello, ninjaasss'
    }

    return{name: name , age:age, handleClick, p}
  }
}
</script>
