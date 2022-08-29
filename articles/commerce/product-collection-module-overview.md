---
title: Afurðasafnseiningar
description: Þessi grein veitir yfirlit yfir vörusöfnunareiningar í Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 05/18/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: 2ad50011e2f4c037a75c8c4b195c728bb58c3b47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269863"
---
# <a name="product-collection-modules"></a>Afurðasafnseiningar

[!include [banner](includes/banner.md)]

Þessi grein veitir yfirlit yfir vörusöfnunareiningar í Microsoft Dynamics 365 Commerce.

Vöruuppgötvun er aðalverkfærið sem smásalar nota til að eiga samskipti við viðskiptavini sína á vefsíðu netverslunar. Afurðasafnseiningar hjálpa smásöluaðilum að byggja upp sannfærandi verslunarupplifun með því að bjóða upp á leiðandi sjónviðmót sem hægt er að nota til að skrifa afurðasöfn á fljótlegan hátt.

Afurðasafnseiningar tákna efnislegar vörur og þjónustu á vefsíðunni. Afurðasafnseining er venjulega tengd við upplýsingasíðu þar sem viðskiptavinir geta keypt vöru eða þjónustu, eða kynnt sér það meira. 

Heimildir fyrir afurðasafni geta verið listar af eftirfarandi fjórum gerðum:

- Ristjórnartlistar yfir afurðir sem eru skilgreindar handvirkt í Dynamics 365 Commerce sem skyldar afurðir fyrir afurð, eða afurðalista
- Reikniritlistar, svo sem listar yfir nýjar, mest seldu eða vinsælar afurðir
- Tilmælalistar sem eru byggðir á vélanámi
- Sérstillingarlistar sem styðja aðlagaðar niðurstöður fyrir viðskiptavini. Viðskiptavinir verða að vera skráðir inn á netverslunarsíðuna til að sjá aðlagaðar niðurstöður. Gestanotendur sjá ekki aðlagaðar niðurstöður. Viðskiptavinir geta afþakkað sérstillingu af [stjórnunarsíðu reikninga](account-management.md).

Eftirfarandi mynd sýnir mismunandi gerðir af afurðasöfnum sem notaðar eru á netverslunarsíðu.

