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
      default: "",
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
          bg: "bg-black",
          bgHover: "bg-gray-500",
          text: "text-white",
        },
        white: {},
        gray: {},
        red: {},
        yellow: {},
        green: {},
        blue: {},
        indigo: {},
        purple: {},
        pink: {},
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
        break;
      case `rounded`:
        this.css = `focus:outline-none text-${this.textColor}-600 text-sm py-1 px-2 rounded-full border border-${this.color}-600 hover:bg-${this.color}-600 hover:text-white`;
        break;
      case `flat`:
        this.css = `focus:outline-none text-${this.textColor}-600 text-sm py-1 px-2 rounded hover:bg-${this.color}-200`;
        break;
      case `flat-rounded`:
        this.css = `bg-${this.color}-500 focus:outline-none text-white text-sm py-1 px-2 rounded-full border border-${this.color}-600 hover:bg-${this.color}-600 hover:text-white`;
        break;
      case `disabled`:
        this.css = `focus:outline-none text-white text-sm py-1 px-2 rounded bg-${this.color}-300`;
        this.disabled = true;
        break;
      default:
        this.css = `${this.colors[this.color].bg} ${
          this.colors[this.color].text
        } hover:${
          this.colors[this.color].bgHover
        } py-1 px-2 rounded font-medium mx-3 transition duration-200 each-in-out`;
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
