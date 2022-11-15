<template>
  <div>
    <AppLayout></AppLayout>
  </div>
</template>


<script>
import AppLayout from './AppLayout.vue';
export default {
    components: {
        AppLayout
    },
  data() {
    return {};
  },
};

</script>


<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,400;0,600;0,700;1,400&display=swap');
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;

  font-size: 10px;
  font-family: 'Poppins', sans-serif;

}
</style>
