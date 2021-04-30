---
title: Sérstilla skilgreiningar rafrænnar skýrslugerðar til að búa til rafrænt skjal
description: Í þessu efnisatriði er útskýrt hvernig á að sérstilla skilgreiningar Microsoft á rafrænni skýrslugerð sem eru notaðar til að búa til sérstillt rafrænt skjal.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ec5b8d0ad1e85a9c4fc7c3eb762c2c7b0b52e8d
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893301"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Sérstilla skilgreiningar rafrænnar skýrslugerðar til að búa til rafrænt skjal

[!include[banner](../includes/banner.md)]

[Rammi rafrænnar skýrslugerðar](general-electronic-reporting.md) gerir þér kleift að hlaða upp [skilgreiningum](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar sem Microsoft býður upp á í Microsoft Dynamics 365 Finance-tilvikið þitt. Á þennan hátt geta skilgreiningar Microsoft þjónar sem rafræn skýrslugerðarlausn sem er notuð til að búa til rafræna reikninga viðskiptavina. Hægt er að nota þessa skilgreiningu rafrænnar skýrslugerðar til að sérstilla rafrænu skýrslugerðarlausnina þína til að fá aðgang að sérstilltum gagnagrunnssvæðum og búa til rafræna reikninga sem falla undir tilteknum kröfum þínum, án þess að þurfa að breyta upprunakóðanum.

## <a name="overview"></a>Yfirlit

Í þessu efnisatriði þarf til dæmis að tilgreina auðkenniskóða alríkisskatts sem nýja sérstillta eigind fyrir hvern viðskiptavin sem þú sendir rafræna reikninga til. Þess vegna þarf að sérstilla skipulag reikningsins sem er nú í notkun með því að bæta við nýrri vöru sem verður að fylla út með skattkóðanum í öllum rafrænum reikningum sem eru búnir til.

Aðferðirnar í þessu efnisatriði útskýra hvernig notandi í hlutverki kerfisstjóra, þróunaraðila rafrænnar skýrslugerðar eðaí hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar getur framkvæmt þessi verk í Finance-tilvikinu þínu:

- [Skilgreina lágmarkssafn af færibreytum rafrænnar skýrslugerðar sem þarf til að byrja að nota ramma rafrænnar skýrslugerðar](#ConfigureER).
- [Flytja inn upphaflegar útgáfur af stöðluðum skilgreiningum rafrænnar skýrslugerðar sem gefnar eru upp til að búa til rafræna reikninga](#ImportERConfigurations1).
- [Skilgreina færibreytur viðskiptakrafna til að byrja að nota staðlaðar skilgreiningar rafrænnar skýrslugerðar](#ConfigureAR1).
- [Skilgreina færibreytur lögaðila til að senda viðskiptavinum reikning](#ConfigureLE).
- [Undirbúa viðskiptavinafærslu fyrir rafræna reikningsfærslu](#ConfigureCustomer1).
- [Bæta við, bóka og senda reikning viðskiptavinar með því að nota skilgreiningar fyrir staðlaða skilgreiningu rafrænnar skýrslugerðar](#ProcessInvoice1).
- [Bæta við sérstilltum gagnagrunnsreit til að stjórna auðkenniskóði alríkisskatts fyrir viðskiptavini](#AddCustomField).
- [Uppfæra lýsigögn rafrænnar skýrslugerðar til að virkja breytingar á gagnagrunni fyrir hönnuð líkanavörpunar fyrir rafræna skýrslugerð](#RefreshERMetadata).
- [Hanna sérstilltar skilgreiningar rafrænnar skýrslugerðar til að búa til rafræna reikninga sem innihalda nýja skattkóðann](#DesignCustomERConfigurations).
- [Skilgreina færibreytur viðskiptakrafna til að byrja að nota sérstilltar skilgreiningar rafrænnar skýrslugerðar](#ConfigureAR2).
- [Uppfæra viðskiptavinafærslu fyrir rafræna reikningsfærslu](#ConfigureCustomer2).
- [Bæta við, bóka og senda reikning viðskiptavinar með því að nota sérstillta skilgreiningu rafrænnar skýrslugerðar](#ProcessInvoice2).
- [Flytja inn nújar útgáfur af stöðluðum skilgreiningum rafrænnar skýrslugerðar sem gefnar eru upp til að búa til rafræna reikninga](#ImportERConfigurations2).
- [Aðlaga breytingarnar að nýjum útgáfum af stöðluðum skilgreiningum rafrænnar skýrslugerðar í sérstilltum skilgreiningum rafrænnar skýrslugerðar](#RebaseCustomERConfigurations).
- [Bæta við, bóka og senda reikning viðskiptavinar með því að nota nýjar útgáfur af sérstilltum skilgreiningum rafrænnar skýrslugerðar](#ProcessInvoice3).

Hægt er að ljúka við allar þessar aðgerðir í **DEMF** fyrirtækinu.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>Skilgreina ramma rafrænnar skýrslugerðar

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar eða þróunarhlutverki rafrænnar skýrslugerðar þarftu að skilgreina lágmarkssafn af færibreytum rafrænnar skýrslugerðar. Síðan geturðu farið að nota umgjörð rafrænnar skýrslugerðar til að sérstilla útgáfur af stöðluðum skilgreiningum rafrænu skýrslugerðarlausnarinnar sem er notuð til að búa til rafræna reikninga.

### <a name="configure-er-parameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Færibreytur rafrænnar skýrslugerðar**.
3. Á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Almennt**, skal stilla valkostinn **Kveikja á hönnunarstillingu** á **Já**.
4. Í flipanum **Viðhengi**, í reitnum **Skilgreiningar**, skal velja **Skrá**.
5. Í reitunum **Verksafn**, **Tímabundið**, **Grunnlína** og **Annað** skal velja gerð fyrir **Skrá**.

Frekari upplýsingar um færibreytur rafrænnar skýrslugerðar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>Virkja skilgreiningarveitu rafrænnar skýrslugerðar

Allar skilgreiningar rafrænnar skýrslugerðar sem bætt er við eru merktar sem eign skilgreingarveitu rafrænnar skýrslugerðar. Skilgreiningarveita rafrænnar skýrslugerðar sem er virkjuð á vinnusvæðinu **Rafræn skýrslugerð** er notuð í þessum tilgangi. Þess vegna þarf að virkja skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð** áður en byrjað er að bæta við eða breyta skilgreiningum rafrænnar skýrslugerðar.

> [!NOTE]
> Aðeins eigandi skilgreiningar rafrænnar skýrslugerðar getur breytt henni. Þess vegna, áður en hægt er að breyta skilgreiningu rafrænnar skýrslugerðar, verður að virkja viðeigandi skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð**.

#### <a name="review-the-list-of-er-configuration-providers"></a>Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Tafla yfir skilgreiningarveitur** er hver færsla með einkvæmt heiti og vefslóð. Farið yfir efnið á þessari síðu. Ef færsla fyrir **Litware, Inc.** (`https://www.litware.com`) er þegar til skal sleppa næsta ferli, [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Skilgreiningarveitur** skal velja **Ný**.
4. Í reitinn **Heiti** skal færa inn **Litware, Inc.**
5. Í reitinn **Veffang** skal færa inn `https://www.litware.com`.
6. Veljið **Vista**.

#### <a name="activate-an-er-configuration-provider"></a>Virkja skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Litware, Inc.** og síðan velja **Stilla sem virkt**.

Nánari upplýsingar um skilgreiningarveitur rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Flytja inn upphaflegar útgáfur staðlaðra skilgreininga rafrænnar skýrslugerðar

Til að bæta stöðluðum skilgreiningum rafrænnar skýrslugerðar við núverandi Finance-tilvikið þitt, þarftu að flytja þær inn úr [gagnageymslu](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar sem var skilgreind fyrir það tilvik.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Microsoft** og síðan velja **Gagnageymslur** til að skoða lista yfir gagnageymslur fyrir Microsoft-veituna.
3. Á síðunni **Skilgreiningageymslur** skal velja gagnageymslu af gerðinni **Altæk** og síðan velja **Opna**. Ef beðið er um heimild til að tengjast við Regulatory Configuration Service, skal fylgja leiðbeiningum um heimild.
4. Á síðunni **Skilgreiningageymsla**, í skilgreiningatrénu vinstra megin á svæðinu, skal velja skilgreiningarsniðið **PEPPOL sölureikningur**.
5. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **11.2.2**.
6. Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu.

![Síðan Skilgreiningagagnasafn](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Ef það reynist erfitt að opna [Altæka geymsla](er-download-configurations-global-repo.md) er hægt að [sækja skilgreiningar](download-electronic-reporting-configuration-lcs.md) hjá Microsoft Dynamics Lifecycle Services (LCS) í staðinn.

### <a name="review-the-imported-er-configurations"></a>Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar** skal stækka flýtiflipann **Skilgreiningarþættir**.
4. Í skilgreiningartrénu vinstra megin skal stækka **Reikningslíkan** og síðan stækka **UBL-sölureikning**.

Takið eftir að til viðbótar við valið rafrænt skýrslugerðarsnið **PEPPOL sölureikningur**, voru aðrar áskildar skilgreiningar rafrænnar skýrslugerðar fluttar inn. Vegna þess að nýjar útgáfur af skilgreiningum rafrænnar skýrslugerðar eru jafnt og þétt birtar í altækri geymslu og LCS til að samsvarandi lausnir fylgi eftir nýjum kröfum, voru nýjustu útgáfur af nauðsynlegri skilgreiningu [gagnalíkans](general-electronic-reporting.md#data-model-and-model-mapping-components) og skilgreiningum [líkanavörpunar](general-electronic-reporting.md#data-model-and-model-mapping-components) fluttar inn.

![Skilgreiningasíða](./media/er-quick-start3-imported-solution1a.png)

Til að líkja eftir stöðunni sem skilgreiningar rafrænnar skýrslugerðar í núverandi Finance-tilviki yrðu ef þú fluttir inn útgáfu **11.2.2** af rafrænu skýrslugerðarsniðinu **PEPPOL sölureikningur** áður fyrr (til dæmis 7. ágúst 2019), skal fylgja þessum skrefum.

- Á aðgerðasvæðinu skal velja **Eyða** til að eyða öllum skilgreiningum rafrænnar skýrslugerðar sem voru gefnar út eftir 7. ágúst 2019. Aðeins skilgreiningarnar **Reikningslíkan**, **Líkanavörpun reiknings** (hét upprunalega **Líkanavörpun viðskiptavinareiknings**), **UBL-sölureikningur** og **PEPPOL sölureikningur** verða að vera eftir.
- Fyrir eftirstandandi skilgreiningar rafrænnar skýrslugerðar, í flýtiflipanum **Útgáfur**, skal velja **Eyða** til að eyða öllum útgáfum af skilgreiningum rafrænnar skýrslugerðar sem voru gefnar út eftir 7. ágúst 2019.

Gangið síðan úr skugga um að eftirfarandi skilgreiningar séu í boði í skilgreiningartrénu:

- **Reikningslíkan** skilgreining gagnalíkans rafrænnar skýrslugerðar (hét upphaflega **Reikningslíkan viðskiptavinar**):

    - Útgáfa 11 inniheldur útgáfu 10 af [gagnalíkansþætti](general-electronic-reporting.md#data-model-and-model-mapping-components) rafrænnar skýrslugerðar sem stendur fyrir gagnskipulag viðskiptaléns reikningsfærslunnar. Þessi skilgreining rafrænnar skýrslugerðar hefur verið flutt inn sem eldri útgáfa af rafrænu skýrslugerðarsniði **PEPPOL sölureiknings** sem var valið fyrir innflutning.
    - Útgáfa 50 inniheldur útgáfu 31 af gagnalíkansþætti rafrænnar skýrslugerðar. Þessi skilgreining rafrænnar skýrslugerðar hefur verið flutt inn sem eldri útgáfa af útgáfunni frá 7. ágúst 2019 af skilgreiningu **Líkanavörpunar reiknings** fyrir rafræn skýrslugerð.

    ![Skilgreining á gagnalíkani rafrænnar skýrslugerðar fyrir reikningslíkan á skilgreiningarsíðunni](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Ef þú sérð ekki útgáfu 50 af þessu gagnalíkani skaltu opna altæku geymsluna og flytja inn útgáfu 50.19 af skilgreiningu **Líkanavörpunar reiknings** fyrir rafræna skýrslugerð.

- Skilgreinin **Líkanavörpunar reiknings** fyrir rafræna skýrslugerð (hét upphaflega **Líkanavörpun viðskiptavinareiknings**):

    - Útgáfa 50.19 hefur verið flutt inn sem nýjasta innleiðingin af útgáfu 50 af skilgreiningu **Reikningslíkans** fyrir gagnalíkan rafrænnar skýrslugerðar. Hún inniheldur tvo þætti [líkanavörpunar](general-electronic-reporting.md#data-model-and-model-mapping-components) fyrir rafræna skýrslugerð sem lýsa því hvernig fyllt er út í gagnalíkanið með forritsgögnum á keyrslutíma.

    ![Skilgreining líkanavörpunar reiknings fyrir líkanavörpun rafrænnar skýrslugerðar á skilgreiningarsíðunni](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Ef þú sérð ekki útgáfu 50.19 af þessari líkanavörpun skaltu opna altæku geymsluna og flytja inn útgáfu 50.19 af skilgreiningu **Líkanavörpunar reiknings** fyrir rafræna skýrslugerð.

- Skilgreining **UBL-sölureiknings** fyrir rafrænt skýrslugerðarsnið:

    - Útgáfa 11.2 inniheldur [sniðið](general-electronic-reporting.md#FormatComponentOutbound) og rafræna skýrslugerðarþætti sniðsvörpunar. Sniðshlutinn tilgreinir útlit skýrslunnar. Sniðsvörpunarhlutinn inniheldur gagnagjafa líkansins og tilgreinir hvernig þessi gagnagjafi er notaður til að fylla út skýrsluútlitið á keyrslutíma. Þetta snið rafrænnar skýrslugerðar var skilgreint til að búa til rafræna reikninga á UBL-sniði. Það hefur verið flutt inn sem yfirsnið af rafrænu skýrslugerðarsnið **PEPPOL-sölureiknings** sem var valið fyrir innflutning.

- Skilgreining **PEPPOL-sölureiknings** fyrir rafrænt skýrslugerðarsnið:

    - Útgáfa 11.2.2 inniheldur sniðhlut og sniðsvörpunarhlut rafrænna skýrslugerðar sem voru skilgreindir til að búa til rafræna reikninga á PEPPOL-sniði.

    ![Skilgreining PEPPOL-sölureiknings fyrir rafrænt skýrslugerðarsnið á skilgreiningarsíðunni](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Skilgreina færibreytur viðskiptakrafna

1. Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur viðskiptakröfu**.
2. Í flipanum **Rafræn skjöl**, í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Sölu- og kreditreikningur með frjálsum texta**, skal velja **PEPPOL-sölureikningur**.
3. Veljið **Vista**.

![Flipi fyrir rafræn skjöl á færibreytusíðu viðskiptakrafna](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Skilgreina færibreytur lögaðila

1. Fara í **Fyrirtækisstjórnun** \> **Fyrirtæki** \> **Lögaðilar**.
2. Fyrir valda fyrirtækið **DEMF**, í flýtiflipanum **Bankareikningsupplýsingar**, í reitinn **Leiðarnúmer**, skal slá inn **1234**.
3. Veljið **Vista**.
4. Lokið síðunni **Lögaðilar**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Búa til færslu viðskiptavinar

1. Farið í **Viðskiptakröfur** \> **Viðskiptavinir** \> **Allir viðskiptavinir**.
2. Á síðunni **Allir viðskiptavinir** skal velja tengil **DE-014** viðskiptavinalykils.

### <a name="add-a-customer-contact"></a>Bæta við tengilið viðskiptavinar

1. Farið í **Viðskiptakröfur** \> **Viðskiptavinir** \> **Allir viðskiptavinir**.
2. Á aðgerðasvæðinu, í flipanum **Viðskiptavinir**, í flokknum **Lyklar**, skal velja **Tengiliðir**.
3. Veljið **Bæta við tengiliðum**.
4. Á síðunni **Tengiliðir**, í reitnum **Fornafn**, skal opna uppflettinguna, velja **Adam Carter** og síðan velja **Velja** til að loka uppflettingunni.
5. Veljið **Vista**.
6. Lokið síðunni **Tengliðir**.

### <a name="define-a-primary-contact"></a>Skilgreina aðaltengilið

1. Farið í **Viðskiptakröfur** \> **Viðskiptavinir** \> **Allir viðskiptavinir**.
2. Á flýtiflipanum **Lýðfræðilegar sölur**, í reitnum **Aðaltengiliður**, skal velja **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>Stilla valkost rafrænnar reikningsfærslu

1. Farið í **Viðskiptakröfur** \> **Viðskiptavinir** \> **Allir viðskiptavinir**.
2. Í flýtiflipanum **Reikningur og afhending** skal stilla valkostinn **Rafrænn reikningur** á **Já**.
3. Veljið **Vista**.
4. Lokið síðunni **Allir viðskiptavinir**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Vinna úr reikningi viðskiptavinar með því að nota staðlaðar skilgreiningar rafrænnar skýrslugerðar

Nú er hægt að nota staðlaðar skilgreiningar rafrænnar skýrslugerðar sem voru fluttar inn til að senda rafrænt reikning með frjálsum texta til viðskiptavinar.

### <a name="add-a-new-invoice"></a>Bæta við nýjum reikningi

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Á síðunni **Reikningur með frjálsum texta** skal velja **Nýr**.
3. Í flýtiflipanum **Haus textareiknings**, í reitnum **Viðskiptavinalykill**, skal velja **DE-014**.
4. Í flýtiflipanum **Reikningslínur** er reikningslínu sjálfkrafa bætt við. Stillið eftirfarandi reiti í þessari línu:

    - Í reitinn **Lýsing** skal slá inn **Minnisbók**.
    - Í reitinn **Aðallykill** skal velja **401100**.
    - Í reitinn **Einingarverð** skal slá inn **1000**.

5. Veljið **Vista**.

![Síða reiknings með frjálsum texta](./media/er-quick-start3-add-invoice.png)

Nánari upplýsingar er að finna í [Stofna reikning með frjálsum texta](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Bóka nýjan reikning

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Á síðunni **Reikningur með frjálsum texta**, á aðgerðasvæðinu, skal velja **Bóka**.
3. Í gátreitinn **Bóka reikning með frjálsum texta** skal velja **Í lagi**.

![Upplýsingasíða um reikninga með frjálsum texta](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Senda bókaðan reikning

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Á síðunni **Reikningur með frjálsum texta**, á aðgerðasvæðinu, í flokknum **Skjal**, skal velja **Senda** \> **Upprunalegt**.

    ![Forskoðun upprunalega reikningsins](./media/er-quick-start3-send-invoice.png)

3. Lokið síðunni **Reikningur með frjálsum texta**.

### <a name="analyze-a-generated-e-invoice"></a>Skoða myndaðan rafrænan reikning

1. Farið í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Rafræn skýrslugerðarvinnsla**.
2. Á síðunni **Rafræn skýrslugerðarvinnsla** skal velja upphaflegu færsluna sem með verklýsinguna **Senda XML rafræns reiknings**.
3. Veljið **Sýna skrár** til að sjá lista yfir myndaðar skrár.

    ![Upplýsingasíða yfir rafræna skýrslugerð](./media/er-quick-start3-jobs-list.png)

4. Veljið **Opna** til að hlaða niður XML-skrá rafræns reiknings sem er búinn til.
5. Greina XML-skrá rafræns reiknings. Takið eftir því að skattaskema viðskiptavinar er sem stendur sýnt með XML-eigindunum **schemeID** og **schemeAgencyID**. Takið einnig eftir því að XML-einingin **cbc:CustomizationID** inniheldur núna eftirfarandi texta: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Forskoða myndaða XML-skrá rafræns reiknings](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Bæta við sérstilltu gagnagrunnssvæði

Hægt er að nota eiginleikann [Sérsniðið svæði](../../fin-ops/get-started/user-defined-fields.md) til að gera eftirfarandi sérstillingu í núverandi Finance-tilviki:

- Sérstillið skipulag gagnagrunns með því að bæta við nýju sérstilltu gagnagrunnssvæði sem geymir auðkenniskóða alríkisskatts fyrir hvern viðskiptavin.
- Sérstillið síðuna **Viðskiptavinur** með því að bæta við nýjum gagnaskráningarreit sem hægt er að nota til að færa inn gildi skattkóða í nýja sérstilla gagnagrunnssvæðið.

Fylgjið þessum skrefum til að gera sérstillinguna.

1. Farið í **Viðskiptakröfur** \> **Viðskiptavinir** \> **Allir viðskiptavinir**.
2. Á síðunni **Allir viðskiptavinir** skal velja tengil **DE-014** viðskiptavinalykils.
3. Í flýtiflipanum **Almennt** skal hægrismella á autt svæði undir reitnum **Tungumál** og síðan velja **Sérstilla: UpperGroup**.

    Efnið í flýtiflipanum **Almennt** er auðkennt og valmyndin **Sérstilla** birtist.

4. Í valmyndinni **Sérstilla** skal velja **Bæta við reit**.
5. Í svarglugganum **Bæta við dálkum** skal velja **Stofna nýjan reit**.
6. Í svarglugganum **Stofna nýjan reit**, í reitnum **Töfluheiti**, skal velja **Viðskiptavinir**.
7. Í reitinn **Forskeyti heitis** skal færa inn **FederalTaxID**.

    > [!NOTE]
    > Allt reitarheitið hefur verið skilgreint sjálfkrafa sem **FederalTaxID\_Custom**.

8. Í reitinn **Merki** skal slá inn **Kóða alríkisskatts**.
9. Í reitnum **Gerð** skal velja **Texti**.
10. Í reitinn **Lengd** skal slá inn **20**.
11. Veljið **Vista**.
12. Í skilaboðaglugganum sem birtist skal velja **Já** til að staðfesta að þú viljir búa til nýja reitarfærslu **FederalTaxID** fyrir töfluna **Viðskiptavinir**.
13. Veljið **Setja inn** til að <a name="insert_custom_field"></a>bæta reitnum **FederalTaxID\_Custom** við núverandi síðu.

    ![Síða allra viðskiptavina](./media/er-quick-start3-create-new-field.gif)

14. Lokið síðunni **Allir viðskiptavinir**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>Uppfæra lýsigögn rafrænnar skýrslugerðar

Uppfæra þarf lýsigögn rafrænnar skýrslugerðar til að gera sérstillta reitinn sem bætt var við [sýnilegan](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) í hönnuði líkanavörpunar rafrænnar skýrslugerðar.

1. Farið í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Endurbyggja töflutilvísanir**.
2. Í svarglugganum **Uppfæra gagnalíkan** skal velja **Í lagi**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Hanna sérstilltar skilgreiningar rafrænnar skýrslugerðar

Hægt er að nota skilgreiningar rafrænnar skýrslugerðar sem Microsoft býður upp á til að hanna þínar eigin sérstilltu skilgreiningar rafrænnar skýrslugerðar þannig að þær geti búið til rafræna reikninga sem innihalda nýja skattkóðann.

### <a name="customize-the-data-model-configuration"></a>Sérstilla skilgreiningu gagnalíkansins

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar, geturðu hannað þín eigin sérstilltu gagnalíkön rafrænnar skýrslugerðar.

#### <a name="add-a-custom-data-model-configuration"></a>Bæta við sérstilltri skilgreiningu gagnalíkans

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan viðskiptavinar**.
3. Í aðgerðasvæðinu velurðu **Stofna skilgreiningu**.
4. Í fellilistanum, í reitnum **Ný**, skal velja **Leiða af heiti: Reikningslíkan viðskiptavinarm Microsoft** til að gefa til kynna að nýja sérstillta skilgreiningin þín af gagnalíkani rafrænnar skýrslugerðar eigi að vera í skilgreiningu gagnalíkans rafrænnar skýrslugerðar.
5. Í reitinn **Heiti** skal færa inn **Reikningslíkan (Litware)**.
6. Veljið **Stofna skilgreiningu** til að bæta við nýrri skilgreiningu rafrænnar skýrslugerðar.

Nú er hægt að nota gagnalíkanshönnuð rafrænnar skýrslugerðar til að breyta útgáfu 50.1 af rafrænu skýrslugerðarskilgreiningunni **Reikningslíkan (Litware)** í **Drög** [stöðuna](general-electronic-reporting.md#component-versioning).

![Útgáfa 50.1 af skilgreiningu rafrænnar skýrslugerðar á skilgreiningarsíðunni](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Skilgreina sérsniðið gagnalíkan

Þú verður að breyta sérsniðnu gagnalíkaninu með því að bæta við nýjum reit til að gefa upp gildi auðkenniskóða alríkisskatts. Þessi kóði er hluti af gögnum viðskiptavinar fyrir hvert snið rafrænnar skýrslugerðar sem notar þetta gagnalíkan sem gagnagjafa.

1. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal velja **Reikningslíkan (Litware)**.
2. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **50.1** af valdri skilgreiningu á gagnalíkani rafræns skýrslugerðarsniðs í stöðunni **Drög**.
3. Á aðgerðasvæðinu skal velja **Hönnuður** fyrir valda útgáfu skilgreiningar.
4. Á síðunni **Hönnuður gagnalíkans**, í gagnalíkanstrénu, skal velja **Upplýsingar um viðskiptavin (viðskiptavinur)**.
5. Veljið **Nýtt**.
6. Í fellilistanum, í reitnum **Nýr hnútur sem**, skal samþykkja sjálfgefið gildi, **Undireining virks hnúts**.
7. Í reitinn **Heiti** skal færa inn **FederalTaxID\_Litware**.
8. Í reitnum **Gerð atriðis** skal samþykkja sjálfgefið gildi, **Strengur**.
9. Veljið **Bæta við** og veljið síðan **Vista**.

    ![Hönnunarsíða gagnalíkans](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > Reitirnir **Merki** og **Lýsing** lýsa tilgangi nýja reitsins. Hægt er að fylla út í þessa reiti á mörgum tungumálum. Frekari upplýsingar er að finna í [Hanna skýrslur á mörgum tungumálum í rafrænni skýrslugerð](er-design-multilingual-reports.md).

10. Lokið síðunni **Hönnuður gagnalíkans**.

#### <a name="complete-a-custom-data-model-configuration"></a>Ljúka sérstilltri skilgreiningu gagnalíkans

[Ljúka](general-electronic-reporting.md#component-versioning) þarf vinnunni á útgáfu 50.1 af sérstilltri skilgreiningu á gagnalíkani rafrænnar skýrslugerðar til að gera hana aðgengilega þannig að hægt sé að bæta við öðrum sérstilltum skilgreiningum rafrænnar skýrslugerðar.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan** og velja **Reikningslíkan (Litware)**.
3. Í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka** og síðan velja **Í lagi**.

Staða útgáfu 50.1 er breytt úr **Drög** í **Lokið** og útgáfa verður skrifvarin. Nýrri og breytanlegri útgáfu 50.2 hefur verið bætt við og er með stöðuna **Drög**. Hægt er að nota þessa útgáfu til að gera seinni tíma breytingar á sérstilltri skilgreiningu á gagnalíkani rafrænnar skýrslugerðar.

![Útgáfu 50.1 lokið á skilgreiningarsíðunni](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Sérstilla skilgreiningu líkanavörpunar

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar geturðu hannað þín eigin sérstilltu líkön rafrænnar skýrslugerðar.

#### <a name="add-a-custom-model-mapping-configuration"></a>Bæta við nýrri sérstilltri skilgreiningu á líkanavörpun

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan viðskiptavinar** og velja **Vörpun reikningslíkans viðskiptavinar**.
3. Í aðgerðasvæðinu velurðu **Stofna skilgreiningu**.
4. Í fellilistanum, í reitnum **Ný**, skal velja **Leiða af heiti: Vörpun reikningslíkans viðskiptavinar Microsoft** til að gefa til kynna að nýja sérstillta skilgreiningin þín á líkanavörpun rafrænnar skýrslugerðar eigi að byggjast á skilgreiningu líkanavörpunar rafrænnar skýrslugerðar.
5. Í reitinn **Heiti** skal færa inn **Vörpun reikningslíkans (Litware)**.
6. Í reitnum **Marklíkan** skal velja **Reikningslíkan (Litware)**.

    > [!IMPORTANT]
    > Þetta skref er mjög mikilvægt. Ef því er sleppt verður ekki hægt að nota sérsniðið gagnalíkan í vörpun á skilgreindu líkani.

7. Veljið **Stofna skilgreiningu** til að bæta við nýrri skilgreiningu rafrænnar skýrslugerðar.

![Skilgreiningu á sérstilltri líkanavörpun bætt við skilgreiningarsíðuna](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Skilgreina sérstillta vörpun líkans

Breyta þarf sérstilltri vörpun líkans og tilgreina hvernig fylla á út sérstillta reitinn **FederalTaxID\_Litware** fyrir sérstillta gagnalíkanið með forritsgögnum á keyrslutíma.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan viðskiptavinar** \> **Vörpun á reikningslíkani viðskiptavinar** og velja **Vörpun Reikningslíkans (Litware)**.
3. Í aðgerðarúðunni skal velja **Hönnuður**.
4. Á síðunni **Vörpun líkans í gagnagjafa** skal velja vörpunina **Reikningur viðskiptavinar**.

    ![Síðan fyrir vörpun líkans í gagnagjafa](./media/er-quick-start3-select-customer-mapping.png)

5. Veljið **Hönnuður**.
6. Á síðunni **Hönnuður líkanavörpunar**, á svæðinu **Gagnagjafar**, skal stækka gagnagjafann **CustInvoiceJour** sem stendur fyrir forritstöfluna **CustInvoiceJour**.
7. Undir **CustInvoiceJour** skal stækka **Tengsl** til að fara yfir listann af tengslum af gerðinni „margar við eina“ (N:1) fyrir töfluna **CustInvoiceJour**.
8. Undir **CustInvoiceJour** \> **Tengsl** skal stækka **Viðskiptavinir (CustTable)** til að fá aðgang að reitum og tengslum í töflunni **Viðskiptavinir (CustTable)**.
9. Veljið **FederalTaxID\_Custom** gagnaveitusvæðið sem var innleitt [fyrr](#insert_custom_field).
10. Á svæðinu **Gagnalíkan** skal stækka **Upplýsingar um viðskiptavin (viðskiptavinur)** og velja gagnalíkansreitinn **FederalTaxID\_Litware**.
11. Veldu **Binda**.

    ![Hönnuðarsíðan líkanavörpun](./media/er-quick-start3-customize-model-mapping.gif)

12. Veljið **Vista**.
13. Lokið síðunni **Hönnuður líkanavörpunar**.
14. Lokið síðunni **Líkanavörpun á gagnagjafa**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Ljúka við nýja sérstillta skilgreiningu á líkanavörpun

[Ljúka](general-electronic-reporting.md#component-versioning) þarf við vinnuna á útgáfu 50.19.1 á sérstilltri skilgreiningu á líkanavörpun rafrænnar skýrslugerðar til að gera hana aðgengilega.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan viðskiptavinar** \> **Vörpun á reikningslíkani viðskiptavinar** og velja **Vörpun Reikningslíkans (Litware)**.
3. Í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka** og síðan velja **Í lagi**.

Staða útgáfu 50.19.1 er breytt úr **Drög** í **Lokið** og útgáfa verður skrifvarin. Nýrri og breytanlegri útgáfa 50.19.2 hefur verið bætt við og er með stöðuna **Drög**. Hægt er að nota þessa útgáfu til að gera seinni tíma breytingar á sérstilltri skilgreiningu á líkanavörpun rafrænnar skýrslugerðar.

![Útgáfu 50.19.1 lokið á skilgreiningarsíðunni](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> [Stuðningstími](general-electronic-reporting-manage-configuration-lifecycle.md) skilgreiningarinnar nær ekki yfir stuðningstíma gagnagrunnsbreytinganna. Ef útgáfa 50.19.1 af skilgreiningunni **Vörpun reikningslíkans (Litware)** er flutt út úr núverandi Finance-tilviki og reynt að flytja hana inn í annað tilvik sem inniheldur ekki sérstilltan reit **FederalTaxID\_Custom** í töflunni **CustTable**, kemur upp undantekning. Undantekningin útskýrir að innflutt skilgreining rafrænnar skýrslugerðar samræmist ekki lýsigögnum Finance-tilviksins.

### <a name="customize-the-format-configuration"></a>Sérstilla skilgreiningu sniðs

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar, geturðu hannað þitt eigið snið rafrænnar skýrslugerðar.

#### <a name="add-a-custom-format-configuration"></a>Bæta við sérstilltri skilgreiningu sniðs

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan viðskiptavinar** \> **UBL-sölureikningur** og velja **PEPPOL-sölureikningur**.
3. Í aðgerðasvæðinu velurðu **Stofna skilgreiningu**.
4. Í fellilistanum, í reitnum **Ný**, skal velja **Leiða af heiti: PEPPOL-sölureikningur, Microsoft** til að gefa til kynna að sérstillta skilgreiningin þín á sniði rafrænnar skýrslugerðar eigi að byggjast á skilgreiningu rafrænnar skýrslugerðar.
5. Í reitinn **Heiti** skal færa inn **Peppol-sölureikningur (Litware)**.
6. Í reitnum **Gagnalíkan** skal velja **Reikningslíkan (Litware)** til að nota sérsniðna hluti gagnalíkans og líkanavörpunar.

    > [!NOTE]
    > Þetta skref er mjög mikilvægt. Ef því er sleppt verður ekki hægt að nota sérsniðið gagnalíkan í skilgreindu sniði.

7. Í reitnum **Gagnalíkan** skal velja rótarskilgreininguna **InvoiceCustomer**.
8. Veljið **Stofna skilgreiningu** til að bæta við nýrri skilgreiningu rafrænnar skýrslugerðar.

![Skilgreiningu á sérstilltri sniði bætt við skilgreiningarsíðuna](./media/er-quick-start3-adding-custom-format.png)

Nú er hægt að nota gagnalíkanshönnuð rafrænnar skýrslugerðar til að breyta útgáfu 11.2.2.1 af rafrænu skýrslugerðarskilgreiningunni **Peppol-sölureikningur (Litware)** í **Drög** [stöðuna](general-electronic-reporting.md#component-versioning).

![Útgáfa 11.2.2.1 af skilgreiningu rafrænnar skýrslugerðar á skilgreiningarsíðunni](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Skilgreina sérstillt snið

Þú verður að breyta sérstillta sniðinu með því að bæta við nýrri sniðseiningu til að fylla út í gildið auðkenniskóða alríkisskatts fyrir reikningsfærðan viðskiptavin.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan viðskiptavinar** \> **UBL-sölureikningur** \> **PEPPOL-sölureikningur** og velja **PEPPOL-sölureikningur (Litware)**.
3. Í aðgerðarúðunni skal velja **Hönnuður**.
4. Í sniðstrénu skal stækka **XMLHeader** \> **Reikningur** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** og velja **cbc:ID**.
5. Veljið **Bæta við** og veljið síðan **XML** \> **Eigind**.
6. Í svarglugganum **Eiginleiki hlutar**, í reitinn **Heiti**, skal færa inn **FederalTaxID**.
7. Veljið **Í lagi** til að bæta við nýrri sniðseiningu til að stofna nýja XML-eigind **FederalTaxID** í myndaðri XML-skrá.
8. Í sniðstrénu sundir **XMLHeader** \> **Reikningur** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** og velja **FederalTaxID**.
9. Veldu **Færa upp**.

![Ný sniðseining á sniðshönnunarsíðunni](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Skilgreina sérstillta sniðsvörpun

1. Á síðunni **Sniðshönnuður** í flipanum **Vörpun** skal stækka gagnagjafann **Reikningur** af gerðinni **Líkan**.
2. Undir **Reikningur** skal stækka **Upplýsingar um viðskiptavin (viðskiptavinur)** og velja **FederalTaxID\_Litware**.
3. Veldu **Binda**.

    ![Síða sniðshönnuðar](./media/er-quick-start3-customized-format-mapping.png)

4. Veljið gagnagjafann **Reikningur** af gerðinni **Líkan** og veljið síðan **Breyta**.
5. Í reitnum **Útgáfa** skal velja útgáfu **1** af sérstillta gagnalíkaninu og velja síðan **Í lagi**.
6. Veljið **Vista**.
7. Lokaðu síðunni **Sniðshönnuður**.

#### <a name="complete-a-custom-format-configuration"></a>Ljúka við sérstillta skilgreiningu á sniði

[Ljúka](general-electronic-reporting.md#component-versioning) þarf við vinnuna á útgáfu 11.2.2.1 á sérstilltri skilgreiningu rafræns skýrslugerðarsniðs til að gera hana aðgengilega.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan viðskiptavinar** \> **UBL-sölureikningur** \> **PEPPOL-sölureikningur** og velja **PEPPOL-sölureikningur (Litware)**.
3. Í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka** og síðan velja **Í lagi**.

Staða útgáfu 11.2.2.1 er breytt úr **Drög** í **Lokið** og útgáfa verður skrifvarin. Nýrri og breytanlegri útgáfa 11.2.2.2 hefur verið bætt við og er með stöðuna **Drög**. Hægt er að nota þessa útgáfu til að gera seinni tíma breytingar á sérstilltri skilgreiningu á sniði rafrænnar skýrslugerðar.

![Útgáfu 11.2.2.1 lokið á skilgreiningarsíðunni](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Skilgreina færibreytur viðskiptakrafna til að byrja að nota sérstilltar skilgreiningar rafrænnar skýrslugerðar

1. Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur viðskiptakröfu**.
2. Í flipanum **Rafræn skjöl**, í flýtiflipanum **Rafræn skýrslugerð**, í reitnum **Sölu- og kreditreikningur með frjálsum texta**, skal velja **PEPPOL-sölureikningur (Litware)**.
3. Veljið **Vista**.

![Færibreytusíða viðskiptakrafna, flipi rafrænna skjala, flýtiflipi rafrænnar skýrslugerðar](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Uppfæra viðskiptavinafærslu með því að bæta við auðkenniskóði skatts

1. Farið í **Viðskiptakröfur** \> **Viðskiptavinir** \> **Allir viðskiptavinir**.
2. Á síðunni **Allir viðskiptavinir** skal velja tengil **DE-014** viðskiptavinalykils.
3. Í flýtiflipanum **Almennt**, í reitinn **Skattnúmer** skal færa inn **LITWARE-6789**.
4. Veljið **Vista**.

    ![DE-014 upplýsingasíða viðskiptavinar](./media/er-quick-start3-added-tax-id-value.png)

5. Lokið síðunni **Allir viðskiptavinir**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Vinna úr reikningi viðskiptavinar með því að nota sérstilltar skilgreiningar rafrænnar skýrslugerðar

### <a name="select-and-send-a-posted-invoice"></a>Velja og senda bókaðan reikning

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Á síðunni **Reikningur með frjálsum texta** skal velja reikninginn sem var bætt við og bókaður hér á undan.
3. Á aðgerðasvæðinu, í flokknum **Skjal**, skal velja **Senda** \> **Upprunalegt**.
4. Lokið síðunni **Reikningur með frjálsum texta**.

### <a name="analyze-a-generated-e-invoice"></a>Skoða myndaðan rafrænan reikning

1. Farið í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Rafræn skýrslugerðarvinnsla**.
2. Á síðunni **Rafræn skýrslugerðarvinnsla** skal velja nýjustu færsluna sem með verklýsinguna **Senda XML rafræns reiknings**.
3. Veljið **Sýna skrár** til að sjá lista yfir myndaðar skrár.
4. Veljið **Opna** til að hlaða niður XML-skrá rafræns reiknings sem er búinn til.
5. Greina XML-skrá rafræns reiknings. Takið eftir því að samkvæmt sérstillingum inniheldur skattskema viðskiptavinar sérstillta **FederalTaxID** XML-eigind til viðbótar við **schemeID** og **schemeAgencyID** XML-eigindir. Gildi þessarar nýju XML-eigindar er tilgreint af skattnúmerinu **LITWARE-6789** sem fært var inn fyrir reikningsfærðan viðskiptavin.

    ![Forskoða myndaða XML-skrá rafræns reiknings með sérstillingunni](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Flytja inn nýjustu útgáfur staðlaðra skilgreininga rafrænnar skýrslugerðar

Til að halda safni staðlaðra skilgreininga rafrænnar skýrslugerðar í Finance-tilvikinu [uppfærðu](general-electronic-reporting-manage-configuration-lifecycle.md) þarf að flytja inn nýjar útgáfur af þeim í hvert sinn sem þær verða aðgengilegar í [gagnageymslu](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar sem var skilgreind fyrir það tilvik.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Microsoft** og síðan velja **Gagnageymslur** til að skoða lista yfir gagnageymslur fyrir Microsoft-veituna.
3. Á síðunni **Skilgreiningageymslur** skal velja gagnageymslu af gerðinni **Altæk** og síðan velja **Opna**. Ef beðið er um heimild til að tengjast við Regulatory Configuration Service, skal fylgja leiðbeiningum um heimild.
4. Á síðunni **Skilgreiningageymsla**, í skilgreiningatrénu vinstra megin á svæðinu, skal velja skilgreiningarsniðið **PEPPOL sölureikningur**.
5. Í flýtiflipanum **Útgáfur** skal velja útgáfu **32.6.7** af valdri skilgreiningu á sniði rafrænnar skýrslugerðar sem hefur verið gefin út til að styðja rafræna reikninga viðskiptavinar á sniði PEPPOL BIS 3. Nánari upplýsingar eru í [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu í núverandi fjármálatilvik.

![Útgáfa 32.6.7 valin á síðu skilgreiningageymslu](./media/er-quick-start3-import-solution2.png)

Frekari upplýsingar um hvernig hægt er að gera þetta ferli sjálfvirkt er að finna í [Flytja inn uppfærðar útgáfur skilgreininga rafrænnar skýrslugerðar](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Stækkið flýtiflipann **Skilgreiningarþættir**.
4. Í skilgreiningartrénu vinstra megin skal stækka **Reikningslíkan**. Takið eftir að heitið á **Reikningslíkani viðskiptavinar** hefur breyst í **Reikningslíkan** í einni innfluttu skilgreiningum á gagnalíkani rafrænnar skýrslugerð.
5. Í skilgreiningartrénu vinstra megin skal stækka **Vörpun reikningslíkans**. Takið eftir að heitið á **Vörpun reikningslíkans viðskiptavinar** hefur breyst í **Vörpun reikningslíkans** í einni af innfluttu skilgreiningum á líkanavörpun rafrænnar skýrslugerðar.
6. Stækkið **UBL-sölureikning** \> **PEPPOL-sölureikning**.

Takið eftir að til viðbótar við valið rafrænt skýrslugerðarsnið **PEPPOL-sölureikningur**, voru nýjustu útgáfur af öðrum áskildum skilgreiningum rafrænnar skýrslugerðar fluttar inn. Vegna þess að nýjar útgáfur af skilgreiningum rafrænnar skýrslugerðar eru jafnt og þétt birtar í altækri geymslu og LCS til að samsvarandi rafrænar skýrslugerðarlausnir fylgi eftir nýjum kröfum, voru nýjustu útgáfur af nauðsynlegri skilgreiningu gagnalíkans og skilgreiningum líkanavörpunar fluttar inn.

Gangið úr skugga um að eftirfarandi skilgreiningar rafrænnar skýrslugerðar verði á endanum í boði í skilgreiningartrénu:

- **Reikningslíkan** Skilgreining gagnalíkans rafrænnar skýrslugerðar:

    - Útgáfa 206 (eða nýrri) inniheldur útgáfu 24 (eða eldri) af gagnalíkansþætti rafrænnar skýrslugerðar sem stendur fyrir gagnskipulag viðskiptaléns reikningsfærslunnar. Þessi skilgreining rafrænnar skýrslugerðar hefur verið flutt inn sem eldri skilgreiningu **Líkanavörpunar reiknings** fyrir rafræna skýrslugerð.

    ![Útgáfa 206 á skilgreiningarsíðunni](./media/er-quick-start3-imported-solution2b1.png)

- Skilgreining líkanavörpunar rafrænnar skýrslugerðar fyrir **Vörpun reikningslíkans**:

    - Útgáfa 206.132 (eða nýrri) hefur verið flutt inn sem nýjasta innleiðingin af útgáfu 206 af skilgreiningu **Reikningslíkans** fyrir gagnalíkan rafrænnar skýrslugerðar. Hún inniheldur nokkra þætti líkanavörpunar fyrir rafræna skýrslugerð sem lýsa því hvernig fyllt er út í gagnalíkanið með forritsgögnum á keyrslutíma.

    ![Útgáfa 206.132 á skilgreiningarsíðunni](./media/er-quick-start3-imported-solution2b2.png)

- Skilgreining **UBL-sölureiknings** fyrir rafrænt skýrslugerðarsnið:

    - Útgáfa 32.6 inniheldur sniðið og rafræna skýrslugerðarþætti sniðsvörpunar. Sniðshlutinn tilgreinir útlit skýrslunnar. Sniðsvörpunarhlutinn inniheldur gagnagjafa líkansins og tilgreinir hvernig þessi gagnagjafi er notaður til að fylla út skýrsluútlitið á keyrslutíma. Þetta snið rafrænnar skýrslugerðar var skilgreint til að búa til rafræna reikninga á UBL-sniði. Það hefur verið flutt inn sem yfirsnið af rafrænu skýrslugerðarsnið **PEPPOL-sölureiknings** sem var valið fyrir innflutning.

- Skilgreining **PEPPOL-sölureiknings** fyrir rafrænt skýrslugerðarsnið:

    - Útgáfa 32.6.7 inniheldur sniðshlut og sniðsvörpunarhlut rafrænna skýrslugerðar sem voru skilgreindir til að búa til rafræna reikninga á PEPPOL-sniði.

    ![Útgáfa 32.6.7 á skilgreiningarsíðunni](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Nota breytingarnar í nýjum stöðluðum skilgreiningum rafrænnar skýrslugerðar í sérstilltum skilgreiningum rafrænnar skýrslugerðar

### <a name="adopt-your-custom-er-data-model"></a>Taka upp sérstillt gagnalíkan rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan** og velja **Reikningslíkan (Litware)**.
3. Í flýtiflipanum **Útgáfur**, fyrir útgáfudrög **50.2** af valdri skilgreiningu gagnalíkans skal velja **Endurreikna grunn**.
4. Í reitnum **Markútgáfa** skal staðfesta val á útgáfu **206** af grunnskilgreiningu gagnalíkans rafrænnar skýrslugerðar og velja síðan **Í lagi**.

    Drög að útgáfu af sérstilltri skilgreiningu á gagnalíkani rafrænnar skýrslugerðar er endurnúmeruð úr **50.2** í **206.2** til að gefa til kynna að nú innihaldi hún sérstillinguna þína sem var sameinuð við breytingarnar á síðustu útgáfunni (206) af grunnskilgreiningu á gagnalíkani rafrænnar skýrslugerðar.

    > [!NOTE]
    > Endurstillingaraðgerð grunns er afturkræf. Til að hætta við þessa endurstillingu grunns skal velja útgáfu **50.1** af líkaninu **Reikningslíkan (Litware)** í flýtiflipanum **Útgáfur** og velja síðan **Ná í þessa útgáfu**. Útgáfa 206.2 verður gerð að **50.2** og efni í útgáfudrögum 50.2 munu samsvara efninu í útgáfu 50.1.

5. Í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka** og síðan velja **Í lagi**.

Staða útgáfu 206.2 er breytt úr **Drög** í **Lokið** og útgáfa verður skrifvarin. Nýrri og breytanlegri útgáfu 206.3 hefur verið bætt við og er með stöðuna **Drög**. Hægt er að nota þessa útgáfu til að gera seinni tíma breytingar á sérstilltri skilgreiningu á gagnalíkani rafrænnar skýrslugerðar.

![Útgáfu 206.2 lokið á skilgreiningarsíðunni](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Taka upp sérstillta líkanavörpun rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan** \> **Vörpun reikningslíkans** og velja **Vörpun reikningslíkans (Litware)**.
3. Í flýtiflipanum **Útgáfur**, fyrir útgáfudrög **50.19.2** af valdri skilgreiningu líkanavörpunar skal velja **Endurreikna grunn**.
4. Í reitnum **Markútgáfa** skal staðfesta val á útgáfu **206.132** af grunnskilgreiningu líkanavörpunar rafrænnar skýrslugerðar og velja síðan **Í lagi**.

    Drög að útgáfu af sérstilltri skilgreiningu á líkanavörpun rafrænnar skýrslugerðar er endurnúmeruð úr **50.19.2** í **206.132.2** til að gefa til kynna að nú innihaldi hún sérstillinguna þína sem var sameinuð við breytingarnar á síðustu útgáfunni (206.132) af grunnskilgreiningu á líkanavörpun rafrænnar skýrslugerðar.

    Takið eftir að nokkrir árekstrar við endurstillingu komu í ljós. Nú þarf að leysa handvirkt úr þessum árekstrum.

    ![Skilaboð vegna áreksturs við endurstillingu á skilgreiningarsíðunni](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Á aðgerðasvæðinu skal velja **Hönnuður** og síðan í listanum yfir varpanir skal velja **Reikningur viðskiptavinar**.
6. Fyrir hvern árekstur endurstillingar skal velja **Halda eigin gildi** vegna þess að þú þarft að halda útgáfunúmerinu á sérstilltu gagnalíkani fyrir hvern hlut sem hefur verið minnst á.

    ![Árekstrar við endurreikning grunns á hönnunarsíðu líkanavörpunar](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Veljið **Vista** og lokið svo síðunni **Hönnuður líkanavörpunar**.
8. Í listanum yfir varpanir skal velja **Verkreikningur**.
9. Fyrir hvern árekstur endurstillingar skal velja **Halda eigin gildi** vegna þess að þú þarft að halda útgáfunúmerinu á sérstilltu gagnalíkani fyrir hvern hlut sem hefur verið minnst á.
10. Veljið **Vista** og lokið svo síðunni **Líkanavarpanir**.

    > [!NOTE]
    > Endurstillingaraðgerð grunns er afturkræf. Til að hætta við þessa endurstillingu grunns skal velja **50.19.1** af líkanavörpuninni **Vörpun reikningslíkans (Litware)** í flýtiflipanum **Útgáfur** og síðan velja **Ná í þessa útgáfu**. Útgáfa 206.132.2 verður síðan gefið aftur númerið **50.19.2** og efni útgáfudraga 50.19.2 mun samsvara efninu í útgáfu 50.19.1.

11. Í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka** og síðan velja **Í lagi**.

Staða útgáfu 206.132.2 er breytt úr **Drög** í **Lokið** og útgáfa verður skrifvarin. Nýrri og breytanlegri útgáfa 206.132.3 hefur verið bætt við og er með stöðuna **Drög**. Hægt er að nota þessa útgáfu til að gera seinni tíma breytingar á sérstilltri skilgreiningu á líkanavörpun rafrænnar skýrslugerðar.

![Útgáfu 206.132.2 lokið á skilgreiningarsíðunni](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Taka upp sérstillt snið rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan** \> **UBL-sölureikningur** \> **PEPPOL-sölureikningur** og velja **PEPPOL-sölureikningur (Litware)**.
3. Í flýtiflipanum **Útgáfur**, fyrir útgáfudrög **11.2.2.2** af valdri sniðsskilgreiningu skal velja **Endurreikna grunn**.
4. Í útgáfureitnum **Mark** skal staðfesta val á útgáfu **32.6.7** af grunnskilgreiningu á sniði rafrænnar skýrslugerðar og velja síðan **Í lagi**.

    Drög að útgáfu af sérstilltri skilgreiningu á sniði rafrænnar skýrslugerðar er endurnúmeruð úr **11.2.2.2** í **32.6.7.2** til að gefa til kynna að nú innihaldi hún sérstillinguna þína sem var sameinuð við breytingarnar á síðustu útgáfunni (32.6.7) af grunnskilgreiningu á sniði rafrænnar skýrslugerðar.

    Takið eftir að nokkrir árekstrar við endurstillingu komu í ljós. Nú þarf að leysa handvirkt úr þessum árekstrum.

5. Í aðgerðarúðunni skal velja **Hönnuður**.
6. Fyrir hvern árekstur endurstillingar skal velja **Halda eigin gildi** vegna þess að þú þarft að halda útgáfunúmerinu á sérstilltu gagnalíkani fyrir hvern hlut sem hefur verið minnst á.
7. Veljið **Vista**.
8. Í flipanum **Vörpun** skal velja gagnagjafann **Reikningur** af gerðinni **Líkan** og veljið síðan **Breyta**.
9. Í reitnum **Útgáfa** skal velja útgáfu **2** af sérstillta gagnalíkaninu og velja síðan **Í lagi**.
10. Veljið **Vista**.

    > [!NOTE]
    > Endurstillingaraðgerð grunns er afturkræf. Til að hætta við þessa endurstillingu grunns skal velja **11.2.2.1** fyrir sniðið **PEPPOL-sölureikningur (Litware)** í flýtiflipanum **Útgáfur** og velja síðan **Ná í þessa útgáfu**. Útgáfa 32.6.7.2 verður síðan gefið aftur númerið **11.2.2.2** og efni útgáfudraga 11.2.2.2 mun samsvara efninu í útgáfu 11.2.2.1.

11. Lokaðu síðunni **Sniðshönnuður**.
12. Í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka** og síðan velja **Í lagi**.

Staða útgáfu 32.6.7.2 er breytt úr **Drög** í **Lokið** og útgáfa verður skrifvarin. Nýrri og breytanlegri útgáfa 32.6.7.3 hefur verið bætt við og er með stöðuna **Drög**. Hægt er að nota þessa útgáfu til að gera seinni tíma breytingar á sérstilltri skilgreiningu á sniði rafrænnar skýrslugerðar.

![Útgáfu 32.6.7.2 lokið á skilgreiningarsíðunni](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Vinna úr reikningi viðskiptavinar með því að nota nýjar útgáfur af sérstilltum skilgreiningum rafrænnar skýrslugerðar

### <a name="select-and-send-a-posted-invoice"></a>Velja og senda bókaðan reikning

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Á síðunni **Reikningur með frjálsum texta** skal velja reikninginn sem var bætt við og bókaður hér á undan.
3. Á aðgerðasvæðinu, í flokknum **Skjal**, skal velja **Senda** \> **Upprunalegt**.

    > [!NOTE] 
    > Þar sem þú ert nú með tvær útgáfur af skilgreiningu rafræns skýrslugerðarsniðs **Peppol-sölureikningi (Litware)** og hvorug útgáfan er með [gildisdagsetningu](general-electronic-reporting.md#component-date-effectivity), er nýjasta útgáfan notuð til að mynda rafrænan reikning.

4. Lokið síðunni **Reikningur með frjálsum texta**.

### <a name="analyze-a-generated-e-invoice"></a>Skoða myndaðan rafrænan reikning

1. Farið í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Rafræn skýrslugerðarvinnsla**.
2. Á síðunni **Rafræn skýrslugerðarvinnsla** skal velja nýlegustu færsluna sem er með verklýsinguna **Senda XML rafræns reiknings**.
3. Veljið **Sýna skrár** til að sjá lista yfir myndaðar skrár.
4. Veljið **Opna** til að hlaða niður XML-skrá rafræns reiknings sem er búinn til.
5. Greina XML-skrá rafræns reiknings. Takið eftir því að samkvæmt sérstillingum inniheldur skattskema viðskiptavinar ennþá sérstillta **FederalTaxID** XML-eigind til viðbótar við **schemeID** og **schemeAgencyID** XML-eigindir. Þar að auki, vegna þess að breytingarnar í nýju útgáfunni af grunnsniðinu **UBL-sölureikningur** voru sameinaðar við sérstillingarnar þínar, hefur textinn fyrir **cbc:CustomizationID** XML-eininguna verið breytt úr `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` í `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Forskoða myndaða XML-skrá rafræns reiknings með sérstillingum](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Sækja skilgreiningar rafrænnar skýrslugerðar úr Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](er-download-configurations-global-repo.md)
- [Stofna textareikning](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Stofna og vinna með sérstillt svæði](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]