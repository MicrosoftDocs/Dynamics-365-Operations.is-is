---
title: Setja upp og uppfæra viðskiptavinagátt
description: Þetta efnisatriði inniheldur upplýsingar um leyfi og uppsetningarleiðbeiningar fyrir viðskiptavinagáttina.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: fa95995320a0f81c040eeebe6fd796200fbff13f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255038"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Setja upp og uppfæra viðskiptavinagátt

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Leyfiskröfur

Til að innleiða viðskiptavinagáttina þarf að hafa eftirfarandi leyfi:

- **Power Apps gáttir** – Þetta leyfi þarf til að hýsa viðskiptavinagáttina. Gáttir fá leyfi samkvæmt notkun. Frekari upplýsingar er að finna í [Leyfiskröfur Power Apps-gátta](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Tvöföld skrif** - Nauðsynlegt er að hafa réttu leyfin til að virkja tvöföld skrif fyrir töflur Supply Chain Management. Frekari upplýsingar er að finna í [kerfiskröfur fyrir tvöföld skrif](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Tengsl í tvöföldum skrifum og Power Apps-gáttum

Viðskiptavinagáttin er háð Power Apps-gáttum og tvöföldum skrifum eins og sýnt er á eftirfarandi mynd.

![Tengsl viðskiptavinagáttar](media/customer-portal-elements.png "Tengsl viðskiptavinagáttar")

Ólíkt öðrum eiginleikum frá Supply Chain Management er sniðmát viðskiptavinagáttar að finna í Power Apps-gáttum. Þess vegna takmarkast viðskiptavinagáttin við virknina og möguleikana sem boðið er upp á af Power Apps-gáttum og töflunum í tvöföldum skrifum.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Nauðsynleg uppsetning til að virkja viðskiptavinagáttina

Eftir að gengið hefur verið úr skugga um að nauðsynleg leyfi séu til staðar, er hægt að setja upp tvöföld skrif eins og lýst er í [leiðbeiningum um fyrstu samstillingu tvöfaldra skrifa](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).

Ganga skal úr skugga um að virkja eftirfarandi töfluvarpanir í tvöföldum skrifum:

- Sölupöntunarhaus
- Upplýsingar um sölupöntun
- Lyklar
- Tengiliðir
- Afurðir

Þegar þessari uppsetningu er lokið er hægt að úthluta sniðmáti viðskiptavinagáttar.

## <a name="provision-the-customer-portal"></a>Úthluta viðskiptavinagátt

Áður en hafist er handa skal ganga úr skugga um að [nauðsynlegri uppsetningu](#required-setup) sé lokið. Síðan skal fylgja þessum skrefum til að úthluta viðskiptavinagáttinni.

1. Opnið [make.powerapps.com](https://make.powerapps.com/).
2. Gangið úr skugga um að notað sé umhverfið þar sem tvöföld skrif voru virkjuð.
3. Á flipanum **Stofna** skal fletta niður á hlutann **Byrja á sniðmáti** og velja sniðmátið sem heitir **Viðskiptavinagátt**.
4. Fylgdu leiðbeiningunum á skjánum.

Eftir að úthlutun er lokið er hægt að fá aðgang að viðskiptavinagáttinni í hlutanum **Forritin þín** á síðunni **Heim**.

> [!NOTE]
> Ef lausn tvöfaldra skrifa er ekki uppsett í umhverfinu sem unnið er í koma upp villuboð og viðskiptavinagáttinni verður ekki úthlutað.

## <a name="update-the-customer-portal"></a>Uppfæra viðskiptavinagáttina

Meiri virkni verður hugsanlega bætt við viðskiptavinagáttina síðar. Allar breytingar sem Microsoft gerir á undirliggjandi hlutum lausnar munu sjálfkrafa birtast í umhverfinu. Hins vegar mun vefsvæðið sem er úthlutað í umhverfinu ekki sjálfkrafa endurspegla breytingar sem eru gerðar á skilgreiningargögnunum. Bæta verður þessum breytingum við handvirkt með því að ná í kóða frá nýja sniðmátinu og sameina það við úthlutað vefsvæði.

## <a name="additional-resources"></a>Frekari upplýsingar

Til að komast að því hvernig á að setja upp og sérsníða viðskiptavinagáttina ætti að byrja á því að fara yfir eftirfarandi fylgiskjöl fyrir undirliggjandi tækni:

- [Power Apps fylgiskjöl gátta](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Tvískrifuð fylgiskjöl](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Til að stjórna gáttunum á áhrifaríkan hátt þarf að skilja gáttir Power Apps og stuðningstíma Microsoft Dataverse. Frekari upplýsingar er að finna í eftirfarandi tilföngum:

- [Um stuðningstíma gáttar](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Uppfæra gátt](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Flytja grunnstillingu gáttar](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Solution Lifecycle Management: Dynamics 365 fyrir forrit Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]