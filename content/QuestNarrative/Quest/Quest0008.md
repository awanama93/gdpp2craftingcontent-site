---
publish: true
created: 2026-07-27T13:19:58.152Z
modified: 2026-07-28T14:53:15.500Z
published: 2026-07-28T14:53:15.500Z
QuestID: "[[Quest0008]]"
Q_Name: Help to build sanitary property with The Settler
Q_Description: We almost settled now. The last thing to do to settle in this rooftop island is making sanitary property
QuestType: Main
Q_GoalType: Item ownership
Q_ConditionType:
IsTimeLimit:
TimeLimit:
QG_QuestID:
QG_ItemE_ID:
QG_ItemE_Amount:
QG_ItemD_ID: "[[IN_ValveSeals]]"
QG_ItemD_Amount: "1"
QG_ItemC_ID: "[[IN_Filtration]]"
QG_ItemC_Amount: "1"
QG_ItemB_ID: "[[IN_PlumbingDrainage]]"
QG_ItemB_Amount: "1"
QG_ItemA_ID: "[[IN_LiquidBasin]]"
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
  - "[[Quest0002]]"
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
