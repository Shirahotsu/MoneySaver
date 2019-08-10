<template>
  <q-page padding>
    <ExpensesSummary class="q-my-lg" :expensesData = averageExpenses></ExpensesSummary>
    <ExpensesSummary class="q-my-lg" :expensesData = favoriteExpenses></ExpensesSummary>
  </q-page>
</template>

<style>
</style>

<script>
import ExpensesSummary from '../components/StartScreen/ExpensesSummary'
export default {
  name: 'PageIndex',
  components: {
    ExpensesSummary: ExpensesSummary
  },
  data () {
    return {
      averageExpenses: {
        header: 'Średnie wydatki',
        array: [{ key: 'Dzienne', value: '30' }, { key: 'Tygodniowe', value: '200' }]
      },
      favoriteExpenses: {
        header: null,
        array: [{ key: 'Jedzenie', value: '30' }, { key: 'Alkochol', value: '200' }]
      }
    }
  }
}
</script>
