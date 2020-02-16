<template>
  <div class="fp">
    <div class="title">
      <h1>TO可能店舗一覧</h1>
    </div>
    <ul class="shop-list">
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 1</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 2</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 3</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 4</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 5</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 6</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 7</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 8</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 9</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
      <li class="shop-item">
        <a href="#" class="shop-item-link">
          <div class="dummy-image">image 10</div>
          <div class="shop-item-summary">
            <h2>池袋店</h2>
            <p>豊島区北池袋3-2-1 1001</p>
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ToContent"
};
</script>

<style scoped lang="scss">
.fp {
  margin: 16px 16px 0;
  padding-bottom: 80px;
}
.shop-item {
  margin-bottom: 16px;
  font-size: 14px;

  &-link {
    display: flex;
    align-items: center;
  }

  &-summary {
    padding-left: 16px;
  }

  h2 {
    font-size: 16px;
    margin: 0 0 8px;
  }

  p {
    margin: 0;
  }
}
.dummy-image {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 120px;
  height: 120px;
  background: #fafafa;
  border: 1px solid #ddd;
}
</style>
