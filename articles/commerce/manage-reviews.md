---
title: Stjórna einkunnum og umsögnum
description: Þetta efni útskýrir hvernig á að stjórna einkunnagjöf og umsögnum með því að nota Microsoft Dynamics 365 Commerce einkunnir og umsagnir stjórnunar tól.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027243"
---
# <a name="manage-ratings-and-reviews"></a>Stjórna einkunnum og umsögnum

[!include [banner](includes/banner.md)]

Þetta efni útskýrir hvernig á að stjórna einkunnagjöf og umsögnum með því að nota Microsoft Dynamics 365 Commerce einkunnir og umsagnir stjórnunar tól.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce notar Microsoft Azure Cognitive Services til að miðla sjálfkrafa endurskoðun texta með því að ritstýra blótsyrði. Að auki geta stjórnendur notað einkunnagjafartólið og skoðað stjórnunartólið fyrir eftirfarandi handvirk verk:

- Breyta umsögnum með því að svara þeim eða fjarlægja þær.
- Eyða umsögnum viðskiptavinarins að beiðni viðskiptavinarins.
- Flyttu inn einkunnir og umsagnir fyrir allar vörur í Microsoft Power BI-sniðmáti, svo að hægt sé að greina þróun á einkunnum og umsögnum.

## <a name="access-ratings-and-reviews-moderation-features"></a>Fara í eiginleika einkunnagjafar og stjórnunar

Fylgdu þessum skrefum til að fá aðgang að einkunnagjöf og yfirfara stjórnunaraðgerðir í stjórnunartólinu fyrir rafræn viðskipti.

1. Skráðu þig inn í [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).
1. Opnaðu verkefnið sem inniheldur umhverfið þar sem þú vilt frumstilla rafræn viðskipti.
1. Í hlutanum **Umhverfi**, veldu umhverfið.
1. Undir **Eiginleikar umhverfis** velurðu **Stjórna Retail**.
1. Á **rafræn viðskipti** flipinn undir **Krækjur**, veldu **tól til að stjórna netverslun**.

## <a name="read-a-review"></a>Lesa umsögn 

1. Farðu í **Heim \> Umsagnir \> Breyting**.
1. Notaðu leitarreitinn efst til hægri á síðunni til að sía umsagnir sem eru sýndar með afurðakenni, vöruheiti eða umsagnartexta.

Viðbótarsíur gera þér kleift að takmarka umsagnir eftir tímabili, einkunn, rás eða áhyggjustöðu (tekin niður, svarað eða tilkynnt).

