<template>
  <div>
    <HeaderAuth />
    <div class="card">
      <div class="form">
        <input placeholder="メールアドレス" type="email" />
        <input placeholder="パスワード" type="password" />
        <button>ログイン</button>
      </div>
    </div>
  </div>
</template>

<script>
import HeaderAuth from "../components/HeaderAuth";
export default {
  components: {
    HeaderAuth
  }
};
</script>


<style scoped>
button {
  width: 100px;
  text-align: center;
  padding: 8px 0 10pxpx;
  color: black;
  background-color: #ffffff;
  border-radius: 5px;
  cursor: pointer;
}
.card {
  margin: 100px auto;
  width: 350px;
  background: rgb(226, 226, 226);
  border-radius: 5px;
  padding: 20px;
}
.card p {
  color: black;
  font-weight: bold;
  text-align: center;
}
input {
  margin-top: 15px;
  width: 80%;
  border-radius: 10px;
  padding: 10px;
  border: 1px solid black;
  color: black;
}
.form {
  text-align: center;
}
.form button {
  margin-top: 15px;
}
</style>