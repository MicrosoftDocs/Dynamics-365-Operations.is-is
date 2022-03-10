---
title: Búðu til hnattvæðingareiginleika
description: Þetta efni útskýrir hvernig á að búa til hnattvæðingareiginleika.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 197a5b983b307758425b1acc1f354d0a8bfbf8a1
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371958"
---
# <a name="create-a-globalization-feature"></a>Búðu til hnattvæðingareiginleika

[!include [banner](../includes/banner.md)]

Þú getur búið til eiginleika fyrir rafræna reikninga frá grunni, eða þú getur byggt hann á núverandi eiginleika. Þegar þú býrð til eiginleika frá grunni, verður þú að bæta handvirkt við rafrænum skýrslugerðum (ER) stillingum og öðrum hlutum, svo sem uppsetningu eiginleika og uppsetningu forrits. Þegar þú býrð til eiginleika sem er byggður á núverandi eiginleika, erfir nýi eiginleikinn allar grunnstillingar og færibreytur grunneiginleikans. Þú getur skoðað hvað er afritað úr grunneiginleikanum yfir í nýja eiginleikann.

## <a name="create-a-feature-from-scratch"></a>Búðu til eiginleika frá grunni

Þessi hluti útskýrir hvernig á að búa til rafrænan reikningseiginleika þegar enginn hnattvæðingareiginleiki er tiltækur í alþjóðlegu geymslunni fyrir viðskiptasviðsmyndir þínar úr kassanum.

Fylgdu þessum skrefum til að búa til eiginleika rafrænna reikninga.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Veldu **Bæta við**, og veldu síðan í fellivalglugganum **Nýr eiginleiki** valmöguleika.
4. Sláðu inn nafn og lýsingu fyrir eiginleika rafrænna reikninga.
5. Veljið **Stofna eiginleika**. Fyrsta útgáfan af nýja eiginleikanum birtist hægra megin á síðunni og hefur stöðuna **Drög**.

    Næst verður þú að bæta við ER stillingum og eiginleikauppsetningum. Áður en þú bætir við nýjum eða núverandi ER sniðstillingum skaltu ganga úr skugga um að þær séu til í RCS geymslunni þinni.

6. Veldu rafræna reikningseiginleikann sem þú ert að vinna að.
7. Í flipanum **Skilgreiningar** skal velja **Bæta við**.
8. Í **Stillingar** grid, flettu að og veldu sniðstillingar sem eru nauðsynlegar fyrir vinnsluleiðsluna (til dæmis til að búa til rafrænar reikningaskrár eða vinna úr svörum frá ytri vefþjónustu).
9. Veldu **Í lagi**. Þú getur nú notað stillingar í aðgerðum vinnsluleiðslunnar. Fyrir frekari upplýsingar, sjá [Vinna með stillingar](e-invoicing-work-configurations.md).
10. Til að bæta við uppsetningu rafrænna reikningaeiginleika skaltu búa hana til á **Uppsetningar** flipi á **Nýr eiginleiki** síðu. Fyrir frekari upplýsingar, sjá [Vinna með eiginleikauppsetningar](e-invoicing-feature-setup.md).
11. Ljúktu við uppsetninguna og settu rafræna reikningseiginleikann í þjónustuumhverfið. Fyrir frekari upplýsingar, sjá [Ljúktu við, birtu og settu upp hnattvæðingareiginleika](e-invoicing-complete-publish-deploy-globalization-feature).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Búðu til stillingar fyrir skráarsnið sem eru fengnar úr núverandi reikningslíkani

Þú getur sleppt þessum hluta ef þú þarft ekki að búa til ER stillingar en getur endurnýtt núverandi útgáfur sem grunn.

Þetta ferli sýnir hvernig á að búa til skráarsniðsstillingarnar sem eru nauðsynlegar fyrir nýja rafræna reikningseiginleikann sem þú vilt búa til. Búðu til skráarsnið rafrænna reikninga og allar aðrar skráarsniðstillingar sem nýi rafræni reikningseiginleikinn þinn krefst.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Veldu **Reikningslíkan** eða, fyrir brasilískar aðstæður, veldu **Ríkisfjármálalíkan**.
4. Veldu **Búðu til stillingar**, og veldu síðan í fellivalglugganum **Snið byggt á gagnalíkani Reikningur** valmöguleika.
5. Færðu inn heiti og lýsingu á sniðsskilgreiningunni.
6. Í reitnum **Sniðsgerð** skal velja gerð skrárendingar.
7. Í **Skilgreining gagnalíkans** reit, veldu rótarbygginguna til að varpa sniðinu þínu við. Til dæmis, **Invoice Viðskiptavinur** er notað fyrir reikningasnið viðskiptavinarins.
8. Veljið **Stofna skilgreiningu**.
9. Veldu nýja sniðstillingu.
10. Veldu **Hönnuður** og notaðu verkfæri sniðshönnuðar til að skilgreina skráarútlitið þannig að það uppfylli forskrift skráarsniðsins.
11. Lokið síðunni.
12. Í flipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka**.
13. Veldu **Breyta stöðu** \> **Deila** til að birta stillingar sniðs í altæka geymslu.

Nýju skráarsniðsstillingunum verður að deila með Microsoft léninu áður en rafræn reikningsþjónusta getur notað þær.

1. Veldu sniðsstillinguna sem þú ert að vinna í. Staða skilgreiningar verður að vera **Samnýtt**.
2. Í flipanum **Útgáfur** skal velja **Ítarleg samnýting** \> **Altæk geymsla**.
3. Í flipanum **Samnýtt með** skal velja **Fyrirtæki**.
4. Í **Færibreytur** reit, slá inn **microsoft.com** til að deila sniðstillingunum með Microsoft léninu.
5. Veldu **Í lagi**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Búðu til eiginleika sem er byggður á núverandi eiginleika

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Í **Stillingarveita** reit skaltu ganga úr skugga um að virka stillingaveitan þín sé valin. Þannig mun nýi eiginleiki rafrænna reikninga birtast á listanum eftir að hann er búinn til. Ef virka stillingaveitan þín er ekki valin verður nýi eiginleikinn síaður út af listanum.
4. Veljið **Bæta við** og síðan í fellilista svarglugga skal velja valkostinn **Byggt á fyrirliggjandi útgáfu**.
5. Færið inn heiti og lýsingu á eiginleikanum.
6. Í **Grunneiginleiki** reit, veldu grunnútgáfu eiginleikans.
7. Veljið **Stofna eiginleika**. Eiginleikinn er búinn til og hefur stöðuna **Drög**.
8. Yfirfara skal íhluti eiginleika til að ákvarða hvort uppfærslur eru nauðsynlegar:

    - Skoðaðu stillingarnar, ef þú verður að sérsníða ER sniðin og bindingu þeirra með sniðavörpum fyrir eiginleikaútgáfuna.
    - Skoðaðu uppsetninguna, ef þú verður að sérsníða **Aðgerðir** flipi, **Gildisreglur** flipa, eða **Breytur** flipa fyrir eiginleika útgáfuna.

9. Ljúktu við uppsetninguna og settu rafræna reikningseiginleikann í þjónustuumhverfið. Fyrir frekari upplýsingar, sjá [Ljúktu við, birtu og settu upp hnattvæðingareiginleika](e-invoicing-complete-publish-deploy-globalization-feature).
