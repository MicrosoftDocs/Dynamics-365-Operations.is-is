---
title: Stofna leiguhóp
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp leigusamningsflokka. Leigusamningsflokkar eru nauðsynlegir til að búa til nýja leigusamninga.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 49a905e9f27f01898628e88c7af781aed1f25ec7
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714146"
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
