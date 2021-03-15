---
title: Hafist handa með innbót rafrænna reikninga
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 07954c5c96f390bc651794f8b6c61f2a1a17ab8b
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5111221"
---
# <a name="get-started-with-the-electronic-invoicing-add-on"></a>Hafist handa með innbót rafrænna reikninga

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu.

Í eftirfarandi töflu er listi yfir eiginleika rafrænnar reikningsfærslu og viðskiptaskjölin sem hægt er að nota þá í.

| Heiti eiginleika                         | Viðskiptaskjal |
|--------------------------------------|-------------------|
| Rafrænir reikningar í Austurríki (AT)    | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Belgískur rafrænn reikningur (BE)      | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Brasilískt NF-e (BR)                  | <p>Fjármálaskjal, líkan 55</p><p>Leiðréttingarbréf</p> |
| Brasilískt NFS-e ABRASF Curitiba (BR) | Fjárhagsskjal þjónustu |
| Brasilískt NFS-e São Paulo (BR)       | Fjárhagsskjal þjónustu |
| Danskur rafrænn reikningur (DK)       | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Egypskur rafrænn reikningur (EG)     | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Eistneskur rafrænn reikningur (EE)     | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Finnskur rafrænn reikningur (FI)       | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Franskur rafrænn reikningur (FR)       | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Þýskur rafrænn reikningur (DE)       | <p>Sölureikningur</p><p>Verkreikningur</p> |
| FatturaPA (IT)                       | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Mexíkóskur CFDI Interfactura (MX)       | <p>Sölureikningur</p><p>Fylgiseðill</p><p>Birgðaflutningur</p><p>Fullnusta greiðslu</p> |
| Hollenskur rafrænn reikningur (NL)        | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Norskur rafrænn reikningur (NO)    | <p>Sölureikningur</p><p>Verkreikningur</p> |
| Spænskur rafrænn reikningur (ES)      | <p>Sölureikningur</p><p>Verkreikningur</p> |
| PEPPOL rafrænn reikningur            | <p>Sölureikningur</p><p>Verkreikningur</p> |

## <a name="prerequisites"></a>Forkröfur

Áður en ferlið í þessu efnisatriði er klárað þurfa eftirfarandi skilyrði að vera til staðar:

