---
title: Leysa úr vandamálum við fyrstu uppsetningu
description: Þetta efnisatriði veitir upplýsingar sem geta hjálpað þér að laga vandamál sem koma upp við upphaflega uppsetningu á samþættingu tvöfaldra skrifa.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f6ff9a304de8a94b86e6866d6d2cb65fbfdfb02f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561179"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Leysa úr vandamálum við fyrstu uppsetningu

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Dataverse. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega uppsetningu á samþættingu tvöfaldra skrifa.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Þú getur ekki tengt forrit Finance and Operations við Dataverse

**Nauðsynlegt hlutverk til að setja upp tvískipt skrif:** Kerfisstjóri í Finance and Operations forritum og Dataverse.

Villur á síðunni **Setja upp tengil á Dataverse** orsakast venjulega af ólokinni uppsetningu eða heimildavandamálum. Gakktu úr skugga um að öll ástandsskoðunin standist á síðunni **Setja upp tengil á Dataverse** eins og sýnt er á eftirfarandi mynd. Þú getur ekki tengt tvískipt skrif nema öll ástandsskoðunin standist.

![Vel heppnuð ástandsskoðun](media/health_check.png)

Þú verður að hafa Azure AD leigjandastjóraskilríki til að tengja Finance and Operations og Dataverse umhverfin. Þegar búið er að tengja umhverfin geta notendur skráð sig inn með því að nota innskráningarupplýsingar sínar og uppfært fyrirliggjandi töflukort.

## <a name="error-when-you-open-the-link-to-dataverse-page"></a>Villa þegar þú opnar tengilinn á síðuna Dataverse

**Nauðsynleg skilríki til að laga vandann:** Azure AD leigjandastjóri

Þú gætir fengið eftirfarandi villuboð þegar þú opnar **Tengill við síðuna Dataverse** í forriti Finance and Operations:

*Kóði svörunarstöðu bendir ekki til árangurs: 404 (Not Found.)*

Þessi villa kemur upp þegar samþykkisskrefinu hefur ekki verið lokið. Til að staðfesta hvort samþykkisskrefinu hafi verið lokið, skráðu þig inn á portal.Azure.com með því að nota Azure AD leigjandastjórareikning og sjáðu hvort forritið frá þriðja aðila sem hefur auðkenni **33976c19-1db5-4c02-810e-c243db79efde** birtist á listanum Azure AD **Enterprise-forrit**. Ef það gengur ekki verður þú að veita samþykki í forriti.

Fylgdu þessum skrefum til að veita samþykki í forriti.

1. Opnaðu eftirfarandi slóð með því að nota skilríki stjórnanda. Þú ættir að fá kvaðninu um samþykki.

    <https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent>

2. Veldu **Samþykkja** til að gefa til kynna að þú veiti samþykki þitt fyrir uppsetningu á forritinu sem er með kennið **33976c19-1db5-4c02-810e-c243db79efde** í leigjanda þínum.

    > [!TIP]
    > Þetta forrit er nauðsynlegt til að tengja forritin Dataverse og Finance and Operations. Ef þú átt í vandræðum með þetta skref skaltu opna vafrann þinn í huliðsstillingu (í Google Chrome) eða InPrivate ham (í Microsoft Edge).

## <a name="verify-that-company-data-and-dual-write-teams-are-set-up-correctly-during-linking"></a>Gakktu úr skugga um að fyrirtækjagögn og tvískipt teymi séu sett upp rétt við tengingu

Til að tryggja að tvískipt skrifun virki rétt eru fyrirtækin sem þú velur við stillingar stofnuð í Dataverse umhverfi. Sjálfgefið er að þessi fyrirtæki séu skrifvarin og eiginleikinn **IsDualWriteEnable** stilltur á **True**. Að auki eru sjálfgefnir eigendur viðskiptaeininga og teymi stofnuð og fela í sér nafn fyrirtækisins. Áður en þú kveikir á kortunum skaltu ganga úr skugga um að sjálfgefinn eigandi hópsins sé tilgreindur. Til að finna töfluna **Companies (CDM\_Company)** fylgirðu þessum skrefum.

1. Veldu síuna í efra hægra horninu í líkansdrifna forritinu í Dynamics 365.
2. Í fellilistanum velurðu **Fyrirtæki**.
3. Veldu **Keyra** til að sjá niðurstöðurnar.
4. Veldu fyrirtækið sem var tengt þegar þú stillir tvískipt skrif.
5. Staðfestu að dálkurinn **Sjálfgefið eigendateymi** hefur gildi. Á eftirfarandi mynd er dálkurinn **Sjálfgefið eigendateymi** stilltur á **USMF tvöfalt skrif**.

    ![Staðfestir sjálfgefið eigendateymi](media/default_owning_team.png)

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finnið mörkin á fjölda lagtaflna eða fyrirtækja sem hægt er að tengja við tvöfalda skráningu

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að virkja varpanir:

*Dual write failure - Plugin registration failed: \[(Ekki tókst að fá skiltáknakort fyrir verk DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Villa fer fram yfir hámarksskiltákn leyfð fyrir vörpun á DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)\], Ein eða fleiri villur komu upp.*

Núverandi mörk þegar tengt er við umhverfið eru um það bil 40 lagatöflur. Þessi villa kemur upp ef reynt er að virkja kort og fleiri en 40 lagatöflur eru tengdar á milli umhverfanna.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]