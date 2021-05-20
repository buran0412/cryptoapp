<template>
  <div class="list">
    <div class="list-content">
      <h1>Value,Description</h1>
      <h1 class="list-title">{{ value }}</h1>
      <div class="list-link">
        <a @click="$router.push({ name: 'Detail', params: { value:value } })">詳細</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["value"]
};
</script>

<style>
.list {
  color: black;
  padding: 60px;
}
.list-content {
  color: black;
  padding: 60px;
}
.h1 {
  color: black;
  padding: 60px;
}

.list-title {
  width: 60%;
  color: black;
  padding: 20px;
  white-space: nowrap;
}
.list-link {
  padding: 5px 10px; /* 上下に5px、左右に20px */
  font-size: 10px;
  color: #000;
  text-decoration: none; /* テキストのスタイルを消す */
  border-radius: 3px; /* 要素の角を丸くする */
  transition: 0.4s ease; /* スタイルが変化する時間 */
  background: #85ff83;
}

.link:hover {
  color: #fff;
  background: #85ff83;
}
</style>

