---
title: Eignafærslukostir
description: Þetta efnisatriði lýsir mismunandi aðferðum sem eru tiltækar til að stofna eignafærslu.
author: ShylaThompson
ms.date: 02/07/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, PurchCreateOrder
audience: Application User
ms.reviewer: roschlom
ms.custom: 23061
ms.assetid: 338c495b-a4d8-461e-b85b-a83faf673730
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f9cd8846688e6b70f3ac2034caa1a9e3015355e
ms.sourcegitcommit: f9b40df70a77136529fbc790325ed657eb203731
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/20/2021
ms.locfileid: "6645373"
---
# <a name="fixed-asset-transaction-options"></a>Eignafærslukostir

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir mismunandi aðferðum sem eru tiltækar til að stofna eignafærslu.

Þú getur sett upp eign fyrir sameiningu með viðskiptaskuldir, viðskiptakröfur, innkaup og uppruna og fjárhag. Einnig er hægt að flytja vörur í birgðastjórnun á eignir eigi að nota þær vörur innan kerfis.

## <a name="accounts-payable"></a>Viðskiptaskuldir
Hægt er að færa inn eignafærslur í síðunni færslubókarfylgiskjal. Þessa síða er aðeins hægt að opna úr skjámyndinni reikningabók. Einnig er hægt að opna síðuna færslubókarfylgiskjal frá síðu færslubókarsamþykkt reiknings. Í svæðinu mótlykill, veljið eignir. Síðan, í mótlykill reit verður að velja númer eignar. Á flipanum eignir færirðu inn gildi í reitina færslugerð og bók.

## <a name="accounts-receivable"></a>Viðskiptakröfur
Hægt er að færa inn eignafærslur í síðunni reikningur með frjálsum texta.  Veljið línuatriði í síðunni reikningur með frjálsum texta, í hnitanetinu reikningslínur. Smellið á flýtiflipa „Upplýsingar um línur“. Færðu inn eignanúmer og bók fyrir afskráningarfærslu. Fyrir reikninga með valfrjálsum texta er gerð eignafærslunnar alltaf afskráninga - sala.

## <a name="procurement-and-sourcing"></a>Innkaup og aðföng
Hægt er að færa inn eignafærslur í síðunni innkaupapöntun. Færa skal inn allar upplýsingar sem krafist er til að búa til innkaupapöntun og síðan smella á Í lagi. Í síðunni innkaupapöntun, Smellið á flýtiflipa „Upplýsingar um línur“. Síðan skal færa inn upplýsingar um eignina á flipann Eignir. 

Til að bóka kaupfærslu fyrir fyrirliggjandi eign skal tilgreina eignanúmer, bók og færslutegund. Eign er hægt að bóka ef einhvern af þessum upplýsingum vantar. Til að bóka kaupfærslu fyrir nýja eign skal velja valkostinn ný eign? og síðan velja eignaflokk til að úthluta nýrri eign á. Hins vegar eru engin af eignasvæðunum fyrir hendi fyrir línu ef varan er í birgðalíkanaflokki sem notar birgðalíkan staðalkostnaðar. Þar að auki, valkostir sem eru skilgreindar í    síðunni færibreytur eignar ákvarða hvort hægt er að bóka kaupfærslur frá innkaupaeiningum. 

Þegar færslubók innkaupapöntunar eða færslubók birgða til eigna eru notaðar fyrir eignakaup hefur það áhrif á birgðavirðið.

## <a name="general-ledger"></a>Fjárhagur
Allar gerðir eignafærsla má bóka í síðunni almenn færslubók. Einnig er hægt að nota færslubækur í eignum til að bóka eignafærslur.

### <a name="options-for-entering-fixed-asset-transaction-types"></a>Valkostir innfærslu á eignafærslugerðum


| Færslugerð                    | Kerfi                   | Valréttarsamningar                                   |
|-------------------------------------|--------------------------|-------------------------------------------|
| Yfirtaka, leiðrétting kaupa | Eignir             | Eignir, birgðir til eigna   |
|                                     | Fjárhagur           | Almenn færslubók                           |
|                                     | Viðskiptaskuldir         | Reikningabók, Staðfestingarbók reiknings |
|                                     | Innkaup og aðföng | Innkaupapöntun                            |
| Afskrift                        | Eignir             | Eignir                              |
|                                     | Fjárhagur           | Almenn færslubók                           |
| Losun                            | Eignir             | Eignir                              |
| ** **                               | Fjárhagur           | Almenn færslubók                           |
| ** **                               | Viðskiptakröfur      | Reikningur með frjálsum texta                         |

Eftirstöðvar eignar á afskriftartímabili eru ekki uppfærðar þegar færslubókarlína afskriftarfærslugerðar er búin til handvirkt eða flutt inn í gegnum gagnaeiningu. Þetta gildi er uppfært þegar ferli afskriftartillögu er notað til að búa til færslubókarlínu.

Frekari upplýsingar eru í [Samþætting eigna](fixed-asset-integration.md).

### <a name="transactions-that-require-different-voucher-numbers"></a>Færslur sem krefjast mismunandi fylgiskjalsnúmera

Eftirtaldar eignafærslur munu nota mismunandi fylgiskjalsnúmer:

- Viðbótarkaup eru gerð á eign og „vinna upp" afskrift er reiknuð út.
- Eign er skipt.
- Breytur til að reikna afskriftir við förgun er kveikt á og þá er eignin fargað.
- Þjónustudagsetning eignar er fyrir kaupdagsetningu. Þar af leiðandi er leiðrétting afskriftar bókuð.

> [!NOTE]
> Þegar þú færir inn færslur skaltu ganga úr skugga um að allar færslurnar gildi um sömu eignina. Fylgiskjal verður ekki bókað ef það inniheldur fleiri en eina fasta eign, jafnvel þó að reiturinn **Nýtt fylgiskjal** sé stilltur á **Aðeins eitt fylgiskjal** á síðunni **Færslubókaheiti** í fjárhag. Ef þú setur fleiri en eina fasta eign í fylgiskjalið færðu upp skilaboðin „Aðeins má vera ein eignafærsla á hvert fylgiskjal“ og þú munt ekki geta sent fylgiskjalið.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
