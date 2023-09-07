<template>
  <div>
    <div class="input-value-group lead">
      <div class="row g-3 mb-3">
        <div class="col-4 form-inline">
          <input v-model="price" type="number" id="inp_int_1" class="form-control" min="25" max="110" required>
        </div>
        <div class="col">
          <p>{{ price - 24 }} <i class="fa-solid fa-person-walking-arrow-right text-danger"></i></p>
        </div>
      </div>
      <div v-for="py in pyentries" :key="py.id">
        <PyramidRow :message=py.id :entry=+(price+py.entry) :sl=+(price+py.sl)></PyramidRow>
      </div>
    </div>
  </div>
</template>

<script setup>
import PyramidRow from './AppComp1.vue'
import { ref } from 'vue'
import { onMounted } from 'vue'
import $ from 'jquery'

const price = ref('')

onMounted(() => {
  $("#inp_int_1").val(25);
  $('#inp_int_1')[0].dispatchEvent(new CustomEvent('input'));
})
</script>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      pyentries: [
        { id: "1", entry: 10, sl: -17 },
        { id: "2", entry: 22, sl: -7 },
        { id: "3", entry: 29, sl: 2 },
        { id: "4", entry: 40, sl: 12 },
        { id: "5", entry: 47, sl: 16 },
        { id: "6", entry: 54, sl: 22 },
        { id: "7", entry: 60, sl: 28 }
      ]

    }
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
