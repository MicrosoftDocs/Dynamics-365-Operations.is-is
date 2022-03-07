---
title: Virkja breytingastjórnun á fyrirliggjandi afurðum
description: Þetta efnisatriði útskýrir hvernig hægt er að virkja breytingastjórnun fyrir fyrirliggjandi afurðir. Það lýsir einnig tilvikum þar sem geta notanda til að virkja breytingastjórnun er takmarkaður.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: f0fba0a9234e5b7cb055f7b97578bff72f1d06ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571978"
---
# <a name="enable-change-management-on-existing-products"></a>Virkja breytingastjórnun á fyrirliggjandi afurðum

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig hægt er að virkja breytingastjórnun fyrir fyrirliggjandi afurðir. Það lýsir einnig tilvikum þar sem geta notanda til að virkja breytingastjórnun er takmarkaður.

Þegar breytingastjórnun er virkjuð fyrir fyrirliggjandi afurð er hægt að búa til útgáfur af þeirri afurð og rekja breytingar sem gerðar eru á henni í gegnum líftíma hennar. Þar af leiðandi er hægt að rekja þær breytingar með því að nota breytingabeiðnir. Til að virkja breytingastjórnun þarf að breyta viðeigandi afurðum í *hönnunarvörur* (einnig þekkt sem hönnunarafurðir). Hönnunarafurðir eru afurðir sem úthlutað er útgáfu og stjórnað í gegnum breytingastjórnun. Leiðsagnarforrit leiðir þig í gegnum umreikningsferlið.

## <a name="turn-on-the-feature-in-your-system"></a>Kveikja á eiginleikanum í kerfinu

Til að nota þennan eiginleika verður að ljúka eftirfarandi verkum:

1. Virkjið eiginleikann fyrir umsjón hönnunarbreytinga og skilgreiningarlykla hans eins og lýst er í [Yfirlit yfir umsjón hönnunarbreytinga](product-engineering-overview.md).
1. Kveikið á eiginleikanum *Virkja breytingastjórnun á fyrirliggjandi afurðum* í eiginleikastjórnun. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="restrictions-and-limitations"></a>Takmarkanir

Ekki er hægt að umbreyta öllum vörutegundum í allar aðrar gerðir. Eftirfarandi takmarkanir gilda:

- Þegar afurð er breytt í hönnunarafurð er hún enn *afurð*. Það verður ekki *afurðarsniðmát*.
- Þegar afurðarsniðmáti sem er með tiltekna víddasamstæðu er breytt, er víddunum viðhaldið eftir breytinguna. Ef til dæmis afurðarsniðmáti með stærðarvíddina er breytt mun það halda stærðarvíddinni.

Þar af leiðandi, ef um er að ræða einkvæma afurð, er aðeins hægt að breyta henni í hönnunarafurð sem rekur ekki afurðarvíddina í færslum (þ.e. útgáfuvíddin er ekki notuð). Skoðið þá hluta sem eftir eru í þessum efnisatriði til að fá frekari upplýsingar um þessi mál.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Undirbúa umbreytingu með því að stofna allar nauðsynlega hönnuarafurðaflokka

Úthluta þarf *afurðaflokki hönnunar* á hverja hönnunarafurð. Þetta er gert þegar leiðsögnin **Breyta í hönnunarafurð** er keyrð. Afurðarflokkar hönnunar verða að vera til fyrir allar viðeigandi staðlaðar afurðir *áður en* hægt er að breyta þessum afurðum.

Afurðarflokkur hönnunar býður upp á grunn til að stofna hönnunarafurð og gefur upp safn af sjálfgildum og reglum. Hönnunareigindir og sjálfgildi þeirra (eins og skilgreint er fyrir hönnunarflokkinn) eru einnig notuð í hönnunarafurðinni sem verður til. Þú getur breytt gildum eiginda og/eða bætt fleiri hönnunareigindum við afurðina eftir þörfum.

Hönnunarafurðarflokkurinn verður að passa við afurðina sem henni er úthlutað á. Afurðargerðin og víddaflokkurinn verða t.d. að passa bæði við afurðina og afurðarflokk hönnunar hennar. Frekari upplýsingar eru í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

