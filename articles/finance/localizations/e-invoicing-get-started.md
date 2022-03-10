---
title: Hafist handa með rafrænar reikningsfærslur
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
ms.date: 11/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ebef9cf97f7a91e0a2fd45f5e0e0fc620070b42a
ms.sourcegitcommit: 5033d42a2aac852916d726e40bd98a164d1a837d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/23/2022
ms.locfileid: "7983872"
---
# <a name="get-started-with-electronic-invoicing"></a>Hafist handa með rafrænar reikningsfærslur

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með rafræna reikningsfærslu. Þetta efnisatriði leiðir þig í gegnum almennt grunnstillingarskref í Regulatory Configuration Services (RCS) og Dynamics 365 Finance, og inniheldur þau skref sem þú þarft að fylgja til að senda inn viðskiptaskjöl og fara yfir niðurstöðurnar.

## <a name="prerequisites"></a>Forkröfur

Áður en ferlið í þessu efnisatriði er klárað þurfa eftirfarandi skilyrði að vera til staðar:

- Grunnstilltu Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), og Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management umhverfið þitt. Frekari upplýsingar eru í [Hafist handa með stjórnun þjónustu rafrænna reikninga](e-invoicing-get-started-service-administration.md).
- Stofna skilgreiningarveitu fyrir fyrirtækið. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitu og merkja hana sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Flytja inn eiginleika rafrænnar reikningsfærslu úr skilgreiningarveitu Microsoft 

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækir eiginleikar**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Smellið á **Flytja inn** og veljið síðan **Samstilla**.
4. Afmarkið dálkinn **Skilgreiningarveita** með **Microsoft**.
5. Veljið heiti rafræns reikningsfærslueiginleika úr töflunni og veljið síðan **Flytja inn**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Stofna eiginleika rafrænnar reikningsfærslu undir þjónustuveitu fyrirtækisins

1. Í RCS, í hlutanum **Eiginleikar** á vinnusvæðinu **Altækir eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
2. Veljið **Bæta við** > **Byggt á fyrirliggjandi eiginleika** og í reitinn **Heiti** skal slá inn heiti á eiginleika rafrænnar reikningsfærslu.
3. Í reitinn **Lýsing** skal slá inn lýsingu eiginleikans.
4. Í **Reitur grunneiginleika** skal velja innfluttan eiginleika rafrænnar reikningsfærslu úr skilgreiningarveitu Microsoft.
5. Veljið **Stofna eiginleika**.

## <a name="country-specific-configuration-for-electronic-invoicing-feature"></a>Landsbundin skilgreining fyrir eiginleika rafrænnar reikningsfærslu

Það fer eftir landi eða svæði hvort eiginleiki rafrænnar reikningsfærslu þurfi tiltekna skilgreiningu. 

> [!NOTE]
> Þegar þú virkjar eiginleikann Rafræn reikningagerð fyrir Finnland eru forritssértækar færibreytur í uppflettingum ekki studdar. Til að vinna í kringum þetta mál, í **Rafræn skýrslugerð** mát, skoðaðu stillingar fyrir sölureikninga og verkreikningasnið. Settu upp reiknaða reitinn handvirkt fyrir **$PaymentMethodSubstitution** kortlagning, og binda síðan þann reit við **EpiPaymentMeansCode** reit úr sniðum sölureiknings og verkreiknings.
>
> Þegar þú virkjar rafræna reikningseiginleikann fyrir Ítalíu eru forritssértækar færibreytur í uppflettingum ekki studdar. Til að vinna í kringum þetta mál, í **Rafræn skýrslugerð** mát, settu handvirkt upp reiknaða reitinn fyrir **$NaturaReverseCharge** kortlagningu.
>
> Fyrir tiltekin skref sem tengjast öðrum staðsetningum, sjá „Byrjaðu“ skjölin sem eru tiltæk fyrir þitt land eða svæði.

## <a name="import-the-model-mapping-configurations-from-electronic-reporting"></a>Flytja inn grunnstillingar líkanavarpana úr rafrænni skýrslugerð

1. Í RCS skal velja **Rafræn skýrslugerð** vinnusvæðið.
2. Af lista **Microsoft** skilgreiningaraðilum skal velja **Geymslur**.
3. Veljið **Altækt** og á aðgerðasvæði **Opna**.
4. Flytjið inn grunnstillingar fyrir líkanavörpum í samræmi við eftirfarandi töflu eftir heiti eiginleika.

