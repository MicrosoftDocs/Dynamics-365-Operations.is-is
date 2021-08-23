---
title: Reikna og stilla virðisaukaskatt á reikningi lánardrottins
description: Þetta efni útskýrir hvernig leiðrétta skal söluskatt í reikningi lánardrottins í Dynamics 365 Finance.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 648d94e895a4941f5f3148134130b3ffa693a9d57e0bb4e236f5d5fb33aca48f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779813"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Reikna og stilla virðisaukaskatt á reikningi lánardrottins

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig leiðrétta skal söluskatt í reikningi lánardrottins. Ef upphaflega upprunaskjal sýnir mismunandi skattupphæðir útreiknaðar, er hægt að leiðrétta þessar upphæðir fyrir bókun. Þetta verkefni notar DEMF-sýnifyrirtækið.

1. Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Reikningabók**.
2. Veljið **Nýtt**.
3. Í reitnum **Nafn** í nýju línunni skaltu velja valkost í fellivalmyndinni.
4. Í aðgerðarúðunni velurðu **Línur**.
5. Í reitnum **Lykill** tilgreinirðu þau gildi sem óskað er eftir.
6. Í reitnum **Reikningur** færirðu inn gildi.
7. Í reitnum **Kredit** skal slá inn tölu.
8. Í reitnum **Mótlykill** skal skilgreina æskileg gildi.
9. Veldu **Virðisaukaskattur**.
10. Í reitnum **Heildarupphæð eiginlegs virðisaukaskatts** færirðu inn tölu.
11. Á flipanum **Leiðrétting** er hægt að leiðrétta vsk-upphæðir fyrir hvern vsk-kóða.
12. Veldu **Endurstilla rauntölur út frá reiknuðum upphæðum**.
13. Veljið **Í lagi**.
14. Veljið **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]