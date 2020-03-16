<template>
  <div>
      <div v-for="counter in 10" :key="counter">
      <h3>Table de {{n}}</h3>
      <table class="table-multiplication">
        <div v-for="counter in 10" :key="counter">
          <tbody>
            <TableRow v-bind:i="n" v-bind:j="counter" />
          </tbody>
        </div>
      </table>
      <br />
    </div>
  </div>
</template>

<script>
import TableRow from "../components/TableRow.vue";

export default {
  name: "Tables",
  components: {
    TableRow
  },
  props: {
    n: Number
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.table-multiplication {
  text-align: center;
  margin-left: auto;
  margin-right: auto;
  background-color: lightblue;

}
.alignement{
    display: inline-block;
}
</style>
