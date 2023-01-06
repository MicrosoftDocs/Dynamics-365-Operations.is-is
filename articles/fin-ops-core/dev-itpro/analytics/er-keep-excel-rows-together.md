---
title: Hanna ER-snið til að halda línum saman á sömu Excel-síðu
description: Í þessari grein er útskýrt hvernig á að hanna snið rafrænnar skýrslugerðar sem heldur saman línum á sömu Microsoft Excel síðunni.
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.custom: 220314
ms.assetid: ''
ms.search.form: EROperationDesigner
ms.openlocfilehash: 7ecc4358a0d4d9ae9e729393bd3ac4cefbf15ad2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287959"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Hanna ER-snið til að halda línum saman á sömu Excel-síðu

[!include [banner](../includes/banner.md)]


Í þessari grein er útskýrt hvernig notandi í hlutverki kerfisstjóra eða í hagnýtu ráðgjafahlutverki rafrænnar skýrslugerðar getur stillt [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) [snið](er-overview-components.md#format-component) til að mynda skjöl á útleið í Microsoft Excel stjórna síðuskiptingu skjals þannig að stofnuðum línum sé haldið á sömu síðu.

Í þessu dæmi breytir þú rafrænu skýrslugerðarsniði frá Microsoft sem er notað til að prenta reikninga með frjálsum texta í Excel. Breytingarnar þínar gera þér kleift að hafa umsjón með síðuskiptingu á myndaðri skýrslu textareikninga þannig að öllum línum stakrar reikningslínu sé haldið á sömu síðunni ef það er mögulegt.

Hægt er að ljúka ferlunum í þessari grein í fyrirtækinu **USMF**. Ekki er þörf á neinni kóðun.

Í þessu dæmi muntu stofna nauðsynlegar ER-[skilgreiningar](general-electronic-reporting.md#Configuration) fyrir sýnifyrirtækið, **Litware, Inc.**. Tryggið að skilgreiningarveita fyrir sýndarfyrirtækið **Litware, Inc.** (`http://www.litware.com`) sé skráð fyrir ramma rafrænnar skýrslugerðar og merkt sem **Virk**. Ef skilgreiningarveita er ekki skráð, eða ef hún er ekki merkt sem **Virk**, skal fylgja skrefunum í greininni [Stofna skilgreiningaveitu og merkja hana sem virka](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Færa inn nýjan reikning með frjálsum texta

1. Fylgdu skrefunum í [Stofna reikning með frjálsum texta](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) til að bæta við reikningi með frjálsum texta.

    1. Bætið einni línu við reikninginn.
    2. Bæta við fimm glósum fyrir reikningslínuna.

    ![Yfirfara athugasemdir reikningslínu á viðhengissíðunni.](./media/er-keep-excel-rows-together-notes.png)

2. Fylgdu skrefunum í [Afrita línur](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) til að búa til fimm reikningslínur í viðbót sem eru afrit af reikningslínunni sem bætt var við í síðasta skrefi.

    ![Farið yfir línur reiknings með frjálsum texta á síðunni Reikningur með frjálsum texta.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ramma rafrænnar skýrslugerðar til að hanna sérsniðna útgáfu af stöðluðu sniði rafrænnar skýrslugerðar.

## <a name="import-the-standard-er-format-configuration"></a>Flytja inn staðlaða skilgreiningu rafræns skýrslugerðarsniðs

Fylgdu skrefunum í [Flytja inn staðlaða skilgreiningu rafræns skýrslugerðarsniðs](er-quick-start2-customize-report.md#ImportERSolution1) til að bæta stöðluðum skilgreiningum rafrænnar skýrslugerðar við núverandi tilvik af Dynamics 365 Finance. Til dæmis skaltu flytja inn útgáfu **252.116** af sniðsskilgreiningunni **Reikningur með frjálsum texta (Excel)**. Grunnútgáfa **252** af grunnskilgreiningu **Reikningslíkans** er sjálfkrafa flutt inn úr geymslunni með nauðsynlegri skilgreiningu fyrir **Vörpun reiknignslíkans**.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Uppsetning prentstýringar til að nota hefðbundið snið rafrænnar skýrslugerðar

Fylgdu skrefunum í [Setja upp prentstýringu](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) til að skilgreina prentstýringu fyrir eininguna **Viðskiptakröfur** þannig að staðlað snið rafrænnar skýrslugerðar sé notað til a prenta reikninga með frjálsum texta.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Skilgreina sniðviðtökustað fyrir hefðbundið snið rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina áfangastað sniðs fyrir forskoðun á skjá](er-quick-start1-new-solution.md#ConfigureDestination) til að skilgreina áfangastað [Skjás](er-destination-type-screen.md) fyrir rafræna skýrslugerð á stöðluðu rafrænu skýrslugerðarsniði þannig að mynduðum skýrslum er umbreytt í PDF-snið og forskoðaðar í nýjum vafraglugga.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Prenta textareikning með því að nota staðlað snið rafrænnar skýrslugerðar

1. Fylgdu skrefunum í [Prenta textareikning](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) til að nota staðlað snið rafrænnar skýrslugerðar til að búa til textareikninga á Excel-sniði fyrir viðbætta reikninga.
2. Sæktu Excel-vinnubókina sem er mynduð og farðu yfir hana í Excel-skjáborðsforritinu.

    Taktu eftir að sjötta lína reikningsins byrjar á fyrstu síðu skýrslunnar og heldur áfram á næstu síðu. Síðasta athugasemdin birtist á annarri síðunni og það er ekki augljóst að hún tilheyri sjöttu reikningslínunni. Því er erfiðara að lesa efnið fyrir miðju reikningslínunnar í skjalinu út af síðuskilunum.

    ![Farið yfir síðuskiptingu myndaðs textareiknings í Excel-skjáborðsforritinu.](./media/er-keep-excel-rows-together-invoice1.gif)

Það sem eftir er af ferlum í þessari grein sýna þér hvernig hægt er að stilla staðlað snið rafrænnar skýrslugerðar til að bæta útlitið og læsileika reikningsskýrslunnar með því að halda efni fyrir eina reikningslínu á sömu blaðsíðunni.

## <a name="create-a-custom-format"></a>Búa til sérsniðið snið

Fylgdu skrefunum í [Búa til sérsniðið snið](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) til að útbúa snið úr innfluttu sniði rafrænnar skýrslugerðar og búa til skilgreiningu **Sérsniðinn textareikningur (Excel)** fyrir rafræna skýrslugerð sem er í boði til að breyta og laga.

## <a name="edit-the-custom-format"></a>Breyta sérstilltu sniði

1. Fylgdu skrefunum í [Búa til sérsniðið snið](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) til að opna afleitt snið rafrænnar skýrslugerðar til að gera breytingar í hönnuði rafræns skýrslugerðarsniðs.
2. Á síðunni **Sniðshönnuður**, í tré sniðsþáttar á vinstra svæðinu, skal stækka **Textareikningur \> Vinnublað \> InvoiceLines** og velja þáttinn **InvoiceLines_Values**.
3. Á flipanum **Snið** skal stilla valkostinn **Halda línum saman** á **Já**.

    ![Að stilla valkostinn Halda línum saman fyrir breytanlegt rafrænt skýrslugerðarsnið á síðu sniðshönnuðar.](./media/er-keep-excel-rows-together-format.png)

4. Veljið **Vista** og lokið skjámyndinni.

## <a name="mark-the-custom-format-as-runnable"></a>Merkja sérstillt snið sem keyranlegt

Fylgdu skrefunum í [Merkja sérsniðna sniðið sem keyranlegt](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) til að gera breytta útgáfu af sérsniðnu sniði rafrænnar skýrslugerðar keyranlegt.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Setja upp prentstýringu til að nota sérstillt snið rafrænnar skýrslugerðar

Fylgdu skrefunum í [Setja upp prentstýringu](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) til að skilgreina prentstýringu fyrir eininguna **Viðskiptakröfur** þannig að sérsniðið snið rafrænnar skýrslugerðar sé notað til a prenta reikninga með frjálsum texta.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Skilgreina sniðviðtökustað fyrir sérsniðið snið rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina áfangastað sniðs fyrir forskoðun á skjá](er-quick-start1-new-solution.md#ConfigureDestination) til að skilgreina áfangastað **Skjás** fyrir rafræna skýrslugerð á sérsniðnu rafrænu skýrslugerðarsniði þannig að mynduðum skýrslum er umbreytt í PDF-snið og forskoðaðar í nýjum vafraglugga.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Prenta textareikning með því að nota snið rafrænnar skýrslugerðar

1. Fylgdu skrefunum í [Prenta textareikning](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) til að nota sérsniðið snið rafrænnar skýrslugerðar til að búa til textareikninga á Excel-sniði fyrir viðbætta reikninga.
2. Sæktu Excel-vinnubókina sem er mynduð og farðu yfir hana í Excel-skjáborðsforritinu.

    Taktu eftir því að sjötta lína reikningsins byrjar á annarri síðu og allar Excel-línurnar sem tákna þessa reikningslínu birtast saman á þeirri síðu.

    ![Farið yfir uppfærða síðuskiptingu myndaðs textareiknings í Excel-skjáborðsforritinu.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Frekari upplýsingar

[Hanna skilgreiningu fyrir myndun skjala á Excel-sniði](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
