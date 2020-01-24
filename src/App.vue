// eslint-disable-next-line vue/valid-template-root
<template>
  <div class="flex flex-wrap relative">
    <SideNav />
    <section class="flex-1">
      <TopNav />
      <section dashboard-body>
        <header>Dashboard</header>
        <section class="flex">
          <div total-budgets class="flex-1">
            <TotalBudgets />
          </div>
          <div reassignments>
            <Reassignment />
          </div>
        </section>
      </section>
    </section>
  </div>
</template>

<script>
import SideNav from "@/components/sideNav";
import TopNav from "@/components/topNav";
import TotalBudgets from "@/components/totalBugets";
import Reassignment from "@/components/reassignment";
export default {
  components: {
    SideNav,
    TopNav,
    TotalBudgets,
    Reassignment
  }
};
</script>

<style>
/* body{
  max-width: 1440px;
  margin: 0 auto;
} */
[dashboard-body] {
  padding: 40px 44px;
}
[dashboard-body] > section {
  margin: -26px;
}
[dashboard-body] > section [total-budgets],
[dashboard-body] > section [reassignments] {
  padding: 26px;
}
header {
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