![Dæmi um mismunandi tegundir afurðasafna á netverslunarsíðu.](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Notaðu ávallt afurðasafnseiningar til að sýna hóp af afurðum af svipaðri gerð.

## <a name="product-collection-modules-and-types"></a>Afurðasafnseiningar og gerðir

Eftirfarandi tafla lýsir ýmsum gerðum af afurðasafnseiningum í Dynamics 365 Commerce.

| Afurðasafnseining  | Gerð | Lýsing |
|----------------------------|------|-------------|
| Tegund                   | Tegund | Þessi eining sýnir lista yfir vörur í flokknum eins og hann er skilgreindur í stigveldi flokksins sem smásalinn bjó til fyrir rás. |
| Tengdar afurðir           | Ritill | Þessi eining sýnir lista yfir afurðir sem verslunarstjóri hefur stillt sem tengdar afurðir í Commerce, fyrir þá tengslagerð sem höfundur hefur valið. |
| Leitarniðurstöður             | Leitarfyrirspurn | Þessi gerð afurðasafnseininga sýnir lista yfir vörur sem passa best við leitarfyrirspurnina sem viðskiptavinurinn sló inn. |
| Sérvaldir afurðalistar      | Ritill | Þessi eining sýnir sérsniðna lista sem söluaðilar og ritstjórar hafa búið til í Commerce. |
| Nýjar                        | Reiknirit | Þessi eining sýnir lista yfir nýjustu afurðirnar sem hafa verið flokkaðar í rásir og vörulista. Þessi listi getur sýnt sérsniðnar niðurstöður fyrir innritaðan notanda ef vefhöfundur velur þann valkost. |
| Mest selt               | Reiknirit | Þessi eining sýnir lista yfir vörur sem eru metnar með mesta sölu. Þessi listi getur sýnt sérsniðnar niðurstöður fyrir innritaðan notanda ef vefhöfundur velur þann valkost. |
| Vinsælt                   | Reiknirit | Þessi eining sýnir lista yfir vörur sem skila mestum árangri á tilteknu tímabili. Þessi listi getur sýnt sérsniðnar niðurstöður fyrir innritaðan notanda ef vefhöfundur velur þann valkost. |
| Oft keypt saman | Gervigreind/Vélanám | Þessi eining notar vélnám til að greina kaupmynstur neytenda og mæla með skyldum vörum sem eru oft keyptar ásamt tiltekinni afurð. Þessi listi getur sýnt sérsniðnar niðurstöður fyrir innritaðan notanda ef vefhöfundur velur þann valkost. |
| Fólki líkar einnig við           | Gervigreind/Vélanám | Þessi eining notar vélnám til að greina kaupmynstur neytenda og mæla með vörum sem tengjast tiltekinni afurð. Þessi listi getur sýnt sérsniðnar niðurstöður fyrir innritaðan notanda ef vefhöfundur velur þann valkost. |
| Tillögur fyrir þig              | Gervigreind/Vélanám | Þessi eining notar vélnám til að greina kaupmynstur innritaðs notanda og veita persónulegar ráðleggingar sem eru byggðar á þessum kaupmynstri. Fyrir gestanotanda verður þessi listi felldur saman. |

## <a name="supported-modules"></a>Studdar einingar 

Vörusafnseiningin styður [flýtiskoðunareininguna](quick-view-module.md), sem gerir notendum kleift að skoða afurðarupplýsingar og bæta vörum við körfuna úr síðu vörusafns.

## <a name="add-a-product-collection-module-to-a-category-page"></a>Bæta afurðasafnseiningu við flokksíðu

Til að bæta afurðasafnseiningu við flokksíðu skaltu fylgja þessum skrefum.

1. Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.
1. Í **Búðu til nýja síðu** svargluggi, undir **Nafn síðu**, sláðu inn viðeigandi síðuheiti og veldu síðan **Næst**.
1. Undir **Veldu sniðmát**, veldu sama sniðmát og notað er á sjálfgefna flokkasíðunni þinni og veldu síðan **Næst**.
1. Undir **Veldu skipulag**, veldu síðuútlit (til dæmis, **Sveigjanlegt skipulag**), og veldu síðan **Næst**.
1. Undir **Farið yfir og klárað**, skoðaðu stillingar síðunnar. Ef þú þarft að breyta síðuupplýsingunum skaltu velja **Til baka**. Ef síðuupplýsingarnar eru réttar skaltu velja **Búa til síðu**. 
1. Í **Undirfótur** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Ílát** mát og veldu síðan **Allt í lagi**.
1. Í **Ílát** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Vörusöfnun** mát og veldu síðan **Allt í lagi**.  
1. Í eiginleikaglugganum fyrir afurðasafnseininguna velurðu **Bæta við afurðalista**.
1. Í glugganum **Velja grunnstillingu afurðalista** skal velja gerð listans og uppruna listans og slá inn fjölda vara. Grunnstillið aðra valkosti sem eru í boði fyrir listagerðina. Nánari upplýsingar um listagerðir er að sjá í töflunni sem fylgir. 
1. Veljið **Í lagi**.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

Eftirfarandi tafla sýnir listagerðirnar sem hægt er að velja í valmyndinni **Velja stillingu afurðalista**.

| Gerð                       | Lýsing | Notkun | Samhengi síðu | Tilgreint samhengi | Sérstilling |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Afurðir eftir flokki       | Listi yfir afurðir sem tilheyra tilteknum flokki. Þessi flokkur er ákvörðaður út frá annaðhvort síðasamhengi eða samhengi sem höfundur býður upp á. | Þessa tegund lista er hægt að nota á hvaða síðu sem er (til dæmis heimasíða, flokkasíðu, markaðssíðu eða upplýsingasíðu vöru \[PDP\]) til að kynna ákveðinn vöruflokk. | Flokkur úr samhengi síðunnar, þar sem það er tiltækt (til dæmis flokkasíðu) | Höfundur getur veitt ákveðinn flokk sem samhengi fyrir listann. | Á ekki við |
| Tengdar afurðir           | Listi yfir afurðir sem verslunarstjóri hefur stillt sem tengdar vörur fyrir tengslagerð í Commerce. | Þessi tegund lista er aðallega notuð á PDP, en það er hægt að nota það á hvaða síðu sem er ef móðurvara er til staðar. | Vara af síðunni, tengslagerð (skylda) | Hægt er að velja vöruna í valinu og tengslagerðin er notuð. | Á ekki við |
| Sérvalið                    | Sérsniðinn listi sem söluaðilar og ritstjórar hafa búið til í Commerce. | Auðgaðu flokksíðu, heimasíðuna, kassa- og körfusíður og vörusíður | Á ekki við | Á ekki við | Á ekki við |
| Reiknirit                | <ul><li>**Nýtt** - Listi yfir nýjustu afurðirnar sem hafa verið flokkaðar í rásir og vörulista.</li><li>**Mest selt** - Listi yfir vörur sem eru metnar með mesta sölu.</li><li>**Vinsælt** - Listi yfir vörur sem skila mestum árangri á tilteknu tímabili.</li></ul> | Heimasíða, auðguð flokkasíða og kassa- og körfusíður | Flokkur úr samhengi síðunnar (til dæmis flokkasíðu) | Flokkurinn sem ræðst af höfundi vefsvæðisins | Stutt |
| Oft keypt saman | Listi sem notar vélnám til að greina kaupmynstur neytenda og mæla með skyldum vörum sem eru oft keyptar ásamt tiltekinni afurð. | Þessi tegund af lista á aðeins við um körfusíðuna. | Karfa | Á ekki við | Stutt |
| Fólki líkar einnig við           | Listi sem notar vélnám til að greina kaupmynstur neytenda og mæla með vörum sem tengjast tiltekinni afurð. | Þessi tegund lista er notuð á PDP til að sýna vörur sem aðrir viðskiptavinir hafa keypt. | Vörusamhengi af síðunni | Varan sem er úthlutuð af höfundi vefsvæðisins | Stutt |
| Tillögur fyrir þig              | Listi sem notar vélnám til að ákvarða óskir viðskiptavina. | Þessa tegund lista er hægt að nota á hvaða síðu sem er. | Ekki tiltækt| Ekki tiltækt | Stutt | 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Myndaræmueining](add-carousel.md)

[Eining fyrir bálk með fjölbreytt efni](add-content-rich-block.md)

[Hólfeining](add-container-module.md)

[Kaupgluggaeining](add-buy-box.md)

[Yfirlit yfir afurðarráðleggingar](product-recommendations.md)

[Flýtiskoðunareining](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
