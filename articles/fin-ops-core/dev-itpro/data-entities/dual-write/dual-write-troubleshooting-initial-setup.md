---
title: Úrræðaleit vandamála við fyrstu uppsetningu
description: Þetta efni veitir upplýsingar um bilanaleit sem geta hjálpað þér að laga vandamál sem gætu komið upp við upphaflega uppsetningu tvískiptrar skrifunar á milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: e20c9c5e1250c8e65b5642a7c45d7ae859315697
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172669"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Úrræðaleit vandamála við fyrstu uppsetningu

[!include [banner](../../includes/banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega uppsetningu á samþættingu tvöfaldra skrifa.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="you-cant-link-a-finance-and-operations-app-to-common-data-service"></a>Þú getur ekki tengt forrit Finance and Operations við Common Data Service

**Nauðsynleg skilríki til að setja upp tvískipt skrifun:** Azure AD leigjandastjóri

Villur á síðunni **Setja upp tengil á Common Data Service** orsakast venjulega af ólokinni uppsetningu eða heimildavandamálum. Gakktu úr skugga um að öll ástandsskoðunin standist á síðunni **Setja upp tengil á Common Data Service** eins og sýnt er á eftirfarandi mynd. Þú getur ekki tengt tvískipt skrif nema öll ástandsskoðunin standist.

![Vel heppnuð ástandsskoðun](media/health_check.png)

Þú verður að hafa Azure AD leigjandastjóraskilríki til að tengja Finance and Operations og Common Data Service umhverfin. Eftir að þú hefur tengt umhverfið geta notendur skráð sig inn með því að nota reikningsskilríki sín og uppfært núverandi einingakort.

## <a name="error-when-you-open-the-link-to-common-data-service-page"></a>Villa þegar þú opnar tengilinn á síðuna Common Data Service

**Nauðsynleg skilríki til að laga vandann:** Azure AD leigjandastjóri

Þú gætir fengið eftirfarandi villuboð þegar þú opnar **Tengill við síðuna Common Data Service** í forriti Finance and Operations:

*Kóði svörunarstöðu bendir ekki til árangurs: 404 (Not Found.)*

Þessi villa kemur upp þegar samþykkisskrefinu hefur ekki verið lokið. Til að staðfesta hvort samþykkisskrefinu hafi verið lokið, skráðu þig inn á portal.Azure.com með því að nota Azure AD leigjandastjórareikning og sjáðu hvort forritið frá þriðja aðila sem hefur auðkenni **33976c19-1db5-4c02-810e-c243db79efde** birtist á listanum Azure AD **Enterprise-forrit**. Ef það gengur ekki verður þú að veita samþykki í forriti.

Fylgdu þessum skrefum til að veita samþykki í forriti.

1. Opnaðu eftirfarandi slóð með því að nota skilríki stjórnanda. Þú ættir að fá kvaðninu um samþykki.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Veldu **Samþykkja** til að gefa til kynna að þú veiti samþykki þitt fyrir uppsetningu á forritinu sem er með kennið **33976c19-1db5-4c02-810e-c243db79efde** í leigjanda þínum.

    > [!TIP]
    > Þetta forrit er nauðsynlegt til að tengja forritin Common Data Service og Finance and Operations. Ef þú átt í vandræðum með þetta skref skaltu opna vafrann þinn í huliðsstillingu (í Google Chrome) eða InPrivate ham (í Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Gakktu úr skugga um að fyrirtækjagögn og tvískipt teymi séu sett upp rétt við tengingu

Til að tryggja að tvískipt skrifun virki rétt eru fyrirtækin sem þú velur við stillingar stofnuð í Common Data Service umhverfi. Sjálfgefið er að þessi fyrirtæki séu skrifvarin og eiginleikinn **IsDualWriteEnable** stilltur á **True**. Að auki eru sjálfgefnir eigendur viðskiptaeininga og teymi stofnuð og fela í sér nafn fyrirtækisins. Áður en þú kveikir á kortunum skaltu ganga úr skugga um að sjálfgefinn eigandi hópsins sé tilgreindur. Til að finna eininguna **Companies (CDM\_Company)** fylgirðu þessum skrefum.

1. Veldu síuna í efra hægra horninu í líkansdrifna forritinu í Dynamics 365.
2. Í fellilistanum velurðu **Fyrirtæki**.
3. Veldu **Keyra** til að sjá niðurstöðurnar.
4. Veldu fyrirtækið sem var tengt þegar þú stillir tvískipt skrif.
5. Staðfestu að reiturinn **Sjálfgefið eigendateymi** hefur gildi. Á eftirfarandi mynd er reiturinn **Sjálfgefið eigendateymi** stilltur á **USMF tvöfalt skrif**.

    ![Staðfestir sjálfgefið eigendateymi](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-entities-or-companies-that-can-be-linked-for-dual-write"></a>Finndu takmörk á fjölda lögaðila eða fyrirtækja sem hægt er að tengja fyrir tvískipt skrif

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að virkja varpanir:

*Dual write failure - Plugin registration failed: \[(Ekki tókst að fá skiltáknakort fyrir verk DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Villa fer fram yfir hámarksskiltákn leyfð fyrir vörpun á DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Ein eða fleiri villur komu upp.*

Núverandi takmörk þegar þú tengir umhverfið eru um það bil 40 lögaðilar. Þessi villa kemur upp ef þú reynir að virkja kort og meira en 40 lögaðilar eru tengdir milli umhverfisins.
