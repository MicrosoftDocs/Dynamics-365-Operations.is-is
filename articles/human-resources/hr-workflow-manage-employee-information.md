---
title: Nota verkflæði til að haga starfsmannaupplýsingum
description: Þetta efnisatriði útskýrir hvernig þú getur notað verkflæði til að stjórna starfsmannaupplýsingum.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7c416a82976bc39464006325f02f1af4d2f32ea4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691527"
---
# <a name="use-workflows-to-manage-employee-information"></a>Nota verkflæði til að haga starfsmannaupplýsingum


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Í þessu efnisatriði er útskýrt hvernig hægt er að nota verkflæðisgetu fyrir mannauð til að stjórna upplýsingum starfsmanns. Til dæmis er hægt að tengja verkflæði við stöðu og skilgreina samþykkisverkflæði sem er ræst þegar starfsmenn breyta skráningu sinni.

Verkflæðisgeta fyrir mannauð veitir fjölda verkflæða fyrir stjórnun mannauðsaðgerða. Þar að auki eru fjölmargir valkostir tiltækir svo að hægt er að breyta tilteknum verkflæðum og tengja þau við skýrslustigveldi. Verkflæði eru tiltæk til að hjálpa til við að stjórna breytingum á nokkrum tegundum starfsmannaupplýsinga. Hægt er að tengja verkflæði við stöðu. Síðan, ef starfsmenn breyta skráningu sinni, er verkflæði hafið sem þarfnast samþykkis áður en nýju upplýsingarnar eru vistaðar. Verkflæði eru fyrirfram skilgreind fyrir eftirfarandi tegundir upplýsinga til að hjálpa þér að stjórna breytingum á skilvirkan hátt og halda gögnum starfsmanna þinna nákvæmum:

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

Þegar starfsmenn eru ráðnir, fluttir eða hættir getur verkflæðið innihaldið endurskoðunarferli. Þannig er hægt að endurskoða skjal eða skilgreina skilmála aðgerða sem hluta af verkflæðinu. Þegar endurskoðunarferli er lokið er skjalið eða aðgerð lokið og verkflæðið færist yfir í endanlegt samþykktarskref.

## <a name="associate-a-workflow-with-a-position-hierarchy"></a>Tengja verkflæði við stigveldi stöðu
Hægt er að tengja verkflæði við öll stigveldi sem eru skilgreind. Til dæmis, ef staða tengist fylki skýrslustigveldis gætirðu skilgreint verkflæði sem beinir kostnaði fyrir tiltekið verk til verksins í stað stjórnanda þess starfsmanns sem tengist þeirri stöðu. Til að búa til nýtt verkflæði eða breyta núverandi verkflæði, á **Starfsflæði mannauðs** síðu, veldu **Nýtt**. Veldu verkflæði á listanum til að opna verkflæðishönnuðinn. Hægt er að nota hönnuðinn til að stofna nýtt verkflæði eða breyta skrefum í fyrirliggjandi verkflæði. Þegar fyrirliggjandi verkflæði er breytt eru breytingarnar vistaðar sem ný útgáfa. Þess vegna er hægt alltaf fara til baka í fyrri útgáfu ef þarf.

## <a name="configure-a-human-resources-workflow"></a>Grunnstilla verkflæði fyrir mannauð
Til að grunnstilla grunnverkflæði sem ræsist þegar starfsmenn biðja um breytingar á persónuupplýsingum sínum, skal fylgja þessum skrefum.

1.  Á **Starfsflæði mannauðs** síðu, veldu **Nýtt**.
2.  Í listanum yfir tiltæk verkflæði velurðu **Auðkennisnúmer**.
3.  Veldu **Hlaupa** til að opna verkflæðishönnuðinn og sláðu síðan inn notandanafn og lykilorð þegar þú ert beðinn um það.
4.  Draga skal eininguna **Samþykkja auðkennisnúmer** úr listanum yfir verkflæðiseiningar á hönnunarstrigann.
5.  Tengja samþykktareininguna við **Ræsa** og **Ljúka**.
6.  Tvísmelltu (eða tvísmelltu) **Samþykkja þátt**, veldu og haltu inni (eða hægrismelltu) og veldu síðan **Eiginleikar**.
7.  Fylgja skal þessum skrefum til að bæta við vöruleiðbeiningum:

    1.  Veldu **Úthlutun** og veldu síðan **Stigveldi** undir úthlutunargerð.
    2.  Undir valinu **Stigveldi** skal velja **Skilgreinanleg stigveldi**.
    3.  Bæta við stöðvunarskilyrði og loka síðunni.

8.  Lokið öllum viðbótarleiðbeiningum (engar aðrar viðvaranir eiga að vera til).
9.  Veljið **Vista og loka**. Virkja nýja verkflæðið þegar svarglugginn opnast og velja **Gera virka**.
10. Fara í **Mannauð** &gt; **Stöður** &gt; **Stigveldisgerðir stöðu**.
11. Velja **Fylki**.
12. Bæta við verkflæðinu **Auðkennisnúmer starfsmanns** við listann.

## <a name="additional-resources"></a>Frekari upplýsingar

[Skoða og hafa umsjón með breytingum á aðsetri](hr-personnel-view-address-changes.md) 





[!INCLUDE[footer-include](../includes/footer-banner.md)]
