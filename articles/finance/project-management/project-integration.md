---
title: Microsoft Project biðlarasamþætting
description: Skipuleggja og vinna með verkáætlun getur verið flókið, þannig að verkefnastjórar þurfa að nota verkfæri sem hjálpa þeim að stjórna þessu verki. Samþætting við Microsoft Project Client veitir stuðning til að opna og stjórna sundurliðun verkþátta í verki.
author: KimANelson
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 610990612d5fb38025bf39cc648d0c9572da37b6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174897"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project biðlarasamþætting

[!include [banner](../includes/banner.md)]

Skipuleggja og vinna með verkáætlun getur verið flókið, þannig að verkefnastjórar þurfa að nota verkfæri sem hjálpa þeim að stjórna þessu verki. Samþætting við Microsoft Project Client veitir stuðning til að opna og stjórna sundurliðun verkþátta í verki. Verkefnastjórinn getur birt allar breytingar aftur í Dynamics 365 Finance sundurliðun verkþátta í verki.

> [!NOTE]
> Ef þú notar uppfærslu frá júlí (útgáfu 10.0.4), verður þú að setja upp KB 4054797 og 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Stilltu viðbótina fyrir Microsoft Project Client
Til að virkja samþættingu við Microsoft Project Client er nauðsynlegt að Microsoft Dynamics 365 viðbót sé sett upp á Microsoft Project forriti biðlara notandans. Þetta er gert með því að opna **Vinnusvæði verkefnastjórnunar**.

• Smelltu á **Stilla verkefnisviðbót biðlara** frá **Tenglar** > **Uppsetningar** hluta vinnusvæðisins.

• Smelltu á **Opna**, smelltu síðan á **Keyra** þegar beðið er um það.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Opnaðu og breyttu núverandi drögum að sundurliðun verkþátta í Microsoft Project Client
Ef verk í Dynamics 365 Finance hefur nú þegar stofnað sundurliðun verkþátta, þá er hægt að opna sundurliðun verkþátta í Microsoft Project Client forritinu ef sundurliðun verkþátta er enn í drögum. Til að opna frá **Verk** síðunni smellirðu á **Opna í Microsoft Project** tengil í **Áætlunar** flipanum. Þessi síða er einnig hægt að opna innan Microsoft Project Client forritinu með því að smella á **Opna** í **Microsoft Dynamics 365** flipanum. Veldu **Lögaðilar** og **Verk** úr listanum.

> [!NOTE]
> Ef þú notar Internet Explorer sem vafra þarftu að smella á **Vista** til að opna handvirkt frá staðsetningu sem skráin er sótt til. Eða smelltu á **Vista og opna** til að opna skrána í Microsoft Project Client. Ekki endurnefna skráarheiti þegar þú vistar.

Áður en þú gerir breytingar á skránni með Microsoft Project Client þarftu að athuga hana. Smelltu á **Skrá út** á flipanum **Microsoft Dynamics 365**. Þetta kemur í veg fyrir að aðrir notendur geti breytt sundurliðun verkþátta innan Finance á sama tíma. Til að birta sundurliðun verkþátta eftir að breytingar hafa verið gerðar skaltu smella á **Skoða í** á **Microsoft Dynamics 365** flipanum.

Ef verkhópi hefur þegar verið bætt við verkið í Finance mun tilfangalistinn innihalda hópmeðlimi. Ef verkhópur hefur ekki enn verið bætt við verkið geturðu valið tilföng og búið til hópinn í Microsoft Project Client með því að smella á hnappinn **Tilföng** á **Microsoft Dynamics 365** flipanum. 

Eftirfarandi gögn verða samstillt aftur til Finance sem hluti af innskráningarferlinu:

• Verkheiti

• Upphafsdagsetning

• Lokadagsetning

• Forverar

• Heiti tilfanga

• Flokkur

• Tilfangaflokkur

• Vinnutími

• Athugasemdir

• Forgangur

> [!NOTE]
> Ef þú bætir við öðrum dálkum við Microsoft Project Client skrána þína, þá verða þær ekki vistaðar í skránni og birtast ekki þegar skráin er opnuð aftur.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Stofnaðu sundurliðun verkþátta fyrir núverandi verk með Microsoft Project Client
Til að stofna nýja sundurliðun verkþátta með Microsoft Project Client skaltu fylgja þessum skrefum:


1.  Opnaðu Microsoft Project Client.

2.  Á **Microsoft Dynamics 365** flipanum skaltu smella á **Opna**.

3.  Veldu **lögaðila** fyrir verkið.

4.  Veldu **Verk**.

5.  Smelltu á **Útritun** á **Microsoft Dynamics 365** flipanum.

6.  Þegar þú ert tilbúin til að birta á Finance, smelltu á **Innritun** á flipanum **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Skiptu um núverandi sundurliðun verkþátta fyrir núverandi verk með Microsoft Project Client
Til að stofna nýja sundurliðun verkþátta með Microsoft Project Client og skipta um núverandi sundurliðun verkþátta fyrir núverandi verk skaltu fylgja þessum skrefum:

1.  Opnaðu Microsoft Project Client.

2.  Stofnaðu áætlunina í Microsoft Project Client.

3.  Á **Microsoft Dynamics 365** flipanum, smelltu á **Vista breytingar** > **Skipta út núverandi verki**.

4.  Veldu **lögaðila** fyrir verkið.

5.  Veldu **Verk**.

6.  Smellið á **Í lagi**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Stofnaðu nýtt verk innan Microsoft Project Client


1.  Opnaðu Microsoft Project Client.

2.  Stofnaðu áætlunina í Microsoft Project Client.

3.  Á **Microsoft Dynamics 365** flipanum skaltu smella á **Vista breytingar** > **Vista sem nýtt verk**.

4.  Veldu **lögaðila** fyrir verkið.

5.  Sláðu inn **kenni verks** ef þörf krefur.

6.  Sláðu inn **Verkheiti**.

7.  Veldu **Gerð verks**, **Verkhóp** og **Kenni verksamnings**. Einnig getur þú búið til nýjan verksamning með því að smella á **Nýr**.

8.  Veldu **Dagatalið** fyrir tilföng.

11. Smellið á **Í lagi**.
