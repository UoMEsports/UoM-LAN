<template>
  <div class="home">
    <img src="@/assets/header.png" class="header">

    <CustomButton class="su-button" @click="goToSU()">
      BUY TICKETS
    </CustomButton>

    <CustomButton @click="goToForm()">
      RESERVE SEAT
    </CustomButton>

    <div class="content">
      <InfoPanel>
        <template v-slot:title>
          What's a LAN?
        </template>

        A bunch of people bringing their PC (or borrowing a laptop from the ever-helpful ROG) to a room in the SU to play PC games all day. Everyone joins the Local Area Network (or LAN) and plays the games they would be playing at home, but now at least they can tell their parents they leave their room. Think splitscreen but with multiple screens.
      </InfoPanel>
      <InfoPanel>
        <template v-slot:title>
          How do I sign up?
        </template>

        Tickets are sold through the SU website at the link above. Once you have purchased your ticket, return here and fill in the signup form.<br><br>

        Just tell us the email you used and if you would like to sit near any of your friends and we'll email you to confirm your seat!
      </InfoPanel>
      <InfoPanel>
        <template v-slot:title>
          What do I need to bring?
        </template>

        If you're bringing your own PC:<br>
        <ul>
          <li>Your PC</li>
          <li>A monitor</li>
          <li>Your peripherals</li>
        </ul>

        Everyone needs to bring:<br>
        <ul>
          <li>Food/money for food</li>
          <li></li>
          <li>Food/money for food</li>
          <li>Your society wristband!</li>
        </ul>
      </InfoPanel>
      <InfoPanel>
        <template v-slot:title>
          What will there be to do?
        </template>

        <ul>
          <li>Mini Tournaments</li>
          <li>VR Games</li>
          <li></li>
        </ul>
      </InfoPanel>
    </div>
  </div>
</template>

<script>
import CustomButton from '@/components/CustomButton.vue';
import InfoPanel from '@/components/InfoPanel.vue';

export default {
  name: 'home',
  methods: {
    goToSU () {
      window.open('https://manchesterstudentsunion.com/groups/esports-society', '_blank');
    }
  },
  components: {
    CustomButton,
    InfoPanel
  }
};
</script>

<style lang="scss" scoped>
.header {
  display: block;
  max-width: 90%;
  margin: 60px auto;
}

.content {
  width: 1000px;
  max-width: 100%;
  margin: auto;
  margin-top: 40px;

  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
}

.su-button {
  margin-bottom: 20px;
}
</style>
