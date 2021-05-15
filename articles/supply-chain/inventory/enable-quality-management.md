---
title: Virkja stjórnun gæða og ósamkvæmni
description: Í þessu efnisatriði er að finna yfirlit yfir ferlið við uppsetningu og skilgreiningu stjórnunareiginleika gæða og ósamkvæmni í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67d5da648e31d07d054246f5d308a6c6cdeb506c
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956255"
---
# <a name="enable-quality-and-nonconformance-management"></a>Virkja stjórnun gæða og ósamkvæmni

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna yfirlit yfir ferlið við uppsetningu og skilgreiningu stjórnunareiginleika gæða og ósamkvæmni í Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm">Virkja stjórnun gæða og ósamkvæmni</a>

Fylgið eftirfarandi skrefum til að virkja gæðastjórnun í kerfinu.

1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur birgða- og vöruhúsakerfis**.
1. Í flipanum **Gæðastjórnun** skal stilla valkostinn **Nota gæðastjórnun** á *Já*.
1. Í reitinn **tímagjald** skal færa inn tímagjald fyrir vinnu í gjaldmiðli landsins. Tímagjaldið er notuð til að reikna kostnað fyrir aðgerðir sem tengjast ósamkvæmni. Tímagjaldið og reiknaður kostnaður veita tilvísunarupplýsingar fyrir ósamkvæmni Þau eiga ekki í samskiptum við aðrar aðgerðir.
1. Veljið **Uppsetning skýrslu**.
1. Bætið við nýjum línum fyrir hinar ýmsu skýrslugerðir og veljið gerð skjals sem á að nota fyrir hverja skýrslu.
1. Lokið síðunni.
1. Lokið síðunni.

## <a name="quality-management-configuration-process"></a>Skilgreiningarferli gæðastjórnunar

Áður en hægt er að byrja að nota eiginleika gæðastjórnunar og búa til gæðapantanir þarf að skilgreina kerfið og forkröfur. Hér er listi yfir skrefin sem eru nauðsynleg til að stilla gæðastjórnun.

1. [Virkja stjórnun gæða og ósamkvæmni](#enable-qm)
1. Valfrjálst: [Stilla prófunartæki](quality-test-instruments.md).
1. [Skilgreina próf](quality-tests.md).
1. [Skilgreina prófunarbreytur og útkomur](quality-test-variables.md).
1. [Skilgreina prófunarflokka](quality-test-groups.md).
1. Valfrjálst: [Stilla gæðaflokka og tengja við vörur](quality-groups.md).
1. Valfrjálst: [Stilla gæðatengingar](quality-associations.md).

Þegar skilgreiningu er lokið er hægt að byrja að stofna og vinna úr gæðapöntunum. Frekari upplýsingar um hvernig á að búa til og vinna með gæðapantanir er að finna í [Gæðapantanir](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Skilgreiningarferli fyrir stjórnun ósamkvæmni

Áður en hægt er að byrja að nota eiginleika fyrir stjórnun ósamkvæmni og búa til ósamkvæmni þarf að skilgreina kerfið og forkröfur. Hér er listi yfir skrefin sem eru nauðsynleg til að stilla stjórnun ósamkvæmis.

1. [Virkja stjórnun gæða og ósamkvæmni](#enable-qm)
1. [Stilla starfskrafta sem bera ábyrgð á að samþykkja ósamkvæmi](quality-responsible-workers.md).
1. [Skilgreina gerðir vandamála](quality-problem-types.md).
1. [Skilgreina biðgeymslusvæði](quality-quarantine-zones.md).
1. [Skilgreina greiningargerðir](quality-diagnostic-types.md).
1. [Skilgreina aðgerðir](quality-operations.md).
1. Valfrjálst: [Stilla gæðagjöld](quality-charges.md).

Þegar skilgreiningunni er lokið er hægt að byrja að stofna og vinna úr ósamkvæmi. Nánari upplýsingar um hvernig á að stofna og vinna með ósamkvæmi eru í [Stofna og meðhöndla ósamkvæmi](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gæðastjórnunaryfirlit](quality-management-processes.md)
- [Virkja stjórnun gæða og ósamkvæmni](enable-quality-management.md)
- [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
