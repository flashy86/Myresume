<template>
  <div>

    <ul id="list_ident">
      <li v-for="item in items" :key="item.identity">
        {{ item.identity }}
      </li>
    </ul>
  </div>

</template>

<script>
export default {
  name: "InfosItem",
  data:function(){
    return{
      items: [
        { identity: '7 rue d\'Ouessant' },
        { identity: '29200' },
        { identity: 'BREST' },
        { identity: 'annec.luc@gmail.com' },
        { identity: '34 ans' },
        { identity: 'Française' },
        { identity: 'Permis B' },
        { identity: '0611671121' },
        { identity: 'Travailleuse handicapée' },
        { identity: 'Célibataire' }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.list_ident{


}
</style>