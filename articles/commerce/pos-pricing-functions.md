---
title: Verðaðgerðir á sölustað
description: Þessi grein lýsir ýmsum verð- og afsláttaraðgerðum í Microsoft Dynamics 365 Commerce umsókn um sölustað (POS).
author: boycez
ms.date: 08/12/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-14
ms.openlocfilehash: 210798ac192ee251594ec8ff9d23dab31ec2043e
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473688"
---
# <a name="pricing-functions-in-pos"></a>Verðaðgerðir á sölustað

[!include [banner](includes/banner.md)]

Þessi grein lýsir ýmsum verð- og afsláttaraðgerðum í Microsoft Dynamics 365 Commerce umsókn um sölustað (POS).

The Dynamics 365 Commerce POS forrit býður upp á mikla möguleika sem gerir fyrstu línu starfsmönnum kleift að framkvæma verslunaraðgerðir. Eftirfarandi tafla sýnir verð- og afsláttaraðgerðir sem eru í boði í forritinu.

| Virkni                       | Aðgerðir sölustaðar |
|--------------------------------|----------------|
| Skoða verð                    | [Verðathugun](#price-check) |
| Skoða afslætti                 | [Skoða alla afslætti](#view-all-discounts)<br>[Skoða afslætti sem eru í boði](#view-available-discounts) |
| Hneka verð                | [Verðhnekking](#price-override) |
| Sækja um eða fjarlægja afslátt      | [Línuafsláttarupphæð](#line-discount-amount)<br>[Línuafsláttarprósenta](#line-discount-percent)<br>[Heildarafsláttarupphæð](#total-discount-amount)<br>[Heildarafsláttarprósenta](#total-discount-percent)<br>[Fjarlægja kerfisafslætti úr færslu](#remove-system-discounts-from-transaction)<br>[Endurnota kerfisafslátt](#reapply-system-discounts) |
| Notaðu eða fjarlægðu afsláttarmiða        | [Bæta við afsláttarmiðakóða](#add-coupon-code)<br>[Fjarlægja afsláttarmiðakóða](#remove-coupon-code) |
| Reiknaðu verð og afslætti | [Endurreikna](#recalculate) |

Til að fá upplýsingar um hvernig hægt er að stilla fyrri aðgerðir í POS forritinu og hvort þær styðja ótengda stillingu, sjá [Aðgerðir á netinu og utan nets (POS)](pos-operations.md).

## <a name="price-check"></a>Verðathugun

The **Verðathugun** aðgerð gerir POS notendum kleift að fletta upp fyrirfram stilltum verði fyrir tiltekna vöru.

## <a name="view-all-discounts"></a>Skoða alla afslætti

The **Skoðaðu alla afslætti** aðgerð gerir POS notendum kleift að fletta upp öllum áhrifaríkum kynningum sem eru í gangi í verslunarrásinni. Nánar tiltekið sýnir þessi aðgerð alla afslætti sem passa við eitthvað af eftirfarandi skilyrðum:

- Verðflokkur afsláttarins samsvarar verðflokki verslunarinnar.
- Verðlagshóp afsláttarins er varpað í hlutdeildar- eða vildarkerfi.
- Verðflokki afsláttarins er varpað í vörulista sem er tengd versluninni.

The **Skoðaðu alla afslætti** aðgerð sýnir aðeins afslætti sem keppa ekki við neinn afslátt sem þegar er notaður. Þessi hegðun hjálpar til við að tryggja að ef söluaðili upplýsir viðskiptavin um afslátt og viðskiptavinurinn grípur til nauðsynlegra aðgerða (til dæmis kaupir viðskiptavinurinn einn hlut til viðbótar til að fá 10 prósent afslátt), þá er afslátturinn notaður á færsluna. Afslættir sem byggja á afsláttarmiða eru aðeins sýndir ef **Sæktu um án afsláttarmiðakóða** kveikt er á breytu.

Inni í **Skoðaðu alla afslætti** aðgerð, POS notendur geta leitað að afslætti eftir nafni og lýsingu og þeir geta síað afslátt eftir því hvort þeir þurfa afsláttarmiða.

## <a name="view-available-discounts"></a>Skoða afslætti sem eru í boði

The **Skoða tiltæka afslætti** aðgerð gerir POS notendum kleift að skoða alla afslætti sem gilda fyrir valda línu í færslu eða fyrir alla færsluna. Afslættirnir sem gilda fyrir valda línu innihalda afslætti sem þegar hafa verið notaðir og afslættir sem hafa ekki enn verið notaðir en hægt er að nota (til dæmis, blanda saman afslætti sem krefjast viðbótarvara). Ef viðeigandi afsláttur er tengdur afsláttarmiða þar sem **Sæktu um án afsláttarmiðakóða** kveikt er á breytu getur POS notandinn líka notað **Sækja afsláttarmiða** virka inni í þessari aðgerð til að innleysa afsláttarmiða beint, án þess að þurfa að slá inn eða skanna afsláttarmiða eða strikamerki afsláttarmiða.

## <a name="price-override"></a>Verðhnekking

The **Verðhækkun** aðgerð gerir POS notendum kleift að hnekkja söluverði vöru í viðskiptum. Þessi aðgerð virkar aðeins fyrir vörur sem eru stilltar til að leyfa verðhækkun.

## <a name="line-discount-amount"></a>Línuafsláttarupphæð

The **Línuafsláttarupphæð** aðgerð gerir POS notendum kleift að slá inn afsláttarupphæð fyrir línu í færslu. Þessi aðgerð á aðeins við um afsláttarvörur og virðir þær **Hámarksupphæð línuafsláttar** gildi sem er tilgreint í POS heimildahópnum fyrir notandann.

## <a name="line-discount-percent"></a>Línuafsláttarprósenta

The **Línuafsláttur prósenta** aðgerð gerir POS notendum kleift að slá inn afsláttarprósentu fyrir línu í færslu. Þessi aðgerð á aðeins við um afsláttarvörur og virðir þær **Hámarkslínuafsláttarprósenta** gildi sem er tilgreint í POS heimildahópnum fyrir notandann.

## <a name="total-discount-amount"></a>Heildarafsláttarupphæð

The **Heildarafsláttarupphæð** aðgerð gerir POS notendum kleift að slá inn afsláttarupphæð fyrir færslu. Þessi aðgerð á aðeins við um afsláttarvörur og virðir þær **Hámarksupphæð heildarafsláttar** gildi sem er tilgreint í POS heimildahópnum fyrir notandann. Ef afsláttarupphæðin sem færð er inn fer yfir hámarks heildarafsláttarupphæð er aðgerðin læst og ekkert leyfishnekningarflæði er ræst. Eins og er er ekki hægt að nota heildarafsláttarupphæð á körfu sem inniheldur blöndu af söluvörum og skilavörum.

## <a name="total-discount-percent"></a>Heildarafsláttarprósenta

The **Heildarafsláttur prósenta** aðgerð gerir POS notendum kleift að slá inn afsláttarprósentu fyrir færslu. Þessi aðgerð á aðeins við um afsláttarvörur og virðir þær **Hámarks heildarafsláttarprósenta** gildi sem er tilgreint í POS heimildahópnum fyrir notandann. Ef afsláttarprósentan sem færð er inn fer yfir hámarks heildarafsláttaprósentu er aðgerðin læst og ekkert leyfishnekningarflæði er ræst. Eins og er er ekki hægt að nota heildarafsláttaprósentu á körfu sem hefur blöndu af söluvörum og skilavörum.

## <a name="remove-system-discounts-from-transaction"></a>Fjarlægja kerfisafslætti úr færslu

The **Fjarlægðu kerfisafslátt úr viðskiptum** aðgerð gerir POS notendum kleift að hreinsa alla notaða kerfisafslátta (þar á meðal afsláttarmiða sem byggjast á afsláttarmiða) af færslu. Eftir að þessi aðgerð er framkvæmd byrjar verðlagningarvélin að útiloka kerfisafslátt frá umfangi afsláttarútreiknings. The **Fjarlægðu kerfisafslátt úr viðskiptum** aðgerð fjarlægir ekki handvirkan afslátt.

## <a name="reapply-system-discounts"></a>Endurnota kerfisafslátt

The **Sækja aftur um kerfisafslátt** aðgerð gerir POS notendum kleift að nota aftur kerfisreiknaða afslætti á færslu ef afslættirnir voru fjarlægðir með því að nota **Fjarlægðu kerfisafslátt úr viðskiptum** aðgerð. Eftir að þessi aðgerð hefur verið framkvæmd byrjar verðlagningarvélin að innihalda alla kerfisafslátta í umfangi afsláttarútreiknings.

## <a name="add-coupon-code"></a>Bæta við afsláttarmiðakóða

The **Bæta við afsláttarmiða kóða** aðgerð gerir POS notendum kleift að bæta afsláttarmiða við færslu með því að slá inn afsláttarmiða kóða. Að öðrum kosti geta POS notendur skannað strikamerki afsláttarmiða eða slegið það inn með því að nota talnalyklaborðið á **Viðskipti** skjár.

## <a name="remove-coupon-code"></a>Fjarlægja afsláttarmiðakóða

The **Fjarlægðu afsláttarmiða kóða** aðgerð gerir POS notendum kleift að velja og fjarlægja einn eða fleiri afsláttarmiða sem eru notaðir á færslu.

## <a name="recalculate"></a>Endurreikna

The **Endurreikna** aðgerð gerir POS notendum kleift að kveikja á verðútreikningi á eftirspurn. Þessi aðgerð er nauðsynleg þegar verðlæsing og/eða seinkaður verðútreikningur er virkur og POS notandi vill endurreikna verð og afslætti eftir breytingar á körfu eða pöntunum. The **Endurreikna** aðgerð endurreikur alltaf alla röðina. Það er ekki hægt að nota það til að endurreikna valdar sölulínur. Til að beita handvirkum afslætti á læsta sölulínu í POS verða notendur POS fyrst að nota **Endurreikna** aðgerð til að opna allar sölulínur.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
