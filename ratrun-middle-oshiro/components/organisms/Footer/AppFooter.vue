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

        <nav class="nav-left">
          <ul class="nav-left-items">
            <!-- v-for=vueの繰り返し文 -->
            <li v-for="(page, key) in pageListleft" :key="key">
              <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
            </li>
          </ul>
        </nav>

        <!-- 右のエリア -->
        <nav class="nav-right">
          <ul class="nav-right-items">
            <!-- v-for=vueの繰り返し文 -->
            <li v-for="(page, key) in pageListright" :key="key">
              <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
            </li>
          </ul>
        </nav>

        <div class="address">
          <p>
            建築・建築デザイン・原状 回復・内装解体・建物br
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
      <div class="sns-icons">
        <img src="@/assets/svg/icon-facebook.svg" alt="" />
        <img src="@/assets/svg/icon-instagram.svg" alt="" />
        <img src="@/assets/svg/icon-pintarest.svg" alt="" />
      </div>
    

    <div class="footer-copy">
      Copyright &copy; 店舗設計・デザイン・施工 CYPHER. AllRights Reserved
    </div>
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
  background-color: #756d6d;
  padding: 40px 20px;
}

.footer-inner {
  padding: 50px 20px;
}
.footer-content {
  display: flex;
  justify-content: space-between;
}
.footer-logo-top {
  width: 150px;
  height: auto;
}

.address {
  border: solid 1px;
  outline: solid 1px;
  outline-offset: 5px;
  margin: 2px;
  padding: 20px;
}

.sns-icons {
  width: 40px;
  height: auto;
  display: flex;
  gap: 20px;
  margin-bottom: 60px;
  margin-left: 30px;
}
//==============
// copyright
//==============
.footer-copy {
  color: #333;
  background-color: #fff;
  text-align: center;
  padding: 20px;
}
</style>