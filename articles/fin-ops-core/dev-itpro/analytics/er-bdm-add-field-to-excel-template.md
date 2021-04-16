---
title: Bættu nýjum reit við sniðmát viðskiptaskjala í Microsoft Excel
description: Þetta efni veitir upplýsingar um hvernig bæta má nýjum reitum við sniðmát viðskiptaskjala í Microsoft Excel með því að nota viðskiptaskjalastjórnunaraðgerð.
author: NickSelin
ms.date: 11/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters, ERBDTemplateEditor
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 991fe4ea56a2726c5df835cfc90a390cef2d5df5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751131"
---
# <a name="add-new-fields-to-a-business-document-template-in-microsoft-excel"></a>Bættu nýjum reit við sniðmát viðskiptaskjala í Microsoft Excel

[!include[banner](../includes/banner.md)]

Þú getur bætt nýjum reitum við sniðmát sem er notað til að búa til viðskiptaskjöl á Microsoft Excel sniði. Þessum reitum er hægt að bæta við sem frátökurum sem eru notaðir til að fylla mynda skjöl með nauðsynlegum upplýsingum úr forritinu. Fyrir alla reiti sem þú bætir við geturðu einnig tilgreint bindingu gagnagjafa til að tilgreina hvaða forritsgögn verða færð inn í reitinn þegar sniðmátið er notað til að búa til viðskiptaskjöl.

Til að fá frekari upplýsingar um þennan eiginleika skaltu ljúka dæminu í þessu efni. Þetta dæmi sýnir hvernig á að uppfæra sniðmát til að fylla út reitina í skjámyndum textareikninga sem eru búnir til.

## <a name="configure-business-document-management-to-edit-templates"></a>Skilgreina stjórnun viðskiptaskjala til að breyta sniðmátum

Vegna þess að viðskiptaskjalastjórnun (BDM) er byggð ofan á rammann [Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md) verður þú að stilla nauðsynlegar færibreytur ER og BDM áður en þú getur byrjað að vinna með BDM.

1.  Skráðu þig inn á Microsoft Dynamics 365 Finance sem kerfisstjóri.
2.  Ljúktu eftirfarandi skrefum í dæminu í efninu [Yfirlit yfir viðskiptaskjöl stjórnun](er-business-document-management.md):

    1.  Skilgreina færibreytur Rafræn skýrslugerðar.
    2.  Kveiktu á BDM.

Þú getur nú byrjað að nota BDM til að breyta sniðmátum fyrir viðskiptaskjöl.

## <a name="import-er-solutions-that-contain-a-template"></a>Flytja inn ER lausnir sem innihalda sniðmát

Dæmið í þessari aðferð notar opinberlega útgefnu ER lausnina. Þú verður að flytja ER stillingar þessarar lausnar inn í núverandi tilvik þitt af Finance.

Skilgreining ER-sniðs **Ókeypis textareikningur (Excel)** þessarar lausnar inniheldur sniðmát viðskiptaskjala á Excel sniði sem hægt er að breyta með BDM. Flytja inn nýjustu útgáfuna af þessu ER sniði frá Microsoft Dynamics Lifecycle Service (LCS). Samsvarandi ER gagnalíkan og skilgreiningar ER-líkanavörpunar verða fluttar inn sjálfkrafa.

Nánari upplýsingar um hvernig eigi að flytja inn ER-skilgreininga er að finna í [Stjórna líftíma ER-stillinga](general-electronic-reporting-manage-configuration-lifecycle.md).

![Síðan LCS samnýtt eignasafn](./media/BDM-AddFldExcel-LCS.png)

### <a name="edit-the-er-solution-template"></a>Breyta sniðmát fyrir ER lausn

1.  Skráðu þig inn sem notandi sem hefur aðgang að vinnusvæðinu **Stjórnun viðskiptaskjala**.
2.  Opnaðu vinnusvæðið **Stjórnun viðskiptaskjala**.

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala](./media/BDM-AddFldExcel-Workspace.png)

3.  Í tölfunni velurðu sniðmátið **Ókeypis textareikningur (Excel)**.
4.  Í hægri glugganum velurðu **Nýtt sniðmát** til að búa til nýtt sniðmát sem byggist á völdu sniðmáti.
5.  Í reitinn **Titill** slærðu inn **Ókeypis textareikningur (Excel) Contoso** sem yfirskrift nýja sniðmátsins.
6.  Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

