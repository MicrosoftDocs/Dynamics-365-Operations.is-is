---
title: Vörusýnishorn gæðastjórnunar
description: Í þessu efnisatriði er lýst hvernig á að setja upp sýnatöku vöru.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 495bef32d63738e367167ee69f2028bc77945cc4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956692"
---
# <a name="quality-management-item-sampling"></a>Vörusýnishorn gæðastjórnunar

Sýnataka vöru er notuð sem hluti af gæðatengingu. Hún skilgreinir magn núverandi efnislegra birgða sem þarf að skoða. Sýnatökur geta verið byggðar á föstu magni, prósentu eða heillri númeraplötu.

## <a name="set-up-item-sampling"></a>Uppsetning vörusýna

Fylgið þessum skrefum til að setja upp sýnatöku vöru.

1. Farið í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Vörusýnishorn**.
1. Veljið **Nýtt**.
1. Í reitinn **Sýnataka vöru** skal færa inn gildi.
1. Sláið inn gildi í reitnum **Lýsing**.
1. Í reitnum **Gildi** skal slá inn númer. Þetta gildi tengist gildi fyrir tilgreint magn sem er valið í aðliggjandi reit.
1. Í hlutanum **Vinna úr** skal velja gátreitinn **Alger stöðvun** ef á að stöðva á alla lotuna eða magn pöntunarlínu ef próf mistekst. Ef þessi gátreitur er hreinsaður verða aðeins vörur í gæðapöntuninni stöðvaðar ef próf mistekst.
1. Veljið **Vista**.
1. Lokið síðunni.

> [!NOTE]
> Eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* bætir við nokkrum nýjum möguleikum fyrir vörusýnatöku. Það bætir við hugmyndinni um *umfang vörusýnatöku* og gerir þér kleift að skilgreina heila númeraplötu sem tilgreint magn. Ef þú hefur kveikt á þessum eiginleika skaltu skoða [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
