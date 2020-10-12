---
title: Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Brasilíu
description: Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Brasilíu í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6472672f5d618cc6d100298dd35939afa4c0066d
ms.sourcegitcommit: 025561f6a21fe8705493daa290f3f6bfb9f1b962
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/23/2020
ms.locfileid: "3835978"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a>Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Brasilíu 

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Viðbót rafrænnar reikningsfærslu fyrir Brasilíu styður ekki sem stendur allar aðgerðir sem eru í boði í samþættingu fjárhagsskjals sem er innbyggt í Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Brasilíu. Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi fyrir sig í Regulatory Configuration Services (RCS) og í Finance og Supply Chain Management. Það leiðir notandann einnig í gegnum ferlið við að senda inn NF-e-fjárhagsskjal (rafrænt fjárhagsskjalslíkan 55) í gegnum þjónustuna og útskýrir hvernig farið er yfir niðurstöður úrvinnslunnar og stöðu fjárhagsskjalanna.

## <a name="prerequisites"></a>Forkröfur

Áður en farið er í gegnum skrefin í þessu efnisatriði þarf að ljúka skrefunum í [Hafist handa með viðbót rafrænnar reikningsfærslu](e-invoicing-get-started.md).

## <a name="rcs-setup"></a>RCS-uppsetning

Við RCS-uppsetningu verður farið í gegnum þessi skref:

1. Flytja inn eiginleika rafrænnar reikningsfærslu fyrir NF-e fjárhagsskjöl.
2. Fara yfir skráarsniðin sem þarf til að senda inn NF-e fjárhagsskjöl til að fá heimild.
3. Fara yfir skráarsniðin sem þarf til að biðja um afturköllun á samþykktu NF-e.
4. Skilgreina tilvikið sem þarf til að senda inn NF-e fjárhagsskjöl til að fá heimild.
5. Skilgreina tilvikið sem þarf til að biðja um afturköllun á samþykktu NF-e.
6. Úthluta eiginleika rafrænnar reikningsfærslu á umhverfi rafrænnar reikningsfærsluviðbótar.
7. Birtið eiginleika rafrænnar reikningsfærslu.

> [!NOTE]
> „Eiginleiki rafrænnar reikningsfærslu“ er almennt heiti fyrir tilfangið sem er skilgreint og gefið út til að nota þjón rafrænnar reikningsfærsluviðbótar. Uppsetning á eiginleika rafrænnar reikningsfærslu sameinar meðal annars notkun á sniðum rafrænna skýrslugerðarskilgreininga til að búa til stillanlegar útflutnings- og innflutningsskrá, og notkun á aðgerðum og aðgerðarflæði til að virkja stofnun á stillanlegum reglum til að senda beiðnir, flytja inn svör og þátta innihald svara.

## <a name="import-the-e-invoicing-feature"></a>Flytja inn eiginleika rafrænnar reikningsfærslu

