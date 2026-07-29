---
publish: true
created: 2026-07-28T11:25:40.245+07:00
modified: 2026-07-29T18:03:08.673+07:00
published: 2026-07-29T18:03:08.673+07:00
ItemID:
ItemType: Lootable
I_BreakPoint:
I_StackSize:
I_Description:
I_SpawnedItem:
I_ProcessingStage: LootableBreakable
I_EffectA:
I_EffectA_Value:
I_EffectB:
I_EffectB_Value:
I_EffectC:
I_EffectC_Value:
I_LootableA: "[[IN_MetalPipe]]"
I_LootableA_DropChance:
I_LootableA_Quantity: "1"
I_LootableB: "[[IN_SyntacticFoam]]"
I_LootableB_DropChance:
I_LootableB_Quantity: "1"
I_LootableC: "[[IN_Gear]]"
I_LootableC_DropChance:
I_LootableC_Quantity: "1"
I_LootableD: "[[IN_MechanicalWheel]]"
I_LootableD_DropChance:
I_LootableD_Quantity: "1"
Cr_IngredientA:
Cr_IngredientAQuantity:
Cr_IngredientB:
Cr_IngredientBQuantity:
Cr_IngredientC:
Cr_IngredientCQuantity:
Cr_IngredientD:
Cr_IngredientDQuantity:
Cr_IngredientE:
Cr_IngredientEQuantity:
CraftingMethod: Non-craftable
I_LootableE: "[[IN_SteelSpring]]"
I_LootableE_DropChance:
I_LootableE_Quantity: "1"
I_LootableF:
I_LootableF_DropChance:
I_LootableF_Quantity:
I_LootableG:
I_LootableG_DropChance:
I_LootableG_Quantity:
I_LootableH:
I_LootableH_DropChance:
I_LootableH_Quantity:
I_IsIngredientOf:
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
