# 001 Adding Charts
## ChartsJS to Quasar

Install npm package

`npm install vue-chartjs chartsjs`

### Making the Chart Component
Make the component separate of the page so that you can later import it into the page. This is just a generic template. Instructions used were [here](https://github.com/apertureless/vue-chartjs). 

 ==example is a bar chart==


```js
<template>
<Bar
:chart-options="chartOptions"
:chart-data="chartData"
:chart-id="chartId"
:dataset-id-key="datasetIdKey"
:plugins="plugins"
:css-classes="cssClasses"
:styles="styles"
:width="width"
:height="height"
/>
</template>

  

<script>
import { Bar } from "vue-chartjs";
import {
Chart as ChartJS,
Title,
Tooltip,
Legend,
BarElement,
CategoryScale,
LinearScale,
} from "chart.js";

ChartJS.register(
Title,
Tooltip,
Legend,
BarElement,
CategoryScale,
LinearScale
);

export default {
name: "BarChart",
components: { Bar },
props: {
chartId: {
type: String,
default: "bar-chart",
},
datasetIdKey: {
type: String,
default: "label",
},
width: {
type: Number,
default: 400,
},
height: {
type: Number,
default: 400,
},
cssClasses: {
default: "",
type: String,
},
styles: {
type: Object,
default: () => {},
},
plugins: {
type: Array,
default: () => [],
},
},
data() {
return {
chartData: {
labels: ["January", "February", "March"],
datasets: [{ data: [40, 20, 12] }],
},
chartOptions: {
responsive: true,
},
};
},
};

</script>

```

### Making the Parent Component
```js
<template>
<q-page padding>

<AccountBalance></AccountBalance>

</q-page>
</template>

<script>

import { defineComponent } from "vue";
import AccountBalance from "../components/AccountBalance";

export default defineComponent({
name: "AccountPage",
components: { AccountBalance },
});

</script>
```

## Quasar Components Chart

Installing packages

`npm i quasar-components-chart --save`

## Making the Chart Component

Import the Component
```js
import QChart from 'quasar-components-chart'
```

Register the Component
```js
import QChart from "chart.js";

export default {
  components: { QChart },
  data() {
    return {};
  }
}
```

Use the Component
```js
<q-chart 
  identifier="myChart"
  stilo="height:30vh; width: 100%"
  :type="line"
  :labels="labels"
  :datasets="datasets"
  :options="options"
/>
```

