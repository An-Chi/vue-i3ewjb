<template>
  密碼: <input v-bind:type="currentType" />
  <!-- 密碼: <input :type="currentType" /> -->
  <!-- v-bind: 可以省略 v-bind -->
  <button>眼睛</button>
</template>

<script>
  import { ref } from "vue";

  export default {
    setup() {
      // const inputType = ["password", "text"];
      const currentType = ref("password");
      const changeType = () =>{
        currentType.value = currentType.value === "password" ? "text" : "password";
      }
      return {
        currentType
      }
    },
  };
</script>

<style lang="scss" scoped>
  label {
    display: block;
  }

  .fa-eye {
    margin-right: 1rem;
  }
</style>