Síðan BDM-sniðmátsritill birtist. Hægt er að nota Microsoft 365 til að breyta völdu sniðmáti á netinu í innbyggðu stýringunni.

![BDM ritilssíða](./media/BDM-AddFldExcel-EditableTemplate.png)

### <a name="add-the-label-for-a-new-field-to-the-template"></a>Bættu merkimiðanum fyrir nýjan reit við sniðmátið

1.  Á ritstjórasíðu BDM sniðmáts, á Excel borði, á flipanum **Útsýni**, velurðu gátreitina **Fyrirsagnir og hnitanet** fyrir breytilegt Excel sniðmát.

    ![Gátreitirnir Fyrirsagnir og hnitanet valdir](./media/BDM-AddFldExcel-EditableTemplate2.png)

2.  Veldu hólf **E8:F8**.
3.  Á Excel-borðanum, á flipanum **Heim**, velurðu **Sameina og miðja** til að sameina valda reiti í nýjan sameinaðan reit **E8:F8**.
4.  Í sameinaða reitnum **E8:F8** slærðu inn **Vefslóð**.
5.  Veldu sameinaðan reit **E7:F7**, veldu **Sniðmálari** og veldu síðan sameinaðan reit **E8:F8** til að forsníða hann á sama hátt og sameinaða reitinn **E7:F7**.

    ![Nýjum reitamerkimiða bætt við sniðmátið](./media/BDM-AddFldExcel-EditableTemplate3.png)

### <a name="format-the-template-to-reserve-space-for-a-new-field"></a>Sníddu sniðmátið til að taka frá pláss fyrir nýjan reit

1.  Á ritilsíðu BDM sniðmáts velurðu sameinaðan reit **G8:H8**.
2.  Á Excel-borðanum, á flipanum **Heim**, velurðu **Sameina og miðja** til að sameina valda reiti í nýjan sameinaðan reit **G8:H8**.
3.  Veldu sameinaðan reit **G7:H7**, veldu **Sniðmálari** og veldu síðan sameinaðan reit **G8:H8** til að forsníða hann á sama hátt og sameinaða reitinn **G7:H7**.

    ![Rými frátekið fyrir nýja reitinn](./media/BDM-AddFldExcel-EditableTemplate4.png)

4.  Í reitinn **Heiti** velurðu **CompanyInfo**.

    Svið **CompanyInfo** núverandi Excel sniðmáts geymir alla reitina sem eru notaðir til að fylla haus á myndaða skýrslu með upplýsingum um núverandi fyrirtæki sem seljanda.

    ![CompanyInfo svið valið](./media/BDM-AddFldExcel-SelectCompanyInfoRange.png)

### <a name="add-a-new-field-to-the-template"></a>Bæta nýjum reit við sniðmátið

1.  Á síðunni **Ritill BDM sniðmáts**, í aðgerðarglugganum, velurðu **Sýna snið**.
2.  Í glugganum **Uppbygging sniðmáts** velurðu **Bæta við**.

    > [!NOTE]
    > Þú verður að aðlaga hluta sniðmátsins sem þú vilt nota sem nýjan reit. Þú hefur þegar gert þessa leiðréttingu með því að forsníða sameinaða reitinn **G8:H8**.

    ![Nýjum reit bætt við sniðmátið](./media/BDM-AddFldExcel-AddCell.png)

3.  Veldu **Excel\Cell** til að bæta við nýjum reit sem reit í sniðmátinu.

    Þú getur valið **Excel\Range** ef þú vilt bæta nýju svið við sniðmátið. Sviðið sem er slegið inn getur innihaldið marga reiti. Þú getur bætt þessum reitum við síðar.
    
    Taktu eftir að sniðmátshlutinn **CompanyInfo** er sjálfkrafa valinn í glugganum **Uppbygging sniðmáts** vegna þess að það er heppilegasti foreldrahlutinn í núverandi sniðmátbyggingu fyrir reitinn sem þú ert að bæta við.
    
