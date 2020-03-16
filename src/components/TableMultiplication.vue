<template>
  <div>
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
  
</template>

<script>
import TableRow from "./TableRow.vue";

export default {
  name: "TableMultiplication",
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
</style>
