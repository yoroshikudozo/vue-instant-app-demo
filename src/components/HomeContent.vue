<template>
  <div class="home">
    <div class="title">
      <h1>ホーム</h1>
    </div>
    <ul>
      <li class="banner">
        <a href="#"><div class="dummy-banner">banner 1</div></a>
      </li>
      <li class="banner">
        <a href="#"><div class="dummy-banner">banner 2</div></a>
      </li>
      <li class="banner">
        <a href="#"><div class="dummy-banner">banner 3</div></a>
      </li>
      <li class="banner">
        <a href="#"><div class="dummy-banner">banner 4</div></a>
      </li>
      <li class="banner">
        <a href="#"><div class="dummy-banner">banner 5</div></a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "HomeContent"
};
</script>

<style scoped lang="scss">
.home {
  margin: 16px 16px 0;
  padding-bottom: 80px;
}
.dummy-banner {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 25vh;
  margin-bottom: 16px;
  background: #fafafa;
  border-radius: 8px;
  border: 1px solid #ddd;
  box-shadow: 0 0 3px rgba(0, 0, 0, 0.15);
}
</style>
