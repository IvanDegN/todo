<template>
  <div class="container">
    <header>To do list</header>
    <button class="plus"></button>
  </div>

</template>

<script>
export default {
  name: "HeaderList"
}
</script>

<style scoped lang="scss">

*{
  padding: 0;
  margin: 0;
}

.container{
  display: flex;
  justify-content: space-between;
  margin-bottom: 30px;
  header{
    font-weight: 700;
    font-size: 24px;
    line-height: 31.68px;
    color:rgba(22, 25, 29, 1);
  }
  .plus{
    border-radius: 50%;
    width: 40px;
    height: 40px;
    cursor: pointer;
    background-color: rgba(214, 219, 235, 1);
    border: none;
    &:before, &:after{
      position: absolute;
      right: 180px;
      top: 110px;
      content: ' ';
      height: 20px;
      width: 2px;
      background-color: #314B99;
    }
    &:before{
      transform: rotate(90deg);
    }
    &:after{
      transform: rotate(180deg);
    }

  }

}


</style>