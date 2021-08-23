---
title: Vinnusvæði bankakerfis
description: Í þessu efnisatriði er að finna upplýsingar um vinnusvæði bankakerfis. Þetta vinnusvæði sýnir upplýsingar sem tengjast bankareikningum fyrirtækis og felur í sér samtöluyfirlit og greiningarsíðu. Samtöluyfirlitið sýnir samantektarreiti, upplýsingar um bankareikninga, myndrit og tengdar upplýsingar. Síðan Greiningar notar getu Microsoft Power BI til að sýna myndefni sem tengjast stöðum bankareikninga.
author: saraschi2
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 18171dd17165268fe0f7ac0cf7b3b225f679b9b6b7aeafb7789e837059cf5d79
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755715"
---
# <a name="bank-management-workspace"></a>Vinnusvæði bankakerfis

[!include [banner](../includes/banner.md)]

Vinnusvæðið **Bankakerfi** birtir upplýsingar sem tengjast bankareikningum fyrirtækis. Í þessu vinnusvæði er yfirlitið **Samtölur** og síðan **Greiningar**. Yfirlitið **Samtölur** sýnir samantektarreiti, upplýsingar um bankareikninga, myndrit og tengdar upplýsingar. Síðan **Greiningar** notar getu Microsoft Power BI til að sýna myndefni sem tengjast stöðum bankareikninga.

## <a name="summary-view"></a>Samtöluyfirlit

### <a name="summary"></a>Samantekt

Reitirnir í hlutanum **Samantekt** sýna yfirlit yfir bankareikninga og veita skjótan aðgang að þeim síðum sem oftast eru notaðar. Upplýsingar um bankaafstemmingu eru bundnar við virkni ítarlegrar bankaafstemmingar. Upplýsingar eru aðeins í boði fyrir þá bankareikninga þar sem valmöguleikinn **Ítarleg bankaafstemming** er stilltur á **Já** á síðunni **Bankareikningur**. Hægt er að flytja rafrænar bankaskrár bankareikninga fyrir alla lögaðila úr hlutanum **Samantekt**.

### <a name="bank-accounts"></a>Bankareikningar

Hver bankareikningur lögaðila er sýndur með spjaldi í hlutanum **Bankareikningar**. Núverandi staða er sýnd og hægt er að kafa niður í færslurnar sem mynda heildarstöðuna. Í upphæðinni í **Færslur á millilykil** er einnig hægt að kafa niður í færslurnar sem mynda heildarupphæðina. Færslur á millilykil eru allar færslur í bið sem hafa verið bókaðar með milliaðgerðum, en hafa ekki enn verið afstemmdar. Upphæðin í **Ógreidd staða** er núverandi staða að frádregnum færslum á millilykil eða færslum í bið.

Spjaldið sýnir einnig hvenær bankareikningurinn var síðast afstemmdur. Þessar upplýsingar birtast aðeins ef ítarleg bankaafstemming er virkjuð fyrir bankareikninginn.

### <a name="balance"></a>Efnahagur

Myndritið **Staða** sýnir annaðhvort sögulegar stöðuupplýsingar fyrir bankareikninginn sem er valinn í hlutanum **Bankareikningar** eða samantekt á sögulegum stöðuupplýsingum fyrir alla bankareikninga lögaðilans. Þessar upplýsingar eru tiltækar fyrir ýmis tímabil, núverandi viku, núverandi mánuð, núverandi ár, síðustu fimm ár og öll tímabil (saga bankareiknings frá upphafi). 

Sé verið að skoða myndritið **Staða** fyrir einn bankareikning birtast sögulegar stöðuupplýsingar í gjaldmiðli bankareikningsins. Sé verið að skoða myndritið fyrir alla bankareikninga lögaðilans birtast sögulegar stöðuupplýsingar í bókhaldsgjaldmiðli.

Upplýsingar um hvenær gögn voru síðast uppfærð birtast efst í myndritinu. Hægt er að uppfæra gögn eftir þörfum.

### <a name="related-information"></a>Tengdar upplýsingar

Úr hlutanum **Tengdar upplýsingar** er hægt að opna síðuna **Almenn færslubók** til að framkvæma bankamillifærslur. Einnig er á fljótlegan hátt hægt að opna síðurnar **Bankafærslur** og **Færslur á millilykil**.

## <a name="analytics-view"></a>Greiningaryfirlit

Síðan **Greiningar** hefur að geyma mikilvæga mælikvarða um bankareikninga í núverandi fyrirtæki. Eftirfarandi myndræn framsetning er tiltæk á síðunni:

-   Heildarupphæð bankainnistæðu í gjaldmiðli kerfisins
-   Staða eftir lögaðila
-   Raunstaða samanborið við áætlaða stöðu dagsins í gjaldmiðli bankareikningsins
-   Staða eftir bankareikningi
-   Staða eftir gjaldmiðlum

Hægt er að skoða bankagreiningu fyrir öll fyrirtæki á vinnusvæðinu **Yfirlit yfir reiðufé - öll fyrirtæki**. Frekari upplýsingar má finna á [Yfirlit yfir reiðufé Power BI efni](Cash-Overview-Power-BI-content.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]