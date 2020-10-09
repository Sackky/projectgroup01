<template>
<div>
    <center>
    <h1>Welcome to the online computer shopping website.</h1>
    </center>
  <v-hover v-slot:default="{ hover }">
    <v-card class="mx-auto" color="grey lighten-4" max-width="600">
      <v-img
        :aspect-ratio="16 / 9"
        src="https://www.jib.co.th/img_master/product/original/2020020709311336665_1.jpg"
      >
        <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text"
            style="height: 100%"
          >
            $421.21
          </div>
        </v-expand-transition>
      </v-img>
      <v-card-text class="pt-6" style="position: relative">
        <v-btn absolute color="orange" class="white--text" fab large right top>
          <v-icon>mdi-cart</v-icon>
        </v-btn>
        <div class="font-weight-light grey--text title mb-2">
          For workstations
        </div>
        <h3 class="display-1 font-weight-light orange--text mb-2">
          CPU RYZEN THREADRIPPER 3990X
        </h3>
        <div class="font-weight-light title mb-2">
          Sockets TRX4<br />
          64 Core 128 Thread<br />
          Frequency 2.9 GHz<br />
          Turbo 4.3 GHz.<br />
          Architecture7 nm<br />
          Cache L232 MB<br />
          Cache L3256 MB<br />
          TDP280 W<br />
        </div>
      </v-card-text>
    </v-card>
  </v-hover>
  <br>
  <v-hover v-slot:default="{ hover }">
    <v-card class="mx-auto" color="grey lighten-4" max-width="600">
      <v-img
        :aspect-ratio="16 / 9"
        src="https://www.jib.co.th/img_master/product/original/2020061508410640302_1.jpg"
      >
        <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text"
            style="height: 100%"
          >
            $196.66
          </div>
        </v-expand-transition>
      </v-img>
      <v-card-text class="pt-6" style="position: relative">
        <v-btn absolute color="orange" class="white--text" fab large right top>
          <v-icon>mdi-cart</v-icon>
        </v-btn>
        <div class="font-weight-light grey--text title mb-2">
          For gaming
        </div>
        <h3 class="display-1 font-weight-light orange--text mb-2">
          RAM THERMALTAKE TOUGHRAM RGB (BLACK) DDR4 BUS 4600
        </h3>
        <div class="font-weight-light title mb-2">
          Capacity : 16 GB<br />
Speed : 4600 MHz<br />
Part Number : R009D408GX2-4600C19A<br />
8GBx2<br />
        </div>
      </v-card-text>
    </v-card>
  </v-hover>
  <br>
  <v-hover v-slot:default="{ hover }">
    <v-card class="mx-auto" color="grey lighten-4" max-width="600">
      <v-img
        :aspect-ratio="16 / 9"
        src="https://www.jib.co.th/img_master/product/original/20190711173156_34428_23_1.jpg"
      >
        <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text"
            style="height: 100%"
          >
            $481.81
          </div>
        </v-expand-transition>
      </v-img>
      <v-card-text class="pt-6" style="position: relative">
        <v-btn absolute color="orange" class="white--text" fab large right top>
          <v-icon>mdi-cart</v-icon>
        </v-btn>
        <div class="font-weight-light grey--text title mb-2">
          For workstations
        </div>
        <h3 class="display-1 font-weight-light orange--text mb-2">
          MAINBOARD MSI PRESTIGE X570 CREATION
        </h3>
        <div class="font-weight-light title mb-2">
          SOCKET : AM4
CHIPSET : AMD X570<br />
Supports 2-Way NVIDIA® SLI™ Technology<br />
Supports 3-Way AMD® CrossFire™ Technology<br />
Slot3 x PCIe 4.0 x16 Slot , 4 x PCIe 2.0 x1 Slots<br />
Chipset LAN1 x Intel I211AT 1 x Aquantia AQC107 10-Gigabit<br />
Wi-Fi Intel Wi-Fi 6 AX200 802.11 a/b/g/n/ac/ax MU-MINO Rx 2.4GHz-5GHz Bluetooth 5<br />
USB 2.02 Port<br />
USB 3.210 x USB 3.2 Gen1 Type-A 2 x USB 3.2 Gen2 Type-A & Type-C Port<br />
Audio Output 5 x Audio jack 1 x Optical S/PDIF Out Port<br />
PS2 Port1 (Keyboard/Mouse combo)<br />
LAN (RJ45) 2<br />
Option Port 1 x Clear CMOS button<br />
2 x Wi-Fi Antenna connectors<br />
        </div>
      </v-card-text>
    </v-card>
  </v-hover>
  </div>
</template>

<script>
export default {};
</script>

<style>
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: 0.5;
  position: absolute;
  width: 100%;
}
</style>