- Skilgreinið Regulatory Configuration Service (RCS) og Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management umhverfi þannig að hægt sé að senda inn viðbót rafrænnar reikningsfærslu.
- Búið til þjónustuumhverfi og birtið það í viðbót rafrænnar reikningsfærslu. Frekari upplýsingar er að finna í [Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu](e-invoicing-get-started-service-administration.md).
- Búa til tengt forrit. Frekari upplýsingar er að finna í [Hafist handa með þjónustuveitu viðbótar rafrænnar reikningsfærslu](e-invoicing-get-started-service-administration.md).
- Stofna skilgreiningarveitu fyrir fyrirtækið. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitu og merkja hana sem virka](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider"></a>Flytja inn eiginleika rafrænnar reikningsfærslu úr skilgreiningarveitu Microsoft 

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, undir hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Smellið á **Flytja inn** og veljið síðan **Samstilla**.
4. Afmarkið dálkinn **Skilgreiningarveita** með **Microsoft**.
5. Veljið heiti rafræns reikningsfærslueiginleika úr töflunni í upphafi þessa efnisatriðis og veljið síðan **Flytja inn**.

## <a name="create-an-electronic-invoicing-feature-under-your-organization-provider"></a>Stofna eiginleika rafrænnar reikningsfærslu undir þjónustuveitu fyrirtækisins

1. Í hlutanum **Eiginleikar** á vinnusvæðinu **Altækur eiginleiki** skal velja reitinn **Rafræn reikningsfærsla**.
2. Veljið **Bæta við** > **Byggt á fyrirliggjandi eiginleika** og í reitinn **Heiti** skal slá inn heiti á eiginleika rafrænnar reikningsfærslu.
3. Í reitinn **Lýsing** skal slá inn lýsingu eiginleikans.
4. Í **Reitur grunneiginleika** skal velja innfluttan eiginleika rafrænnar reikningsfærslu úr skilgreiningarveitu Microsoft.
5. Veljið **Stofna eiginleika**.

## <a name="configure-the-electronic-invoicing-feature"></a>Skilgreina eiginleika rafrænnar reikningsfærslu

Það fer eftir landi eða svæði hvort eiginleiki rafrænnar reikningsfærslu þurfi frekari skilgreiningu. Fyrir nákvæmar leiðbeiningar skal skoða fylgiskjalið „Hafist handa“ sem er í boði fyrir tilheyrandi land eða svæði.

## <a name="configure-the-application-setup"></a>Skilgreina uppsetningu forrits

1. Veljið eiginleika rafrænnar reikningsfærslu sem var stofnaður.
2. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
3. Í flipanum **Uppsetningar** skal velja **Uppsetning forrits**.

    > [!NOTE]
    > Gangið úr skugga um að fyrirtækið sé stillt sem **Virka** skilgreiningarveitan. Nánari upplýsingar er að finna í [Stofna skilgreiningarveitu og merkja hana sem virka.](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)

4. Veljið **Uppsetning eiginleika** og veljið síðan **Tengt forrit**.
5. Í hlutanum **Gerðir rafrænna skjala** skal velja **Bæta við**.
6. Fyrir hvert viðskiptaskjal sem eiginleikinn styður skal velja og færa inn gildi fyrir **Töfluheiti** samkvæmt eftirfarandi töflu.

    | Heiti eiginleika                         | Viðskiptaskjal | Töfluheiti |
    |--------------------------------------|-------------------|------------|
    | Rafrænir reikningar í Austurríki (AT)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Belgískur rafrænn reikningur (BE)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Reikningabók viðskiptavinar</p><p>Verkreikningur</p> |
    | Brasilískt NF-e (BR)                  | <p>Fjárhagsskjal</p><p>Leiðréttingarbréf</p> | Fjárhagsskjal |
    | Brasilískt NFS-e ABRASF Curitiba (BR) | Fjárhagsskjal þjónustu | Fjárhagsskjal |
    | Brasilískt NFS-e São Paulo (BR)       | Fjárhagsskjal þjónustu | Fjárhagsskjal |
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

7. Fyrir hvert viðskiptaskjal sem eiginleikinn styður skal velja og færa inn gildi fyrir **Samhengi** samkvæmt eftirfarandi töflu.

    | Heiti eiginleika                         | Viðskiptaskjal | Samhengi |
    |--------------------------------------|-------------------|---------|
    | Rafrænir reikningar í Austurríki (AT)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Belgískur rafrænn reikningur (BE)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi viðskiptavinareiknings</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi verkreiknings</p> |
    | Brasilískt NF-e (BR)                  | <p>Fjárhagsskjal</p><p>Leiðréttingarbréf</p> | <p>Samhengislíkan viðskiptavinareiknings – Samhengi fjárhagsskjals</p><p>Samhengislíkan viðskiptavinareiknings – Samhengi leiðréttingarbréfs fjárhagsskjals</p> |
    | Brasilískt NFS-e ABRASF Curitiba (BR) | Fjárhagsskjal þjónustu| Samhengislíkan viðskiptavinareiknings – Samhengi fjárhagsskjals |
    | Brasilískt NFS-e São Paulo (BR)       | Fjárhagsskjal þjónustu| Samhengislíkan viðskiptavinareiknings – Samhengi fjárhagsskjals |
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

8. Fyrir hvert viðskiptaskjal sem eiginleikinn styður skal velja og færa inn gildi fyrir **Vörpun á viðskiptaskjali** samkvæmt eftirfarandi töflu.

    | Heiti eiginleika                         | Viðskiptaskjal | Vörpun viðskiptaskjals |
    |--------------------------------------|-------------------|---------------------------|
    | Rafrænir reikningar í Austurríki (AT)    | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Belgískur rafrænn reikningur (BE)      | <p>Sölureikningur</p><p>Verkreikningur</p> | <p>Vörpun reikningslíkans – Reikningur viðskiptavinar</p><p>Vörpun reikningslíkans – Verkreikningur</p> |
    | Brasilískt NF-e (BR)                  | <p>Fjárhagsskjal</p><p>Leiðréttingarbréf</p> | <p>Vörpun fjárhagsskjals – Vörpun fjárhagsskjals</p><p>Vörpun fjárhagsskjals – vörpun leiðréttingarbréfs</p> |
    | Brasilískt NFS-e ABRASF Curitiba (BR) | Fjárhagsskjal þjónustu | Vörpun fjárhagsskjals – Vörpun fjárhagsskjals |
    | Brasilískt NFS-e São Paulo (BR)       | Fjárhagsskjal þjónustu | Vörpun fjárhagsskjals – Vörpun fjárhagsskjals |
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

Það fer eftir landi eða svæði hvort eiginleiki rafrænnar reikningsfærslu þurfi frekari skilgreiningu. Fyrir nákvæmar leiðbeiningar skal skoða fylgiskjalið „Hafist handa“ sem er í boði fyrir tilheyrandi land eða svæði.

## <a name="deploy-the-electronic-invoicing-feature"></a>Nota eiginleika rafrænnar reikningsfærslu

1. Í flipanum **Útgáfur** skal velja útgáfu rafræns reikningsfærslueiginleika sem á að nota.
2. Veljið **Breyta stöðu** \> **Ljúka**.
3. Veljið **Breyta stöðu** \> **Birta**.
4. Veljið **Nota**.
5. Stillið valkostinn **Nota fyrir tengt forrit** á **Já**.
6. Á síðunni **Tengja forrit** skal velja tenginguna sem tengist tilviki þínu af Finance eða Supply Chain Management.
7. Stillið valkostinn **Nota fyrir þjónustuumhverfi** á **Já**.
8. Í reitnum **Þjónustuumhverfi** skal velja þjónustuumhverfi fyrir viðbót rafrænnar reikningsfærslu þar sem á að nota eiginleika rafrænnar reikningsfærslu.
9. Í reitnum **Frá dagsetningu** skal velja dagsetninguna þegar eiginleiki rafrænnar reikningsfærslu verður að taka gildi í viðbót rafrænnar reikningsfærslu.
10. Veljið **Í lagi**.

## <a name="turn-on-the-electronic-invoicing-feature-in-finance-or-supply-chain-management"></a>Kveikja á eiginleika rafrænnar reikningsfærslu í Finance eða Supply Chain Management

1. Skráðu þig inn í Finance eða Supply Chain Management og gakktu úr skugga um að þú sért í réttum lögaðila.
2. Farið í **Fyrirtækisstjórnun** \> **Uppsetning** \> **Færibreytur rafræns skjals**.
3. Í flipanum **Eiginleikar** skal velja tilvísanir eiginleika sem eru sýndir í eftirfarandi töflu til að kveikja á eiginleika rafrænnar reikningsfærslu fyrir Finance eða Supply Chain Management.

    | Heiti eiginleika                         | Land/svæði  | Tilvísun eiginleika |
    |--------------------------------------|-----------------|-------------------|
    | Rafrænir reikningar í Austurríki (AT)    | Austurríki         | EUR-00023 |
    | Belgískur rafrænn reikningur (BE)      | Belgía         | EUR-00023 |
    | Brasilískt NF-e (BR)                  | Brasilía          | BR-00053 |
    | Brasilískt NFS-e ABRASF Curitiba (BR) | Brasilía          | BR-00095 |
    | Brasilískt NFS-e São Paulo (BR)       | Brasilía          | BR-00095 |
    | Danskur rafrænn reikningur (DK)       | Danmörk         | <p>EUR-00023</p><p>DK-00001</p> |
    | Hollenskur rafrænn reikningur (NL)        | Hollandi | EUR-00023 |
    | Egypskur rafrænn reikningur (EG)     | Egyptaland           | EG-00008 |
    | Eistneskur rafrænn reikningur (EE)     | Eistland         | EUR-00023 |
    | Finnskur rafrænn reikningur (FI)      | Finnland         | EUR-00023 |
     Franskur rafrænn reikningur (FR)       | Frakkland           | EUR-00023 |
    | Þýskur rafrænn reikningur (DE)       | Þýskaland         | EUR-00023 |
    | Mexíkóskur CFDI Interfactura (MX)       | Mexíkó          | <p>MX-00010</p><p>MX-00016</p> |
    | Norskur rafrænn reikningur (NO)    | Noregur          | <p>EUR-00023</p><p>NO-00010</p> |
    | Spænskur rafrænn reikningur (ES)      | Spánn           | <p>EUR-00023</p><p>ES-00025</p> |
    | Ítalskur rafrænn reikningur (IT)      | Ítalía           | <p>EUR-00023</p><p>IT-00036</p> |
    | PEPPOL rafrænn reikningur            | Evrópa          | EUR-00023 |

4. Veljið **Vista**.

## <a name="issue-electronic-invoices"></a>Gefa út rafræna reikninga

1. Farið í **Fyrirtækisstjórnun** \> **Reglubundið** \> **Rafræn skjöl** \> **Senda inn rafræn skjöl**.
2. Í flýtiflipanum **Færsla sem hafa á með** skal velja **Sía**.
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

Það fer eftir landi eða svæði hvort eiginleiki rafrænnar reikningsfærslu þurfi frekari skilgreiningu. Fyrir nákvæmar leiðbeiningar skal skoða fylgiskjalið „Hafist handa“ sem er í boði fyrir tilheyrandi land eða svæði.

## <a name="related-topics"></a>Tengd efnisatriði

- [Yfirlit innbótar rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Brasilíu](e-invoicing-bra-get-started.md)
- [Hafist handa með innbót rafrænna reikninga fyrir Mexíkó](e-invoicing-mex-get-started.md)
- [Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Ítalíu](e-invoicing-ita-get-started.md)
- [Rafrænir reikningar viðskiptavinar í Egyptalandi](emea-egy-e-invoices.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]