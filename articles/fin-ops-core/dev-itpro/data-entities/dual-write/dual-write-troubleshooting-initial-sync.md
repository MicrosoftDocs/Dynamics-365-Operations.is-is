---
title: Úrræðaleit vandamála við fyrstu samstillingu
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu.
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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172715"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Úrræðaleit vandamála við fyrstu samstillingu

[!include [banner](../../includes/banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál sem kunna að koma upp við upphaflega samstillingu. 

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Athugaðu hvort fyrstu samstillingarvillur eru í forriti Finance and Operations

Eftir að þú hefur gert kortlagningarsniðmát virkt ætti staða korta að vera **Í keyrslu**. Ef staðan er **Ekki í gangi** geta villur komið upp við fyrstu samstillingu. Til að skoða villurnar velurðu flipann **Upphaflegar samstillingarupplýsingar** á síðunni **Tvöfalt skrif**.

![Flipi upphafssamstillingar](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Þú getur ekki lokið fyrstu samstillingu: 400 Bad Request

**Nauðsynlegt hlutverk til að laga vandamálið:** Kerfisstjóri

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að keyra vörpun og upphafssamstillingu:

*Fjartengdi þjónninn skilaði villu: (400) Bad Request.), AX export encountered an error*

Hér er dæmi um full villuboð.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Ef þessi villa kemur stöðugt fram og þú getur ekki klárað fyrstu samstillingu, fylgdu þessum skrefum til að laga málið.

1. Skráðu þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.
2. Opnaðu stjórnborð Microsoft. 
3. Í glugganum **Þjónusta** skaltu ganga úr skugga um að Microsoft Dynamics 365 rammaþjónusta gagnainnflutnings-útflutnings er í gangi. Endurræstu það ef það hefur verið stöðvað, vegna þess að fyrsta samstillinga krefst þess.

## <a name="initial-synchronization-error-403-forbidden"></a>Upphafleg samstillingarvilla: 403 Forbidden

Þú gætir fengið eftirfarandi villuboð við fyrstu samstillingu:

*(\[Forbidden\], Fjartengdi þjónninn skilaði villu: (403) Forbidden.), AX export encountered an error*

Til að laga úr vandamálið skal fylgja þessum skrefum.

1. Innskráning í forritið Finance and Operations.
2. Á síðunni **Azure Active Directory forrit** eyðirðu **DtAppID** biðlaranum og bætir honum síðan við aftur.

![Listi yfir Azure AD forrit](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a>Sjálf-tilvísun mistök við fyrstu samstillingu

Þú gætir fengið villuboð sem líkjast eftirfarandi dæmi ef einhver af vörpunum þínum hefur sjálfsvísanir:

*Á Vendors V2, eftirfarandi villa: Record Id: new record, ErrorMessage: Couldn't resolve the guid for the field: msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber. The lookup value was not found: CN-001. Prófaðu þessa slóð til að athuga hvort tilvísunargögn eru til staðar: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Þessi tegund af villu á sér stað við fyrstu samstillingu varpana sem hafa sjálftilvísanir. Í dæminu á undan vísar reiturinn reikningslykill til lánadrottinseiningarinnar.

Til að laga málið gætirðu þurft að keyra vörpunina tvisvar áður en fyrsta samstilling tekst.

