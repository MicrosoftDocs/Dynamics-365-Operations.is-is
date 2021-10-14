---
title: Yfirlit hættulegra efna
description: Í þessu efnisatriði er að finna yfirlit yfir eiginleika sem tengjast meðhöndlun og skráningu hættulegra efna við afurðarupplýsingastjórnun og vöruhúsastjórnun.
author: t-benebo
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 22e1b0838160378f3ff9484faaf87c9aec6e8964
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7570682"
---
# <a name="hazardous-materials-overview"></a>Yfirlit hættulegra efna

[!include [banner](../includes/banner.md)]

Til að fylgja eftir reglum um sendingar og flutninga verða fyrirtæki sem senda efni sem flokkast sem hættulegur varningur að vera með aukalega pappírsvinnu með sendingum sínum. Eiginleiki hættulegra efna gerir viðskiptavinum kleift að geyma upplýsingar sem tengjast losuðum vörum. Þessar upplýsingar er síðan hægt að nota til að undirbúa flutningsgögn. Fyrirtæki sem sendir hættulegan varning verður að hafa eigin ferla og verklagsreglur til að stjórna sendingarferlinu. Microsoft Dynamics 365 Supply Chain Management er bara verkfæri sem getur hjálpað til við að búa til nauðsynleg skjöl.

Eftirfarandi skýringarmynd sýnir skrefin sem þarf til að setja upp og nota eiginleika hættulegra efna.

![Uppsetning og notkun á eiginleika hættulegra efna.](media/hazmat-overview.png "Uppsetning og notkun á eiginleika hættulegra efna")

Eiginleiki hættulegra efna er settur upp í afurðaupplýsingastjórnun og býður upp á skjöl sem hægt er að prenta í gegnum vöruhúsakerfi. Almennt séð eru þessi svæði þar af leiðandi tvö helstu svæðin þar sem þú ferð yfir, setur upp og notar þessa virkni eiginleikans:

- **Afurðarupplýsingastjórnun** – Setjið upp kóðana sem verða notaðir fyrir útgefna afurð.
- **Vöruhúsakerfi** – vinna með fleiri sendingarskjöl sem verða prentuð fyrir sendingar.

> [!IMPORTANT]
> Eiginleikar hættulegra efna í Supply Chain Management bjóða upp á safn af gagnlegum reitum afurðarupplýsinga og tengdrar virkni sem getur hjálpað til við að skrá og vísa í upplýsingar sem tengjast hættulegum afurðum þínum. Þessir eiginleikar geta einnig hjálpað þér að hanna og prenta afhendingarskjöl sem innihalda einhverjar sömu upplýsingar um öll hættuleg efni sem þú ert að afhenda. Kerfið mun hins vegar ekki láta þig sjálfkrafa fylgja eftir öllum viðeigandi reglugerðum í landinu eða svæðinu þínu. Þótt þessum verkfærum sé ætlað að hjálpa til við að fylgja sameiginlegum reglugerðum eru þær hvorki nægilegar út af fyrir sig né tryggja að svo verði gert. Fyrirtækið þitt ber ábyrgð á því að gera sér grein fyrir öllum viðeigandi reglugerðum og gera allar nauðsynlegar ráðstafanir til að fylgja þeim eftir.

## <a name="product-information-management"></a>Vöruupplýsingastjórnun

Afurðarupplýsingastjórnun býður upp á úrval af uppsetningartöflum þar sem hægt er að færa inn tilvísunarupplýsingar fyrir ýmsa lista yfir hættulegan varning fyrir flutning á landi, í flugi eða sjóleiðis.

Vísað var til eftirfarandi sameiginlegra reglugerða þegar þessi virkni var þróuð:

- **ADR** - Reglugerðir sem tengjast alþjóðlegum flutningi á hættulegum farmi á vegum
- **CFR 49** - Reglugerðir í Sameinuðu þjóðunum um flutning hættulegs vara
- **IMDG** - Alþjóðlega sjávarhættulegu vörurnar (IMDG) kóðinn
- **IATA** - Alþjóðlega flugsamgöngusamtökin (IATA) reglugerðir um hættulegan varning

Í öllum reglugerðum er sýndur staðlaður listi yfir hættulegan varning og tilvísunarkóða. Þess vegna býður Supply Chain Management upp á tilvísunartöflu fyrir algengu kóðana í þessum listum. Hver listi er einnig með nokkra einkvæma kóða sem hægt er að skilgreina.

Frekari upplýsingar um hvernig setja á upp reglugerðir og gildi fyrir hættuleg efni, og hvernig á að úthluta gildunum á viðeigandi afurðir er að finna í eftirfarandi efnisatriðum:

- [Setja upp hættuleg efni](hazmat-setup.md)
- [Hættuleg efni í afurðum, pöntunum, sendingum og förmum](hazmat-items.md)

## <a name="warehouse-management"></a>Vöruhúsakerfi

Þegar sending er undirbúin í vöruhúsakerfinu er hægt að prenta út margar nýjar skýrslur sem nota upplýsingarnar sem eru settar upp í afurðaupplýsingastjórnun. Frekari upplýsingar um tiltækar skýrslur og hvernig á að nota þær er að finna í [Fyrirspurnir og skýrslur um hættuleg efni](hazmat-reports.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]