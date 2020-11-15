<template>
  <div class="home">
    <h2>Home</h2>
    <p>{{data.id}}</p>
    <p>{{data.name}}</p>
    <button @click="transition()">遷移</button>
  </div>
</template>

<script>
export default {
  data(){
    return {
      list: [
        { id: 1, name: "first" },
        { id: 2, name: "second" },
        { id: 3, name: "third" }
      ]
    }
  },
  methods:{
    transition(dataId){
      this.$router.push({name:"Detail",params:{id:dataId}});
    }
  }
};
</script>