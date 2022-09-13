<template>
  <div class="list">
    <div class="list__description">Описание</div>
    <div class="list__inline">
      <div class="list__status">Статус</div>
      <div class="list__date">Дата</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TitleList"
}
</script>

<style scoped lang="scss">



.list__description, .list__status, .list__date{
  font-weight: 400;
  font-size: 14px;
  line-height: 18.48px;
}

.list{
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 20px 80px;

  .list__description{
    &:before{
      content: url("../assets/03.svg");
      margin-right: 20px;
      display: inline-block;
    }

  }

  .list__inline{
    display: inline-flex;

    .list__status{
      &:before{
        content: url("../assets/03.svg");
        margin-right: 20px;
        display: inline-block;

      }

    }

    .list__date{
      &:before{
        content: url("../assets/03.svg");
        margin-right: 20px;
        margin-left: 80px;
        display: inline-block;
      }

    }
  }


}

</style>