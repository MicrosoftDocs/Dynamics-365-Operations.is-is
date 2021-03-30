---
title: Stofna leiguhóp
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp leigusamningsflokka. Leigusamningsflokkar eru nauðsynlegir til að búa til nýja leigusamninga.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8ad226e87776615d9c19a239e0fb90b648d9c49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210458"
---
# <a name="create-a-lease-group"></a>Stofna leiguhóp

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp leigusamningsflokka. Leigusamningsflokkar eru nauðsynlegir til að búa til nýja leigusamninga. Leigubækur eru tengdar við hvern leigusamningsflokk. Leigubækur ákvarða sjálfgefnu bækurnar sem þarf að stofna fyrir hverja leigu. Hægt er að úthluta tilteknum lyklum á leiguflokk á síðunni **Færibreytur leigubókunar**.

## <a name="create-a-lease-book-and-add-a-lease-group"></a>Stofna leigubók og bæta við leigusamningsflokki

1. Opnið **Eignarleiga \> Uppsetning \> Leigusamningsflokkar**.
2. Á aðgerðasvæðinu skal velja **Ný** til að bæta við leigusamningsflokki. Línu er bætt við hnitanetið.
3. Í nýju línunni, í reitnum **Leigusamningsflokkur** skal slá inn gildi.
4. Sláið inn gildi í reitnum **Lýsing**.

Upplýsingunum sem voru slegnar inn er bætt við svæðið **Leigusamningsflokkur** á síðunni **Bæta við leigusamningi**.

## <a name="associate-a-book-with-a-lease-group"></a>Tengja bók við leigusamningsflokk

Þegar búið er að stofna leigusamningsflokka er hægt að úthluta bókum í hvern hóp. Þegar búið er að stofna leigusamning og úthluta honum á leiguflokk stofnar kerfið áætlun fyrir hverja bók sem tengist þessum leigusamningsflokki.

> [!NOTE]
> Setja verður upp bækur áður en hægt er að úthluta þeim á leigusamningsflokk.

1. Opnið **Eignarleiga \> Uppsetning \> Leigusamningsflokkur**.
2. Veljið leigusamningsflokk og svo **Bækur**.
3. Veljið **Nýtt** og síðan, á svæðinu **Bókargerð**, bókina sem á að úthluta á leigusamningsflokkinn. Hægt er að úthluta mörgum bókum á leigusamningsflokk ef taka þarf tillit til leigusamnings á mismunandi hátt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]