---
title: Setja upp og vinna með endurtekna reikninga
description: Í þessari grein er því lýst hvernig endurtekinn reikningur er sett upp og unnið. Þú getur notað endurtekinn reikningur ef þú þarft að senda viðskiptavinur reikning fyrir sama upphæð reglulega.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: roschlom
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b155d163c57f3c917b4d87fae7cbd737e7c45fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971604"
---
# <a name="set-up-and-process-recurring-invoices"></a>Setja upp og vinna með endurtekna reikninga

[!include [banner](../includes/banner.md)]

Í þessari grein er því lýst hvernig endurtekinn reikningur er sett upp og unnið. Þú getur notað endurtekinn reikningur ef þú þarft að senda viðskiptavinur reikning fyrir sama upphæð reglulega.

<a name="create-a-recurring-free-text-invoice-template"></a>Stofna sniðmát fyrir endurtekna textareikninga
---------------------------------------------

Til að reikningsfæra viðskiptavini fyrir sömu þjónustu reglulega, verður að skilgreina sniðmát textareiknings sem hægt er að endurnýta til að stofna reikninga. Sniðmátið inniheldur eftirfarandi upplýsingar:

-   Hausupplýsingar, eins og skattaflokk, greiðsluskilmála og greiðsluhátt
-   Línuupplýsingar, eins og í þjónustulýsingu, tekjulykla, einingarverð og reikningsupphæð
-   Gjöld fyrir sendingu eða meðhöndlun
-   Dreifingar fjárhagsupphæða með fjárhagsvíddaupplýsingum, eins og kostnaðarstöðum og viðskiptaeiningum

Í rauninni er verið að stofna heilan reikning og vista hann sem sniðmát. Hægt er að setja upp sniðmát sem nota síðuna **Endurteknir reikningar**.

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a>Úthluta viðskiptavini sniðmáti textareiknings og færa inn upplýsingar um endurtekningu
Eftir að sniðmát er stofnað, verður að úthluta sniðmáti til viðskiptavina sem óskað er að reikningsfæra. Að auki þarf að tilgreina hvenær og hversu oft reikningurinn verður notaður. Sniðmátum er hægt að úthluta á flipanum **Reikningur** á síðunni **Viðskiptavinir**. Bættu sniðmátinu á listanum og uppfærðu eftirfarandi upplýsingar:

-   Upphafsdagsetningin og hugsanlega lokadagsetningin fyrir endurtekinn reikning
-   Tíðni endurtekinnar reikningsreglu (t.d. daglega eða einu sinni í mánuði)
-   Hámarksupphæð innheimtu (ef þessara upplýsinga er krafist)

Viðskiptavinur getur haft mörg sniðmát sem hafa mismunandi tíðnir.

## <a name="generate-the-recurring-invoices"></a>Búa til endurtekna reikninga
Á síðunni **Endurteknir reikningar** er verk sem vinnur úr endurteknum reikningum. Þú tilgreinir dagsetningu reiknings og sniðmát til að mynda reikninga úr. Reikningar verða myndaðir og úthlutað á eitt kenni endurtekningar fyrir hvern flokk af reikningum sem eru unnir.

<a name="post-recurring-free-text-invoices"></a>Bóka endurtekna textareikninga
---------------------------------

Eftir að endurteknir reikningar eru búnir til birtast kenni endurtekinna reikninga í bókunarverki á síðunni **Endurteknir reikningar**. Hægt er að skoða alla reikninga fyrir kenni endurtekningar með því að smella á tengilinn. Við endurskoðun reikninga fyrir kenni endurtekningar er hægt að eyða einstökum reikningum. Endurtekningarstillingar viðskiptavinar verða endurstilltar fyrir sniðmátið, þannig að hægt er að endurmynda það síðar. Hægt er að bóka einn, marga eða alla reikninga fyrir endurtekningu. Ef verkflæði eru virkjuð þarf að smella á **Senda** áður en hægt er að bóka reikninga.

<a name="print-recurring-free-text-invoices"></a>Prenta endurtekna textareikninga
----------------------------------

Eftir að endurteknir reikningar hafa verið bókaðir er hægt að prenta reikningana úr listasíðu textareikningsins. Hægt er að prenta reikninga sem eru valdar, eða hægt er að velja bil reikninga sem á að prenta.



