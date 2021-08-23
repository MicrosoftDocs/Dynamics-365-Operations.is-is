---
title: Stofna nýjan eiginleika rafrænnar reikningsfærslu.
description: Þetta efnisatriði útskýrir hvernig á að búa til nýjan eiginleika rafrænnar reikningsfærslu þegar enginn stillanlegur tilbúinn eiginleiki er í boði fyrir landið þitt eða landsvæði.
author: gionoder
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ffef49c78fd0564db7a2329580ad33a9ccc633c8ac74557e625d1cfb29931576
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744936"
---
# <a name="create-a-new-electronic-invoicing-feature"></a>Stofna nýjan eiginleika rafrænnar reikningsfærslu.

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að búa til nýjan eiginleika rafrænnar reikningsfærslu þegar enginn stillanlegur tilbúinn eiginleiki er í boði fyrir landið þitt eða landsvæði.

Til að búa til nýjan eiginleika rafrænnar reikningsfærslu skal ljúka þessum verkum:

1. Búðu til nýja stillingu á skráarsniði með því að nota stillingar reikningsfærslulíkansins sem fylgir með og nýttu þér fyrirliggjandi reikningsvörpun fyrir eiginleikann sem á að búa til.
2. Bættu stillingum skráarsniðs við stillingar á eiginleika rafrænnar reikningsfærslu.
3. Stofnaðu eiginleikauppsetningu rafrænnar reikningsfærslu.
4. Ljúktu við nýjan eiginleika rafrænnar reikningsfærslu og birtu hann í altækri geymslu fyrir fyrirtækið þitt.
5. Nota eiginleika rafrænnar reikningsfærslu í þjónustuumhverfi

## <a name="create-new-file-format-configurations-that-are-derived-from-the-existing-invoice-model"></a>Búa til nýjar stillingar á skráarsniði sem eru koma frá fyrirliggjandi reikningslíkani

Í þessu ferli stofnarðu skilgreiningar skráarsniðs sem þarf fyrir nýjan eiginleika rafrænnar reikningsfærslu sem á að stofna. Hægt er að búa til stillingu skráarsniðs rafrænnar reikningsfærslu og allar aðrar stillingar skráarsniðs sem nýi eiginleiki rafrænnar reikningsfærslu gæti þurft á að halda.

Skráðu þig inn á Regulatory Configuration Service (RCS) reikninginn þinn áður en þú hefst handa.

1. Í Microsoft Dynamics 365 Finance, á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Gagnageymslur** fyrir skilgreiningarveitu **Microsoft**.
2. Veldu **Altækt**, veldu **Opinn** og því næst vinstra megin skaltu velja skilgreininguna **Reikningslíkan**.

    > [!IMPORTANT]
    > Fyrir Brasilíu skaltu velja líkanastillinguna **Fjárhagsskjöl** í staðinn.

3. Í flipanum **Skilgreiningar** skal velja **Flytja inn**.
4. Lokið síðunni.
5. Lokið síðunni.
6. Veldu reitinn **Skýrsluskilgreiningar** og síðan skaltu velja reikningslíkanið sem þú fluttir inn.
7. Veldu **Stofna skilgreiningu** og veldu svo **Snið byggt á samhengislíkan reiknings**.
8. Færðu inn heiti og lýsingu á sniðsskilgreiningunni.
9. Í reitnum **Sniðsgerð** skal velja gerð skrárendingar.
10. Veldu **Stofna skilgreiningu** og síðan skaltu velja sniðsskilgreininguna sem þú stofnaðir.
11. Veldu **Hönnuður** og notaðu verkfæri sniðshönnuðar til að skilgreina skráarútlitið þannig að það uppfylli forskrift skráarsniðsins.
12. Lokið síðunni.
13. Í flipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka**.
14. Veldu **Breyta stöðu** \> **Deila** til að birta stillingar sniðs í altæka geymslu.

Deila þarf nýrri stillingu skráarsniðs með léni Microsoft áður en rafræna reikningsfærsluþjónustan getur notað stillinguna.

1. Veldu sniðsstillinguna sem þú ert að vinna í. Staða skilgreiningar verður að vera **Samnýtt**.
2. Í flipanum **Útgáfur** skal velja **Ítarleg samnýting** \> **Altæk geymsla**.
3. Í flipanum **Samnýtt með** skal velja **Fyrirtæki**.
4. Í reitnum **færibreytur**, sláðu **inn** Microsoft.com til að deila sniðstillingunni með Microsoft léninu.
5. Veldu **Í lagi**.

## <a name="create-the-new-electronic-invoicing-feature"></a>Stofna nýjan eiginleika rafrænnar reikningsfærslu.

1. Í RCS, á vinnusvæðinu **Altækir eiginleikar**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
2. Veldu **Bæta við** og veldu því næst **Nýr eiginleiki**.
3. Færðu inn heiti og lýsingu á eiginleika rafrænnar reikningsfærslu.
4. Veljið **Stofna eiginleika**.

## <a name="add-electronic-invoicing-feature-configurations"></a>Bæta við skilgreiningum á eiginleika rafrænnar reikningsfærslu

1. Veldu eiginleika rafrænnar reikningsfærslu sem verið er að vinna í.
2. Í flipanum **Skilgreiningar** skal velja **Bæta við**.
3. Í hnitanetinu **Skilgreiningar** skal finna og velja skilgreiningar skráarsniðs sem eiginleiki rafrænnar reikningsfærslu þarf til að mynda skrá rafræns reiknings.
4. Veldu **Í lagi**.

## <a name="add-electronic-invoicing-feature-setups"></a>Bæta við uppsetningum á eiginleika rafrænnar reikningsfærslu

1. Í flipanum **Uppsetningar** skal velja **Bæta við** og síðan velja **Sérsniðin uppsetning**.
2. Færið inn heiti og lýsingu á uppsetningu eiginleikans.
3. Í reitnum **Gerð uppsetningar** skal velja **Unnið úr sölukeðju**.
4. Velja **Stofna**.
5. Veldu uppsetninguna sem þú ert að vinna með og svo **Breyta**.
6. Í flipanum **Unnið úr sölukeðju** skal velja **Ný** til að bæta við nýrri aðgerð sölukeðju. Frekari upplýsingar um sölukeðjur er að finna í [Aðgerðir](e-invoicing-configuration-rcs.md#actions).
7. Í flipanum **Gildissviðsreglur** skal velja **Nýtt** til að bæta við ákvæði gildissviðsreglu. Frekari upplýsingar um gildissviðsreglur er að finna í [Gildissviðsreglur](e-invoicing-configuration-rcs.md#applicability-rules).
8. Í flipanum **Breytur** skal velja **Ný** til að bætta breytum við eftir þörfum.
9. Veldu **Vista** og veldu því næst **Villuleita** til að athuga samræmi skilgreiningarinnar.
10. Lokið síðunni.

## <a name="deploy-the-electronic-invoicing-feature-to-the-service-environment"></a>Nota eiginleika rafrænnar reikningsfærslu í þjónustuumhverfi

Fyrir upplýsingar um hvernig á að ljúka þessu verki, sjá [Nota eiginleika rafrænnar reikningsfærslu í þjónustuumhverfi](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="deploy-the-electronic-invoicing-feature-to-a-connected-application"></a>Nota eiginleika rafrænnar reikningsfærslu í tengt forrit

Fyrir upplýsingar um hvernig á að ljúka þessu verki er að finna í [Skilgreina uppsetningu forrits](e-invoicing-get-started.md#configure-the-application-setup) og [Nota eiginleika rafrænnar reikningsfærslu í tengt forrit](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application).
