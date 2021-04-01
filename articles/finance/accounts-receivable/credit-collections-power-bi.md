---
title: Skulda- og innheimtuumsjón Power BI efni
description: Þetta efnisatriði lýsir því hvað er innifalið í skulda- og innheimtuumsjón Power BI efnis. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: dfa79b3fb4099d64390c17b39508deaac63deb1c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235162"
---
# <a name="credit-and-collections-management-power-bi-content"></a>Skulda- og innheimtuumsjón Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í **Skulda- og innheimtuumsjón** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Skulda- og innheimtuumsjón** Power BI efni var búið til fyrir stjórnendur skulda og innheimta og innheimtufulltrúa. Hún hefur að geyma mikilvæga mælikvarða í skulda- og innheimtumálum, eins og útistandandi dagsölu, vanskil, váhrif lánamarks og viðskiptavini sem eru komnir yfir lánamörk. Hún notast við færslugögn og veitir samantekna sýn yfir skulda- og innheimtumál fyrir öll fyrirtæki. Hún gefur einnig sundurliðun á fyrirtæki, viðskiptavinahópa og viðskiptavini.

Þetta Power BI efni samanstendur af 10 skýrslusíðum:

- Tvær yfirlitssíður (ein síða fyrir skuldayfirlit og ein fyrir innheimtuyfirlit)
- Átta ítarlegar síður sem veita upplýsingar um mælieiningar í skulda- og innheimtumálum sem hægt er að skoða samkvæmt ýmsum víddum.

Allar upphæðir eru sýndar í gjaldmiðli kerfisins. Hægt er að stilla gjaldmiðil kerfis á síðunni **Kerfisfæribreytur**.

Sjálfgefið er að skulda- og innheimtugögn fyrir núverandi fyrirtæki séu sýnd. Til að skoða gögnin í öllum fyrirtækjum, úthlutaðu skyldunni **CustCollectionsBICrossCompany** á hlutverkið.

## <a name="setup-needed-to-view-power-bi-content"></a>Uppsetningu þarf til að skoða efni Power BI

Eftirfarandi uppsetningu þarf að vera lokið svo að gögn birtist í myndefni **Skuldir og innheimta viðskiptavinar** Power BI.

1. Farðu í **Kerfisstjórnun > Uppsetning > Kerfisfæribreytur** til að stilla **Kerfisgjaldmiðil** og **Kerfisgengi**.
2. Farðu í **Fjárhagur > Dagatöl > Fjárhagsdagatöl** til að staðfesta dagsetningar fjárhagsdagatala sem er úthlutað á virka tímabilið.
3. Farðu í **Fjárhag> Uppsetning> Fjárhag** og stilltu **Bókhaldsgjaldmiðil** og **Gerð gengis**.
4. Skilgreindu gengi milli færslugjaldmiðla og bókhaldsgjaldmiðils, bókhaldsgjaldmiðils og kerfismynt. Til að gera þetta skaltu fara í **Fjárhag> Gjaldmiðla> Gengi gjaldmiðla**.
5. Farðu í **Fara í Kerfisstjórnun > Uppsetning > Eining averslun** til að uppfæra **CustCollectionsBIMeasurementsV2** uppsöfnuðu mælingarnar.

>[!NOTE] 
> Skilgreiningar aldurstímabils verða að vera sett upp í **Færibreytur viðskiptakrafna > Söfn > Sjálfgefin söfn** til að virkja aldursgreiningargögn í Power BI efni.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni

**Skulda- og innheimtustjórnun** Power BI efni er sýnt í vinnusvæðinu **Skuldir og innheimta viðskiptavinar**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Skýrslur sem eru hafðar með í Power BI efni

**CustCollectionsBICrossCompany** Power BI efni inniheldur skýrslu sem samanstendur af safni mælikvarða. Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur. Eftirfarandi tafla veitir yfirlit yfir myndrænar framsetningar í **CustCollectionsBICrossCompany** Power BI efni.