| Heiti eiginleika                         | Skilgreining líkanavörpunar |
|--------------------------------------|-----------------------------|
| Rafrænir reikningar í Austurríki (AT)    | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Belgískur rafrænn reikningur (BE)      | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Brasilískt NF-e (BR)                  | <p>Samhengislíkan viðskiptavinareiknings</p><p>Fjárhagsskjöl</p><p>Skilaboðalíkan svars</p> |
| Brasilískt NFS-e ABRASF Curitiba (BR) | <p>Samhengislíkan viðskiptavinareiknings</p><p>Fjárhagsskjöl</p><p>Skilaboðalíkan svars</p> |
| Danskur rafrænn reikningur (DK)       | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Egypskur rafrænn reikningur (EG)     | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p><p>Skilaboðalíkan svars</p> |
| Eistneskur rafrænn reikningur (EE)     | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Finnskur rafrænn reikningur (FI)       | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Franskur rafrænn reikningur (FR)       | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Þýskur rafrænn reikningur (DE)       | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| FatturaPA (IT)                       | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Mexíkóskur CFDI Interfactura (MX)       | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p><p>Skilaboðalíkan svars</p> |
| Hollenskur rafrænn reikningur (NL)        | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Norskur rafrænn reikningur (NO)    | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Spænskur rafrænn reikningur (ES)      | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| PEPPOL rafrænn reikningur            | <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |
| Rafrænn reikningur Sádi-Arabíu (SA)| <p>Samhengislíkan viðskiptavinareiknings</p><p>Reikningslíkan</p> |


## <a name="configure-the-application-setup"></a>Skilgreina uppsetningu forrits

1. Veljið eiginleika rafrænnar reikningsfærslu sem var stofnaður.
2. Í flipanum **Uppsetningar** skal velja **Uppsetning forrits**.
3. Í reitinum **Tengja forrit** skal velja tenginguna sem tengist tilviki þínu af Finance eða Supply Chain Management.
4. Í hlutanum **Gerðir rafrænna skjala** skal velja **Bæta við**.
5. Veljið og færið inn gildi fyrir **Töfluheiti** samkvæmt eftirfarandi töflu.

    | Heiti eiginleika                         | Viðskiptaskjal | Töfluheiti |
    |--------------------------------------|-------------------|------------|
    | Rafrænir reikningar í Austurríki (AT)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Belgískur rafrænn reikningur (BE)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Brasilískt NF-e (BR)                  | <p>Fjárhagsskjal</p><p>Leiðréttingarbréf</p> | Fjárhagsskjal |
    | Brasilískt NFS-e ABRASF Curitiba (BR) | Fjárhagsskjal þjónustu | Fjárhagsskjal |
    | Danskur rafrænn reikningur (DK)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Egypskur rafrænn reikningur (EG)     | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Eistneskur rafrænn reikningur (EE)     | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Finnskur rafrænn reikningur (FI)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Franskur rafrænn reikningur (FR)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Þýskur rafrænn reikningur (DE)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | FatturaPA (IT)                       | <p>Sölureikningur</p><p>Verkreikningur | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Mexíkóskur CFDI Interfactura (MX)       | <p>Sölureikningur</p><p>Fylgiseðill</p><p>Birgðaflutningur</p><p>Fullnusta greiðslu</p> | Reikningabók viðskiptavinar |
    | Hollenskur rafrænn reikningur (NL)        | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Norskur rafrænn reikningur (NO)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Spænskur rafrænn reikningur (ES)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | PEPPOL rafrænn reikningur            | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Rafrænn reikningur Sádi-Arabíu (SA)| <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |

6. Fyrir hvert töfluheiti sem er búið til skal velja og færa inn gildi fyrir samhengi samkvæmt eftirfarandi töflu.

    | Heiti eiginleika                         | Viðskiptaskjal | Samhengi |
    |--------------------------------------|-------------------|---------|
    | Rafrænir reikningar í Austurríki (AT)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Belgískur rafrænn reikningur (BE)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Brasilískt NF-e (BR)                  | <p>Fjárhagsskjal</p><p>Leiðréttingarbréf</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi fjárhagsskjals</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi leiðréttingarbréfs fjárhagsskjals</p> |
    | Brasilískt NFS-e ABRASF Curitiba (BR) | Fjárhagsskjal þjónustu| Samhengislíkan viðskiptavinareiknings – Samhengi fjárhagsskjals |
    | Danskur rafrænn reikningur (DK)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Egypskur rafrænn reikningur (EG)     | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Eistneskur rafrænn reikningur (EE)     | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Finnskur rafrænn reikningur (FI)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Franskur rafrænn reikningur (FR)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Þýskur rafrænn reikningur (DE)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | FatturaPA (IT)                       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Mexíkóskur CFDI Interfactura (MX)       | <p>Sölureikningur</p><p>Fylgiseðill</p><p>Birgðaflutningur</p><p>Fullnusta greiðslu</p> | Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings |
    | Hollenskur rafrænn reikningur (NL)        | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Norskur rafrænn reikningur (NO)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Spænskur rafrænn reikningur (ES)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | PEPPOL rafrænn reikningur            | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Rafrænn reikningur Sádi-Arabíu (SA)| <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |

