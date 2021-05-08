<template>
  <main>
    <div class="album">
      <div>
        <Copertine />
      </div>
    </div>
  </main>
</template>

<script>
import axios from "axios";
import Copertine from "@/components/Copertine.vue";
export default {
  name: "Main",
  components: {
    Copertine,
  },

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
      axios
        .get(this.apiURL)
        .then((res) => {
          console.log(res.data);
          this.discoList = res.data;
          this.loading = false;
        })
        .catch((err) => {
          console.log("Error", err);
        });
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
.album {
  display: flex;
}
</style>