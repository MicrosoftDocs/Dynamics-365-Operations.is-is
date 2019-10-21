---
title: Yfirlit yfir verkflæðiskerfi
description: Þetta efnisatriði lýsir verkflæðiskerfinu.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190006"
---
# <a name="workflow-system-overview"></a>Yfirlit yfir verkflæðiskerfi

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir verkflæðiskerfinu.

## <a name="what-is-workflow"></a>Hvað er verkflæði?

Hugtakið *verkflæði* er hægt að skilgreina á tvo vegu: sem kerfi og sem viðskiptaferli.

### <a name="workflow-is-a-system"></a>Verkflæði er kerfi

Workflow er kerfi sem keyrir á Application Object Server (AOS). Verkflæðiskerfi veitir aðgerðir sem þú getur notað til að mynda einstakt verkflæði, eða viðskiptaferli.

### <a name="workflow-is-a-business-process"></a>Verkflæði er viðskiptaferli

Verkflæði endurspeglar viðskiptaferli. Það skilgreinir hvernig skjal flæðir eða hreyfist gegnum kerfið með því að sýna hver verður að ljúka verki, taka ákvörðun eða samþykkja skjal. Til dæmis sýnir eftirfarandi teikning verkflæði fyrir kostnaðarskýrslur.

![Verkflæði með einingum sem hefur verið úthlutað til notenda](./media/workflow_user.gif)

Til að skilja þetta verkflæði betur er gert ráð fyrir að Sam sendi kostnaðarskýrslu fyrir 7,000 USD. Í þessari lýsingu þarf Ivan að endurskoða kvittanirnar sem Sam sendi til hans. Síðan verða Frank og Sue að samþykkja kostnaðarskýrsluna. Gerum nú ráð fyrir að Sam sendi kostnaðarskýrslu fyrir 11.000. Í þessari lýsingu verður Ivan að endurskoða kvittanirnar og Frank, Sue og Ann að samþykkja kostnaðarskýrsluna.

## <a name="benefits-of-using-the-workflow-system"></a>Kostir við notkun Verkflæðiskerfisins

Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:

- **Samræmt ferli** — Hægt er að skilgreina hversu nákvæmlega skjöl, , eins og innkaupabeiðnir og kostnaðarskýrslur, skuli vera unnin. Með því að nota verkflæðiskerfi er gengið úr skugga um að skjölin eru unnin og samþykkt með samræmdum og skilvirkum hætti.
- **Sýnileiki ferlis** — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks. Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.
- **Miðlægur verkefnalisti** — Notendur geta skoðað miðlægan verkefnalista sem birtir verkflæðisverk og samþykktir sem tilheyra þeim.


## <a name="workflow-content"></a>Samhengi verkflæðis

+ [Uppbygging verkflæðis](workflow-system-architecture.md)
+ [Verkflæðiseiningar](workflow-elements.md)
+ [Verkflæðisaðgerðir](workflow-actions.md)
+ [Verkflæði stofnað](create-workflow.md)
+ [Skilgreining verkflæðiseiginleika](configure-workflow-properties.md)
+ [Skilgreina handvirkt verk í verkflæði](configure-manual-task-workflow.md)
+ [Skilgreina sjálfvirkt verki í verkflæði](configure-automated-task-workflow.md)
+ [Skilgreina samþykktarferli í verkflæði](configure-approval-process-workflow.md)
+ [Skilgreina samþykktarskref í verkflæði](configure-approval-step-workflow.md)
+ [Skilgreina handvirka ákvörðun í verkflæði](configure-manual-decision-workflow.md)
+ [Skilgreina skilyrta ákvörðun í verkflæði](configure-conditional-decision-workflow.md)
+ [Grunnstilla hliðstæðan verkþátt í verkflæði](configure-parallel-activity-workflow.md)
+ [Grunnstilla samhliða grein í verkflæði](configure-parallel-branch-workflow.md)
+ [Skilgreining verkflæðis línuatriðis](configure-line-item-workflow.md)
+ [Algengar spurningar um verkflæði](workflow-FAQ.md)
