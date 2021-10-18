<template>
  <div id="container" v-on:mousemove="tinhToaDo">
    <h2>{{ content }}</h2>
    <h2 v-once style="color: red">{{ contents }} - {{ changeContent() }}</h2>
    <a id="nhat" type="text" v-bind:href="link">My Google</a>
    <h1 style="color: green" v-once>{{ sayHello() }}</h1>
    <p v-html="testHTML" v-bind:href="link">{{ testHTML }}</p>
    <p>{{ dem > 0 ? dem : "biến đếm không được nhỏ hơn 0" }}</p>
    <button v-on:click="thayDoiGT">Tăng</button>
    <button v-on:click="dem--">Trừ</button>
    <p>{{ x }} / {{ y }}</p>
    <p v-on:mousemove.stop>Stop</p>
    <input type="text" @keyup.enter.space="Keyup" />
    <button v-on:click="a++">Tăng A</button>
    <button v-on:click="b--">Trừ B</button>
    <p>Gía trị A: {{ tangA }}</p>
    <p>Gía trị B: {{ tangB }}</p>
  </div>
</template>
<script>
export default {
  name: "DemoVue",
  props: {
    content: String,
  },
  data() {
    return {
      link: "https://www.google.com/",
      contents: "Nội dung ban đầu",
      testHTML: '<a href="http://www.google.com">Test HTML</a>',
      dem: 0,
      x: 0,
      y: 0,
      dem2: 0,
      a: 0,
      b: 0,
    };
  },
  //computed thực hiện như 1 function nhưng nó chỉ như một properties
  computed: {
    tangB: function () {
      console.log("trừ b");
      return this.b;
    },
    tangA: function () {
      console.log("cong a");
      return this.a;
    },
  },
  watch: {
      a: function () {
          console.log('biến a đã được thay đổi');
      }
  },
  methods: {
    changeContent: function () {
      this.contents = "Nội dung đã được cập nhật";
      return this.contents;
    },
    sayHello: function () {
      document.write("Tôi đang bắt đầu học Vuejs");
    },
    thayDoiGT: function () {
      return this.dem++;
    },
    tinhToaDo: function (event) {
      (this.x = event.clientX), (this.y = event.clientY);
    },
    Keyup: function (event) {
      alert(event.target.value);
    },
  },
};

</script>
