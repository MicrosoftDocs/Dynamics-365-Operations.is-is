---
title: Rifta greiðsluáætlunum
description: Þetta efnisatriði útskýrir hvernig á að slíta innheimtuáætlunum og innheimtuáætlunarlínum í áskriftarreikningum.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: e823ce950d6a4687dc7cda14e06bffdbb4f37f7e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690977"
---
# <a name="terminate-billing-schedules"></a>Rifta greiðsluáætlunum

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að slíta innheimtuáætlunum og innheimtuáætlunarlínum í áskriftarreikningum. Þegar þú segir upp innheimtuáætlun verður hún að hafa stöðuna **Virkur**. Það getur ekki haft stöðu á **Á bið**. Sömuleiðis, þegar þú segir upp greiðsluáætlunarlínu, verður hún að hafa stöðuna **Virkur**. Höfuðhluti innheimtuáætlunarinnar verður ekki fyrir áhrifum þegar þú segir upp innheimtuáætlunarlínu.

Til að slíta innheimtuáætlun eða innheimtuáætlunarlínu skaltu fara á einn af eftirfarandi stöðum:

- The **Allar/virkar innheimtuáætlanir** listasíðu
- Sérstök innheimtuáætlun á **Allar innheimtuáætlanir** síðu
- Sérstök innheimtuáætlunarlína á **Allar innheimtuáætlanir** síðu

> [!NOTE]
> Ef þú vilt segja upp nokkrum innheimtuáætlunum á sama tíma skaltu nota **Fjöldauppsagnarvinnsla** síðu.

## <a name="terminate-a-billing-schedule-or-line"></a>Hætta innheimtuáætlun eða línu

Til að slíta innheimtuáætlun eða innheimtuáætlunarlínu skaltu fylgja þessum skrefum.

1. Veldu innheimtuáætlun eða línu fyrir innheimtuáætlun og veldu síðan **Hætta**. 
2. Stilltu **Uppsagnardagur**, **·**, og **Ástæðukóði** sviðum.
3. Stilltu **Lánarmöguleiki** sviði til **Gefðu út lánsfé**.
4. Veldu **Hætta**.

Staða innheimtuáætlunarinnar breytist, byggt á uppsagnargerðinni sem þú valdir. Ef þú valdir **Reikningur eftir** sem uppsagnartegund er staða allra lína í innheimtuáætlun **Síðasta innheimta**. Staða innheimtuáætlunar er eftir **Virkur** þar til síðasti reikningur er afgreiddur. Eftir að síðasta reikningur hefur verið afgreiddur er staðan uppfærð í **Hætti**. Ef þú valdir **Stilla áætlun** sem uppsagnartegund er staða innheimtuáætlunarinnar strax uppfærð í **Hætti**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Slepptu innheimtuáætlun eða línu og sóttu um endurgreiðslu

Til að slíta innheimtuáætlun eða innheimtuáætlunarlínu og beita endurgreiðslu skaltu fylgja þessum skrefum.

1. Veldu innheimtuáætlun eða línu fyrir innheimtuáætlun og veldu síðan **Hætta**.
2. Stilltu **Uppsagnardagur**, **·**, **·**, og **Lánarmöguleiki** sviðum.
3. Veldu **Hætta með endurgreiðslu**. The **Fjöldauppsagnarvinnsla** síða birtist og er síuð þannig að hún sýnir innheimtuáætlun.
4. Veldu **Skoða forskoðun** til að skoða línur innheimtuáætlunar og veldu síðan **Ferli**.

Eftir að inneign hefur verið afgreidd skaltu opna **Skoða innheimtuupplýsingar** síðu til að skoða inneignina sem var sett á innheimtuáætlunina. Ef kreditupphæðin er hærri en 0 (núll), er öllum óinnheimtu línum í framtíðinni eytt og skipt út fyrir línur með innheimtuupplýsingar sem sýna neikvæðar upphæðir fyrir inneignina sem var sett á innheimtuáætlunina.

### <a name="view-example"></a>Skoða dæmi

Innheimtuáætlun hefur eftirfarandi upplýsingar:

- Upphafsdagur er 1. janúar 2020.
- Lokadagur er 31. desember 2020.
- Upphæð innheimtutímabilsins er 100,00 á mánuði.
- Reikningar hafa verið búnir til fyrir innheimtutímabil frá janúar til júlí.
- Uppsagnardagur samningsins er 15. júní 2020.

Þegar lánaleiðréttingin er afgreidd eru öll framtíðarreikningstímabil (ágúst til desember) fjarlægð úr **Skoða innheimtuupplýsingar** síðu. Línuleiðréttingarlínu er bætt við eftir reikningstímabilið í júlí:

- 16. júní–31. júlí, með inneign 150,00

