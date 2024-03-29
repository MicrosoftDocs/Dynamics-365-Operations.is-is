---
title: Hlaupandi meðaltal
description: Hlaupandi meðaltal er kostnaðarútreikningur sem byggist á meðaltalsreglunni, þar sem kostnaður birgða breytist ekki á meðan innkaupakostnaður gerir það. Mismunurinn er eignfærður og byggir á hlutfallsútreikningi. Eftirstandandi upphæð er skráð sem kostnaður.
author: JennySong-SH
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0be72c8ba3c123300be83513531d2f805dc8f5e3
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676104"
---
# <a name="moving-average"></a>Hlaupandi meðaltal

[!include [banner](../includes/banner.md)]

Hlaupandi meðaltal er kostnaðarútreikningur sem byggist á meðaltalsreglunni, þar sem kostnaður birgða breytist ekki á meðan innkaupakostnaður gerir það. Mismunurinn er eignfærður og byggir á hlutfallsútreikningi. Eftirstandandi upphæð er skráð sem kostnaður.

Við notkun hlaupandi meðaltals er birgðajöfnun og birgðamerkingar ekki studdar. Birgðalokun hefur ekki áhrif á vörur með hlaupandi meðaltal sem flokk birgðalíkana og hún myndar ekkert uppgjör milli færslna.

Eftirfarandi eru forkröfur þegar hlaupandi meðaltal kostnaðar er notað sem aðferð kostnaðarútreiknings.

1. Á síðunni **Vörulíkanaflokkar** seturðu upp vörulíkanaflokk sem hefur **Hlaupandi meðaltal** valið í reitnum **Birgðalíkan**.

    > [!NOTE]
    > Sjálfgefið er að þegar **hlaupandi meðaltal** er valið eru reitirnir **Bóka efnislegar birgðir** og **Bóka fjárhagslegar birgðir** einnig valdir.

1. Á síðunni **Bókun** úthlutarðu lyklum á lyklana **Verðmunur á hlaupandi meðaltali**. Notaðu lykilinn **Verðmunur á hlaupandi meðaltali** þegar kostnaður hefur verið gjaldfærður hlutfallslega. Þetta kemur fram í eftirfarandi tveimur aðstæðum:
    - Það er mismunur á kostnaði á innkaupakvittun og innkaupareikningi vegna þess að það er mismunur milli upprunalegs birgðamagns og núverandi lagerbirgða.
    - Færslurnar færa birgðirnar úr neikvæðu í núll og það er mismunur á milli færslukostnaðar og núverandi hreyfanlegs meðalkostnaðar.

1. Á síðunni **Bókun** skaltu úthluta lyklum á **Kostnaðarendurmat á hlaupandi meðaltali** á flipanum **Birgðir**. Þú notar **Kostnaðarendurmat á hlaupandi meðaltali** þegar þú vilt leiðrétta lykil hlaupandi meðaltals vöru í nýtt einingarverð.

1. Á síðunni **Útgefnum afurðum** skal úthluta vörulíkanaflokk hlaupandi meðaltals á afurðina.

    > [!NOTE]
    > Birgðalokunarferlið lokar aðeins reikningstímabilinu. Það hefur ekki áhrif á afurðir sem hafa hlaupandi meðaltal úthlutað sem vörulíkanaflokk.

## <a name="convert-to-the-moving-average-costing-method"></a>Umbreyta í kostnaðaraðferð hlaupandi meðaltals

Hægt er að umbreyta afurðum til að nota hlaupandi meðaltal birgðamatsaðferðar. Þessi gerð af umreikningi er yfirleitt gerð við lok árs, eftir að síðasta mánuði gildandi árs er lokað. Það er gert með því að nota núgildandi kostnaðarlíkan afurðarinnar. Hægt er að breyta kostnaðaraðferð birgða úr aðferð kostnaðarútreiknings sem er byggð á meðalkostnaði eða stöðluðum kostnaði í aðferð sem er byggð á hlaupandi meðaltali.

Ef aðferð kostnaðarútreiknings er breytt úr aðferð staðalkostnaðar í aðferð hlaupandi meðaltals verður að ljúka eftirfarandi verkum:

1. Gera leiðréttingar til að fá birgðamagn og gildi niður í 0 (núll).
1. Þegar birgðavirði og magn er 0 (núll) er vörulíkanaflokknum breytt í hlaupandi meðaltal.
1. Gera leiðréttingar til að fá magn og virði aftur inn í birgðir.

Ekki er hægt að breyta aðferð birgðakostnaðar úr hlaupandi meðaltali í Fyrst inn, Fyrst út (FIFO) aðferð, Síðast inn, Fyrst út (LIFO) aðferð eða aðferð vegins meðaltals.

