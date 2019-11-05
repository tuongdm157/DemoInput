<template>
  <div>
    <b-form>
      <b-form-group id="input-group-1" label="User Name:" label-for="input-1">
        <b-form-input id="input-1" v-model="userInfo.userName"></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-2" label="Address:" label-for="input-2">
        <b-form-input id="input-2" v-model="userInfo.address"></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label="Food:" label-for="input-3">
        <b-form-select id="input-3" :options="foods" v-model="userInfo.food"></b-form-select>
      </b-form-group>

      <b-form-group id="input-group-4">
        <b-form-checkbox-group id="checkboxes-4" v-model="userInfo.isChecked">
          <b-form-checkbox value="me">Check me out</b-form-checkbox>
          <b-form-checkbox value="that">Check that out</b-form-checkbox>
        </b-form-checkbox-group>
      </b-form-group>

      <b-button variant="primary" @click="onSubmit">Submit</b-button>
    </b-form>
  </div>
</template>
<script>
export default {
  data() {
    return {
      userInfo: {
        userName: "",
        address: "",
        food: "Carrots",
        isChecked: []
      },

      foods: ["Carrots", "Beans", "Tomatoes", "Corn"]
    };
  },
  methods: {
    onSubmit() {
      this.$emit("onSubmit", this.userInfo);
    }
  }
};
</script>