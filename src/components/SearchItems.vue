<template>
  <div class="search">
    <div>
      <img src="../assets/01.svg" alt="search">
      <input type="text" placeholder="Поиск Имени, статуса или даты">
    </div>
    <div class="search-by">Сортировать по: дата</div>

  </div>
</template>

<script>
export default {
  name: "SearchItems"
}
</script>

<style scoped lang="scss">
  .search{
    display: flex;
    justify-content: space-between;


    input{
      border: none;
      width: 210px;
      font-weight: 400;
      font-size: 14px;
      line-height: 18.48px;
      margin-left: 16px;
    }
    .search-by{
      font-weight: 400;
      font-size: 14px;
      line-height: 18.48px;
      &:after{
        content: url("../assets/02.svg");
        margin-left: 5px;
      }
    }

  }

</style>