---
title: Skilgreina kostnaðarreglur
description: Hægt er að skilgreina reglur sem starfskraftar þurfa að fylgja þegar þeir búa til og skila kostnaðarskýrslum og ferðabeiðnum í Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389716"
---
# <a name="define-expense-policies"></a>Skilgreina kostnaðarreglur

[!include [banner](../includes/banner.md)]

Hægt er að skilgreina reglur sem starfskraftar þurfa að fylgja þegar þeir búa til og skila kostnaðarskýrslum og ferðabeiðnum.         
Innleiðing kostnaðarreglna getur hjálpað til við að stjórna kostnaði á áhrifaríkan hátt.         

Til dæmis er hægt að setja þá reglu að í New York borg geti hótelkostnaður fyrir hverja nótt ekki farið yfir 250 Bandaríkjadali.       
Ef starfsmaður skilar inn kostnaðarskýrslu eða ferðabeiðni þar sem herbergistaxtinn er yfir þessari upphæð lætur kerfið        
starfskraftinn vita að hann hafi farið fram úr kostnaði samkvæmt reglubundnu kostnaðarupphæðinni. Hægt er að breyta skilaboðunum sem starfskrafturinn mun fá þegar        
stefnan er skilgreind.      
        
Hægt er að stofna þrjár gerðir reglna:         
        
- Viðvörun - Leyfir starfskrafti að leggja fram kostnaðarskýrslu eða ferðabeiðni en kostnaðurinn verður merktur fyrir alla samþykktaraðila og        
  fyrir síðari skýrslugerð.        

- Villa - Krefst þess að starfskrafturinn endurskoði kostnaðinn til að hann verði í samræmi við reglu áður en hann sendir kostnaðarskýrslu eða ferðabeiðni.       
 
 - Rökstuðningur - Krefst þess að starfskrafturinn eða stjórnandi leggi fram rök fyrir því að farið sé yfir regluupphæð áður en hann sendir kostnaðarskýrslu eða ferðabeiðni.        

## <a name="policy-tips"></a>Ábendingar um reglu
Hér eru nokkrar tillögur sem geta aðstoðað þig við að búa til nýjar reglur varðandi útgjaldastýringu. 
* Reglur miðast við dagsetningar og taka ekki gildi ef reglan er búin til með dagsetningu sem kemur á eftir dagsetningunni sem kostnaðurinn átti sér stað. Ef þú til dæmis býrð til nýja reglu í dag til að framfylgja hámarkskostnaði á máltíð sem nemur 50 USD, verður enginn núverandi kostnaður sem var færður inn í gær athugaður í tengslum við þessa reglu.
* Þegar reglu er búin til fyrir kostnaðartegund sem hægt er að sundurliða, skaltu íhuga að bæta við skilyrði fyrir gerð kostnaðarlínu. Sumar reglur á borð við að krefjast kvittunar passa hugsanlega ekki við sundurliðaðar línur og ætti aðeins að nota þær fyrir hauslínu eða línu sem er ekki sundurliðuð. 
* Reglur útgjaldastýringar eru sjálfkrafa metnar gagnvart frumeiningunni. Fyrir aðstæður innan samstæðu er hægt að stilla regluna á að vera metin gagnvart einingu áfangastaðar (lána einingu) í staðinn. Til að keyra reglur gagnvart einingu áfangastaðar skal kveikja á eiginleikanum „Meta kostnaðarreglu á móti lögaðila sem fær lánað“ á vinnusvæði **Eiginleikastjórnun**.

## <a name="when-to-evaluate-policies"></a>Hvenær meta skal reglur

Í færibreytum útgjaldastýringar er möguleiki á því að annaðhvort meta reglur útgjaldastýringar þegar lína er vistuð eða þegar kostnaðarskýrsla er send inn. Ef valið er að meta þegar lína er vistuð tryggir það að notendur verði með sýnileika fyrr á því hvað þurfi að gera til að ljúka allri kostnaðarskýrslunni í einu. Annars er hægt að fresta reglumati og spara tíma ef villuleit er gerð í lokin við innsendingu á verkflæði.
