---
title: Vörusýnishorn gæðastjórnunar
description: Þessi grein lýsir því hvernig á að setja upp sýnatöku vöru.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 644eae4fbd9f82027c1cb69efba00dc893f8fc66
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8865151"
---
# <a name="quality-management-item-sampling"></a>Vörusýnishorn gæðastjórnunar

[!include [banner](../includes/banner.md)]

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
