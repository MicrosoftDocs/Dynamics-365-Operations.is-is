---
title: Breyta sniði rafrænnar skýrslugerðar til að mynda sérsniðið rafrænt skjal
description: Í þessari grein er útskýrt hvernig á að breyta rafrænu skýrslugerðarsniði frá Microsoft svo það búi til sérsniðið rafrænt skjal.
author: kfend
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.custom: 220314,  ""intro-internal
ms.assetid: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
ms.openlocfilehash: 8b0bcdbd011c4c04e2693a3dcb8033c3cbe2adc7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283559"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a>Breyta sniði rafrænnar skýrslugerðar til að mynda sérsniðið rafrænt skjal

[!include[banner](../includes/banner.md)]

Aðferðirnar í þessari grein útskýra hvernig notandi í hlutverki kerfisstjóra eða í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar getur framkvæmt þessi verk:

- Skilgreinið færibreytur fyrir [Ramma rafrænnar skýrslugerðar](general-electronic-reporting.md).
- Flytjið inn skilgreiningar rafrænnar skýrslugerðar sem Microsoft veitir og eru notaðar til að búa til greiðsluskrár á meðan [greiðsla lánardrottins](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) er í vinnslu.
- Búið til sérsniðna útgáfu af staðlaðri skilgreiningu rafræns skýrslugerðarsniðs sem Microsoft býður upp á.
- Breytið sérsniðinni skilgreiningu rafrænnar skýrslugerðar þannig að hún búi til greiðsluskrár sem uppfylla kröfur tiltekins banka.
- Innleiðið breytingar sem gerðar eru á staðlaðri skilgreiningu rafræns skýrslugerðarsniðs í sérsniðinni skilgreiningu rafræns skýrslugerðarsniðs.

Öll eftirfarandi ferli er hægt að vinna í **GBSI** fyrirtækinu. Ekki er þörf á neinni kóðun.

