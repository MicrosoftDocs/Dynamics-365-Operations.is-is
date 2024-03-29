---
title: Setja upp greiningu nýleika-, tíðni- og peningastigs (RFM)
description: Þessi grein útskýrir hvernig á að setja upp nýliða-, tíðni- og peningagreiningu (RFM) á viðskiptavinum þínum.
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRRFMDefinition
audience: Application User
ms.reviewer: josaw
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 153759ac6b70235b79c080e934819536c2861371
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850172"
---
# <a name="set-up-recency-frequency-and-monetary-rfm-analysis"></a>Setja upp greiningu nýleika-, tíðni- og peningastigs (RFM)

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp nýliða-, tíðni- og peningagreiningu (RFM) á viðskiptavinum þínum.

Greiningin Nýleikastig, Tíðnistig og Peningastig (RFM) er markaðssetningarverkfæri sem fyrirtæki þitt getur notað til að meta gögn sem myndast við innkaup viðskiptavina. Eftir að þú sett upp RFM-greiningu, eru viðskiptavinir úthlutað reiknað RFM-stigum þegar þeir gera innkaup. Rfm-stig getur þriggja stafa einkunn eða steypa saman núver, eftir því hvernig fyrirtæki þitt hefur skilgreint rfm-greining. Svona virkar einkunnargjöfin ef fyrirtækið notar þriggja stafa einkunn fyrir stigaskor:

- Fyrsti stafurinn er einkunn viðskiptavinar fyrir nýleika, sem er hve nýlega viðskiptavinur gerði innkaup frá fyrirtækinu.
- Annar stafurinn er einkunn viðskiptavinarins fyrir tíðni, sem er hversu oft viðskiptavinurinn gerir innkaup frá fyrirtækinu.
- Þriðji stafurinn er peningalegt einkunn viðskiptavinarins, sem er hversu miklu hann eyðir þegar hann gerir innkaup frá fyrirtækinu.

Til dæmis hefur fyrirtækið stillt einkunnir á skalanum 1 til 5, þar sem 5 er hæsta einkunn. Í þessu tilviki gefur mat viðskiptavinar upp á 535 eftirfarandi upplýsingar um viðskiptavininn:

- **Nýleikastig upp á 5** – Viðskiptavinurinn gerði innkaup nýlega.
- **Tíðnistig upp á 3** – Viðskiptavinurinn kaupir vörur frá fyrirtækinu í meðallagi oft.
- **Peningaeinkunn upp á 5** - Þegar viðskiptavinurinn gerir innkaup eyðir hann umtalsverðu magni af peningum.

Ef fyrirtækið notar uppsöfnuð númer, eru stigin lögð saman. Í sama dæmi er einkunn viðskiptavinarins 13 (5 + 3 + 5).

## <a name="set-up-rfm-analysis-for-the-customers-in-your-organization"></a>Setja upp RFM-greiningu fyrir viðskiptavini fyrirtækisins

1. Farðu í **Símaver** \> **Reglubundið** \> **RFM-greining**.
2. Á **RFM greining** síðu skaltu velja **Nýtt**. Í reitnum **RFM skilgreining** er fært inn heiti fyrir RFM skilgreininguna. Til dæmis, hægt væri að kalla á skilgreiningu RFM-A.
3. Færið inn upphafsdagsetningu og lokadagsetningu fyrir RFM skilgreiningu.
4. Á flýtiflipanum **Almennt** er eftirfarandi gert:

    - Ef hver hluti RFM stigaskors verður að innihalda jafnan fjöldi viðskiptavinum, veljið þá **Jöfn dreifing** gátreitinn.
    - Velja skal **Bæta við stigaskori** gátreit til að steypa saman öllum þremur stigaskorum. Þetta, til dæmis, myndi veita viðskiptavini RFM skor upp á 13 í stað 535.
    - Velja skal **Vista feril** gátreit til að krefja kerfið til að vista tölfræðileg gögn fyrir viðskiptavini þannig að gögnin sé hægt er að nota til að reikna út RFM skorið.

