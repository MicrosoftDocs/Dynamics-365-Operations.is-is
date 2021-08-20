---
title: Frestun á úrvinnslu handvirkrar birgðahreyfingar
description: Í þessu efnisatriði er lýst hvernig eigi að nota frestaða úrvinnslu handvirkrar birgðahreyfingar í Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
ms.date: 04/27/2021
ms.topic: article
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: Mirzaab
ms.search.validFrom: 2021-04-27
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: a15c913c876e961c6824c1e8812ab2be2d6ffa4333cd0d4e6f80cae8bac79394
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746748"
---
# <a name="deferred-processing-of-manual-inventory-movement"></a>Frestun á úrvinnslu handvirkrar birgðahreyfingar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig eigi að nota frestaða úrvinnslu handvirkrar birgðahreyfingar í Microsoft Dynamics 365 Supply Chain Management.

Frestuð úrvinnsla gerir starfsmönnum vöruhúss kleift að sinna annarri vinnu á meðan unnið er úr frágangsaðgerð í bakgrunni. Frestuð úrvinnsla er gagnleg þegar netþjónninn getur verið með tilfallandi eða ófyrirséða aukningu í vinnslutíma og slík aukning á vinnslutíma getur haft áhrif á afköst notanda. Vinnugerðin *Birgðahreyfing* hefur nú verið bætt við safn vinnugerða sem þessi eiginleiki styður.

Bakgrunnsvinnsla er gerð með [Vinna úr viðburðum vöruhúsaforrits](warehouse-app-events.md).

## <a name="turn-on-this-feature-for-your-system"></a>Kveikja á þessum eiginleika fyrir kerfið

Til að gera þennan eiginleika tiltækan skal kveikja á eftirfarandi eiginleikum í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md): Þú verður að kveikja á þeim í þessari röð:

1. Vinnulokun fyrir allt fyrirtækið
1. Vinna úr viðburðum vöruhúsaforrits
1. Frestuð frágangsaðgerð
1. Frestun á úrvinnslu handvirkrar aðgerðar birgðahreyfingar

## <a name="configure-the-work-processing-policies"></a>Skilgreina stefnur vinnuferla

Til að nota frestaða úrvinnslu þarf að setja upp og nota stefnu vinnuferla. Fyrir frestaðar úrvinnslu frágangs styður [Eiginleika fyrir frestaða úrvinnslu vöruhúsavinnu](deferred-put.md) eftirfarandi vinnugerðir: *Sölupöntun*, *Útgáfa flutningspöntunar* og *Áfylling*. Eiginleikarnir *Frestun á úrvinnslu handvirkrar aðgerðar birgðahreyfingar* bætir við nýrri vinnugerð: *Birgðahreyfing*.

Til að setja upp vinnslustefnu skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Stefnur vinnuferla**.
1. Veljið annaðhvort fyrirliggjandi stefnu í listanum eða stofnið nýja stefnu með því að velja **Nýtt** á aðgerðasvæðinu. Eftirfarandi reitir eru í hausnum á hverri stefnu:

    - **Heiti stefnu vinnslu** – Heiti vinnslustefnunnar.
    - **Lýsing:** Lýsing á stefnunni.

1. Í flýtiflipanum **Úrvinnslureglur** skal setja upp safn af reglum sem stefnan á við um. Notaðu hnappana á tækjastikunni til að bæta við eða fjarlægja reglur eftir þörfum. Fyrir hverja reglu skal stilla eftirfarandi reiti:

    - **Gerð vinnupöntunar** – Veljið vinnutegund sem stefnan á við um.
    - **Aðgerð** – Veljið aðgerðina sem stefnan er notuð til að vinna úr. Ef þú valdir *Birgðahreyfingu* í reitnum **Gerðir vinnupöntunar** þarftu ekki að stilla þennan reit vegna þess að unnið er úr bæði tiltektar- og frágangsaðgerðum sem eitt tilvik.
    - **Aðferð vinnuferlisins** – Veljið aðferðina sem er notuð til að vinna vinnulínuna. Ef þú velur *Strax* líkist hegðunin hegðuninni þegar engar vinnslureglur eru notaðar til að vinna úr línunni. Ef valið er *Frestað* mun kerfið nota frestaða úrvinnslu sem notar runurammann.
    - **Þröskuldur fyrir frestað ferli** – Ef þú stillir þennan reit á *0* (núll) er enginn þröskuldur. Í því tilviki er úrvinnsluaðferðin *Frestað* notuð ef mögulegt er. Ef tiltekin útreikningur á mörkum er undir mörkunum verður *Strax* aðferðin notuð. Annars er aðferðin *Frestað* notuð ef mögulegt er. Fyrir sölu og flutningstengda vinnu er þröskuldurinn reiknaður sem fjöldi tilheyrandi upphleðslulína sem eru í vinnslu vegna verksins. Fyrir endurnýjunarvinnu er þröskuldurinn reiknaður sem fjöldi vinnulína sem verið er að endurnýja af verkinu. Með því að setja mörk upp á t.d. *5* fyrir sölu tryggir þú að minni verk sem eru með færri en fimm hleðslulínum í upphafi muni ekki nota frestaða úrvinnslu, en stærri verk munu nota hana. Þessi þröskuldur hefur aðeins áhrif ef reiturinn **Aðferð vinnuferlisins** er stilltur á *Frestað*.
    - **Frestun vinnslu á runuhóp** – Tilgreinið runuflokkinn sem er notaður til vinnslu. Ef valið var *Birgðahreyfing* í reitnum **Gerð vinnupöntunar** þarf ekki að stilla þennan reit vegna þess að runuflokkurinn er valinn í svarglugganum **Vinna úr viðburðum vöruhúsaforrits**.

