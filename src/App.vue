<template>
  <div id="app">
    <div id="top-block">
      <b-row>
        <b-col cols="3">
          <b-button variant="success" class="start-button">start</b-button>
        </b-col>
        <b-col cols="5">
          <h1 id="title">Elevator Simulator</h1>
        </b-col>
        <b-col cols="3">
          <h3 id="title">wait time: </h3>
        </b-col>
      </b-row>
    </div>
    <TopFloor 
      :peopleNumber="0"
      :floorNumber="16"
     />
     <div v-for="n in 15" :key="n">
       <MiddleFloor
        :peopleNumber="0"
        :floorNumber="16 - n"
       />
     </div>
     <BottomFloor
      :peopleNumber="0"
      :floorNumber="-1"
     />
  </div>
</template>

<script>
import TopFloor from './components/TopFloor.vue';
import MiddleFloor from './components/MiddleFloor.vue';
import BottomFloor from './components/BottomFloor.vue';

export default {
  name: 'App',
  components: {
    TopFloor,
    MiddleFloor,
    BottomFloor,
  },
  data() {
    return {
      floorPeopleCount: [],
    };
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

#top-block {
  width: 90%;
  min-width: 1000px;
  height: 60px;
  margin: auto;
}

#title {
  text-align: center;
}

.start-button {
  height: 48px;
  width: 80px;
}
</style>
