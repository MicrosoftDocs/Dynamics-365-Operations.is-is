---
title: Reikna og stilla virðisaukaskatt á reikningi lánardrottins
description: Þetta efni útskýrir hvernig leiðrétta skal söluskatt í reikningi lánardrottins í Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2f3521f7bc56659fc6f7a6d47f581ddbfea16523
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139968"
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

