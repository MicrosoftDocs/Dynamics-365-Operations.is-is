---
title: Taka þyngd og rúmmál gáms með í hleðslu
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp og nota virkni til að taka með þyngd gáms og rúmtak í farmi.
author: Henrikan
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b42bd0b97564a493a50331d1424ca8084b389b29518f012f443d9cf722efe7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763916"
---
# <a name="include-container-weight-and-volume-on-load"></a>Taka þyngd og rúmmál gáms með í hleðslu

[!include [banner](../includes/banner.md)]

Virkni til aðtaka með taka með þyngd gáms og rúmtak í hleðslu gefur skýrt fram heildarþyngd og rúmmál gáma og vöru sem fer í farm.

Farmur inniheldur eina sendingu eða margar sendingar og þessar sendingar innihalda mismunandi vörur sem tilheyra einum söluáfangi eða mörgum sölufyrirmælum. Vörurnar eru geymdar í ílát, gámi og gámum er hlaðið í farm. Vörur sem ekki eru inni í gámi geta einnig verið hlit af farmi. Byggt á þessum skilyrðum, reiknar kerfið gildi fyrir þyngd og rúmmál í farminum með því að taka tillit til þyngdar og rúmmáls bæði gáma og hluta.

Ef reiknuð gildi eru ekki nákvæm, getur þú breytt þeim með því að slá inn raunveruleg gildi fyrir þyngd og rúmmál í farminum. Gildin fyrir þyngd og rúmmál eru notuð í flutningsstjórnunarferlum. Til dæmis eru gildin notuð á vinnusvæði leiðar þar sem þau hjálpa til við að skilgreina hraða og leið fyrir farma, og þau eru einnig notuð við flutningstilboð og innskráningu ökumanns.

## <a name="where-it-applies"></a>Þar sem það á við

Virknin til að taka með þyngd og rúmmál gáms í farmi gildir í flutningsstjórnunarferli, svo sem vinnusvæði leiðar, flutningstilboðum og innskráningu ökumanns.

## <a name="how-it-is-set-up"></a>Hvernig er það sett upp

Fjöldi gáma sem koma til greina fyrir farm er reiknað út frá þyngd og rúmmáli gáms og nýtingarhlutfalli gáms.

-   Til að stilla þyngd og rúmmál fyrir gám skal smella á **Vöruhúsastjórnun** \> **Uppsetning** \> **Gámar** \> **Gámagerð**.

-   Til að stilla gámanýtingarhlutfallið, smelltu á **Vöruhúsastjórnun** \> **Uppsetning** \> **Gámar** \> **Gámaflokkar** og sláðu síðan inn gildi í reitinn **Nýtingarhlutfall gáms**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]