![Heimasíða breytingar](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Svara umsögn 

Stundum lýsa viðskiptavinir sem keyptu vöru ánægju sinni eða óánægju, eða skilja ekki hvernig þeir nota vöruna. Sem stjórnandi geturðu sent svar við gagnrýni. Þetta svar birtist ásamt umsögninni á síðunni. 

Fylgdu þessum skrefum til að svara umsögn.

1. Farðu í **Heim \> Umsagnir \> Breyting**.
1. Finndu og veldu umsögnina sem krefst svara.
1. Í eiginleikaglugganum til hægri velurðu **Bæta við svari**.
1. Sláðu inn svartexta og nafn sem ætti að sýna fyrir svarandann. Sjálfgefið svar svarandsins er **Stjórnandi**.
1. Þegar því er lokið skal velja **Bóka svar**.

![Svar við umsögn](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Fjarlægja umsögn 

Stundum er viðskiptaleg réttlæting fyrir því að stjórnendur fjarlægi umsagnir viðskiptavina. 

Til að fjarlægja umsögn fylgirðu þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Breyting**.
1. Finndu og veldu umsögnina sem þarf að fjarlægja.
1. Veldu eiginleikagluggann til hægri, veldu ástæðu fjarlægingar og síðan **Fjarlægja**.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Eyða umsögnum viðskiptavinarins að beiðni viðskiptavinarins 

Stundum vilja viðskiptavinir að einkunna- og umsagnagögnum þeirra verði varanlega eytt af vefsíðu netverslunar. Stjórnandi sem fær beiðni um flutning frá viðskiptavini getur fjarlægt gögn viðskiptavinarins með því að nota endurskoðunaraðgerðina. Til að finna og eyða gögnum viðskiptavinar þarf stjórnandinn netfangið sem viðskiptavinurinn notaði til að skrá sig inn og veita umsagnir. 

Fylgdu þessum skrefum til að finna og eyða gögnum viðskiptavina.

1. Farðu í **Heim \> Umsagnir \> Eyða**.
1. Í reitnum **Leita að notendum með netfangi** slærðu inn netfang viðskiptavinarins og velur síðan **Leita**.
1. Ef viðskiptavinurinn hefur einhverjar umsagnaraðgerðir (til dæmis, endurskoða innsendingar, atkvæði um hjálpsemi umsagna annars viðskiptavinar eða athugasemdir um umsögn annars viðskiptavinar) eru niðurstöðurnar sýndar. Fyrir hvern lið er hnappurinn **Eyða**.
1. Fyrir hvert atriði sem þarf að eyða velurðu **Eyða**. Þegar þú færð kvaðningu um staðfestingu skaltu velja **Já**. 
    
![Eyðing á gögnum viðskiptavinar](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Það getur tekið allt að sjö daga þar til gögn eru fjarlægð að fullu úr kerfinu. Stjórendur ættu að tilkynna viðskiptavinum um þessa seinkun.
> - Ef viðskiptavinir hafa breytt nafni sínu í reikningsstillingunum gætu mörg atriði birst í leitarniðurstöðum. Í þessu tilfelli, til að eyða gögnum viðskiptavina að fullu verður stjórnandinn að velja **Eyða** fyrir hverja vöru. 

## <a name="download-ratings-and-reviews-data"></a>Sækja einkunna- og umsagnagögn

Stjórnendatól einkunna og umsagna gerir stjórnendum kleift að flytja inn einkunna- og umsagnagögn í magni, svo að þau geti greint leitni. Power BI-sniðmát sem inniheldur grunnmælingar er fáanlegt. Stjórnendur geta notað þetta snið til að tengja magninnflutt gögn og skoða stjórnborð. Þeir þurfa ekki að búa til sérsniðið mælaborð. Stjórnendur geta sérsniðið Power BI-sniðmát til að mæta tilteknum þörfum sínum. 

Fylgdu þessum skrefum til að hlaða niður einkunnagjöf og umsögnum.

1. Farðu í **Heim \> Umsagnir \> Skýrslugerð**.
1. Veldu **Sækja umsagnargögn** til að sækja einkunna- og umsagnargögn í magni með kommuaðskildu gildum (CSV) sniði.

## <a name="view-ratings-and-reviews-trends"></a>Skoða einkunnir og umsagnaleitni

Stjórnendur geta hlaðið niður Power BI-sniðinu svo að þeir geti skoðað leitni í stjórnborði.

Til að skoða einkunna- og umsagnaleitni skaltu fylgja þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Skýrslugerð**.
1. Veldu **PowerBI sniðmát** til að hlaða niður sniðmátinu.

    ![Sæki Power BI sniðmátið](media/rnr-moderation-reports.png) 

1. Opnaðu sniðmátið sem hlaðið var niður með því að nota Power BI forritð. Lokaðu glugganum **Aðgangur að vefefni** sem birtist og lokaðu síðan villunni "Endurnýja" sem birtist.
1. Farðu í **Heim**, veldu **Breyta fyrirspurnum** og veldu síðan **Stillingar gagnagjafa**.
1. Í valmyndinni **Stillingar gagnagjafa** velurðu **Breyta gjafa**.
1. Í reitinn **Vefslóð** slærðu inn slóð umsagnargagnanna sem þú sóttir í fyrra ferli (til dæmis, **c:\\reviews\\ReviewsData.csv**).

    ![Vefslóðareitur í svarglugganum með kommuaðgreindum gildum](media/rnr-powerbi-datasource-settings.png) 

1. Veldu **Í lagi** og veldu síðan **Beita breytingum**. Það mun taka eina til tvær mínútur að nota breytingarnar á gagnagjafa.
1. Veldu **Þróunarblað** til að skoða einkunnir og rifja upp þróun.

    ![Einkunna- og umsagnaþróun](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md)

[Velja að nota einkunnir og umsagnir](opt-in-ratings-reviews.md)

[Skilgreina einkunnir og umsagnir](configure-ratings-reviews.md)

[Samstilla afurðaeinkunnir í Dynamics 365 Retail](sync-product-ratings.md)
