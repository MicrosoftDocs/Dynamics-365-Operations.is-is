---
title: Hafist handa með innbót rafrænna reikninga fyrir Mexíkó
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Mexíkó í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
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
ms.openlocfilehash: d91f377af2514af932ea585adb75a56bdee13871
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988481"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a>Hafist handa með innbót rafrænna reikninga fyrir Mexíkó

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Viðbót rafrænnar reikningsfærslu fyrir Mexíkó styður hugsanlega ekki sem stendur allar aðgerðir sem eru í boði í skjalinu Comprobante Fiscal Digital por Internet (CFDI) og í tengdri samþættingu sem er byggð inn í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Mexíkó. Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi fyrir sig í Regulatory Configuration Services (RCS) og Finance. Það fer einnig í gegnum skrefin sem þarf að fylgja í Finance til að senda inn CFDI-reikninga í gegnum þjónustuna og það útskýrir hvernig á að fara yfir niðurstöður vinnslunnar og stöður CFDI-reikninga.

## <a name="prerequisites"></a>Forkröfur

Áður en farið er í gegnum skrefin í þessu efnisatriði þarf að ljúka skrefunum í [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-uppsetning

Við RCS-uppsetningu verður farið í gegnum þessi skref:

1. Flytja inn eiginleika rafrænnar reikningsfærslu fyrir úrvinnslu á CFDI-reikningum.
2. Farið yfir skilgreiningar sniðsins sem þarf til að búa til, senda inn og taka við svörum um CFDI-reikninga og til að senda inn og taka á móti svörum um afturköllun.
3. Skilgreinið tilvikin sem styðja við innsendingar CFDI-reikninga.
4. Birta eiginleika rafrænnar reikningsfærslu fyrir CFDI-reikninga.

> [!NOTE]
> „Eiginleiki rafrænnar reikningsfærslu“ er almennt heiti fyrir tilfangið sem er skilgreint og gefið út til að nota þjón rafrænnar reikningsfærsluviðbótar. Í þessu tilfelli eru CFDI-reikningar (MX) eiginleikinn fyrir rafræna reikningsfærslu sem verður settur upp.

## <a name="import-the-e-invoicing-feature"></a>Flytja inn eiginleika rafrænnar reikningsfærslu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækir eiginleikar**, undir hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Flytja inn** til að flytja inn eiginleikann **CFDI-reikningar (MX)** úr altæku geymslunni.

    > [!NOTE]
    > Ef ekki er hægt að sjá eiginleikann í listanum skal velja **Samstilla** og síðan endurtaka skref 3.

![Eiginleiki CFDI-reikninga (MX) fluttur inn](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

Þegar eiginleikinn **CFDI-reikningar (MX)** er fluttur inn úr altæku geymslunni, eru allar stillingar eiginleikans, þ.m.t. skilgreiningar og aðgerðir, einnig fluttar inn.

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>Búa til nýja útgáfu af eiginleika CFDI-reikninga (MX)

Hægt er að búa til nýja útgáfu ef til dæmis þarf að uppfæra vefslóðir. Frekari upplýsingar er að finna í [Rafræn reikningsfærsla CFDI](tasks/mx-00010-e-invoicing-cfdi.md).

- Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja **Ný**.

![Nýrri útgáfu rafrænnar reikningsfærslu bætt við](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>Uppfæra útgáfu skilgreiningar

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Skilgreiningar**, skal velja **Bæta við** eða **Eyða** til að stjórna útgáfum skilgreininga (skilgreiningar á skráarsniði rafrænnar skýrslugerðar).

    ![Stjórnun skilgreininga á eiginleikum rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    Þegar ný útgáfa er stofnuð eru allar skilgreiningar erfðar frá síðustu birtu útgáfu. Til að vinna úr CFDI-reikningum eru eftirfarandi skilgreiningar nauðsynlegar:

    - CFDI-reikningur (BusinessDocumentService)
    - Innflutningur á svarskilaboði CFDI
    - Innflutningur á villukladda CFDI
    - CFDI-afturköllunarbeiðni (MX) (BusinessDocumentService)
    - CFDI-reikningur (BusinessDocumentService)

2. Í listanum skal velja skilgreiningarútgáfu og síðan velja **Breyta** eða **Skoða** til að opna síðuna **Sniðshönnuður** þar sem hægt er að breyta eða skoða skilgreininguna.

    ![Síða sniðshönnuðar opnuð](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. Notið síðuna **Sniðshönnuður** til að breyta og skoða skilgreiningar á skrá rafræns skýrslugerðarsniðs. Frekari upplýsingar er að finna í [Stofna skilgreiningar rafræns skjals](../../dev-itpro/analytics/electronic-reporting-configuration.md).

    ![Síða sniðshönnuðar](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>Stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu

- Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, skal velja **Bæta við**, **Eyða** eða **Breyta** til að stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu.

![Umsjón með uppsetningum á eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

Til að senda CFDI-reikninga fyrir heimild (búa til XML-skrána, senda XML-skrána inn og vinna úr svari), þarf að setja upp eiginleikann **Sölureikningur**.

Til að senda inn afturköllun á CFDI-reikningi þarf að setja upp eiginleikana **Afturköllun** og **Hætta við**.

### <a name="configure-the-sales-invoice-feature-setup"></a>Skilgreina uppsetningu á eiginleika sölureiknings

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, í dálknum **Uppsetning eiginleika**, skal velja **Sölureikningur**.
2. Veljið **Breyta** til að skilgreina aðgerðir, gildissviðsreglur og breytur.

    ![Uppsetning á eiginleika rafrænnar reikningsfærslu breytt](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. Á síðunni **Uppsetning á útgáfu eiginleika** skal velja flipann **Aðgerðir** til að stjórna lista yfir aðgerðir. Aðgerðir skilgreina lista yfir aðgerðir sem þarf að keyra í réttri röð til að ná fullri keyrslu á tilvikinu.

    ![Flipinn Aðgerðir.](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | Aðgerðarkenni | Aðgerð                   | Heiti aðgerðar                                  | Aðgerðarlýsing                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | Breyta skjali       | Mynda rafrænan CFDI-reikning án stafrænnar undirskriftar | Mynda rafrænan CFDI-reikning.                                |
    | 2         | Skrifa undir skjal            | Stafræn undirskrift                                 | Skrifið stafrænt undir rafrænan reikning fyrir innsendingu.                |
    | 3         | Hringja í PAC-þjónustu í Mexíkó | Senda inn rafrænan CFDI-reikning                        | Biðlarinn Windows Communication Foundation (WCF) sendir inn rafrænan CFDI-reikning. |
    | 4         | Vinna úr svari         | Greina svar vefþjónustu                 | Greina svar vefþjónustunnar og skila villukladdanum. |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Setja upp vefslóð fyrir mexíkóska PAC-vefþjónustu 

1. Á síðunni **Uppsetning á útgáfu eiginleika**, í flipanum **Aðgerðir**, í flýtiflipanum **Aðgerðir**, skal velja **Hringja í mexíkóska PAC-þjónustu**.
2. Í flýtiflipann **Færibreytur**, í reitinn **Veffang**, skal slá inn vefslóð vefþjónustunnar fyrir innsendingu á CFDI-reikningi.

> [!NOTE]
> Notið sömu skrefin til að uppfæra vefslóðina fyrir aðgerðina **Hringja í mexíkóska PAC-þjónustu** fyrir uppsetninga á eiginleikunum **Hætta við** og **Afturköllunarbeiðni**.

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>Úthluta útgáfudrögum á umhverfi rafrænnar reikningsfærslu

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Umhverfi**, skal velja **Virkja**.
2. Í reitnum **Umhverfi** skal velja umhverfið.
3. Í reitnum **Gildir frá** skal velja dagsetninguna þegar nýja umhverfið tekur gildi.
3. Veljið **Virkja**.

![Umhverfi rafrænnar reikningsfærslu virkjað](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>Breyta stöðu útgáfu í Lokið

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Drög**.
2. Velduð **Breyta stöðu \> Ljúka**.

## <a name="change-the-version-status-to-published"></a>Breyta stöðu útgáfu í Birt

- Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja **Breyta stöðu \> Birta**.

## <a name="publish-the-e-invoicing-feature"></a>Birta eiginleika rafrænnar reikningsfærslu

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja flipann **Útgáfur** til að stjórna stöðunni á eiginleikanum **CFDI-reikningar (MX)**.
2. Veljið **Breyta stöðu** til að breyta stöðu eiginleikans.

![Stöðu eiginleika rafrænnar reikningsfærslu breytt](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a>Setja upp samþættingu á viðbót rafrænnar reikningsfærslu í Finance

Til að setja upp viðbót rafrænnar reikningsfærslu í Finance þarf að ljúka þessum verkum:

1. Flytjið inn gagnalíkan rafrænnar skýrslugerðar, gagnalíkansvörpun rafrænnar skýrslugerðar og snið sem eru nauðsynleg fyrir CFDI-reikninga.
2. Skilgreinið svargerðir fyrir uppfærslu á CFDI-reikningum. Þessar svargerðir eru notaðar fyrir svar frá þjóni samþykktrar vottorðaveitu (PAC).

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>Flytja inn gagnalíkan rafrænnar skýrslugerðar, gagnalíkanavörpun rafrænnar skýrslugerðar og skilgreiningar samhengis fyrir CFDI-reikninga

1. Skráðu þig inn í Finance.
2. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**. Gangið úr skugga um að þessi skilgreiningarveita sé stillt á **Virk**. Frekari upplýsingar um hvernig á að stilla veitu á **Virk** er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Veldu **Geymslur**.
4. Veljið **Altæk tilföng \> Opna**.
5. Flytjið inn **Reikningslíkan**, **Vörpun reikningslíkans**, **CFDI-reikningssnið (MX)**, **Snið afturköllunarbeiðni CFDI-reiknings (MX)** og **Afturköllunarsnið CFDI-reiknings (MX)**.

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>Kveikja á eiginleikanum fyrir úrvinnslu CFDI-reikninga

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipanum **Eiginleikar** skal velja gátreitinn **Virkja** í línunum fyrir tilvísanir eiginleika **MX-00010** og **MX-00016**.

![Kveikt á eiginleikunum fyrir úrvinnslu CFDI-reikninga](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>Flytja inn skilgreiningar rafrænnar skýrslugerðar og setja upp svargerðir fyrir uppfærslu á CFDI-reikningum

#### <a name="import-er-configurations"></a>Flytja inn rafræn skýrslugerð grunnstillingar

1. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**.
3. Veldu **Geymslur**.
4. Veljið **Altæk tilföng \> Opna**.
5. Flytjið inn **Líkan svarskilaboða**, **Innflutningur á villukladda CFDI (MX)** og **Innflutningur á svarskilaboði CFDI (MX)**.

#### <a name="set-up-the-response-types"></a>Setja upp svargerðirnar

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipanum **Rafrænt skjal** skal velja **Bæta við**.
3. Færið inn reikningabók viðskiptavinar og síðan í reitnum **Töfluheiti** skal velja verkreikninginn.
4. Fyrir hverja töflu skal skilgreina tengt skjalasamhengi:

    - Fyrir **Reikningabók viðskiptavinar** skal færa inn **Samhengi viðskiptavinareiknings**.
    - Fyrir **Verkreikningur** skal færa inn **Samhengi verkreiknings**.

4. Veljið **Svargerðir** til að skilgreina svargerðirnar sem hægt er að skila úr viðbót rafrænnar reikningsfærslu og hafa með í reikningabók viðskiptavinar eða verkreikningi.
5. Veljið **Nýtt** og svo, í reitnum **Svargerð**, skal velja **Svar**.
6. Í reitnum **Staða sendingar** skal velja **Í bið**.
7. Í reitnum **Líkanavörpun** skal velja **Innflutningssnið svarskilaboða - Líkanavörpun úr svarskilaboðum**.
8. Veljið **Vista**.
9. Veljið **Nýtt** og svo, í reitnum **Svargerð**, skal velja **ResponseData**.
10. Í reitnum **Staða sendingar** skal velja **Í bið**.
11. Í reitinn **Líkanavörpun** skal velja **Gagnainnflutningssnið CFDI-svars (upplýsingar) - Gagnainnflutningur svars**.
12. Veljið **Vista**.

## <a name="process-electronic-invoices-in-finance"></a>Vinna úr rafrænum reikningum í Finance 

Við vinnslu CFDI-reikninga í Finance í gegnum viðbót rafrænnar reikningsfærslu er hægt að framkvæma eftirfarandi verk:

- Senda inn rafræna CFDI-reikninga.
- Skoða keyrslukladda fyrir sendingar.
- Senda inn afturköllun á CFDI-reikningi.

### <a name="submit-cfdi-invoices"></a>Senda inn rafræna CFDI-reikninga

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, verður ekki lengur hægt að nota ferlið **Útflutningur/innflutningur á rafrænum reikningi** (**Viðskiptakröfur \> Reikningar \> Rafrænir reikningar**) til að senda inn CFDI-reikninga. Því er skipt út fyrir nýtt ferli sem kallast **Senda inn rafræn skjöl**.

> [!NOTE]
> Áður en nýja ferlið **Senda inn rafræn skjöl** er notað skal ganga úr skugga um að uppsetningunni sem þarf fyrir rafræna mexíkóska reikninga sé lokið. Frekari upplýsingar er að finna í [CFDI-útlitsútgáfu 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Senda inn rafræn skjöl**.
2. Fyrir fyrstu innsendingu á skjali skal alltaf stilla valkostinn **Senda skjöl inn aftur** á **Nei**. Ef senda þarf skjal inn aftur í gegnum þjónustuna skal stilla þennan valkost á **Já**.
3. Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann **Fyrirspurn** þar sem hægt er að búa til fyrirspurn til að velja skjöl til innsendingar.

![CFDI-skjal sent inn](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> Í fyrstu tilraun til að senda inn skjal í gegnum þjónustuna verður beðið um að staðfesta tenginguna við viðbót rafrænnar reikningsfærslu. Veljið **Smelltu hér til að tengjast sendingarþjónustu rafrænna skjala**.

### <a name="view-submission-logs"></a>Skoða innsendingarkladda

Hægt er að skoða innsendingarkladda fyrir öll send skjöl eða fyrir aðeins eitt innsent skjal.

#### <a name="view-all-submission-logs"></a>Skoða alla innsendingarkladda

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu** er ný síða í boði sem gerir kleift að fylgja eftir innsendingarferli skjalsins. Hægt er að nota þessa síðu til að skoða innsendingarkladda fyrir öll send skjöl.

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.
2. Í reitnum **Gerð skjals** skal velja **Reikningabók viðskiptavinar** til að sía fyrir nauðsynlegum rafrænum skjölum.

    ![Gerð skjals valin til að skoða innsendingarkladda](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.

    ![Skoða upplýsingar um innsendingarkladda](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

Upplýsingunum í innsendingarkladdanum er skipt niður á þrjá flýtiflipa:

- **Vinnsluaðgerðir** - Þessi flýtiflipi sýnir keyrslukladdann fyrir aðgerðirnar sem eru skilgreindar í útgáfu eiginleikans sem var sett upp í RCS. Dálkurinn **Staða** sýnir hvort tekist hafi að keyra aðgerðina.
- **Aðgerðaskrár** – Þessi flýtiflipi sýnir milliskrárnar sem voru myndaðar við keyrslu aðgerðanna. Hægt er að velja **Skoða** til að hlaða niður og skoða skrána.
- **Aðgerðarkladdi vinnslu** - Þessi flýtiflipi sýnir niðurstöður samskiptanna milli viðbótar rafrænnar reikningsfærslu og tilheyrandi vefþjónustu. Hann sýnir hverju úrvinnsla vefþjónustunnar skilaði. Dálkurinn **Villukóði** sýnir skilakóðann sem vefþjónusta heimildar skilaði.

Þegar innsendur CFDI-reikningur er heimilaður verður staða hans uppfærð í **Samþykktur**.

#### <a name="view-submission-logs-from-cfdi-invoices"></a>Skoða innsendingarkladda úr CFDI-reikningum

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu** er einnig hægt að skoða innsendingarkladdana úr CFDI-reikningum.

1. Farið í **Viðskiptakröfur \> Fyrirspurnir og skýrslur \> CFDI (rafrænir reikningar)**.
2. Veljið CFDI-reikning sem var sendur inn eftir að kveikt var á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**.
3. Á aðgerðasvæðinu, í flipanum **Ferill**, skal velja **Kladdi rafræns skjals**.

![Innsendingarkladdar skoðaðir í CFDI-reikningum](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> Fyrir CFDI-reikninga sem voru sendir inn áður en kveikt var á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, er hnappurinn **Ferill** í boði. Hnappurinn **Ferill** er ekki tiltækur fyrir CFDI-reikninga sem voru sendir inn eftir að kveikt var á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**.

### <a name="submit-cancellation-of-cfdi-invoices"></a>Senda inn afturköllun CFDI-reikninga

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, verður ekki lengur hægt að nota gamla ferlið til að hætta við CFDI-reikninga. Því er skipt út fyrir nýja afturköllunarferlið sem er fellt inn í síðuna **Innsendingarkladdi rafrænna skjala**.

1. Farið í **Viðskiptakröfur \> Fyrirspurnir og skýrslur \> CFDI (rafrænir reikningar)**.
2. Ef CFDI-reikningurinn er með stöðuna **Samþykktur** skal velja **Aðgerðir \> Hætta við CFDI**.
3. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.
4. Veljið CFDI reikninginn og veljið síðan **Aðgerðir \> Senda tengdar innsendingar**.
5. Færið inn lýsingu fyrir tengdu innsendinguna og veljið síðan **Í lagi**.

#### <a name="view-cancellation-submission-logs"></a>Skoða innsendingarkladda afturköllunar

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.
2. Í reitnum **Gerð skjals** skal velja **Reikningabók viðskiptavinar** til að sía eingöngu fyrir skjölum reikningabókar viðskiptavinar.
3. Veljið CFDI reikninginn og síðan, á aðgerðasvæðinu, skal velja **Fyrirspurnir \> Tengdar innsendingar**.

    Síðan **Tengdar innsendingar** sýnir allar tengdar innsendingar og stöðu þeirra fyrir tilgreindan CFDI-reikning. Á eftirfarandi mynd merkir fyrsta línan innsendinguna sem bað um samþykki á CFDI-reikningnum. Önnur línan táknar innsendingu sem hætti við þennan CFDI-reikning.

    ![Innsendingarkladdar afturköllunar skoðaðir](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.

    ![Upplýsingar um innsendingarkladda afturköllunar skoðaðar](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>Tilkynning um persónuvernd
Til að virkja eiginleikana MX-00010 og MX-00016 (CFDI-reikningur og CFDI-afturköllun) þarf hugsanlega að senda takmörkuð gögn, sem fela í sér skattskráningarkenni fyrirtækisins. Þetta verður sent til stofnanir þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda. Stjórnandi getur kveikt og slökkt á eiginleikum MX-00010 og MX-00016 (CFDI-reikningur og CFDI-afturköllun) með því að fara í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**. Veljið flipann **Eiginleikar**, veljið línurnar sem innihalda MX-00010 og MX-00016 eiginleikana og veljið viðeigandi atriði. Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í köflunum um persónuverndaryfirlýsingu í fylgiskjölum um eiginleika eftir löndum.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit innbótar rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með innbót rafrænna reikninga](e-invoicing-get-started.md)
- [Setja upp viðbót rafrænnar reikningsfærslu](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]