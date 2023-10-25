<script>
export default {
  data(){
    return{
      parentLangs : 'Web',
      items:[
        {id:1, title:'HTML', desc:'HTML ...'},
        {id:2, title:'CSS', desc:'CSS ...'},
        {id:3, title:'Javascript', desc:'Javascript ...'},
      ]
    }
  }
}

</script>

<template>
  <div class="layout">
    <h1>This is List Rendering page</h1>

    <ul>
      <li v-for="(item, index) in items" :key="item.id">
       {{ parentLangs }}: {{ index }}-{{ item.title }}
      </li>

    </ul>

  </div>
</template>

<style>

</style>