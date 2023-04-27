<template>
  <div class="home">
    <p><router-link :to="{ name: 'btn' }">
        Btn
      </router-link></p>
    <p><router-link :to="{ name: 'banks' }">
        banks page
      </router-link></p>
    <p><router-link :to="{ name: 'search' }">
        Search page
      </router-link></p>
    <p><button @click="() => openExampleModal()">Открыть модалку</button></p>
    <p><router-link :to="{ name: 'sper-page' }">
        Sper Page
      </router-link></p>
    <p><router-link :to="{ name: 'result' }">
        Result Page
      </router-link></p>
    <ImportantComponent :comment="comment"></ImportantComponent>
  </div>
</template>

<script>
import ImportantComponent from './../components/Important/ImportantComponent.vue'
export default {
  name: 'HomeView',
  components: {
    ImportantComponent
  },
  computed: {
    comment () {
      return 'Прежде чем подписать договор, его надо внимательно прочитать. Чтобы понять содержание договора требуется время. Один неучтенный маленький пункт договора, набранный мелким шрифтом, может разрушить ваши мечты и планы по накоплению. Чтобы выбрать для себя наиболее подходящий вариант депозита, надо хорошо понимать, какие условия есть у этого финансового инструмента. Если что-то в договоре вы не поняли, возьмите паузу, чтобы разобраться.'
    }
  },
  methods: {
    openExampleModal () {
      this.$openExampleModal({ param2: '2' })
    }
  }
}
</script>
