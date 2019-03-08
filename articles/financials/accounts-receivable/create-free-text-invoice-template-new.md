---
title: Stofna sniðmát fyrir reikning með frjálsum texta
description: Þessi aðferð sýnir hvernig á að búa til sniðmát fyrir reikningur með frjálsum texta.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 91f2ec2f8ab21616c6a1b886ee89d6faf84023e4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "310784"
---
# <a name="create-a-free-text-invoice-template"></a>Stofna sniðmát fyrir reikning með frjálsum texta

[!include [banner](../includes/banner.md)]

Í þessari sýnikennslu skal nota USMF sýnifyrirtæki. Þetta ferli er ætluð fyrir notandann sem ber ábyrgð á stjórnun og vinnslu reikninga viðskiptakrafna.

## <a name="create-a-template"></a>Búa til sniðmát

1. Fara í Viðskiptakröfur > Reikningar > Endurteknir reikningar > Sniðmát textareiknings.
    * Notið þessa skjámynd til að stofna sniðmát sem getur innihaldið línur á reikningi, gjöld, sniðmát fyrir dreifingu á fjárhagsupphæð og upplýsingar um fjárhagslykil.  
2. Smellt er á 'Nýtt' til að búa til nýja sniðmát reiknings með frjáls texti.
3. Í reitinn Heiti sniðmáts skal slá inn gildi.
    * 'Sniðmátsheiti' auðkennir á einkvæman hátt sniðmát reikningur með frjálsum texta. Engin tvö sniðmát til að geta haft sama 'sniðmátsheiti'.  
4. Færið inn lýsingu á sniðmát í svæðinu Lýsing..
5. Útvíkka flipanum reikningslína.
6. Færið inn lýsingu á reikningslína í svæðinu Lýsing..
7. Í aðallykill svæðinu, veljið reikning fyrir tekjur.
    * Þú getur valið mótfærslulykil fyrir lánsfé viðskiptavinar fyrir heildarupphæð reiknings í síðunni bókunarregla Viðskiptavinar .  
8. Í reitnum VSK-flokkur skal smella á fellilistahnappinn til að opna leitina.
    * VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.  
9. Í listanum skal smella á tengilinn í valinni línu.
10. Í svæði skattflokkur vöru, velja vsk-flokk vöru fyrir gildandi reikningslínu.
11. Í listanum skal smella á tengilinn í valinni línu.
12. Í svæðinu einingarverð, færa inn eða skoða verð á einingu fyrir reikningslínu
    * Magnið er margfaldað með magnsvæði til að ákvarða endanlegan upphæð línu.  
13. Bæta við nýrri línu við sniðmát reikningur með frjálsum texta.
14. Færið inn lýsingu á reikningslína í svæðinu Lýsing..
15. Í aðallykill svæðinu, veljið reikning fyrir tekjur.
    * Þú getur valið mótfærslulykil fyrir lánsfé viðskiptavinar fyrir heildarupphæð reiknings í síðunni bókunarregla Viðskiptavinar .  
16. Í reitnum VSK-flokkur skal smella á fellilistahnappinn til að opna leitina.
    * VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.  
17. Í listanum skal smella á tengilinn í valinni línu.
18. Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.
    * VSK-flokkur vöru fyrir núgildandi reikningslínuna.  
19. Í listanum skal smella á tengilinn í valinni línu.
20. Færa inn eða skoða fjöldi eininga fyrir reikningslínu
    * Númerið er margfaldað með svæði einingaverðs til að ákvarða endanlegan upphæð reikningslínu.  
21. Færa inn eða skoða verð á einingu fyrir reikningslínu. 
    * Magnið er margfaldað með gildinu á magnsvæði til að ákvarða endanlegan upphæð línu.  
22. Skoða og breyta dreifingar á fjárhagsupphæð fyrir staka línu og allar línur undirstigs.
    * Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig tekjur, skatta eða gjöld verður að teknir með á reikningi með frjáls texti  
23. Uppfæra dreifing á fjárhagsupphæð fyrir Valið reikningslína.
24. Smellið á „Loka“.

## <a name="save-a-free-text-invoice-as-a-template"></a>Vistaðu reikningur með frjálsum texta sem sniðmát
Þú getur líka vistað fyrirliggjandi reikningur með frjálsum texta sem sniðmát. Þegar þú velur Vista í sniðmát á flipanum Reikningur, gefðu upp nafn og lýsingu fyrir sniðmátið. Ef sniðmát með nafninu er þegar til, munt þú sjá tilkynningu um að sniðmát með því nafni sé þegar til. Þú getur ennþá smellt á Í lagi til að skipta því út. 
