```dataviewjs
dv.span("**🏋️Exercise🏋️**")

const calendarData = {
    colors: {
        red: ["#ff9e82", "#ff7b55", "#ff4d1a", "#e73400", "#bd2a00"]
    },
    entries: []
}

// Define the start date (July 1st of the current year)
const startDate = new Date(new Date().getFullYear(), 6, 1); // July is month 6 (0-indexed)

// Function to parse the date from the filename
function parseDateFromFilename(filename) {
    // Adjust this logic according to your filename format
    const [year, month, day] = filename.split('-').map(Number);
    return new Date(year, month - 1, day); // JavaScript months are 0-indexed
}

for (let page of dv.pages('"Daily Note"').where(p => p.Exercise)) {
    const pageDate = parseDateFromFilename(page.file.name);
    
    // Check if the page date is after July 1st
    if (pageDate >= startDate) {
        calendarData.entries.push({
            date: page.file.name,
            intensity: page.Exercise,
            content: await dv.span(`[](${page.file.name})`), // for hover preview
        });
    }
}

renderHeatmapCalendar(this.container, calendarData);

```

```dataviewjs
dv.span("**🔗Leet Code **- Dont break the chain! 🔗🔗🔗🔗")
const calendarData = {
    colors: {
        white: ["#fff","#fff","#fff","#fff333","#fff"],
    },
    entries: []
}

for(let page of dv.pages('"Daily Note"').where(p=>p.LeetCode)){
    calendarData.entries.push({
        date: page.file.name,
	        intensity: page.LeetCode,
	        content: "🔗"
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```

```dataviewjs
dv.span("**Study**")
const calendarData = {
    colors: {
        red: ["#ff9e82","#ff7b55","#ff4d1a","#e73400","#bd2a00",]
    },
    entries: []
}

for(let page of dv.pages('"Daily Note"').where(p=>p.Study)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.Study,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```

```dataviewjs
dv.span("**Project**")
const calendarData = {
    colors: {
		blue: ["#8cb9ff","#69a3ff","#428bff","#1872ff","#0058e2"],
        pink: ["#ff96cb","#ff70b8","#ff3a9d","#ee0077","#c30062"],
    },
    entries: []
}

for(let page of dv.pages('"Daily Note"').where(p=>p.Project)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.Project,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```

```dataviewjs
dv.span("**Reading**")
const calendarData = {
    colors: {
        red: ["#ff9e82","#ff7b55","#ff4d1a","#e73400","#bd2a00",]
    },
    entries: []
}

for(let page of dv.pages('"Daily Note"').where(p=>p.Reading)){
    calendarData.entries.push({
        date: page.file.name,
        intensity: page.Reading,
        content: await dv.span(`[](${page.file.name})`), //for hover preview
    })
       
}

renderHeatmapCalendar(this.container, calendarData)
```