1. Skráðu þig inn á RCS-reikninginn þinn
2. Á vinnusvæðinu **Altækir eiginleikar**, undir hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja **Flytja inn** til að flytja inn eiginleika rafrænnar reikningsfærslu fyrir NF-e fjárhagsskjal úr altæku geymslunni.

    ![Flytja inn hnappur](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. Veljið eiginleika NF-e-fjárhagsskjals og veljið svo **Flytja inn**.

    ![Eiginleiki NF-e fluttur inn](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a>Búa til nýja útgáfu af eiginleika NF-e fjárhagsskjals

- Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja **Ný**.

![Nýrri útgáfu rafrænnar reikningsfærslu bætt við](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a>Uppfæra útgáfu skilgreiningar

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Skilgreiningar**, skal velja **Bæta við** eða **Eyða** til að stjórna útgáfum skilgreininga (skilgreiningar á skráarsniði rafrænnar skýrslugerðar).

    ![Stjórnun skilgreininga á eiginleikum rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - Þegar ný útgáfa af eiginleika NF-e fjárhagsskjals er búin til er öll skilgreiningarútgáfan (skráarsnið rafrænnar skýrslugerðar) erfð frá nýjustu útgáfunni.
    - Til að senda inn NF-e fjárhagsskjal vegna heimildar, eru eftirfarandi útgáfur skilgreiningar nauðsynlegar:

        - Útflutningssnið á innsendu NF-e
        - Innflutningur á svarskilaboði NF-e
        - Innflutningur á villukladda NF-e

    - Til að senda inn afturköllun á NF-e er eftirfarandi útgáfa skilgreiningar nauðsynleg:

        - Hætta við útflutningssnið NFe

2. Í listanum skal velja skilgreiningarútgáfu og síðan velja **Breyta** eða **Skoða** til að opna síðuna **Sniðshönnuður** þar sem hægt er að breyta eða skoða skilgreininguna.

    ![Síða sniðshönnuðar opnuð](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. Notið síðuna **Sniðshönnuður** til að breyta eða skoða skilgreiningar á skrá rafræns skýrslugerðarsniðs. Frekari upplýsingar er að finna í [Stofna skilgreiningar rafræns skjals](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).

    ![Síða sniðshönnuðar](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a>Stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu

- Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, skal velja **Bæta við** eða **Eyða** til að stjórna uppsetningum á eiginleika rafrænnar reikningsfærslu (þ.e. tilvikum NF-e).

![Umsjón með uppsetningum á eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

Þegar ný útgáfa af eiginleika NF-e fjárhagsskjals sem fengin er frá öðrum eiginleika rafrænnar reikningsfærslu, eru allar uppsetningar eiginleikans (tilvik NF-e) erfðar frá nýjustu útgáfunni.

Til að senda inn NF-e fjárhagsskjöl vegna heimildar, er uppsetning eiginleikans **Senda inn** nauðsynleg.

Til að senda inn afturköllun á NF-e, er uppsetning eiginleikans **Afturköllun** nauðsynleg.

#### <a name="configure-the-submit-feature-setup"></a>Skilgreina uppsetningu á eiginleika innsendingar

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, í dálknum **Uppsetning eiginleika**, skal velja **Senda inn**.
2. Veljið **Breyta**.

    ![Breyta uppsetningu á eiginleika rafrænnar reikningsfærslu](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. Á síðunni **Uppsetning á útgáfu eiginleika** skal velja flipann **Aðgerðir** til að stjórna lista yfir aðgerðir.

    ![Flipinn Aðgerðir.](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. Farið yfir þær aðgerðir sem þarf til að senda inn NF-e vegna heimildar.

    | Aðgerðarkenni | Heiti aðgerðar                  | Aðgerðarlýsing                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | 1         | Breyta skjali           | Stofnið NF-e XML-skrá til að senda inn.                          |
    | 2         | Skrifa undir skjal                | Notið stafrænt vottorð í XML-skránni.                    |
    | 3         | Hringja í SEFAZ-þjónustu í Brasilíu | Sendið inn undirritaða XML-skrá til vefþjónustunnar til að fá heimild. |
    | 4         | Vinna úr svari             | Fá svar vefþjónustunnar.                                     |
    | 5         | Breyta skjali           | Þáttið innihald skráarinnar sem er móttekið svar.     |
    | 6         | Breyta skjali           | Stofnið XML-skrána til að spyrjast fyrir um stöðu innsendingar.    |
    | 7         | Hringja í SEFAZ-þjónustu í Brasilíu | Sendið inn XML-skrána sem biður um stöðu innsendingar.          |
    | 8         | Vinna úr svari             | Fá svar vefþjónustunnar.                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Setja upp vefslóð fyrir SEFAZ-vefþjónustu 

1. Á síðunni **Uppsetning á útgáfu eiginleika**, í flipanum **Aðgerðir**, í flýtiflipanum **Aðgerðir**, skal velja **Hringja í SEFAZ-þjónustu í Brasilíu** (aðgerðarkenni **3**).
2. Í flýtiflipann **Færibreytur**, í reitinn **Færibreyta veffangs**, skal slá inn vefslóð SEFAZ-vefþjónustunnar fyrir innsendingu NF-e.
3. Í flýtiflipanum **Aðgerðir** skal velja **Hringja í SEFAZ-þjónustu í Brasilíu** (aðgerðarkenni **7**).
4. Í flýtiflipann **Færibreytur**, í reitinn **Færibreyta veffangs**, skal slá inn vefslóð SEFAZ-vefþjónustunnar fyrir innsendingu NF-e.

#### <a name="configure-the-cancellation-feature-setup"></a>Skilgreina uppsetningu á eiginleika afturköllunar

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Uppsetningar**, í dálknum **Uppsetning eiginleika**, skal velja **Afturköllun**.
2. Veljið **Breyta**.
3. Á síðunni **Uppsetning á útgáfu eiginleika** skal velja flipann **Aðgerðir** til að stjórna lista yfir aðgerðir.
4. Fara yfir aðgerðirnar sem þarf til að biðja um afturköllun á samþykktu NF-e.

    | Aðgerðarkenni | Heiti aðgerðar                  | Aðgerðarlýsing                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | 1         | Breyta skjali           | Stofnið NF-e XML-skrá afturköllunar til að senda inn.            |
    | 2         | Skrifa undir skjal                | Notið stafrænt vottorð í XML-skránni.                   |
    | 3         | Hringja í SEFAZ-þjónustu í Brasilíu | Sendið inn undirritaða XML-skrá til vefþjónustunnar vegna afturköllunar. |
    | 4         | Vinna úr svari             | Fá svar vefþjónustunnar.                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a>Setja upp vefslóð fyrir SEFAZ-vefþjónustu

1. Á síðunni **Uppsetning á útgáfu eiginleika**, í flipanum **Aðgerðir**, í flýtiflipanum **Aðgerðir**, skal velja **Hringja í SEFAZ-þjónustu í Brasilíu** (aðgerðarkenni **3**).
2. Í flýtiflipann **Færibreytur**, í reitinn **Færibreyta veffangs**, skal slá inn vefslóð SEFAZ-vefþjónustunnar fyrir afturköllun á samþykktu NF-e.

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a>Gera umhverfi rafrænnar reikningsfærslu tiltækt og úthluta útgáfudrög

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Umhverfi**, skal velja **Virkja**.
2. Í reitnum **Umhverfi** skal velja umhverfið.
3. Í reitnum **Gildir frá** skal velja dagsetninguna þegar nýja umhverfið tekur gildi.
4. Veljið **Virkja**.

![Umhverfi rafrænnar reikningsfærslu virkjað](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a>Breyta stöðu í lokið

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Drög**.
2. Velduð **Breyta stöðu \> Ljúka**.

### <a name="change-the-status-to-publish"></a>Breyta stöðu í birta

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu**, í flipanum **Útgáfur**, skal velja útgáfu fyrir eiginleika rafrænnar reikningsfærslu sem er með stöðuna **Lokið**.
2. Veljið **Breyta stöðu \> Birta**.

![Eiginleiki rafrænnar reikningsfærslu birtur](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a>Setja upp samþættingu rafrænnar reikningsfærsluviðbótar í Finance eða Supply Chain Management

Við uppsetningu verður farið í gegnum þessi skref:

1. Kveikið á eiginleika NF-e Federal fyrir Brasilíu.
2. Flytjið inn tilgreint gagnalíkan rafrænnar skýrslugerðar, gagnalíkansvörpun og snið sem eru nauðsynleg fyrir NF-e-fjárhagsskjöl.
3. Flytjið inn skilgreiningu rafrænnar skýrslugerðar og setjið upp svargerðir sem eru nauðsynlegar til að uppfæra stöðu fjárhagsskjalsins þegar innsendingarferlinu er skilað.

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a>Kveikja á eiginleika NF-e Federal fyrir Brasilíu

1. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
2. Í flipanum **Eiginleikar** skal velja gátreitinn **Virkja** í línunni fyrir tilvísun eiginleika **BR00053**.

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a>Flytja inn gagnalíkanavörpun rafrænnar skýrslugerðar sem þarf fyrir NF-e fjárhagsskjöl

1. Skráðu þig inn í Finance.
2. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**. Gangið úr skugga um að þessi skilgreiningarveita sé stillt á **Virk**. Frekari upplýsingar um hvernig á að stilla veitu á **Virk** er að finna í [Stofna skilgreiningarveitendur og merkja þá sem virka](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).
3. Veldu **Geymslur**.
4. Veljið **Altæk tilföng \> Opna**.
5. Flytja inn skilgreiningar **Fjárhagsskjalavörpunar**.

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a>Flytja inn skilgreiningar rafrænnar skýrslugerðar og setja upp svargerðir fyrir fjárhagsskjöl

1. Á vinnusvæðinu **Rafræn skýrslugerð**, í hlutanum **Veitendur skilgreininga**, skal velja reitinn **Microsoft**.
2. Veldu **Geymslur**.
3. Veljið **Altæk tilföng \> Opna**.
4. Flytjið inn **Innflutningur villukladda NF-e**, **Gagnainnflutningssnið NF-e svars** og **Innflutning svarskilaboða NF-e**.
5. Farið í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**.
6. Í flipanum **Rafrænt skjal** skal velja **Bæta við**.
6. Í reitinn **Töfluheiti** skal færa inn **Haus fjárhagsskjals**.
7. Í reitnum **Samhengi skjals** skal velja **Samhengislíkan viðskiptavinareiknings - Samhengi fjárhagsskjals**.
8. Veljið **Svargerðir**.
9. Veljið **Nýtt** og svo, í reitnum **Svargerð**, skal velja **Svar**.
10. Í reitnum **Staða sendingar** skal velja **Í bið**.
11. Í reitnum **Líkanavörpun** skal velja **Innflutningssnið svarskilaboða - Líkanavörpun úr svarskilaboðum**.
12. Veljið **Vista**.
13. Veljið **Nýtt** og svo, í reitinn **Svargerð**, skal velja **ResponseData**.
14. Í reitnum **Staða sendingar** skal velja **Í bið**.
15. Í reitinn **Líkanavörpun** skal velja **Gagnainnflutningssnið NF-e svars - Gagnainnflutningur svars**.
16. Veljið **Vista**.

## <a name="electronic-invoice-processing"></a>Rafræn reikningsfærsla í vinnslu

Við úrvinnslu í Finance verður lokið við þessi verk:

1. Sendið inn fjárhagsskjal í gegnum viðbót rafrænnar reikningsfærslu.
2. Skoðið keyrslukladda fyrir innsendingar og yfirfarið niðurstöður vinnslu.
3. Sendið inn afturköllun á fjárhagsskjali í gegnum viðbót rafrænnar reikningsfærslu.

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a>Sendið inn NF-e-fjárhagsskjöl fyrir SEFAZ-heimild 

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, ekki er elengur hægt að nota gamla ferlið til að senda inn NF-e fjárhagsskjöl fyrir heimild (**Útflutningur/innflutningur á NF-e-ferli**). Því er skipt út fyrir nýtt ferli sem kallast **Senda inn rafræn skjöl**.

> [!NOTE]
> Áður en haldið er áfram skal ganga úr skugga um að til staðar sé eitt eða fleiri fjárhagsskjalalíkan viðskiptavinar 55 sem voru gefin út af fjárhagsstofnun viðskiptavinar. Stefna þessara fjárhagsskjala verður að vera stillt á **Á útleið** og staðan verður að vera **Stofnað**. Frekari upplýsingar er að finna í [Gefa út fjárhagsskjal viðskiptavinar (Brasilía)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Senda inn rafræn skjöl**.
2. Fyrir fyrstu innsendingu á skjali skal alltaf stilla valkostinn **Senda skjöl inn aftur** á **Nei**. Ef senda þarf skjal inn aftur í gegnum þjónustuna skal stilla þennan valkost á **Já**.
3. Í flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann **Fyrirspurn** þar sem hægt er að búa til fyrirspurn til að velja skjöl til innsendingar.
4. Í flipanum **Svið** skal velja **Bæta við**.
5. Í reitnum **Tafla** skal velja **Haus fjárhagsskjals**.
6. Í reitnum **Afleidd tafla** skal velja **Haus fjárhagsskjals**.
6. Í reitnum **Svæði** skal velja **Númer**.
7. Í reitinn **Skilyrði** skal færa inn númer fjárhagsskjalsins sem á að senda inn.
8. Veljið **Í lagi** til að loka svarglugganum **Fyrirspurn**.
8. Veljið **Í lagi** til að senda inn valin skjöl.

> [!NOTE]
> Í fyrstu tilraun til að senda inn skjal í gegnum þjónustuna verður beðið um að staðfesta tenginguna við viðbót rafrænnar reikningsfærslu. Veljið **Smelltu hér til að tengjast sendingarþjónustu rafrænna skjala**.

### <a name="view-all-submission-logs"></a>Skoða alla innsendingarkladda

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu** er ný síða í boði sem gerir kleift að fylgja eftir innsendingarferli skjalsins. Hægt er að nota þessa síðu til að skoða innsendingarkladda fyrir öll send skjöl.

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.
2. Í reitnum **Gerð skjals** skal velja **Haus fjárhagsskjals** til að sía eingöngu fyrir fjárhagsskjölum.
3. Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.

![Skoða upplýsingar um innsendingarkladda](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> Fyrir NF-e-fjárhagsskjöl, sýnir dálkurinn **Villukóði** skilakóðann sem SEFAZ-vefþjónustan skilaði.

### <a name="view-submission-logs-through-the-fiscal-document-page"></a>Skoða innsendingarkladda í gegnum síðu fjárhagsskjala

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, er einnig hægt að skoða innsendingarkladdana í gegnum síðu fjárhagsskjala.

1. Farið í **Fjárhagur \> Fyrirspurnir og skýrslur \> Fjárhagsskjöl \> Öll fjárhagsskjöl**.
2. Veljið fjárhagsskjal sem var áður sent inn í gegnum viðbót rafrænnar reikningsfærslu.
3. Á aðgerðasvæðinu, í flipanum **NF-e Federal** skal velja **Kladdi rafræns skjals**.

![Innsendingarkladdar skoðaðir á síðu fjárhagsskjala](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a>Senda inn samþykkt NF-e-fjárhagsskjöl fyrir SEFAZ-afturköllun

Þegar kveikt hefur verið á eiginleikanum **Samþætting á stillanlegri viðbót rafrænnar reikningsfærslu**, verður ekki lengur hægt að nota gamla ferlið til að afturkalla NF-e fjárhagsskjöl. Því er skipt út fyrir nýja afturköllunarferlið sem er fellt inn í síðuna **Innsendingarkladdi rafrænna skjala**.

> [!NOTE]
> Gangið úr skugga um að afturköllun á fjárhagsskjali viðskiptavinar hafi verið keyrð fyrir samþykkt NF-e fjárhagsskjal. Frekari upplýsingar er að finna í [Hætta við fjárhagsskjal viðskiptavinar (Brasilía)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.
2. Veljið fjárhagsskjalið og veljið síðan **Aðgerðir \> Senda tengdar innsendingar**.
3. Færið inn lýsingu fyrir tengdu innsendinguna og veljið síðan **Í lagi**.

### <a name="view-cancellation-submission-logs"></a>Skoða innsendingarkladda afturköllunar

1. Farið í **Fyrirtækisstjórnun \> Reglubundið \> Rafræn skjöl \> Innsendingarkladdi rafrænna skjala**.
2. Í reitnum **Gerð skjals** skal velja **Haus fjárhagsskjals** til að sía eingöngu fyrir fjárhagsskjölum.
3. Veljið fjárhagsskjalið og síðan, á aðgerðasvæðinu, skal velja **Fyrirspurnir \> Tengdar innsendingar**.

    Tengdar innsendingar eru innsendingar sem tengjast aðalinnsendingunni sem var gerð fyrst. Til dæmis er innsendingin sem heimilar tiltekið NF-e aðalinnsendingin. Innsendingin sem biður um afturköllun á sama NF-e í SEFAZ er tengd innsending. Hún er aðeins til vegna þess að hún biður um afturköllun vinnslunnar sem var gerð í gegnum aðra innsendingu.

    Síðan **Tengdar innsendingar** sýnir allar tengdar innsendingar og stöðu þeirra fyrir tilgreint fjárhagsskjal. Á eftirfarandi mynd merkir fyrsta línan innsendinguna sem bað um samþykki á fjárhagsskjali. Önnur línan táknar innsendingu sem afturkallaði fjárhagsskjalið.

    ![Innsendingarkladdar afturköllunar skoðaðir](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. Á aðgerðasvæðinu skal velja **Fyrirspurnir \> Upplýsingar um sendingu** til að skoða upplýsingar um keyrslukladda innsendingar.

    ![Upplýsingar um innsendingarkladda afturköllunar skoðaðar](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a>Tilkynning um persónuvernd
Til að virkja eiginleikann BR-00053 (NF-e Federal) þarf hugsanlega að senda takmörkuð gögn, sem fela í sér skattskráningarkenni fyrirtækisins. Þetta verður sent til stofnanir þriðja aðila sem skattyfirvöld heimila að megi senda rafræna reikninga til þessara skattyfirvalda á fyrirframskilgreindu sniði sem þarf fyrir samþættingu við vefþjónustu yfirvalda. Stjórnandi getur kveikt og slökkt á eiginleika BR-00053 (NF-e Federal) með því að fara í **Fyrirtækisstjórnun \> Uppsetning \> Færibreytur rafrænna skjala**. Veljið flipann **Eiginleikar**, veljið línuna sem inniheldur BR-00053 eiginleikann og veljið viðeigandi atriði. Gögn sem eru flutt inn úr þessum ytri kerfum í þessa Dynamics 365-netþjónustu falla undir [yfirlýsingu okkar um persónuvernd](https://go.microsoft.com/fwlink/?LinkId=512132). Frekari upplýsingar er að finna í köflunum um persónuverndaryfirlýsingu í fylgiskjölum um eiginleika eftir löndum.


## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit innbótar rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með innbót rafrænna reikninga](e-invoicing-get-started.md)
- [Setja upp viðbót rafrænnar reikningsfærslu](e-invoicing-setup.md)
