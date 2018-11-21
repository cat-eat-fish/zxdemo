<template>
  <div class="hello">
    
  </div>
</template>

<script>
export default {
  name: 'ceshi',
  data () {
    return {
     
    }
  },
  created(){
        fetch("/api/",{}).then(res=>{
            return res.json()
        }).then(data=>{
            console.log(data)
        })

      this.$axios.get('/cityapi/region/init').then(function (response) {
            console.log(response.data);
        }).catch(function (error) {
            console.log(error);
        });
  },
  computed:{

  },
}
</script>

<style scoped>

</style>
