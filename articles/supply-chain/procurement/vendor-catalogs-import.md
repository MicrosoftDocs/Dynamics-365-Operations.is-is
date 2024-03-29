---
title: Flytja inn vörulista lánardrottins
description: Þessi grein lýsir ferlinu til að flytja inn vörulistagögn lánardrottins.
author: GalynaFedorova
ms.date: 03/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendProspectiveVendorRegistrationRequests, CatVendorCatalogDetails, CatVendorCatalogReleaseApprovedProducts, CatVendorCMRDetails, CatVendorCatalogProductPerCompanyStatus, CatVendorMaintenanceEventLog, CatVendorCatalogReviewTool, CatVendorCatalogFileUpload, CatVendorCatalogMaintenanceRequest, CatVendorCatalogFileInLegalEntity, CatVendorCatalogSchema, CatVendorCatalogFilePreviewPane, CatVendorCatalogImportParameter
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gfedorova
ms.search.validFrom: 2018-04-20
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 923715893b9f1c4b87d7bbb67e200f8cb8f92e6b
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9015556"
---
# <a name="import-vendor-catalogs"></a>Flytja inn vörulista lánardrottins

[!include[banner](../includes/banner.md)]

## <a name="vendor-catalogs-import"></a>Innflutningur vörulista lánardrottins

Í Dynamics 365 Supply Chain Management geta innkaupasérfræðingar stofnað og unnið með vörulista sem starfsmenn fyrirtækis geta notað þegar þeir panta vörur og þjónustu til innri notkunar. Til að stofna innkaupavörulista er hægt að bæta við vörum og þjónustu sem eiga að vera í boði fyrir starfsmenn, annaðhvort með því að flytja inn innkaupavörulisti eða handvirkt bæta innkaupavörulista við afurðarsniðmát. 

Hægt er að hlaða upp vörulistagögnum sem lánardrottinn hefur sent með biðlara Microsoft Dynamics 365.

Afurðargögnin sem lánardrottinn sendir til þín sem skáarformið viðhaldsbeiðni vörulista (CMR) verður að vera á XML-skráarsniði. CMR-skráin ætti að innihalda upplýsingar um afurðirnar sem lánardrottinn veitir fyrirtækinu þínu.

## <a name="import-vendor-catalog-data"></a>Flytja inn vörulistagögn lánardrottins

Til að flytja inn vörulistagögn lánardrottins þarf að ljúka eftirfarandi verkum:

1. Settu upp verk á vinnusvæði Gagnastjórnunar þar sem þú hefur skilgreint reglur gagnavörpunar. Veldu **Gagnastjórnun** og veldu síðan **Setja upp hlutverk fyrir gagnaverk**.

2. Settu upp tegundastigveldi innkaupa og úthlutaðu lánardrottnum þínum á innkaupaflokka. Ef þú notar vörukóða skaltu bæta vörukóðanum við innkaupaflokka. Til að fá upplýsingar um uppsetningu á tegundastigveldi innkaupa skaltu sjá [Setja upp tegundastigveldi innkaupa](../procurement/tasks/set-up-procurement-category-hierarchy.md).

3. Stilla lánardrottinn fyrir innflutning vörulista. Veldu lánardrottin og veldu síðan **Innkaup** > **Setja upp** > **Stilla lánardrottin fyrir vörulistainnflutning**.

4. Stilla verkflæði fyrir vörulistainnflutning. Stofna CMR-skráarsniðmát og deila því með lánardrottni.

5. Veldu **Innkaup og aðföng** \> **Vörulistar** \> **Vörulistar lánardrottins**  Vörulistar lánardrottins til að stofna vörulista lánardrottins. Skrárnar fyrir viðhaldsbeiðni vörulista (CMR) sem þú færð frá lánardrottni eru flokkaðar í þessum vörulista.

6. Hlaða upp CMR-skránni.

7. Yfirfara, samþykkja eða hafna afurðum í vörulista lánardrottins. Vörunum er sjálfkrafa varpað á innkaupaflokka. 

Samþykktum afurðum er bætt við afurðarsniðmát og sendar til valins lögaðila. Aðeins er hægt að bæta samþykktum afurðum við innkaupavörulistann.

## <a name="generate-a-catalog-import-file-template"></a>Mynda sniðmát fyrir innflutningsskrá vörulista

Sniðmát fyrir innflutningsskrá vörulista er XSD-skrá sem notuð er til að stofna CMR-skrá fyrir afurðir lánardrottins. Hægt er að nota CMR-skrána til að stofna nýjan vörulista, skipta út fyrirliggjandi vörulista eða breyta fyrirliggjandi vörulista.

1. Veldu **Innkaup og aðföng** \> **Vörulistar** \> **Vörulistar lánardrottins** og tvísmelltu á vörulistann sem þú vilt vinna með.

2. Sæktu núverandi sniðmát vörulistainnflutnings (XSD-skrá). Á síðunni **Uppfæra vörulista**, á **Aðgerðarsvæði**, á flipanum **Vörulistar** í flokknum **Tengdar upplýsingar** skaltu smella á **Búa til sniðmát vörulista** og velja **Innkaupategund**.

    - Með valkostinum **Innkaupaflokkar** er hægt að búa til sniðmát vörulista sem inniheldur innkaupaflokka þar sem lánardrottni er heimilað að útvega afurðir.

3. Í svarglugganum **Vista sem** skaltu velja staðsetningu þar sem á að geyma sniðmát fyrir vörulistaskrá og vista skrána.

Nánari upplýsingar og dæmi er að finna í þessari bloggfærslu: [Vörulistar lánardrottins í Dynamics AX](https://blogs.msdn.microsoft.com/dynamicsaxscm/2016/05/25/vendor-catalogs-in-dynamics-ax/).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]