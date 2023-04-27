<template>
    <div class="result-page">
        <ResultComponent
            v-for="(item, index) in bank"
            :result="item"
            :key="index"
        />
        <div class="result-comment">
            <div class="result-comment__item">{{ title }}</div>
        </div>
        <div class="result-again">
            <button class="result-again__button">
                попробовать снова
            </button>
        </div>
    </div>
</template>

<script>
import ResultComponent from './components/ResultComponent.vue'
export default {
  name: 'ResultPage',
  components: {
    ResultComponent
  },
  computed: {
    title () {
      return 'gdfbnknkbv'
    },
    bank: function () {
      return [{
        img: '/bankIcons/Ivanoff.png',
        beaver: true,
        items: this.items1
      },
      {
        img: '/bankIcons/Vigoda.png',
        beaver: false,
        items: this.items2
      },
      {
        img: '/bankIcons/Sper.png',
        beaver: true,
        items: this.items3
      }
      ]
    },
    items1: function () {
      return [
        {
          title: 'прозрачные условия'
        },
        {
          title: 'входит в АВС'
        },
        {
          title: 'есть лицензия Банка РФ'
        },
        {
          title: 'честный договор'
        }
      ]
    },
    items2: function () {
      return [
        {
          title: 'непрозрачные условия'
        },
        {
          title: 'входит в АВС'
        },
        {
          title: 'есть лицензия Банка РФ'
        },
        {
          title: 'фактический процент меньше'
        }
      ]
    },
    items3: function () {
      return [
        {
          title: 'самые выгодные условия'
        },
        {
          title: 'лицензия отозвана'
        },
        {
          title: 'плохой договоp'
        },
        {
          title: 'реклама на сайте'
        }
      ]
    }
  }
}

</script>

<style lang="less">

.result {

    &-page {
        width: 860px;
        margin: 0 auto;
    }

    &-comment {
        margin-top: 20px;
        height: 158px;
        background: #9aa6e7;
        border-radius: 30px;
        border: 26px solid #9aa6e7;
        box-sizing: border-box;
        margin-bottom: 30px;

        &__item {
            display: flex;
            align-items: center;
            justify-content: center;
            background: #ffffff;
            height: 100%;
            border-radius: 16px;
            font-size: large;
            font-weight: 700;
            text-align: center;
        }
    }

    &-again {
        display: flex;
        align-items: center;
        justify-content: center;

        &__button {
            background: #5C6273;
            color: #ffffff;
            width: 284px;
            height: 54px;
            border-radius: 14px;
            font-size: 26px;
            font-weight: 700;
            cursor: pointer;
        }
    }
}

</style>
