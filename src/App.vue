<template>
  <div class="Hero">
    <div>
      <form>
      <input type="text" v-model="Qr" placeholder="Generate Qrcode" />
    </form>
    <div class="Qr">
      <qrcode-vue v-if="Qr" :value="Qr" :size="size" level="H" />
    </div>
  </div>
  </div>
</template>

<script>
import QrcodeVue from "qrcode.vue";
export default {
  data() {
    return {
      Qr: null,
      size: 300,
    };
  },
  components: {
    QrcodeVue,
  },
}
</script>

<style>
body{
  margin:0;
  padding:0;
  background:#0077b6;
}
.Hero {
  text-align: center;
   position: relative;
    -webkit-align-items: center;
    -ms-flex-align: center;
    align-items: center;
    height: 100%;
    justify-content: center;
}
form input {
  padding: 10px;
  margin: 20px;
  font-size: 20px;
  font-family: "Times New Roman", Times, serif;
}
.Qr {
  margin: 20px;
  padding: 20px;
}
 .particles-js {
    position: absolute;
    bottom: -30% !important;
    left: 0;
    width: 100%;
    height: 100%;
  }
</style>