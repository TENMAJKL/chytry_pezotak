<template>
  <view class="container">
    <text class="h1">Pežoťák</text>
    <view class="card">
       <text class="h3">Poslední jízda</text>
       <text class="text">Kaufland -> Škola</text>
       <text class="text">69 Km</text>
       <text class="text">23. 4. 2021 14:00 - 14:03</text>
    </view>
    <view class="card">
        <text class="h3">Celkem najeto</text>
        <text class="text">{{ total_mileage }} Km</text>
    </view>
    <view class="card">
        <text class="h3">Celkem projeto</text>
        <text class="text">{{ debt }} HC</text>
        <text class="text">Prodej ledvinu</text>
    </view>
  </view>
</template>

<style>

.container {
    background-color: #21252b;
    flex: 1;
}

.h1 {
    font-size: 30;
    margin-top: 28;
    margin-left: 12;
    color: white;
}

.h3 {
    font-size: 15;
    color: white;
}

.text {
    color: white;
    font-size: 22;
}

.card {
    margin-top: 12;
    margin-left: 12;
    margin-right: 12;
    padding-top: 21;
    padding-left: 12;
    padding-bottom: 26;
    background-color: #282c34;
}
</style>


<script>
export default {
    data() {
        return {
            total_mileage: 23000,
            oil_price: 31,
            debt: 0
        }
    },
    mounted() {
        this.debt = this.total_mileage * this.oil_price
    },
    watch: {
        total_mileage() {
            this.debt = this.total_mileage * this.oil_price
        }
    }
}
</script>