7. Fyrir hvert töfluheiti og samhengi skal velja og færa inn gildi fyrir vörpun á viðskiptaskjali samkvæmt eftirfarandi töflu.

    | Heiti eiginleika                         | Viðskiptaskjal | Vörpun viðskiptaskjals |
    |--------------------------------------|-------------------|---------------------------|
    | Rafrænir reikningar í Austurríki (AT)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Belgískur rafrænn reikningur (BE)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Brasilískt NF-e (BR)                  | <p>Fjárhagsskjal</p><p>Leiðréttingarbréf</p> | <p>Vörpun fjárhagsskjals – Vörpun fjárhagsskjals</p><p>Vörpun fjárhagsskjals – vörpun leiðréttingarbréfs</p> |
    | Brasilískt NFS-e ABRASF Curitiba (BR) | Fjárhagsskjal þjónustu | Vörpun fjárhagsskjals – Vörpun fjárhagsskjals |
    | Danskur rafrænn reikningur (DK)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Egypskur rafrænn reikningur (EG)     | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Eistneskur rafrænn reikningur (EE)     | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Finnskur rafrænn reikningur (FI)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Franskur rafrænn reikningur (FR)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Þýskur rafrænn reikningur (DE)       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | FatturaPA (IT)                       | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Mexíkóskur CFDI Interfactura (MX)       | <p>Sölureikningur</p><p>Fylgiseðill</p><p>Birgðaflutningur</p><p>Fullnusta greiðslu</p> | Vörpun reikningslíkans – Reikningur viðskiptavinar |
    | Hollenskur rafrænn reikningur (NL)        | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Norskur rafrænn reikningur (NO)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Spænskur rafrænn reikningur (ES)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | PEPPOL rafrænn reikningur            | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Rafrænn reikningur Sádi-Arabíu (SA)| <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |


## <a name="country-specific-configuration-of-application-setup"></a>Landsháð grunnstilling á uppsetningu forrits

Það fer eftir landi eða svæði hvort uppsetning forrits þurfi tiltekna skilgreiningu. 

Fyrir nákvæmar leiðbeiningar skal skoða fylgiskjalið „Hafist handa“ sem er í boði fyrir tilheyrandi land eða svæði.

## <a name="deploy-the-electronic-invoicing-feature-to-service-environment"></a>Nota eiginleika rafrænnar reikningsfærslu í þjónustuumhverfi

1. Í flipanum **Útgáfur** skal velja útgáfu rafræns reikningsfærslueiginleika sem á að nota.
2. Veljið **Breyta stöðu** \> **Ljúka**.
3. Veljið **Breyta stöðu** \> **Birta**.
4. Veljið **Nota**.
5. Stillið valkostinn **Nota fyrir tengt forrit** á **Nei**.
6. Stillið valkostinn **Nota fyrir þjónustuumhverfi** á **Já**.
7. Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi fyrir rafræna reikningsfærslu þar sem á að nota eiginleika rafrænnar reikningsfærslu.
8. Í reitnum **Frá dagsetningu** skal velja dagsetninguna þegar eiginleiki rafrænnar reikningsfærslu verður að taka gildi í rafrænni reikningsfærslu.
9. Veljið **Í lagi**.

## <a name="deploy-the-electronic-invoicing-feature-to-connected-application"></a>Nota eiginleika rafrænnar reikningsfærslu í tengt forrit

1. Í flipanum **Útgáfur** skal velja útgáfu rafræns reikningsfærslueiginleika sem á að nota.
2. Veljið **Nota**.
3. Stillið valkostinn **Nota fyrir tengt forrit** á **Já**.
4. Í reitinum **Tengja forrit** skal velja tenginguna sem tengist tilviki þínu af Finance eða Supply Chain Management.
5. Stillið valkostinn **Nota fyrir þjónustuumhverfi** á **Nei**.
6. Veljið **Í lagi**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Kveikja á eiginleika rafrænnar reikningsfærslu í Finance eða Supply Chain Management

