---
title: Stjórna nokkrum afleiddum vörpunum fyrir eina rót líkans
description: Þetta efnisatriði útskýrir hvernig á að stjórna nokkrum afleiddum vörpunum sem voru skilgreindar fyrir eina rót líkans.
author: NickSelin
manager: AnnBe
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERModelMappingTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb4fcda42361b0f14e37027d21739dfc42b44cb1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565492"
---
# <a name="manage-several-derived-mappings-for-a-single-model-root"></a>Stjórna nokkrum afleiddum vörpunum fyrir eina rót líkans

[!include [banner](../includes/banner.md)]

[Gagnalíkanshluti](general-electronic-reporting.md) [rafrænnar skýrslugerðar](general-electronic-reporting.md#data-model-and-model-mapping-components) er notaður í öllum skilgreindum hlutum [rafræns skýrslugerðarsniðs](general-electronic-reporting.md#FormatComponentOutbound) sem gagnagjafinn til að mynda skjöl á útleið. Til að lýsa einu viðskiptaléni skal skilgreina gagnalíkanshlut sem er með margar rótarskilgreiningar. 

Allar rótarskilgreiningar gera notanda kleift að tákna gögn í þessu léni sem hentar best tilteknum markmiðum skýrslugerðar. Fyrir hverja rótarskilgreiningu er hægt að skilgreina [gagnalíkanshlut](general-electronic-reporting.md#data-model-and-model-mapping-components) rafrænnar skýrslugerðar sem tiltekna samþættingu Microsoft Dynamics 365 Finance á gagnalíkaninu. Á þennan hátt er lýst hvernig gagnalíkanið verður fyllt út við keyrslu.

Gagnalíkanshlutar rafrænnar skýrslugerðar geta verið í [skilgreiningum](general-electronic-reporting.md#Configuration) gagnalíkans rafrænnar skýrslugerðar og skilgreiningum gagnavörpunar rafrænnar skýrslugerðar. Ein skilgreining rafrænnar skýrslugerðar getur innihaldið vörpunarhluta sem hver fyrir sig er skilgreindur fyrir eina rótarskilgreiningu. Að öðrum kosti getur ein skilgreining rafrænnar skýrslugerðar innihaldið aðeins einn vörpunarhluta sem er skilgreindur fyrir eina rótarskilgreiningu.

Margar skilgreiningarveitur bjóða mögulega upp á skilgreiningar líkanavörpunar rafrænnar skýrslugerðar fyrir sama gagnalíkan rafrænnar skýrslugerðar. Þessar skilgreiningar líkanavörpunar gætu innihaldið vörpunarhluta fyrir mismunandi rótarskilgreiningar. Hugsanlega er hægt að nota líkanavörpun fyrir eina rótarskilgreiningu sem er ein [veita](general-electronic-reporting.md#Provider) býður upp á og nota líkanavörpun fyrir aðra rótarskilgreiningu sem önnur veita býður upp á.

Ferlin í þessu efnisatriði útskýra hvernig á að stjórna mörgum skilgreiningum líkanavörpunar rafrænnar skýrslugerðar fyrir gagnalíkan rafrænnar skýrslugerðar þegar þær innihalda mismunandi þætti líkanavörpunar fyrir sömu rótarskilgreininguna. 

Til að ljúka ferlinu í þessu efnisatriði þarf notanda að vera úthlutað hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar.

Öll eftirfarandi ferli er hægt að vinna í USMF fyrirtækinu. Ekki er þörf á neinni kóðun.

## <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Sem notandi í hlutverki þróunaraðila rafrænnar skýrslugerðar skal [skilgreina lágmarkssafn](er-quick-start2-customize-report.md#ConfigureFramework) af færibreytum rafrænnar skýrslugerðar áður en rammi rafrænnar skýrslugerðar er notaður til að mynda viðskiptaskjöl.

## <a name="import-the-standard-er-format-configurations"></a>Flytja inn staðlaðar skilgreiningar rafræns skýrslugerðarsniðs

Til að bæta stöðluðum skilgreiningum rafrænnar skýrslugerðar við núverandi tilvik af Finance, þarf að flytja þær inn úr gagnageymslu rafrænnar skýrslugerðar sem var skilgreind fyrir það tilvik. Fylgið þessum skrefum í [Sækja skilgreiningar rafrænnar skýrslugerðar úr altækri geymslu skilgreiningarþjónustu](er-download-configurations-global-repo.md) til að flytja inn eftirfarandi skilgreiningar rafrænnar skýrslugerðar:

- **Reikningur með frjálsum texta (Excel)**, útgáfa 220.106
- **Verkreikningur (Excel)**, útgáfa 226.27

## <a name="review-the-imported-er-configurations"></a>Skoða innfluttar skilgreiningar rafrænnar skýrslugerðar

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja reitinn **Skilgreiningar skýrslugerðar**.
3. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Reikningslíkan**.

    ![Innfluttar skilgreiningar yfirfarnar á skilgreiningarsíðunni](./media/er-multiple-model-mappings-image1.png)

4. Farið yfir sniðið **Reikningur með frjálsum texta (Excel)**:

    1. Í skilgreiningatrénu í glugganum vinstra megin skal velja **Reikningur með frjálsum texta (Excel)**.
    2. Í aðgerðarúðunni skal velja **Hönnuður**.
    3. Á síðunni **Sniðshönnuður**, í flipanum **Vörpun**, í gagnagjafanum, skal velja **Líkan**.
    4. Velja **Skoða**.
    
       Núverandi snið rafrænnar skýrslugerðar er skilgreint til að nota rótarskilgreiningu **InvoiceCustomer** í **Reikningslíkan**. Þegar þetta snið er keyrt og kallað er á gagnagjafann **Líkan**, er líkanavörpunin sem er skilgreind fyrir rótarskilgreininguna **InvoiceCustomer** notuð til að nálgast forritsgögn og fylla út í gagnalíkanið.

        ![Gagnagjafi líkans yfirfarinn á síðu sniðshönnuðar](./media/er-multiple-model-mappings-image2.png)

    6. Lokaðu síðunni **Sniðshönnuður**.

5. Farið yfir skilgreininguna **Vörpun reikningslíkans**:

    1. Í skilgreiningatrénu á svæðinu til vinstri skal velja **Vörpun reikningslíkans**.
    2. Í aðgerðarúðunni skal velja **Hönnuður**.
    3. Athugið að á síðunni **Líkanavörpun á gagnagjafa** inniheldur núverandi skilgreining á líkanavörpun rafrænnar skýrslugerðar nokkra þætti líkanavörpunar:

        + Líkanavörpunin **Reikningur viðskiptavinar** er skilgreindur fyrir rótarskilgreininguna **InvoiceCustomer** í **Reikningslíkan**. Þar af leiðandi, þegar rafræna skýrslugerðarsniðið **Reikningur með frjálsum texta (Excel)** er keyrt, er hægt að velja líkanavörpunina **Reikningur viðskiptavinar** í þessari skilgreiningu rafrænnar skýrslugerðar til að nálgast forritsgögn og fylla út gagnalíkanið.
        + Líkanavörpunin **Verkreikningur** er skilgreindur fyrir rótarskilgreininguna **InvoiceProject** í **Reikningslíkan**. Þar af leiðandi, þegar rafræna skýrslugerðarsniðið **Verkreikningur (Excel)** er keyrt, er hægt að velja líkanavörpunina **Verkreikningur** í þessari skilgreiningu rafrænnar skýrslugerðar til að nálgast forritsgögn og fylla út gagnalíkanið.

        ![Líkanavörpun reiknings á síðu líkanavörpunar á gagnagjafa](./media/er-multiple-model-mappings-image3.png)

    4. Lokið síðunni **Líkanavörpun á gagnagjafa**.
    5. Í flýtiflipanum **Útgáfur** skal velja **Eyða** til að eyða öllum útgáfum þessarar skilgreiningu rafrænnar skýrslugerðar sem eru eldri en útgáfa 240.175.

6. Farið yfir efni skilgreiningarinnar **Líkanavörpun verkreiknings (RDP)**:

    1. Í skilgreiningatrénu á svæðinu til vinstri skal velja **Líkanavörpun verkreiknings (RDP)**.
    2. Í aðgerðarúðunni skal velja **Hönnuður**.
    3. Athugið að á síðunni **Líkanavörpun á gagnagjafa** inniheldur núverandi skilgreining á líkanavörpun rafrænnar skýrslugerðar líkanavörpunina **InvoiceProject** og að þessi líkanavörpun er skilgreind fyrir rótarskilgreininguna **InvoiceProject** í **Reikningslíkan**. Þegar rafræna skýrslugerðarsniðið **Verkreikningur (Excel)** er keyrt skal velja líkanavörpun **InvoiceProject** í þessari skilgreiningu rafrænnar skýrslugerðar til að nálgast forritsgögn og fylla út gagnalíkanið.

        ![Líkanavörpun verkreiknings á síðu líkanavörpunar á gagnagjafa](./media/er-multiple-model-mappings-image4.png)

    4. Lokið síðunni **Líkanavörpun á gagnagjafa**.
    5. Í flýtiflipanum **Útgáfur** skal velja **Eyða** til að eyða öllum útgáfum þessarar skilgreiningu rafrænnar skýrslugerðar sem eru eldri en útgáfa 226.35.

## <a name="customize-the-imported-er-configurations"></a>Sérstilla innfluttar skilgreiningar rafrænnar skýrslugerðar

Þessi hluti útskýrir hvernig á að [sérstilla](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration) líkanavarpanir sem Microsoft býður upp á. Til dæmis gæti sérstilling verið nauðsynleg til að innleiða sérsniðna reglu eða bæta við bindingar sem vantar.

### <a name="customize-the-invoice-model-mapping-configuration"></a>Sérstilla skilgreiningu á líkanavörpun reiknings

1. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal velja **Reikningslíkanavörpun**.
2. Í aðgerðasvæðinu velurðu **Stofna skilgreiningu**.
3. Í fellilistaglugganum **Stofna skilgreiningu**, í reitnum **Ný**, skal velja **Leiða af heiti: Líkanavörpun reiknings, Microsoft**.
4. Í reitinn **Heiti** skal færa inn **Vörpun reikningslíkans (Litware)**.
5. Veljið **Stofna skilgreiningu**.
6. [Merkið](er-quick-start2-customize-report.md#MarkFormatRunnable) útgáfu [draga](general-electronic-reporting.md#component-versioning) fyrir afleidda vörpun sem tilbúna fyrir keyrslu:

    1. Á aðgerðasvæðinu, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.
    2. Í glugganum **Færibreytur notanda** skal stilla valkostinn **Keyra stillingar** á **Já** og síðan velja **Í lagi**.
    3. Veljið **Breyta** til að gera síðuna breytanlega ef þörf krefur.
    4. Fyrir skilgreininguna **Reikningslíkanavörpun Litware** sem er þegar valin í skilgreiningatrénu skal stilla valkostinn **Keyra drög** á **Já**.

7. Á aðgerðasvæðinu skal velja **Hönnuður** til að yfirfara líkanavarpanir þessarar skilgreiningar.

    ![Líkanavörpun reiknings yfirfarin á síðu líkanavörpunar á gagnagjafa](./media/er-multiple-model-mappings-image5.png)

    > [!TIP]
    > Nú er hægt að opna alla þætti líkanavörpunar fyrir rafræna skýrslugerð í þessari skilgreiningu rafrænnar skýrslugerðar í hönnuðinum til að skilgreina sérstillta reglu. Frekari upplýsingar er að finna í [Sérstilla skilgreiningu líkanavörpunar](er-quick-start3-customize-report.md#customize-the-model-mapping-configuration).

8. Lokið síðunni **Líkanavörpun á gagnagjafa**.

Nú eru komnar skilgreiningarnar **Líkanavörpun reiknings** og **Reikningslíkanavörpun Litware**, sem hvor fyrir sig er með líkanavörpun sem er skilgreind fyrir rótarskilgreininguna **InvoiceCustomer**. Úthlutið sérstaklega einni líkanavörpuninni sem sjálfgefinni líkanavörpun sem er notuð af einhverju rafræna skýrslugerðarsniðinu á borð við sniðið **Reikningur með frjálsum texta (Excel)** sem inniheldur gagnagjafa líkans sem er með rótarskilgreininguna **InvoiceCustomer**. Að öðrum kosti, þegar eitt þessara sniða rafrænnar skýrslugerðar er keyrt, breytt eða villuleitað, er eftirfarandi undantekning notuð til að tilkynna notanda um að engin sjálfgefin líkanavörpun hafi verið valin sérstaklega:
 
> Fleiri en ein líkanavörpun er fyrirliggjandi fyrir gagnalíkanið \<model name\> (\<root descriptor\>) í skilgreiningunum \<configuration names separated by commas\>. Stillið eina skilgreininguna sem sjálfgefna.

![Sniðið opnað til að breyta því á síðu skilgreininga](./media/er-multiple-model-mappings-image6.gif)

### <a name="customize-the-project-invoice-model-mapping-rdp-configuration"></a>Sérstilla skilgreiningu líkanavörpunar verkreiknings (RDP)

1. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal velja **Líkanavörpun verkreiknings (RDP)**.
2. Í aðgerðasvæðinu velurðu **Stofna skilgreiningu**.
3. Í svarglugganum **Stofna skilgreiningu**, í reitnum **Ný**, skal velja **Leiða af heiti: Líkanavörpun verkreiknings (RDP), Microsoft**.
4. Í reitinn **Heiti** skal færa inn **Líkanavörpun verkreiknings Litware**.
5. Veljið **Stofna skilgreiningu**.
6. Fyrir skilgreininguna **Líkanavörpun verkreiknings Litware** sem er þegar valin í skilgreiningatrénu skal stilla valkostinn **Keyra drög** á **Já**.
7. Á aðgerðasvæðinu skal velja **Hönnuður** til að yfirfara líkanavarpanir þessarar skilgreiningar.

    ![Yfirfara sérstilltar líkanavarpanir verkreikninga á síðu líkanavörpunar á gagnagjafa](./media/er-multiple-model-mappings-image7.png)

8. Lokið síðunni **Líkanavörpun á gagnagjafa**.

Nú eru til staðar skilgreiningarnar **Líkanavörpun reiknings**, **Líkanavörpun verkreiknings (RDP)** og **Líkanavörpun verkreiknings Litware**. Hver þessara skilgreininga er með líkanavörpun skilgreinda fyrir rótarskilgreininguna **InvoiceProject**. Úthlutið sérstaklega einni líkanavörpuninni sem sjálfgefinni líkanavörpun sem er notuð af einhverju rafræna skýrslugerðarsniðinu. Notið til dæmis sniðið **Verkreikningur (Excel)** sem inniheldur gagnagjafa líkans sem er með rótarskilgreininguna **InvoiceProject**. Að öðrum kosti, þegar eitt þessara sniða rafrænnar skýrslugerðar er keyrt eða breytt, er undantekning notuð til að tilkynna notanda um að engin sjálfgefin líkanavörpun hafi verið valin sérstaklega.

## <a name="select-the-derived-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Velja afleidda skilgreiningu reikningslíkanavörpunar Litware sem skilgreininguna sem inniheldur sjálfgefnar líkanavarpanir

1. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal velja **Reikningslíkanavörpun Litware**.
2. Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.

    ![Stilla líkanavörpun sem sjálfgefna líkanavörpun á síðu skilgreininga](./media/er-multiple-model-mappings-image8.png)

    Vegna þessarar stillingar er líkanavörpunin **Afrit af reikningi viðskiptavinar** notuð til að keyra **Reikningur með frjálsum texta (Excel)** eða þegar henni er breytt eða hún villuleituð. Líkanavörpunin **Reikningur viðskiptavinar** úr skilgreiningunni **Líkanavörpun reiknings** er hunsuð.

    Nú er hægt að opna sniðið **Reikningur með frjálsum texta (Excel)** til að yfirfara í sniðshönnuðinum.

## <a name="select-the-derived-project-invoice-model-mapping-litware-configuration-as-the-configuration-that-contains-default-model-mappings"></a>Velja afleidda skilgreiningu líkanavörpunar verkreiknings Litware sem skilgreininguna sem inniheldur sjálfgefnar líkanavarpanir

1. Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal velja **Reikningslíkanavörpun Litware**.
2. Stillið valkostinn **Sjálfgefið fyrir líkanavörpun** á **Já**.

    Í þessu tilfelli, ólíkt tilfellinu sem er lýst fyrir skilgreininguna **Reikningslíkanavörpun Litware** í hlutanum hér á undan, er hægt að byrjað að nota líkanavörpun **Afrit af InvoiceProject** úr skilgreiningunni **Líkanavörpun verkreiknings Litware**. Tvær skilgreiningar sem innihalda líkanavörpun fyrir rótarskilgreininguna **InvoiceProject** eru sem stendur merktar sem sjálfgefin skilgreining. Þær eru þar af leiðandi með jafnan forgang. Til að leysa úr þessu vandamáli skal ljúka eftirstandandi skrefum í þessu ferli.

3. Í skilgreiningatrénu á svæðinu til vinstri skal velja **Reikningslíkanavörpun Litware**.
4. Í aðgerðarúðunni skal velja **Hönnuður**.
5. Á síðunni **Líkanavörpun á gagnagjafa** skal velja **Breyta** til að gera síðuna breytanlega ef þörf krefur.
6. Veljið líkanavörpunina **Afrit af verkreikningi** og veljið síðan gátreitinn **Er eytt** fyrir hana.

    ![Líkanavörpunin stillt sem sýndareyðing á síðu líkanavörpunar á gagnagjafa](./media/er-multiple-model-mappings-image9.png)

    Vegna þessarar stilllingar er litið á skilgreininguna **Reikningslíkanavörpun Litware** eins og hún hafi enga líkanavörpun fyrir rótarskilgreininguna **InvoiceProject**. Líkanavörpun **Afrit af InvoiceProject** er sjálfgefið birt. Skilgreiningin **Líkanavörpun verkreiknings Litware**, sem inniheldur þessa líkanavörpun, er merkt sem sjálfgefin skilgreining. Þar sem hún er merkt sem sjálfgefin, hefur hún hærri forgang en líkanavörpun **InvoiceProject** úr skilgreiningunni **Líkanavörpun verkreiknings (RDP)**.

## <a name="other-considerations"></a>Annað sem skal hafa í huga

Líkanavörpunin **Afrit af InvoiceProject** í skilgreiningunni **Líkanavörpun verkreiknings Litware** er hönnuð til að nota gagnagjafa **ReportDataProvider**. Gagnagjafinn er hluti af gerðinni *Hlutur* sem vísar í forritsklasann **PsaProjInvoiceDP**. Þessi klasi er innleiddur sem gagnaveita fyrir skýrslu SQL Server Reporting Services (SSRS) verkreiknings í ramma prentstýringar. Veljið þennan gagnagjafa sem [samþættingarpunkt](er-apis-app10-0-11.md#api-to-run-a-format-mapping-for-the-generation-of-outbound-documents) rafrænnar skýrslugerðar. Núverandi innleiðing rafrænnar skýrslugerðar fyrir skýrslur prentstýringar tekur þessa stillingu til greina. Fyrir frekari upplýsingar skal yfirfara frumkóða forritsklasans **ERPrintMgmtDataProviderReport**. Við keyrslu neyðir úthlutun á gagnagjafa **ReportDataProvider**, sem samþættingarpunkt líkanavörpunar, Finance til að taka þennan vörpunarhluta fram yfir vörpunarhlutann **InvoiceProject** úr skilgreiningunni **Líkanavörpun verkreiknings (RDP)**.

## <a name="see-also"></a>Sjá einnig

- [Stjórna vörpunarlíkani rafrænnar skýrslugerðar í aðskilinni skilgreiningu rafrænnar skýrslugerðar](./tasks/er-manage-model-mapping-configurations-july-2017.md)
- [Skilgreina varpanir rafrænna skýrslugerðarlíkana sem háð eru samhengi við lönd](er-country-dependent-model-mapping.md)
- [Breytingar á API rafræns skýrslugerðarramma](er-apis-app10-0-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]