> [!IMPORTANT]
> Leiðsögnin **Breyta í hönnunarafurð** getur aðeins breytt afurð í hönnunarafurðir þar sem útgáfan er ekki rakin í færslum. Þess vegna þarf að stilla valkostinn **Rekja útgáfu í færslum** á *Nei* fyrir afurðarflokka hönnunar sem eru stofnaðir til að breyta fyrirliggjandi afurðum.

Frekari upplýsingar um hvernig á að stofna afurðarflokka hönnunar er að finna í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).

## <a name="run-the-convert-to-engineering-product-wizard"></a>Leiðsögnin fyrir breytingu í hönnunarafurð keyrð

Leiðsögnin **Breyta í hönnunarafurð** aðstoðar við að breyta einni eða fleiri fyrirliggjandi afurðum í hönnunarafurðir. Hún breytir afurðunum í hönnunarafurðir (afurðir með útgáfu) þar sem útgáfan er ekki rakin í færslum (þ.e. útgáfuvíddin er ekki notuð). Eftir að breytingunni er lokið er hægt að stjórna afurðunum með því að nota breytingastjórnun hönnunar.

Umbreytingin er varanleg. Þess vegna er ekki hægt að snúa henni síðar. 

Hver umbreytt hönnunarafurð áfram losuð í sömu fyrirtækin og upprunalega afurðin. Hins vegar eru hönnunaruppskriftirnar og leiðirnar ekki losaðar sjálfkrafa til þessara fyrirtækja.

Fylgið þessum skrefum til að keyra leiðsögnina **Breyta í hönnunarafurð** og breyta afurð í hönnunarafurð.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið gátreitinn fyrir hverja afurð sem á að umbreyta í hnitanetinu.
1. Á aðgerðasvæðinu, í flipanum **Hönnun**, í flokknum **Umsjón hönnunarbreytinga**, skal velja **Breyta í hönnunarafurð** til að opna leiðsögnina.
1. Á fyrstu síðu leiðsagnarforritins er síðan **Velkomin(n)**. Ef þú þekkir ekki umreikningsferlið skaltu lesa upplýsingarnar á þessari síðu vandlega. Þegar notandi er reiðubúinn að halda áfram skal velja **Áfram**.
1. Síðan **Veldu upplýsingarnar fyrir afurðirnar sem skal breyta** sýnir hverja afurð sem var valin áður en leiðsögnin var opnuð. Skoðaðu listann. Notaðu hnappana **Nýtt** og **Eyða** á tækjastikunni til að bæta við eða fjarlægja afurðir eftir því sem þú þarfnast.
1. Notið eftirfarandi reiti efst í hnitanetinu til að úthluta sjálfgefnum gildum á hverja afurð sem er gefin upp. (Hægt verður að breyta þessum gildum fyrir einstakar afurðir eftir að breytingu lýkur.) Sjálfgefnum gildum verður ekki úthlutað afurðum þar sem viðeigandi gildi hefur þegar verið úthlutað.

    - **Sjálfgefinn hönnunarflokkur** – Veljið upphaflegan hönnunarflokk afurðar til að úthluta á hverja afurð sem er gefin upp. Flokkurinn sem er valinn verður aðeins notaður fyrir afurðir sem eru samhæfar við hann.
    - **Sjálfgefin útgáfa** – Færa inn upphaflegu afurðarútgáfuna sem á að úthluta á hverja skráða afurð. Þegar hönnunarafurðir eru notaðar hefur hver afurð a.m.k. eina hönnunarútgáfu.
    - **Sjálfgefin líftímastaða** – Veljið upphaflega líftímastöðu afurðar sem á að úthluta á hverja skráða afurð.
    - **Núverandi uppskrift verður hluti af hönnunarafurðinni** – Veljið þennan gátreit ef núverandi uppskrift fyrir hverja skráða afurð á að vera notuð fyrir hönnunarafurðina.

    Frekari upplýsingar um afurðarstillingar er að finna í næsta skrefi.

