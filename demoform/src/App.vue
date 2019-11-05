<template>
  <div id="app">
    <b-container>
      <form-input @onSubmit="onSubmit"></form-input>
      <data-submit :initData="initData"></data-submit>
    </b-container>
    <!-- <router-view/> -->
  </div>
</template>

<script>
import formInput from "./views/Form1.vue";
import DataSubmit from "./views/DataSubmit.vue";
export default {
  components: {
    formInput,
    DataSubmit
  },
  data() {
    return {
      initData: {}
    };
  },
  methods: {
    onSubmit(data) {
      this.initData = {...data}
    }
  }
};
</script>

<style>
</style>
