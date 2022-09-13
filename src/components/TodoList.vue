<template>
    <div class="wrapper">
      <HeaderList/>
      <SearchItems/>
      <TitleList/>
      <ListItem :items="items"/>
    </div>
</template>

<script>
import HeaderList from "@/components/HeaderList";
import SearchItems from "@/components/SearchItems";
import TitleList from "@/components/TitleList";
import ListItem from "@/components/ListItem";
export default {
  name: 'TodoList',
  components: {ListItem, SearchItems, HeaderList, TitleList},
  data(){
    return{
      items:[
        { id: 1, description: 'Покормить кота', status: true, date: '10.09.2022'},
        { id: 2, description: 'Купить хлеба', status: false, date: '11.09.2022'},
        { id: 3, description: 'Помыть посуду', status: true, date: '09.09.2022'},
      ]
    }
  }
}
</script>


<style lang="scss">
.wrapper{
  margin: 100px 150px;

}
</style>
