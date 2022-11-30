<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h2>{{ text }}</h2>
  </div>
</template>

export default {
  data(){
    return{
      text: "This is an about page"
    }
  }
}