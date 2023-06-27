<template>
  <div class="home">
    <p>my name is {{ name }} and my age is{{ age }} </p>
    <button @click="handleClick">click me</button>
  </div>
</template>

<script>

export default {
  name: 'Home',
  // mounted(){
  //   console.log('mounted')},
  // created(){
  //   console.log('created')},
  setup(){                  //setup runs before anything else!
    console.log('setup')
    let name = 'samara'
    let age = 23

    const handleClick = () => {
      console.log('you clicked')
    }

    return{name: name , age:age, handleClick}
  }
}
</script>
