<template>
  <header>
    <div id="wrapper">
      <div class="header flex">
        <div class="left">
          <p>CryptoApp</p>
        </div>
        <div class="right flex">
          <p @click="$router.push('/signup')">会員登録</p>
          <p @click="$router.push('/login')">ログイン</p>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
.left p {
  margin-left: 40px;
  font-size: 40px;
  cursor: pointer;
  color: black;
}

.right {
  align-items: center;
}
.right p {
  margin-right: 20px;
  cursor: pointer;
  color: black;
}
.wrapper {
  width: 100%;
}
.header {
  background: #85ff83;
}
.logo {
  width: 150px;
  height: 250px;
  cursor: pointer;
}
.flex {
  display: flex;
  justify-content: space-between;
}
</style>