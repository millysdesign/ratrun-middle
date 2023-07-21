<template>
  <footer>
    <div class="footer-inner">
      <div class="footer-content">
        <!-- 左のエリア -->
        <div class="footer-left">
          <div class="footer-logo-top">
            <a href=""><img src="@/assets/svg/logo-2.png" alt="" /></a>
          </div>

          <div class="footer-logo-bottom">
            <p>
              Interior design <br />
              &
              <br />
              Construction
            </p>
          </div>
        </div>

        <!-- 中央左のエリア -->
        <nav class="nav-left">
          <ul class="nav-left-items">
            <!-- v-for=vueの繰り返し文 -->
            <li v-for="(page, key) in pageListleft" :key="key">
              <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
            </li>
          </ul>
        </nav>

        <!-- 中央右のエリア -->
        <nav class="nav-right">
          <ul class="nav-right-items">
            <!-- v-for=vueの繰り返し文 -->
            <li v-for="(page, key) in pageListright" :key="key">
              <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
            </li>
          </ul>
        </nav>

        <!-- 右のエリア -->
        <div class="address">
          <p>
            建築・建築デザイン・原状 回復・内装解体・建物
            解体・アスベスト除去工事はSENT IAにお任せく ださい！
          </p>
          <p>
            株式会社SENTIA <br />
            〒454-0982 <br />
            愛知県名古屋市高見1-20-2 <br />
            TEL : 052-1212-2029
          </p>
        </div>
      </div>

      <!-- SNSアイコン -->
      <div class="sns">
        <div class="sns-icons">
          <img src="@/assets/svg/icon-facebook.svg" alt="" />
          <img src="@/assets/svg/icon-instagram.svg" alt="" />
          <img src="@/assets/svg/icon-pintarest.svg" alt="" />
        </div>
      </div>
    </div>

    <div class="footer-copy">
      Copyright &copy; 店舗設計・デザイン・施工 CYPHER. AllRights Reserved
    </div>
  </footer>
</template>
  
  
  <script>
export default {
  setup() {
    const pageListleft = reactive([
      { title: "ホーム", to: "#" },
      { title: "私たちについて", to: "#" },
      { title: "選ばれる理由", to: "#" },
      { title: "ワークフロー", to: "#" },
      { title: "FAQ", to: "#" },
      { title: "事例紹介", to: "#" },
    ]);

    const pageListright = reactive([
      { title: "会社概要", to: "#" },
      { title: "お問い合わせ・お見積", to: "#" },
      { title: "個人情報保護法について", to: "#" },
    ]);
    return { pageListleft, pageListright };
  },
};
</script>
  
  <style lang="scss" scoped>
footer {
  color: #fff;
}

.footer-inner {
  background-color: #756d6d;
  padding: 100px;
}
.footer-content {
  display: flex;
  justify-content: space-between;
  @include mobile {
    display: block;
  }
}
.footer-logo-top {
  width: 200px;
  height: auto;
}

.footer-left {
  width: 20%;
  font-size: 22px;
  @include mobile {
    width: 100%;
  }
}

.nav-left {
  width: 20%;
  font-size: 18px;
  @include mobile {
    width: 100%;
  }
}

.nav-right {
  width: 20%;
  font-size: 18px;
  padding-right: 80px;
  @include mobile {
    width: 100%;
  }
}

.address {
  width: 40%;
  font-size: 18px;
  border: solid 1px;
  outline: solid 1px;
  outline-offset: 5px;
  margin: 2px;
  padding: 10px 20px;
  @include mobile {
    width: 100%;
  }
}

.sns {
  display: flex;
  justify-content: flex-end;
  padding-top: 20px;
  margin-right: 150px;
}
.sns-icons {
  width: 40px;
  height: auto;
  gap: 20px;
  display: flex;
}

//==============
// copyright
//==============
.footer-copy {
  color: #333;
  font-size: 10px;
  background-color: #fff;
  text-align: center;
  padding: 20px;
}
</style>