## <a name="assign-the-work-creation-policy"></a>Úthluta við stofnferli vinnu

Nánari upplýsingar um hvernig á að úthluta stefnu við stofnun vinnu er að finna í [Frestuð vinnsla vöruhúsavinnu](deferred-put.md).

## <a name="set-up-a-batch-job-to-process-warehouse-app-events"></a>Setja upp runuvinnslu til að vinna úr viðburðum vöruhúsaforrits

Til að nota *Frestun á úrvinnslu handvirkrar aðgerðar birgðahreyfingar* þarf að setja upp áætlað lotuvinnu.

1. Farið í **Vöruhúsakerfi \> Reglubundin verk \> Vinna úr viðburðum vöruhúsaforrits**.
1. Í svarglugganum **Vinna úr viðburðum vöruhúsaforrits**, í flýtiflipanum **Keyra í bakgrunni**, skal stilla valkostinn **Runuvinnsla** á *Já*.
1. Veljið **Endurtekning** og setjið upp keyrsluáætlun sem uppfyllir kröfur rekstursins.
1. Veljið **Í lagi** í hverjum svarglugga.

## <a name="inquire-about-the-warehouse-app-events"></a>Spyrjast fyrir um tilvik vöruhúsaforrits

Hægt er að skoða viðburðaröðina og viðburðaskilaboðin sem vöruhúsaforritið býr til með því að fara í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Kladdar fartækis \> Viðburðir vöruhúsaforrits**.

Skilaboðin *Birgðahreyfing* hafa stöðuna *Í biðröð* þegar þau eru fyrst búin til. Þessi staða gefur til kynna að runuvinnslan **Vinna úr viðburðum vöruhúsaforrits** muni sækja viðburðarskilaboðin og vinna úr þeim. Þegar staðan er uppfærð í *Lokið*, er öllum tengdum tilvikum eytt úr biðröðinni.

Öllum viðburðum *Birgðahreyfingar* er safnað saman undir eitt safn á hverja viðburðargerð og vöruhús.

Runuvinnslan mun vinna úr viðburðum vöruhúsaforritsins samkvæmt endurtekningunni sem er sett upp í svarglugganum **Vinna úr viðburðum vöruhúsaforrits**. Þar til skilaboð eru unnin er því hægt að finna kenni vöruhússins með því að skoða reitinn **Kenni**.

Upplýsingar í skilaboðunum innihalda upplýsingar um hreyfinguna (til dæmis staðsetningarnar „frá“ og „til“).

Frekari upplýsingar er að finna í [Úrvinnsla á tilviki vöruhúsaforrits](warehouse-app-events.md).

## <a name="configure-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Stilla valmynd fartækisins til að sleppa reglu um frestaða úrvinnslu

Nánari upplýsingar um hvernig skilgreina á valmynd fartækisins til að sleppa reglum um frestaða úrvinnslu er að finna í [Frestuð vinnsla vöruhúsavinnu](deferred-put.md).

## <a name="impact-on-closed-work-dates"></a>Áhrif á lokaða vinnudaga

Upplýsingar um áhrif á lokaðar vinnudagsetningar er að finna í [Frestuð vinnsla vöruhúsavinnu](deferred-put.md).

## <a name="additional-resources"></a>Frekari upplýsingar

- [Frestuð vinnsla vöruhúsavinnu](deferred-put.md)
- [Vinnsla viðburða í vöruhúsaforriti](warehouse-app-events.md)
- [Uppsetning fartækja fyrir vöruhúsavinnu](configure-mobile-devices-warehouse.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
