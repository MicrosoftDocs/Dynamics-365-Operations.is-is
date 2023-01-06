---
title: Yfirlit yfir verkflæðiskerfi
description: Þessi grein lýsir verkflæðikerfi.
author: ChrisGarty
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "56381"
- intro-internal
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13dd4335a8b939a44ea7176a90f660999c32a83a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863189"
---
# <a name="workflow-system-overview"></a>Yfirlit yfir verkflæðiskerfi

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Þessi grein lýsir verkflæðikerfi.

## <a name="what-is-workflow"></a>Hvað er verkflæði?

Hugtakið *verkflæði* er hægt að skilgreina á tvo vegu: sem kerfi og sem viðskiptaferli.

### <a name="workflow-is-a-system"></a>Verkflæði er kerfi

Workflow er kerfi sem keyrir á Application Object Server (AOS). Verkflæðiskerfi veitir aðgerðir sem þú getur notað til að mynda einstakt verkflæði, eða viðskiptaferli.

### <a name="workflow-is-a-business-process"></a>Verkflæði er viðskiptaferli

Verkflæði endurspeglar viðskiptaferli. Það skilgreinir hvernig skjal flæðir eða hreyfist gegnum kerfið með því að sýna hver verður að ljúka verki, taka ákvörðun eða samþykkja skjal. Til dæmis sýnir eftirfarandi teikning verkflæði fyrir kostnaðarskýrslur.

![Verkflæði með einingum sem hefur verið úthlutað til notenda.](./media/workflow_user.gif)

Til að skilja þetta verkflæði betur er gert ráð fyrir að Sam sendi kostnaðarskýrslu fyrir 7,000 USD. Í þessari lýsingu þarf Ivan að endurskoða kvittanirnar sem Sam sendi til hans. Síðan verða Frank og Sue að samþykkja kostnaðarskýrsluna. Gerum nú ráð fyrir að Sam sendi kostnaðarskýrslu fyrir 11.000. Í þessari lýsingu verður Ivan að endurskoða kvittanirnar og Frank, Sue og Ann að samþykkja kostnaðarskýrsluna.

## <a name="benefits-of-using-the-workflow-system"></a>Kostir við notkun Verkflæðiskerfisins

Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:

- **Samræmt ferli** — Hægt er að skilgreina hversu nákvæmlega skjöl, , eins og innkaupabeiðnir og kostnaðarskýrslur, skuli vera unnin. Með því að nota verkflæðiskerfi er gengið úr skugga um að skjölin eru unnin og samþykkt með samræmdum og skilvirkum hætti.
- **Sýnileiki ferlis** — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks. Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.
- **Miðlægur verkefnalisti** — Notendur geta skoðað miðlægan verkefnalista sem birtir verkflæðisverk og samþykktir sem tilheyra þeim.


## <a name="workflow-content"></a>Samhengi verkflæðis

+ [Kerfisskipulag verkflæðis](workflow-system-architecture.md)
+ [Verkflæðiseiningar](workflow-elements.md)
+ [Verkþættir í samþykktarferli verkflæðis](workflow-actions.md)
+ [Yfirlit yfir stofnun verkflæðis](create-workflow.md)
+ [Skilgreining verkflæðiseiginleika](configure-workflow-properties.md)
+ [Skilgreina handvirk verk í verkflæði](configure-manual-task-workflow.md)
+ [Skilgreina sjálfvirk verk í verkflæði](configure-automated-task-workflow.md)
+ [Grunnstilla samþykktarferli í verkflæði](configure-approval-process-workflow.md)
+ [Grunnstilla samþykktarskref í verkflæði](configure-approval-step-workflow.md)
+ [Skilgreina handvirkar ákvarðanir í verkflæði](configure-manual-decision-workflow.md)
+ [Skilgreina skilyrtar ákvöarðanir í verkflæði](configure-conditional-decision-workflow.md)
+ [Skilgreina hliðstæða verkþætti í verkflæði](configure-parallel-activity-workflow.md)
+ [Skilgreina samhliða greinar í verkflæði](configure-parallel-branch-workflow.md)
+ [Skilgreina verkflæði línuatriða](configure-line-item-workflow.md)
+ [Algengar spurningar um verkflæði](workflow-FAQ.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]