<template>
  <div>
    <p>UserName :{{initData.userName}}</p>
    <p>Address : {{initData.address}}</p>
    <p>Food: {{initData.food}}</p>
    <p>Checked: {{initData.isChecked}}</p>
  </div>
</template>
<script>
export default {
  props: ["initData"]
};
</script>