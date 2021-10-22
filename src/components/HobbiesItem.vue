<template>
  <div>
    <ul id="list_hob">
      <li v-for="item in items" :key="item.hobbie">
        {{ item.hobbie }}
      </li>
    </ul>
  </div>

</template>

<script>
export default {
  name: "HobbiesItem",
  data:function (){
    return{
      items:[
        {hobbie:' Bullet Journal'},
        {hobbie:'Calligraphie & Lettering'},
        {hobbie:'Peinture aquarelle'},
        {hobbie:'acrylique'},
        {hobbie:'Linogravure'},
        {hobbie:'Actualités technologiques'}
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.list_hob{
  list-style: none;
  grid-area: hobbies ;
  text-align: left;

}
</style>