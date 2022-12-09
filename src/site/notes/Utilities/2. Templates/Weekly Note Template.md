```dataviewjs
const daysPath = dv.current().file.folder;

const attributes = {
	'money-spent': {
		label: 'Money Spent',
		backgroundColor: 'rgba(85, 174, 229, 0.2)',
		borderColor: 'rgba(85, 174, 229, 1)',
		average: 20,
	},
	'steps': {
		label: 'Steps',
		backgroundColor: 'rgba(141, 82, 188, 0.2)',
		borderColor: 'rgba(141, 82, 188, 1)',
		average: 10000,
	},
	'hours-worked': {
		label : 'Hours Worked',
		backgroundColor: 'rgba(143, 208, 50, 0.2)',
		borderColor: 'rgba(143, 208, 50, 1)',
		average: 6
	},
};

const date = "<% tp.date.now('YYYY-MM-DD') %>";

customJS.DvCharts.renderWeeklyChart({
	dv,
	context: this,
	daysPath: '02 Personal/02.01 Periodic Notes/<% tp.date.now("YYYY") %>/Daily/<%tp.date.now("MM MMMM")%>',
	attributes,
	type: 'average',
	date
})
```