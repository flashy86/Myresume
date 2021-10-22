<template class="experiences">
  <div class="experiences_item">
   <p><strong>{{poste}}</strong> {{entreprise}} {{localisation}} / {{datedeb}} - {{datefin}}</p>
   <p>{{description}}</p>
  </div>
</template>

<script>
export default {
  name: "ExperiencesProItem",
    props:{
      poste:{
          type: String,
          required:true
      },
        entreprise:{
            type: String,
            required:true
        },
        localisation:{
            type: String,
            required:true
        },
        datedeb:{
            type: Date,
            required:true
        },
        datefin:{
            type: Date,
            required:true
        },
        description:{
            type: String,
            required:true
        }
    }
}
</script>

<style scoped lang="scss">
.experiences{
  display: flex;

}
.li{
  flex-direction: row;
}

</style>