<template>
  <div style="display: flex; width: 100%; justify-content: space-between">
    <div
      class="vuong"
      @click="quanlydo = !quanlydo"
      :class="{ do: quanlydo }"
    ></div>
    <div class="vuong" @click="quanlydo = !quanlydo" :class="{ do: quanlydo }"></div>
    <div class="vuong" @click="quanlyxanh = !quanlyxanh" :class="{ do: quanlydo }"></div>
    <div
      class="vuong"
      @click="quanlydo = !quanlydo"
      :class="{ do: quanlydo }"
    ></div>
  </div>
</template>

<script>
export default {
  name: "Demo",
  data() {
    return {
      quanlydo: false,
      quanlyxanh: false,
    };
  },
  computed: {
    changColor: function () {
      return this.quanlydo ? true : false;
    },
  },
  methods: {},
};
</script>
<style>
.vuong {
  background-color: gray;
  width: 300px;
  height: 300px;
  border: 1px solid yellowgreen;
  box-shadow: 1px 1px 1px 3px gray;
  cursor: pointer;
}
.do {
  background-color: red;
}
.xanh {
  background-color: green;
}
</style>
