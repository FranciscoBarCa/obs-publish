---
cssClasses: cards
---

## Semester

```dataviewjs
var a = moment("2022-09-7"); //start date
var b = moment("2022-12-5"); //end

var n = moment()
var t = moment().startOf('day');

let q =  b.diff(a, 'days');
let p =  b.diff(t, 'days');
let r =  t.diff(a, 'days');

let h = n.diff(a, 'hours');
let i = b.diff(a, 'hours');

let html = `<progress style="height:10px;width:80%" value="`+h+`" max="`+i+`"></progress>`

if (r>0 && r<q) {
	html += `\n#### `+p+` days left of `+q+` days\n`
	html += (h/i*100).toFixed(2)+`% complete`
} else if (r==0) {
	html += `\nstars today`
} else if (r==q) {
	html += `\nends today`
} else if (r>q) {
	html += `\nended `+-p+` days ago`
}else {
	html += `\n#### `+-r+` days to go`
}

dv.paragraph(html)

```
## Classes
```dataview
table
where (degree = "MII" or "MIC") and year = 1 and semester = 1
```
 ## Logseq
-
-