---
title: Stofna altækan eiginleika
description: Þessi grein útskýrir hvernig á að stofna altækan eiginleika.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5432de8f8a70a4e6a0facd546083b37fd8690556
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283176"
---
# <a name="create-a-globalization-feature"></a>Stofna altækan eiginleika

[!include [banner](../includes/banner.md)]

Hægt er að búa til eiginleika rafrænnar reikningsfærslu frá grunni eða byggja hann á fyrirliggjandi eiginleika. Þegar eiginleiki er búinn til frá grunni þarf að bæta við skilgreiningum rafrænnar skýrslugerðar handvirkt og öðrum þáttum eins og upplýsingar um uppsetningu eiginleika og forrits. Þegar eiginleiki sem byggir á fyrirliggjandi eiginleika er búinn til mun nýi eiginleikinn erfa allar grunnskilgreiningar og færibreytur eiginleikans. Þú getur farið yfir það sem er afritað úr grunneiginleikanum yfir í nýja eiginleikann.

## <a name="create-a-feature-from-scratch"></a>Búa til eiginleika frá grunni

Í þessum hluta er útskýrt hvernig á að búa til eiginleika rafrænnar reikningsfærslu þegar enginn altækur eiginleiki er í boði í altæku geymslunni fyrir tilbúnar viðskiptaaðstæður.

Til að búa til eiginleika rafrænnar reikningsfærslu skal fylgja þessum skrefum.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Veldu **Bæta við** og síðan í fellilistanum skal velja valkostinn **Nýr eiginleiki**.
4. Færðu inn heiti og lýsingu á eiginleika rafrænnar reikningsfærslu.
5. Veljið **Stofna eiginleika**. Fyrsta útgáfan af nýja eiginleikanum birtist hægra megin á síðunni og er með stöðuna **Uppkast**.

    Næst þarf að bæta við skilgreiningum rafrænnar skýrslugerðar og uppsetningum eiginleikans. Áður en nýjum eða fyrirliggjandi skilgreiningum rafræns skýrslugerðarsniðs er bætt við skal ganga úr skugga um að þau séu til í staðbundinni RCS-gagnageymslu.

6. Veldu eiginleika rafrænnar reikningsfærslu sem verið er að vinna í.
7. Í flipanum **Skilgreiningar** skal velja **Bæta við**.
8. Í hnitanetinu **Skilgreiningar** skal fara í og velja skilgreiningar sniðsins sem þarf til að vinna úr keðju (t.d. til að búa til skrár rafrænna reikninga eða vinna úr svörum frá ytri vefþjónustum).
9. Veldu **Í lagi**. Nú er hægt að nota skilgreiningarnar í vinnsluaðgerðum keðju. Frekari upplýsingar er að finna í [Vinna með skilgreiningar](e-invoicing-work-configurations.md).
10. Til að bæta við uppsetningu á eiginleika rafrænnar reikningsfærslu skal búa hana til í flipanum **Uppsetningar** á síðunni **Nýr eiginleiki**. Frekari upplýsingar er að finna í [Vinna með uppsetningu eiginleika](e-invoicing-feature-setup.md).
11. Ljúktu við uppsetninguna og settu upp eiginleika rafrænnar reikningsfærslu í umhverfi þjónustunnar. Frekari upplýsingar er að finna í [Ljúka við, birta og setja upp altækan eiginleika](e-invoicing-complete-publish-deploy-globalization-feature.md).

### <a name="create-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Búa til skilgreiningar skráarsniðs sem koma frá fyrirliggjandi reikningslíkani

Þú getur sleppt þessum hluta ef þú þarft ekki að búa til ER stillingar en getur endurnotað núverandi útgáfur sem grunn.

Þetta ferli sýnir hvernig á að búa til skilgreiningar skráarsniðs sem þarf fyrir nýjan eiginleika rafrænnar reikningsfærslu sem á að stofna. Búðu til skilgreiningu skráarsniðs fyrir rafræna reikningsfærslu og allar aðrar skilgreiningar skráarsniðs sem nýi eiginleiki rafrænnar reikningsfærslu þarf á að halda.

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Veldu **Reikningslíkan** eða fyrir brasilískar aðstæður skal velja **Fjárhagslíkan**.
4. Veldu **Stofna skilgreiningu** og síðan í fellilistanum skal velja valkostinn **Snið byggir á reikningi gagnalíkans**.
5. Færðu inn heiti og lýsingu á sniðsskilgreiningunni.
6. Í reitnum **Sniðsgerð** skal velja gerð skrárendingar.
7. Í reitnum **Skilgreining gagnalíkans** skal velja rótarskipulagið til að varpa sniðinu í. Til dæmis er **InvoiceCustomer** notað fyrir snið viðskiptavinareikninga.
8. Veljið **Stofna skilgreiningu**.
9. Veldu stillingar fyrir nýja sniðið.
10. Veldu **Hönnuður** og notaðu verkfæri sniðshönnuðar til að skilgreina skráarútlitið þannig að það uppfylli forskrift skráarsniðsins.
11. Lokið síðunni.
12. Í flipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka**.
13. Veldu **Breyta stöðu** \> **Deila** til að birta stillingar sniðs í altæka geymslu.

Deila þarf nýrri stillingu skráarsniðs með léni Microsoft áður en rafræna reikningsfærsluþjónustan getur notað stillinguna.

1. Veldu sniðsstillinguna sem þú ert að vinna í. Staða skilgreiningar verður að vera **Samnýtt**.
2. Í flipanum **Útgáfur** skal velja **Ítarleg samnýting** \> **Altæk geymsla**.
3. Í flipanum **Samnýtt með** skal velja **Fyrirtæki**.
4. Í reitnum **Færibreytur** skal færa inn **microsoft.com** til að deila skilgreiningu sniðs með Microsoft-léninu.
5. Veldu **Í lagi**.

## <a name="create-a-feature-that-is-based-on-an-existing-feature"></a>Búa til eiginleika sem byggir á fyrirliggjandi eiginleika

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Í reitnum **Skilgreiningarveita** skal ganga úr skugga um að virk skilgreiningarveita sé valin. Á þennan hátt mun nýr eiginleiki rafrænnar reikningsfærslu birtast í listanum eftir að hann er búinn til. Ef virk skilgreiningarveita er ekki valin mun nýi eiginleikinn vera síaður út af listanum.
4. Veljið **Bæta við** og síðan í fellilista svarglugga skal velja valkostinn **Byggt á fyrirliggjandi útgáfu**.
5. Færið inn heiti og lýsingu á eiginleikanum.
6. Í reitnum **Grunneiginleiki** skal velja grunnútgáfu eiginleikans.
7. Veljið **Stofna eiginleika**. Eiginleikinn er búinn til og er með stöðuna **Uppkast**.
8. Yfirfara skal íhluti eiginleika til að ákvarða hvort uppfærslur eru nauðsynlegar:

    - Farðu skal yfir skilgreiningarnar ef skyldi reynast nauðsynlegt að sérstilla snið rafrænnar skýrslugerðar og bindingu þeirra við sniðsvarpanir fyrir eiginleikaútgáfuna.
    - Farðu yfir uppsetninguna ef skyldi reynast nauðsynlegt að sérstilla flipann **Aðgerðir**, flipann **Gildissviðsreglur** eða flipann **Breytur** fyrir eiginleikaútgáfuna.

9. Ljúktu við uppsetninguna og settu upp eiginleika rafrænnar reikningsfærslu í umhverfi þjónustunnar. Frekari upplýsingar er að finna í [Ljúka við, birta og setja upp altækan eiginleika](e-invoicing-complete-publish-deploy-globalization-feature.md).
