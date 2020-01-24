<template>
  <div>
    <div CAPPEX>
      <div class="flex items-center justify-between">
        <div cappex-title>
          Total Annual CAPEX Budget
          <button class="outline-none price">N 50,000,000</button>
        </div>
        <div>
          <button class="dropdown">Annual</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
[cappex-title] {
  font-family: SourceSansPro;
  font-size: 17px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.29;
  letter-spacing: normal;
  color: #13244e;
}
.dropdown {
  padding: 3px 10px;
  border-radius: 6px;
  background-color: rgba(77, 213, 153, 0.2);
  font-family: SourceSansPro;
  font-size: 14px;
  font-weight: normal;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.43;
  letter-spacing: normal;
  color: #4dd599;
}

[CAPPEX] {
  border-radius: 6px;
  box-shadow: 0 7px 64px 0 rgba(19, 36, 78, 0.07);
  background-color: #ffffff;
  padding: 8px 16px 24px;
}

.price {
  padding: 7.6px 17px;
  border-radius: 6px;
  background-color: rgba(81, 44, 98, 0.2);
  font-family: SourceSansPro;
  font-size: 21px;
  font-weight: 600;
  font-stretch: normal;
  font-style: normal;
  line-height: 1.05;
  letter-spacing: normal;
  color: #512c62;
}
</style>
