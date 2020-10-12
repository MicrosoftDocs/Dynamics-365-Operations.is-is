---
title: Nýtt notendaviðmót skjala í viðskiptaskjalastjórnun
description: Þetta efni veitir upplýsingar um hvernig nota á nýtt notendaviðmót (UI) skjals í viðskiptaskjalastjórnunaraðgerð rafrænna skýrslugerðar (ER) ramma.
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 015b595f85397fc1cf2c0368814ddc0369176f82
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893196"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Nýtt notendaviðmót skjala í viðskiptaskjalastjórnun

[!include [banner](../includes/banner.md)]

Business Document Management leyfir notendum að breyta sniðmátum viðskiptaskjala með Microsoft 365-þjónustu eða viðeigandi Microsoft Office skjáborðsforriti. Breytingar gætu innihaldið hönnunarbreytingar eða nýjar dreifingar, eða notendur gætu bætt við frátökutákni til að innihalda viðbótargögn án þess að þurfa að breyta kóðanum. Nánari upplýsingar um hvernig á að vinna með skjalastjórnun viðskipta, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).

Nýja notendaviðmót skjalanna (UI) er skýrara og þægilegra í notkun. Svæðið **Viðskiptaskjal** sýnir aðeins sniðmát sem eru í boði fyrir núverandi þjónustuaðila.

Hnappurinn **Nýtt skjal** gerir notendum kleift að búa til og breyta sniðmáti í rafrænni skýrslugerð (ER) sniði sem annar veitandi veitir. Í dæminu í þessu efni er veitan Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gerðu nýja skjalið UI í viðskiptaskjalastjórnun tiltækt

Til að byrja að nota nýja skjalið UI í viðskiptaskjalastjórnun verður þú að kveikja á eiginleikanum **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á vinnusvæðinu **Stjórnun eiginleika**.

Fylgdu þessum skrefum til að kveikja á þessum eiginleika fyrir alla lögaðila.

1. Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Nýtt**, velurðu eiginleikann **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á listanum.
2. Veldu **Virkja núna** til að kveikja á völdum eiginleika.
3. Endurnýjaðu síðuna til að fá aðgang að nýja eiginleikanum.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Breyta sniðmátum sem eru í eigu annarra veitenda

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala](./media/BDM_overview_new_template1.png)

2. Veldu skjalið til að nota sem sniðmát í valmyndinni og veldu síðan **Stofna skjal**.

    ![Gluggi viðskiptaskjala](./media/BDM_overview_new_template2.png)

3. Í nýja glugganum, í reitnum **Titill**, breytirðu titlinum eins og þú þarfnast. Titiltextinn er notaður til að nefna nýju skilgreiningu ER-sniðsins sem er sjálfkrafa búin til. Drög að þessari skilgreiningu (**Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)**) sem munu innihalda breytt sniðmát og verða notuð til að keyra þetta ER-snið fyrir núverandi notanda. Hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.
4. Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður sjálfkrafa stofnað.
5. Í reitnum **Athugasemd** skaltu uppfæra athugasemdinar fyrir breytanlega endurskoðun sem verður sjálfkrafa stofnuð.
6. Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

    ![Gluggi skjalagerðar](./media/BDM_overview_new_template3.png)

Hnappurinn **Nýtt skjal** er notaður til að búa til og breyta sniðmáti á ER-sniði sem annar veitandi veitir. Í þessu dæmi er veitan Microsoft. Þegar þú velur **Nýtt skjal** geturðu skoðað öll sniðmát sem eru í eigu núverandi og annarra veitenda. Eftir að þú velur sniðmátið verður það opnað fyrir breytingar. Síðan verður breytt sniðmátið geymt í nýrri skilgreiningu á ER-sniði sem er sjálfkrafa mynduð.

Fyrir frekari upplýsingar, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).
