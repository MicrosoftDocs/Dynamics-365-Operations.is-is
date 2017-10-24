---
title: "Reglur vöruhúsavinnu"
description: "Vöruhús vinnu reglur stýra hvort vöruhúsavinna sé stofnuð af ferli vöruhúsa í framleiðsluumhverfi, samkvæmt gerð verks, staðsetningu birgða og vöru."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: ec7dd3b91851729e866bc90ca85a118839f9d71d
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="warehouse-work-policies"></a>Reglur vöruhúsavinnu

[!include[banner](../includes/banner.md)]


Vöruhúsavinnureglur í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition stýra hvort vöruhúsavinna sé stofnuð af ferli vöruhúsa í framleiðsluumhverfi, samkvæmt gerð verks, staðsetningu birgða og vöru.

Þessi regla vinnu stýrir því hvort vöruhúsavinnu er stofnað fyrir ferli vöruhúsa í framleiðslu. Setja upp stefnu vinnu með samsetningu **vinnupantanagerðir**, **staðsetningu birgða**, og **afurð**. Til dæmis er afurð L0101 skráð sem lokið á staðsetningu framleiðslufrálags 001. Fullbúin framleiðsluvara er síðar notuð í aðra framleiðslupöntun á staðsetningu frálags 001. Í þessu tilfelli er hægt að setja upp reglu vinnu til að koma í veg fyrir að vinna fyrir fullbúnar vörur frágangur stofnað þegar afurð L0101 tilbúið að staðsetningu framleiðslufrálags 001. Regla vinnu er einstök eining sem lýst hægt að með eftirfarandi upplýsingum:

-   **Vinnuregluheiti**(einkvæmt kenni reglunnar vinna)
-   **Vinnupantanagerðir** og **aðferð fyrir stofnun Vinnu**
-   **Birgðastaðsetningar**
-   **Afurðir**

## <a name="work-order-types"></a>Gerðir vinnupöntunar
Hægt er að velja um eftirfarandi gerðir vinnupöntunar:

-   Frágangur á fullunnum vörum
-   Frágangur aukaafurða og hliðarafurða
-   Tiltekt hráefnis

Í **aðferð fyrir stofnun Vinnu** svæðið hefur gildið **Aldrei**. Þetta gildi gefur til kynna að vinnu regla kemur í veg fyrir vöruhúsavinnu verið stofnuð fyrir valda vinnupöntunargerð.

## <a name="inventory-locations"></a>Birgðastaðsetningar
Velja má á staðsetningu sem reglan vinna á við um. Ef engin staðsetning er tengd vinnureglu vinnureglu ekki eiga við um ferli. Á **Staðsetningar** síðu er einnig er hægt að velja eða hætta við val á vinnu reglu fyrir ákveðna staðsetningu.

## <a name="products"></a>Afurðir
Velja má á vöru sem reglan vinna á við um. Hægt er að nota regluna vinnu allar afurðir eða valdar afurðir.

## <a name="example"></a>Dæmi
Í eftirfarandi dæmi eru tvær framleiðslupantanir, PRD 001 og PRD 00*2*. Framleiðslupöntunin PRD 001 hefur aðgerðar sem nefnist **Samsetningu**, þar sem afurð SC1 verið skráð sem lokið á staðsetningu O1. Framleiðslupöntunin PRD 002 hefur aðgerðar sem nefnist **Málun** og notar afurð SC1 frá staðsetningu O1. Framleiðslupöntunin PRD 002 notar einnig RM1 hráefni úr staðsetningunni O1. RM1 er geymd á staðsetningu vöruhúss BULK-001 og verður tekið til staðsetningu O1 eftir vöruhúsi vinnu fyrir tiltekt hráefnis. Vinna tiltektar er myndað þegar PRD 002 framleiðsla er losuð. 

