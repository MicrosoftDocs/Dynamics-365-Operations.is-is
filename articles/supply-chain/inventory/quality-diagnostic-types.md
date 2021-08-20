---
title: Gerðir greininga fyrir ósamkvæmni
description: Í þessu efnisatriði er lýst hvernig eigi að nota og búa til greiningartegundir sem hægt er að nota með ósamkvæmi.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestDiagnosticType, InventTestCorrection
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 560627bf5ecd38f3fc79448629390acb549e40fb1388958d9eac094517925039
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781514"
---
# <a name="diagnostic-types-for-nonconformances"></a>Gerðir greininga fyrir ósamkvæmni

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er lýst hvernig eigi að nota og búa til greiningartegundir sem hægt er að nota með ósamkvæmi.

Notaðu **Greiningargerðir** síðuna til að skilgreina flokkun greiningaraðgerða. Þegar leiðrétting er svo stofnuð vegna ósamræmis er greining valin. Leiðrétting auðkennir hvers konar greiningaraðgerð á að framkvæma á samþykktri ósamkvæmni, hver á að framkvæma hana. Hún tilgreinir einnig umbeðin lokadagsetning og áætluð lokadagsetning.

## <a name="examples-of-diagnostic-types"></a>Dæmi um greiningagerðir

Þú vinnur hjá framleiðslufyrirtæki og nokkrar vörur hafa fallið á gæðaprófunum. Þessir hlutir eru fluttir inn á biðgeymsluna og merktir sem ósamræmdar vörur. Ósamkvæmniskýrsla er stofnuð í Microsoft Dynamics 365 Supply Chain Management til að rekja upplýsingar í gegnum lausn vandamála.

Í þessu tilviki eiga gæðavandamálin sér stað vegna þess að legur í vélinni sem pakkar vörunum hafa skemmst og ofhitna. Lausnin við þessu vandamáli er að skipta um íhluti í vélinni.

Þegar þú skilgreinir greiningargerðirnar geturðu stofnað margar færslur, hver þeirra stendur fyrir mismunandi tegundir vandamála sem steðja að vélinni. Einnig er hægt að stofna eina almenna greiningartegund sem táknar vélarviðgerð.

## <a name="create-a-diagnostic-type"></a>Stofna gerð greiningar

1. Fara í **Birgðastjórnun \> Uppsetningu \> gæðastjórnun \> gerðir Greininga**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta línu við hnitanetið. Stillið svo eftirfarandi reiti fyrir nýju línuna:

    - **Greining** – Færið inn einkvæmt kenni eða heiti fyrir greiningargerðina.
    - **Lýsing** – Færið inn ítarlega lýsingu á greiningargerðinni.

1. Lokið síðunni.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Gæðastjórnunaryfirlit](quality-management-processes.md)
- [Virkja stjórnun gæða og ósamkvæmni](enable-quality-management.md)
- [Starfsmenn ábyrgir fyrir samþykki ósamkvæmni](quality-responsible-workers.md)
- [Biðgeymslusvæði fyrir ósamkvæmi](quality-quarantine-zones.md)
- [Gerðir vandamála fyrir ósamkvæmni](quality-problem-types.md)
- [Gæðagjöld fyrir ósamkvæmi](quality-charges.md)
- [Aðgerðir fyrir ósamkvæmni.](quality-operations.md)
- [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
