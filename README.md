*A Vue.js wrapper for the beautiful date-range picker made by the Baremetrics team.*

The Vue-Baremetrics date range picker is a simplified solution for selecting both date ranges and single dates all from a single calender view. With a revamped minimalistic redesign.

Redesigned and Wrapped for Vue.js by Divyansh Tripathi

**View a demo
**NPM Package


*Installation*
npm i --save vue2-baremetrics-calendar

Usage
Global Usage
Global Registeration via Vue.use() method.

// main.js
import Vue from "vue";
import App from "./App.vue";
import router from "./router";
// import the plugin
import Calendar from "vue2-baremetrics-calendar";

Vue.config.productionTip = false;

// use the plugin
Vue.use(Calendar);

new Vue({
  router,
  render: h => h(App)
}).$mount("#app");
Once registered you can use the component in its default settings with as follows:-

<Calendar
  type="double"
  @rangeEdit="processDateRange()"
  elementName="doubleRangePicker"
/>

<Calendar
  type="single"
  @dateEdit="processDate()"
  elementName="singleRangePicker"
/>
REMEMBER elementName is the only required prop and it should be different for each datepicker in your component

<template>
  <div id="app">
    <Calendar
      @rangeEdit="processOutput"
      type="double"
      elementName="otherRangePicker"
    />

    <Calendar
      @dateEdit="processOutput"
      type="single"
      elementName="primaryRangePicker"
    />
  </div>
</template>

<script>
  import Calendar from "./components/Calendar";
  export default {
    components: {
      Calendar
    },
    methods: {
      processOutput(output) {
        console.log(output);
      }
    }
  };
</script>

============
Мы на столько крутые, что уже успели поработать со следующими команиями:

ООО «Рога и копыта»
Издательство «Читый лист»
Космопорт «Черезтерновый Кзвёздный»
Дизайн-студия имени Слишком Известного Персонажа
Ниже пример кода из нашего приложения:

```
.selector {
  font-family: "Awesome", Arial, sans-serif;
  color: red;
}
```