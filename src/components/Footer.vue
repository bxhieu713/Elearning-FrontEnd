<template>
  <footer class="footer">
    <div class="lefty">
      <el-row class="footer-row">
        <router-link to="/credits"> Credits </router-link>
      </el-row>
      <el-row class="footer-row">About Us</el-row>
      <el-row class="footer-row">
        <!-- Place this tag where you want the button to render. -->
        <github-button
          href="https://github.com/bxhieu713"
          aria-label="Follow @bxhieu713 on GitHub"
        >
          Follow @bxhieu713
        </github-button>
      </el-row>
    </div>
    <div class="righty">
      <el-row>&copy; 2022, Davis T</el-row>
      <el-row>
        <img src="@/assets/final_white.png" alt="logo" id="ft-logo" />
      </el-row>
      <el-row class="credit-cards" title="Supported Payment methods">
      <img height="30" src="https://shoplineimg.com/assets/footer/card_visa.png"/>
      <img height="30" src="https://shoplineimg.com/assets/footer/card_master.png"/>
      <img height="30" src="https://shoplineimg.com/assets/footer/card_paypal.png"/>
      <img height="30" src="https://shoplineimg.com/assets/footer/card_amex.png"/>
      <img height="30" src="https://shoplineimg.com/assets/footer/card_jcb.png"/>
      </el-row>
    </div>
  </footer>
</template>

<script>
import GithubButton from "vue-github-button";
export default {
  name: "Footer",
  data() {
    return {};
  },
  components: {
    GithubButton,
  },
};
</script>

<style scoped>
.footer {
  width: inherit;
  position: relative;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  bottom: 0;
  padding: 0.25em;
  height: max-content;
  color: white;
  background-color: var(--dark);
}

.lefty {
  margin-top: 0.5em;
  float: left;
}

.footer-row {
  margin-bottom: 5px;
}

.credit-cards {
  margin-bottom: 0.5em;
}

a {
  color: white !important;
}

a:hover {
  border-bottom: 1px solid white;
  /* padding-bottom: 10px; */
}

.credit-cards img {
  margin-right: 0.5em;
}

.righty {
  margin-top: 0.5em;
  float: right;
}

#ft-logo {
  width: 10em;
  margin-top: 1em;
  height: 100%;
}
@media screen and (max-width: 770px) {
  .credit-cards {
    display: none;
  }
}
</style>
