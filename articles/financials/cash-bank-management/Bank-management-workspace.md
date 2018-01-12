---
title: "Vinnusvæði bankakerfis"
description: "Í þessu efnisatriði er að finna upplýsingar um vinnusvæði bankakerfis. Þetta vinnusvæði sýnir upplýsingar sem tengjast bankareikningum fyrirtækis og felur í sér samtöluyfirlit og greiningarsíðu. Samtöluyfirlitið sýnir samantektarreiti, upplýsingar um bankareikninga, myndrit og tengdar upplýsingar. Greiningarsíðan notar virkni Microsoft Power BI til að birta myndræna framsetningu á stöðu bankareikninga."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5d9f9aab56441a7ecd2407b5571de77ece2ab3f
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---
# <a name="bank-management-workspace"></a>Vinnusvæði bankakerfis

Vinnusvæðið **Bankakerfi** birtir upplýsingar sem tengjast bankareikningum fyrirtækis. Í þessu vinnusvæði er yfirlitið **Samtölur** og síðan **Greiningar**. Yfirlitið **Samtölur** sýnir samantektarreiti, upplýsingar um bankareikninga, myndrit og tengdar upplýsingar. Síðan **Greiningar** notar virkni Microsoft Power BI til að birta myndræna framsetningu á stöðu bankareikninga.

## <a name="summary-view"></a>Samtöluyfirlit

### <a name="summary"></a>Samantekt

Reitirnir í hlutanum **Samantekt** sýna yfirlit yfir bankareikninga og veita skjótan aðgang að þeim síðum sem oftast eru notaðar. Upplýsingar um bankaafstemmingu eru bundnar við virkni ítarlegrar bankaafstemmingar. Upplýsingar eru aðeins í boði fyrir þá bankareikninga þar sem valmöguleikinn **Ítarleg bankaafstemming** er stilltur á **Já** á síðunni **Bankareikningur**. Hægt er að flytja rafrænar bankaskrár bankareikninga fyrir alla lögaðila úr hlutanum **Samantekt**.

### <a name="bank-accounts"></a>Bankareikningar

Hver bankareikningur lögaðila er sýndur með spjaldi í hlutanum **Bankareikningar**. Núverandi staða er sýnd og hægt er að kafa niður í færslurnar sem mynda heildarstöðuna. Í upphæðinni í **Færslur á millilykil** er einnig hægt að kafa niður í færslurnar sem mynda heildarupphæðina. Færslur á millilykil eru allar færslur í bið sem hafa verið bókaðar með milliaðgerðum, en hafa ekki enn verið afstemmdar. Upphæðin í **Ógreidd staða** er núverandi staða að frádregnum færslum á millilykil eða færslum í bið.

Spjaldið sýnir einnig hvenær bankareikningurinn var síðast afstemmdur. Þessar upplýsingar birtast aðeins ef ítarleg bankaafstemming er virkjuð fyrir bankareikninginn.

### <a name="balance"></a>Efnahagur

Myndritið **Staða** sýnir annað hvort sögulegar stöðuupplýsingar fyrir bankareikninginn sem er valinn í hlutanum **Bankareikningar** eða samantekt á sögulegum stöðuupplýsingum fyrir alla bankareikninga lögaðilans. Þessar upplýsingar eru tiltækar fyrir ýmis tímabil, núverandi viku, núverandi mánuð, núverandi ár, síðustu fimm ár og öll tímabil (saga bankareiknings frá upphafi). 

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

Hægt er að skoða bankagreiningu fyrir öll fyrirtæki á vinnusvæðinu **Yfirlit yfir reiðufé - öll fyrirtæki**.

