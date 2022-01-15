<template>
  <div class="hello">
    <p>{{tittle}}</p>
    <h5>{{greet('Morning')}}</h5>
  </div>
</template>

<script>
export default {
  data(){
    return {
      tittle:"Helloe Brian"
    }
  },
  methods:{
    greet(time){
      return "Good "+ "" + time;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
