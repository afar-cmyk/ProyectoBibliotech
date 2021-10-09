<template>
  <div>
    <div class="title-format">
      <h3>Categoría: Ilustración</h3><!--Esta categoría se pinta con la lista y cambiar el nombre de categoría en la que se está-->
    </div> 
    <b-row class="row-books">
      <b-col cols="12" md="6" lg="4">
        <!--Libro 1-->
        <CardBook1 />
      </b-col>
      <b-col cols="12" md="6" lg="4">
        <!--Libro 2-->
        <CardBook2 />
      </b-col>
      <b-col cols="12" md="6" lg="4">
        <!--Libro 3-->
        <CardBook3 />
      </b-col>
      <b-col cols="12" md="6" lg="4">
        <!--Libro 4-->
        <CardBook4 />
      </b-col>
      <b-col cols="12" md="6" lg="4">
        <!--Libro 5-->
        <CardBook5 />
      </b-col>
      <b-col cols="12" md="6" lg="4">
        <!--Libro 6-->
        <CardBook6 />
      </b-col>
    </b-row>
  </div>
</template>
<script>
    import CardBook1 from "./cardBook1.vue";
    import CardBook2 from "./cardBook2.vue";
    import CardBook3 from "./cardBook3.vue";
    import CardBook4 from "./cardBook4.vue";
    import CardBook5 from "./cardBook5.vue";
    import CardBook6 from "./cardBook6.vue";
export default {
  components: {
    CardBook1,
    CardBook2,
    CardBook3,
    CardBook4,
    CardBook5,
    CardBook6,
  },
};
</script>
