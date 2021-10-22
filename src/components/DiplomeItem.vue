<template class="diplome">
  <div class="diplome_item">
    <p><strong>{{name}}</strong>  {{ecole}} / {{date_debut}} - {{date_fin}}</p>
    <div>{{presentation}}</div>
  </div>
</template>

<script>
export default {
  name: "DiplomeItem",
  props:{
    name:{
      type: String,
      required: true
    },
    ecole:{
      type: String,
      required: true
    },
    site:{
      type: String,
    },
    date_debut:{
      type: Date,
      required: true
    },
    date_fin:{
      type: Date,
      required: true
    },
    presentation:{
      type: String
    }
  }

}
</script>






<style scoped lang="scss">
.diplome{
  grid-area: diplome;
}
.diplome_details{
  list-style: none;
  display: flex;
  flex-direction: column;
}
</style>