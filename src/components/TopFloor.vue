<template>
  <div id="floor-block">
    <div id="left-outline"></div>
    <div id ="right-outline">
      <b-img src="../assets/People-05.svg" class="people-icon" />
      <span class="number">{{ peopleNumber }}</span>
      <span class="floor-number">{{ floorNumber }}F</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'TopFloor',
  data() {
    return {
    };
  },
  props: {
    peopleNumber: Number,
    floorNumber: Number,
  },
};
</script>
<style scoped>
#floor-block {
  width: 90%;
  min-width: 1000px;
  height: 120px;
  margin: auto;
  margin-bottom: 30px;
}

#left-outline {
  width: 50%;
  height: 100%;
  border-style: ridge;
  border-width: 2px;
  border-color: gray;
  border-right: transparent;
  border-bottom: transparent;
  border-top-left-radius: 20px;
  border-bottom-left-radius: 20px;
  float: left;
}

#right-outline {
  width: 50%;
  height: 100%;
  border-style: ridge;
  border-width: 2px;
  border-color: gray;
  border-left: transparent;
  border-top-right-radius: 20px;
  border-bottom-right-radius: 20px;
  float: left;
  padding: 20px;
}

.people-icon {
  text-align: left;
  width: 80px;
  height: 80px;
  vertical-align: baseline;
  margin-right: 20px;
  float: left;
}

.number {
  line-height: 1;
  font-size: 80px;
}

.floor-number {
  line-height: 1;
  font-size: 80px;
  float: right;
}
</style>