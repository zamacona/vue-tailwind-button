<script>
import { defineComponent } from "vue";

export default /*#__PURE__*/ defineComponent({
  name: "VueTailwindButton", // vue component name
  props: {
    type: {
      type: String,
      default: "submit",
    },
    mode: {
      type: String,
      default: "solid",
    },
    color: {
      type: String,
      default: "blue",
    },
    textColor: {
      type: String,
      default: null,
    },
    hoverTextColor: {
      type: String,
      default: null,
    },
    rounded:{
      type: Boolean,
      default: false
    },
    disabled:{
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      css: null,
      disabled: false,
      colors: {
        black: {
          bg: this.mode == "solid" ? "bg-black" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-gray-500" : this.mode == "outline" || this.mode == "flat" ? "bg-black" : "",
          text: this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-black" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-black" : this.mode == "outline" ? "border-black" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" || this.mode == "flat" ? "ring-gray-400" : "",
        },
        white: {
          bg: this.mode == "solid" ? "bg-white" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-gray-500" : this.mode == "outline" || this.mode == "flat" ? "bg-gray-500" : "",
          text: this.mode == "solid" ? "text-black" : this.mode == "outline" || this.mode == "flat" ? "text-black" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-white" : this.mode == "outline" ? "border-white" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" || this.mode == "flat" ? "ring-gray-400" : "",
        },
        gray: {
          bg: this.mode == "solid" ? "bg-gray-500" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-gray-600" : this.mode == "outline" || this.mode == "flat" ? "bg-gray-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" || this.mode == "flat" ? "text-gray-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-gray-500" : this.mode == "outline" ? "border-gray-500" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" || this.mode == "flat" ? "ring-gray-400" : "",
        },
        red: {
          bg: this.mode == "solid" ? "bg-red-500" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-red-700" : this.mode == "outline" || this.mode == "flat" ? "bg-red-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" || this.mode == "flat" ? "text-red-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-red-500" : this.mode == "outline" ? "border-red-500" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-red-400" : this.mode == "outline" || this.mode == "flat" ? "ring-red-400" : "",
        },
        yellow: {
          bg: this.mode == "solid" ? "bg-yellow-500" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-yellow-700" : this.mode == "outline" || this.mode == "flat" ? "bg-yellow-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" || this.mode == "flat" ? "text-yellow-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-yellow-500" : this.mode == "outline" ? "border-yellow-500" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-yellow-400" : this.mode == "outline" || this.mode == "flat" ? "ring-yellow-400" : "",
        },
        green: {
          bg: this.mode == "solid" ? "bg-green-500" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-green-700" : this.mode == "outline" || this.mode == "flat" ? "bg-green-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" || this.mode == "flat" ? "text-green-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-green-500" : this.mode == "outline" ? "border-green-500" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-green-400" : this.mode == "outline" || this.mode == "flat" ? "ring-green-400" : "",
        },
        blue: {
          bg: this.mode == "solid" ? "bg-blue-500" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-blue-700" : this.mode == "outline" || this.mode == "flat" ? "bg-blue-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" || this.mode == "flat" ? "text-blue-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-blue-500" : this.mode == "outline" ? "border-blue-500" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-blue-400" : this.mode == "outline" || this.mode == "flat" ? "ring-blue-400" : "",
        },
        indigo: {
          bg: this.mode == "solid" ? "bg-indigo-500" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-indigo-700" : this.mode == "outline" || this.mode == "flat" ? "bg-indigo-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" || this.mode == "flat" ? "text-indigo-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-indigo-500" : this.mode == "outline" ? "border-indigo-500" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-indigo-400" : this.mode == "outline" || this.mode == "flat" ? "ring-indigo-400" : "",
        },
        purple: {
          bg: this.mode == "solid" ? "bg-purple-500" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-purple-700" : this.mode == "outline" || this.mode == "flat" ? "bg-purple-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" || this.mode == "flat" ? "text-purple-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-purple-500" : this.mode == "outline" ? "border-purple-500" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-purple-400" : this.mode == "outline" || this.mode == "flat" ? "ring-purple-400" : "",
        },
        pink: {
          bg: this.mode == "solid" ? "bg-pink-500" : this.mode == "outline" || this.mode == "flat" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-pink-700" : this.mode == "outline" || this.mode == "flat" ? "bg-pink-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" || this.mode == "flat" ? "text-pink-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" || this.mode == "flat" ? "text-white" : "",
          border:  this.mode == "solid" ? "border-pink-500" : this.mode == "outline" ? "border-pink-500" : this.mode == "flat" ? "" : "",
          ring: this.mode == "solid" ? "ring-pink-400" : this.mode == "outline" || this.mode == "flat" ? "ring-pink-400" : "",
        },
      },
    };
  },
  // https://tailwindcomponents.com/component/button-component
  mounted() {
    switch (this.mode) {
      case "outline":
        this.css = `focus:${this.colors[this.color].ring} ${this.colors[this.color].border} ${this.colors[this.color].bg} ${this.colors[this.color].text} hover:${this.colors[this.color].bgHover} hover:${this.colors[this.color].textHover} border focus:outline-none focus:ring-4 py-1 px-2 rounded font-medium mx-3 transition duration-200 each-in-out`;
        break;
      case "flat":
        this.css = `focus:${this.colors[this.color].ring} ${this.colors[this.color].border} ${this.colors[this.color].bg} ${this.colors[this.color].text} hover:${this.colors[this.color].bgHover} hover:${this.colors[this.color].textHover} focus:outline-none focus:ring-4 py-1 px-2 rounded font-medium mx-3 transition duration-200 each-in-out`;
        break;
      case "solid":
        this.css = `focus:${this.colors[this.color].ring} ${this.colors[this.color].border} ${this.colors[this.color].bg} ${this.colors[this.color].text} hover:${this.colors[this.color].bgHover} hover:${this.colors[this.color].textHover} border focus:outline-none focus:ring-4 py-1 px-2 rounded font-medium mx-3 transition duration-200 each-in-out`;
        break;
    }

    if(this.rounded) this.css += " rounded-full";
  },
});
</script>

<template>
  <button :disabled="disabled" :type="type" :class="css">
    <slot></slot>
  </button>
</template>