Ef óinnheimtar tekjur eiginleiki er notaður, **Úttekt á óinnheimtu tekjubókarfærslu** síða er uppfærð með uppsagnarfærslunni.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Slepptu innheimtuáætlun eða línu án þess að nota inneign

Til að slíta innheimtuáætlun eða innheimtuáætlunarlínu án þess að nota inneign skaltu fylgja þessum skrefum.

1. Veldu innheimtuáætlun eða línu fyrir innheimtuáætlun og veldu síðan **Hætta**.
2. Stilltu **Uppsagnardagur** sviði.
3. Stilltu **Uppsagnartegund** sviði til **Engin aðlögun**. The **Lánarmöguleiki** reiturinn er sjálfkrafa stilltur á **Engin inneign**.
3. Stilltu **Ástæðukóði** sviði.
4. Í **Uppsagnarseðlar** reit, sláðu inn allar athugasemdir sem þarf.
5. Veldu **Hætta**. 

Þegar uppsögnin er afgreidd eru allar innheimtuupplýsingarnar eftir uppsagnardaginn fjarlægðar. (Þessar línur innihalda línuna sem inniheldur uppsagnardagsetningu.) Ekki er hægt að búa til reikninga fyrir uppsagnar línur. Ef uppsögnin er fjarlægð, bætast allar uppsagnar línur aftur við **Skoða innheimtuupplýsingar** síðu og verða aðgengileg fyrir reikningagerð.

## <a name="fields"></a>Svæði

The **Skoða innheimtuupplýsingar** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|-------|-------------| 
| Starfslokadagur | Veldu dagsetninguna þegar þú vilt segja upp innheimtuáætlun eða innheimtuáætlunarlínu. |
| Tegund uppsagnar | <p>Veldu uppsagnartegund:</p><ul><li>**Stilla áætlun** – Slepptu innheimtutímabilum fyrir línuna á uppsagnardegi og breyttu stöðu línunnar í **Síðasta innheimta**. Ef frestunaráætlun er til fyrir línuvöruna er hún leiðrétt með því að bakfæra upphæðina sem ekki má lengur viðurkenna. Ef upphafsdagur innheimtu er eftir uppsagnardaginn eru reikningstímabilin sem eftir eru fjarlægð.</li><li>**Reikningur eftir** – Bættu eftirstandandi upphæð fyrir reikningstímabilið við uppsagnartímabilið og breyttu stöðu línunnar í **Síðasta innheimta**. Ef frestunaráætlun er til fyrir línuna er lokadagsetning frestunarinnar uppfærð. Ef upphafsdagur innheimtu er eftir uppsagnardagsetningu er heildarupphæð allra eftirstandandi innheimtutímabila bætt við innheimtutímabilið og eftirstandandi innheimtutímabil eru fjarlægð.</li><li>**Engin aðlögun** – Ljúktu innheimtutímabilum línunnar á tilgreindum uppsagnardegi. Engar lagfæringar eru gerðar. Þegar þessi uppsagnartegund er valin, **Lánarmöguleiki** reiturinn er stilltur á **Engin inneign**, og **Hlutfallslega daglega** reiturinn er stilltur á **Nei**. Báðir þessir reiti verða þá skrifvarinn og ekki er hægt að breyta þeim.</li></ul> |
| Valkostur kreditfærslu | <p>Veldu hvernig inneignin er notuð þegar þú segir upp greiðsluáætlunarlínu:</p><ul><li>**Leiðrétting lána** – Búðu til inneignarleiðréttingu fyrir innheimtuáætlun þegar línu er hætt. Lánsfjárleiðréttingin birtist á framtíðarreikningstímabili fyrir innheimtuáætlunina. Leiðréttingin leiðréttir einnig sjálfkrafa reikningsupphæð fyrir næsta reikningstímabil þar til inneign hefur lokið við að setja innheimtuáætlunina.</li><li>**Gefðu út lánsfé** – Búðu til kreditnótu þegar innheimtuáætlun eða innheimtuáætlunarlínu er hætt.</li><li>**Engin inneign** – Ekki búa til kreditleiðréttingu eða inneignarnótu þegar innheimtuáætlun eða innheimtuáætlunarlínu er hætt. Þessi valkostur er aðeins í boði þegar þú notar uppsögn á **Engin aðlögun** tegund til að slíta innheimtuáætlun.</li></ul><p>Sjálfgefinn valkostur er frá **Endurteknar innheimtufæribreytur samnings** síðu.</p> |
| Ástæðukóði | Veldu ástæðukóðann fyrir uppsögninni. |
| Lýsing á ástæðu | Lýsingin á ástæðukóðanum. |
| Starfslokaglósur | Sláðu inn allar athugasemdir um uppsögnina. |

<!--## Additional information-->
