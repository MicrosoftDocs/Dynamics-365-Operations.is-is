---
title: Biðgeymslupantanir
description: Þessi grein lýsir því hvernig á að nota sóttkvíspantanir til að loka á birgðum.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3ee1ba338d90c6ee9cdc37948061f518040ae1a1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8869663"
---
# <a name="quarantine-orders"></a>Biðgeymslupantanir

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að nota sóttkvíspantanir til að loka á birgðum.

Með biðgeymslupöntun geturðu lokað á birgðir. Til dæmis gætir þú viljað láta vörur í biðgeymslu vegna gæðaeftirlits. Birgðir sem hafa verið settar í biðgeymslu eru fluttar í biðgeymsluvöruhús.

> [!NOTE]
> Ef verið er að nota ítarlegt vöruhúsakerfisferli (í vöruhúsakerfi) er vinnsla pantana í biðgeymslu einungis notuð fyrir skil á sölupöntunum.

## <a name="quarantine-on-hand-inventory-items"></a>Vörur biðgeymslubirgða á lager

Þegar vörur eru settar í biðgeymslu geturðu annaðhvort stofnað biðgeymslupantanir handvirkt eða sett upp kerfið til að stofna þær sjálfkrafa í ferli á innleið.

Fylgið eftirfarandi skrefum til að setja kerfið upp þannig að það búi sjálfkrafa til biðgeymslupantanir.

1. Opnið **Birgðastjórnun \> Uppsetning \> Birgðir \> Vörulíkanaflokkar.**
1. Veljið viðeigandi líkanahóp á listasvæði eða stofnið nýjan líkanahóp.
1. Í flýtiflipanum **Birgðareglur** skal velja gátreitinn **Biðgeymslustjórnun**.
1. Lokið síðunni.
1. Tilgreinið sjálfgefið biðgeymsluvöruhús í svæðinu **Biðgeymsluvöruhús** fyrir móttökuvöruhúsin.

Þegar var sem er skráð sem móttekin í vöruhúsinu sem tilheyrir líkanaflokki þar sem gátreiturinn **Biðgeymslustjórnun** er valinn, býr kerfið til biðgeymslupöntun fyrir hana. Í biðgeymslupöntuninni er starfskröftum gefin fyrirmæli um að flytja vöruna í biðgeymsluvöruhúsið.

Þegar þú stofnar biðgeymslupantanir handvirkt á síðunni **Biðgeymslupantanir** þarf varan ekki að vera sett upp fyrir biðgeymslustjórnun í tengdum vörulíkanaflokki. Fyrir þetta ferli þarf að tilgreina biðgeymsluvöruhús sem á að nota og birgðir á lager sem á að setja í biðgeymslu. Það er hægt að nota stöðu biðgeymslupöntunar til að auðvelda áætlun ferlisins.

## <a name="quarantine-order-statuses"></a>Staða biðgeymslupöntunar.

Biðgeymslupantanir geta haft eftirfarandi stöðu:

- Stofnaður
- Hafin
- Tilgreint sem tilbúið
- Lokið

### <a name="created"></a>Stofnaður

Þegar Biðgeymslupöntunin er stofnuð handvirkt en varan er ekki enn staðsett í biðgeymsluvöruhúsinu, fær biðgeymslupöntunin stöðuna **Stofnað**. Tvær birgðafærslur eru myndaðar: Ein færslan er úthreyfingarfærsla sem getur haft stöðuna **Í pöntun**, **Frátekið á lager**, eða **Tiltekið**. Hin færslan er innhreyfingarfærsla sem getur haft stöðuna **Pantað** eða **Skráð** í biðgeymsluvöruhúsinu. Hægt er að taka frá, taka til og skrá uppfærslur á birgðum með því að nota vanalegt ferli.

### <a name="started"></a>Hafin

Þegar biðgeymslupöntun er í stöðunni **Hafin** eru vörurnar færðar úr hefðbundna vöruhúsinu í biðgeymsluvöruhúsið og eru tvær birgðafærslur myndaðar. Ein færsla hefur stöðuna **Frádregið**, og önnur færslan hefur stöðuna **Móttekið**. Á sama tíma eru einnig tvær birgðafærslur myndaðar til að annast skilafærsluna. Þessar færslur fá ekki dagsetningu. Ein færsla hefur stöðuna **efnislega frátekið**, og önnur færslan hefur stöðuna **pantað**.

### <a name="reported-as-finished"></a>Tilbúið

Til að tilkynna hafna biðgeymslupöntun sem lokna er hún opnuð og valið **Tilkynna sem lokið** á aðgerðasvæðinu. Varan er leyst úr biðgeymslu en hún er ekki færð aftur í vanalega vöruhúsið. Þetta er hægt að vinna með vörukomubók sem má frumstilla á meðan ferlið Bóka sem tilbúið er enn í gangi.

### <a name="ended"></a>Búið

Þegar biðgeymslupöntun er lokið er vara færð úr biðgeymsluvöruhúsi og aftur í vanalegt vöruhús. Staða vörufærslunnar er stillt á *Selt* í biðgeymsluvöruhúsinu og *Keypt* í venjulegt vöruhús.

## <a name="quarantine-order-scrap"></a>Rýrnun Biðgeymslupöntunar

Hægt er að rýra birgðir sem hluta af biðgeymslupöntunarferlinu. Við vinnslu á rýrnun er staða birgða stillt á *Selt* með úthreyfingarfærslu úr biðgeymsluvöruhúsi.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Stöðvun í birgðum](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
