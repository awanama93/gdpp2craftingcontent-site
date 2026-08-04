---
publish: true
created: 2026-07-27T12:45:35.533Z
modified: 2026-07-28T14:53:15.024Z
published: 2026-07-28T14:53:15.024Z
QuestType: Main
QuestID: "[[Quest0001]]"
Q_Name: Learn how the world works
Q_Description: Ask around to help you understand how this world works
Q_GoalType: Quest completion
Q_ConditionType: none
IsTimeLimit:
TimeLimit:
QG_QuestID:
  - "[[Quest0016]]"
  - "[[Quest0017]]"
  - "[[Quest0018]]"
  - "[[Quest0019]]"
  - "[[Quest0020]]"
  - "[[Quest0021]]"
  - "[[Quest0022]]"
  - "[[Quest0023]]"
QG_ItemE_ID:
QG_ItemE_Amount:
QG_ItemD_ID:
QG_ItemD_Amount:
QG_ItemC_ID:
QG_ItemC_Amount:
QG_ItemB_ID:
QG_ItemB_Amount:
QG_ItemA_ID:
QG_ItemA_Amount:
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
  - "[[Quest0002]]"
  - "[[Quest0003]]"
  - "[[Quest0004]]"
  - "[[Quest0023]]"
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
