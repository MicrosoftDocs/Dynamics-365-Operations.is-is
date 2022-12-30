---
title: Staðfesta sendingar á útleið úr runuvinnslum
description: Þessi grein lýsir því hvernig setja á upp runuvinnslu sem staðfestir sjálfkrafa sendingar flutningspantana á útleið fyrir farma sem eru tilbúnir fyrir afhendingu.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 00749a69b17b0064290d7b41ccb2171386716302
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875102"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Staðfesta sendingar á útleið úr runuvinnslum

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig setja á upp runuvinnslu sem staðfestir sjálfkrafa sendingar flutningspantana á útleið fyrir farma sem eru tilbúnir fyrir afhendingu. Runuvinnslan sem lýst er hér gildir aðeins um sendingar flutningspantana, ekki sölupantanir.

## <a name="turn-the-confirm-outbound-shipments-from-batch-jobs-feature-on-or-off"></a>Kveikja eða slökkva á eiginleikanum „Staðfesta sendingar á útleið úr runuvinnslum“

Til að nota virknina sem lýst er í þessari grein þarf að kveikja á eiginleikanum *Staðfesta sendingar á útleið úr runuvinnslum* fyrir kerfið. Sem hluti af Supply Chain Management, útgáfa 10.0.21, er sjálfgefið kveikt á þessum eiginleika. Frá og með útgáfu 10.0.25 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á henni. Ef þú ert að keyra útgáfu sem er eldri en 10.0.25, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Staðfesta sendingar á útleið úr runuvinnslum* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="process-outbound-shipments"></a>Vinna úr sendingum á útleið

Til að setja upp áætlaða runuvinnslu til að keyra staðfestingu á sendingu á útleið fyrir farma sem eru tilbúnir til afhendingar:

1. Farið í **Vöruhúsakerfi \> Reglubundin verk \> Vinna úr sendingum á útleið**.
1. Svarglugginn **Staðfesta sendingu** opnast. Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.
1. Svargluggi fyrirspurnarritils opnast. Í flipanum **Svið** skal bæta við línu með eftirfarandi gildum:
    - **Tafla** - *Farmar*
    - **Afleidd tafla** - *Farmar*
    - **Reitur** - *Farmstaða*
    - **Skilyrði** - *Hlaðinn*
1. Veljið **Í lagi** til að fara aftur í svargluggann **Staðfesta sendingu**.
1. Í flýtiflipanum **Keyra í bakgrunni** skal stilla **Runuvinnsla** á **Já**.
1. Í flýtiflipanum **Keyra í bakgrunni** skal velja **Endurtekning**.
1. Svarglugginn **Skilgreina endurtekningu** opnast. Stillið keyrslu áætlunar eftir þörfum fyrir fyrirtækið.
1. Veljið **Í lagi** til að fara aftur í svargluggann **Staðfesta sendingu**.
1. Veljið **Í lagi** í svarglugganum **Staðfesta sendingu** til að bæta runuvinnslunni við runubiðröðina.

Nánari upplýsingar er að finna í [Yfirlit runuvinnslu](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]