---
title: Stofna sniðmát fyrir reikning með frjálsum texta
description: Þessi aðferð sýnir hvernig á að búa til sniðmát fyrir reikningur með frjálsum texta.
author: abruer
ms.date: 02/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7baa29ad341bdf7ff874bd7f69cf483b7afc075a
ms.sourcegitcommit: 6102f70d4595d01b90afe5b23dfd8ec2ea030653
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182510"
---
# <a name="create-a-free-text-invoice-template"></a>Stofna sniðmát fyrir reikning með frjálsum texta

[!include [banner](../includes/banner.md)]

Í þessari sýnikennslu skal nota USMF sýnifyrirtæki. Þetta ferli er ætluð fyrir notandann sem ber ábyrgð á stjórnun og vinnslu reikninga viðskiptakrafna.

## <a name="create-a-template"></a>Búa til sniðmát

1. Fara í **Viðskiptakröfur > Reikningar > Endurteknir reikningar > Sniðmát textareiknings**.
    * Notið þessa síðu til að stofna sniðmát sem getur innihaldið línur á reikningi, gjöld, sniðmát fyrir dreifingu á fjárhagsupphæð og upplýsingar um fjárhagslykil.  
2. Smellt er á **Nýtt** til að búa til nýja sniðmát reiknings með frjáls texti.
3. Í reitinn **Heiti sniðmáts** skal slá inn gildi.
    * 'Sniðmátsheiti' auðkennir á einkvæman hátt sniðmát reikningur með frjálsum texta. Engin tvö sniðmát til að geta haft sama 'sniðmátsheiti'.  
4. Færið inn lýsingu á sniðmát í svæðinu **Lýsing**.
5. Útvíkka flipanum **Reikningslínur**.
6. Færið inn lýsingu á reikningslína í svæðinu **Lýsing**.
7. Í **Aðallykill** reitinn skal velja reikning fyrir tekjur.
    * Þú getur valið mótfærslulykil fyrir lánsfé viðskiptavinar fyrir heildarupphæð reiknings í síðunni **Bókunarreglur viðskiptavina**.  
8. Í reitnum **VSK-flokkur** skal smella á fellilistahnappinn til að opna leitina.
    * VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.  
9. Í listanum skal smella á tengilinn í valinni línu.
10. Í svæði **Skattflokkur vöru**, velja vsk-flokk vöru fyrir gildandi reikningslínu.
11. Í listanum skal smella á tengilinn í valinni línu.
12. Í svæðinu **Einingarverð** skal færa inn eða skoða verð á einingu fyrir reikningslínu
    * Magnið er margfaldað með svæðinu **Magn** til að ákvarða endanlegan upphæð línu.  
13. Bæta við nýrri línu við sniðmát reikningur með frjálsum texta.
14. Færið inn lýsingu á reikningslína í svæðinu **Lýsing**.
15. Í **Aðallykill** reitinn skal velja reikning fyrir tekjur.
    * Þú getur valið mótfærslulykil fyrir lánsfé viðskiptavinar fyrir heildarupphæð reiknings í síðunni **Bókunarreglur viðskiptavina**.  
16. Í reitnum **VSK-flokkur** skal smella á fellilistahnappinn til að opna leitina.
    * VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.  
17. Í listanum skal smella á tengilinn í valinni línu.
18. Í reitnum **VSK-flokkur vöru** skal smella á fellilistahnappinn til að opna leitina.
    * VSK-flokkur vöru fyrir núgildandi reikningslínuna.  
19. Í listanum skal smella á tengilinn í valinni línu.
20. Færa inn eða skoða fjöldi eininga fyrir reikningslínu.
    * Númerið er margfaldað með svæði einingaverðs til að ákvarða endanlegan upphæð reikningslínu.  
21. Færa inn eða skoða verð á einingu fyrir reikningslínu. 
    * Magnið er margfaldað með gildinu á **Magn** svæðinu til að ákvarða endanlegan upphæð línu.  
22. Skoða og breyta dreifingar á fjárhagsupphæð fyrir staka línu og allar línur undirstigs.
    * Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig tekjur, skatta eða gjöld verður að teknir með á reikningi með frjáls texti  
23. Uppfæra dreifing á fjárhagsupphæð fyrir Valið reikningslína.
24. Smellið á **Loka**.

## <a name="save-a-free-text-invoice-as-a-template"></a>Vistaðu reikningur með frjálsum texta sem sniðmát
Þú getur líka vistað fyrirliggjandi reikningur með frjálsum texta sem sniðmát. Þegar þú velur **Vista í sniðmát** á flipanum **Reikningur**, gefðu upp nafn og lýsingu fyrir sniðmátið. Ef sniðmát með nafninu er þegar til, munt þú sjá tilkynningu um að sniðmát með því nafni sé þegar til. Þú getur ennþá smellt á **Í lagi** til að skipta því út. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
