<template>
  <div>{{ answer }}</div>
</template>

<script>
import axios from "axios";
export default {
  name: "ConnectAPI",
  data() {
    return {
      data:{},
    };
  },
  mounted(){
    this.connectCheck();
  },
  methods: {
    async connectCheck() {
      const { data } = await axios.get("http://127.0.0.1:8000/ConnectCheck");
      this.answer = data;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
