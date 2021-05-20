<template>
  <div>
    <HeaderAuth />
    <ul>
      <li>取引価格:{{price}}</li>
      <li>最終取引時間:{{time}}</li>
    </ul>
  </div>
</template>

<script>
import HeaderAuth from "../components/HeaderAuth";
import axios from "axios";
export default {
  props: ["value"],
  data() {
    return {
      price: "",
      time: ""
    };
  },
  async created() {
    const item = await axios.get(
      "https://api.coin.z.com/ws/public=${this.value}i3g2pGbTjj0E1OBqqUorHJCu+Bmzw3OP"
    );
    const coindata = item.data;
    this.price = coindata.price;
    this.time = coindata.time;
  },
  components: {
    HeaderAuth
  }
};
</script>

<style>
ul,
ol {
  padding: 0;
  position: relative;
}

ul li,
ol li {
  color: black;
  border-left: solid 10px #85ff83; /*左側の線*/
  background: #0000; /*背景色*/
  margin-bottom: 20px; /*下のバーとの余白*/
  line-height: 3;
  padding: 0.5em;
  list-style-type: none !important; /*ポチ消す*/
}
</style>