1. Yfirfarið hverja afurð sem er gefin upp í hnitanetinu og metið hvernig sjálfgefnu gildin sem þeim var úthlutað eiga við. Skoðið eftirfarandi upplýsingar í hverri línu og setjið upp viðeigandi reiti:

    - **Afurðarnúmer** – Afurðarnúmerið.
    - **Vöruheiti** – Nafn vörunnar.
    - **Flokkur hönnunar** – Veljið afurðarflokk hönnunar sem afurðin á að tilheyra eftir að búið er að breyta henni. Viðeigandi gerð verður þegar að vera til fyrir hverja afurð, eins og var útskýrt í fyrri hluta þessa efnisatriðis. Úthluta verður flokki á hverja afurð.
    - **Útgáfa** – Færið inn afurðarútgáfuna sem á að úthluta á afurðina eftir að henni hefur verið umbreytt. Til dæmis væri hægt að velja númer sem passar við númeraröðina sem flokkurinn notar þegar. Sérhver hönnunarútgáfa geymir gögnin sem tengjast hönnuninni sem á sérstaklega við þessa útgáfu. Frekari upplýsingar eru í [Hönnunarútgáfur og flokkar hönnunarafurðar](engineering-versions-product-category.md).
    - **Lífferilsstaða afurðar** – Veljið líftímastöðu afurðar sem afurðin á að vera í eftir að henni hefur verið umbreytt. Líftímastaða afurðar gerir þér kleift að hafa eftirlit með því hvaða færslur eru leyfðar fyrir tiltekna hönnunarútgáfu. Frekari upplýsingar er að finna í [Líftímastöður afurðar og færslur](product-lifecycle-state-transactions.md).
    - **Er með uppskrift** – Valinn gátreitur gefur til kynna að afurðin sé með uppskrift. Stillingin á þessum gátreit getur hjálpað til við að ákveða hvernig á að stilla gátreitinn **Núverandi uppskrift verður hluti af hönnunarafurðinni**.
    - **Núverandi uppskrift verður hluti af hönnunarafurðinni** – Veljið þennan gátreit ef núverandi uppskrift afurðarinnar á að vera notuð fyrir hönnunarafurðina. Þessari uppskrift verður síðan stjórnað af umsjón hönnunarbreytinga. Ef afurðin er ekki með uppsrkfit, eða ef þú kýst frekar að búa til uppskrift handvirkt fyrir breyttu afurðina seinna meir skaltu hreinsa þennan gátreit.
    - **Er með villur** – Valinn gátreitur gefur til kynna að afurðauppsetningin innihaldi eina eða fleiri villur. Til dæmis getur gerð afurðar eða víddaflokkur ekki haft samsvörun í flokknum. Vörum með villum verður sleppt og þeim verður ekki umbreytt.

1. Þegar því er lokið skal velja **Villuleita** á tækjastikunni til að villuleita uppsetningu afurðar. Fyrir hverja línu verður gátreiturinn **Er með villur** uppfærður til að gefa til kynna stöðu afurðarinnar. Stilltu gildin þar til uppsetning hverrar afurðar er villulaus.
1. Þegar allar afurðir eru settar upp á réttan hátt skal velja **Áfram** til að halda áfram.
1. Síðan **Staðfesta val** sýnir fjölda afurða sem er með villum í uppsetningu þeirra og eru þar af leiðandi tilbúnar fyrir breytingu. Hún sýnir einnig fjölda afurða sem verður slvegna villna. Til að keyra umbreytinguna sem runuvinnslu skal stilla **Keyra í runu** valkostinn *Já*.
1. Veljið **Ljúka** til að nota stillingarnar og byrjaðu að umbreyta afurðunum í hönnunarafurðir.

> [!NOTE]
> Ef kerfið er sett upp til að samþykkja afurðir handvirkt áður en þær eru losaðar þarf að samþykkja hverja breytta afurð fyrir sig með því að nota síðuna **Opna afurðarlosanir** í viðeigandi fyrirtækjum. Frekari upplýsingar eru í [Yfirfara og samþykkja afurðina áður en hún er gefin út í staðbundnu fyrirtæki](engineering-scenarios.md#accept).
