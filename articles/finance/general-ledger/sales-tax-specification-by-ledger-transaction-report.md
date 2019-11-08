---
title: VSK-upplýsingar eftir fjárhagsfærslum (skýrsla)
description: Þetta efnisatriði útskýrir hvernig nota á skýrsluna VSK-upplýsingar eftir fjárhagsfærslum til að skoða og prenta upplýsingar um höfuðbókarviðskipti sem VSK-skattur er reiknaður út fyrir.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 1c36d9f8fb81a0a7e7a6de3db48cebdcf9d13b2d
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2019
ms.locfileid: "2591195"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>VSK-upplýsingar eftir fjárhagsfærslum (skýrsla)
[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig nota á skýrsluna **VSK-upplýsingar eftir fjárhagsfærslum** til að skoða og prenta upplýsingar um höfuðbókarviðskipti sem VSK-skattur er reiknaður út fyrir.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Skattalyklar samanborið við lykla sem ekki eru skattur

Skýrslan **VSK-upplýsingar eftir fjárhagsfærslum** sýnir skattafærslur bæði fyrir skattalykla og utan skatta. Þessir reikningar eru flokkaðir á eftirfarandi hátt:

- **Skattalykill** - Lykill er talinn skattalykill þegar skattafærsla er bókuð og aðallykillinn á færslubókarlínunni **Virðisaukaskattur** er skattalykill, svo sem greiðslulykill VSK eða viðskiptaskuldalykill VSK.
- **Lykill sem er ekki skattur** - Lykill er talinn tengjast ekki skatti þegar skattafærsla er bókuð og aðallykillinn á upprunalegri færslu er lykill sem tengist ekki skatti, svo sem tekjulykill eða kostnaðarlykill.

Fyrir skattalykla sýna dálkarnir **Uppruni**, **Innskattur** og **Útskattur** í skýrslunni **0** (núll). Fyrir lykla sem ekki eru skattur sýna þeir dálkar fjárhæðir.

## <a name="filtering-the-data-on-the-report"></a>Síun á gögnum í skýrslunni

Þegar skýrslan er mynduð eru eftirfarandi sjálfgefnir reitir tiltækir. Nota má þessai reiti til að sía út hvaða gögn eru sýnd í skýrslunni.

| Svæði                      | Lýsing |
|----------------------------|-------------|
| Dagsetning                       | Notaðu reitina í hlutunum **Frá** og **Til** til að skilgreina tímabil fyrir skattafærslur. |
| Aðallykill               | Notaðu reitina í hlutunum **Frá** og **Til** til að skilgreina tímabil fyrir aðallykla. |
| VSK-kóði             | Notaðu reitina í hlutunum **Frá** og **Til** til að skilgreina tímabil fyrir VSK-kóða. |
| Flokkun                   | Veldu hvort skýrslan eigi að vera flokkuð eftir fjárhagslykli eða VSK-kóða. |
| Millisamtala eftir VSK-kóða | Stilltu þennan valkost á **Já** til að sýna millisamstölur eftir VSK-kóða. |
| Eingöngu samtölur                | Stilltu þennan valkost á **Já** til að sýna aðeins samtölur. |
| Eingöngu aðallyklar         | Stilltu þennan valkost á **Já** til að taka innihalda aðallykla í skýrslunni. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Sýnir aðeins lykla án skatta í skýrslunni

Til að sýna aðeins lykla sem ekki eru skattar í skýrslunni skaltu setja upp síuskilyrði, svo sem stjörnu (\*), eins og sýnt er á eftirfarandi mynd.

![Skýrsla sem sýnir lykla án skatta](media/taxspecperledgertrans.png)
