---
title: Rifta greiðsluáætlunum
description: Þessi grein útskýrir hvernig á að segja upp greiðsluáætlun og greiðsluáætlunarlínum í Áskriftargreiðslu.
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
ms.openlocfilehash: 4fce23f3cf35ef8c388ce13fc422f268a2bd8e32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872558"
---
# <a name="terminate-billing-schedules"></a>Rifta greiðsluáætlunum

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að segja upp greiðsluáætlun og greiðsluáætlunarlínum í Áskriftargreiðslu. Þegar þú segir upp greiðsluáætlun verður hún að hafa stöðuna **Virk**. Hún getur ekki haft stöðuna **Í bið**. Sömuleiðis, þegar þú segir upp greiðsluáætlunarlínu verður hún að hafa stöðuna **Virk**. Haushluti greiðsluáætlunarinnar verður ekki fyrir áhrifum ef greiðsluáætlunarlínu er sagt upp.

Til að segja upp greiðsluáætlun eða greiðsluáætlunarlínu skal opna einn af eftirfarandi stöðum:

- Listasíðan **Allar/Virkar greiðsluáætlanir**
- Sérstök greiðsluáætlun á síðunni **Allar greiðsluáætlanir**
- Sérstök greiðsluáætlunarlína á síðunni **Allar greiðsluáætlanir**

> [!NOTE]
> Ef segja á upp mörgum greiðsluáætlunum á sama tíma skal nota síðuna **Úrvinnsla fjöldauppsagnar**.

## <a name="terminate-a-billing-schedule-or-line"></a>Segja upp greiðsluáætlun eða línu

Til að segja upp greiðsluáætlun eða greiðsluáætlunarlínu skal fylgja þessum skrefum.

1. Veljið greiðsluáætlun eða greiðsluáætlunarlínu og svo **Segja upp**. 
2. Stilltu **Dagsetning uppsagnar**, **Tegund uppsagnar** og **Ástæðukóði** reitina.
3. Stillið reitinn **Valkostur kreditfærslu** á **Gefa út kreditfærslu**.
4. Velja **Segja upp**

Staða greiðsluáætlunarinnar breytist í samræmi við þá tegund uppsagnar sem valin var. Ef þú valdir **Eftirstöðvar greiðslu** sem uppsagnargerð er staða allra lína í greiðsluáætluninni **Síðasta reikningsfærsla**. Staða greiðsluáætlunarinnar er áfram **Virk** þar til síðasti reikningurinn er meðhöndlaður. Eftir að síðasti reikningurinn er meðhöndlaður er staðan uppfærð í **Sagt upp**. Ef þú valdir **Breyta áætlun** sem tegund uppsagnar er staða greiðsluáætlunarinnar strax uppfærð í **Sagt upp**.

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>Segja upp greiðsluáætlun eða línu og nota endurgreiðslu

Til að segja upp greiðsluáætlun eða greiðsluáætlunarlínu og nota endurgreiðslu skal fylgja þessum skrefum.

1. Veljið greiðsluáætlun eða greiðsluáætlunarlínu og svo **Segja upp**.
2. Stilltu **Dagsetning uppsagnar**, **Tegund uppsagnar**, **Ástæðukóði** og **Valkostur kreditfærslu** reitina.
3. Veljið **Uppsögn með endurgreiðslu**. Síðan **Úrvinnsla fjöldauppsagnar** birtist og er síuð þannig að hún sýni greiðsluáætlunina.
4. Veljið **Skoða forskoðun** til að skoða greiðsluáætlunarlínur og veljið síðan **Ferli**.

Þegar inneignin hefur verið meðhöndluð opnar þú síðuna **Skoða greiðsluupplýsingar** til að fara yfir inneignina sem var notuð á greiðsluáætlunina. Ef upphæð inneignar er hærri en 0 (núll) er öllum óútfylltum línum í framtíðinni eytt og þeim skipt út fyrir reikningsupplýsingalínur sem sýna neikvæðar upphæðir fyrir inneignina sem var notuð á greiðsluáætlunina.

### <a name="view-example"></a>Skoða dæmi

Eftirfarandi upplýsingar koma fram í greiðsluáætlun:

- Upphafsdagsetning er 1. janúar 2020.
- Lokadagsetning er 31. desember 2020
- Upphæð reikningstímabils er kr. 100,00 á mánuði.
- Reikningar hafa verið stofnaðir fyrir reikningstímabil frá janúar til og með júlí.
- Uppsagnarfrestur samnings er til 15. júní 2020.

Þegar kreditleiðréttingin er meðhöndluð eru öll reikningstímabil (ágúst til og með desember) fjarlægð af síðunni **Skoða greiðsluupplýsingar**. Kreditleiðréttingarlínu er bætt við eftir reikningstímabilið í júlí:

- 16. júní til 31. júlí 31, með kreditupphæð 150,00