> [!NOTE]
> Umbreyting úr stöðluðum kostnaði yfir í hlaupandi vegið meðaltal er handvirk ferli.

Eftirfarandi dæmi skýra áhrif þess að nota aðferð kostnaðarútreiknings hlaupandi meðaltals: Skilgreiningarnar eru fjórar:

- Innkaupapöntun og mismunur hlutfallslega gjaldfærðs kostnaðar
- Hlaupandi meðaltal afurða- og birgðaleiðréttingar
- Hlaupandi meðaltal með framleiðslu
- Hlaupandi meðaltal með bakfærslu

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Innkaupapöntun og mismunur hlutfallslega gjaldfærðs kostnaðar

Með hlaupandi meðaltali ákvarðast kostnaður afurðarinnar af innhreyfingum innkaupapantana. Þegar reikningur innkaupapöntunar er bókaður, ef mismunur er á kostnaði milli innkaupakvittunar og innkaupareiknings, er mismunurinn hlutfallslega leiðréttur í gildandi afurðir á lager og upphæðin sem eftir er gjaldfærð.

Í þessu dæmi er innkaupapöntun stofnuð og móttekin á einn kostnað og innkaupareikningurinn er bókaður með annan kostnað.

1. Stofna innkaupapöntun fyrir magnið 2 og einingarverð 10,00.
1. Stofna innkaupakvittun afurðar.
1. Stofna innkaupapöntun fyrir magnið 1 og einingarverð 10,00.
1. Stofna innkaupapöntun fyrir magnið 2 og einingarverð 12,00.

Mismunur í einingarverði, 2,00, er bókaður á lykilinn Verðmunur á hlaupandi meðaltali þegar innkaupareikningur er bókaður. Ástæðan er að afurðirnar tvær voru keyptar fyrir kostnaðinn 20,00. Önnur afurðanna var seld fyrir einingarverðið 10,00. Innkaupareikningurinn var bókaður með einingarverðinu 12,00 með magninu 2. Ekki er hægt að bóka einingarverð afurðar á 14,00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Hlaupandi meðaltal afurða- og birgðaleiðréttingar

Ef nauðsynlegt er að leiðrétta kostnað hlaupandi meðaltals afurðar eru leiðréttingar á birgðum leyfðar frá og með deginum í dag. Ekki er hægt að bakfæra birgðaleiðréttingu til að leiðrétta kostnað hlaupandi meðaltals afurðar. Ekki er hægt að hafa kostnaðarflæði í gegnum síðari færslur.

Í þessu dæmi er kostnaður hlaupandi meðaltals leiðréttur fyrir afurð.

1. Velja afurð sem á að leiðrétta kostnað hlaupandi meðaltals fyrir. 

 > [!NOTE]
 > Síðan **Endurmat á hlaupandi meðaltali** kannar tiltækar birgðir afurðar. Valin afurð hefur bókaða magnið 1, bókaða gildið 12,00, bókaðan einingarkostnað 12,00 og einingakostnaðinn 12,00.
    
1. Uppfærðu reitinn **Einingarkostnaðar** í 16,00. Kerfið reiknar út eftirstandandi reitina.
1. Leiðréttingin eru bókuð.

> [!NOTE]
> Aðeins er hægt að leiðrétta kostnað hlaupandi meðaltals frá og með deginum í dag.

Á síðunni **Jafnanir fylgiskjals** er hægt að sjá leiðréttinguna 4,00 bókaða á lykilinn Kostnaðarendurmat á hlaupandi meðaltali.

## <a name="moving-average-with-production"></a>Hlaupandi meðaltal með framleiðslu

Hlaupandi meðaltal styður framleiddar vörur. Ef ætlunin er að nota hlaupandi meðaltal í vinnsluumhverfi skaltu velja **Nota áætlað kostnaðarverð** á síðunni **Færibreytur framleiðslustýringar**. Þetta þýðir að kostnaðarverð er reiknað á meðan mat er notað í stað raunverulegs kostnaðarverðs útreikninga uppskrifta.

## <a name="moving-average-with-a-backdated-transaction"></a>Hlaupandi meðaltal með bakfærslu

Bakfærðar færslur eru úthlutaðar á gildandi kostnað hlaupandi meðaltals og efnislegt magn afurðarinnar er uppfært en kostnaður hlaupandi meðaltals verður ekki fyrir áhrifum. Í þessu dæmi um hlaupandi meðaltal er bakfærsla bókuð fyrir afurð hlaupandi meðaltals.

