<template>
  <div>
    <aside class="d-flex flex-column barra-lateral">
      <barraNav />
    </aside>
  </div>
</template>
<script>
import barraNav from "../components/barraNav.vue";

export default {
  components: {
    barraNav,
  },
};
</script>
<style scoped>
.barra-lateral {
  background-color: white;
  width: 16vw;
  height: 100vh;
  border-right: 1px solid #0000001f;
  box-shadow: 0 1px 3px rgba(0, 0, 0, 0.082), 0 1px 2px rgba(0, 0, 0, 0.158);
}
</style>
