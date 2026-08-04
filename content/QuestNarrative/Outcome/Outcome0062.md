---
publish: true
created: 2026-07-27T15:36:45.723Z
modified: 2026-07-28T13:37:11.761Z
published: 2026-07-28T13:37:11.761Z
OutcomeID: "[[Outcome0062]]"
O_ResponseText:
O_AlternativeResponse:
O_ExperiencePoint:
O_QuestDataA:
O_QuestStatusA:
O_ResponseRelation:
O_QuestDataB:
O_QuestStatusB:
O_QuestDataC:
O_QuestStatusC:
O_QuestDataD:
O_QuestStatusD:
O_QuestDataE:
O_QuestStatusE:
---

```datacorejsx

return function TitleHeader() {

const file = dc.useCurrentFile();

if (!file) return null;

// file.$name contains the clean string of the note title

return <h1>{file.$name}</h1>; }

  

```

```datacorejsx

  

return function View() {

  

  const file = dc.useCurrentFile();

  

  if (!file) return <p>loading</p>;

  

  const KUMPULAN = file.$frontmatter;

  

  

  const items = Object.entries(KUMPULAN)

  

    .filter(([key]) => !key.startsWith("__"))

  

    .map(([key, field]) => `${key}: ${field?.value}`);

  

  

  return <dc.List rows={items} />;

  

}

  

```
