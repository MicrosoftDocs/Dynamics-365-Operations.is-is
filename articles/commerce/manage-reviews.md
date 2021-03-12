---
title: Stjórna einkunnum og umsögnum
description: Þetta efnisatriði útskýrir hvernig á að stjórna einkunnum og umsögnum í Microsoft Dynamics 365 Commerce vefsmið.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a70d0526fb2443605a6b11df3ee281d4dd12f1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982567"
---
# <a name="manage-ratings-and-reviews"></a>Stjórna einkunnum og umsögnum

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að stjórna einkunnum og umsögnum í Microsoft Dynamics 365 Commerce vefsmið.

## <a name="overview"></a>Yfirlit

Dynamics 365 Commerce notar Microsoft Azure Cognitive Services til að miðla sjálfkrafa endurskoðun texta með því að ritstýra blótsyrði. Auk þess geta stjórnendur notað Dynamics 365 Commerce-vefsmið til að innleiða eftirfarandi handvirk verk:

- Breyta umsögnum með því að svara þeim eða fjarlægja þær.
- Eyða umsögnum viðskiptavinarins að beiðni viðskiptavinarins.
- Flyttu inn einkunnir og umsagnir fyrir allar vörur í Microsoft Power BI-sniðmáti, svo að hægt sé að greina þróun á einkunnum og umsögnum.

## <a name="read-a-review"></a>Lesa umsögn 

Til að lesa umsögn í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Breyting**.
1. Notaðu leitarreitinn efst til hægri á síðunni til að sía umsagnir sem eru sýndar með afurðakenni, vöruheiti eða umsagnartexta.

Viðbótarsíur gera þér kleift að takmarka umsagnir eftir tímabili, einkunn, rás eða áhyggjustöðu (tekin niður, svarað eða tilkynnt).

![Heimasíða breytingar](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a>Svara umsögn 

Stundum lýsa viðskiptavinir sem keyptu vöru ánægju sinni eða óánægju, eða skilja ekki hvernig þeir nota vöruna. Sem stjórnandi geturðu sent svar við gagnrýni. Þetta svar birtist ásamt umsögninni á síðunni. 

Til að svara umsögn í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Breyting**.
1. Finndu og veldu umsögnina sem krefst svara.
1. Í eiginleikaglugganum til hægri velurðu **Bæta við svari**.
1. Sláðu inn svartexta og nafn sem ætti að sýna fyrir svarandann. Sjálfgefið svar svarandsins er **Stjórnandi**.
1. Þegar því er lokið skal velja **Bóka svar**.

![Svar við umsögn](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a>Fjarlægja umsögn 

Stundum er viðskiptaleg réttlæting fyrir því að stjórnendur fjarlægi umsagnir viðskiptavina. 

Til að fjarlægja umsögn í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Breyting**.
1. Finndu og veldu umsögnina sem þarf að fjarlægja.
1. Á eiginleikasvæðinu til hægri skal velja ástæðu fjarlægingar undir **Umsögn um fjarlægingu** og velja síðan **Fjarlægja**.
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a>Eyða umsögnum viðskiptavinarins að beiðni viðskiptavinarins 

Stundum vilja viðskiptavinir að einkunna- og umsagnagögnum þeirra verði varanlega eytt af vefsíðu netverslunar. Stjórnandi sem fær beiðni um flutning frá viðskiptavini getur fjarlægt gögn viðskiptavinarins með því að nota endurskoðunaraðgerðina. Til að finna og eyða gögnum viðskiptavinar þarf stjórnandinn netfangið sem viðskiptavinurinn notaði til að skrá sig inn og veita umsagnir. 

Til að finna og eyða gögnum viðskiptavinar í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Eyða**.
1. Í glugganum **Leita að notendum eftir netfangi** skal færa inn netfang viðskiptavinar og velja síðan **Leita**.
1. Ef viðskiptavinurinn hefur einhverjar umsagnaraðgerðir (til dæmis, endurskoða innsendingar, atkvæði um hjálpsemi umsagna annars viðskiptavinar eða athugasemdir um umsögn annars viðskiptavinar) eru niðurstöðurnar sýndar. Fyrir hvern lið er hnappurinn **Eyða**.
1. Fyrir hvert atriði sem þarf að eyða velurðu **Eyða**. Þegar þú færð kvaðningu um staðfestingu skaltu velja **Já**. 
    
![Eyðing á gögnum viðskiptavinar](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - Það getur tekið allt að sjö daga þar til gögn eru fjarlægð að fullu úr kerfinu. Stjórendur ættu að tilkynna viðskiptavinum um þessa seinkun.
> - Ef viðskiptavinir hafa breytt nafni sínu í reikningsstillingunum gætu mörg atriði birst í leitarniðurstöðum. Í þessu tilfelli, til að eyða gögnum viðskiptavina að fullu verður stjórnandinn að velja **Eyða** fyrir hverja vöru. 

## <a name="download-ratings-and-reviews-data"></a>Sækja einkunna- og umsagnagögn

Vefsmiður Commerce leyfir ritstjórum að flytja inn gögn einkunna og umsagna í magni, þannig að hægt sé að greina mynstur. Power BI-sniðmát sem inniheldur grunnmælingar er fáanlegt. Stjórnendur geta notað þetta snið til að tengja magninnflutt gögn og skoða stjórnborð. Þeir þurfa ekki að búa til sérsniðið mælaborð. Stjórnendur geta sérsniðið Power BI-sniðmát til að mæta tilteknum þörfum sínum. 

Til að sækja gögn einkunna og umsagna í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Skýrslugerð**.
1. Veljið **Sækja umsagnargögn** til að sækja gögn einkunna og umsagna í magni í gildum aðskildum með kommu (CSV-sniði).

## <a name="view-ratings-and-reviews-trends"></a>Skoða einkunnir og umsagnaleitni

Stjórnendur geta hlaðið niður Power BI-sniðinu svo að þeir geti skoðað leitni í stjórnborði.

Til að skoða mynstur einkunna og umsagna í vefsmið Commerce skal fylgja þessum skrefum.

1. Farðu í **Heim \> Umsagnir \> Skýrslugerð**.
1. Veldu **PowerBI sniðmát** til að hlaða niður sniðmátinu.

    ![Sækja Power BI-sniðmátið](media/rnr-moderation-reports.png) 

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
