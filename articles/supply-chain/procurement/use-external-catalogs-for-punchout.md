---
title: "Nota ytri vörulista fyrir PunchOut eProcurement"
description: "Þetta efnisatriði útskýrir hvernig hægt er að nota ytri vörulista til að stofna og senda innkaupabeiðnir."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchVendorPortalRequests
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 01955aefb27bd18809b35fd025c9dd1b8eb70520
ms.contentlocale: is-is
ms.lasthandoff: 06/20/2017

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a>Nota ytri vörulista fyrir PunchOut eProcurement
Með því að nota ytri vörulistar PunchOut e-innkaup, ekki þarf að halda utan um upplýsingar um vörum í eigin aðalgögn við lánardrottna. Þess í stað innkaupakörfu á vefsvæði lánardrottins breytt innkaupabeiðni sem hefur verið rétt afurðarupplýsingar. 

Ætti að forðast umsjón með lýsingum og verð í lánardrottnar vörum í eigin aðalgögnum vöru. Þess í stað skaltu nota ytri vörulista fyrir PunchOut eProcurement. Síðan, þegar starfsmönnum er að stofna innkaupabeiðnir, þær geta "punch" lánardrottins vörulista ytra setur (með öðrum orðum þær skilja kerfið og fara sem lánardrottinn setur). Vörurnar sem bætt er í innkaupakörfuna á vefsvæði lánardrottins getur síðan breytt til línur innkaupabeiðni. Þar af leiðandi fæst rétt afurðarupplýsingar: framleiðslulíkans Kenni, nafn, verð og o.s.frv.

Nota ytri vörulistar sem starfsmaður verður að stofna beiðni á við **innkaupabeiðnir Mínar** síðu.

Starfsmaðurinn sem stofnar beiðni kallast útskráningarferli beiðninnar. Útskráningarferli, sem hægt er að ljúka eftirfarandi verkum.

Notkun á **Ytri vörulistar** línu aðgerð til að opna síðuna sem inniheldur öll ytri vörulistar sem eru í boði fyrir tiltekna requester kaupa lögaðili og móttaka rekstrarfærslna einingu.

Breyta requester kaupa lögaðili og móttaka rekstrarfærslna einingu eftir heimildum þínum. Breytingar á þessum gildum breyst lista yfir ytri vörulistar eru tiltæk í requester. Ytri vörulistar sem eru tiltækar fara eftir núverandi virka innkaup reglurnar fyrir veitta lögaðili eða móttöku rekstrarfærslna eininguna. Þessar reglur má gera eða torvelda aðgang að tilteknum innkaupaflokkana. Þar af leiðandi lista yfir ytri vörulistar sem tengt er þessum innkaupaflokkana getur fyrir áhrifum.

Frekari upplýsingar um hvernig reglur eru settir upp eru í [Innkaupastefnum](../procurement/purchase-policies.md).

- Finna ytri vörulistar fyrir tiltekna innkaupaflokkana, færa inn texta í leitarsvæðið vörulista.
- Til að bæta vörum úr vörulista lánardrottins ytri á vefsvæði lánardrottins, smellt er á utanaðkomandi vörulistann. Svo að bæta vörum í innkaupakörfuna og athuga. Í innkaupakörfuna körfu verða línurnar færðar í Microsoft Dynamics 365.

Ef það eru margir valkostir innkaupaflokkana velja rétta innkaupaflokkurinn áður en línum er bætt við við innkaupabeiðnina.
Eftir að línum hefur verið bætt við innkaupabeiðni er hægt að bæta viðbótarlínum án þess að nota ytri vörulistar. Einnig er hægt er að áfram ytri vörulistar er notuð til að bæta við línu.

Þegar beiðnin er tilbúin fyrir **Verkflæði** > **Senda** aðgerð til að senda hana til samþykktar.
