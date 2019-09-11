---
title: Búa til nýtt vöruhúsaútlit
description: Þetta efnisatriði lýsir hvernig setja á upp upplýsingar um staðsetningar í vöruhúsi.
author: perlynne
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 302c028a93dfdb57972e4759abbbc4fdedabbd17
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867237"
---
# <a name="create-a-new-warehouse-layout"></a>Búa til nýtt vöruhúsaútlit

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta efnisatriði lýsir hvernig setja á upp upplýsingar um staðsetningar í vöruhúsi. Þetta á aðeins við vöruhús sem eru stofnaðar með "grunn vöruhús" í kerfinu birgðastjórnun, ekki á við vöruhús sem er stofnað í vöruhúsakerfinu. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.


## <a name="set-the-default-location-capacity"></a>Stilla sjálfgefna afkastagetu staðsetningar
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Birgðir og færibreytur vöruhúsakerfis**.
2. Veldu flipann **Staðsetningar**.
3. Í reitinn **Stöðluð breidd** skal slá inn tölu.
4. Í reitinn **Stöðluð dýpt** skal slá inn númer.
5. Í reitinn **Stöðluð hæð** skal slá inn tölu.
6. Veljið **Vista**.
7. Lokið síðunni.

## <a name="define-the-location-name-format"></a>Skilgreina heiti staðsetningarsniðið
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Birgðastýring > Uppsetning > Niðurbrot birgða > Vöruhús**.
2. Veljið **Nýtt**.
3. Í reitinn **Vöruhús** skal slá inn gildi.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitnum **Svæði** velurðu skrána sem óskað er eftir í uppflettingunni.
6. Víxla útvíkkun á liðnum **Heiti staðsetninga**. Valkostirnir í þessum hluta er að skilgreina sjálfgefið snið fyrir heiti staðsetningu. Í dæminu okkar mælt verður að innihalda gangnúmers, rekkanúmer og hillunúmer.  
7. Stilltu valkostinn **Taka gang með** á **Já**.
8. Stilltu valkostinn **Taka rekka með** á **Já**. 
9. Í reitinn **Snið** ritarðu gildi fyrir rekkann.
10. Stilltu valkostinn **Taka hillu með** á **Já**.
11. Í reitinn **Snið** skal færa inn gildi fyrir hilluna.

## <a name="define-warehouse-locations"></a>Skilgreina Staðsetningar vöruhúsa
1. Í aðgerðarúðunni velurðu **Vöruhús**.
2. Veldu **Leiðsagnarforrit staðsetninga**.
3. Veljið **Næst**.
4. Afveljið valkostinn **Úthlið**
5. Afveljið valkostinn **Fjöldastaðsetningar**
6. Veldu **Næst** þangað til þú kemur að möguleikanum á að velja **Ljúka**.
7. Lokið síðunni.
8. Endurhlaðið síðuna.

