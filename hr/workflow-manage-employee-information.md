---
title: "Verkflæði er notuð til að stjórna upplýsingum starfsmanns"
description: "Í þessu efnisatriði er útskýrt hvernig hægt er að nota getu verkflæði fyrir mannauð til að stjórna upplýsingum starfsmanns. Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkis verkflæðisins sem er ræst þegar starfsmenn breyta þeirra."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: a76ec0cd86bcc810b42ae3cd8efd8a584e6c4da3
ms.openlocfilehash: f286436aa4833babaeb3de875ee393d18e5f8eea
ms.lasthandoff: 03/31/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Verkflæði er notuð til að stjórna upplýsingum starfsmanns

Í þessu efnisatriði er útskýrt hvernig hægt er að nota getu verkflæði fyrir mannauð til að stjórna upplýsingum starfsmanns. Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkis verkflæðisins sem er ræst þegar starfsmenn breyta þeirra.

Getu verkflæði fyrir mannauð veitir tengilaðila verkflæði fyrir stjórnun mannauðsaðgerðir. Þar að auki er tengilaðila valkostir eru tiltækir þannig að hægt er að breyta tilteknu verkflæði og tengja þá við skýrslugerð stigveldi. Verkflæði eru tiltæk til að aðstoða breytingar á nokkrum staðlaðar gerðir starfsmannaupplýsingar. Hægt er að tengja verkflæði við stöðu. Svo ef starfsmenn þeirra færslu starfsmanns er breytt verkflæðis er hafin sem þarfnast samþykkis áður en nýju upplýsingarnar eru vistaðar. Verkflæði eru forskilgreindar fyrir eftirfarandi gerðir upplýsinga um hjálp við að stjórna hagkvæman hátt breytingar og halda við starfsmenn gögn nákvæmar:

-   Auðkennisnúmer
-   Námskeið
-   Menntun
-   Mynd
-   Lánsvörur
-   Starfsreynsla
-   Verkreynsla
-   Hæfni
-   Ábyrgðarstöður
-   Aðgerðir í mannauði
-   Námskeiðsskráningu

Þegar starfsmenn eru ráðnir, fluttar eða hættur, verkflæði taka endurskoðunarferli. Á þennan hátt er hægt að endurskoða skjal eða skilmála aðgerð getur verið skilgreindur sem hluti af verkflæðinu. Þegar endurskoðunarferli er lokið er skjalið eða aðgerð er lokið og verkflæðið flytur endanleg samþykktarskrefi.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Tengja verkflæði við stigveldi stöðu
Hægt er að tengja verkflæði við öllum þrepum sem er skilgreind. Til dæmis, ef staða tengist skýrslugerð stigveldi fylki, gæti verið að skilgreina verkflæði sem leiðir til kostnaðar fyrir tiltekið verk ábendingu verks í stað stjórnanda þess starfsmanns sem tengist þeirri stöðu. Til að stofna nýtt verkflæði eða breyta fyrirliggjandi verkflæði, á við **mannauður verkflæði** síðunni er smellt á **Nýtt**. Velja verkflæðis í listanum til að hefja hönnuður Verkflæði. Hægt er að nota í hönnuð til að stofna nýtt verkflæði eða breyta skref í verkflæði. Þegar verkflæði er breytt eru breytingarnar vistaðar sem ný útgáfa. Þess vegna er hægt alltaf fara aftur í fyrri útgáfu ef þarf.

## <a name="configure-a-human-resources-workflow"></a>Skilgreina verkflæði fyrir mannauð
Fylgið eftirfarandi skrefum til að skilgreina grunnupplýsingar verkflæði sem er ræst þegar starfsmönnum er beðið um breytingar á persónuleg kenni þeirra.

1.  Á við **verkflæðum mannauðs** síðunni er smellt á **Nýtt**.
2.  Veljið í listanum yfir tiltæk verkflæði **tölur Auðkenni**.
3.  Smellið á **Keyra** til að hefja Verkflæði hönnuður og síðan færa inn notandanafn þitt og aðgangsorð þegar beðið verið.
4.  Draga skal **Samþykkja kenninúmer** einingu úr listanum yfir verkflæðiseiningar hönnuður striga.
5.  Samþykktareining til að tengja **Ræsa** og **Ljúka**.
6.  Tvísmellið á **Samþykkja eining**, og svo hægrismella og velja **Eiginleika**.
7.  Fylgið eftirfarandi skrefum til að bæta verkleiðbeiningarnar vöru:
    1.  Velja **Úthlutun**, og veljið síðan **Stigveldi** undir verkefnisgerð.
    2.  Undir á **Stigveldi** val velja **Skilgreinanleg stigveldi**.
    3.  Bæta við stöðvunarskilyrði og loka síðan.

8.  Lokið öllum viðbótarleiðbeiningar (engar aðrar viðvaranir eiga til).
9.  Smellið á **Vista og loka**. Virkja verkflæðið þegar svargluggann reitnum opnast og velja **Gera virka**.
10. Fara í **Mannauður**&gt;**Stöður**&gt;**stigveldisgerðir Stöðu**.
11. Velja **Fylki**.
12. Bæta við **kenninúmer Starfsmanns** verkflæði við listann.



