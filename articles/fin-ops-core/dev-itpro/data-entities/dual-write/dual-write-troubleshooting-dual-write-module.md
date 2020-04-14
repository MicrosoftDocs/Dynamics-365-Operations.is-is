---
title: Úrræðaleit vandamál með tvískrifaðan einingunni í forritum Finance and Operations
description: Þetta efni veitir bilanaleit sem getur hjálpað þér að laga vandamál með tvískrifunareiningunni í forritum Finance and Operations.
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
ms.openlocfilehash: 34c10e38400a72a670a93f2a72d0aa7a4aed561a
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172761"
---
# <a name="troubleshoot-issues-with-the-dual-write-module-in-finance-and-operations-apps"></a>Úrræðaleit vandamál með tvískrifaðan einingunni í forritum Finance and Operations

[!include [banner](../../includes/banner.md)]



Þetta efni veitir upplýsingar um úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service. Einkum veitir það upplýsingar sem geta hjálpað þér að laga vandamál með **tvískrifunareiningunni** í forritum Finance and Operations.

> [!IMPORTANT]
> Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda. Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Þú getur ekki hlaðið tvíritunar eininguna í forriti Finance and Operations

Ef þú getur ekki opnað síðuna **Tvöfalt skrif** með því að velja reitinn **Tvöfalt skrif** á vinnusvæðinu **Gagnastjórnun** liggur gagnasamstillingarónustan líklega niðri. Búðu til stuðningseðil til að biðja um endurræsingu gagnasamstillingarþjónustunnar.

## <a name="error-when-you-try-to-create-a-new-entity-mapping"></a>Villa þegar þú reynir að búa til nýja vörpun eininga

**Nauðsynleg skilríki til að laga vandann:** Azure AD leigjandastjóri

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stilla nýja einingu fyrir tvískipt skrifun:

*Kóði svörunarstöðu bendir ekki til árangurs: 401 (Óheimilt)*

Þessi villa kemur upp vegna þess að aðeins Azure AD leigjandi getur bætt við nýrri vörpun eininga.

Til að laga málið, skráðu þig inn á forrit Finance and Operations sem Azure AD stjórnandaleigjandi. Þú verður líka að fara á web.PowerApps.com og staðfesta tenginguna.

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Villa þegar þú opnar tvískipt notendaviðmót

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að komast í tvískipt skrif úr vinnusvæðinu **Gagnastjórnun**:

*login.microsoftonline.com neitaði að tengjast.*

Til að laga málið, skráðu þig inn með því að nota InPrivate glugga í Microsoft Edge, huliðsglugga í Chromium, eða huliðsglugga í Google Chrome. Þú verður einnig að opna eða hreinsa smákökur frá þriðja aðila.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-entity-mapping"></a>Villa þegar þú tengir umhverfið fyrir tvískipt skrif eða bætir við nýrri vörpun eininga

**Nauðsynleg skilríki til að laga vandann:** Azure AD leigjandastjóri

Þú gætir lent í eftirfarandi villu þegar þú tengir eða býrð til kort:

*Svörunarstaðakóði bendir ekki til árangurs: 403 (tokenexchange).<br> Auðkenni fundar: \<lotuauðkenni þitt\><br> Auðkenni rótareksturs: \<auðkenni rótarstarfseminnar\>*

Þessi villa getur komið fram ef þú hefur ekki nægar heimildir til að tengja tvöfalt skrif eða búa til kort. Þú verður að nota Azure AD leigjandastjórareikning til að tengja umhverfi og bæta við nýjum vörpunum eininga. Eftir uppsetningu geturðu samt notað reikning sem ekki er stjórnandi til að fylgjast með stöðu og breyta vörpunum.

## <a name="error-when-you-stop-the-entity-mapping"></a>Villa þegar þú hættir við vörpun einingar

Þú gætir fengið eftirfarandi villuboð þegar þú reynir að stöðva varpanir einingarinnar:

*\[Forbidden\], \[{"staða":403,"uppruni":"","skilaboð":"Villa úr táknskiptum: Notanda er ekki heimild að fara í tengingu dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], The remote server returned an error: (403) Forbidden.*

Þessi villa kemur upp þegar tengt umhverfi Common Data Service er ekki í boði.

Til að laga málið, stofnaðu miða fyrir Data Integration teymið. Festu netsporið svo að gagnasamstillingarteymið geti merkt kortin sem **Ekki í gangi** í bakvinnslunni.
