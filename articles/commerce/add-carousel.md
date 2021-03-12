---
title: Myndaræmueining
description: Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0b4ce8fdb7b598e55db59ddf5a99a0ba46eb6f91
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986005"
---
# <a name="carousel-module"></a>Myndaræmueining

[!include [banner](includes/banner.md)]

Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Myndaræmueining er notuð til að setja margar kynningarvörur (þar með talið rtf-myndir) í myndaræmuborða sem snýst og viðskiptavinir geta skoðað. Til dæmis getur smásali notað myndræmueiningu á heimasíðu til að sýna margar nýjar vörur eða kynningar.

Þú getur bætt innihaldsbálkaeiningum í myndaræmueiningu. Eiginleikar myndaræmueiningarinnar skilgreina síðan hvernig þessar einingar eru birtar.

## <a name="examples-of-carousel-modules-in-e-commerce"></a>Dæmi um myndaræmueiningar í rafrænum viðskiptum

- Hægt er að nota myndaræmu með mörgum kynningareiningum á heimasíðunni.
- Hægt er að nota myndaræmu með mörgum kynningareiningum á vöruupplýsingasíðunni.
- Hægt er að nota myndaræmu á hvaða markaðssíðu sem er til að auglýsa margar kynningar eða vörur.

Eftirfarandi mynd sýnir dæmi um myndaræmueiningu sem er notuð á heimasíðu. Þessi myndaræmueining inniheldur mörg efnissvæði.

![Dæmi um myndaræmueiningu](./media/Hero.PNG)

## <a name="carousel-module-properties"></a>Eiginleikar myndaræmueiningar

| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Sjálfvirk spilun                  | **Satt** eða **Ósatt** | Ef gildi er stillt á **Satt** á breytingin á milli hluta í myndaræmunni sér stað sjálfkrafa. Ef gildi er stillt á **Rangt** eiga engin umskipti sér stað nema viðskiptavinurinn noti lyklaborðið eða músina til að fara frá einum hlut til næsta hlutar. |
| Tími á milli skyggna | Gildi í sekúndum    | Bilið fyrir umbreytingar milli atriða. |
| Umbreytingargerð           | **Renna** eða **Hverfa** | Umskiptaáhrif milli liða. |
| Fela flettingu myndaræmu     | **Satt** eða **Ósatt** | Ef gildi er stillt á **Satt** eru myndaræmuflipinn og raðvísirinn faldir. |
| Leyfa að myndaræmu sé hafnað    | **Satt** eða **Ósatt** | Ef gildið er stillt á **Satt** geta notendur hafnað myndaræmunni. |

## <a name="add-a-carousel-module-to-a-page"></a>Bæta myndaræmueiningu við síðu

Fylgdu þessum skrefum til að bæta myndaræmueiningu við nýja síðu og stilla nauðsynlega eiginleika.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í svarglugganum **Nýtt sniðmát** fyrir neðan undir **Heiti sniðmáts**, slærðu inn **Sniðmát myndaræmu** og smellir síðan á **Í lagi**.
1. Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.
1. Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.  
1. Notaðu sniðmát myndaræmu sem þú varst að búa til til að búa til síðu sem heitir **Myndaræmusíða**.
1. Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu. 
1. Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla skjá**.
1. Undir **Útlínur síðu** bæirðu myndaræmueiningu við gámaeininguna.
1. Bættu innihaldsbálkseiningu við myndaræmueininguna. Stilltu eiginleika innihaldsbálkseiningar með því að veita **Fyrirsögn**, **Tengil**, **Skipulag** og aðra eiginleika.
1. Bæta við og stilla aðra innihaldsbálkseiningu.
1. Stilltu viðbótareiginleika fyrir myndaræmueininguna eins og þú þarft.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Síðan ætti að sýna myndaræmu sem hefur tvær einingar í sér (hetjueining og eiginleikaeining). Þú getur breytt viðbótareiginleikum fyrir myndaræmu-, hetju- og eiginleikaeiningarnar til að ná tilætluðum áhrifum.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Tilboðsborðaeining](add-alert.md)

[Textabálkseining](add-content-rich-block.md)

[Eining fyrir bálk með efni](add-hero-module.md)

[Myndspilaraeining](add-video-player.md)
