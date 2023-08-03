<template>
  <div>
    <div class="top-image">
      <div class="top-description">
        <h1>理念の文章が入ります</h1>
        <p>
          母体が内装解体専門会社であるからこそ、一般的な施工会社 <br />
          よりも解体費用を抑えることができます。つまり、解体費用を <br />
          抑えることで、余力のある資金が生まれ、使い道を広げることが <br />
          できるということです。<br />
          選択のできる予算の使途も合わせてご提案いたします。
        </p>
      </div>
    </div>
    <!-- 事業目的のボタン手前まで書く -->

    <!-- main-title -->
    <div class="main-title">
      <h2>メインタイトルが 入ります</h2>
      <p>
        タイトルが入ります。タイトルが入ります。
        タイトルが入ります。タイトルが入ります。
        タイトルが入ります。タイトルが入 <br />ります。
        タイトルが入ります。タイトルが入ります。
        タイトルが入ります。タイトルが入ります。 タイトルが入ります。タイ<br />タイトルが入りま
        す。タイトルが入ります。タイトルが入りま す。トルが入ります。
      </p>
    </div>

    <!-- philosophy -->
    <div class="philosophy">
      <h2>経営理念 PHILOSOPHY</h2>
    </div>

    <!-- vision -->

    <div class="vision">
      <h2>事業目的　VISION</h2>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
// top0image
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
// main-title
.main-title {
  text-align: center;
  h2 {
    font-family: "DNPShueiShogoMinStd-Hv";
    font-weight: normal;
    font-size: 40px;
    margin: 60px 0 30px;
  }

  p {
    font-family: "KozGoPr6N-Regular";
    margin: 30px 0;
    display: inline-block;
    text-align: left;
    
  }
}

// philosophy
.philosophy {
  text-align: center;
  h2 {
    font-family: "DNPShueiShogoMinStd-Hv";
    font-weight: normal;
    font-size: 40px;
    margin: 60px 0 30px;
  }
}

.vision {
  text-align: center;
  h2 {
    font-family: "DNPShueiShogoMinStd-Hv";
    font-weight: normal;
    font-size: 40px;
    margin: 60px 0 30px;
  }
}
</style>