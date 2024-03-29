---
title: Sniðmát hleðslu
description: Þessi grein lýsir því hvernig eigi að setja upp farmsniðmát og hvernig á að tengja farmsniðmát við í nýjan farm.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 47b4925c528b64b835ce3e88659ee6ab0572eb2b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844181"
---
# <a name="load-templates"></a>Sniðmát hleðslu

[!include [banner](../../includes/banner.md)]

Þegar ný hleðsla er búin til er hægt að úthluta hleðslusniðmáti. Hleðslusniðmátið inniheldur upplýsingar um búnað, og um mælingar á borð við hæð, breidd, dýpt og rúmmál hleðslunnar.

Þessi grein lýsir því hvernig eigi að setja upp farmsniðmát og hvernig á að tengja farmsniðmát við í nýjan farm.

## <a name="set-up-a-load-template"></a>Setja upp hleðslusniðmát

1. Farið í **-flutningsstjórnun \> Uppsetning \> Hleðsluáætlun \> Hleðslusniðmát**.
1. Á aðgerðasvæðinu skal velja **Ný** til að bæta við nýju sniðmáti eða **Breyta** til að breyta fyrirliggjandi sniðmáti.
1. Í línunni fyrir nýtt eða fyrirliggjandi sniðmát skal stilla eftirfarandi reiti:

    - Í reitnum **Auðkenni hleðslusniðmáts** færirðu inn einkvæmt kenni fyrir hleðslusniðmátið.
    - **Búnaður** - Veljið búnað sem á að nota til að senda farminn.
    - **Hæð farms**, **Breidd farms** og **Dýpt farms** – Sláðu inn mál farmsins.
    - **Leyfilegt ummál farms að hámarki** og **Þyngd farms að hámarki** – Sláðu inn leyfilegt ummál og leyfilega þyngd farms að hámarki.
    - **Hámarks leyfileg brúttóþyngd** – Sláið inn hámarks leyfilega brúttóþyngd hleðslunnar. Brúttóþyngd farms inniheldur bæði umbúðaþyngd hans og hleðsluþyngd.
    - **Hámarksfjöldi leyfilegra farmhluta** – Færið inn hámarksfjölda farmhluta sem farmurinn getur innihaldið.
    - **Staflahleðsla á gólfi** – Veljið þennan gátreit til að nota gólfhleðslu. Við aðstæður þegar hlaðið er á gólf, er kössum staflað frá gólfi upp í loft, vegg til veggjar innan í gámnum til að hámarksnýta rýmið.

1. Í aðgerðarúðunni skal velja **Vista**.

## <a name="associate-a-load-template-with-a-new-load"></a>Tengja álagssniðmát við nýja álag

1. Farið í **Flutningsstjórnun \> Áætlanagerð \> Vinnusvæði hleðsluáætlunar**.
1. Í efri hluta síðunnar skal velja einn af eftirfarandi flipum, allt eftir gerð upprunaskjalsins sem verið er að búa til farm fyrir: **Sendingar**, **Sölulínur**, **Flutningslínur** eða **Innkaupapöntunarlínur**. 
1. Veljið tiltekið skjal til að áætla hleðsluna fyrir.
1. Á aðgerðasvæðinu, í flipanum **Framboð og eftirspurn**, í flokknum **Bæta við**, skal velja **Við nýjan farm**.
1. Í svarglugganum **Úthlutun hleðslusniðmáts**, í reitnum **Kenni hleðslusniðmáts**, skal velja sniðmátið sem á að nota.
1. Veljið **Í lagi** til að nota sniðmátið.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]