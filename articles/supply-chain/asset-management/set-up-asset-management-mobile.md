---
title: Nota fartækjavinnusvæði eignastýringar
description: Þessi grein lýsir því hvernig á að setja upp Microsoft Dynamics 365 Supply Chain Management og fjármála- og rekstrarforritið (Dynamics 365) til að keyra farsímavinnusvæði eignastýringar sem starfsmenn geta notað til að framkvæma eignastýringarverkefni.
author: johanhoffmann
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-22
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ef4e6bf2ae59adb05c7d4aacc3f5675a5adcafc9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070054"
---
# <a name="set-up-the-asset-management-mobile-workspace"></a>Nota fartækjavinnusvæði eignastýringar

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp Microsoft Dynamics 365 Supply Chain Management og fjármála- og rekstrarforritið (Dynamics 365) til að keyra **Eignastýring** færanlegt vinnusvæði sem starfsmenn geta notað til að framkvæma eignastýringarverkefni.

## <a name="set-up-maintenance-worker-users-in-supply-chain-management"></a>Setja upp notendur viðhaldsstarfskrafta í Supply Chain Management

Fyrir hvern notanda sem þarf aðgang að fartækjavinnusvæðinu **Eignastýring** skal fylgja þessum skrefum.

1. Í Supply Chain Management skal fara í **Human Resources \> Starfskraftar** og ganga úr skugga um skrá starfsmanns sé til fyrir notandann sem á að setja upp. Búið til nýja skrá starfsmanns eftir þörfum.
1. Farið í **Eignastýring \> Uppsetning \> Starfskraftar \> Starfskraftar** og gangið úr skugga um skrá starfsmanns sem gerð var grein fyrir (eða var stofnaður) í skrefinu á undan sé varpað í skrá viðhaldsstarfskrafts. Stofnið nýja skrá viðhaldsstarfskrafts eftir þörfum og stillið reitinn **Starfskraftur** á skrá starfsmanns úr fyrra skrefinu.
1. Farið í **Eignastýring \> Uppsetning \> Starfskraftar \> Hópar viðhaldsstarfskrafta** og gangið úr skugga um að skrá viðhaldsstarfskrafts sem gerð var grein fyrir (eða var stofnaður) í fyrra skrefi tilheyri hópi viðhaldsstarfskrafta.
1. Farið í **Kerfisstjórnun \> Notendur**.
1. Veljið viðeigandi notanda í hnitanetinu.
1. Í flýtiflipanum **Upplýsingar um notanda** skal stilla reitinn **Einstaklingur** á starfsmannareikninginn sem á að tengja við núverandi notandareikning. Þessi starfsmannareikningur ætti að vera starfsmannaskráin sem gerð var grein fyrir (eða stofnuð) í skrefi 1 og varpað í skrá viðhaldsstarfskrafts í skrefi 2.

> [!NOTE]
> Heimildir og öryggishlutverk notanda eiga við um eiginleika á fartækjavinnusvæðinu **Eignastýring** rétt eins og þau eiga við um eiginleika í notandaviðmóti Supply Chain Management. Þess vegna verður sérhver notandi sem settur er upp til að fá aðgang að fartækjavinnusvæðinu **Eignastýring** að vera með öryggishlutverkin sem þarf til að framkvæma svipaðar aðgerðir beint í Supply Chain Management.

## <a name="publish-the-asset-management-mobile-workspace"></a>Birta fartækjavinnusvæði eignastýringar

Til að gera eignastýringareiginleika aðgengilega í fjármála- og rekstrarforritinu (Dynamics 365) verður þú að birta **Eignastýring** færanlegt vinnusvæði.

1. Í Supply Chain Management skal velja hnappinn **Stillingar** (tannhjólið efst í hægra horninu) og síðan velja **Fartækjaforrit** í valmyndinni.
1. Í svarglugganum **Stjórna fartækjaforriti** skal finna reitinn **Eignastýring**. Ef hann inniheldur textann „Í lýsigögnum - ekki birt“ hefur vinnusvæðið ekki enn verið birt. Ef hann inniheldur textann „Í lýsigögnum - birt“ hefur vinnusvæðið þegar verið birt og hægt er að sleppa því sem eftir er af þessu ferli.

    ![Svarglugginn Stjórna fartækjaforriti.](media/mobile-workspaces.png "Stjórna svarglugga fyrir farsímaforrit")

1. Velja skal reitinn **Eignastýring** og síðan velja **Birta** í tækjastikunni. Eftir nokkrar sekúndur ætti að berast tilkynning sem segir til um að vinnusvæði hafi verið birt. Þar að auki ætti textinn í reitnum að breytast í „Í lýsigögnum - birt.“

## <a name="install-and-set-up-the-finance-and-operations-dynamics-365-mobile-app"></a>Settu upp og settu upp fjármála- og rekstrarforritið (Dynamics 365).

1. Farðu í eina af eftirfarandi forritabúðum til að setja upp **Microsoft fjármál og rekstur (Dynamics 365)** app á farsímanum þínum:

    - [Fyrir Google Android-tæki](https://go.microsoft.com/fwlink/?linkid=850662)
    - [Fyrir Apple iOS-tæki](https://go.microsoft.com/fwlink/?linkid=850663)

1. Opnaðu fjármála- og rekstrarappið (Dynamics 365). Innskráningarsíðan ætti að birtast. Í reitinn **Innskráning** skal færa inn vefslóð Supply Chain Management eða velja nýlega vefslóð úr listanum **Nýleg umhverfi** og síðan pikka á **Tengja**.

    ![Innskráningarsíða.](media/mobile-app-sign-in.png "Innskráningarsíða")

1. Ef notandi er beðinn um að staðfesta tenginguna skal velja gátreitinn **Ég skil** og síðan flipann **Tengja**.
1. Á síðunni **Velja reikning** skal nota Microsoft-reikninginn til að skrá sig inn í farsímaforritið.

    Síðan **Vinnusvæði** birtist. Hún sýnir öll fartækjavinnusvæði sem hafa verið gefin út af tilviki Supply Chain Management.

    ![Listi vinnusvæða.](media/mobile-app-workspaces.png "Listi vinnusvæða")

1. Ef breyta þarf lögaðilanum (fyrirtækinu) skal pikka á valmyndarhnappinn (stundum kallaður hamborgarinn eða hamborgarahnappurinn) efst í vinstra horninu og síðan pikka á **Breyta fyrirtæki**.

    ![Breyting lögaðila.](media/mobile-app-change-comp.png "Breying lögaðila")

1. Á síðunni **Vinnusvæði** skal velja vinnusvæðið sem ætlunin er að vinna með til að opna það.

    ![Fartækjavinnusvæði eignastýringar.](media/mobile-app-asset-workspace.png "Fartækjavinnusvæði eignastýringar")

## <a name="work-with-the-asset-management-mobile-workspace"></a>Vinna með fartækjavinnusvæði eignastýringar

Frekari upplýsingar um hvernig á að vinna með fartækjavinnusvæðið **Eignastýring** er að finna í [Nota fartækjavinnusvæði eignastýringar](asset-management-mobile-workspace.md).

Fyrir frekari upplýsingar um fjármál og rekstur (Dynamics 365) farsímaforritið, sjáðu [Heimasíða farsímaforrits](../../fin-ops-core/dev-itpro/mobile-apps/Mobile-app-home-page.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
