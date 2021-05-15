---
title: Birgðaleiðrétting vöruhúss
description: Í þessu efnisatriði er að finna upplýsingar um birgðaleiðréttingabók vöruhúss og úrvinnslu þegar einingakvarðar eru notaðir.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938227"
---
# <a name="warehouse-inventory-adjustment"></a>Birgðaleiðrétting vöruhúss

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Birgðaleiðréttingareiginleiki vöruhúss er notaður þegar einingakvarðar skýs og jaðra er keyrt fyrir [vinnuálag framleiðslu](cloud-edge-workload-manufacturing.md) og [vinnuálag vöruhúsakerfis](cloud-edge-workload-warehousing.md).

Þegar starfsmaður framkvæmir birgðaleiðréttingu með því að nota vöruhúsaforritið gagnvart einingakvarða vinnuálags vöruhúsakerfis verður runuvinnslan **Birgðaleiðréttingabók vöruhúss** að vinna úr uppfærslu efnislegra birgða sem er keyrð og tímasett með því að fara í **Vöruhúsakerfi > Reglubundin verk > Birgðaleiðréttingabók vöruhúss**.

Eftirfarandi vinnuferli vöruhúsaforrits notar **Birgðaleiðréttingabók vöruhúss** í vinnuálagi einingakvarða:

- Leiðrétting (inn/út)
- Regluleg talning
- Hleðsla númeraplötu

Nokkrar birgðafærslur eru stofnaðar sem hluti af skýi og jaðri í ferli birgðaleiðréttingar vegna þess að uppsetningar miðstöðvar og einingakvarða deila birgðafærslum.

## <a name="inventory-adjustment-example"></a>Dæmi um birgðaleiðréttingu

Í þessu dæmi hefur starfsmaður í vöruhúsi notað vöruhúsaforritið til að skrá lagerbirgðir sem bætt er við.

Fyrst býr vinnuálag einingakvarða til birgðaleiðréttingafærslu vöruhúss fyrir jákvæða efnislega leiðréttingu sem er síðan samstillt við miðstöðina og leiðir til aukningar á lagerbirgðum í miðstöðinni.

| Gerð                                    | Kvörðunareining | Stefna | Stöð |
|-----------------------------------------|------------|-----------|-----|
| Birgðaleiðrétting vöruhúss          | +1         | ->        | +1  |

Miðstöðin vinnur síðan úr bókun talningabókar sem er síðan móttekin í gegnum [skilaboð skilaboðaúrvinnslu](cloud-edge-message-processor-messages.md). Þetta uppfærir viðbótarbirgðir á lager. Til að koma í veg fyrir tvöfladar birgðir á lager býr miðstöðin til mótfærslu sem hluta af þessu ferli og fjarlægir fyrri skráðar lagerbirgðir sem tengjast birgðaleiðréttingu vöruhússins.

| Gerð                                    | Kvörðunareining | Stefna | Stöð |
|-----------------------------------------|------------|-----------|-----|
| Talning                                | +1         | <-        | +1  |
| Birgðaleiðrétting vöruhúss (mótfærsla) | -1         | <-        | -1  |

Þegar einingakvarði hefur búið til **Birgðaleiðréttingabók vöruhúss** í miðstöðinni er hægt að yfirfara bæði **Talningarbók** og **Jöfnunarbók** sem miðstöðin stofnar sem hluta af breytingaferlinu.

Þú getur farið yfir allar þessar dagbókarfærslur og færslur í Supply Chain Management með því að gera framkvæma skref:

1. Skráðu þig inn á kvörðunareiningu.
1. Farið í **Vöruhúsakerfi \> Reglubundin verk \> Birgðaleiðréttingabók vöruhúss**.
1. Á síðunni **Birgðaleiðréttingabók vöruhúss** skal finna og opna færslubókina sem skráði breytingu lagerbirgða. Hlutinn **Færslubókarlínur** sýnir hverja leiðréttingu sem þessi færslubók hefur skráð.
1. Skráðu þig inn í miðstöðina.
1. Farið í **Vöruhúsakerfi \> Reglubundin verk \> Birgðaleiðréttingabók vöruhúss**.
1. Á síðunni **Birgðaleiðréttingabók vöruhúss** ættirðu að sjá sömu færslubókina sýnda ef miðstöðin og einingakvarðinn eru samstillt.
1. Opna færslubókina Ef unnið hefur verið úr [skilaboðum skilaboðaúrvinnslu](cloud-edge-message-processor-messages.md) sjást tenglar á **Talningarbókina** og **Jöfnunarbókina** í hausnum.
    - **Talningarbókin** á að sýna sömu víddargildin og færslubókarlínurnar.
    - **Jöfnunarbókin** á að sýna mótfærsluna, sem fjarlægir tvöföldu birgðaleiðréttinguna.
    > [!NOTE]
    > Þegar allri samstillingu og úrvinnslu er lokið eru **Talningarbókin** og **Jöfnunarbókin** samstillt aftur í einingakvarðann. Þessar upplýsingar er einnig hægt að skoða á viðkomandi **Birgðaleiðréttingabók vöruhúss** síðu.
