---
date: {{date:YYYY-MM-DD}}
tags: [journal, daily]
rating:
sleep:
productivity:
mood:
energy:
workout:
---

### Navigation
<< [[{{date:YYYY-MM-DD|-1 day}}|Yesterday]] | [[{{date:YYYY-MM-DD|+1 day}}|Tomorrow]] >>

---

### Morning Journal

**What am I grateful for today?**
- 

**What would make today great?**
- 

**Today's goal:**
- 


### Habits

- [ ] Meditation
- [ ] Reading (15+ minutes)
- [ ] Exercise
- [ ] Journaling
- [ ] 2L water


### Day Log

#### What I did today
- 

#### What I learned
- 

#### How I felt
- 


### Evening Review

**Daily Rating:**  / 10

**Today's wins:**
- 

**What could I have done better?**
- 


### Metadata for Dataview

sleep:: 
productivity:: 
mood:: 
energy:: 
workout:: 
rating:: 

---

### 📊 Dynamic Blocks with DataviewJS

#### Smart Navigation Between Existing Notes

```dataviewjs
const curr = dv.current();
const currFile = curr.file;

let pages = dv.pages('"Journal"')
  .where(p => p.file.day)
  .sort(p => p.file.day);

let thisPrevious = null;
let thisNext = null;
let previous = null;

for (let page of pages) {
  if (previous && (page.file.path === currFile.path)) {
    thisPrevious = previous.file;
  }
  if (previous && (previous.file.path === currFile.path)) {
    thisNext = page.file;
    break;
  }
  previous = page;
}

const linkSection = [
  thisPrevious ? thisPrevious.link : "No previous note",
  `[[${currFile.path}|Today]]`,
  thisNext ? thisNext.link : "No next note"
].join(' · ');

dv.span(`<< ${linkSection} >>`);
