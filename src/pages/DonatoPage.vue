<template>
  <div class="page-header signup-page section-image">
    <div
      class="page-header-image"
      style="background-image: url('img/bg18.jpg')"
    />
    <div class="content">
      <div class="container">
        <div class="row align-center">
          <!-- <div class="col-md-4 ml-auto mr-auto">
            <div class="into info-horizontal">
              <div class="icon icon-primary">
                <i class="now-ui-icons media-2_sound-wave" />
              </div>
              <div class="description">
                <h5 class="info-title">
                  Marketing
                </h5>
                <p class="description">
                  We've created the marketing campaign of the website. It was a very interesting
                  collaboration.
                </p>
              </div>
            </div>
            <div class="info info-horizontal">
              <div class="icon icon-primary">
                <i class="now-ui-icons media-1_button-pause" />
              </div>
              <div class="description">
                <h5 class="info-title">
                  Fully Coded in HTML5
                </h5>
                <p class="description">
                  We've developed the website with HTML5 and CSS3. The client has access to the code
                  using GitHub.
                </p>
              </div>
            </div>
            <div class="info info-horizontal">
              <div class="icon icon-info">
                <i class="now-ui-icons users_single-02" />
              </div>
              <div class="description">
                <h5 class="info-title">
                  Built Audience
                </h5>
                <p class="description">
                  There is also a Fully Customizable CMS Admin Dashboard for this product.
                </p>
              </div>
            </div>
          </div> -->
          <div >

           <div class="col mr-auto">
            <div class="" style="background: #333333">
              <div class="card-body">
                <p class="card-text">Sergii S raises funds</p> 
                <h4 class="card-title text-center">
                  For 100 quadrocopters
                </h4>
                <p class="card-text">We are fundraising for a large batch of 100 Reconnaissance drones DJI Mavic 3 for Armed Forces of Ukraine</p> 

                <p class="card-text">Collected<br> $15 994</p> 
                <p class="card-text">Goal<br> $25 000</p> 

                <!-- <div class="social text-center">
                  <n-button
                    round
                    icon
                    class="btn-twitter"
                  >
                    <i class="fab fa-twitter" />
                  </n-button>
                  <n-button
                    round
                    icon
                    class="btn-dribbble"
                  >
                    <i class="fab fa-dribbble" />
                  </n-button>
                  <n-button
                    round
                    icon
                    class="btn-facebook"
                  >
                    <i class="fab fa-facebook" />
                  </n-button>
                  <h5 class="card-description">
                    or be classical
                  </h5>
                </div> -->
                <!-- <fg-input
                  v-model="form.firstName"
                  addon-left-icon="now-ui-icons users_circle-08"
                  placeholder="First Name..."
                />

                <fg-input
                  v-model="form.lastName"
                  addon-left-icon="now-ui-icons text_caps-small"
                  placeholder="Last Name..."
                />

                <fg-input
                  v-model="form.email"
                  addon-left-icon="now-ui-icons ui-1_email-85"
                  placeholder="Your Email..."
                />

                <n-checkbox v-model="form.agree">
                  I agree to the terms and
                  <a href="#something">conditions</a>.
                </n-checkbox> -->
                <ul>

                  <a
                    class="btn btn-primary btn-round btn-lg btn-block"
                    :href="getAndroidLink()"
                    :v-if="isAndroid()">
                    Pay with Binance 
                </a>

                  <n-button
                    class="btn btn-primary btn-round btn-lg"
                    :v-if="isAndroid() !==true"
                    block
                    @click="$router.push('binancepay')">
                    Pay with Binance (QR)
                  </n-button>

                  <n-button
                    type="primary"
                    round
                    block
                    size="lg"
                    @click="$router.push('accounts')"
                  >
                    I have other wallet
                  </n-button>
                </ul>

              </div>
            </div>
            </div>
          </div>
        </div>
      </div>

    </div>

    <main-footer />
  </div>
</template>
<script>
  import { Button, FormGroupInput, Checkbox, Modal} from '@/components';
  import MainFooter from '@/layout/MainFooter';

  export default {
    name: 'SignupPage',
    bodyClass: 'signup-page',
    components: {
      MainFooter,
      [Button.name]: Button,
      [Checkbox.name]: Checkbox,
      [FormGroupInput.name]: FormGroupInput,
      [Modal.name]: Modal
    },
    data() {
      return {
        form: {
          firstName: '',
          lastName: '',
          email: '',
          agree: false,
        },
        binanceQrLink: "app.binance.com/qr/dplk5354bef1ed4d4832960aa7e61989d71d",
        binanceAndroidIntent: "intent://app.binance.com/qr/dplk5354bef1ed4d4832960aa7e61989d71d#Intent;scheme=https;package=com.binance.dev;end",
        // binanceUri:  binanceAndroidIntent,//: "https://"+ binanceQrLink

      }
    },
    methods: {
      isAndroid() {
        return /Android/i.test(navigator.userAgent);
      },
      getAndroidLink() {
        if (this.isAndroid()){
          return this.binanceAndroidIntent;
        }
        return "https://"+this.binanceQrLink;
      }
    }
  }
</script>
<style>
</style>
