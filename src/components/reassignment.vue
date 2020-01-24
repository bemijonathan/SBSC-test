<template>
  <div>
    <div v-for="(status, i) in budgets" :key="i" class="reassignment">
      <div reassignment-title>
        <img :src="status.image" />
        {{ status.title }}
      </div>
      <div class="text-center" reassignment-value>{{ status.value }}</div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      budgets: [
        {
          title: "Pending Budget Reassignment Status",
          value: 200,
          image: ""
        },
        {
          title: "Approved Budget Reassignment Status",
          value: 373,
          image: ""
        },
        {
          title: "Declined Budget Reassignment Status",
          value: 372,
          image: ""
        }
      ]
    };
  }
};
</script>

<style>
.reassignment {
  width: 385px;
  border-radius: 6px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
  padding: 3px 19px 30px 24px;
  margin-bottom: 16px;
}
[reassignment-value] {
  height: 71px;
  padding: 24px;
  border-radius: 8px;
  background-color: #f0f3f9;
  font-family: SourceSansPro;
  font-size: 37px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 0.59;
  letter-spacing: normal;
  color: #000000;
}
[reassignment-title] {
  margin-bottom: 25px;
  margin-top: 8px;
  font-family: SourceSansPro;
  font-size: 17px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.29;
  letter-spacing: normal;
  color: #13244e;
}
</style>
