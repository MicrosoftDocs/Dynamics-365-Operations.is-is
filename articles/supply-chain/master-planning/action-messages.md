---
title: Aðgerðaboð
description: Aðgerðaboð eru tillaga sem mynduð er í kerfinu til að breyta fyrirliggjandi áætlaðri eða staðfestri pöntun.
author: ChristianRytt
manager: tfehr
ms.date: 10/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.assetid: 52b46d93-7d02-46b5-aad1-9fd08206bf9d
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd9efebbe5cfea1bb2c9beedfea4fa0492040ddc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989769"
---
# <a name="action-messages"></a>Aðgerðaboð

[!include [banner](../includes/banner.md)]

Aðgerðaboð eru tillaga sem mynduð er í kerfinu til að breyta fyrirliggjandi áætlaðri eða staðfestri pöntun.

## <a name="introduction"></a>Inngangur

Útreikningur aðalröðunar myndar aðgerðaboð sem viðbrögð við breyttum þörfum. Til dæmis gæti sendingardagsetningu eða magn hafa verið breytt í sölupöntun sem innkaupapöntun hefur þegar verið stofuð fyrir til að uppfylla eftirspurnina. Í þessu tilfelli eru ein eða fleiri aðgerðaboð mynduð af útreikningi aðalröðunar til að uppfæra innkaupapöntunina. Þú ákveður hvort framkvæma eigi ráðlagðar breytingar.

Hægt er að skilgreina hvernig aðgerðaboðin eru reiknuð fyrir þekjuhóp sem hægt er að tengja við vöru.

## <a name="select-action-messages"></a>Skoða aðgerðarboð

Á síðunni **Þekjuflokkar** er hægt að velja aðgerðaboð sem óskað er eftir að kerfið myndi, aðgerðaboð og þekjuflokka eða vörur sem skilaboðin skulu notuð við. Hægt er að velja eftirfarandi aðgerðaboð:

| Skilaboð             | Lýsing                                                                                                                                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Flýta**         | Ef þessi boð eru valin myndar kerfið aðgerðaboð, ef þörf krefur, til að færa pantanir á fyrri dagsetningar. Í reitnum **Fyrirframgreiðsla** er einnig hægt að tilgreina hámarksfjölda daga sem mega líða á milli innhreyfinga og úthreyfinga án ítarlegra aðgerða. |
| **Fresta**        | Ef þessi boð eru valin myndar kerfið aðgerðaboð, ef þörf krefur, til að færa pantanir á seinni dagsetningar. Í reitnum **Mörk frestunaraðgerða** er einnig hægt að tilgreina hámarksfjölda daga sem mega líða á milli innhreyfinga og úthreyfinga án frestunaraðgerða.       |
| **Lækka**        | Ef þessi skilaboð eru valin þarf að draga úr framleiðslupöntunum, innkaupapöntunum eða öðrum innhreyfingum til að forðast umfram birgðastig.                                                                                                   |
| **Hækka**        | Ef þessi skilaboð eru valin þarf að auka framleiðslupantanir, innkaupapantanir eða aðrar innhreyfingar til að forðast skortstöðu í birgðum.                                                                                                    |
| **Afleiddar aðgerðir** | Ef þessi boð eru valin eru aðgerðaskilaboð stofnuð fyrir afleiddar þarfir, t.d. aðgerðir fyrir íhlutapantanir sem til að uppfylla framleiðslu.                                                                                                   |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]