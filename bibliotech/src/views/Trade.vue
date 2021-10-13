<template>
  <div>
    <NavBar />
    <ListBooks />
    <Footer />
  </div>
</template>
<script>
import NavBar from "../components/navbar.vue";
import Footer from "../components/footer.vue";
import ListBooks from "../components/listBooks.vue";
export default {
  components: {
    NavBar,
    Footer,
    ListBooks,
  },
};
</script>
<style scoped>
.btn-secondary{
    background-color: #485eb2 !important;
    border: 1px solid #485eb2 !important;
}
</style>
