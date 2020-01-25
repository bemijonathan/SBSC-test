// eslint-disable-next-line vue/valid-template-root
<template>
  <div class="flex flex-wrap relative">
    <SideNav />
    <section class="flex-1">
      <TopNav />
      <section dashboard-body>
        <div class="flex justify-between items-center">
           <header>Dashboard</header>
           <div class="date">20 Dec 2019, Friday</div>
        </div>
        <section class="flex">
          <div total-budgets class="flex-1">
            <TotalBudgets />
          </div>
          <div reassignments>
            <Reassignment />
          </div>
        </section>
        <div charts class="flex justify-between">
          <ApexStats class="w-1/2" />
          <OpexStats class="w-1/2" />
        </div>
      </section>
    </section>
  </div>
</template>

<script>
import ApexStats from "./components/apexStatistics";
import OpexStats from "./components/opexStatistics";
import SideNav from "@/components/sideNav";
import TopNav from "@/components/topNav";
import TotalBudgets from "@/components/totalBugets";
import Reassignment from "@/components/reassignment";
export default {
  components: {
    SideNav,
    TopNav,
    TotalBudgets,
    Reassignment,
    ApexStats,
    OpexStats
  }
};
</script>

<style>

@font-face {
  font-family: 'SourceSansPro';
  src: URL('/fonts/SourceSansPro-Regular.ttf') format('truetype');
}

.date{
   font-family: SourceSansPro;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.43;
  letter-spacing: normal;
  color: #000000;
}

[charts] {
  margin: -10px;
}
[charts] > div{
  padding: 10px;
}
/* body{
  max-width: 1440px;
  margin: 0 auto;
} */
[dashboard-body] {
  padding: 40px 44px;
}
[dashboard-body] > section {
  margin: -12px;
}
[dashboard-body] > section [total-budgets],
[dashboard-body] > section [reassignments] {
  padding: 12px;
}
header {
  margin-bottom: 14px;
  font-family: France;
  font-size: 22px;
  font-weight: bold;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.27;
  letter-spacing: normal;
  color: #13244e;
}
</style>
