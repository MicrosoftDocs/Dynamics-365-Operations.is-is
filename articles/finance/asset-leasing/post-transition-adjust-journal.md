---
title: Bóka færslur umbreytingar leiðréttingarbókar í eignarleigu
description: Þetta efnisatriði lýsir virkninni sem gerir þér kleift að umbreyta safni leigusamninga í nýjar bókhaldsreglur um leigusamninga, efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4af7b9dc7a03a6d17ff34ffc726eb87e848dd785
ms.sourcegitcommit: f0f5545a8ff99583e0131f435d91c64bb68a1c38
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/30/2020
ms.locfileid: "4444596"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a>Bóka færslur umbreytingar leiðréttingarbókar í eignarleigu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir virkninni sem gerir þér kleift að umbreyta safni leigusamninga í nýjar bókhaldsreglur um leigusamninga: Efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) sem er staðall fyrir almennt samþykktar reikningsskilareglur í Bandaríkjunum (US GAAP) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16).

Frekari upplýsingar um hvernig á að setja upp bók til umbreytingar í nýju staðlana að finna í [Setja upp leigubækur](set-up-lease-books.md).

Þegar stofnuð er færsla umbreytingar leiðréttingabókar er bókarfærsla stofnuð. Þessi færsla endurspeglar áhrif efnahagsreiknings með því að skrá leigusamninginn samkvæmt nýjum stöðlunum á þeirri dagsetningu. Viðeigandi eignalykill er debetfærður fyrir bókfært virði á þeirri dagsetningu og skuldalykillinn er kreditfærður. Mismunurinn er annaðhvort debetfærður eða kreditfærður í óráðstafað eigið fé.

Til að bóka leiðréttingu umbreytingar samkvæmt nýju bókhaldsstöðlunum skal fylgja þessum skrefum.

1. Á síðunni **Samantekt leigu** skal velja leiguna og síðan **Bækur**.
2. Í bókinni skal velja **Greiðsluáætlun**.
3. Í svarglugganum **Greiðsluáætlun** skal velja **Staðfesta**. Lokið svo svarglugganum.
4. Veljið **Leiðrétting umbreytingar**.

    > [!NOTE]
    > Aðeins er hægt að stofna leiðréttingu umbreytingar fyrir leigubækur sem er úthlutað á bók þar sem svæðið **Umbreytingarbók** er tiltækt. Ef gildið í svæðinu **Upphafsdagsetning leigusamnings** er síðar en umbreytingardagsetningin verður gildið í svæðinu **Leiðrétting umbreytingar** ekki uppfært.

5. Til að skoða bókarfærsluna skal velja **Færslubækur eignarleigu**.
6. Veldu nýja bók og veldu síðan **Bóka**.
