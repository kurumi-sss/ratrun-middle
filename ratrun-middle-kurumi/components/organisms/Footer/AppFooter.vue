<template>
  <footer>
    <div class="footer">
      <div class="footer-one">
        <img class="logo" src="@/assets/png/logo-2-1.png" alt="ratrun" />
        <p>Interior design<br />&<br />Construction</p>
      </div>
      <div class="footer-two">
        <nav class="nav">
          <ul class="navlist">
            <li class="list" v-for="(one, key) in ListOne" :key="key">
              <nuxt-link to="#">{{ one.title }}</nuxt-link>
            </li>
          </ul>
        </nav>
      </div>
      <div class="footer-three">
        <nav class="nav">
          <ul class="navlist">
            <li class="list" v-for="(two, key) in ListTwo" :key="key">
              <nuxt-link to="#">{{ two.title }}</nuxt-link>
            </li>
          </ul>
        </nav>
      </div>
      <div class="footer-four">
        <div class="address">
          <p>
            建築・建築デザイン・現状回復・内装解体・建物解体・アスベスト除去工事はSENTIAにお任せください！
          </p>
          <p>
            <br />株式会社SENTIA<br />〒445-0982<br />愛知県名古屋市高見1-20-2<br />TEL:052-1212-2029
          </p>
        </div>
        <div class="sns">
          <img
            class="icon"
            src="@/assets/svg/icon-facebook.svg"
            alt="facebook"
          />
          <img
            class="icon"
            src="@/assets/svg/icon-instagram.svg"
            alt="instagram"
          />
          <img
            class="icon"
            src="@/assets/svg/icon-pintarest.svg"
            alt="pintarest"
          />
        </div>
      </div>
    </div>
    <div class="copyrigth">
      Copyrigth(c)店舗設計・デザイン・施工 CYPHER.AllRights Reserved
    </div>
  </footer>
</template>

<script>
export default {
  setup() {
    const ListOne = ref([
      { title: "ホーム" },
      { title: "私達について" },
      { title: "選ばれる理由" },
      { title: "ワークフロー" },
      { title: "FAQ" },
      { title: "事例紹介" },
    ]);
    const ListTwo = ref([
      { title: "会社概要" },
      { title: "お問合せ・お見積" },
      { title: "個人情報保護法について" },
    ]);
    return { ListOne, ListTwo };
  },
};
</script>

<style>
.footer {
  width: 100%;
  /* height: 300px; */
  background-color: #756d6d;
  color: white;
  display: flex;
  padding-top: 70px;
}

.footer-one {
  width: 25%;
  text-align: center;
}

.logo {
  width: 50%;
  margin: 0 auto;
}

.list {
  padding-bottom: 10px;
}

.footer-one > p {
  margin: 0 auto;
  padding-top: 30px;
}

.footer-two {
  color: white;
  width: 15%;
}

.footer-three {
  color: white;
  width: 15%;
}

.footer-four {
  width: 45%;
  margin-right: 30px;
  /* position: relative; */
}

.address {
  border: double 5px white;
  padding: 30px;
}

.sns {
  display: flex;
  /* position: absolute; */
  /* margin-right: 50px; */
  justify-content: flex-end;
  padding: 20px 0;
}

.icon {
  width: 30px;
  padding-left: 10px;
  text-align: right;
}

.copyrigth {
  width: 100%;
  background-color: white;
  color: #756d6d;
  text-align: center;
  margin-top: 30px;
}
</style>