| Skýrslusíða                 | Myndbirting |
|-----------------------------|---------------|
| Innheimtuyfirlit        | <ul><li>Viðskipatvinir komnir fram yfir gjalddaga</li><li>Viðskiptavinir yfir kreditmörk</li><li>Dagar útistandandi sölu 30</li><li>Opin mál</li><li>Dagar að meðaltali til lokunar tilviks</li><li>Opnir verkþættir</li><li>Dagar að meðaltali til lokunar aðgerða</li><li>Opna vaxtanótur</li><li>Opna innheimtubréf</li><li>Viðskiptavinur á bið</li><li>Sala á bið</li><li>Aldursgreindar stöður</li><li>Upphæðir innheimtustöðu</li><li>Upphæðir innheimtukóða</li><li>Afskriftir eftir ástæðum</li><li>Gjaldfallið eftir svæðum</li><li>Væntanlegar greiðslur</li></ul> |
| Yfirlit yfir lánamark             | <ul><li>Viðskipatvinir komnir fram yfir gjalddaga</li><li>Lánamark gegn gjaldfallinni stöðu</li><li>Hnitanet fyrir viðskiptavini yfir lánamörkum</li><li>Viðskiptavinir yfir lánamörkum á hvert fyrirtæki</li><li>Nýtt lánamark gegn heildarlánamarki</li><li>Lánamark gegn notuðu lánsfé eftir svæðum</li><li>Viðskiptavinir á hver lánamörk</li></ul> |
| Lánamörk                | <ul><li>Lánamörk</li><li>Upplýsingar um lánamark</li><li>Lánamark á viðskiptavin</li><li>Lánamark á hvern viðskiptavinaflokk</li><li>Lánamark á hverja lánshæfiseinkunn á hvert fyrirtæki</li><li>Lánamark gegn notuðu lánsfé eftir svæðum</li></ul> |
| Viðskiptavinir yfir kreditmörk | <ul><li>Viðskiptavinir yfir kreditmörk</li><li>Upplýsingar um viðskiptavini yfir lánamörkum</li><li>Viðskiptavinir yfir lánamörkum á hvert fyrirtæki</li><li>Viðskiptavinur yfir lánamarki á hvern viðskiptavinaflokk</li><li>Viðskiptavinir yfir lánamörkum eftir svæðum</li></ul> |
| Viðskipatvinir komnir fram yfir gjalddaga          | <ul><li>Viðskipatvinir komnir fram yfir gjalddaga</li><li>Upplýsingar um viðskiptavini komna fram yfir gjalddaga</li><li>Viðskiptavinur með gjaldfallna skuld á hvert fyrirtæki</li><li>Viðskiptavinur með gjaldfallna skuld á hvern viðskiptavinaflokk</li><li>Viðskiptavinur með gjaldfallna skuld eftir svæðum</li></ul> |
| Aldursgreindar stöður               | <ul><li>Aldursgreindar stöður</li><li>Upplýsingar um aldursgreindar stöður</li><li>Aldursgreindar stöður á hvert fyrirtæki</li><li>Aldursgreindar stöður á hvern viðskiptavinaflokk</li></ul> |
| Væntanlegar greiðslur           | <ul><li>Væntanlegar greiðslur</li><li>Upplýsingar um væntanlegar greiðslur</li><li>Greiðslur sem er búist við fyrir hvert fyrirtæki</li><li>Greiðslur sem er búist við fyrir hvern viðskiptavinaflokk</li><li>Greiðslur sem er búist við eftir svæðum</li></ul> |
| Afskriftir                  | <ul><li>Afskriftir eftir svæðum</li><li>Upplýsingar um afskriftir</li><li>Afskriftir eftir aðallyklum</li><li>Afskriftir fyrir hvert fyrirtæki</li><li>Afskriftir á hvern flokk viðskiptavina</li><li>Afskriftir eftir svæðum</li></ul> |
| Staða innheimtu          | <ul><li>Umdeild</li><li>Loforð um greiðslu svikið</li><li>Gefa loforð um greiðslu</li><li>Upplýsingar um innheimtustöðu</li><li>Upphæðir innheimtustöðu</li><li>Opin mál</li><li>Opnir verkþættir</li></ul> |
| Innheimtubréf         | <ul><li>Upphæðir innheimtukóða</li><li>Upplýsingar um upphæðir innheimtukóða</li><li>Upphæðir innheimtubréfa á hvert fyrirtæki</li><li>Upphæðir innheimtubréfa á hvern viðskiptavinaflokk</li><li>Upphæðir innheimtubréfa eftir svæðum</li></ul> |

Hægt er að sía og festa Gröf og reitir á þessar skýrslur við mælaborð. Nánari upplýsingar um hvernig á að sía og festa í Power BI, sjá [Stofna og Skilgreina Mælaborð](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Einnig má nota virknina til að Flytja út undirliggjandi gögn til að flytja út undirliggjandi gögn sem eru sýnd í myndrænni samantekt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]