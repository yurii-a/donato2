<template>
  <div class="wrapper starter-page d-flex justify-content-center align-items-center">
    <div class=" card-blog text-center">
      <!-- <div class="card-image">
        <img class="img rounded" src="img/binance-qr.png">
      </div> -->
      <div class="card-body">
        <h4 class="card-title">Donate with Binance App</h4>
        <p class="card-text">Pay by scanning QR code in your Binance app</p>
        <div class="picture">
          <img src="img/binance-qr.png" alt="QR code" class="rounded img-raised" width="300px">
        </div>
        <button id="paid-btn" class="btn btn-primary btn-round btn-lg" @click="$router.go(-1)">
          I have paid</button>
      </div>
    </div>
  </div>
</template>
<script>
import { Button, Card } from '@/components';
export default { components: {
    [Card.name]: Card,    
    [Button.name]: Button,
} }
</script>
<style scoped>
    .starter-page {
        min-height: calc(100vh - 79px)
    }
    #paid-btn {
      margin-top: 30px;
    }
</style>
