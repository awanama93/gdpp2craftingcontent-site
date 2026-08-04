---
publish: true
created: 2026-07-27T12:51:42.003Z
modified: 2026-07-28T14:53:15.257Z
published: 2026-07-28T14:53:15.257Z
QuestID: "[[Quest0002]]"
Q_Name: Help The Settler to build more permanent shelter
Q_Description: Help The Settler Head to build various things to help them settling
QuestType: Main
Q_GoalType: Quest completion
Q_ConditionType:
IsTimeLimit:
TimeLimit:
QG_QuestID:
  - "[[Quest0005]]"
  - "[[Quest0006]]"
  - "[[Quest0007]]"
  - "[[Quest0008]]"
QG_ItemE_ID:
QG_ItemE_Amount:
QG_ItemD_ID: "[[GA_Campfire]]"
QG_ItemD_Amount: "1"
QG_ItemC_ID: "[[GA_Sanitary]]"
QG_ItemC_Amount: "1"
QG_ItemB_ID: "[[GA_Roofing]]"
QG_ItemB_Amount: "1"
QG_ItemA_ID: "[[GA_Lighting]]"
QG_ItemA_Amount: "1"
QG_DialogueID:
QG_ConvictionType:
QG_ConvictionCharacter:
QG_ConvictionAmount:
QG_ClosenessNPC:
QG_ClosenessAmount:
QC_Time:
QC_ItemE_ID:
QC_ItemE_Amount:
QC_ItemD_ID:
QC_ItemD_Amount:
QC_ItemC_ID:
QC_ItemC_Amount:
QC_ItemB_ID:
QC_ItemB_Amount:
QC_ItemA_ID:
QC_ItemA_Amount:
QC_DialogueID:
QC_ConvictionType:
QC_ConvictionCharacter:
QC_ConvictionAmount:
QC_ClosenessNPC:
QC_ClosenessAmount:
canvas:
  - "[[QuestMapping.canvas]]"
QuestMapping:
  - "[[Quest0005]]"
Q_GoalActionType:
Q_GoalActionTargetObject:
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
