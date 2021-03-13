---
title: Hanna skilgreiningu fyrir myndun skjala á Excel-sniði
description: Í þessu efni er útskýrt hvernig á að hanna snið rafrænnar skýrslugerðar til að fylla út Excel-sniðmát og síðan mynda skjöl á Excel-sniði á útleið.
author: NickSelin
manager: AnnBe
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8d6a18741d57829d1929fb8362dc4ba8e03a1bd
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094030"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Hanna skilgreiningu fyrir myndun skjala á Excel-sniði

[!include[banner](../includes/banner.md)]

Hægt er að hanna skilgreiningu [rafræns skýrslugerðarsniðs (ER)](general-electronic-reporting.md) sem er með [sniðsþátt](general-electronic-reporting.md#FormatComponentOutbound) rafrænnar skýrslugerðar sem hægt er að skilgreina til að mynda skjal á útleið á Microsoft Excel-vinnubókarsniði. Nota verður tiltekna sniðsþætti rafrænnar skýrslugerðar í þessum tilgangi.

Til að læra meira um þennan eiginleika skal fylgja skrefunum í efnisatriði [Hanna skilgreiningu fyrir myndun skýrslna í OPENXML-sniði](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Bæta við nýju sniði rafrænnar skýrslugerðar

Þegar skilgreiningu nýs sniðs rafrænnar skýrslugerðar er bætt við til að mynda skjal á útleið á Excel-vinnubókarsniði verður annaðhvort að velja **Excel**-gildið fyrir eigindina **Sniðsgerð** fyrir sniðið eða hafa eigindina **Sniðsgerð** auða.

- Ef **Excel** er valið er hægt að skilgreina sniðið til að mynda skjal á útleið aðeins á Excel-sniði.
- Ef eigindin er höfð auð er hægt að skilgreina sniðið til að mynda skjal á útleið á hvaða því sniði sem rafræna skýrslugerðin styður.

Til að skilgreina sniðsþátt rafrænnar skýrslugerðar skal velja **Hönnuður** á aðgerðasvæðinu og opna sniðsþátt rafrænnar skýrslugerðar fyrir breytingar í aðgerðarhönnuði rafrænnar skýrslugerðar.

![Skilgreiningasíða](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel-skrárþáttur

### <a name="manual-entry"></a>Handvirk færsla

Bæta þarf þætti **Excel\\-skráar** við skilgreint snið rafrænnar skýrslugerðar til að mynda skjal á útleið á Excel-sniði.

![Excel\skráarþáttur](./media/er-excel-format-add-file-component.png)

Til að tilgreina útlit skjals á útleið skal hengja Excel-vinnubók með .xlsx skrárendingu við þátt **Excel\\-skrárinnar** sem sniðmát fyrir skjöl á útleið.

> [!NOTE]
> Þegar sniðmát er handvirkt hengt við þarf að nota [gerð skjals](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) sem hefur verið skilgreind í þeim tilgangi í [færibreytum rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Viðhengi bætt við Excel\skráarþátt](./media/er-excel-format-add-file-component2.png)

Til að tilgreina hvernig viðhengt sniðmát er fyllt út þegar skilgreint snið rafrænnar skýrslugerðar er keyrt þarf að bæta við földuðum þáttum **vinnublaðs**, **sviðs** og **hólfs** í þætti **Excel\\-skráar**. Hver faldaður þáttur þarf að vera tengdur við Excel-vöru.

### <a name="template-import"></a>Sniðmátsinnflutningur

Hægt er að velja **Flytja inn úr Excel** á flipanum **Innflutningur** á aðgerðasvæðinu til að flytja nýtt sniðmát inn í autt snið rafrænnar skýrslugerðar. Í þessu dæmi er þáttur **Excel\\-skráar** stofnaður sjálfkrafa og innflutta sniðmátið verður hengt við hann. Allir nauðsynlegir þættir rafrænnar skýrslugerðar verða einnig stofnaðir sjálfkrafa, samkvæmt lista yfir greindar Excel-vörur.

![Val á „Flytja inn úr Excel“](./media/er-excel-format-import-template.png)

> [!NOTE]
> Ef stofna á valfrjálsa einingu fyrir **Vinnublað** á breytanlegu sniði rafrænnar skýrslugerðar þarf að stilla valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já**.

## <a name="sheet-component"></a>Vinnublaðsþáttur

Þátturinn **Vinnublað** gefur til kynna vinnublað viðhengdu Excel-vinnubókarinnar sem þarf að fylla út. Heiti vinnublaðs í Excel-sniðmáti er skilgreint í eiginleikanum **Vinnublað** fyrir þennan þátt.

> [!NOTE]
> Þessi þáttur er valfrjáls fyrir Excel-vinnubækur sem innihalda eitt vinnublað.

Á flipanum **Vörpun** í aðgerðarhönnuði rafrænnar skýrslugerðar er hægt að skilgreina eiginleikann **Virkt** fyrir þátt af gerðinni **Vinnublað** til að tilgreina hvort setja þurfi þátt í myndað skjal:

- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rétt** í keyrslu eða ef engin segð er skilgreind, verður viðeigandi vinnublað sett í myndaða skjalið.
- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu mun myndaða skjalið ekki innihalda vinnublað.

![Dæmi um vinnublaðsþátt](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Sviðsþáttur

Þátturinn **Svið** gefur til kynna Excel-svið sem þessi þáttur rafrænnar skýrslugerðar þarf að stýra. Heiti sviðsins er skilgreint í eiginleikanum **Excel-svið** fyrir þennan þátt.

Eiginleikinn **Eftirlíkingarátt** tilgreinir hvort og hvernig svið verður endurtekið í mynduðu skjali:

- Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Engin eftirlíking** verður viðeigandi Excel-svið ekki endurtekið í myndaða skjalinu.
- Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Lóðrétt** verður viðeigandi Excel-svið endurtekið í myndaða skjalinu. Hvert endurtekið svið er sett undir upprunalega sviðið í Excel-sniðmáti. Fjöldi endurtekninga er skilgreindur af fjölda færslna í gagnagjafa af gerðinni **Færslulisti** sem er bundin þessum þætti rafrænnar skýrslugerðar.
- Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Lárétt** verður viðeigandi Excel-svið endurtekið í myndaða skjalinu. Hvert endurtekið svið er sett til hægri við upprunalega sviðið í Excel-sniðmáti. Fjöldi endurtekninga er skilgreindur af fjölda færslna í gagnagjafa af gerðinni **Færslulisti** sem er bundin þessum þætti rafrænnar skýrslugerðar.

Frekari upplýsingar um lárétta eftirlíkingu er að hægt að nálgast með því að fylgja skrefunum í [Nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum](tasks/er-horizontal-1.md).

Þátturinn **Svið** getur verið með aðra faldaða þætti rafrænnar skýrslugerðar sem eru notaðir til að færa inn gildi í viðeigandi Excel-svið.

- Ef þáttur í flokknum **Texti** er notaður til að færa inn gildi er gildið fært inn í Excel-svið sem textagildi.

    > [!NOTE]
    > Notið þetta mynstur til að sníða innfærð gildi út frá landsstaðlinum sem er skilgreindur í forritinu.

- Ef þátturinn **Hólf** í flokknum **Excel** er notaður til að færa inn gildi er gildið fært inn í Excel-svið sem gildi gagnagerðar sem er skilgreind af bindingum viðkomandi **Hólf**-þáttar (til dæmis **Strengur**, **Raunverulegt** eða **Heiltala**).

    > [!NOTE]
    > Notið þetta mynstur til að virkja Excel-forritið til að sníða innfærð gildi út frá landsstaðli tölvunnar sem opnar skjal á útleið.

Á flipanum **Vörpun** í aðgerðarhönnuði rafrænnar skýrslugerðar er hægt að skilgreina eiginleikann **Virkt** fyrir þátt af gerðinni **Svið** til að tilgreina hvort setja þurfi þátt í myndað skjal:

- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rétt** í keyrslu eða ef engin segð er skilgreind, verður viðeigandi svið sett í myndaða skjalið.
- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu, og ef þetta svið stendur ekki fyrir allar línur eða dálka, verður viðeigandi svið ekki fyllt út í mynduðu skjalið.
- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu, og ef þetta svið stendur fyrir allar línur eða dálka, mun myndaða skjalið innihalda þessar línur og dálka sem faldar línur og falda dálka.

## <a name="cell-component"></a>Þáttur hólfs

Þátturinn **Hólf** er notaður til að fylla út Excel-hólf, form og myndir. Til að gefa til kynna Excel-hlut sem þarf að fylla út með þættinum **Hólf** fyrir rafræna skýrslugerð þarf að tilgreina heiti þess hlutar í eiginleikanum **Excel-svið** fyrir þáttinn **Hólf**.

Á flipanum **Vörpun** í aðgerðarhönnuði rafrænnar skýrslugerðar er hægt að skilgreina eiginleikann **Virkt** fyrir þátt af gerðinni **Hólf** til að tilgreina hvort fylla þurfi hlutinn út í mynduðu skjali:

- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rétt** í keyrslu eða ef engin segð er skilgreind, verður viðeigandi hlutur settur í myndaða skjalið. Binding fyrir þennan **Hólf**-þátt tilgreinir gildi sem er sett í viðeigandi hlut.
- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu verður viðeigandi hlutur ekki fylltur út í myndaða skjalinu.

Þegar þátturinn **Hólf** er skilgreindur á að færa inn gildi í hólf er hægt að binda hann við gagnagjafa sem skilar gildi frumstæðrar gagnagerðar (til dæmis **Strengur**, **Raunverulegt** eða **Heiltala**). Í þessu tilviki er gildið fært inn í hólfið sem gildi sömu gagnagerðar.

Þegar þátturinn **Hólf** er skilgreindur á að færa inn gildi í Excel-form er hægt að binda hann við gagnagjafa sem skilar gildi frumstæðrar gagnagerðar (til dæmis **Strengur**, **Raunverulegt** eða **Heiltala**). Í þessu tilviki er gildið fært inn í Excel-formið sem texti á því formi. Fyrir gildi gagnagerða sem eru ekki **Strengur** er sjálfkrafa breytt í texta.

> [!NOTE]
> Hægt er að skilgreina þáttinn **Hólf** til að fylla aðeins út form í tilvikum þar sem eiginleiki formtexta er studdur.

Þegar þátturinn **Hólf** er skilgreindur á að færa inn gildi í Excel-mynd er hægt að binda hann við gagnagjafa sem skilar gildi gagnagerðarinnar **Geymsla** sem stendur fyrir mynd á tvíundarsniði. Í þessu tilviki er gildið slegið inn í Excel-mynd sem mynd.

> [!NOTE]
> Sérhver Excel-mynd og -form er talin vera fest á efra horni til vinstri við tiltekið Excel-hólf eða -svið. Ef ætlunin er að endurtaka Excel-mynd eða -form þarf að skilgreina hólfið eða sviðið sem það er fest við sem endurtekið hólf eða svið.

Frekari upplýsingar um hvernig á að fella inn myndir og form eru í [Fella inn myndir og form í skjöl sem búin eru til með rafrænni skýrslugerð](electronic-reporting-embed-images-shapes.md).

## <a name="page-break-component"></a>Síðuskilaþáttur

Þátturinn **PageBreak** þvingar Excel til að byrja nýja síðu. Ekki þarf að nota þennan þátt þegar nota á sjálfgefið blaðsíðutal Excel en mælt er að hann sé notaður þegar Excel á að fylgja viðkomandi sniði rafrænnar skýrslugerðar við blaðsíðutal.

## <a name="edit-an-added-er-format"></a>Breyta sniði rafrænnar skýrslugerðar sem bætt er við

### <a name="update-a-template"></a>Uppfæra sniðmát

Hægt er að velja **Uppfæra úr Excel** á flipanum **Innflutningur** á aðgerðasvæðinu til að flytja uppfært sniðmát inn í breytanlegt snið rafrænnar skýrslugerðar. Á meðan á þessu stendur er sniðmáti af valinni einingu **Excel\\skrá** skipt út fyrir nýtt sniðmát. Efni breytanlegs sniðs rafrænnar skýrslugerðar verður samstillt við efni með uppfærðs sniðmáts rafrænnar skýrslugerðar.

- Nýr sniðsþáttur rafrænnar skýrslugerðar verður sjálfkrafa stofnaður fyrir hvert Excel-heiti ef sniðsþáttur rafrænnar skýrslugerðar finnst ekki í breytanlega sniðinu.
- Öllum sniðsþáttum rafrænnar skýrslugerðar verður eytt úr breytanlegu sniði rafrænnar skýrslugerðar ef viðeigandi Excel-heiti finnst ekki fyrir það.

> [!NOTE]
> Stilla þarf valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já** ef stofna á valfrjálsa **Skjal** einingu á breytanlegu sniði rafrænnar skýrslugerðar.
>
> Ef breytanlegu sniði rafrænnar skýrslugerðar, var upphaflega í einingunum **Vinnublað** er mælt með því að stilla valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já** þegar flutt er inn uppfært sniðmát. Að öðrum kosti verða allar faldaðar einingar upprunalegu einingarinnar **Vinnublað** búnar til frá grunni. Af þeim ástæðum glatast allar bindingar endurstofnaðra sniðseininga í uppfærðu sniði rafrænnar skýrslugerðar.

![Valkosturinn „Stofna sniðseiningu Excel-vinnublaðs“ í svarglugganum Uppfæra úr Excel](./media/er-excel-format-update-template.png)

Til að fá frekari upplýsingar um þennan eiginleika skal fylgja skrefunum í [Breyta rafrænum skýrslugerðarsniðum með því að endurnýta Excel-sniðmát](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Villuleita snið rafrænnar skýrslugerðar

Þegar snið rafrænnar skýrslugerðar sem hægt er að breyta er sannprófað er samræmisathugun framkvæmd til að ganga úr skugga um að Excel-heitið sé til staðar í Excel-sniðmátinu sem er í notkun. Þú munt fá tilkynningu ef ósamræmi kemur upp. Boðið er upp á valkost til að lagfæra sum vandamál sjálfkrafa.

![Staðfestingarvilluboð](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Stjórnun útreiknings Excel-formúla

Þegar skjal á útleið á Microsoft Excel -vinnubókarsniði er myndað kunna tiltekin hólf þessa skjals að innihalda Excel-formúlur. Þegar eiginleikinn **Virkja notkun á EPPlus-safni í rafrænum skýrslugerðarramma** er virkur getur þú stjórna hvenær formúlurnar eru reiknaðar út með því að breyta gildi **færibreytunnar** [Valkostir útreikninga](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) í Excel-sniðmátinu sem verið er að nota:

- Veljið **Automatic** til að endurreikna allar háðar formúlur í hvert sinn sem ný svið, hólf o.s.frv. er bætt við myndað skjal.
    >[!NOTE]
    > Þetta gæti valdið afkastavandamálum í Excel-sniðmátum sem innihalda margar tengdar formúlur.
- Veljið **Handvirk** til að forðast endurreikning formúlu þegar skjal er myndað.
    >[!NOTE]
    > Endurútreikningur formúlu er þvingaður handvirkt þegar myndað skjal er opnað í forskoðun með Excel.
    > Ekki nota þennan valkost ef áfangastaður rafrænnar skýrslugerðar er skilgreindur sem gerir ráð fyrir notkun á mynduðu skjali án forskoðunar þess í Excel (PDF-umbreyting, sending í tölvupósti o.s.frv.) vegna þess að skjalið sem var myndað inniheldur hugsanlega ekki gildi í hólfum sem innihalda formúlur.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði](tasks\er-design-reports-openxml-2016-11.md)

[Breyta rafrænum skýrslugerðarsniðum með því að endurnýta Excel-sniðmát](modify-electronic-reporting-format-reapply-excel-template.md)

[Nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum](tasks/er-horizontal-1.md)

[Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md)

[Skilgreina rafræna skýrslugerð (ER) til að draga gögn inn í Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)
