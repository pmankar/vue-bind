<template>
    <div class="mb-3">
        <div class="border border-light rounded shadow p-2">
            <label class="col-sm-4 col-form-label "><i class="fa-solid fa-stairs text-info-emphasis"></i> {{ message }} </label>
            <label class="col-sm-4 col-form-label"><i class="fa-solid fa-seedling text-success"></i> {{ entry }} </label>
            <label class="col-sm-4 col-form-label">{{ sl }} <i class="fa-solid fa-person-walking-arrow-right text-danger"></i></label>
        </div>
    </div>
</template>

<script>
export default {
  name: 'PyramidRow',
  props: {
    message: String,
    entry: Number,
    sl: Number
  }
}
</script>