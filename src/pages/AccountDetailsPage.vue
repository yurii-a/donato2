<template>
  <div class="wrapper starter-page d-flex justify-content-center align-items-center">
    <div class=" card-blog text-center">
      <!-- <div class="card-image">
        <img class="img rounded" src="img/binance-qr.png">
      </div> -->
      <div class="card-body">
        <h4 class="card-title">Donate to crypto accounts</h4>
        <p class="card-text">Pay from your crypto wallet through the chain of your choice</p>
        <ul>
          

Рахунок BITCOIN<br>
bc1qkd5az2ml7dk5j5h672yhxmhmxe9tuf97j39fm6<br/>
<br/>
Рахунок ETHEREUM (eth, usdt, usdc)<br/>
0xa1b1bbB8070Df2450810b8eB2425D543cfCeF79b<br/>
0x93Bda139023d582C19D70F55561f232D3CA6a54c<br/>
<br/>
Рахунок TRC20 (tether)<br/>
TX9aNri16bSxVYi6oMnKDj5RMKAMBXWzon<br/>
<br/>
Рахунок Solana (sol)<br/>
8icxpGYCoR8SRKqLYsSarcAjBjBPuXAuHkeJjJx5ju7a<br/>
</ul>


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
