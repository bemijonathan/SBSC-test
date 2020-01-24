<template>
  <div class="text-white h-100" side-bar>
    <section class>
      <div class="logo mt-5 mb-10">
        <img src="../assets/images/logo.png" width="137" />
      </div>
      <li v-for="(nav, i) in nav" :key="i" class="list-none w-100">
        <img :src="nav.image" class="inline" width="16px" />
        {{ nav.title }}
      </li>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      nav: [
        { title: "Dashboard", image: "images/dashboard_home.png" },
        { title: "Budget", image: "images/budget.png" },
        { title: "Approval", image: "images/Approval@3x.png" }
      ]
    };
  }
};
</script>

<style>
.logo {
  font-family: SourceSansPro;
  font-size: 16px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.22;
  letter-spacing: normal;
  margin-left: 32px;
}
[side-bar] {
  width: 243px;
  height: 100vh;
  background-color: #13244e;
}
[side-bar] li {
  margin: 5px 16px;
  padding: 8px 16px;
  height: 36px;
  font-family: SourceSansPro;
  font-size: 15px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.33;
  letter-spacing: normal;
  display: flex;
  align-items: center;
}
[side-bar] li:first-of-type {
  border-radius: 4px;
  background-color: #0093dd;
}
[side-bar] li img {
  width: 16px;
  margin-right: 10px;
}
</style>
