<template>
  <div class="list" v-for="item in items" :key="item.id"  >
    <div class="list__item">
      <button v-if="item.status === true" v-on:click="item.status = !item.status"></button>
      <button class="btn" v-else v-on:click="item.status = !item.status"></button>
      <div class="list__item__title">{{item.description}}</div>
    </div>
    <div class="list__inline">
      <div class="list__status true" v-if="item.status === true" :class="{true: item.status}">Выполнено</div>
      <div class="list__status false" v-else :class="{false: item.status}">В работе</div>
      <div class="list__date">{{item.date}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ListItem",
  props: ['items']
}
</script>

<style scoped lang="scss">

.true{
  color: rgba(19, 78, 193, 1);
}

.false{
  color: rgba(248, 155, 17, 1);
}

.list__item__title, .list__status, .list__date{
  padding-bottom: 20px;
  padding-top: 20px;
  font-weight: 400;
  font-size: 14px;
  line-height: 18.48px;
}

.btn{
  content: '';
  background: #FFFFFF;
  border: 1px solid #134EC1;
  box-shadow: 0px 4px 4px rgba(19, 78, 193, 0.15);
  border-radius: 50%;
  display: inline-flex;
  width: 20px;
  height: 20px;
  margin-left: 40px;
  cursor: pointer;
}

button{
  content: url("../assets/04.svg");
  background: #FFFFFF;
  border: 1px solid #134EC1;
  box-shadow: 0px 4px 4px rgba(19, 78, 193, 0.15);
  border-radius: 50%;
  display: inline-flex;
  width: 20px;
  height: 20px;
  margin-left: 40px;
  cursor: pointer;
  //&:hover{
  //  content: '';
  //  border: 1px solid rgba(22, 25, 29, 1);
  //  border-radius: 50%;
  //}
}

.list{
  display: flex;
  justify-content: space-between;
  background-color: rgba(246, 249, 255, 1);
  border-bottom: solid #EEEBE9 1px;
  border-top: solid #EEEBE9 1px;

  .list__item{

    &:before{

    }
  }
  .list__inline{
    display: inline-flex;
  }

  .list__date{
    margin-left: 76px;
    padding-right: 32px;
  }

  .list__item__title{
    display: inline-flex;
    margin-left: 41px;
  }

}

</style>