---
title: "Verkflæði eru notuð til að stjórna upplýsingum starfsmanns"
description: "Í þessu efnisatriði er útskýrt hvernig hægt er að nota verkflæðisgetu fyrir mannauð til að stjórna upplýsingum starfsmanns. Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkisverkflæði sem er ræst þegar starfsmenn breyta skráningu sinni."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 806860e5df9252c074e04e9e1670f4215fd94ca2
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="use-workflows-to-manage-employee-information"></a>Verkflæði eru notuð til að stjórna upplýsingum starfsmanns

[!include[banner](includes/banner.md)]


Í þessu efnisatriði er útskýrt hvernig hægt er að nota verkflæðisgetu fyrir mannauð til að stjórna upplýsingum starfsmanns. Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkisverkflæði sem er ræst þegar starfsmenn breyta skráningu sinni.

Verkflæðisgeta fyrir mannauð veitir fjölda verkflæða fyrir stjórnun mannauðsaðgerða. Þar að auki eru fjölmargir valkostir tiltækir svo að hægt er að breyta tilteknum verkflæðum og tengja þau við skýrslustigveldi. Verkflæði eru tiltæk til að aðstoða við stjórnun á breytingum á nokkrum stöðluðum gerðum starfsmannaupplýsinga. Hægt er að tengja verkflæði við stöðu. Síðan, ef starfsmenn breyta skráningu sinni, er verkflæði hafið sem þarfnast samþykkis áður en nýju upplýsingarnar eru vistaðar. Verkflæði eru forskilgreind fyrir eftirfarandi gerðir upplýsinga til að hjálpa við skilvirka stjórnun og halda starfsmannagögnum nákvæmum:

-   Auðkennisnúmer
-   Námskeið
-   Menntun
-   Mynd
-   Lánsvörur
-   Starfsreynsla
-   Verkreynsla
-   Hæfni
-   Ábyrgðarstöður
-   Mannauðsaðgerðir
-   Námskeiðsskráning

Þegar starfsmenn eru ráðnir, fluttir eða hættir getur verkflæðið innihaldið endurskoðunarferli. Á þennan hátt er hægt að endurskoða skjal eða skilgreina skilmála aðgerðar sem hluta af verkflæðinu. Þegar endurskoðunarferli er lokið er skjalið eða aðgerð lokið og verkflæðið færist yfir í endanlegt samþykktarskref.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Tengja verkflæði við stigveldi stöðu
Hægt er að tengja verkflæði við öll stigveldi sem eru skilgreind. Til dæmis, ef staða tengist fylki skýrslustigveldis gætirðu skilgreint verkflæði sem beinir kostnaði fyrir tiltekið verk til verksins í stað stjórnanda þess starfsmanns sem tengist þeirri stöðu. Til að stofna nýtt verkflæði eða breyta fyrirliggjandi verkflæði á síðunni **Verkflæði fyrir mannauð** er smellt á **Nýtt**. Veldu verkflæði í listanum til að hefja Verkflæðishönnuð. Hægt er að nota hönnuðinn til að stofna nýtt verkflæði eða breyta skrefum í fyrirliggjandi verkflæði. Þegar fyrirliggjandi verkflæði er breytt eru breytingarnar vistaðar sem ný útgáfa. Þess vegna er hægt alltaf fara til baka í fyrri útgáfu ef þarf.

## <a name="configure-a-human-resources-workflow"></a>Grunnstilla verkflæði fyrir mannauð
Til að grunnstilla grunnverkflæði sem ræsist þegar starfsmenn biðja um breytingar á persónuupplýsingum sínum, skal fylgja þessum skrefum.

1.  Á síðunni **Verkflæði fyrir mannauð** er smellt á **Nýtt**.
2.  Í listanum yfir tiltæk verkflæði velurðu **Auðkennisnúmer**.
3.  Smellið á **Keyra** til að hefja Verkflæðishönnuð og færið síðan inn notandanafn þitt og aðgangsorð við kvaðningu.
4.  Draga skal eininguna **Samþykkja auðkennisnúmer** úr listanum yfir verkflæðiseiningar á hönnunarstrigann.
5.  Tengja samþykktareininguna við **Ræsa** og **Ljúka**.
6.  Tvísmellið á **Samþykkja einingu** og hægrismellið svo og veljið **Eiginleika**.
7.  Fylgja skal þessum skrefum til að bæta við vöruleiðbeiningum:
    1.  Veldu **Úthlutun** og veldu síðan **Stigveldi** undir úthlutunargerð.
    2.  Undir valinu **Stigveldi** skal velja **Skilgreinanleg stigveldi**.
    3.  Bæta við stöðvunarskilyrði og loka síðunni.

8.  Lokið öllum viðbótarleiðbeiningum (engar aðrar viðvaranir eiga að vera til).
9.  Smellið á **Vista og loka**. Virkja nýja verkflæðið þegar svarglugginn opnast og velja **Gera virka**.
10. Fara í **Mannauð**&gt;**Stöður**&gt;**Stigveldisgerðir stöðu**.
11. Velja **Fylki**.
12. Bæta við verkflæðinu **Auðkennisnúmer starfsmanns** við listann.




