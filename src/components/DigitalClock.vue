<template>
  <div class="timeanddate">
    <div>
      <p class="time">
        {{ currentTime.toLocaleTimeString() }}
      </p>
    </div>
  </div>
</template>
<script>
import { useCurrentTime } from "../composables/useCurrentTime";
export default {
  name: "CurrentTimeExample",
  setup() {
    const { currentTime } = useCurrentTime();
    console.log(currentTime.value);
    return { currentTime };
  },
};
</script>
<style>
@media (min-width: 1024px) {
  .timeanddate {
    display: flex;
    align-items: center;
    justify-self: center;
  }
  .time {
    font-family: "Orbitron", sans-serif;
    color: white;
    font-size: 150px;
    padding-top: 80px;
    text-align: center;
    text-shadow: 10px;
  }

  .date {
    font-family: "Orbitron", sans-serif;
    color: white;
    font-size: 100px;
    text-align: center;
  }
}
</style>