1. Stofnaðu birgðaleiðréttingu fyrir afurð hlaupandi meðaltals fyrir magn 1 og kostnaðinn 20,00.
1. Saga birgðafærslna fyrir afurðina er svipuð eftirfarandi:
    - Birgðafærsla 1, kostnaður 16,00, bókunardagsetning 15. janúar og færsludagsetning 15. janúar.
    - Birgðaleiðrétting 1, kostnaður 20,00, bókunardagsetning 1. janúar og færsludagsetning 15. janúar.
1. Bókaðu leiðréttinguna.

Á síðunni **Birgðafærslur** er hægt að sjá að 4,00 er gjaldfært þar sem gildandi hlaupandi meðaltal afurðarinnar er 16,00. Hægt er að bóka aftur í tímann en mismunur á kostnaði er gjaldfærður, svo að kostnaður hlaupandi meðaltals verður ekki fyrir áhrifum.

## <a name="negative-inventory-balances"></a>Neikvæð birgðastaða

Færslur eru meðhöndlaðar með ólíkum hætti, allt eftir því hvort nýtt magn á lager eftir færsluna er neikvætt, núll eða jákvætt.

### <a name="new-balance-is-negative-or-zero"></a>Ný staða er neikvæð eða núll

Ef nýja lagerbirgðamagnið er neikvætt eða núll er færslan kostnaðarstillt í núgildandi meðalkostnaði. Ef mismunur er á innkaupsverði og núverandi meðalkostnaði er það bókað á **Verðmunur á hlaupandi meðaltali**.

### <a name="new-balance-is-positive"></a>Ný staða er jákvæð

Ef nýja lagerbirgðamagnið er jákvætt eftir færsluna er færslunni skipt í tvo hluta og kostnaður verður mismunandi eins og tekið er saman í eftirfarandi töflu.

| Hluti | lýsing |
|---|---|
| Magn úr neikvæðu í núll | Birgðir notast við núgildandi kostnaður hlaupandi meðaltals á vörunni fremur en færslukostnað fyrir þann hluta af innhreyfingarmagninu sem eykur lagerbirgðastöðu úr neikvæðu í núll. Mismunurinn milli færslukostnaðar og kostnað hlaupandi meðaltals er bókaður í **Verðmunur á hlaupandi meðaltali**. |
| Magn úr núll í jákvæða stöðu | Birgðir nota færslukostnað fyrir þann hluta af innhreyfingarmagninu sem eykur lagerstöðu úr núll í jákvæða.                                                  |

## <a name="inventory-value-report"></a>Virðisskýrsla birgða

Í þessu dæmi um hlaupandi meðaltal er birgðavirðisskýrsla prentuð til að styðja gildandi útreikning hlaupandi meðaltals fyrir afurð. Birgðavirðisskýrslan getur prentað færslur í tímaröð, ásamt kostnaði við að styðja kostnaðarútreikning hlaupandi meðaltals afurðar. Skýrslan birtir kostnað hlaupandi meðaltals fyrir afurðina. Í svarglugganum **Birgðavirðisskýrslur** gerir dagsetningabil kleift að velja **Færslutími** eða **Bókunardagsetning** til að flokka skýrsluna eftir. Valkosturinn **Bókunardagsetning** er hvernig skýrslan er venjulega prentuð. Valkosturinn **Færslutími** er raunveruleg dagsetning þegar færslan er skráð og kostnaður hlaupandi meðaltals fyrir afurðina er uppfærður. Hægt er að prenta birgðavirðisskýrsluna með því að nota valkostinn **Röðun færslutíma** ef óskað er að finna kostnaðarútreikning hlaupandi meðaltals yfir tíma. Eftirfarandi tafla birtir færslurnar fyrir afurðina sem skýrslan er prentuð þegar valkosturinn **Röðun færslutíma** er notaður.

| Færslutími | Dagsetning         | Færslugerð           | Magn | Upphæð | Meðaleiningarkostnaður |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. október    | Upphafsstaða          | 0        | 0,00   | 0,00              |
| 8. október        | 28. september | Bakfærð innhreyfing          | 1        | 16,00  | 16,00             |
| 3. október        | 3. október    | Innkaupakvittun           | 2        | 20,00  | 12             |
| 5. október        | 5. október    | Sölupöntun                | -1       | -10,00 | 13,00             |
| 7. október        | 7. október    | Innkaupareikningur           |          | 2,00   | 14.00             |
| 8. október        | 8. október    | Færir meðaltal endurmats |          | 4.00   | 16.00             |
|                  | 31. október   | Alls                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Ekki er hægt að afstemma fjárhag með birgðum með því að nota valkostinn **Röðun færslutíma**. Prenta verður skýrsluna með því að nota valkostinn **Bókunardagsetning**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]