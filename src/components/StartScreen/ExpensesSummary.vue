<template>
  <q-card>
    <q-card-section v-if="expensesData.header" class="flex row col-12 justify-around">
  {{expensesData.header}}
    </q-card-section>
    <q-separator v-if="expensesData.header" />
    <q-card-section class="flex row col-12 justify-around">
      <div v-for="(item, index) in expensesData.array" :key="index" class="fex column justify-around">
        <div class="row justify-center q-pb-sm">{{item.key}}</div>
        <div class="row justify-center">{{item.value}}</div>
      </div>
    </q-card-section>
  </q-card>
</template>

<script>
export default {
  props: {
    expensesData: Object
  }
}
</script>

<style scoped>
.v-separator{
  width: 1px;
  background-color: #000;
}
</style>
