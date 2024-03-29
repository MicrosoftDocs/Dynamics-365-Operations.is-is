---
title: Leysa úr vandamálum við fyrstu uppsetningu
description: Þessi grein veitir upplýsingar sem geta hjálpað þér að laga vandamál sem koma upp við upphaflega uppsetningu á samþættingu tvöfaldra skrifa.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289515"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Leysa úr vandamálum við fyrstu uppsetningu

[!include [banner](../../includes/banner.md)]

Þessi grein veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita fjármála- og reksturs og Dataverse. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega uppsetningu á samþættingu tvöfaldra skrifa.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þessi grein fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Þú getur ekki tengt fjármála- og reksturs-forrit við Dataverse

**Nauðsynlegt hlutverk til að setja upp tvískipt skrif:** Kerfisstjóri í forritum fjármála- og reksturs og Dataverse.

Villur á síðunni **Setja upp tengil á Dataverse** orsakast venjulega af ólokinni uppsetningu eða heimildavandamálum. Gakktu úr skugga um að öll ástandsskoðunin standist á síðunni **Setja upp tengil á Dataverse** eins og sýnt er á eftirfarandi mynd. Þú getur ekki tengt tvískipt skrif nema öll ástandsskoðunin standist.

![Vel heppnuð ástandsskoðun.](media/health_check.png)

Þú verður að hafa Azure AD leigjandastjóraskilríki til að tengja fjármál- og rekstur og Dataverse umhverfin. Þegar búið er að tengja umhverfin geta notendur skráð sig inn með því að nota innskráningarupplýsingar sínar og uppfært fyrirliggjandi töflukort.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finnið mörkin á fjölda lagtaflna eða fyrirtækja sem hægt er að tengja við tvöfalda skráningu

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að virkja varpanir:

*Dual write failure - Plugin registration failed: (Ekki tókst að fá skiltáknakort fyrir verk DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Villa fer fram yfir hámarksskiltákn leyfð fyrir vörpun á DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea), Ein eða fleiri villur komu upp.*

Núverandi mörk þegar tengt er við umhverfið eru um það bil 40 lagatöflur. Þessi villa kemur upp ef reynt er að virkja kort og fleiri en 40 lagatöflur eru tengdar á milli umhverfanna.

## <a name="connection-set-failed-while-linking-environment"></a>Stilling tengingar mistókst við tengingu umhverfis

Við tengingu umhverfi tvöfaldrar skráningar mistekst aðgerðina með villuboðinu:

*Vistun tengistillingar mistókst! Vöru með sama lykli hefur þegar verið bætt við.*

Tvöföld skráning styður ekki marga lögaðila/fyrirtæki með sama heitinu. Til dæmis ef þú ert með tvö fyrirtæki með heitið „DAT“ í Dataverse þá koma upp þessi villuboð.

Til að afblokka viðskiptavininn skal fjarlægja tvíteknar færslur úr töflunni **cdm_company** í Dataverse. Einnig, ef taflna **cdm_company** er með færslur með auðu heiti skal fjarlægja eða leiðrétta þessar færslur.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Villa þegar síða tvöfaldrar skráningar var opnuð í fjármála- og reksturs forritum fjármála- og reksturs

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að tengja Dataverse umhverfi fyrir tvöfalda skráningu:

*Kóði svörunarstöðu bendir ekki til árangurs: 404 (Not Found.)*

Þessi villa kemur upp þegar ekki er búið að ljúka við samþykktarskref forritsins. Þú getur staðfest hvort samþykki hafi verið veitt með því að skrá þig inn á `portal.azure.com` með stjórnandareikningi leigjanda og athuga hvort forrit þriðja aðila með auðkennið `33976c19-1db5-4c02-810e-c243db79efde` birtist í AAD-fyrirtækjalista. Ef svo er ekki skaltu keyra samþykkisþrepið aftur eins og lýst er í næsta hluta.

### <a name="providing-app-consent"></a>Veita forriti samþykki

+ Ræstu eftirfarandi vefslóð með innskráningarupplýsingum stjórnanda.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Veldu **Samþykkja** til að veita samþykki. Þú ert að veita samþykki til að setja upp forritið (með `id=33976c19-1db5-4c02-810e-c243db79efde`) í leigjandanum þínum.
+ Þetta forrit er nauðsynlegt fyrir Dataverse til að eiga samskipti við forrit fjármála- og reksturs.

    ![Úrræðaleit fyrir uppsetningu upphaflegrar samstillingar.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Ef þetta virkar ekki skaltu ræsa vefslóðina í einkastillingu í Microsoft Edge eða huliðsstillingu í Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Ekki er hægt að finna umhverfi fjármála- og reksturs 

Þú gætir fengið eftirfarandi villuboð:

*Forritaumhverfi fjármála- og reksturs \*\*\*.cloudax.dynamics.com finnst ekki.*

Það er tvennt sem getur valdið vandræðum með umhverfi sem ekki er hægt að finna:

+ Notandinn sem notaður er við innskráningu er ekki sami leigjandi og tilvik fjármála- og reksturs.
+ Það komu upp vandamál við að finna nokkur eldri tilvik fjármála- og reksturs sem voru hýst af Microsoft. Til að lagfæra þetta skaltu uppfæra tilvik fjármála- og reksturs. Hægt verður að finna umhverfið með hvaða uppfærslu sem er.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>403 (Forbidden)-villa á meðan tengingum var komið á

Sem hluti af tengingarferli tvöfaldrar skráningar eru tvær Power Apps tengingar (einnig þekkt sem *Apihub* tengingar) eru búnar til af hálfu notandans í tengda Dataverse umhverfinu. Ef viðskiptavinurinn er ekki með leyfi fyrir Power Apps umhverfið mun stofnun ApiHub-tenginga ekki takast og 403 (Bannað) villa er sýnd. Hér er dæmi um villuboð:

> MSG=\[Ekki tókst að setja upp umhverfi tvöfaldrar skráningar. Villuupplýsingar: Stöðukóði svars gefur ekki til kynna að hafi tekist: 403 (Bannað). - Kóði svörunarstöðu bendir ekki til árangurs: 403 (Forbidden).\] STACKTRACE=\[   á Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() í X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs:line 297 --- Endir staflarakningar úr fyrri staðsetningu þar sem undantekning koma fram --- á System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) at Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

Þessi villa kom upp vegna skorts á Power Apps-leyfi. Úthlutaðu viðeigandi leyfi (til dæmis Power Apps prufuútgáfu 2 áskriftarleið) á notandann þannig að hann hafi leyfi til að búa til tengingar. Til að staðfesta leyfið getur viðskiptavinurinn farið á svæðið [Reikningurinn minn](https://portal.office.com/account/?ref=MeControl#subscriptions) til að skoða úthlutuð leyfi notandans.

Frekari upplýsingar um Power Apps leyfi er hægt að finna í eftirfarandi greinum:

- [Úthluta leyfum á notendur](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [Kaupa Power Apps fyrir stofnun/fyrirtæki notanda](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

