---
title: Sérstilla tölvupósta vegna færslna eftir afhendingarmáta
description: Þessi grein lýsir því hvernig á að setja upp sérsniðin tölvupóstsniðmát fyrir sérstakar tilkynningagerðir og afhendingarmáta í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.16
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 0c0bd218c10a373d142ddcc7780c5339569f7a07
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275705"
---
# <a name="customize-transactional-emails-by-mode-of-delivery"></a>Sérstilla tölvupósta vegna færslna eftir afhendingarmáta

[!include [banner](includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp sérsniðin tölvupóstsniðmát fyrir sérstakar tilkynningagerðir og afhendingarmáta í Microsoft Dynamics 365 Commerce.

Nú er hægt að sérstilla tölvupóst færslna fyrir samsetningu tilkynningagerðar (til dæmis, **Pöntun stofnuð**, **Pöntun pakkað** eða **Pöntun reikningsfærð**) og afhendingarmáta (til dæmis yfir nótt, sótt í verslun eða sótt fyrir utan verslun). Sérsniðinn tölvupóstur færslna gerir söluaðilum kleift að leyfa viðskiptavinum sínum að panta með afgreiðsluupplifun sem er sérsniðin að afhendingarmáta pöntunarinnar. Hægt er t.d. að sérsníða tilvikið „pöntun pakkað“ til að veita leiðbeiningar um afhendingu fyrir utan verslun fyrir viðskiptavini sem velja að sækja fyrir utan verslun. Einnig getur tilvikið veitt upplýsingar um farmflytjanda og afhendingarupplýsingar fyrir viðskiptavini sem velja að fá pöntunina sína senda.

> [!NOTE]
> Til að nota virkni fyrir sérstilltan tölvupóst fyrir færslur verður fyrst að kveikja á **Sérsniðin sniðmát fyrir tölvupóst færslna** með því að opna **Vinnusvæði \> Eiginleikastjórnun** í Commerce Headquarters.

Hægt er að sérsníða tölvupóst eftir afhendingarmáta fyrir eftirfarandi tilkynningagerðir:

- **Afturköllun pöntunar** – Þessi tilkynning með tölvupósti er ný af nálinni.
- **Pöntun búin til**
- **Pöntun staðfest**
- **Pöntun reikningsfærð** – Þessi tilkynning með tölvupósti er ný af nálinni. Hægt er að nota hana í staðinn fyrir tilkynningargerðina **Pöntun send** sem sendir tilkynningu vegna allra reikningsatvika afhendingarmátann sent (ekki sótt, borið út né afhent rafrænt).
- **Pöntun tekin til**
- **Pöntun pakkað**
- **Pöntun tilbúin til afhendingar** – Aðeins er hægt að sérsníða þessa tilkynningagerð eftir afhendingarmáta ef kveikt er á eiginleikanum **Stuðningur fyrir margar afhendingarmáta**. Í slíku tilviki hefur þessi tilkynningargerð svipaða virkni og tilkynningargerðin **Pöntun pakkað**.
- **Greiðsla mistókst**
- **Skiptipöntun stofnuð**

## <a name="configure-email-templates-for-specific-modes-of-delivery"></a>Skilgreina sniðmát fyrir tölvupóst fyrir tiltekna afhendingarmáta

Þegar þetta ferli fer fram er gert ráð fyrir því að þú hafir þegar stofnað ný, sérsniðin sniðmát fyrir tölvupóst og bætt þeim við síðuna **Sniðmát fyrir tölvupóst fyrirtækis**. Frekari upplýsingar um hvernig á að búa til og hlaða upp sniðmátum fyrir tölvupóst er að finna í [Stofna sniðmát fyrir tölvupóst fyrir færslutilvik](email-templates-transactions.md).

Fylgdu eftirfarandi skrefum til að skilgreina sniðmát fyrir tölvupóst fyrir tiltekna afhendingarmáta í Commerce Headquarters.

1. Opnaðu **Forstilling tilkynningar í tölvupósti fyrir Commerce**.
1. Fyrir neðan **Tilkynningastillingar smásölutilvika** skaltu velja núverandi tilkynningargerð.
1. Á meðan tilkynningagerð er enn valin skal velja **Skilgreina afhendingarmáta**.
1. Í svarglugganum **Afhendingarmátar** skal velja **Nýtt**.
1. Í nýju línunni í svæðinu **Afhendingarmáti** skal velja afhendingarmáta.
1. Í svæðinu **Kenni tölvupósts** skal velja sniðmát fyrir tölvupóst sem skal varpa á afhendingarmátann.
1. Velja skal gátreitinn **Virkt** .
1. Endurtakið skref 4 til 7 til að bæta við fleiri afhendingarmátum.
1. Þegar þessu er lokið skal velja **Í lagi**.

> [!NOTE]
> - Þegar fleiri en einn afhendingarmáti er til staðar á milli lína í sölupöntun verður sjálfgefið sniðmát notað. Sjálfgefið sniðmát er sniðmátið sem er varpað er á tilkynningagerðina á síðunni **Forstilling tilkynningar í tölvupósti fyrir Commerce**.
> - Þegar sölupöntun er með afhendingarmáta sem hefur ekki verið skilgreindur fyrir sérsniðið sniðmát fyrir tölvupóst, verður sjálfgefna sniðmátið fyrir tölvupóst notað.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stofna símaverspantanir](tasks/create-call-center-orders.md)

[Breyta afhendingarmáta á sölustað](pos-change-delivery-mode.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
