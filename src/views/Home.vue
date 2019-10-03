<template>
  <div class="home">
    <img src="@/assets/header.png" class="header">

    <CustomButton class="su-button" @click="goToSU()">
      BUY TICKETS
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

        Tickets are sold through the SU website at the link above. You'll be asked questions like do you want to borrow a laptop, do you need PC pickup etc. When you're done we'll email you to confirm your seating position and laptop hire status.<br><br>
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
          <li>Food or money for food</li>
          <li>Ethernet cables (if you have any)</li>
          <li>Your society wristband!</li>
        </ul>
      </InfoPanel>
      <InfoPanel>
        <template v-slot:title>
          What will there be to do?
        </template>

        <ul>
          <li>Mini Tournaments in all kinds of games (suggest some when you signup)</li>
          <li>Playing VR Games</li>
          <li>Drinking your weight in energy drinks</li>
          <li>Pick up some League of Legends Realms swag</li>
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
      window.open('https://manchesterstudentsunion.com/groups/esports-society/events/freshers-lan-4c77/buy_ticket', '_blank');
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
  width: 800px;
  display: block;
  max-width: 90%;
  margin: auto;
  margin-bottom: 60px;
  margin-top: 25px;
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
