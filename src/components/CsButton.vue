<template>
  <div>
    <button v-on:click="upFunction" class="btn btn-#42b983"> <img src="../assets/like.gif" width="100" height="100" > {{lable}}</button>
    <button v-on:click="downFunction" class="btn btn-#42b983 ml-3"><img src="../assets/dd.gif" width="70" height="70" > {{lable}}</button>
    <button v-on:click="LoveFunction" class="btn btn-#42b983 ml-3"><img src="../assets/loev.gif" width="100" height="100" > {{lable}}</button>
    <button v-on:click="ResetFunction" class="btn btn-#42b983 ml-3"><img src="../assets/f.png" width="100" height="100" > {{lable}}</button>
  </div>
</template>
<script>
export default {
  data: function () {
    return {
      counter: 0,
    };
  },
  props: {
    lable: String,
  },
  methods: {
    upFunction: function () {
      this.counter += 1;
      this.$emit("cc", this.counter);
    },

    downFunction: function () {
      this.counter += -5;
      this.$emit("cc", this.counter);
    },

    LoveFunction: function () {
      this.counter += 10;
      this.$emit("cc", this.counter);
    },

    ResetFunction: function () {
      this.counter = 0;
      this.$emit("cc", this.counter);
    },
  },
};
</script>
<style>
</style>