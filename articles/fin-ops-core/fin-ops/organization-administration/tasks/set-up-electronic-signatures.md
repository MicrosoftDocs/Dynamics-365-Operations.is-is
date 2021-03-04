---
title: Uppsetning rafrænna undirskrifta
description: Notaðu þetta ferli til að setja upp rafrænar undirskriftir.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 088fe3c42b00a6a495aeee19a4e3640054a8aa2a
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694766"
---
# <a name="set-up-electronic-signatures"></a>Uppsetning rafrænna undirskrifta

[!include [banner](../../includes/banner.md)]

Notaðu þetta ferli til að setja upp rafrænar undirskriftir. Rafræn undirskrift staðfestir deili á þeim aðila sem er í þann mund að hefja eða samþykkja ferli. Sýnigögn gögn fyrirtækisins til að stofna þetta ferli er DAT.


## <a name="enable-the-electronic-signature-configuration-key"></a>Virkja skilgreiningarlykilinn Rafræn undirskrift
1. Fara í Kerfisstjórnun > Uppsetning > Skilgreining leyfis.
2. Í trénu skal víkka út „Stjórnun“.
    * Staðfesta að gátreiturinn Rafræn undirskrift sé valinn.  
    * Ef gátreiturinn Rafræn undirskrift er ekki valinn þarf að virkja viðhaldsham. Hægt er að virkja viðhaldsham í þessu umhverfi með því að keyra viðhaldvinnslu frá Lifecycle Services eða með því að nota verkfærið Deployment.Setup staðbundið.  
3. Lokið síðunni.

## <a name="set-up-electronic-signature-parameters"></a>Uppsetning á færibreytum rafræna undirskrifta
1. Fara í Fyrirtækisstjórnun > Uppsetning > Rafræn undirskrift > Færibreytur rafrænna undirskrifta.
2. Smellið á „Breyta“.
3. Í reitinn Tilkynning skal slá inn gildi.
    * Færðu inn tilkynningu sem notendur fá þegar beðið er um undirskrift. Hægt er að færa inn hvaða texta sem er. Venjulega segir þessi texti notanda frá því hvað rafræn undirskrift felur í sér.  
    * Ef óskað er að færa inn texta fyrir Tilkynningar á öðrum tungumálum, smellið á hnappinn Þýðingar.  
4. Smellið á „Vista“.
5. Lokið síðunni.

## <a name="set-up-reason-codes-for-electronic-signatures"></a>Setja upp ástæðukóða fyrir rafrænar undirskriftir
1. Fara í Fyrirtækisstjórnun > Uppsetning > Rafræn undirskrift > Ástæðukóðar rafrænna undirskrifta.
2. Smellið á „Nýtt“.
    * Áður en hægt er að nota rafrænar undirskriftir verður að setja upp ástæðukóða. Þegar skjal er undirritað þarf að gefa upp gildan ástæðukóða.     Áritari velur ástæðukóða til að tilgreina tilgang rafrænnar undirskriftar. Til dæmis gæti ástæðukóði gefið til kynna lagalegt samþykki.  
3. Í reitinn Ástæðukóði skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
    * Færa inn viðbótar ástæðukóða, ef þörf krefur.  
5. Smellið á „Vista“.
6. Lokið síðunni.

## <a name="require-electronic-signatures-for-existing-processes"></a>Krefjast rafrænna undirskrifta fyrir fyrirliggjandi ferli
1. Fara í Fyrirtækisstjórnun > Uppsetning > Rafræn undirskrift > Kröfur um rafrænar undirskriftir.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja ferli sem krefst rafrænna undirskrifta.  
3. Veldu eða hreinsaðu gátreitinn Undirskriftar krafist.
    * Endurtakið þessi skref fyrir hvert ferli sem þarfnast rafrænna undirskrifta.  
4. Smellið á „Vista“.

## <a name="create-a-custom-requirement-for-electronic-signatures"></a>Stofna sérstilltar kröfur fyrir rafrænar undirskriftir
1. Smellið á „Nýtt“.
2. Veldu eða hreinsaðu gátreitinn Undirskriftar krafist.
3. Í reitnum Heiti skal færa inn heiti fyrir ferli sem þarfnast rafrænna undirskrifta.
4. Í reitnum Heiti töflu skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal finna og velja þá töflu þar sem gögnin sem verður að undirrita eru geymd.
6. Í listanum skal smella á tengilinn í valinni línu.
7. Í reitnum Heiti reits skal smella á fellilistahnappinn til að opna leitina.
8. Í reitnum skal finna og velja töflu sem á að bæta fylgjast með.
9. Í listanum skal smella á tengilinn í valinni línu.
    * Tilgreindu hvenær undirskrift er nauðsynleg.     Velja Alltaf ef undirskriftar er krafist þegar gögn í reitnum breytast.     Velja Aðeins ef undirskriftar er krafist við ákveðin skilyrði. Ef Aðeins, verður einnig að velja einn af eftirfarandi valkostum: Þegar færsla er færð inn, Þegar færsla er uppfærð eða þegar færslu er eytt.  
10. Smellið á „Vista“.
11. Lokið síðunni.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]