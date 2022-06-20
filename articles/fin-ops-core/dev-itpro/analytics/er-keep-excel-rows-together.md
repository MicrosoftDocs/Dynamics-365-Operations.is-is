---
title: Hanna ER-snið til að halda línum saman á sömu Excel-síðu
description: Þessi grein útskýrir hvernig á að hanna rafræna skýrslugerð (ER) sem heldur línum saman á sama stað Microsoft Excel síðu.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 98e6dd4f926908f65239f3e4f3608f9c9408f9d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8854670"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Hanna ER-snið til að halda línum saman á sömu Excel-síðu

[!include [banner](../includes/banner.md)]


Þessi grein útskýrir hvernig notandi í hlutverki kerfisstjóra eða rafrænnar skýrslugerðar virkur ráðgjafi getur stillt [Rafræn skýrslugerð (ER)](general-electronic-reporting.md)[sniði](er-overview-components.md#format-component) sem býr til skjöl á útleið inn Microsoft Excel og stjórna blaðsíðuflokkun skjala þannig að raðir sem eru búnar til haldist á sömu síðu.

Í þessu dæmi muntu breyta ER-sniði frá Microsoft sem er notað til að prenta ókeypis textareikninga í Excel. Breytingarnar þínar munu gera þér kleift að stjórna blaðsíðuskipun á myndaðri reikningsskýrslu með frjálsum texta þannig að allar línur í einni reikningslínu haldist á sömu síðu þegar mögulegt er.

Verklagsreglurnar í þessari grein er hægt að ljúka í **USMF** fyrirtæki. Ekki er þörf á neinni kóðun.

Í þessu dæmi muntu búa til nauðsynlega ER [stillingar](general-electronic-reporting.md#Configuration) fyrir **Litware, Inc.** sýnishorn fyrirtæki. Gakktu úr skugga um að stillingarveitan fyrir **Litware, Inc.** (`http://www.litware.com`) sýnishornsfyrirtæki er skráð fyrir ER ramma og að það sé merkt sem **Virkur**. Ef þessi stillingarveita er ekki á listanum eða ef hún er ekki merkt sem **Virkur**, fylgdu skrefunum í [Búðu til stillingarveitu og merktu hana sem virkan](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Sláðu inn nýjan ókeypis textareikning

1. Fylgdu skrefunum í [Búðu til ókeypis textareikning](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) til að bæta við ókeypis textareikningi.

    1. Bættu einni línu við reikninginn.
    2. Bættu við fimm athugasemdum fyrir reikningslínuna.

    ![Farið yfir athugasemdir reikningslínunnar á síðunni Viðhengi.](./media/er-keep-excel-rows-together-notes.png)

2. Fylgdu skrefunum í [Afritaðu línur](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) til að búa til fimm viðbótarreikningslínur sem eru afritar reikningslínuna sem þú bættir við í fyrra skrefi.

    ![Skoðaðu reikningslínur með frjálsum texta á síðunni Frjáls textareikningur.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>Skilgreina ramma rafrænnar skýrslugerðar

Fylgdu skrefunum í [Skilgreina ramma rafrænnar skýrslugerðar](er-quick-start2-customize-report.md#ConfigureFramework) til að setja upp lágmarksfjölda af færibreytum rafrænnar skýrslugerðar. Þú verður að ljúka þessari uppsetningu áður en þú byrjar að nota ramma rafrænnar skýrslugerðar til að hanna sérsniðna útgáfu af stöðluðu sniði rafrænnar skýrslugerðar.

## <a name="import-the-standard-er-format-configuration"></a>Flytja inn staðlaða skilgreiningu rafræns skýrslugerðarsniðs

Fylgdu skrefunum í [Flytja inn staðlaða ER sniðstillingu](er-quick-start2-customize-report.md#ImportERSolution1) til að bæta stöðluðum ER stillingum við núverandi tilvik þitt af Dynamics 365 Finance. Til dæmis, innflutningsútgáfa **252.116** af **Ókeypis textareikningur (Excel)** sniðstillingar. Grunnútgáfa **252** af grunninum **Reikningslíkan** stillingar eru sjálfkrafa fluttar inn úr geymslunni ásamt nauðsynlegum **Kortlagning reikningslíkana** stillingar.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Settu upp prentstjórnun til að nota staðlað ER snið

Fylgdu skrefunum í [Settu upp prentstjórnun](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) til að stilla prentstjórnun fyrir **Reikningur fáanlegur** mát þannig að staðlað ER snið er notað til að prenta reikninga með frjálsum texta.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Stilltu snið áfangastað fyrir staðlað ER snið

Fylgdu skrefunum í [Stilltu áfangastað fyrir snið fyrir forskoðun á skjánum](er-quick-start1-new-solution.md#ConfigureDestination) til að stilla [Skjár](er-destination-type-screen.md) ER áfangastaður staðlaðs ER sniðs þannig að útbúnum skýrslum er breytt í PDF snið og forskoðað á nýjum vafraflipa.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Prenta textareikning með því að nota staðlað snið rafrænnar skýrslugerðar

1. Fylgdu skrefunum í [Prentaðu ókeypis textareikning](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) að nota staðlað ER snið til að búa til reikningsskýrslu með frjálsum texta á Excel sniði fyrir reikninginn sem bætt er við.
2. Sæktu útbúna Excel vinnubókina og skoðaðu hana í Excel skjáborðsforritinu.

    Taktu eftir að sjötta lína reikningsins byrjar á fyrstu síðu skýrslunnar og heldur áfram á annarri síðu. Síðasta athugasemdin birtist á annarri síðu og það er ekki augljóst að hún tilheyri sjöttu reikningslínunni. Þess vegna gerir síðuskil í miðju innihaldi reikningslínunnar þetta skjal erfiðara að lesa.

    ![Farið yfir blaðsíðuskiptingu myndaðs ókeypis textareiknings í Excel skjáborðsforritinu.](./media/er-keep-excel-rows-together-invoice1.gif)

Aðferðirnar sem eftir eru í þessari grein sýna hvernig hægt er að stilla staðlaða ER sniðið til að bæta útlit og læsileika reikningsskýrslunnar með því að halda öllu innihaldi einni reikningslínu á sömu síðu.

## <a name="create-a-custom-format"></a>Búa til sérsniðið snið

Fylgdu skrefunum í [Búðu til sérsniðið snið](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) að draga snið úr innfluttu ER sniðinu og búa til a **Ókeypis textareikningur (Excel) sérsniðinn** ER stillingar sem hægt er að breyta og breyta.

## <a name="edit-the-custom-format"></a>Breyta sérstilltu sniði

1. Fylgdu skrefunum í [Búðu til sérsniðið snið](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) til að opna afleitt ER snið til að breyta í ER sniðhönnuðinum.
2. Á **Sniðhönnuður** síðu, í sniðihlutatrénu í vinstri glugganum, stækkaðu **Ókeypis textareikningur \> Blað \> InvoiceLines**, og veldu **InvoiceLines_Values** hluti.
3. Á **Snið** flipann, stilltu **Haltu röðum saman** valmöguleika til **Já**.

    ![Stilling á Halda röðum saman valmöguleikanum fyrir breytanlegt ER snið á Format hönnuður síðunni.](./media/er-keep-excel-rows-together-format.png)

4. Veljið **Vista** og lokið skjámyndinni.

## <a name="mark-the-custom-format-as-runnable"></a>Merkja sérstillt snið sem keyranlegt

Fylgdu skrefunum í [Merktu sérsniðna sniðið sem keyranlegt](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) til að gera breytta útgáfu af sérsniðnu ER sniði keyranlega.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Settu upp prentstjórnun til að nota sérsniðið ER snið

Fylgdu skrefunum í [Settu upp prentstjórnun](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) til að stilla prentstjórnun fyrir **Reikningur fáanlegur** mát þannig að sérsniðið ER snið er notað til að prenta reikninga með frjálsum texta.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Stilltu snið áfangastað fyrir sérsniðna ER sniðið

Fylgdu skrefunum í [Stilltu áfangastað fyrir snið fyrir forskoðun á skjánum](er-quick-start1-new-solution.md#ConfigureDestination) til að stilla **Skjár** ER áfangastaður sérsniðna ER sniðsins þannig að útbúnum skýrslum er breytt í PDF snið og forskoðað á nýjum vafraflipa.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Prenta textareikning með því að nota snið rafrænnar skýrslugerðar

1. Fylgdu skrefunum í [Prentaðu ókeypis textareikning](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) til að nota sérsniðna ER sniðið til að búa til reikningsskýrslu með frjálsum texta á Excel sniði fyrir bættan reikning.
2. Sæktu útbúna Excel vinnubókina og skoðaðu hana í Excel skjáborðsforritinu.

    Taktu eftir að sjötta lína reikningsins byrjar á annarri síðu og allar Excel línur sem tákna þessa reikningslínu birtast saman á þeirri síðu.

    ![Farið yfir uppfærða blaðsíðugerð myndaðs reiknings með frjálsum texta í Excel skjáborðsforritinu.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Frekari upplýsingar

[Hanna skilgreiningu fyrir myndun skjala á Excel-sniði](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
