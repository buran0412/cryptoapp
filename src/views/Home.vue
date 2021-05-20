<template>
  <div>
    <HeaderAuth />
    <div class="home flex">
      <List v-for="(data, index) in lists" :key="index" :value="data.value" />
    </div>
  </div>
</template>


<script>
import HeaderAuth from "../components/HeaderAuth";
import List from "../components/List";
export default {
  data() {
    return {
      lists: [
        {
          value: "BTC"
        },
        {
          value: "ETH"
        },
        {
          value: "LTC"
        },
        {
          value: "XRP"
        },
        {
          value: "BTC_JPY"
        },
        {
          value: "ETH_JPY"
        },
        {
          value: "BCH_JPY"
        },
        {
          value: "LTC_JPY"
        },
        {
          value: "XRP_JPY"
        }
      ]
    };
  },
  components: {
    HeaderAuth,
    List
  }
};
</script>

<style scoped>
table {
  margin: 100px;
  width: 80%;
}
table th,
table td {
  width: 60%;
  color: black;
  padding: 20px;
  white-space: nowrap;
}
.link {
  padding: 5px 10px; /* 上下に5px、左右に20px */
  font-size: 10px;
  color: #000;
  text-decoration: none; /* テキストのスタイルを消す */
  border-radius: 3px; /* 要素の角を丸くする */
  transition: 0.4s ease; /* スタイルが変化する時間 */
  white-space: nowrap;
  background: #85ff83;
}

.link:hover {
  color: #fff;
  background: #85ff83;
}
</style>