5. Á flýtiflipanum **Nýleiki** er eftirfarandi gert:

    - Í því **Deildir** svæðinu, færið inn fjölda deilda eða flokka sem verður notað til að reikna út á nýleikaskor fyrir viðskiptavini. Til dæmis, ef þú átt 100 viðskiptavinir þýðir skipting upp á 5 að það eru 20 viðskiptavina fyrir hvert stig. Þeir 20 viðskiptavinir sem hafa gert innkaup nýlega hafa nýleikaskor 5. Næstu 20 viðskiptavinir hafa nýleikaskor 4, og svo framvegis. Ef 50 viðskiptavini, 10 viðskiptavinir hafa stig recency upp á 5, 10 hafa recency stig 4 og svo framvegis.
    - Í **Forgangur** svæðinu skal velja hversu mikið vægi á að gefa nýleikafæribreytu miðað við aðrar færibreytur þegar RFM skorið er reiknuð út fyrir viðskiptavini. Til dæmis gætirðu lagt hærra gildi á nýleikastig en á peningastig.
    - Í **Margfaldari** svæðinu, færið inn gildi sem á að margfalda nýleikaskor með. Ef gildi er ekki færður þeirri einkunn sem er ekki margfaldað.
    - Í því **Tímabil** svæðinu, veljið það tímabil þar sem nýleikaskor er reiknuð. Til dæmis eftir viku eða mánuð.

6. Á flýtiflipanum **Tíðni** er eftirfarandi gert:

    - Í **Deildir** svæðinu, færið inn fjölda deilda eða flokka sem verður notað til að reikna út tíðniskor fyrir viðskiptavini.
    - Í **Forgangur** svæðinu skal velja hversu mikið vægi á að gefa tíðnifæribreytu miðað við aðrar þegar RFM skorið er reiknuð út fyrir viðskiptavini.
    - Í **Margfaldari** svæðinu, færið inn gildi sem margfalda á tíðniskor með. Ef gildi er ekki færður þeirri einkunn sem er ekki margfaldað.

7. Á flýtiflipanum **Peningalegt** er eftirfarandi gert:

    - Í **Deildir** svæðinu, færið inn fjölda deilda eða flokka sem verður notað til að reikna út á peningalegt skor fyrir viðskiptavini.
    - Í **Forgangur** svæðinu skal velja hversu mikið vægi á að gefa peningafæribreytu miðað við aðrar þegar RFM skorið er reiknuð út fyrir viðskiptavini.
    - Í **Margfaldari** svæðinu, færið inn gildi sem margfalda á peningaskorið með. Ef gildi er ekki færður þeirri einkunn sem er ekki margfaldað.
    - Í **Brúttó/nettó** svæðinu skal velja hvort eigi að reikna peningaskor viðskiptavinar með því að nota brúttó eða nettó reikningsupphæð.
    - Ef ætti að draga skilaupphæðir viðskiptavinar frá heildarútreikningi reiknings viðskiptavinar skal velja gátreitinn **Draga frá skil**.

## <a name="view-a-customers-rfm-score"></a>Skoða RFM-skor viðskiptavinar

Notið þessa aðferð til að skoða RFM-skor viðskiptavinar.

1. Fara í **Símaver** \> **Færslubækur** \> **Þjónustuver**.
2. Á **Þjónustuver** síðunni, á **Þjónustuver** rúðunni, í leitarsvæðunum, velja gerð lykilorðs til að leita í og færið inn leitartextann.
3. Velja **Leita**.
4. Á síðunni **Leit viðskiptavinur** skal velja viðskiptavinaskrá sem þú vilt og smellið síðan á **Velja viðskiptavinur**.

RFM skorið birtist í **Pöntunarferill** hópnum hægra megin á **Þjónustuver** síðunni.

## <a name="view-or-clear-the-history-of-an-rfm-analysis-record"></a>Skoða eða hreinsa sögu til RFM-greiningarfærslu

Notið þetta ferli til að skoða eða hreinsa sögu RFM analysis færslu.

1. Farðu í **Símaver** \> **Reglubundið** \> **RFM-greining**.
2. Á **RFM greining** síðunni skal velja skrána sem á að skoða.
3. Til að skoða skráarferil, smellið á flýtiflipann **Ferill**.
4. Til að hreinsa feril skráar, smellið á **Hreinsa feril**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]