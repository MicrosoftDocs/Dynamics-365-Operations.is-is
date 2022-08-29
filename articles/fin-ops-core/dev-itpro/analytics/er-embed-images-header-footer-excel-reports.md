---
title: Hanna snið rafrænnar skýrslugerðar til að búa til skýrslu á Excel-sniði með myndum sem eru felldar inn í síðuhausa eða -fætur
description: Þessi grein útskýrir hvernig á að nota rafræna skýrslugerð (ER) til að búa til viðskiptaskjöl sem hafa myndir og form innbyggðar í síðuhausa eða -fætur.
author: kfend
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.custom: ''
ms.assetid: ''
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 5b46d92094bb3f2dab67a5cb2f0e1a34b05d52f0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281813"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>Hanna snið rafrænnar skýrslugerðar til að búa til skýrslu á Excel-sniði með myndum sem eru felldar inn í síðuhausa eða -fætur

[!include[banner](../includes/banner.md)]

Þessi grein útskýrir hvernig notandi í hlutverki kerfisstjóra eða rafrænnar skýrslugerðar ráðgjafa getur framkvæmt þessi verkefni:

- Skilgreinið færibreytur fyrir ramma [Rafrænnar skýrslugerðar](general-electronic-reporting.md).
- Flytja inn [skilgreiningar](general-electronic-reporting.md#Configuration) ER sem Microsoft [býður upp á](general-electronic-reporting.md#Provider) og eru notaðar til að búa til [reikninga með frjálsum texta](../../../finance/accounts-receivable/create-free-text-invoice-new.md) samkvæmt [sniðmáti](er-fillable-excel.md#excel-file-component) á Microsoft Excel sniði.
- Búið til [sérsniðna (afleidda)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) útgáfu af staðlaðri skilgreiningu rafræns skýrslugerðarsniðs sem Microsoft býður upp á.
- Breytið sérstilltri skilgreiningu ER-sniðs þannig að hún myndi skýrslu um reikning með frjálsum texta sem er með mynd af fyrirtækislógói í síðufætinum.

Verklagsreglurnar í þessari grein er hægt að ljúka í **USMF** fyrirtæki. Ekki er þörf á neinni kóðun. Áður en hafist er handa skal sækja og vista eftirfarandi skrá.

| lýsing        | Skrárnafn |
|--------------------|-----------|
| Mynd af merki fyrirtækis | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Efni

- [Skilgreina lögaðila](#ConfigureLegalEntity)
- [Skilgreina ramma rafrænnar skýrslugerðar](#ConfigureFramework)

    - [Skilgreina færibreytur Rafræn skýrslugerðar](#ConfigureParameters)
    - [Virkja skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider)

        - [Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar](#ReviewProvidersList)
        - [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#AddProvider)
        - [Virkja nýja skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateAddedProvider)

- [Flytja inn staðlaðar skilgreiningar rafræns skýrslugerðarsniðs](#ImportERSolution1)

    - [Flytja inn staðlaðar skilgreiningar rafrænnar skýrslugerðar](#ImportERFormat)
    - [Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar](#ReviewImportedERSolution)

- [Prenta reikning með frjálsum texta með stöðluðu sniði rafrænnar skýrslugerðar](#PrintInvoice1)

    - [Setja upp prentstýringu](#ConfigurePrintManagement1)
    - [Prenta textareikning](#ProcessInvoice1)

- [Sérsníða staðlað snið rafrænnar skýrslugerðar](#CustomizeProvidedFormat)

    - [Búa til sérsniðið snið](#DeriveProvidedFormat)
    - [Breyta sérstilltu sniði](#ConfigureDerivedFormat)
    - [Merkja sérstillt snið sem keyranlegt](#MarkFormatRunnable)

- [Prenta textareikning með því að nota sérstillt snið rafrænnar skýrslugerðar](#PrintInvoice2)

    - [Setja upp prentstýringu](#ConfigurePrintManagement2)
    - [Prenta textareikning](#ProcessInvoice2)

- [Frekari upplýsingar](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>Skilgreina lögaðila

1. Fara í **Fyrirtækisstjórnun** \> **Fyrirtæki** \> **Lögaðilar**.
2. Á síðunni **Lögaðilar**, í flýtiflipanum **Tilkynna um mynd fyrirtækjalógós**, skal velja **Breyta**.
3. Í svarglugganum **Velja myndskrá til að hlaða upp** skal velja **Fletta** og velja skrána **Company logo.png** sem þú sóttir áðan.
4. Veldu **Vista** og lokaðu síðan síðunni **Lögaðilar**.

![Mynd af merki fyrirtækis valið á síðu lögaðila.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Sem notandi í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar þarf að skilgreina lágmarksstillingu á færibreytum rafrænnar skýrslugerðar áður en byrjað er að nota ramma rafrænnar skýrslugerðar til að hanna sérsniðna útgáfu á stöðluðu snið rafrænnar skýrslugerðar.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Skilgreina færibreytur Rafræn skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Færibreytur rafrænnar skýrslugerðar**.
3. Á síðunni **Færibreytur rafrænnar skýrslugerðar**, í flipanum **Almennt**, skal stilla valkostinn **Kveikja á hönnunarstillingu** á **Já**.
4. Í flipanum **Viðhengi** skal stilla eftirfarandi færibreytur:

    - Í reitnum **Skilgreiningar** skal velja gerðina **Skrá** fyrir **USMF** fyrirtækið.
    - Í reitunum **Verksafn**, **Tímabundið**, **Grunnlína** og **Annað** skal velja gerð fyrir **Skrá**.

Frekari upplýsingar um færibreytur rafrænnar skýrslugerðar er að finna í [Skilgreina ramma rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Virkja skilgreiningarveitu rafrænnar skýrslugerðar

Allar skilgreiningar rafrænnar skýrslugerðar sem bætt er við eru merktar sem eign skilgreingarveitu rafrænnar skýrslugerðar. Skilgreiningarveita rafrænnar skýrslugerðar sem er virkjuð á vinnusvæðinu **Rafræn skýrslugerð** er notuð í þessum tilgangi. Þess vegna þarf að virkja skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð** áður en byrjað er að bæta við eða breyta skilgreiningum rafrænnar skýrslugerðar.

> [!NOTE]
> Einungis eigandi skilgreiningarinnar má breyta ER-skilgreiningu. Áður en hægt er að breyta skilgreiningu rafrænnar skýrslugerðar verður að virkja viðeigandi skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Tafla yfir skilgreiningarveitur** er hver færsla með einkvæmt heiti og vefslóð. Farið yfir efnið á þessari síðu. Ef færsla fyrir **Litware, Inc.** (`https://www.litware.com`) er þegar til skal sleppa næsta ferli, [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Skilgreiningarveitur** skal velja **Ný**.
4. Í reitinn **Heiti** skal færa inn **Litware, Inc.**
5. Í reitinn **Veffang** skal færa inn `https://www.litware.com`.
6. Veldu **Vista**.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Virkja nýja skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Litware, Inc.** og síðan velja **Stilla sem virkt**.

Nánari upplýsingar um skilgreiningarveitur rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Flytja inn staðlaðar skilgreiningar rafræns skýrslugerðarsniðs

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>Flytja inn staðlaðar skilgreiningar rafrænnar skýrslugerðar

Til að bæta stöðluðum ER stillingum við núverandi tilvik þitt af Dynamics 365 Finance, verður þú að flytja þær inn úr ER [geymsla](general-electronic-reporting.md#Repository) sem var stillt fyrir það tilvik.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Microsoft** og síðan velja **Gagnageymslur** til að skoða lista yfir gagnageymslur fyrir **Microsoft** veituna.
3. Á síðunni **Skilgreiningageymslur** skal velja gagnageymslu af gerðinni **Altæk** og síðan velja **Opna**. Ef beðið er um heimild til að tengjast við [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md), skal fylgja leiðbeiningum um heimild.
4. Á síðunni **Skilgreiningageymsla**, í skilgreiningatrénu vinstra megin á svæðinu, skal velja skilgreiningarsniðið **Reikningur með frjálsum texta (Excel)**.
5. Í flýtiflipanum **Útgáfur** skal velja nýjustu útgáfuna (til dæmis **240.112**) af valdri skilgreiningu rafræns skýrslugerðarsniðs.
6. Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu í núverandi fjármálatilvik.

![Innflutningur á stöðluðum ER-skilgreiningum á síðu skilgreiningageymsla.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Ef það reynist erfitt að opna [Altæka geymsla](er-download-configurations-global-repo.md) er hægt að [sækja skilgreiningar](download-electronic-reporting-configuration-lcs.md) hjá Microsoft Dynamics Lifecycle Services (LCS) í staðinn.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan**.
4. Til viðbótar við valið ER-snið **Reiknings með frjálsum texta (Excel)** voru aðrar áskildar skilgreiningar rafrænnar skýrslugerðar fluttar inn. Gangið úr skugga um að eftirfarandi skilgreiningar rafrænnar skýrslugerðar séu í boði í skilgreiningartrénu:

    - **Reikningslíkan** – Þessi uppsetning inniheldur gagnalíkanið ER hluti sem táknar gagnaskipulag reikningsviðskiptaléns.
    - **Kortlagning reikningslíkana** – Þessi uppsetning inniheldur líkanakortlagningu ER íhlutinn sem lýsir því hvernig gagnalíkanið er fyllt út með forritsgögnum á keyrslutíma.
    - **Ókeypis textareikningur (Excel)** – Þessi uppsetning inniheldur snið- og sniðkortlagningu ER hluti. Sniðshlutinn tilgreinir útlit skýrslunnar út frá sniðmáti á Excel-sniði. Sniðsvörpunarhlutinn inniheldur gagnagjafa líkansins og tilgreinir hvernig þessi gagnagjafi er notaður til að fylla út skýrsluútlitið á keyrslutíma.

![Innfluttar ER grunnstillingar á skilgreiningasíðunni.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Prenta textareikning með því að nota staðlað snið rafrænnar skýrslugerðar

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Setja upp prentstýringu

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Á síðunni **Reikningur með frjálsum texta** skal velja reikninginn **FTI-00000002** og síðan á aðgerðasvæðinu, í flipanum **Reikningur**, í hópnum **Prentstýring**, skal velja **Prentstýring**.
3. Á síðunni **Uppsetning á prentstýringu**, í trénu vinstra megin, skal útvíkka **Eining - Viðskiptakröfur \> Skjöl \> Reikningur með frjálsum texta** og síðan velja atriðið **Upprunalegt \<Default\>**.
4. Í reitnum **Skýrslusnið** skal velja **Reikningur með frjálsum texta (Excel)**.
5. Veldu **Esc** til að fara af síðunni **Uppsetning á prentstýringu** og aftur á síðuna **Reikningur með frjálsum texta**.

![Stillingar prentstýringar fyrir reikning með frjálsum texta á stöðluðu sniði rafrænnar skýrslugerðar á uppsetningarsíðu prentstýringar.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Prenta textareikning

1. Á síðunni **Reikningur með frjálsum texta** skal ganga úr skugga um að reikningurinn **FTI-00000002** sé enn valinn og síðan á aðgerðasvæðinu, í flipanum **Reikningur**, í hópnum **Skjal**, skal velja **Prenta** \> **Valið**.
2. Sæktu myndaðan reikning á Excel-sniði og opnaðu hann til forskoðunar.
3. Athugaðu að í samræmi við uppbyggingu Excel sniðmátsins fyrir uppgefið ER-snið inniheldur síðufótur reikningsins upplýsingar um núverandi blaðsíðunúmer og heildarfjölda blaðsíðna í skýrslunni.

![Myndaður textareikningur.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Sérsníða staðlað snið rafrænnar skýrslugerðar

Í þessum hluta er til dæmis hægt að nota ER-stillingarnar sem Microsoft útvegar til að búa til textareikning á Excel-sniði. Hins vegar verður að bæta við sérstillingu til að setja merki fyrirtækis eða mynd í síðufótinn á útbúnum reikningi.

Í þessu tilfelli, sem fulltrúi Litware, Inc., þarf að búa til (afleiða) nýja skilgreiningu rafrænnar skýrslugerðar sem byggir á skilgreining **Textareiknings** sem Microsoft býður upp.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Búa til sérsniðið snið

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan** og síðan velja **Reikningur með frjálsum texta (Excel)**. Litware, Inc. notar innflutta útgáfu (til dæmis **240.112**) af þessari skilgreiningu á sniði rafrænnar skýrslugerðar sem grunn fyrir sérsniðnu útgáfuna.
3. Veljið **Stofna skilgreiningu** til að opna fellilistagluggann. Notaðu þennan glugga til að stofna nýja skilgreiningu fyrir sérstillt greiðslusnið.
4. Í reitahópnum **Ný** skal velja valkostinn **Leiða af heiti: Reikningur með frjálsum texta (Excel), Microsoft**.
5. Í reitinn **Heiti** skal færa inn **Sérstilltur reikningur með frjálsum texta (Excel)**.
6. Veljið **Stofna skilgreiningu**.

![Skilgreining stofnuð fyrir sérstillt greiðslusnið í fellilista svargluggans Stofna skilgreiningu.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Útgáfa 240.112.1 af skilgreiningu **Reiknings með frjálsum texta (Excel)** fyrir ER-snið er stofnuð. Þessi útgáfa hefur stöðuna **Drög** og er hægt að breyta. Núverandi efni af sérstilltu sniði rafrænnar skýrslugerðar samsvarar efni sniðsins sem Microsoft býður upp á.

![Ný útgáfa af skilgreiningu ER-sniðs stofnuð á skilgreiningasíðunni.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>Breyta sérstilltu sniði

Skilgreina sérstillt snið þannig að mynd af merki fyrirtækis sé sett í síðufótinn á öllum síðum skýrslunnar.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan** og velja síðan **Sérstilltur reikningur með frjálsum texta (Excel)**.
3. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **240.112.1** af valdri skilgreiningu.
4. Veljið **Hönnuður**.
5. Á síðunni **Sniðshönnuður** skal velja **Sýna upplýsingar** til að skoða frekari upplýsingar um sniðseiningarnar.
6. Stækkið og yfirfarið eftirfarandi einingar:

    - Einingin **Textareikningar** af gerðinni **Excel**. Þessi eining er notuð til að búa til reikning á sniði Excel-vinnubókar.
    - Einingin **Reikningur með frjálsum texta \\ Reikningur** af gerðinni **Vinnublað**. Þessi eining er notuð til að mynda vinnublað fyrir myndaða Excel-vinnubók.
    - Einingin **Reikningur með frjálsum texta \\ Reikningur \\ Síðufótur** af gerðinni **Síðufótur**. Þessi eining er notuð til að fylla út síðufót reiknings.

7. Veldu eininguna **Reikningur með frjálsum texta \\ Reikningur \\ Síðufótur**.

    ![Eining síðufótar í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Allir síðufætur í mynduðum reikningi inniheldur upplýsingar um núverandi blaðsíðunúmer og heildarfjölda blaðsíðna í skýrslunni. Eins og þú sérð inniheldur einingin **Reikningur með frjálsum texta \\ Reikningur \\ Síðufótur** engar undireiningar. Þar af leiðandi er Excel-sniðmátið sem er notað skilgreint til að sýna upplýsingar um blaðsíðutal fyrir miðju á öllum síðufótum skýrslunnar.

8. Veljið **Bæta við** og síðan gerðina **Excel \\ Mynd** fyrir sniðseininguna sem verið er að bæta við:

    1. Í reitnum **Stilling** skal velja **Hægrijafnað**.
    2. Í reitnum **Skala hæð** skal velja **Hlutfallslegt**.
    3. Í reitinn **Skala í prósentu** skal færa inn **70**.
    4. Veldu **Í lagi**.

        > [!NOTE]
        > Einingin **Excel \\ Mynd** er notuð til að bæta við mynd af merki fyrirtækis og hægrijafna það í síðufætinum.

    ![Eiginleikar myndeinarinnar í svarglugga fyrir eiginleikahlutinn.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Í tré sniðsskipulags til vinstri skal velja eininguna **Mynd** sem var bætt við og síðan í flipanum **Vörpun** skal stækka gagnagjafann **líkan**.
10. Stækkaðu **model.Payment** \> **model.InvoiceBase \> model.InvoiceBase.CompanyInfo** og veldu síðan gagnagjafareitinn **model.InvoiceBase.CompanyInfo.Logo**. Gagnagjafareiturinn af gerðinni [Geymsla](er-formula-supported-data-types-composite.md#container) sýnir mynd af merki fyrirtækisins sem margmiðlunarefni.
11. Veldu **Binda**. Sniðseiningin **Mynd** er nú bundin við gagnagjafareitinn **model.InvoiceBase.CompanyInfo.Logo**. Því verður mynd af merki fyrirtækis við keyrslu sett í síðufót myndaðra reikninga.

    ![Sniðseining myndar bundin við gagnagjafareitinn model.InvoiceBase.CompanyInfo.Logo í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Veljið **Vista** og lokið svo síðunni **Hönnuður**.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Merkja sérstillt snið sem keyranlegt

Þar sem fyrsta útgáfa af sérstilltu sniði hefur verið stofnuð og er með stöðuna **Drög** er hægt að prufukeyra sniðið. Til að keyra skýrsluna skal vinna úr greiðslu lánardrottins með því að nota greiðslumátann sem vísar til sérstillts sniðs rafrænnar skýrslugerðar. Sjálfgefið er, þegar þú hringir í ER snið úr forritinu, aðeins útgáfur sem hafa stöðuna **Lokið** eða **Deilt** koma til greina. Þessi leið hjálpar til við að koma í veg fyrir að snið rafrænnar skýrslugerðar með ókláraðri hönnun verði notuð. Fyrir prufukeyrslur er hinsvegar hægt að þvinga forritið til að nota sniðsútgáfu rafrænnar skýrslugerðar sem er með stöðuna **Drög**. Á þennan hátt er hægt að leiðrétta núverandi sniðsútgáfu ef gera þarf einhverjar breytingar. Frekari upplýsingar er að finna í [Nothæfni](electronic-reporting-destinations.md#applicability).

Til að nota útgáfudrög af sniði rafrænnar skýrslugerðar þarf sérstaklega að merkja rafræna skýrslugerðarsniðið.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Í glugganum **Færibreytur notanda** skal stilla valkostinn **Keyra stillingar** á **Já** og síðan velja **Í lagi**.
4. Veldu **Breyta** til að gera núverandi síðu breytanlega og síðan í skilgreiningatrénu í glugganum vinstra megin skal velja **Reikningur með frjálsum texta (Excel)**.
5. Stillið valkostinn **Keyra drög** á **Já**.

![Merking sérstillta sniðsins sem keyranlegt á skilgreiningarsíðunni.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Prenta textareikning með því að nota snið rafrænnar skýrslugerðar

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Setja upp prentstýringu

1. Fara í **Viðskiptakröfur** \> **Reikningar** \> **Allir reikningar með frjálsum texta**.
2. Á síðunni **Reikningur með frjálsum texta** skal velja reikninginn **FTI-00000002** og síðan á aðgerðasvæðinu, í flipanum **Reikningur**, í hópnum **Prentstýring**, skal velja **Prentstýring**.
3. Á síðunni **Uppsetning á prentstýringu**, í trénu vinstra megin, skal útvíkka **Eining - Viðskiptakröfur** \> **Skjöl** \> **Reikningur með frjálsum texta** og síðan velja atriðið **Upprunalegt** **\<Default\>**.
4. Í reitnum **Skýrslusnið** skal velja **Sérsniðinn reikningur með frjálsum texta (Excel)**.
5. Veldu **Esc** til að fara af síðunni **Uppsetning á prentstýringu** og aftur á síðuna **Reikningur með frjálsum texta**.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Prenta textareikning

1. Á síðunni **Reikningur með frjálsum texta** skal ganga úr skugga um að reikningurinn **FTI-00000002** sé enn valinn og síðan á aðgerðasvæðinu, í flipanum **Reikningur**, í hópnum **Skjal**, skal velja **Prenta** \> **Valið**.
2. Sæktu myndaðan reikning á Excel-sniði og opnaðu hann til forskoðunar.
3. Taktu eftir að í samræmi við skipulag á sérsniðinni rafrænni skýrslugerð inniheldur síðufótur myndaðs skjals mynd af merki fyrirtækisins ásamt upplýsingum um blaðsíðutal skýrslunnar.

![Reikningur með frjálsum texta myndaður með mynd af merki fyrirtækis í síðufætinum.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Frekari upplýsingar

- [Hanna skilgreiningu fyrir myndun skjala á Excel-sniði](er-fillable-excel.md)
- [Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md)
