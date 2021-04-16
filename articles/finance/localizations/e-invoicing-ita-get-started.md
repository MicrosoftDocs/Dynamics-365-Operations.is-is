---
title: Hafist handa með rafrænar reikningsfærslur fyrir Ítalíu
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Ítalíu.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 23cb0523b6d6d065ad19f6c3bddf881b0dc82a7d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840101"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a>Hafist handa með rafrænar reikningsfærslur fyrir Ítalíu

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> Rafræn reikningsfærsla fyrir Ítalíu styður eins og er hugsanlega ekki allar aðgerðir sem eru í boði fyrir rafræna reikningsfærslu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management. 

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Ítalíu. Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi fyrir sig í Regulatory Configuration Services (RCS) og Finance. Það leiðir notandann einnig í gegnum ferlið til að senda inn rafræna reikninga sem eru myndaðir á ítalska sniðinu **FatturaPA** í gegnum þjónustuna og það útskýrir hvernig á að yfirfara niðurstöður vinnslunnar.

## <a name="prerequisites"></a>Forkröfur

Áður en farið er í gegnum skrefin í þessu efnisatriði þarf að ljúka skrefunum í [Hafist handa með rafrænni reikningsfærslu](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-uppsetning

Við RCS-uppsetningu verður farið í gegnum þessi skref:

1. Flytjið inn eiginleika rafrænnar reikningsfærslu fyrir útflutning á rafrænum reikningum viðskiptavinar á sniði **FatturaPA**.
2. Farið yfir skilgreiningar sniðsins sem þarf til að búa til, senda inn og taka við svörum um rafræna reikninga.
3. Skilgreinið tilvikin sem styðja við innsendingar rafrænna reikninga.
4. Birtið eiginleika rafrænnar reikningsfærslu.

> [!NOTE]
> „Eiginleiki rafrænnar reikningsfærslu“ er almennt heiti fyrir tilfangið sem er skilgreint og gefið út til að nota þjón rafrænnar reikningsfærslu. Í þessu tilfelli er útflutningur á rafrænum reikningum viðskiptavinar eiginleiki rafrænnar reikningsfærslu sem á að setja upp.

## <a name="import-the-e-invoicing-feature"></a>Flytja inn eiginleika rafrænnar reikningsfærslu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækir eiginleikar**, undir hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Flytja inn** til að flytja inn eiginleika rafrænnar reikningsfærslu úr altæku geymslunni.

    > [!NOTE]
    > Ef listinn yfir tiltæka eiginleika sést ekki skal velja **Samstilla**. 

4. Veljið eiginleikann **Útflutningur rafrænna reikninga (IT)** og síðan **Flytja inn**.

![Eiginleiki fyrir útflutning rafrænna reikninga (IT) fluttur inn](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

Þegar eiginleikinn **Útflutningur rafrænna reikninga (IT)** úr altæku geymslunni, eru allar stillingarnar sem lýst er í næsta hluta einnig fluttar inn.

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>Búa til nýja útgáfu af eiginleika fyrir útflutning rafrænna reikninga (IT)

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja **Ný**. 

    ![Nýrri útgáfu rafrænnar reikningsfærslu bætt við](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    Næst verða skilgreind snið rafrænnar skýrslugerðar sem tengjast eiginleika rafrænnar reikningsfærslu.

2. Í flipanum **Skilgreiningar** skal velja **Bæta við** til að stjórna útgáfum skilgreininga.

    ![Umsjón með skilgreiningarútgáfum fyrir eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    Í þessu skrefi er bætt við og skilgreind snið rafrænnar skýrslugerðar fyrir mismunandi skrár sem notaðar eru til að flytja út ítalska rafræna reikninga. Fyrir ítalska FatturaPA rafræna reikninga skal nota annaðhvort hefðbundnar skilgreiningar eða sérstilltu skilgreiningarnar sem notaðar eru fyrir rafræna reikningsfærslu:

    - Sölureikningur (IT)
    - Verkreikningur (IT)

    Þegar búinn er til eiginleiki rafrænnar reikningsfærslu út frá öðrum eiginleika rafrænnar reikningsfærslu, eru öll snið rafrænnar skýrslugerðar erfð frá upprunalega eiginleikanum.

3. Veljið ákveðna skráarskilgreiningu fyrir snið rafrænnar skýrslugerðar.
4. Veljið **Breyta** eða **Skoða** til að opna síðuna **Sniðshönnuður**.

    ![Síða sniðshönnuðar opnuð](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. Notið síðuna **Sniðshönnuður** til að breyta og skoða skilgreiningar á skrá rafræns skýrslugerðarsniðs.

    ![Síða sniðshönnuðar](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu

- Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, skal velja **Bæta við**, **Eyða** eða **Breyta** til að stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu.

![Umsjón með uppsetningum á eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

Í þessu skrefi eru skilgreind tilvik sem eiga við um rafræna reikninga, þar á meðal myndun XML-úttaksskráa á **FatturaPA** sniði og stafræna undirskrift (ef þess er krafist).

### <a name="configure-the-sales-invoice-feature-setup"></a>Skilgreina uppsetningu á eiginleika sölureiknings

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, í dálknum **Uppsetning eiginleika**, skal velja **Sölureikningur**.
2. Veljið **Breyta**.
3. Á síðunni **Uppsetning á útgáfu eiginleika** skal velja flipann **Aðgerðir** til að stjórna lista yfir aðgerðir. Aðgerðir skilgreina lista yfir aðgerðir sem þarf að keyra í réttri röð til að ná fullri keyrslu á tilvikinu.

    ![Flipinn Aðgerðir.](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | Aðgerðarkenni | Heiti aðgerðar        | Aðgerðarlýsing                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | Breyta skjali | Stofnið XML-skrá fyrir rafrænan reikning á **FatturaPA** sniði. |
    | 2         | Skrifa undir skjal      | Notið stafræna undirskrift á XML-skrána.             |

4. Veljið flipann **Gildissviðsreglur** til að skoða og vinna með gildissviðsreglur. Gildissviðsreglur skilgreina samhengið þar sem aðgerðin verður framkvæmd.

    ![Flipi fyrir gildissviðsreglur](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. Veljið flipann **Breytur** til að skoða og vinna með breyturnar.

    ![Breytuflipi](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. Skilgreinið almennu breyturnar sem eru nauðsynlegar til að framkvæma aðgerðirnar.

### <a name="configure-the-project-invoice-feature-setup"></a>Skilgreina uppsetningu á eiginleika verkreiknings 

Skrefin og stillingarnar sem eru nauðsynleg til að skilgreina uppsetningu á eiginleika **Verkreiknings** eru mjög svipuð skrefum og stillingum fyrir uppsetningu á eiginleika **Sölureiknings**. Þegar unnið er með verkreikninga skal líta á ferla fyrir sölureikninga.

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>Úthluta eiginleika rafrænnar reikningsfærslur á umhverfið

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Umhverfi**, skal velja **Virkja**.
2. Í reitnum **Umhverfi** skal velja umhverfið.
3. Í reitnum **Gildir frá** skal velja dagsetninguna þegar nýja umhverfið tekur gildi.
4. Veljið **Virkja**. 

![Umhverfi rafrænnar reikningsfærslu virkjað](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>Birta eiginleika rafrænnar reikningsfærslu

Hægt er að birta eiginleika rafrænnar reikningsfærslu með því að breyta stöðu útgáfunnar í **Lokið** eða **Birtur**.

### <a name="change-the-version-status-to-completed"></a>Breyta stöðu útgáfu í Lokið

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Drög**.
2. Velduð **Breyta stöðu \> Ljúka**. 

### <a name="change-the-version-status-to-published"></a>Breyta stöðu útgáfu í Birt 

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Lokið**.
2. Veljið **Breyta stöðu \> Birta**.

![Stöðu eiginleika rafrænnar reikningsfærslu breytt](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a>Setja upp samþættingu rafrænnar reikningsfærslu í Finance

Við uppsetningu á Finance verður þessum verkum lokið:

1. Flytjið inn gagnalíkan rafrænnar skýrslugerðar, gagnalíkanavörpun rafrænnar skýrslugerðar og skilgreiningar samhengis fyrir rafræna FatturaPA-reikninga.
2. Skilgreinið vottorðið sem er krafist til að skrifa undir ítalska rafræna reikninga.

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>Flytja inn gagnalíkan rafrænnar skýrslugerðar, vörpun gagnalíkans og snið

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal staðfesta að skilgreiningarveitan **Þjónusta viðskiptaskjala** sé stillt á **Virk**.
2. Veldu **Geymslur**.
3. Veljið **Altæk tilföng \> Opna**.
4. Flytjið inn **Reikningslíkan**, **Vörpun reikningslíkans** og **Samhengislíkan viðskiptavinareiknings**.

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>Kveikja á eiginleikanum fyrir útflutning á rafrænum reikningum viðskiptavinar fyrir Ítalíu

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipanum **Eiginleikar** skal velja gátreitinn **Virkjað** í línunni fyrir tilvísun eiginleika **IT00036**.

![Kveikt á eiginleika FatturaPA](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>Skilgreina rafræn skjöl

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipanum **Rafrænt skjal** skal velja **Bæta við** og færa inn töflurnar sem þarf til að mynda ítalska rafræna reikninga:

    - **Töfluheiti:** Reikningabók viðskiptavinar
    - **Töfluheiti:** Verkreikningur

3. Fyrir hverja töflu skal skilgreina tengt skjalasamhengi:

    - Fyrir **Reikningabók viðskiptavinar** skal velja **Samhengi viðskiptavinareiknings**.
    - Fyrir **Verkreikningur** skal velja **Samhengi verkreiknings**.

![Svargerðir settar upp](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>Rafræn reikningsfærsla í vinnslu

Við úrvinnslu í Finance verður lokið við þessi verk:

1. Mynda ítalska rafræna reikninga í gegnum rafræna reikningsfærslu
2. Skoða keyrslukladda og yfirfara niðurstöður vinnslu

### <a name="generate-electronic-invoices"></a>Búa til rafræna reikninga

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri rafrænnni reikningsfærslu** og eiginleikinn **IT00036** hefur verið virkjaður, verður ekki lengur hægt að nota gamla Finance-ferlið til að mynda ítalska rafræna reikninga. Því er skipt út fyrir nýtt ferli sem kallast **Senda inn rafræn skjöl**.

Hægt er að senda skjölin inn handvirkt, út frá eftirspurn eftir skjölum rafrænna reikninga.

> [!NOTE]
> Áður en haldið er áfram skal ganga úr skugga um að uppsetningunni sem krafist er fyrir ítalska rafræna reikninga sé lokið. Frekari upplýsingar er að finna í [Rafrænir reikningar viðskiptavinar](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices). Hafa skal í huga að einhver uppsetningarskref sem lýst er í því efnisatriði kunna að vera ekki í boði vegna virkjunar á rafrænni reikningsfærslu.

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Senda inn rafræn skjöl**.
2. Fyrir fyrstu innsendingu á skjali skal stilla valkostinn **Senda skjöl inn aftur** á **Nei**. Ef senda þarf skjal inn aftur í gegnum þjónustuna skal stilla þennan valkost á **Já**.
3. Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann **Fyrirspurn** þar sem hægt er að búa til fyrirspurn til að velja skjöl til innsendingar.

![Svarglugginn fyrir innsendingu rafrænna skjala](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>Síufyrirspurn

1. Í svarglugganum **Fyrirspurn** skal skilgreina síuskilyrðin fyrir bæði sölureikninga og verkreikninga eða skilja skilyrðin eftir auð til að hafa með alla ósenda reikninga.

    ![Síuskilyrði innsendingar stillt](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. Veljið **Í lagi** til að loka svarglugganum **Fyrirspurn**.
3. Veljið **Í lagi** til að senda inn valin skjöl.

> ![ATHUGIÐ] Í fyrstu tilraun til að senda inn skjal í gegnum þjónustuna verður beðið um að staðfesta tenginguna við rafræna reikningsfærslu. Veljið **Smelltu hér til að tengjast sendingarþjónustu rafrænna skjala**.

#### <a name="view-submission-logs"></a>Skoða innsendingarkladda

Hægt er að skoða innsendingarkladda fyrir öll send skjöl.

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.
2. Í reitnum **Gerð skjals** skal velja **Reikningabók viðskiptavinar** eða **Verkreikningur** til að síða fyrir nauðsynleg rafræn skjöl.

    ![Gerð skjals valin til að skoða innsendingarkladda](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    Gildið sem er sýnt í dálknum **Staða innsendingar** táknar stöðu innsendingarferlisins. Það gefur til kynna hvort ferlið hafið gengið samkvæmt skilgreiningu og hvort frekari aðgerða sé þörf.

3. Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.

    ![Skoða upplýsingar um innsendingarkladda](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. Í flýtiflipanum **Vinnsluaðgerðir** er hægt að skoða keyrslukladdann fyrir aðgerðirnar sem eru skilgreindar í útgáfu eiginleikans sem var sett upp í RCS. Dálkurinn **Staða** sýnir hvort tekist hafi að keyra aðgerðina.
5. Í flýtiflipanum **Aðgerðaskrár** er hægt að skoða milliskrár sem voru myndaðar við keyrslu aðgerðanna. Hægt er að velja **Skoða** til að hlaða niður XML-úttaksskránni á **FatturaPA** sniði og skoða innihald hennar.

## <a name="related-topics"></a>Tengd efnisatriði

- [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með rafrænar reikningsfærslur](e-invoicing-get-started.md)
- [Setja upp rafrænar reikningsfærslur](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
