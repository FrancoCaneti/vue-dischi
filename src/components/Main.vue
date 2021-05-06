<template>
  <main>
    <div class="album">
      <h1>ok</h1>
    </div>
  </main>
</template>

<script>
import axios from "axios";
export default {
  name: "Main",
  data() {
    return {
      apiURL: "https://flynn.boolean.careers/exercises/api/array/music",
      discoList: [],
      loading: true,
    };
  },
  created() {
    this.getDisco();
  },
  methods: {
    getDisco() {
      axios;
    },
  },
};
</script>



<style>
main {
  width: 100%;
  height: 651px;
  background-color: #151a28e3;
}
</style>