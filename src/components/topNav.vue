<template>
  <div class="top-nav bg-white flex justify-between items-center w-100">
    <div>
      <img src="images/menu.png" width="20" />
    </div>
    <div class="flex item-center">
      <img src="images/alert.png" class="mr-4" width="34px" />
      <div class="profile-details">
        <p>Bidemi Yusuf</p>
        <p>Executive</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.top-nav {
  padding: 14px 41px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
}
.profile-details p {
  line-height: 1.18;
  letter-spacing: normal;
  color: #000000;
}
.profile-details p:nth-of-type(2) {
  height: 13px;
  font-family: SourceSansPro;
  font-size: 11px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
}
</style>
