<template>
  <q-card>
    <q-card-section class="flex row col-12 justify-around">
      <q-list separator class="col-12">
        <div class="row justify-between text-grey q-mb-sm text-caption">
          <div>{{dailyExpenses.date}}</div>
          <div>{{dailyExpenses.wholeExpenses}}</div>
        </div>
        <q-item v-for="(item, index) in dailyExpenses.expenses" :key="index">
          <q-item-section avatar>
            <q-icon color="white" class="categoryIcon" :class="item.iconColor" :name="item.icon" />
          </q-item-section>
          <q-item-section>
            <div class="itemName">{{item.name}}</div>
          </q-item-section>
          <q-tooltip>{{item.name}}</q-tooltip>
          <q-item-section avatar>{{item.value}}</q-item-section>
        </q-item>
      </q-list>
    </q-card-section>
  </q-card>
</template>

<script>
export default {
  props: {
    dailyExpenses: Object
  },
  data () {
    return {
      red: 'bg-red'
    }
  }
}
</script>

<style>
.itemName {
  white-space: nowrap;
  overflow: hidden;
  width: 100%;
  text-overflow: ellipsis;
}
.categoryIcon {
  border-radius: 50%;
  width: 30px;
  height: 30px;
  padding: 2px;
}
</style>
