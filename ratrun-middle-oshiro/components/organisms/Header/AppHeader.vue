<template>
  <header>
    <div class="pc-header">
      <nav class="nav">
        <ul class="nav-list">
          <!-- v-for=vueの繰り返し文 -->
          <li v-for="(page, key) in pageList" :key="key">
            <!-- nuxt-linkはaタグと一緒 -->
            <!-- hrefがtoになったイメージ -->
            <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
          </li>
        </ul>
      </nav>
    </div>

    <div class="sp-header">
      <button class="menu-button" @click="isClickMenu">
        <img src="@/assets/svg/hamburger.svg" alt="" />
      </button>

      <!-- v-sho -->
      <div class="display-menu" v-show="isOpenMenu">
        <ul class="nav-list-sp">
          <!-- v-for=vueの繰り返し文 -->
          <li v-for="(page, key) in pageList" :key="key">
            <!-- nuxt-linkはaタグと一緒 -->
            <!-- hrefがtoになったイメージ -->
            <nuxt-link :to="page.to">{{ page.title }}</nuxt-link>
          </li>
        </ul>

        <!-- SNSアイコン -->
        <div class="sns-icons">
          <img src="@/assets/svg/icon-facebook.svg" alt="" />
          <img src="@/assets/svg/icon-instagram.svg" alt="" />
          <img src="@/assets/svg/icon-pintarest.svg" alt="" />
        </div>
      </div>
    </div>
  </header>
</template>


<script>
export default {
  setup() {
    const pageList = reactive([
      // objectの配列{}の中身が
      { title: "ホーム", to: "#" },
      { title: "経営理念", to: "#" },
      { title: "事業理念", to: "#" },
      { title: "事業目的", to: "#" },
      { title: "お問い合わせ", to: "#" },
    ]);

    // v-show(true or (初期値)falseがデフォルト)クリックした時にに変更する,ref reactive(中身がobject,それ以外はref)
    // refがついてると.valueをつけないと値が取れない
    const isOpenMenu = ref(false);
    // アロー関数
    const isClickMenu = () => {
      isOpenMenu.value = !isOpenMenu.value;
      // console.log (!isOpenMenu.value)
    };

    return { pageList, isOpenMenu, isClickMenu };
  },
};
</script>

<style lang="scss" scoped>
//====================
// header
//====================
header {
 // absoluteだけでも使えてその場合は1番上になる
 position: absolute;
  left: 0;
  top: 0;
  z-index: 1;
}
.pc-header {
  @include mobile {
    display: none;
  }
  font-size: 16px;
}

.sp-header {
  display: none;
  @include mobile {
    display: block;
  }
}

.display-menu {
  border: 1px solid;
  position: fixed;
  top: 50px;
  width: 99%;
  background-color: #fff;
}
.nav-list-sp {
}
.menu-button {
  width: 40px;
  height: 40px;
  border: none;
  background-color: #fff;
  position: fixed;
  right: 0;
}
.nav-list {
  display: flex;
  gap: 20px;
}

.sns-icons {
  width: 40px;
  height: auto;
  display: flex;
  gap: 20px;
  margin-bottom: 60px;
  margin-left: 30px;
}
.top {
  background-image: url("@assets/svg/cyber-g15cd33eba_1920.png");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;

  .top-title {
    font-size: 60px;
  }
  .top-subtitle {
  }

  //====================
  // section
  //====================
  .section {
    // padding: 60px 0;
  }

  .section-title {
    font-size: 32px;
    text-align: center;
  }
}
</style>