<template>
  <div class="competences_item">
    <h5>{{libelle}}</h5>
    <input type="range" min="1" max="100" step="1" value="{{score}}" id="score" name="score">
    <p>{{description}}</p><br>
  </div>

</template>

<script>
export default {
  name: "CompetencesItem",
  props:{
    libelle:{
      type:String,
      required: true
    },
    description:{
      type:String,
      required: true
    },
    score:{
      type:Number,
      required: true,

    }
  },

}
</script>

<style scoped lang="scss">

</style>