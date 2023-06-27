<template>
  <div class="home">
    <!-- <p ref="p">my name is {{ name }} and my age is{{ age }} </p>
    <button @click="handleClick">click me</button>
    <button @click="age++">Add 1 to age</button>
    <input type="text" v-model="name"> -->
      <h1>Home</h1>
      <h2>Refs</h2>
    <p>{{ ninjaOne.name }}-{{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">update ninjaOne</button>
    <h2>Reactive</h2>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }} -{{ nameTwo }}</p>
    <button @click="updateNinjaTwo">Update Ninja Two</button>
  </div>
</template>

<script>
import { ref,reactive } from 'vue'

export default {
  name: 'Home',
  // mounted(){
  //   console.log('mounted')},
  // created(){
  //   console.log('created')},
  setup(){                  //setup runs before anything else!
    console.log('setup')

    // const p = ref(null)

    // let name = ref('samara')
    // let age = ref(30)

    // const handleClick = () => {
    //   // console.log('you clicked')
    //   console.log(p, p.value)
    //   // p.value.classList.add('test')
    //   // p.value.textContent = 'hello, ninjaasss'
    //   name.value = 'Sohaima'
    //   name.age = 25
    // }

    // return{name: name , age:age, handleClick, p}

    //----xxxxxxxxx-------------video 74-------------xxxxxxxxxx----------
    const ninjaOne = ref({name:'Mario', age:30})
    const ninjaTwo = reactive({name:'abc', age:35})

    const nameOne = ref('cat')
    const nameTwo = reactive('dog')


    const updateNinjaOne = () => {
        ninjaOne.value.age = 40;
    }

    const updateNinjaTwo = () =>{
      ninjaTwo.age = 45 
      nameTwo = reactive('cat22')
    }

    return{ninjaOne,updateNinjaOne,ninjaTwo,updateNinjaTwo,nameTwo}
  }
}
</script>
