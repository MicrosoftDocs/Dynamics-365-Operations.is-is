---
title: Bókun á sölu á netinu og greiðslur
description: Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864154"
---
# <a name="posting-of-online-sales-and-payments"></a>Bókun á sölu á netinu og greiðslur

[!include[task guide banner](../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.

Að birta sölu og greiðslur á netinu er tveggja þrepa ferli.

- Dragðu færslugögn netverslunar inn í HQ.
- Samstilling pantana til að búa til sölupantanir í HQ.

Að draga gögn um smásöluviðskipti á netinu má gera annaðhvort handvirkt með því að keyra P-vinnslu eða með því að búa til endurtekna runuvinnslu.

### <a name="manually-running-the-p-job"></a>Að keyra P-vinnsluna handvirkt

1. Farðu á Öll vinnusvæði > Upplýsingatækni í smásölu.
2. Smelltu á Dreifingaráætlun.
3. Veldu P-0001.
4. Stilltu gagnagrunnshópa rásar, ef þess þarf.
5. Smellt er á Keyra núna.
6. Smella á Já.

### <a name="scheduling-a-recurring-p-job"></a>Tímasetning endurtekinna P-vinnsla

1. Farðu á Öll vinnusvæði > Upplýsingatækni í smásölu.
2. Smelltu á Dreifingaráætlun.
3. Veldu P-0001.
4. Smelltu á Stofna runuvinnslu.
5. Smelltu á Keyra í bakgrunni.
5. Virkjaðu Runuvinnslu.
6. Smelltu á Endurtekning.
7. Velja Valkosturinn enginn valkostur um lokadag.
8. Í Teljarareitnum slærðu inn millibil á milli keyrsla í mínútum. Venjulega myndi þetta vera 5-10.
9. Smellt er á Í lagi.
10. Smellt er á Í lagi.

Hægt er að samstilla pantanir annaðhvort með því að keyra vinnsluna „Samstilla pantanir“ handvirkt eða með því að stofna endurtekna runuvinnslu.

### <a name="manually-running-order-synchronization"></a>Handvirk keyrsla á samstillingu pöntunar 

Fylgdu þessum skrefum til að keyra starfið „Samstilla pantanir“ handvirkt einu sinni.

1. Fara á Öll vinnusvæði > fjárhagur smásöluverslana.
2. Smellt er á Samstilla pantanir
3. Í svæðinu stigveldi Fyrirtækis, veljið 'Smásöluverslanir eftir Svæði'.
    * Annað hvort velja ákveðna verslun á netinu, eða velja hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.  
    * Smella á örina til að bæta vali.  
4. Smella á Keyra í bakgrunni flipanum.
5. Afvirkjaðu Runuvinnslu
6. Smellið á Endurtekning.
7. Veldu valkostinn lok eftir
8. Í reitinn Lok eftir skal slá inn 1.
9. Smellt er á Í lagi.
10. Smellt er á Í lagi.

### <a name="scheduling-recurring-order-synchronization"></a>Tímasetning endurteknar pöntunarsamstillingar

Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu. Þetta ferli notar sýnigögn fyrirtæki USRT.

1. Fara á Öll vinnusvæði > fjárhagur smásöluverslana.
2. Smellt er á Samstilla pantanir
3. Í svæðinu stigveldi Fyrirtækis, veljið 'Smásöluverslanir eftir Svæði'.
    * Annað hvort velja ákveðna verslun á netinu, eða velja hnút ef óskað er að búa til runuvinnslu fyrir hóp verslanir.  
    * Smella á örina til að bæta vali.  
4. Smella á Keyra í bakgrunni flipanum.
5. Virkjaðu Runuvinnslu
6. Smellið á Endurtekning.
7. Velja Valkosturinn enginn valkostur um lokadag.
8. Í Teljarareitnum slærðu inn millibil á milli keyrsla í mínútum. Venjulega myndi þetta vera 2-20
9. Smellt er á Í lagi.
10. Smellt er á Í lagi.

## <a name="data-entities-involved-in-the-process"></a>Gagnaeiningar sem taka þátt í ferlinu

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans
