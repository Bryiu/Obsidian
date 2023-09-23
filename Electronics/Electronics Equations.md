
## Ohms Law
![[Pasted image 20230922114921.png]]
$$E = mc^2$$
# Calculations
1.  Power in a Load
	1.  Is to find the power being used by a load
		1. This was used in class for determining the power across a resistor

$$P_2=I_t^2R_x$$
2. Voltage Divider Formula
	1. Consists of two or more resistors connected in series with a voltage source. They're used to obtain a smaller voltage from a larger voltage source

$$ V_2 = V_s(\frac {R_x}{R_t})$$
		2. When applying this formula, $$R_x$$ is applied to the divider and the following resistors between the output terminals.


==For Figure 8-5==
dataviewjs
const labels = ['Volts'];
const data = [.01, .1, 1, 10];

const chartData = {
	type: 'line',
	data: {
		labels: labels,
		datasets: [{
			label: 'Fig 8-5',
			data: data
				}]
			}
}
window.renderChart(chartData, this.container);


```
```dataviewjs
const labels = ['One', 'Two', 'Three'];
const data = [1, 2, 3];

const chartData = {  
    type: 'bar',
    data: {
        labels: labels,
        datasets: [{
            label: 'Numbers',
            data: data
        }]
    }
}

window.renderChart(chartData, this.container);
```
 ![[Obsnote1.jpg]]