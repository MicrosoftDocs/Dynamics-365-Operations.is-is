---
title: Úthluta sniðmáti reiknings með frjálsum texta á viðskiptavin
description: Þetta verk sýnir hvernig á að tengja við sniðmát reiknings með frjáls texti við viðskiptavinar.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fb8a683792051a95b443fac47b4670f37c12cc4b4142ee2290b89ee1845662cf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740099"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Úthluta sniðmáti reiknings með frjálsum texta á viðskiptavin

[!include [banner](../../includes/banner.md)]

Þetta verk sýnir hvernig á að tengja við sniðmát reiknings með frjáls texti við viðskiptavinar. Þetta verk notar USMF sýnigögn fyrirtækið og er ætlaður fyrir notandann sem er ábyrgur fyrir stjórnun og vinnslu viðskiptakröfureikninga.

1. Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í **aðgerðasvæðinu** er smellt á **Reikningur**.
4. Smelltu á **Endurteknir reikningar**. Notið þessa síðu til að úthluta sniðmát reikningur með frjálsum texta til viðskiptavina og tilgreina hve oft reikningar verða send til viðskiptavinarins.  
5. Smelltu á **Nýtt** til að úthluta nýju sniðmáti til viðskiptavinar.
6. Í reitnum **Sniðmát** skal velja það sniðmát reiknings með frjálsum texta sem á að úthluta viðskiptavininum.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
8. Í listanum skal smella á tengilinn í valinni línu.
9. Í ritinn **Upphafsdagur innheimtu** skal slá inn dagsetninguna þegar fyrsti reikningurinn verður búinn til.
10. Í kaflanum **Lok endurtekningar** skal slá inn endurtekna lokadagsetningu.  
    * Veljið eina af eftirfarandi: Engin lokadagsetning – Reikningar verða myndaðir óráðinn tíma þar til sniðmátið er fjarlægð úr viðskiptavinalykli.
    * Lokadagur Víxils – Velja þennan valkostur og færðu inn lokadagsetning sem stofna má reikningur.  
11. Í reitinn **Hámarksheildarupphæð** skaltu slá inn hámarksheildarupphæð sem reikningsmyndun stöðvast eftir. Færa inn hámarksheildarupphæð sem hægt er að ná með völdu sniðmáti. Til dæmis, ef fært er inn 1000,00 og mynda mánaðarlegar reikninga fyrir 100,00 hverja reikninga mun stöðva myndun sína eftir að tíunda reikningurinn er myndaður.  
12. Í kaflanum **Mynda endurtekna reikninga með því að nota sjálfgefin gildi úr** skal velja annaðhvort sniðmát reiknings með frjálsum texta eða viðskiptavinalykil. Velja hvort eigi að nota sniðmát textareiknings eða reikning viðskiptavinar til að ákvarða sjálfgefin gildi fyrir tungumál, bókun forstillingu, vsk-flokk, vsk-flokkur vöru, listakóði, land/svæði fyrir afhendingu, gjaldmiðill, greiðsluskilmála, greiðslumáta, greiðsluskilgreiningar, greiðsluáætlun, staðgreiðsluafsláttur, fjárhagsvíddir og gíróseðils þegar reikningar eru stofnaðir.  
13. Í reitinn **Endurtekningarmynstur** skal velja endurtekningarmynstrið.
    + Daglega – veldu þennan valkost og færðu inn fjölda daga í reitnum Eftir Til dæmis, ef fært er inn 15 er reikningurinn verður myndaður 15 daga fresti fyrir þennan viðskiptavin.
    + Vikulega– veldu þennan valkost og færðu inn fjölda vikna í reitnum Eftir Til dæmis, ef fært er inn 2 er reikningurinn verður myndaður á tveggja vikna fresti fyrir þennan viðskiptavin.
    + Mánaðarlega – veldu þennan valkost og færðu inn fjölda mánaða í reitnum Eftir Til dæmis, ef fært er inn 6 er reikningurinn verður myndaður á sex mánaða fresti fyrir þennan viðskiptavin.
    + Árlega – veldu þennan valkost og færðu inn fjölda ára í reitnum Eftir Til dæmis, ef fært er inn 2 er reikningurinn verður myndaður á tveggja ára fresti fyrir þennan viðskiptavin.  
14. Í reitinn **Eftir** skal slá inn tölu.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]