4.  Í reitinn **Excel-svið** reit slærðu inn **CompanyURL_Value**.
5.  Veljið **Í lagi**.

    ![CompanyURL_Value sviði bætt við sniðmátaskipan](./media/BDM-AddFldExcel-EditableTemplate5.png)

6.  Í glugganum **Uppbygging sniðmáts** velurðu úrfellingarhnappinn (...) og velur síðan **Sýna bindingar**.

    ![Sýna valdar bindingar](./media/BDM-AddFldExcel-ShowBindings.png)

    Glugginn **Uppbygging sniðmáts** sýnir nú gagnagjafana sem eru fáanlegir á undirliggjandi ER sniði.

7.  Veldu **CompanyInfo_Value** sem reitinn sem þú ætlar að binda við gagnagjafa af undirliggjandi ER sniði.
8.  Í hlutanum **Gagnagjafar** í glugganum **Uppbygging sniðmáts** stækkarðu **Model \> InvoiceBase \> CompanyInfo**.
9.  Undir **CompanyInfo** velurðu liðinn **WebsiteURI**.

    ![Liðurinn WebsiteURI valið](./media/BDM-AddFldExcel-BindURL.png)

10. Veldu **Binda**.
11. Í glugganum **Uppbygging sniðmáts** velurðu **Vista** og lokar síðan ritilssíðu BDM sniðmáts.

Á vinnusvæðinu **Stjórnun viðskiptaskjala** sýnir flipinn **Sniðmát** í hægri glugganum uppfærða sniðmátið. Í netinu skaltu taka eftir því að reitnum **Staða** fyrir breytt sniðmát hefur verið breytt í **Drög** og að reiturinn **Endurskoðun** er ekki lengur auður. Þessar breytingar benda til þess að ferlið við að breyta þessu sniðmáti er hafið.

![Breytt sniðmát í vinnusvæðinu Stjórnun viðskiptaskjala](./media/BDM-AddFldExcel-Workspace2.png)

## <a name="review-company-settings"></a>Yfirfara fyrirtækjastillingar

1.  Farðu í **Fyrirtækisstjórnun \> Fyrirtæki \> Lögaðilar**.
2.  Á flýtiflipanum **Upplýsingar um tengiliði** staðfestirðu að vefslóð fyrirtækisins sé slegin inn.

![Vefslóð fyrirtækisins slegin inn á síðu Lögaðila](./media/BDM-AddFldExcel-CompanyInfo.png)

## <a name="generate-business-documents-to-test-the-updated-template"></a>Búðu til viðskiptaskjöl til að prófa uppfærða sniðmátið

1.  Í forritinu skal breyta fyrirtækinu í **USMF** og fara í **Viðskiptakröfur \> Reikningar \> Allir textareikningar**.
2.  Veldu reikninginn **FTI-00000002** og síðan **Prentstjórnun**.
3.  Stækkaðu í vinstri glugganum **Eining - viðskiptakröfur \> Skjöl \> Textareikningur**.
4.  Undir **Textareikningur** velurðu **Upprunalegt skjal** til að tilgreina umfang reikninga til vinnslu.
5.  Í hægri glugganum, í reitnum **Skýrslusnið**, velurðu sniðmátið **Textareikningur (Excel) Contoso** fyrir tilgreint skjalastig.

    ![Sniðmátið Textareikningur (Excel) Contoso valið](./media/BDM-AddFldExcel-PrintMngtSetting.png)

6.  Ýttu á **Esc** til að loka núverandi síðu.
7.  Veldu **Prenta \> Valið**.
8.  Sæktu skjalið sem myndað var og opnaðu það í Excel.

    ![Textareikningur í Excel](./media/BDM-AddFldExcel-PreviewReport.png)

Breytta sniðmátið er notað til að mynda skýrslu reiknings með frjálsum texta fyrir valinn hlut. Til að greina hvernig þessi skýrsla hefur áhrif á breytingarnar sem eru gerðar á sniðmátinu skaltu keyra þessa skýrslu í einni forritslotu strax eftir að þú breytir sniðmátinu í annarri forritslotu.

## <a name="related-links"></a>Skyldir tenglar

[Yfirlit yfir rafræna skýrslugerð (ER)](general-electronic-reporting.md)

[Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md)

[Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði](tasks/er-design-reports-openxml-2016-11.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]