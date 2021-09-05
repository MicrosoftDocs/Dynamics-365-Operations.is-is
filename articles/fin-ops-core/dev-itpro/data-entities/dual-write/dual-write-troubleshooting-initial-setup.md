---
title: Leysa úr vandamálum við fyrstu uppsetningu
description: Þetta efnisatriði veitir upplýsingar sem geta hjálpað þér að laga vandamál sem koma upp við upphaflega uppsetningu á samþættingu tvöfaldra skrifa.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2b75155aac12d79b9d68cce3e066acaaf80d6764
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380189"
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

![Vel heppnuð ástandsskoðun.](media/health_check.png)

Þú verður að hafa Azure AD leigjandastjóraskilríki til að tengja Finance and Operations og Dataverse umhverfin. Þegar búið er að tengja umhverfin geta notendur skráð sig inn með því að nota innskráningarupplýsingar sínar og uppfært fyrirliggjandi töflukort.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finnið mörkin á fjölda lagtaflna eða fyrirtækja sem hægt er að tengja við tvöfalda skráningu

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að virkja varpanir:

*Dual write failure - Plugin registration failed: (Ekki tókst að fá skiltáknakort fyrir verk DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Villa fer fram yfir hámarksskiltákn leyfð fyrir vörpun á DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea), Ein eða fleiri villur komu upp.*

Núverandi mörk þegar tengt er við umhverfið eru um það bil 40 lagatöflur. Þessi villa kemur upp ef reynt er að virkja kort og fleiri en 40 lagatöflur eru tengdar á milli umhverfanna.

## <a name="connection-set-failed-while-linking-environment"></a>Stilling tengingar mistókst við tengingu umhverfis

Við tengingu umhverfi tvöfaldrar skráningar mistekst aðgerðina með villuboðinu:

*Vistun tengistillingar mistókst! Vöru með sama lykli hefur þegar verið bætt við.*

Tvöföld skráning styður ekki marga lögaðila/fyrirtæki með sama heitinu. Til dæmis ef þú ert með tvö fyrirtæki með heitið „DAT“ í Dataverse þá koma upp þessi villuboð.

Til að afblokka viðskiptavininn skal fjarlægja tvíteknar færslur úr töflunni **cdm_company** í Dataverse. Einnig, ef taflna **cdm_company** er með færslur með auðu heiti skal fjarlægja eða leiðrétta þessar færslur.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Villa þegar síða tvöfaldrar skráningar var opnuð í Finance and Operations forritum

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að tengja Dataverse umhverfi fyrir tvöfalda skráningu:

*Kóði svörunarstöðu bendir ekki til árangurs: 404 (Not Found.)*

Þessi villa kemur upp þegar ekki er búið að ljúka við samþykktarskref forritsins. Þú getur staðfest hvort samþykki hafi verið veitt með því að skrá þig inn á `portal.azure.com` með stjórnandareikningi leigjanda og athuga hvort forrit þriðja aðila með auðkennið `33976c19-1db5-4c02-810e-c243db79efde` birtist í AAD-fyrirtækjalista. Ef svo er ekki skaltu keyra samþykkisþrepið aftur eins og lýst er í næsta hluta.

### <a name="providing-app-consent"></a>Veita forriti samþykki

+ Ræstu eftirfarandi vefslóð með innskráningarupplýsingum stjórnanda.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Veldu **Samþykkja** til að veita samþykki. Þú ert að veita samþykki til að setja upp forritið (með `id=33976c19-1db5-4c02-810e-c243db79efde`) í leigjandanum þínum.
+ Þetta forrit er nauðsynlegt fyrir Dataverse til að eiga samskipti við Finance and Operations forrit.

    ![Úrræðaleit fyrir uppsetningu upphaflegrar samstillingar.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Ef þetta virkar ekki skaltu ræsa vefslóðina í einkastillingu í Microsoft Edge eða huliðsstillingu í Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Ekki er hægt að finna Finance and Operations umhverfi

Þú gætir fengið eftirfarandi villuboð:

*Finance and Operations forritsumhverfi \*\*\*.cloudax.dynamics.com finnst ekki.*

Það er tvennt sem getur valdið vandræðum með umhverfi sem ekki er hægt að finna:

+ Notandinn sem notaður er við innskráningu er ekki sami leigjandi og Finance and Operations tilvikið.
+ Það komu upp vandamál við að finna nokkur eldri Finance and Operations tilvik sem voru hýst af Microsoft. Til að lagfæra þetta skaltu uppfæra Finance and Operations tilvikið. Hægt verður að finna umhverfið með hvaða uppfærslu sem er.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
