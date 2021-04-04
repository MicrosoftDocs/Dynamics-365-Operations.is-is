---
title: Safnvistun útprentaðra reikninga viðskiptavina með tætigildum
description: Þetta efnisatriði útskýrir hvernig á að virkja safnvistun til þess að geyma prentaða reikninga viðskiptavina með tætigildum.
author: ilyako
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d502ec5d286573c72e207419b66f283183009c09
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557481"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Safnvistun útprentaðra reikninga viðskiptavina með tætigildum

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Í sumum löndum eru lagalegar kröfur um að geyma reiknuð tætigildi í kerfinu ásamt útprentun á sömu skjala. Tætigildi er hægt að nota til að tilkynninga yfirvöldum og við endurskoðun.

Þetta efnisatriði útskýrir hvernig á að skilgreina safnvistun til þess að geyma prentaða reikninga viðskiptavina með tætigildum.

## <a name="prerequisites"></a>Forkröfur

- Á vinnusvæðinu **Eiginleikastjórnun** skal kveikja á eiginleikanum **Safnvistun útprentaðra reikninga viðskiptavina með tætigildum**. Frekari upplýsingar er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Skilgreinið prentvæn snið nauðsynlegra skjala í **Prentstýringu**.

Virknin gildir um eftirfarandi skjöl.

**Viðskiptakröfur**
- Reikningur viðskiptavina
- Kreditnóta viðskiptavina
- Textareikningur
- Textakreditnóta

**Verkefnastjórnun og bókhald**
- Verkreikningur
- Kreditnóta verks

## <a name="configure-customer-master-data"></a>Skilgreina aðalgögn viðskiptavinar
Ljúkið eftirfarandi skrefum til að skilgreina gögn viðskiptavinar og kveikið á sjálfvirkri vistun útprentaðra reikninga sem viðhengi.

1. Farið í **Viðskiptakröfur** > **Allir viðskiptavinir**. 
2. Veljið viðskiptavin og í flýtiflipanum **Reikningur og afhending**, í hlutanum **Rafrænn reikningur**, í reitnum **Rafrænn reikningur í viðhengi**, skal velja **Já**.

## <a name="print-invoices"></a>Prenta reikninga
Hægt er að bóka og prenta út alla frjálsa texta, viðskiptavini og verkreikninga eða kreditnótur fyrir viðskiptavininn sem er skilgreindur í ferlinu hér á undan.

Opnið síðuna **Viðhengi** fyrir prentaðan reikning. Í flýtiflipanum **Viðhengi**, í reitahópnum **Frekari upplýsingar**, í reitnum **Tætinúmer skjals**, skal leita að geymdu tætigildi sem var reiknað út fyrir prentaðan reikning.

![Tætinúmer viðhengis](media/attach-hash-num.jpg)

