<template>
  <q-page padding>
    <ExpensesSummary class="q-my-lg" :expensesData="averageExpenses"></ExpensesSummary>
    <ExpensesSummary class="q-my-lg" :expensesData="favoriteExpenses"></ExpensesSummary>
    <DailyExpenses class="q-my-lg" v-for="(item, index) in dailyExpenses" :key="index" :dailyExpenses = item></DailyExpenses>
  </q-page>
</template>

<style>
</style>

<script>
import ExpensesSummary from '../components/StartScreen/ExpensesSummary'
import DailyExpenses from '../components/StartScreen/DailyExpenses'
export default {
  name: 'PageIndex',
  components: {
    ExpensesSummary: ExpensesSummary,
    DailyExpenses: DailyExpenses
  },
  data () {
    return {
      averageExpenses: {
        header: 'Średnie wydatki',
        array: [
          { key: 'Dzienne', value: '30' },
          { key: 'Tygodniowe', value: '200' }
        ]
      },
      favoriteExpenses: {
        header: null,
        array: [
          { key: 'Jedzenie', value: '30' },
          { key: 'Alkochol', value: '200' }
        ]
      },
      dailyExpenses: [
        {
          date: '12.06.19',
          wholeExpenses: '40',
          expenses: [
            {
              name: 'Pizza',
              icon: 'bluetooth',
              iconColor: 'bg-red',
              value: '20',
              uuId: '1e42bbcd-6ec2-4cbf-943e-cdf5a71aa239'
            },
            {
              name: 'Kaaapustaaa',
              icon: 'book',
              iconColor: 'bg-green',
              value: '20',
              uuId: 'cb537fa0-1a85-4625-b0cf-dcc7e42b4eca'
            },
            {
              name: 'Kino',
              icon: 'phone',
              iconColor: 'bg-yellow',
              value: '20',
              uuId: 'ea1cdfa6-c129-416b-bf3d-eab1576e82be'
            }
          ]
        },
        {
          date: '11.06.19',
          wholeExpenses: '40',
          expenses: [
            {
              name: 'Spagetti',
              icon: 'bluetooth',
              iconColor: 'bg-red',
              value: '20',
              uuId: '3f274adc-bb7b-11e9-bf00-2a2ae2dbcce4'
            },
            {
              name: 'Ogóreczki',
              icon: 'book',
              iconColor: 'bg-green',
              value: '20',
              uuId: '3f274e1a-bb7b-11e9-bf00-2a2ae2dbcce4'
            }
          ]
        }
      ]
    }
  }
}
</script>
