---
title: Setja upp stigveldi fyrirtækis
description: Þetta efnisatriði lýsir hvernig á að setja upp stigveldi fyrirtækis í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 4238d1aa277bf2f1df30825ef20dbf3095d13ebc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800568"
---
# <a name="set-up-organization-hierarchies"></a>Setja upp stigveldi fyrirtækis

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að setja upp stigveldi fyrirtækis í Microsoft Dynamics 365 Commerce.

Áður en þú býrð til rásir þarftu að tryggja að stigveldi fyrirtækis hafi verið sett upp.

Hægt er að nota stigveldi fyrirtækis til að skoða og gefa skýrslu um reksturinn frá ýmsum sjónarhornum. Til dæmis er hægt að setja upp eitt stigveldi fyrir skattalega-, lagalega- eða lögboðna skýrslugerð. Hægt að setja upp annað stigveldi til að gefa skýrslu um fjárhagslegar upplýsingar sem ekki er krafist samkvæmt lögum, en sem er notuð við innri skýrslugerð.

Áður en hægt er að stofna stigveldi fyrirtækis þarf að stofna fyrirtæki. Nánari upplýsingar er að finna í [Stofna lögaðila](channels-legal-entities.md) eða [Stofna rekstrareiningar](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json).


Frekari upplýsingar er hægt að finna í eftirfarandi efni.
- [Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
- [Skipuleggja stigveldi fyrirtækis](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)
- [Stofna fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/tasks/create-organization-hierarchy.md?toc=/dynamics365/commerce/toc.json)

## <a name="create-an-organizational-hierarchy"></a>Búa til stigveldi fyrirtækis

Til að stofna stigveldi fyrirtækis skaltu fylgja þessum skrefum.

1. Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Stigveldi fyrirtækis**.
1. Í aðgerðaglugganum velurðu **Nýtt**.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Í kaflanum **Tilgangur** skal velja **Úthluta tilgangi**.
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Veljið tilgangur sem úthluta á stigveldi fyrirtækisins.
1. Í kaflanum **Úthlutuð stigveldi** skal velja **Bæta við**.
1. Í listanum skal merkja valda línu. Finna stigveldið sem var verið að stofna.
1. Veljið **Í lagi**.

Eftirfarandi mynd sýnir dæmi um skipulag stigveldis sem er búið til fyrir upphugsaðar verslanir „Adventure Works“.

![Dæmi um stigveldi fyrirtækis](media/organizational-hierarchies.png)

### <a name="add-organizations-to-a-hierarchy"></a>Bæta við fyrirtækjum í stigveldi

Til að bæta fyrirtækjum við í stigveldi skaltu fylgja þessum skrefum.

1. Í listanum skal finna og velja þá skráningu sem óskað er eftir. Velja skal þitt stigveldi.
1. Í aðgerðaglugganum velurðu **Skoða**.
1. Bæta við fleiri fyrirtæki eftir þörfum.
1. Til að bæta fyrirtæki við velurðu **Breyta** og velur síðan **Setja inn**. Þegar gerðar eru breytingar er hægt drög að vista og birta breytingarnar.

Eftirfarandi mynd sýnir lögaðila sem er bætt við stigveldisrótina með fjórum kostnaðarmiðstöðvum bætt við fyrir „verslunarmiðstöð“, „sölustöð“, „net“ og „símaþjónustuver“. Síðan er hægt að bæta við ýmsum smásölu-, síma- og netrásum.

![Dæmi um hönnuð stigveldis](media/hierarchy-designer.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir fyrirtæki og fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[Skipuleggja fyrirtækjastigveldi](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[Stofna lögaðila](channels-legal-entities.md)

[Stofna rekstrareiningar](../fin-ops-core/fin-ops/organization-administration/tasks/create-operating-unit.md?toc=/dynamics365/commerce/toc.json)

[Yfirlit yfir rásir](channels-overview.md)

[Skilyrði fyrir rásauppsetningu](channels-prerequisites.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
