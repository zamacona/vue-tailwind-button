<script>
import { defineComponent } from "vue";
import VueTailwindButton from "@/vue-tailwind-button.vue";
import "./index.css";
export default defineComponent({
  name: "ServeDev",
  components: {
    VueTailwindButton,
  },
});
</script>

<template>
  <div id="app" class="mt-10 mx-28">
    <div class="grid justify-items-center grid-cols-10">
      <vue-tailwind-button color="black"> black </vue-tailwind-button>
      <vue-tailwind-button color="white"> white </vue-tailwind-button>
      <vue-tailwind-button color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button color="red"> red </vue-tailwind-button>
      <vue-tailwind-button color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button color="green"> green </vue-tailwind-button>
      <vue-tailwind-button color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button color="pink"> pink </vue-tailwind-button>
    </div>
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button mode="outline" color="black"> black </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="white"> white </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="red"> red </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="green"> green </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button mode="outline" color="pink"> pink </vue-tailwind-button>
    </div>
  </div>
</template>