[![Reglur vöruhúsavinnu](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png) 

Þegar ætlunin er að skilgreina vöruhús regla vinnu á þessu dæmi ætti að íhuga að eftirfarandi upplýsingar:

-   Vöruhúsavinnu fyrir fullbúnar vörur frágangur er ekki áskilin þegar afurð SC1 tilbúið úr framleiðslunni pöntun PRD-001 til staðsetningu O1 er tilkynnt. Þetta er vegna þess að í **Málun** aðgerð fyrir framleiðslupöntun PRD 002 notar SC1 á sama stað.
-   Vinna vöruhús fyrir tiltekt hráefnis er krafist til að flytja RM1 hráefni frá staðsetningu vöruhúss BULK-001 á staðsetningu O1.

Hér er dæmi um vinnu regluna sem hægt er að setja upp, byggðar á þessum atriðum.

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|**Heiti vinnureglu**<br>                 |**Gerðir vinnupöntunar**<br>                               |
| Enginn frágangur 01                         |- Frágangur á fullunnum vörum<br>                           |
|                                         |**Staðsetningar**<br>                                      |
|                                         |- O1   |                                               |
|                                         |**Afurðir** <br>                                      |
|                                         |- SC1                                                  |

Eftirfarandi ferli lýsa nákvæmar leiðbeiningar um hvernig setja á upp reglu vinnu vöruhús fyrir þetta dæmi. Sýnishorn uppsetningar sýnir hvernig tilkynnt framleiðslupöntun sem lokið á staðsetningu sem er ekki númeraplötustýrð eru einnig lýst.

## <a name="set-up-a-warehouse-work-policy"></a>Setja upp reglur vöruhúsavinnu
Ferli vöruhúsa ekki alltaf hafa vöruhús vinnu. Með því að skilgreina vinnustefnu, sem getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði. USMF sýniútgáfu fyrirtækis notað til að stofna þetta ferli. 

SKREF (21)

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| 1.  | Fara í vöruhúsakerfi &gt; Uppsetning &gt; Vinna &gt; Vinnureglur.        |
| 2.  | Smellið á Nýtt.                                                                 |
| 3.  | Í svæðið Vinnu reglu heiti, skrifa 'Engin frágangsvinna‘                    |
| 4.  | Smelltu á Vista.                                                                |
| 5.  | Smelltu á Bæta við.                                                                 |
| 6.  | Í listanum skal merkja valda línu.                                        |
| 7.  | Í Gerð vinnupöntun svæðinu, veljið 'Fullunninna vöru frágangur'.            |
| 8.  | Smelltu á Bæta við.                                                                 |
| 9.  | Í listanum skal merkja valda línu.                                        |
| 10. | Í Gerð vinnupöntun svæðinu, veljið 'Aukaafurða og hliðarafurða frágangur'. |
| 11. | Útvíkka hlutann birgðastaðsetning.                                    |
| 12. | Smelltu á Bæta við.                                                                 |
| 13. | Í listanum skal merkja valda línu.                                        |
| 14. | Í vöruhúsalistanum, sláðu inn "51"                                         |
| 15. | Sláið inn eða veldu '001‘ í staðsetning reitnum.                              |
| 16. | Víkka út hlutann Afurðir.                                               |
| 17. | Í reitnum afurðaval skal velja valið.                         |
| 18. | Smelltu á Bæta við.                                                                 |
| 19. | Í listanum skal merkja valda línu.                                        |
| 20. | Í reitinn Vörunúmer skal slá inn eða veldu L0101.                         |
| 21. | Smelltu á Vista.                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a>Tilkynna framleiðslupöntun sem lokið er á staðsetningu sem ekki númeraplötustýrð
Þessi ferli sýnir dæmi um skýrslugerð sem lokið á staðsetningu sem ekki númeraplötustýrð. Gildandi vinnureglu er skilyrði fyrir þetta verk. Fyrri ferli sýna uppsetningu vinnureglu. 

SKREF (25)

<table>
<tbody>
<tr>
<td colspan="3"><strong>Undirverk: Setja upp staðsetningu úttaks</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Fara á fyrirtækisstjórnun &gt; Tilföng &gt; Tilfangaflokka.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Á listanum, veljið tilfangaflokk 5102</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Smella á Breyta.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Í úttaksvöruhús svæðinu veljið 51.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Í staðsetning úttaks svæðinu sláið inn 001.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Staðsetning 001 ekki númeraplötustýrð staðsetningu. Hægt er að setja upp staðsetningu úttaks ekki númeraplötu aðeins ef gildandi vinnureglu er til fyrir staðsetningarinnar.</td>
</tr>
<tr>
<td colspan="3"><strong>Undirverk: Stofna framleiðslupöntun og skrá sem lokið.</strong></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td>Lokið síðunni.</td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td>Fara í framleiðslustýringar &gt; Framleiðslupantanir &gt; Allar framleiðslupantanir.</td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td>Smella á Ný framleiðslupöntun.</td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td>Í vörunúmer svæðið sláið inn L0101.</td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td>Smellið á Stofna.</td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td>Á Aðgerðasvæðinu skal smellt á framleiðslupöntun.</td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td>Smellt er á Mat.</td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td>Smellt er á Í lagi.</td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td>Smellt er á Byrja.</td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td>Smellt er á flipannAlmennt.</td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td>Veljið ‚Aldrei‘ í reitnum Sjálfvirk uppskriftarnotkun.</td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td>Smellt er á Í lagi.</td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td>Smellið á Bóka sem tilbúið.</td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td>Smellt er á flipannAlmennt.</td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td>Velja skal Já í reitnum leyfa villu.</td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td>Smellt er á Í lagi.</td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td>Í aðgerðasvæðinu er smellt á vöruhús.</td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td>Smellt er á Upplýsingar um vinnu</td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td>Þegar framleiðslupöntunin var skráð sem lokið, engin vinna var mynduð fyrir frágangur. Þetta gerist vegna þess að vinna regla er skilgreind sem kemur í veg fyrir vinnu búnar til þegar afurð L0101 er skráð sem lokið á staðsetningu 001.</td>
</tr>
</tbody>
</table>




