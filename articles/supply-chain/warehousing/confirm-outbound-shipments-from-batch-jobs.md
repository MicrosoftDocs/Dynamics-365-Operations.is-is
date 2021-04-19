---
title: Staðfesta sendingar á útleið úr runuvinnslum
description: Þetta efnisatriði lýsir því hvernig setja á upp runuvinnslu sem staðfestir sjálfkrafa sendingar flutningspantana á útleið fyrir farma sem eru tilbúnir fyrir afhendingu.
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 69e61e1c04dd72efbe1d2f028c078100e07176f6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838443"
---
# <a name="confirm-outbound-shipments-from-batch-jobs"></a>Staðfesta sendingar á útleið úr runuvinnslum

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig setja á upp runuvinnslu sem staðfestir sjálfkrafa sendingar flutningspantana á útleið fyrir farma sem eru tilbúnir fyrir afhendingu. Runuvinnslan sem lýst er hér gildir aðeins um sendingar flutningspantana, ekki sölupantanir.

## <a name="enable-the-confirm-outbound-shipments-from-batch-jobs-feature"></a>Virkja eiginleikann Staðfesta sendingar á útleið úr runuvinnslum

Áður en hægt er að nota þennan eiginleika þarf að virkja hann í kerfinu. Stjórnendur geta notað síðuna [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og virkjað hann ef þörf krefur. Eiginleikinn er skráður sem:

- **Eining** - *Vöruhúsakerfi*
- **Heiti eiginleika** - *Staðfesta sendingar á útleið úr runuvinnslum*

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