- [Skilgreina ramma rafrænnar skýrslugerðar](#ConfigureFramework)

    - [Skilgreina færibreytur Rafræn skýrslugerðar](#ConfigureParameters)
    - [Virkja skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider)

        - [Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar](#ReviewProvidersList)
        - [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider)
        - [Virkja skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateAddedProvider)

- [Flytja inn staðlaðar skilgreiningar rafræns skýrslugerðarsniðs](#ImportERSolution1)

    - [Flytja inn staðlaðar skilgreiningar rafrænnar skýrslugerðar](#ImportERFormat1)
    - [Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar](#ReviewImportedERSolution)

- [Undirbúa greiðslu lánardrottins fyrir úrvinnslu](#PrepareVendorPayment)

    - [Bæta við bankaupplýsingum fyrir lánardrottnalykil](#AddBankAccount)
    - [Færa inn greiðslu lánardrottins](#EnterVendorPayment)

- [Vinna úr lánardrottnagreiðslu með því að nota staðlað snið rafrænnar skýrslugerðar](#ProcessVendorPayment1)

    - [Setja upp rafrænan greiðslumáta](#ConfigureMethodOfPayment1)
    - [Vinna úr lánardrottnagreiðslu](#ProcessPayment1)

- [Sérsníða staðlað snið rafrænnar skýrslugerðar](#CustomizeProvidedFormat)

    - [Búa til sérsniðið snið](#DeriveProvidedFormat)
    - [Breyta sérsniðnu sniði](#ConfigureDerivedFormat)
    - [Merkja sérsniðið snið sem keyrsluhæft](#MarkFormatRunnable)

- [Vinna úr greiðslu lánardrottins með því að nota sérsniðið snið rafrænnar skýrslugerðar](#ProcessVendorPayment2)

    - [Setja upp rafrænan greiðslumáta](#ConfigureMethodOfPayment2)
    - [Vinna úr lánardrottnagreiðslu](#ProcessPayment2)

- [Flytja inn nýjar útgáfur af stöðluðum skilgreiningum rafræns skýrslugerðarsniðs](#ImportERSolution2)

    - [Flytja inn nýjar útgáfur af stöðluðum skilgreiningum rafrænnar skýrslugerðar](#ImportERFormat2)
    - [Fara yfir innfluttar skilgreiningar rafræns skýrslugerðarsniðs](#ReviewImportedERFormat)

- [Innleiða breytingarnar í nýju útgáfu innflutts sniðs í sérsniðnu sniði](#AdoptNewBaseVersion)

    - [Ljúkið við núgildandi drög að útgáfu sérsniðins sniðs](#CompleteDerivedFormat)
    - [Endurstilla grunn sérsniðins sniðs á nýja grunnútgáfu](#RebaseDerivedFormat)
    - [Vinna úr greiðslu lánardrottins með því að nota endurstilltan grunn rafræns skýrslugerðarsniðs](#ProcessPayment3)

- [Frekari upplýsingar](#References)

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
> Aðeins eigandi skilgreiningar rafrænnar skýrslugerðar getur breytt henni. Þess vegna, áður en hægt er að breyta skilgreiningu rafrænnar skýrslugerðar, verður að virkja viðeigandi skilgreiningarveitu rafrænnar skýrslugerðar á vinnusvæðinu **Rafræn skýrslugerð**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Fara yfir lista yfir skilgreiningarveitur rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Tafla yfir skilgreiningarveitur** er hver færsla með einkvæmt heiti og vefslóð. Farið yfir efnið á þessari síðu. Ef færsla fyrir **Litware, Inc.** (`https://www.litware.com`) er þegar til skal sleppa næsta ferli, [Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Bæta við nýrri skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Skilgreiningarveitur**.
3. Á síðunni **Skilgreiningarveitur** skal velja **Ný**.
4. Í reitinn **Heiti** skal færa inn **Litware, Inc.**
5. Í reitinn **Veffang** skal færa inn `https://www.litware.com`.
6. Veljið **Vista**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Virkja skilgreiningarveitu rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Litware, Inc.** og síðan velja **Stilla sem virkt**.

Nánari upplýsingar um skilgreiningarveitur rafrænnar skýrslugerðar er að finna í [Stofna skilgreiningarveitur og merkja þær sem virkar](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>Flytja inn staðlaðar skilgreiningar rafræns skýrslugerðarsniðs

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a>Flytja inn staðlaðar skilgreiningar rafrænnar skýrslugerðar

Til að bæta stöðluðum skilgreiningum rafrænnar skýrslugerðar við núverandi tilvik af Microsoft Dynamics 365 Finance þarf að flytja þær inn úr [gagnageymslu ](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar sem var skilgreind fyrir það tilvik.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Microsoft** og síðan velja **Gagnageymslur** til að skoða lista yfir gagnageymslur fyrir Microsoft-veituna.
3. Á síðunni **Skilgreiningageymslur** skal velja gagnageymslu af gerðinni **Altæk** og síðan velja **Opna**. Ef beðið er um heimild til að tengjast við Regulatory Configuration Service, skal fylgja leiðbeiningum um heimild.
4. Á síðunni **Skilgreiningageymsla**, í skilgreiningatrénu vinstra megin á svæðinu, skal velja skilgreiningarsniðið **BACS (Bretland)**.
5. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1** af valdri skilgreiningu rafræns skýrslugerðarsniðs.
6. Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu í núverandi fjármálatilvik.

![Gagnageymslusíða skilgreininga.](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> Ef það reynist erfitt að opna [Altæka geymsla](er-download-configurations-global-repo.md) er hægt að [sækja skilgreiningar](download-electronic-reporting-configuration-lcs.md) hjá Microsoft Dynamics Lifecycle Services (LCS) í staðinn.

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan**.
4. Takið eftir að til viðbótar við valið **BACS (Bretland)** snið rafrænnar skýrslugerðar, voru aðrar áskildar skilgreiningar rafrænnar skýrslugerðar fluttar inn. Gangið úr skugga um að eftirfarandi skilgreiningar rafrænnar skýrslugerðar séu í boði í skilgreiningartrénu:

    - **Greiðslulíkan** – Þessi skilgreining inniheldur hlutann gagnalíkan í rafrænni skýrslugerð sem táknar gagnaskipulag fyrir viðskiptalén greiðslna.
    - **Vörpun greiðslulíkans 1611** – Þessi skilgreining inniheldur hlutann líkanavörpun fyrir rafræna skýrslugerð sem lýsir því hvernig gagnalíkanið er fyllt út með forritsgögnum við keyrslu.
    - **BACS (UK)** – Þessi skilgreining inniheldur hlutann snið og sniðsvörpun í rafrænni skýrslugerð. Sniðshlutinn tilgreinir útlit skýrslunnar. Sniðsvörpunarhlutinn inniheldur gagnagjafa líkansins og tilgreinir hvernig fyllt er út í skýrsluútlitið með því að nota þennan gagnagjafa við keyrslu.

![Skilgreiningasíða með skilgreindum skilgreiningum rafrænnar skýrslugerðar í trénu.](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a>Undirbúa greiðslu lánardrottins fyrir úrvinnslu

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a>Bæta við bankaupplýsingum fyrir lánardrottnalykil

Bæta þarf við bankaupplýsingum fyrir lánardrottnalykil sem vísað verður til síðar í skráðri greiðslu.

1. Farið í **Viðskiptaskuldir** \> **Lánardrottnar** \> **Allir lánardrottnar**.
2. Á síðunni **Allir lánardrottnar** skal velja lánardrottnalykilinn **GB_SI_000001** og síðan, á aðgerðasvæðinu, í flipanum **Lánardrottinn**, í flokknum **Uppsetning**, skal velja **Bankareikningar**.
3. Á síðunni **Bankareikningar lánardrottins** skal smella á **Nýr** og færa síðan inn eftirfarandi upplýsingar:

    1. Í reitinn **Bankareikningur** skal færa inn **GBP OPER**.
    2. Í reitnum **Bankaflokkar** skal velja **BankGBP**.
    3. Í reitinn **Bankareikningsnúmer** skal færa inn **202015**.
    4. Í reitinn **SWIFT-kóði** skal færa inn <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.
    5. Í reitinn **IBAN** skal færa inn **GB33BUKB20201555555555**.
    6. Í reitnum **Leiðarnúmer** skal halda sjálfgefna gildinu <a id="DefineRoutingNumber"></a>**123456**.

    ![Síða fyrir bankareikninga lánardrottna.](./media/er-quick-start2-bank-account.png)

4. Veldu **Vista**.
5. Lokið síðunni.
6. Á síðunni **Allir lánardrottnar** skal opna lánardrottnalykilinn **GB_SI_000001**.
7. Á upplýsingasíðu lánardrottins skal velja **Breyta** til að gera síðuna breytanleg ef á þarf að halda.
8. Í flýtiflipanum **Greiðsla**, í reitnum **Bankareikningur**, skal velja **GBP OPER**.

    ![Upplýsingasíða lánardrottins.](./media/er-quick-start2-bank-account-reference.png)

9. Veldu **Vista**.
10. Lokið síðunni.

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a>Færa inn greiðslu lánardrottins

Færa verður inn nýja lánardrottnagreiðslu með því að nota [greiðslutillaga](../../../finance/accounts-payable/create-vendor-payments-payment-proposal.md).

1. Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.
2. Á síðunni **Greiðslubók lánardrottins** skal velja **Ný**.
3. Í reitinn **Heiti** skal velja **VendPay**.
4. Veldu **Línur**.
5. Veljið **Greiðslutillaga** \> **Stofna greiðslutillögu**.
6. Í svarglugganum **Greiðslutillaga lánardrottins** skal stilla skilyrði til að afmarka færslur niður í eingöngu lánardrottnalykilinn **GB_SI_000001** og velja síðan **Í lagi**.
7. Veljið línuna fyrir reikninginn **00000007_Inv** og veljið síðan **Stofna greiðslu**.

    ![Svargluggi greiðslutillögu lánardrottins.](./media/er-quick-start2-payment-proposal.png)

8. Gangið úr skugga um að greiðslan sem slegin er inn sé skilgreind til að nota **Rafrænan** greiðslumáta.

    ![Síða lánardrottnagreiðslna.](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a>Vinna úr lánardrottnagreiðslu með því að nota staðlað snið rafrænnar skýrslugerðar

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a>Setja upp rafrænan greiðslumáta

Skilgreina þarf rafrænan greiðslumáta þannig að hann noti innflutta skilgreiningu fyrir snið rafrænnar skýrslugerðar.

1. Farið í **Viðskiptaskuldir** \> **Greiðsluuppsetning** \> **Greiðsluháttur**.
2. Á síðunni **Greiðslumátar - lánardrottnar** skal velja greiðslumátann **Rafrænt** vinstra megin á svæðinu.
3. Veljið **Breyta**.
4. Í flýtiflipanum **Skráarsnið** skal stilla valkostinn **Almennt rafrænt útflutningssnið** á **Já**.
5. Í reitnum **Skilgreining útflutningssniðs** skal velja skilgreiningarsniðið **BACS (Bretland)**.

    ![Greiðslumátar - síða lánardrottins til að setja upp rafrænan greiðslumáta til að vinna greiðslur frá lánardrottnum með hefðbundnu sniði.](./media/er-quick-start2-method-of-payment1.png)

6. Veldu **Vista**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a>Vinna úr lánardrottnagreiðslu

1. Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.
2. Á síðunni **Greiðslubók lánardrottins** skal velja þá greiðslubók sem var áður bætt við og síðan velja **Línur**.
3. Á síðunni **Greiðslur lánardrottna** skal velja **Búa til greiðslur**.
4. Í svarglugganum **Búa til greiðslur** skal færa inn eftirfarandi upplýsingar:

    - Í reitnum **Greiðslumáti** skal velja **Rafrænn**.
    - Í reitnum **Bankareikningur** skal velja **GBSI OPER**.

5. Veljið **Í lagi**.
6. Í svarglugganum **Rafrænar skýrslufæribreytur** skal stilla valkostinn **Prenta eftirlitsskýrslu** á **Já** og velja síðan **Í lagi**.

    ![Síða rafrænna skýrslufæribreyta.](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > Auk greiðsluskrárinnar er nú hægt að búa til eftirlitsskýrsluna.

7. Sækið zip-skrána og dragið síðan eftirfarandi skrár út úr henni:

    - Eftirlitsskýrslan á Excel-sniði
    - Greiðsluskráin á TXT-sniði

        Takið eftir því, að í samræmi við [skipulag](#PositionRoutingNumber) á uppgefnu sniði rafrænnar skýrslugerðar, hefst greiðslulínan í útbúinni skrá á leiðarnúmerinu sem var [skilgreint](#DefineRoutingNumber) fyrir skilgreindan bankareikning.

        ![Greiðsluskrá á TXT-sniði.](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>Sérsníða staðlað snið rafrænnar skýrslugerðar

Fyrir dæmið sem sýnt er í þessum hluta er best að nota skilgreiningar rafrænnar skýrslugerðar sem Microsoft býður upp á til að búa til greiðsluskrár lánardrottna á BACS-sniði, en bæta verður við sérstillingu til að styðja kröfur tiltekins banka. Einnig á að vera hægt að uppfæra sérstillta sniðið þegar koma nýjar útgáfur á skilgreiningum rafrænnar skýrslugerðar. Aftur á móti vill maður geta uppfært með sem minnstum kostnaði.

Í þessu tilfelli, sem fulltrúi Litware, Inc., þarf að búa til (afleiða) nýja skilgreiningu rafrænnar skýrslugerðar með því að nota **BACS (Bretland)** skilgreiningu sem Microsoft býður upp á sem grunn.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Búa til sérsniðið snið

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja síðan **BACS (Bretland)**. Litware, Inc. notar útgáfu 1.1 af þessari skilgreiningu rafrænnar skýrslugerðar sem grunn fyrir sérsniðnu útgáfuna.
3. Veljið **Stofna skilgreiningu** til að opna fellilistagluggann. Hægt er að nota þennan glugga til að stofna nýja skilgreiningu fyrir sérstillt greiðslusnið.
4. Í reitahópnum **Ný** skal velja valkostinn **Leiða af heiti: BACS (Bretland), Microsoft**.
5. Í reitinn **Heiti** skal færa inn **BACS (Bresk tollayfirvöld)**.

    ![Fellilisti í svarglugga fyrir stofnun skilgreiningar.](./media/er-quick-start2-add-derived-format.png)

6. Veljið **Stofna skilgreiningu**.

Útgáfa 1.1.1 af **BACS (Bresk tollayfirvöld)** skilgreiningarsniði rafrænnar skýrslugerðar er stofnuð. Þessi útgáfa er með stöðuna **Drög** og er hægt að breyta. Núverandi efni af sérstilltu sniði rafrænnar skýrslugerðar samsvarar efni sniðsins sem Microsoft býður upp á.

![Skilgreiningasíða með útgáfu 1.1.1 af BACS (UK custom) skilgreiningarsniði rafrænnar skýrslugerðar.](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a>Breyta sérsniðnu sniði

Skilgreina þarf sérstillta sniðið þannig að það standist tilteknar kröfur bankans. Bank gæti til dæmis gert kröfu um að greiðsluskrár sem búnar eru til feli í sér SWIFT-kóða þess banka sem úthlutað er hlutverki umboðsaðila í meðhöndlaðri greiðslu lánardrottins. SWIFT-kóðar eru alþjóðlegir bankakóðar sem auðkenna tiltekna banka um allan heim. Þeir eru einnig þekktar sem auðkenniskóðar banka (BICs). SWIFT-kóðinn verður að vera 11 stafir að lengd og það verður að færa hann inn við upphaf allra greiðslulína í greiðsluskrá sem búin er til.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja síðan **BACS (Bresk tollayfirvöld)**.
3. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1.1** af valdri skilgreiningu.
4. Veljið **Hönnuður**.
5. Á síðunni **Sniðshönnuður** skal velja **Sýna upplýsingar** til að skoða frekari upplýsingar um sniðseiningarnar.
6. Stækkið og yfirfarið eftirfarandi einingar:

    - **BACSReportsFolder** eining af gerðinni **Mappa**. Þessi eining er notuð til að búa til úttak á ZIP-sniði.
    - Einingin **skrá** af gerðinni **Skrá**. Þessi eining er notuð til að búa til greiðsluskrá á TXT-sniði.
    - Einingin **færslur** af gerðinni **Röð**. Þessi eining er notuð til að búa til eina greiðslulínu í greiðsluskrá.
    - Einingin **færsla** af gerðinni **Röð**. Þessi eining er notuð til að búa til staka reiti fyrir eina greiðslulínu.

7. Veljið eininguna **færsla**.

    ![Færslueining í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > Uppgefin skýrsla er stillt þannig að <a id="PositionRoutingNumber"></a>hver greiðslulína hefjist á leiðarnúmeri bankans. Sniðseiningin **vendBankRouteNum** er notuð í þessum tilgangi. 

8. Veljið **Bæta við** og síðan gerðina **Texti\\Strengur** fyrir sniðseininguna sem verið er að bæta við:

    1. Í reitinn **Heiti** skal færa inn **vendBankSWIFT**.
    2. Í reitinn **Lágmarkslengd** skal slá inn **11**.
    3. Í reitinn **Hámarkslengd** skal slá inn **11**.
    4. Veljið **Í lagi**.

    > [!NOTE]
    > Einingin **vendBankSWIFT** verður notuð til að færa inn SWIFT-kóða fyrir banka lánardrottins í útbúnum skrám.

9. Í trjáskipan sniðs skal velja **vendBankSWIFT**.
10. Veljið **Færa upp** til að færa valda sniðseiningu upp um eitt stig. Endurtakið þetta skref þar til einingin **vendBankSWIFT** er <a id="PositionSWIFTCode"></a>fyrsta einingin undir yfireiningunni **færsla**.

    ![VendBankSWIFT sem fyrsta einingin undir færslu í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start2-derived-format1.png)

11. Á meðan **vendBankSWIFT** er enn valið í trjáskipan sniðs skal velja flipann **Vörpun** og síðan stækka gagnagjafann **líkan**.
12. Stækkið **model.Payment** \> **model.Payment.CreditorAgent** og veljið gagnagjafareitinn **model.Payment.CreditorAgent.BICFI**. Þessi gagnagjafareitur sýnir SWIFT-kóðann fyrir banka lánardrottins sem úthlutað er hlutverki umboðsaðila í meðhöndlaðri greiðslu lánardrottins.
13. Veldu **Binda**. Sniðseiningin **vendBankSWIFT** er nú bundin við gagnagjafareitinn **model.Payment.CreditorAgent.BICFI** þannig að SWIFT-kóðar verða færðir inn í greiðsluskrár sem búnar eru til.

    ![vendBankSWIFT sniðseiningin bundin við gagnagjafareitinn model.Payment.CreditorAgent.BICFI í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start2-derived-format2.png)

14. Veldu **Vista**.
15. Lokið hönnunarsíðunni.

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>Merkja sérsniðið snið sem keyrsluhæft

Nú þegar fyrsta útgáfa af sérstilltu sniði hefur verið stofnuð og er með stöðuna **Drög**, er hægt að prufukeyra hana. Til að keyra skýrsluna þarf að vinna úr greiðslu lánardrottins með því að nota greiðslumátann sem vísar til sérstillts sniðs rafrænnar skýrslugerðar. Sjálfgefið er að þegar kallað er á snið rafrænnar skýrslugerðar úr forritinu, eru aðeins útgáfur sem eru með stöðuna **Lokið** eða **Samnýtt** teknar til greina. Þessi leið hjálpar til við að koma í veg fyrir að snið rafrænnar skýrslugerðar með ókláraðri hönnun verði notuð. Fyrir prufukeyrslur er hinsvegar hægt að þvinga forritið til að nota sniðsútgáfu rafrænnar skýrslugerðar sem er með stöðuna **Drög**. Á þennan hátt er hægt að leiðrétta núverandi sniðsútgáfu ef gera þarf einhverjar breytingar. Frekari upplýsingar er að finna í [Nothæfni](electronic-reporting-destinations.md#applicability).

Til að nota útgáfudrög af sniði rafrænnar skýrslugerðar þarf sérstaklega að merkja rafræna skýrslugerðarsniðið.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
3. Í glugganum **Færibreytur notanda** skal stilla valkostinn **Keyra stillingar** á **Já** og síðan velja **Í lagi**.
4. Veljið **Breyta** til að gera núverandi síðu breytanlega ef þörf krefur.
5. Í skilgreiningatrénu vinstra megin á svæðinu skal velja **BACS (Bresk tollayfirvöld)**.
6. Stillið valkostinn **Keyra drög** á **Já**.

    ![Keyra valkostinn fyrir drög á skilgreiningarsíðunni.](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a>Vinna úr greiðslu lánardrottins með því að nota sérsniðið snið rafrænnar skýrslugerðar

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a>Setja upp rafrænan greiðslumáta

Skilgreina þarf rafrænan greiðslumáta þannig að sérstillt snið rafrænnar skýrslugerðar sé notað til að vinna úr lánardrottnagreiðslum.

1. Farið í **Viðskiptaskuldir** \> **Greiðsluuppsetning** \> **Greiðsluháttur**.
2. Á síðunni **Greiðslumátar - lánardrottnar** skal velja greiðslumátann **Rafrænt** vinstra megin á svæðinu.
3. Veljið **Breyta**.
4. Í flýtiflipanum **Skráarsnið** skal stilla valkostinn **Almennt rafrænt útflutningssnið** á **Já**.
5. Í reitnum **Skilgreining útflutningssniðs** skal velja skilgreiningarsniðið **BACS (Bresk tollayfirvöld)**.

    ![Greiðslumátar - síða lánardrottins til að setja upp rafrænan greiðslumáta til að vinna greiðslur frá lánardrottnum með sérstilltu sniði.](./media/er-quick-start2-method-of-payment2.png)

6. Veldu **Vista**.

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a>Vinna úr lánardrottnagreiðslu

1. Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.
2. Á síðunni **Greiðslubók lánardrottins** skal velja þá greiðslubók sem var áður búin til.
3. Veldu **Línur**.
4. Á síðunni **Greiðslur lánardrottna**, fyrir ofan hnitanetið, skal velja **Greiðslustaða** \> **Engin**.
5. Smellið á **Búa til greiðslu**.
6. Í svarglugganum **Búa til greiðslur** skal færa inn eftirfarandi upplýsingar:

    - Í reitnum **Greiðslumáti** skal velja **Rafrænn**.
    - Í reitnum **Bankareikningur** skal velja **GBSI OPER**.

7. Veljið **Í lagi**.
8. Í svarglugganum **Rafrænar skýrslufæribreytur** skal stilla valkostinn **Prenta eftirlitsskýrslu** á **Já** og velja síðan **Í lagi**.

    > [!NOTE]
    > Auk greiðsluskráarinnar er eingöngu hægt að búa til eftirlitsskýrsluna.

9. Sækið zip-skrána og dragið síðan eftirfarandi skrár út úr henni:

    - Eftirlitsskýrslan á Excel-sniði
    - Greiðsluskráin á TXT-sniði

        Takið eftir því, í samræmi við skipulag á sérstilltu sniði rafrænnar skýrslugerðar, að greiðslulínan [hefst](#PositionSWIFTCode) nú á SWIFT-kóðanum sem var [sleginn inn](#DefineSWIFTCode) fyrir bankareikning lánardrottins sem er með greiðslu sem unnið hefur verið úr.

        ![Greiðsluskrá á TXT-sniði notuð til að vinna greiðslu lánardrottins.](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a>Flytja inn nýjar útgáfur af stöðluðum skilgreiningum rafræns skýrslugerðarsniðs

Fyrir dæmið sem sýnt er í þessum hluta kemur tilkynning um þekkingargrunnsgreinina [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046). Þessi tilkynning veitir upplýsingar um nýju sniðsútgáfuna **BACS (Bretland)** fyrir rafræna skýrslugerð sem Microsoft hefur gefið út. Ásamt eftirlitsskýrslunni gerir þessi nýja útgáfa notendum kleift að búa til skýrslu greiðslutilkynningr og skýrsla um þátttökuathugasemd á meðan unnið er úr greiðslu lánardrottins. Mælt er með því að hefja notkun á þessari virkni.

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a>Flytja inn nýjar útgáfur af stöðluðum skilgreiningum rafrænnar skýrslugerðar

Til að bæta nýjum útgáfum af skilgreiningum rafrænnar skýrslugerðar við núverandi Finance-tilvik þarf að flytja þær inn úr [gagnageymslu](general-electronic-reporting.md#Repository) rafrænnar skýrslugerðar sem voru skilgreindar.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Skilgreiningarveitur**, skal velja reitinn **Microsoft** og síðan velja **Gagnageymslur** til að skoða lista yfir gagnageymslur fyrir Microsoft-veituna.
3. Á síðunni **Skilgreiningageymslur** skal velja gagnageymslu af gerðinni **Altæk** og síðan velja **Opna**. Ef beðið er um heimild til að tengjast við Regulatory Configuration Service, skal fylgja leiðbeiningum um heimild.
4. Á síðunni **Skilgreiningageymsla**, í skilgreiningatrénu vinstra megin á svæðinu, skal velja skilgreiningarsniðið **BACS (Bretland)**.
5. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **3.3** af valdri skilgreiningu rafræns skýrslugerðarsniðs.
6. Veljið **Flytja inn** til að sækja valda útgáfu úr altækri geymslu í núverandi fjármálatilvik.

![Skilgreiningageymslusíða, flýtiflipi útgáfa, Flytja inn hnappur.](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> Ef það reynist erfitt að opna [Altæka geymsla](er-download-configurations-global-repo.md) er hægt að [sækja skilgreiningar](download-electronic-reporting-configuration-lcs.md) hjá LCS í staðinn.

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a>Fara yfir innfluttar skilgreiningar rafræns skýrslugerðarsniðs

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja síðan **BACS (Bretland)**.
4. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **3.3**.
5. Veljið **Hönnuður**.
6. Á síðunni **Sniðshönnuður** skal stækka sniðseininguna **BACSReportsFolder**.
7.  Takið eftir að útgáfa 3.3 inniheldur sniðseininguna **PaymentAdviceReport** sem notuð er til að búa til skýrslu greiðslutilkynninga þegar unnið er úr greiðslu lánardrottins.

    ![Sniðseiningin PaymentAdviceReport í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start2-imported-solution2.png)

8. Lokið hönnunarsíðunni.

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a>Innleiða breytingarnar í nýju útgáfu innflutts sniðs í sérsniðnu sniði

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a>Ljúkið við núgildandi drög að útgáfu sérsniðins sniðs

Ef ætlunin er að halda núverandi ástandi á sérstilltu sniði, skal ljúka útgáfudrögum 1.1.1 með því að breyta stöðu hennar úr **Drög** í **Lokið**.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan**, stækka **BACS (Bretland)** og velja síðan **BACS (Bresk tollayfirvöld)**.
4. Í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** \> **Ljúka** og síðan velja **Í lagi**.

Staða útgáfu 1.1.1 er breytt úr **Drög** í **Lokið** og útgáfa verður skrifvarin. Nýrri og breytanlegri útgáfa 1.1.2 hefur verið bætt við og er með stöðuna **Drög**. Hægt er að nota þessa útgáfu til að gera frekari breytingar á sérstilltu sniði rafrænnar skýrslugerðar.

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a>Endurstilla grunn sérsniðins sniðs á nýja grunnútgáfu

Til að byrja að nota nýja virkni fyrir útgáfu 3.3 af sniðinu **BACS (Bretland)** í sérstillingunum, þarf að breyta grunnskilgreiningu útgáfunnar fyrir sérstilltu skilgreininguna, **BACS (Bresk tollayfirvöld)**. Þetta ferli kallast [endurreikningur](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase). Í stað útgáfu 1.1 af **BACS (Bretland)** skal nota útgáfu 3.3.

1. Farðu í **Fyrirtækisstjórnun** \> **Rafræn skýrslugerð** \> **Skilgreiningar**.
2. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja síðan **BACS (Bresk tollayfirvöld)**.
3. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **1.1.2** og síðan velja **Endurstilla grunn**.
4. Í svarglugganum **Endurstilla grunn**, í reitnum **Markútgáfa**, skal velja útgáfu **3.3** grunnskilgreiningarinnar til að nota hana sem nýja grunninn og til að uppfæra skilgreininguna.

    ![Gluggi fyrir endurreikning grunns.](./media/er-quick-start2-rebase1.png)

5. Veldu **Í lagi**.
6. Takið eftir að númer útgáfudraga hefur breyst úr **1.1.2** í **3.3.2** til að endurspegla breytinguna í grunnútgáfunni.

    Þegar sérstillta útgáfan og nýja grunnútgáfan eru sameinaðar gætu einhverjir árekstrar uppgötvast vegna sniðsbreytinga sem ekki er hægt að sameina sjálfkrafa.

    ![Endurstilltur grunnur skilgreiningar með árekstrum á skilgreiningarsíðunni.](./media/er-quick-start2-rebase2.png)

    Ef árekstrar uppgötvast verða að leysa úr þeim handvirkt í sniðshönnuðinum.

7. Í flýtiflipanum **Útgáfur** skal velja útgáfuna **3.3.2**.
8. Veljið **Hönnuður**.
9. Á síðunni **Sniðshönnuður**, í flýtiflipanum **Upplýsingar**, skal velja færslu fyrir árekstur endurstillts grunns og síðan velja **Nota grunngildi**.

    ![Færsla fyrir árekstur endurstillts grunns í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start2-rebase3.png)

10. Veldu **Vista**.

    Færsla fyrir árekstur endurstillts grunns ætti ekki lengur að birtast í flýtiflipanum **Upplýsingar**.

    ![Leyst úr árekstri í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > Leyst var úr árekstrinum með því að staðfesta að nota verður útgáfu 3 fyrir grunnlíkanið í þessu sniði rafrænnar skýrslugerðar.

11. Stækkið **BACSReportsFolder** \> **skrá** \> **færslur** \> **færsla**.
12. Takið eftir í flipanum **Vörpun** að útgáfa 3.3.2 af sérstilltu sniði rafrænnar skýrslugerðar inniheldur bæði sérstillinguna (sniðseiningin **vendBankSWIFT** og bindingu hennar) og nýja virkni útgáfu 3.3 af grunnsniði rafrænnar skýrslugerðar sem kom frá Microsoft (sniðseiningin **PaymentAdviceReport** ásamt földuðum einingum og skilgreindum bindingum). Í aðeins örfáum músarsmellum voru breytingarnar gerðar á nýju grunnútgáfunni með því að sameina þær við sérstillinguna.

    ![Sameinað snið í aðgerðarhönnuði rafrænnar skýrslugerðar.](./media/er-quick-start2-rebase5.png)

13. Lokið hönnunarsíðunni.

> [!NOTE]
> Endurstillingaraðgerð grunns er afturkræf. Til að hætta við þessa endurstillingu grunns skal velja **1.1.1** fyrir sniðið **BACS (Bresk tollayfirvöld)** í flýtiflipanum **Útgáfur** og velja síðan **Ná í þessa útgáfu**. Útgáfa 3.3.2 verður síðan gefið númerið 1.1.2 og efni útgáfudraga 1.1.2 munu samsvara efni í útgáfu 1.1.1.

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a>Vinna úr greiðslu lánardrottins með því að nota endurstilltan grunn rafræns skýrslugerðarsniðs

1. Farið í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók lánardrottins**.
2. Á síðunni **Greiðslubók lánardrottins** skal velja þá greiðslubók sem var áður búin til.
3. Veldu **Línur**.
4. Á síðunni **Greiðslur lánardrottna**, fyrir ofan hnitanetið, skal velja **Greiðslustaða** \> **Engin**.
5. Smellið á **Búa til greiðslu**.
6. Í svarglugganum **Búa til greiðslur** skal færa inn eftirfarandi upplýsingar:

    - Í reitnum **Greiðslumáti** skal velja **Rafrænn**.
    - Í reitnum **Bankareikningur** skal velja **GBSI OPER**.

7. Veljið **Í lagi**.
8. Í svarglugganum **Rafrænar skýrslufæribreytur** skal færa inn eftirfarandi upplýsingar:

    - Stilltu valkostinn **Prenta eftirlitsskýrslu** á **Já**.
    - Stillið valkostinn **Prenta greiðslutilkynningu** á **Já**.

    ![Svargluggi rafrænna skýrslufæribreyta.](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > Auk greiðsluskráarinnar er nú hægt að búa til eftirlitsskýrsluna og skýrslu greiðslutilkynningar.

9. Veljið **Í lagi**.
10. Sækið zip-skrána og dragið síðan eftirfarandi skrár út úr henni:

    - Eftirlitsskýrslan á Excel-sniði
    - Skýrsla greiðslutilkynningar á Excel-sniði

        ![Skýrsla greiðslutilkynningar á Excel-sniði.](./media/er-quick-start2-payment-advice-report.png)

    - Greiðsluskráin á TXT-sniði

        Takið eftir því að greiðslulínan í myndaðri skrá hefst á SWIFT-kóðanum sem var sleginn inn fyrir bankareikning lánardrottins sem er með greiðslu sem unnið hefur verið úr.

        ![Greiðsluskrá á TXT-sniði notuð til að vinna greiðslu lánardrottins með endurstilltan grunn rafræns skýrslugerðarsniðs.](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a>Frekari upplýsingar

- [Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)
- [Sækja skilgreiningar rafrænnar skýrslugerðar úr Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
