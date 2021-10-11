<template>
  <div>
    <aside class="d-flex flex-column barra-lateral">
      <SideBar :option="3"/>
    </aside>
  </div>
</template>
<script>
import SideBar from "../components/SideBar.vue"

export default {
  components: {
    SideBar
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
