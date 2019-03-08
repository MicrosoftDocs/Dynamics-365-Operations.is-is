---
title: Breyta eiganda vörusendingabirgða samkvæmt eftirspurn eftir framleiðslu
description: Þessi verklýsing sýnir hvernig á að breyta eiganda vörusendingabirgða úr lánardrottni í þinn lögaðila þegar eftirspurn er til staðar fyrir birgðirnar í framleiðslu.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1324da6996230eb383e2f37d3a133ec35cb0f41
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "319018"
---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a>Breyta eiganda vörusendingabirgða samkvæmt eftirspurn eftir framleiðslu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að breyta eiganda vörusendingabirgða úr lánardrottni í þinn lögaðila þegar eftirspurn er til staðar fyrir birgðirnar í framleiðslu. Þessari breytingu á eignarhaldi er gert með því að stofna og bóka birgðabók eignarhaldsbreytingar. Hægt er að stofna Færslubókarlínur eignarhaldsbreytingar handvirkt eða, eins og sést í þessari skráningu, byggt á fyrirliggjandi framleiðslueftirspurn. Yfirleitt, getur yfirmaður í vinnusal framkvæmt verkið. Hægt er að nota þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn. Ef verið er að nota eigin gögn, skal ganga úr skugga um að vera með eftirfarandi forsendur: heiti birgðabókar sem hefur verið sett upp fyrir breytingu á eignarhaldi birgða, efnislega skráð vara á lager í eigu lánardrottins og ein eða fleiri framleiðslupöntunarlínur fyrir efni. Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="create-an-inventory-ownership-journal"></a>Stofna færslubóka fyrir eignarhald birgða.
1. Fara í Birgðastjórnun > Færslubókarfærslur > Vörur > Eignarhaldsleiðrétting birgða.
2. Smellið á „Nýtt“.
    * Birgðafærslubók fyrir breytingu á eignarhaldi er notuð til að breyta eiganda vörusendingabirgða úr lánardrottni í núverandi lögaðila. Þessari breytingu á eignarhaldi er gert með því að losa lagerbirgðir sem er í eigu lánardrottins og taka á móti þessum birgðum í núverandi lögaðila.  
3. Sláið inn eða veldu gildi í reitnum heiti.
    * Aðeins er hægt að velja heiti birgðabóka sem eru með færslubókargerðina eignarhaldsbreyting.  
4. Smellið á „Í lagi“.
5. Smellið á Aðgerðir.
6. Smelltu á Stofna færslubókarlínur úr framleiðslupöntunum
    * Hægt er að hefja ferlið við breytingu á eignarhaldi með því að spyrjast fyrir um allar framleiðslulínur sem eru með eftirspurn eftir notkun á hráefni.  
7. Veljið valkost í reitnum stöður birgðaúthreyfinga sem taka á með.
    * Þessi valkostur gerir þér kleift að sía eftir úthreyfingarstöðu birgðafærslna. Til dæmis er hægt að stofna færslubókarlínur fyrir birgðir hefur tekið efnislegar stöður Tekið til og frátekið.  
8. Útvíkka Færslur til að taka hluta.
    * Í þessum hluta er hægt að beita frekari síun. Til dæmis er hægt að velja ákveðna hráefnisdagsetningu.  
9. Smellið á „Í lagi“.

## <a name="post-the-inventory-ownership-change-journal"></a>Bóka birgðabók eignarhaldsbreytingar.
1. Smellið á „Bóka“.
    * Þegar færslubókin er bókuð, eru birgðir í eigu lánardrottins losaðar með "Breytingu á Eignarhaldi" tilvísun. Birgðum er síðan móttekin sem Á lager með því að nota birgðafærslu sem er uppfærð með innhreyfingarskjali afurðar fyrir innkaupapöntun. Athugið að aðeins eru stofnaðar færslur sem tengjast bókaðri færslubók. Ekki eru stofnaðar neinar væntanlegar birgðafærslur.  
2. Smellið á „Í lagi“.
3. Lokið síðunni.

