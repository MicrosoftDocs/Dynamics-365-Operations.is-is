---
title: Bókun á sölu á netinu og greiðslur
description: Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2e482b0fb5f2cf67e687c2b278bc5b54ad09839
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802672"
---
# <a name="posting-of-online-sales-and-payments"></a>Bókun á sölu á netinu og greiðslur

[!include [banner](../includes/banner.md)]

Þetta ferli fer í gegnum skilgreiningu og keyrslu runuvinnslu ítrekað til að stofna sölupantanir og greiðslur fyrir færslur smásöluverslunar á netinu.

Að birta sölu og greiðslur á netinu er tveggja þrepa ferli.

- Dragðu færslugögn netviðskipta inn í HQ.
- Samstilling pantana til að búa til sölupantanir í HQ.

Að draga færslugögn á netinu má gera annaðhvort handvirkt með því að keyra P-vinnslu eða með því að búa til endurtekna runuvinnslu.

### <a name="manually-running-the-p-job"></a>Að keyra P-vinnsluna handvirkt

1. Fara í Öll vinnusvæði > Upplýsingatækni Retail og Commerce.
2. Smelltu á Dreifingaráætlun.
3. Veldu P-0001.
4. Stilltu gagnagrunnshópa rásar, ef þess þarf.
5. Smellt er á Keyra núna.
6. Smella á Já.

### <a name="scheduling-a-recurring-p-job"></a>Tímasetning endurtekinna P-vinnsla

1. Fara í Öll vinnusvæði > Upplýsingatækni Retail og Commerce.
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

1. Opna Öll vinnusvæði > Fjármál verslunar.
2. Smellt er á Samstilla pantanir
3. Í svæðinu stigveldi Fyrirtækis, veljið „Verslanir eftir Svæði”.
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

1. Opna Öll vinnusvæði > Fjármál verslunar.
2. Smellt er á Samstilla pantanir
3. Í svæðinu stigveldi Fyrirtækis, veljið „Verslanir eftir Svæði”.
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]