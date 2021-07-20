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
  <div class="my-10 mx-28">
    <p class="mt-6 text-center">SOLID</p>
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button href="http://lvh.me:8000/" target="_blank" color="black"> black </vue-tailwind-button>
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
      <vue-tailwind-button disabled color="black"> black </vue-tailwind-button>
      <vue-tailwind-button disabled color="white"> white </vue-tailwind-button>
      <vue-tailwind-button disabled color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button disabled color="red"> red </vue-tailwind-button>
      <vue-tailwind-button disabled color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button disabled color="green"> green </vue-tailwind-button>
      <vue-tailwind-button disabled color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button disabled color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button disabled color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button disabled color="pink"> pink </vue-tailwind-button>
    </div>
      <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button rounded color="black"> black </vue-tailwind-button>
      <vue-tailwind-button rounded color="white"> white </vue-tailwind-button>
      <vue-tailwind-button rounded color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button rounded color="red"> red </vue-tailwind-button>
      <vue-tailwind-button rounded color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button rounded color="green"> green </vue-tailwind-button>
      <vue-tailwind-button rounded color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button rounded color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button rounded color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button rounded color="pink"> pink </vue-tailwind-button>
    </div>

    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button disabled rounded color="black"> black </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="white"> white </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="red"> red </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="green"> green </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button disabled rounded color="pink"> pink </vue-tailwind-button>
    </div>
    <p class="mt-6 text-center">OUTLINE</p>
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
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button disabled mode="outline" color="black"> black </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="white"> white </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="red"> red </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="green"> green </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button disabled mode="outline" color="pink"> pink </vue-tailwind-button>
    </div>
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button rounded mode="outline" color="black"> black </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="white"> white </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="red"> red </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="green"> green </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button rounded mode="outline" color="pink"> pink </vue-tailwind-button>
    </div>
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button disabled rounded mode="outline" color="black"> black </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="white"> white </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="red"> red </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="green"> green </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button disabled rounded mode="outline" color="pink"> pink </vue-tailwind-button>
    </div>
    <p class="mt-6 text-center">FLAT</p>
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button mode="flat" color="black"> black </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="white"> white </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="red"> red </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="green"> green </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button mode="flat" color="pink"> pink </vue-tailwind-button>
    </div>
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button disabled mode="flat" color="black"> black </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="white"> white </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="red"> red </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="green"> green </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" color="pink"> pink </vue-tailwind-button>
    </div>
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button mode="flat" rounded color="black"> black </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="white"> white </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="red"> red </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="green"> green </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button mode="flat" rounded color="pink"> pink </vue-tailwind-button>
    </div>
    <div class="grid justify-items-center grid-cols-10 mt-5">
      <vue-tailwind-button disabled mode="flat" rounded color="black"> black </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="white"> white </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="gray"> gray </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="red"> red </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="yellow"> yellow </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="green"> green </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="blue"> blue </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="indigo"> indigo </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="purple"> purple </vue-tailwind-button>
      <vue-tailwind-button disabled mode="flat" rounded color="pink"> pink </vue-tailwind-button>
    </div>
  </div>
</template>
