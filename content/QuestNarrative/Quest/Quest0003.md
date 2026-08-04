---
publish: true
created: 2026-07-27T12:55:51.328Z
modified: 2026-07-28T14:53:15.084Z
published: 2026-07-28T14:53:15.084Z
QuestID: "[[Quest0003]]"
Q_Name: Help The Self-Sufficient to build the Boat
Q_Description: Help The Self-Sufficient to build the big boat to sail to the Safe Place
QuestType: Main
Q_GoalType: Quest completion
Q_ConditionType:
IsTimeLimit:
TimeLimit:
QG_QuestID:
  - "[[Quest0009]]"
  - "[[Quest0010]]"
  - "[[Quest0011]]"
  - "[[Quest0012]]"
QG_ItemE_ID:
QG_ItemE_Amount:
QG_ItemD_ID: "[[GA_Propulsion]]"
QG_ItemD_Amount: "1"
QG_ItemC_ID: "[[GA_Decking]]"
QG_ItemC_Amount: "1"
QG_ItemB_ID: "[[GA_Frame]]"
QG_ItemB_Amount: "1"
QG_ItemA_ID: "[[GA_Bouyancy]]"
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
  - "[[Quest0009]]"
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
