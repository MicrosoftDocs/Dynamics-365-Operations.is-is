--- 
title: "Lykilgögn reiknings í AP kerfið með því að nota færslubókarsamþykkt"
description: "Þessi leiðarvísi fyrir verk sýnir hvernig á að nota komubók til að stofna reikninga og nota síðan færslubókarsamþykkt til að uppfæra kostnaðarlykla."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 048eda77064b6aa3f666e998a8e551d2f7adc385
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a>Lykilgögn reiknings í AP kerfið með því að nota færslubókarsamþykkt

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk sýnir hvernig á að nota komubók til að stofna reikninga og nota síðan færslubókarsamþykkt til að uppfæra kostnaðarlykla.


## <a name="create-and-post-and-invoice"></a>Stofna og bóka og reikningsfæra
1. Fara í Viðskiptaskuldir > Reikningar > Komubók.
2. Smellið á „Nýtt“.
3. Veldu heiti komubókarinnar sem þú vilt nota.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Smellið á Línur til að opna afgreiðslukassann og færa inn kostnaðarlínur.
6. Veljið lánardrottin. Til dæmis færirðu inn eða velur US-104
7. Í reitinn Reikningur skal færa inn gildi.
8. Í reitinn Lýsing skal slá inn gildi.
9. Í reitnum Kredit skal slá inn tölu.
10. Í reitnum Samþykkt skal smella á fellilistahnappinn til að opna leitina.
11. Merkið samþykkjanda og smelltu á Velja til að velja þann samþykkjanda.
12. Smellið á „Bóka“.
13. Lokið síðunni.
14. Lokið síðunni.

## <a name="approve-an-invoice"></a>Samþykkja reikning
1. Fara í Viðskiptaskuldir > Reikningar > Reikningssamþykki.
2. Smellið á „Nýtt“.
3. Veldu heiti færslubókarsamþykkt reiknings sem þú vilt nota.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Smellið á línur til að birta síðu þar sem er hægt að velja reikninga sem á að samþykkja.
6. Veljið Finna Fylgiskjöl til að birta alla reikninga sem eru tilbúnar til samþykkis.
7. Merkja reikninginn sem þú stofnaðir.
8. Smellið á Velja.
    * Fylgiskjala sem valinn er fyrir ofan eru fluttar yfir á þessum lista eftir að þeim var valið.  
9. Smellið á „Í lagi“.
10. Smella á svæðið lykilnúmers til að bæta kostnaðarlykli við reikning.
11. Færið inn lykilnúmer og flipinn við svæðið. Til dæmis færirðu inn 600120.
12. Smellið á „Bóka“.
13. Smellt er á Fylgiskjal til að skoða færslur sem voru bókaðar.
    * Lykill Reiknings sem bíður samþykkist er bakfærður og skipt út fyrir raunverulega kostnaðarlykil.  