Ef eiginleiki óreikningsfærðra tekna er notaður er síðan **Eftirlit með bókarfærslu óreikningsfærðra tekna** uppfærð með lokafærslunni.

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>Segja upp greiðsluáætlun eða línu án þess að nota inneign

Ef þú vilt segja upp greiðsluáætlun eða greiðsluáætlun án þess að nota inneign skaltu fylgja þessum skrefum.

1. Veljið greiðsluáætlun eða greiðsluáætlunarlínu og svo **Segja upp**.
2. Stillið reitinn **Starfslokadagur**.
3. Stilla reitinn **Tegund uppsagnar** á **Engin leiðrétting**. Reiturinn **Valkostur kreditfærslu** er sjálfkrafa stilltur á **Engin inneign**.
3. Stillið reitinn **Ástæðukóði**.
4. Í reitnum **Starfslokaglósur** slærðu inn allar athugasemdir sem þarf til viðbótar.
5. Velja **Segja upp** 

Þegar unnið er úr uppsögninni eru allar upplýsingar um reikningslínur eftir lokadag fjarlægðar. (Þessar línur innihalda línuna sem inniheldur lokadagsetningu.) Ekki er hægt að búa til reikninga fyrir línurnar sem lokað hefur verið fyrir. Ef uppsögnin er fjarlægð er öllum línum sem hefur verið sagt upp bætt aftur við síðuna **Skoða reikningsupplýsingar** og þær verða tiltækar fyrir reikningagerð.

## <a name="fields"></a>Svæði

Á síðunni **Skoða reikningsupplýsingar** eru eftirfarandi reitir.

| Svæði | Lýsing |
|-------|-------------| 
| Starfslokadagur | Veldu dagsetningu þegar þú vilt segja upp greiðsluáætlun eða greiðsluáætlunarlínu. |
| Tegund uppsagnar | <p>Velja tegund uppsagnar:</p><ul><li>**Breyta áætlun** – Slökkva á reikningstímabilum fyrir línuna á lokadegi og breyta stöðu línunnar í **Síðasta reikningsfærsla**. Ef frestunaráætlun er til staðar fyrir línuatriðið er hún leiðrétt með því að bakfæra upphæðina sem ekki má lengur færa. Ef upphafsdagur reiknings er á eftir lokadegi eru eftirstandandi reikningstímabil fjarlægð.</li><li>**Eftirstöðvar greiðslu** – Bættu öllum eftirstandandi upphæðum fyrir reikningstímabilið við uppsagnartímann og breyttu stöðu línunnar í **Síðasta reikningsfærsla**. Ef frestunaráætlun er til fyrir línuatriðið er lokadagur frestunar uppfærður. Ef upphafsdagur reiknings er eftir lokadaginn er heildarupphæð allra eftirstandandi reikningstímabila bætt við reikningstímabilið og eftirstandandi reikningstímabil fjarlægð.</li><li>**Engin leiðrétting** – Ljúka reikningstímabilum fyrir línuna á tilgreindum lokadegi. Engar leiðréttingar eru gerðar. Þegar þessi tegund uppsagnar er valin er reiturinn **Valkostur kreditfærslu** stilltur á **Engin inneign** og **Hlutfallsskipta daglega** reiturinn er stilltur á **Nei**. Báðir þessir reitir verða þá skrifvarðir og ekki er hægt að breyta þeim.</li></ul> |
| Valkostur kreditfærslu | <p>Veldu hvernig inneignin er notuð þegar þú hættir greiðsluáætlunarlínu:</p><ul><li>**Kreditleiðréttingar** – Búðu til kreditleiðréttingu fyrir greiðsluáætlun þegar línu er sagt upp. Kreditleiðréttingin birtist á reikningstímabilum í framtíðinni fyrir greiðsluáætlunina. Leiðréttingin mun einnig sjálfkrafa leiðrétta reikningsupphæðina fyrir næsta greiðslutímabil þar til búið er að nota inneignina á greiðsluáætlunina.</li><li>**Gefa út kreditfærslu** – Stofna kreditnótu þegar greiðsluáætlun eða greiðsluáætlunarlínu er sagt upp.</li><li>**Engin inneign** – Ekki stofna kreditleiðréttingu eða kreditnótu þegar greiðsluáætlun eða greiðsluáætlunarlínu er sagt upp. Þessi valkostur er aðeins í boði þegar greiðsluáætlun er sagt upp með valkostinum **Engin leiðrétting**.</li></ul><p>Sjálfgefinn kostur er frá síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.</p> |
| Ástæðukóði | Velja ástæðukóða fyrir uppsögninni. |
| Lýsing á ástæðu | Lýsing á ástæðukóða. |
| Starfslokaglósur | Sláðu inn athugasemdir um uppsögnina. |

<!--## Additional information-->
