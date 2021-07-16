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
  },
  data() {
    return {
      css: null,
      disabled: false,
      colors: {
        black: {
          bg: this.mode == "solid" ? "bg-black" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-gray-500" : this.mode == "outline" ? "bg-black" : "",
          text: this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-black" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-black" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
        white: {
          bg: this.mode == "solid" ? "bg-white" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-gray-500" : this.mode == "outline" ? "bg-gray-500" : "",
          text: this.mode == "solid" ? "text-black" : this.mode == "outline" ? "text-black" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-white" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
        gray: {
          bg: this.mode == "solid" ? "bg-gray-500" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-gray-600" : this.mode == "outline" ? "bg-gray-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" ? "text-gray-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-gray-500" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
        red: {
          bg: this.mode == "solid" ? "bg-red-500" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-red-700" : this.mode == "outline" ? "bg-red-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" ? "text-red-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-red-500" : "",
          ring: this.mode == "solid" ? "ring-red-400" : this.mode == "outline" ? "ring-red-400" : "",
        },
        yellow: {
          bg: this.mode == "solid" ? "bg-yellow-500" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-yellow-700" : this.mode == "outline" ? "bg-yellow-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" ? "text-yellow-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-yellow-500" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
        green: {
          bg: this.mode == "solid" ? "bg-green-500" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-green-700" : this.mode == "outline" ? "bg-green-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" ? "text-green-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-green-500" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
        blue: {
          bg: this.mode == "solid" ? "bg-blue-500" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-blue-700" : this.mode == "outline" ? "bg-blue-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" ? "text-blue-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-blue-500" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
        indigo: {
          bg: this.mode == "solid" ? "bg-indigo-500" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-indigo-700" : this.mode == "outline" ? "bg-indigo-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" ? "text-indigo-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-indigo-500" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
        purple: {
          bg: this.mode == "solid" ? "bg-purple-500" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-purple-700" : this.mode == "outline" ? "bg-purple-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" ? "text-purple-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-purple-500" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
        pink: {
          bg: this.mode == "solid" ? "bg-pink-500" : this.mode == "outline" ? "bg-white" : "",
          bgHover: this.mode == "solid" ? "bg-pink-700" : this.mode == "outline" ? "bg-pink-600" : "",
          text: this.mode == "solid" ? "text-gray-100" : this.mode == "outline" ? "text-pink-500" : "",
          textHover:  this.mode == "solid" ? "text-white" : this.mode == "outline" ? "text-white" : "",
          border:  this.mode == "solid" ? "" : this.mode == "outline" ? "border-pink-500" : "",
          ring: this.mode == "solid" ? "ring-gray-400" : this.mode == "outline" ? "ring-gray-400" : "",
        },
      },
    };
  },
  // https://tailwindcomponents.com/component/button-component
  mounted() {
    switch (this.mode) {
      case "outline":
        this.css = `focus:outline-none 
        text-sm py-1 px-2 rounded border 
        text-${this.textColor ?? this.color}${
          (this.textColor ?? this.color) != "white" ? "-600" : ""
        }
        border-${this.color}${this.color != "white" ? "-600" : ""}
        hover:bg-${this.color}${this.color != "white" ? "-600" : ""} 
        hover:text-${this.hoverTextColor ?? "white"}${
          (this.hoverTextColor ?? "white") != "white" ? "-600" : ""
        }
        `;


        this.css = `focus:${this.colors[this.color].ring} ${this.colors[this.color].border} ${this.colors[this.color].bg} ${this.colors[this.color].text} hover:${this.colors[this.color].bgHover} hover:${this.colors[this.color].textHover} border focus:outline-none focus:ring-4 py-1 px-2 rounded font-medium mx-3 transition duration-200 each-in-out border`;
        break;
      case "rounded":
        this.css = `focus:outline-none text-${this.textColor}-600 text-sm py-1 px-2 rounded-full border border-${this.color}-600 hover:bg-${this.color}-600 hover:text-white`;
        break;
      case "flat":
        this.css = `focus:outline-none text-${this.textColor}-600 text-sm py-1 px-2 rounded hover:bg-${this.color}-200`;
        break;
      case "flat-rounded":
        this.css = `bg-${this.color}-500 focus:outline-none text-white text-sm py-1 px-2 rounded-full border border-${this.color}-600 hover:bg-${this.color}-600 hover:text-white`;
        break;
      case "disabled":
        this.css = `focus:outline-none text-white text-sm py-1 px-2 rounded bg-${this.color}-300`;
        this.disabled = true;
        break;
      case "solid":
        this.css = `${this.colors[this.color].bg} ${this.colors[this.color].text} hover:${this.colors[this.color].bgHover} hover:${this.colors[this.color].textHover} py-1 px-2 rounded font-medium mx-3 transition duration-200 each-in-out`;
        break;
    }
  },
});
</script>

<template>
  <button :disabled="disabled" :type="type" :class="css">
    <slot></slot>
  </button>
</template>
