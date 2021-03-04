---
title: Biðgeymslupantanir
description: Þetta efnisatriði lýsir því hvernig biðgeymslupantanir eru notaðar til að loka birgðum.
author: perlynne
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25ba4aa92d968f4dfb0dc23b1ac459cda2d52b61
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430607"
---
# <a name="quarantine-orders"></a>Biðgeymslupantanir

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig biðgeymslupantanir eru notaðar til að loka birgðum.

Hægt er að nota Biðgeymslupantanir til að loka birgðum. Til dæmis gætir þú viljað láta vörur í biðgeymslu vegna gæðaeftirlits. Birgðir sem hafa verið settar í biðgeymslu eru fluttar í biðgeymsluvöruhús. **Athugasemd:** Ef verið er að nota ítarlegt vöruhúsakerfisferli (í vöruhúsakerfi) er vinnsla pantana í biðgeymslu einungis notuð fyrir skil á sölupöntunum.

## <a name="quarantine-on-hand-inventory-items"></a>Vörur biðgeymslubirgða á lager
Þegar vara er sett í biðgeymslu geturðu annað hvort stofnað biðgeymslupantanir handvirkt eða stillt kerfið til að stofna biðgeymslupantanir sjálfkrafa við ferli á innleið. Til að stofna biðgeymslupantanir sjálfkrafa, veljið **Stjórnun Biðgeymslu** valkostinn í flipanum **Birgðareglur** á síðunni **Vörulíkanaflokkar**. Einnig þarf að tilgreina sjálfgefið biðgeymsluvöruhús í svæðinu **Biðgeymsluvöruhús** fyrir móttökuvöruhúsin. Í Supply Chain Management eru vörur í biðgeymslu sjálfkrafa settar í biðgeymsluvöruhús þegar efnislegar birgðir á lager eru skráðar gegnum innkaupapöntun eða framleiðslupöntun. Þessa hreyfing gerist vegna þess að stöðu biðgeymslupöntunar hefur verið breytt í **Byrjað**. Þegar þú stofnar biðgeymslupantanir handvirkt, þarf varan ekki að vera sett upp fyrir biðgeymslustjórnun í tengdum vörulíkanaflokkum. Fyrir þetta ferli þarf að tilgreina biðgeymsluvöruhús sem á að nota og birgðir á lager sem á að setja í biðgeymslu. Það er hægt að nota stöðu biðgeymslupöntunar til að auðvelda áætlun ferlisins.

## <a name="quarantine-order-statuses"></a>Staða biðgeymslupöntunar.
Biðgeymslupantanir geta haft eftirfarandi stöðu:

-   Stofnaður
-   Hafin
-   Tilgreint sem tilbúið
-   Lokið

### <a name="created"></a>Stofnaður

Þegar Biðgeymslupöntunin er stofnuð handvirkt en varan er ekki enn staðsett í biðgeymsluvöruhúsinu, fær biðgeymslupöntunin stöðuna **Stofnað**. Tvær birgðafærslur eru myndaðar: Ein færslan er úthreyfingarfærsla sem getur haft stöðuna **Í pöntun**, **Frátekið á lager**, eða **Tiltekið**. Hin færslan er innhreyfingarfærsla sem getur haft stöðuna **Pantað** eða **Skráð** í biðgeymsluvöruhúsinu. Hægt er að taka frá, taka til og skrá uppfærslur á birgðum með því að nota vanalegt ferli.

### <a name="started"></a>Hafin

Þegar biðgeymslupöntun er í stöðunni **Hafin** eru vörurnar færðar úr hefðbundna vöruhúsinu í biðgeymsluvöruhúsið og eru tvær birgðafærslur myndaðar. Ein færsla hefur stöðuna **Frádregið**, og önnur færslan hefur stöðuna **Móttekið**. Á sama tíma eru einnig tvær birgðafærslur myndaðar til að annast skilafærsluna. Þessar færslur fá ekki dagsetningu. Ein færsla hefur stöðuna **efnislega frátekið**, og önnur færslan hefur stöðuna **pantað**.

### <a name="reported-as-finished"></a>Tilgreint sem tilbúið

Með því að smella á **Bóka sem tilbúið** er hægt að tilkynna byrjaða biðgeymslupöntun sem tilbúna. Varan er leyst úr biðgeymslu en hún er ekki færð aftur í vanalega vöruhúsið. Þetta er hægt að vinna með vörukomubók sem má frumstilla á meðan ferlið Bóka sem tilbúið er enn í gangi.

### <a name="ended"></a>Lokið

Þegar biðgeymslupöntun er lokið er vara færð úr biðgeymsluvöruhúsi og aftur í vanalegt vöruhús. Staða vörufærslunnar er stillt á **Selt** í biðgeymsluvöruhúsinu og **Keypt** í venjulegt vöruhús.

## <a name="quarantine-order-scrap"></a>Rýrnun Biðgeymslupöntunar
Hægt er að rýra birgðir sem hluta af biðgeymslupöntunarferlinu. Við vinnslu á rýrnun verður staða birgða stillt á **Selt** með úthreyfingarfærslu úr biðgeymsluvöruhúsi.

<a name="additional-resources"></a>Frekari upplýsingar
--------

[Stöðvun í birgðum](inventory-blocking.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]