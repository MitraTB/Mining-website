<template>
  <div class="d-flex">
    <div class="d-flex">
      <div class="bit mx-xl-2 mx-1 mx-lg-2 mx-md-2 mx-sm-2">
        <v-icon>mdi-bitcoin</v-icon>
      </div>
      <div style="color: #70df70">
        <p>$60300.37</p>
        <p>(3.08%)</p>
      </div>
    </div>
    <div class="d-flex">
      <div class="ether mx-1 mx-xl-2 mx-lg-2 mx-md-2 mx-sm-2">
        <v-icon>mdi-ethereum</v-icon>
      </div>
      <div style="color: #ff6565">
        <p>$60300.37</p>
        <p>(3.08%)</p>
      </div>
    </div>
  </div>
</template>
<style scoped>
.ether {
  border-radius: 50%;
  border: thick double #ff6565;
  width: 85px;
  height: 85px;
  padding: 30px;
  color: #ff6565;
}
.bit {
  border-radius: 50%;
  border: thick double #70df70;
  width: 85px;
  height: 85px;
  padding: 30px;
  color: #70df70;
}
</style>
