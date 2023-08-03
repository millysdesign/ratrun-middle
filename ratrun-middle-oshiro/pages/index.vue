<template>
  <div>
    <div class="top-image">
      <div class="top-description">
        <h1>理念の文章が入ります</h1>
        <p>母体が内装解体専門会社であるからこそ、一般的な施工会社 <br>
          よりも解体費用を抑えることができます。つまり、解体費用を  <br>
          抑えることで、余力のある資金が生まれ、使い道を広げることが <br>
          できるということです。<br>
          選択のできる予算の使途も合わせてご提案いたします。
        </p>
      </div>
    </div>
    <!-- 事業目的のボタン手前まで書く -->
    <!-- main-title -->
    <div></div>
    <!-- philosophy -->
    <div></div>
    <!-- vision -->
    <div></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.top-image {
  width: 100%;
  height: 800px;
  background-image: url("@/assets/img/top.png");
  // coverが画面いっぱいになるように表示する
  background-size: cover;
  // relativeはこの後画像の上に文字を書くため
  position: relative;
  @include mobile {
    background-position: center bottom;
  }
}

.top-description {
  position: absolute;
  right: 0;
  top: 30%;
  margin-right: 100px;
  color: #fff;
}
</style>