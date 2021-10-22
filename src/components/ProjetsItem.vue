<template>
  <div class="projets_Item">
      <p>{{name}} {{description}} {{date}}</p>
      <p>{{technologies}}</p>
  </div>
</template>

<script>
export default {
  name: "ProjetsItem",
    props:{
      name:{
          type:String,
          required: true
      },
      date:{
          type:Date,
          required: true
      },
      description:{
          type:String,
          required: true
      },
      technologies:{
          type: String,
          required:true
      }
    }
  }
</script>

<style scoped lang="scss">

</style>