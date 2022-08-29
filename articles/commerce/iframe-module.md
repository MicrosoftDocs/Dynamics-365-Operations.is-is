---
title: Iframe-eining
description: Þessi grein fjallar um iframe-eininguna og lýsir því hvernig á að bæta henni við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 248da5132d1a2c6dcf8f246628f969c8a200b26c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269896"
---
# <a name="iframe-module"></a>Iframe-eining

[!include [banner](includes/banner.md)]

Þessi grein fjallar um iframe-eininguna og lýsir því hvernig á að bæta henni við vefsíður í Microsoft Dynamics 365 Commerce.

Iframe-eining býður upp á iframe (ramma innan línu) sem hýsir ytra efni á vefsvæði. Til dæmis er hægt að nota hana til að hýsa YouTube-myndband eða PDF-skráaskoðun á hvaða síðu sem er. 

Iframe-eining krefst markvefsslóðar. Hún hýsir svo efni marksíðunnar innan HTML einingar **iframe**. Ytri vefslóðir verða að vera á heimildarlistanum samkvæmt leiðbeiningum fyrir öryggisreglu um efni vefsvæðis. Fyrir iframe-efni ættu vefslóðir að vera leyfðar með því að nota leiðbeininguna **frame-ancestor**. Frekari upplýsingar er að finna í [Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md).

> [!NOTE]
> iframe-einingin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.13.

Eftirfarandi mynd sýnir dæmi um iframe-einingar sem sýna ytri myndbönd á síðum vefsvæðis.

![Dæmi um iframe-einingar sem sýna ytri myndbönd.](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a>Eiginleikar Iframe-einingar

| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Yfirskrift | Texti | Fyrirsögn einingarinnar. |
| Viðtökuslóð | URL | Vefslóðin sem er hýst í einingunni. |
| Hæð | Númer eða prósentuhlutfall | Hæð einingarinnar, í pixlum eða sem prósenta. Til dæmis verður gildið **100** meðhöndlað sem fjöldi pixla og gildið **100%** verður meðhöndlað sem prósenta. |
| Aria merki | Texti | Hægt er að skilgreina ARIA-merki (Accessible Rich Internet Applications) fyrir aðgengi. |

## <a name="add-an-iframe-module-to-a-page"></a>Bæta iframe-einingu við síðu

Til að bæta iframe-einingu við síðu til að sýna ytra myndband skal fylgja þessum skrefum.

1. Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.
1. Í **Nýtt sniðmát** svargluggi, undir **Nafn sniðmáts**, koma inn **Markaðssetning sniðmát**, og veldu síðan **Allt í lagi**.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.
1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, koma inn **Markaðssetning síða**, og veldu síðan **Næst**.
1. Undir **Veldu sniðmát**, veldu **Markaðssetning sniðmát** þú bjóst til og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu síðuútlit (til dæmis, **Sveigjanlegt skipulag**), og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú þarft að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**. 
1. Í **Aðal** rauf á nýju síðunni, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **iframe** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði einingarinnar skal stilla gildið **Markvefslóð** á ytri vefslóð fyrir myndband.
1. Stillið aðra eiginleika, t.d. **Fyrirsögn** og **Hæð**, eftir því sem þörf krefur.
1. Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.
1. Opnaðu markaðssíðuna á vefsvæðinu þinni. Þú ættir að sjá að myndbandið er sýnt í iframe-einingunni.

> [!NOTE]
> Vegna þess að iframe-einingin hýsir ytra efni verða síðuhöfundar að tryggja að efni sem hýst er innan iframe-einingarinnar brjóti ekki í bága við reglur um takmarkanir á efni á viðkomandi markaði. Ef það er efnisbrot á síðu sem notar iframe-eininguna getur höfundur vefsvæðisins fjarlægt iframe-eininguna með því að opna síðuna í Site builder, velja **Fjarlægðu einingu** í iframe mát rauf, og síðan vista og endurbirta síðuna.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
