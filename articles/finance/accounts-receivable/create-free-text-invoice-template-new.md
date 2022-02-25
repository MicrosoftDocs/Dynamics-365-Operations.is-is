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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/16/2022
ms.locfileid: "8182510"
---
# <a name="create-a-free-text-invoice-template"></a>Stofna sniðmát fyrir reikning með frjálsum texta

[!include [banner](../includes/banner.md)]

Í þessari sýnikennslu skal nota USMF sýnifyrirtæki. Þetta ferli er ætluð fyrir notandann sem ber ábyrgð á stjórnun og vinnslu reikninga viðskiptakrafna.

## <a name="create-a-template"></a>Búa til sniðmát

1. Fara til **Viðskiptakröfur > Reikningar > Endurteknir reikningar > Free texta reikningssniðmát**.
    * Notaðu þessa síðu til að búa til reikningssniðmát með frjálsum texta sem geta innihaldið reikningslínur, gjöld, dreifingarsniðmát bókhalds og upplýsingar um fjárhagsreikning.  
2. Smellur **Nýtt** til að búa til nýtt ókeypis reikningssniðmát.
3. Í **Nafn sniðmáts** reit, sláðu inn gildi.
    * 'Sniðmátsheiti' auðkennir á einkvæman hátt sniðmát reikningur með frjálsum texta. Engin tvö sniðmát til að geta haft sama 'sniðmátsheiti'.  
4. Í **Lýsing** reit, sláðu inn lýsingu á sniðmátinu.
5. Stækkaðu **Reikningslínur** flipa.
6. Í **Lýsing** reit, sláðu inn lýsingu á reikningslínunni.
7. Í **Aðalreikningur** reit, veldu tekjureikning.
    * Hægt er að velja mótfærslureikning viðskiptavinakredit fyrir heildarupphæð reiknings í **Sendingarprófílar viðskiptavina** síðu.  
8. Í **Vöruskattshópur** reit, smelltu á fellilistann til að opna leitina.
    * VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.  
9. Í listanum skal smella á tengilinn í valinni línu.
10. Í **Vöruskattflokkur** reit, veldu vörusöluskattsflokk fyrir núverandi reikningslínu.
11. Í listanum skal smella á tengilinn í valinni línu.
12. Í **Einingaverð** reit, sláðu inn eða skoðaðu verð á einingu fyrir reikningslínuna
    * Þessi upphæð er margfölduð með **Magn** reit til að ákvarða reikningslínuupphæð.  
13. Bæta við nýrri línu við sniðmát reikningur með frjálsum texta.
14. Í **Lýsing** reit, sláðu inn lýsingu á reikningslínunni.
15. Í **Aðalreikningur** reit, veldu tekjureikning.
    * Hægt er að velja mótfærslureikning viðskiptavinakredit fyrir heildarupphæð reiknings í **Sendingarprófílar viðskiptavina** síðu.  
16. Í **Vöruskattshópur** reit, smelltu á fellilistann til að opna leitina.
    * VSK-flokkur fyrir núgildandi reikningslínu er sjálfgefinn VSK-flokkur fyrir viðskiptavinalykill.  
17. Í listanum skal smella á tengilinn í valinni línu.
18. Í reitnum **VSK-flokkur vöru** skal smella á fellilistahnappinn til að opna leitina.
    * VSK-flokkur vöru fyrir núgildandi reikningslínuna.  
19. Í listanum skal smella á tengilinn í valinni línu.
20. Sláðu inn eða skoðaðu fjölda eininga fyrir reikningslínuna.
    * Númerið er margfaldað með svæði einingaverðs til að ákvarða endanlegan upphæð reikningslínu.  
21. Færa inn eða skoða verð á einingu fyrir reikningslínu. 
    * Þessi upphæð er margfölduð með gildinu í **Magn** reit til að ákvarða reikningslínuupphæð.  
22. Skoða og breyta dreifingar á fjárhagsupphæð fyrir staka línu og allar línur undirstigs.
    * Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig tekjur, skatta eða gjöld verður að teknir með á reikningi með frjáls texti  
23. Uppfæra dreifing á fjárhagsupphæð fyrir Valið reikningslína.
24. Smellið á **Loka**.

## <a name="save-a-free-text-invoice-as-a-template"></a>Vistaðu reikningur með frjálsum texta sem sniðmát
Þú getur líka vistað fyrirliggjandi reikningur með frjálsum texta sem sniðmát. Þegar þú velur **Vista í sniðmát** frá **Reikningur** flipa, gefðu upp nafn og lýsingu fyrir sniðmátið. Ef sniðmát með nafninu er þegar til, munt þú sjá tilkynningu um að sniðmát með því nafni sé þegar til. Þú getur samt smellt á **Allt í lagi** að skipta um það. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
