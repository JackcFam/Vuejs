<template>
  <div>
    <h2>Are You a teacher ?</h2>
    <input type="text" v-model="dieuKien" />
    <form>
      <div class="form-check" v-if="dieuKien">
        <label class="form-check-label">
          <input type="checkbox" class="form-check-input" name="" id="" value="checkedValue" :checked='{dieuKien}' />
         Yes, I am
        </label>
      </div>

    <div class="form-check">
      <label class="form-check-label">
        <input type="checkbox" class="form-check-input" name="" id="" value="checkedValue">
        No, I don't
      </label>
    </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "CauDieuKien",
  data() {
    return {
      dieuKien: 'uncheck',
    };
  },
};
</script>
