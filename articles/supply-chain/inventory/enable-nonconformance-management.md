---
title: Stjórnun ósamkvæmni
description: Þetta grein lýsir grunnuppsetningu sem er krafist til að nota ósamkvæmni. Viðbótaruppsetning er nauðsynleg ef á að nota gæðapantanir.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28951
ms.assetid: a62d4ba8-eebc-4b14-b587-630be7298522
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e66353dc3a4b4b7d9ff3c5f63bf3d4b0c70bda0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430406"
---
# <a name="nonconformance-management"></a>Stjórnun ósamkvæmni

[!include [banner](../includes/banner.md)]

Þetta grein lýsir grunnuppsetningu sem er krafist til að nota ósamkvæmni. Viðbótaruppsetning er nauðsynleg ef á að nota gæðapantanir.

Fylgið eftirfarandi skrefum til að virkja ósamkvæmnistýringu:

1.  Skilgreinið birgðafæribreyturnar pg vöruhúsafæribreyturnar sem eru tengdar ósamkvæmni.
    -   Setja skal **Nota gæðastjórnun** valkosturinn á **Já**.
    -   Í reitinn **tímagjald** skal færa inn tímagjald fyrir vinnu í gjaldmiðli landsins. Tímagjaldið er notuð til að reikna kostnað fyrir aðgerðir sem tengjast ósamkvæmni. Tímagjaldið og reiknaður kostnaður veita tilvísunarupplýsingar fyrir ósamkvæmni Þau eiga ekki í samskiptum við aðrar aðgerðir.
    -   Nota skal flipann **Gæðastjórnun** á síðunni **Skýrsluuppsetning** til að skilgreina gerð skjals til að prenta. Hægt er að prenta skýrslu um ósamkvæmni, ósamkvæmnimerki eða skýrslu um leiðréttingar. Hægt er að skilgreina fleiri en eina skráningu til að prenta mismunandi skjalategundir í skýrslu, eða til að prenta innri og ytri athugasemdir. Hjálplegt er að nota skjámyndina **Gerð fylgiskjals** til að skilgreina einkvæma gerð skjals fyrir ósamkvæmi og einkvæma gerð skjals fyrir leiðréttingu. Til dæmis á að færa inn athugasemdir um ósamkvæmni með því að nota einkvæma skjalgerð fyrir ósamkvæmni. Í þessu tilfelli auðkenna einkvæmu skjalgerðina í skýrsluvalkostum.
    -   Virkja númeraraðir fyrir ósamkvæmni og tilvísanir fyrir leiðréttingu.

2.  Virkja notendasamþykki fyrir ósamkvæmni. Notaðu skjámyndina **Nafn** á síðunni **notendur** til að úthluta starfsmanni á hvern notanda sem verður að samþykkja ósamkvæmni. Kerfið notar starfsmönnunum sem breyta stöðunni ósamkvæmi til að rekja sögu ósamkvæmninnar. Notendur getur ekki samþykkt ósamkvæmni nema þær hafa verið úthlutað starfsmannakenni.
3.  Skilgreinið vandamálagerðirnar sem verða tengdar við ósamkvæmni. Nota skal **vandamálagerðir** síðu til að skilgreina flokkun gæðavanda sem kemur fyrir í ýmsum ósamkvæmnigerðum. Hægt er að setja upp eftirfarandi gerðir ósamkvæmi: **Viðskiptavinur**, **Innra**, **Framleiðsla**, **Þjónustubeiðni** eða **Lánardrottinn** og **framleiðsla aukaafurða** Notaðu skjámyndina **gerð ósamkvæmi** til að heimila vandamálagerð til að nota í einni eða fleiri gerðum ósamkvæmni. Til dæmis getur vandamálagerð sem tengist gallakóða átt við um allar gerðir ósamkvæmni, en aftur á móti getur vandamálagerð um kvartanir viðskiptamanna aðeins átt við um **viðskiptavininn** og gerðir ósamkvæmni í **þjónustubeiðnum**.
4.  Skilgreina einangrunarsvæði til leiðbeiningar um hvernig meðhöndla skal gallað efni. Notaðu skjámyndina **biðgeymslusvæði** til að skilgreina svæði sem hægt er að úthluta á ósamkvæmni. Prentað ósamkvæmismerki birtir úthlutað biðgeymslusvæði og upplýsingar um notkun til þess að leiðbeina um meðferð á gallaðri vöru. Svæðin gætu samsvari birgðastaðsetning eða rekstrartilföng.
5.  Skilgreinið greiningargerðir sem verða tengdar leiðréttingu. Notaðu **greiningargerðir** síðuna til að skilgreina flokkun greiningaraðgerða. Leiðrétting auðkennir hvers konar greiningaraðgerð á að framkvæma á samþykktri ósamkvæmni, hver á að framkvæma hana. Hún tilgreinir einnig umbeðin lokadagsetning og áætluð lokadagsetning.
6.  Skilgreinið tengdar aðgerðir sem verður úthlutað á ósamkvæmni. Notið síðuna **aðgerðir** til þess að skilgreina flokkun á vinnu sem hægt er að framkvæmda fyrir samþykkta ósamkvæmni. Þegar tengdri aðgerð er úthlutað á ósamkvæmni, er líka hægt að skilgreina nánari upplýsingar eins og um tengt efni, vinnustundir og ýmis gjöld sem eru nauðsynleg til þess að framkvæma aðgerðina. Þessar upplýsingar eru notaðar til að reikna út áætlaðan kostnað fyrir aðgerðina. Upplýsingarnar og áætlaður kostnaður er notaður fyrir tilvísanir. Tengdar aðgerðir varðandi gæði eru öðruvísi en aðgerðir sem hægt er að skilgreina fyrir framleiðsluleið.


<a name="additional-resources"></a>Frekari upplýsingar
--------

[Stofna og vinna úr samræmi](tasks/create-process-non-conformance.md)

[Gæðastjórnunarferli](quality-management-processes.md)

[Setja upp forsendur fyrir ósamkvæmistýringu.](tasks/set-up-prerequisites-nonconformance-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]