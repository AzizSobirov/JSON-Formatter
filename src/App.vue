<template>
  <form action="" v-on:submit.prevent="loadJson()">
    <div class="content">
      <textarea name="" v-model="input" placeholder="Enter your JSON file."></textarea>
      <textarea name="" v-text="result" placeholder="Your Formated JSON file goes here."></textarea>
    </div>
    <div class="btn">
      <button type="submit" class="as_btn"><a href="#">Format</a></button>
      <button type="reset" class="as_btn"><a href="#">Reset</a></button>
    </div>
  </form>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import './css/style.css'
export default {
  name: 'App',
  data() {
    return{
      input:'',
      result:''
    }
  },
  methods: {
    loadJson(){
      this.result = JSON.stringify(JSON.parse(this.input),null,4)
      return false;
    }
  },
}
</script>
