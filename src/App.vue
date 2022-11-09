<script setup lang="ts">
import { ref } from "vue";
const count = ref<number>(0);

let increment = () => {
  count.value++;
};

let modeule = ref<boolean>(false);
// let modeule: boolean = false;

let modeuleSwitch = () => {
  modeule.value = !modeule.value;
  // count.value++;
};
// import { RouterLink, RouterView } from "vue-router";
// import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <!-- <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>

  <RouterView /> -->

  <div class="h-[100vh]">
    <!-- Header -->
    <div>
      <!-- {{ count }} -->
      <!-- {{ modeule }} -->
      <div class="h-[60px] flex justify-center bg-slate-800">
        <div class="w-[100%] flex justify-end items-center bg-slate-700">
          <div class="w-[40px] h-[40px] mr-[20px] bg-slate-600">
            <RouterLink to="/">Home</RouterLink>
          </div>
          <div class="w-[40px] h-[40px] mr-[20px] bg-slate-600">
            <RouterLink to="/admin">Admin</RouterLink>
          </div>
          <div class="w-[40px] h-[40px] mr-[20px] bg-slate-600">
            <RouterLink to="/about">About</RouterLink>
          </div>
          <!--  -->
          <div
            @click="modeuleSwitch"
            class="w-[40px] h-[40px] bg-slate-600"
          ></div>
        </div>
      </div>
    </div>
    <!-- Main -->
    <RouterView />
    <!-- <div
      class="max-h-[100%] h-[100vh] flex flex-col justify-center items-center bg-slate-900"
    >
      <div
        class="w-[50%] mb-[20px] flex bg-slate-800 justify-start overflow-x-scroll scrollbar-hide snap-x"
      >
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
        <div
          class="max-w-[160px] min-w-[160px] w-[100%] h-[160px] mr-[10px] last:mr-0 bg-slate-700 snap-start"
        ></div>
      </div>
    </div> -->
  </div>

  <div
    v-if="modeule"
    @click="modeuleSwitch"
    class="w-[100%] h-[100%] absolute top-0 left-0 bg-slate-300"
  >
    <div class="w-[100%] h-[100%] flex justify-center items-center">
      <div @click.stop class="w-[450px] h-[250px] bg-slate-400"></div>
    </div>
  </div>
</template>

<style scoped></style>
