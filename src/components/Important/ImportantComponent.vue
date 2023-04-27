<template>
<div class="window">
  <h2 class="window-important">Важно!</h2>
    <div class="window-beaver">
      <img class="window-beaver__img" src="/img/money-beaver.png">
    </div>
  <div class="window-information">
      {{ comment }}
  </div>
  <button class="window-further">Далее</button>
</div>
</template>

<script>
export default {
  name: 'ImportantComponent',
  props: {
    comment: Text
  }
}
</script>

<style lang="less">

.window {
  width: 610px;
  padding-bottom: 12px;
  background: #5C6273;
  color: #ffffff;
  border-radius: 30px;

  &-important {
    padding: 14px 0 0 20px;
    font-weight: 700;
    color: #F2F2F2;
  }

  &-information {
    margin: -10px 20px 10px;
    background: #D9D9D9;
    color: #212940;
    border-radius: 20px;
    padding: 10px 10px 10px 142px;
    text-align: center;
  }

  &-further {
    display: flex;
    justify-content: center;
    width: 76px;
    margin: 0 auto;
    padding: 4px;
    cursor: pointer;
    background: #F2F2F2;
    border-radius: 8px;
    border-color: #F2F2F2;
    border: 0px;
    font-weight: 600;
  }

  &-beaver {
    position: absolute;
    width: 218px;
    height: 150px;

    &__img {
      width: 100%;
      height: 100%;
    }
  }
}

</style>