1. Skráðu þig inn í Finance eða Supply Chain Management og gakktu úr skugga um að þú sért í réttum lögaðila.
2. Farið í **Fyrirtækisstjórnun** \> **Uppsetning** \> **Færibreytur rafræns skjals**.
3. Í flipanum **Eiginleikar** skal velja eiginleika sem eru háðir landi/svæði til að kveikja á eiginleika rafrænnar reikningsfærslu fyrir Finance eða Supply Chain Management. Eftirfarandi tafla inniheldur lista yfir rafræna reikningsfærslueiginleika sem eru í boði fyrir tiltekin lönd/landsvæði. 

    | Heiti eiginleika                                          | Land/svæði  |
    |-------------------------------------------------------|-----------------|
    | Rafrænir reikningar í Austurríki (AT)                     | Austurríki         |
    | Belgískur rafrænn reikningur (BE)                       | Belgía         |
    | CFDI - Mexíkóskur rafrænn reikningur (MX)                  | Mexíkó          |
    | Danskur rafrænn reikningur (DK)                        | Danmörk         |
    | Hollenskur rafrænn reikningur (NL)                         | Hollandi |
    | Egypskur rafrænn reikningur (EG)                      | Egyptaland           |
    | Eistneskur rafrænn reikningur (EE)                      | Eistland         |
    | Finnskur rafrænn reikningur (FI)                       | Finnland         |
    | Franskur rafrænn reikningur (FR)                        | Frakkland          |
    | Þýskur rafrænn reikningur (DE)                        | Þýskaland         |
    | Ítalskur rafrænn reikningur (IT)                       | Ítalía           |
    | NF-e Ríki - rafrænn reikningur fyrir Brasilíu (BR)      | Brasilía          |
    | NFS-e - Brasilísk Þjónusta (borg) rafrænn reikningur   | Brasilía          |
    | Norskur rafrænn reikningur (NO)                     | Noregur          |
    | PEPPOL rafrænn reikningur                             | Altæk          |
    | Spænskur rafrænn reikningur (ES)                       | Spánn           |
    | Rafrænn reikningur Sádi-Arabíu (SA)                 | Sádi-Arabía    |
    

4. Veldu **Vista**.

## <a name="issue-electronic-invoices"></a>Gefa út rafræna reikninga

1. Farið í **Fyrirtækisstjórnun** \> **Reglubundið** \> **Rafræn skjöl** \> **Senda inn rafræn skjöl**.
2. Á flýtiflipanum **Færslur til að hafa með** velurðu **Sía**.
3. Veljið **Bæta við** til að bæta töfluheiti við fyrirspurnarsíuna.
4. Veljið töfluna sem inniheldur reikningana.

    > [!NOTE]
    > Töfluheitið verður að vera skráð í töflunni í hlutanum [Skilgreina uppsetningu forrits](#configure-the-application-setup) fyrr í þessu efnisatriði.

5. Veljið heiti reits úr töflunni sem á að spyrjast fyrir um.
6. Færið inn töfluheiti og reitarheiti fyrir skilyrðið sem á að spyrjast fyrir um.
7. Endurtakið skref 5 og 6 til að bæta fleiri reitum og skilyrðum við fyrirspurnina og veljið síðan **Í lagi**.
8. Veljið **Í lagi**.

## <a name="view-submission-logs"></a>Skoða innsendingarkladda

1. Farið í **Fyrirtækisstjórnun** \> **Reglubundið** \> **Rafræn skjöl** \> **Innsendingarkladdi rafræns skjals**.
2. Í reitnum **Gerð skjals** skal velja töfluna sem inniheldur reikningana.

    > [!NOTE]
    > Töfluheitið verður að vera skráð í töflunni í hlutanum [Skilgreina uppsetningu forrits](#configure-the-application-setup) fyrr í þessu efnisatriði.

3. Veljið reikning í hnitanetinu og veljið síðan **Spyrjast fyrir** \> **Upplýsingar um sendingu**.

## <a name="download-an-electronic-document-file"></a>Sækja rafræn skjal

1. Farið í **Fyrirtækisstjórnun** \> **Reglubundið** \> **Rafræn skjöl** \> **Innsendingarkladdi rafræns skjals**.
2. Í reitnum **Gerð skjals** skal velja töfluna sem inniheldur reikningana.
3. Veldu skjal í hnitanetinu og veldu síðan **Rafræn skjal** \> **Hlaða niður skrá**. Stungið verður upp á skjalasafni sem inniheldur rafrænu skjalaskrána til niðurhals.

> [!NOTE]
> Áður en þú getur hlaðið niður skrám, **Útflutningsniðurstaða** kveikt verður á valmöguleikanum fyrir tengda aðgerð í eiginleikauppsetningu rafrænna reikninga í RCS.

## <a name="related-topics"></a>Tengd efnisatriði

- [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með þjónustu rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með rafrænr reikningsfærslur fyrir Brasilíu](e-invoicing-bra-get-started.md)
- [Hafist handa með rafrænar reikningsfærslur fyrir Mexíkó](e-invoicing-mex-get-started.md)
- [Hafist handa með rafrænar reikningsfærslur fyrir Ítalíu](e-invoicing-ita-get-started.md)
- [Rafrænir reikningar viðskiptavinar í Egyptalandi](emea-egy-e-invoices.md)
- [Rafrænir reikningar viðskiptavinar í Sádi-Arabíu](emea-sau-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
