<template>
  <div class="text-white h-100" side-bar>
    <section class="fixed" fixed-bar  side-bar>
      <div class="logo mt-5 mb-10">
        <img src="images/logo.png" width="137" />
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
[fixed-bar] {
  width: 243px;
  height: 100vh;
}
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
  /* height: 100vh; */
  background: rgb(19, 36, 78);
  background: linear-gradient(
    144deg,
    rgba(19, 36, 78, 1) 36%,
    rgba(30, 64, 99, 1) 36%,
    rgba(30, 64, 99, 1) 55%,
    rgba(19, 36, 78, 1) 55%,
    rgba(19, 36, 78, 1) 72%,
    rgba(30, 64, 99, 1) 72%,
    rgba(30, 64, 99, 1) 87%
  );
}
[side-bar] li {
  cursor: pointer;
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
