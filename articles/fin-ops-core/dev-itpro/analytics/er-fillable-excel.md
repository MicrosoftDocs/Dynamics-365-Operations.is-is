---
title: Hanna skilgreiningu fyrir myndun skjala á Excel-sniði
description: Í þessu efni er útskýrt hvernig á að hanna snið rafrænnar skýrslugerðar til að fylla út Excel-sniðmát og síðan mynda skjöl á Excel-sniði á útleið.
author: NickSelin
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ebe2647bb382421921aa6ffc733953f379a8af10
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2021
ms.locfileid: "7890866"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Hanna skilgreiningu fyrir myndun skjala á Excel-sniði

[!include[banner](../includes/banner.md)]

Þú getur hannað an [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) sniðstillingar sem hefur ER sniðshluta sem þú getur stillt til að búa til skjal á útleið í a Microsoft Excel vinnubókarsniði. Nota verður tiltekna sniðsþætti rafrænnar skýrslugerðar í þessum tilgangi.

Til að læra meira um þennan eiginleika skal fylgja skrefunum í efnisatriði [Hanna skilgreiningu fyrir myndun skýrslna í OPENXML-sniði](tasks/er-design-reports-openxml-2016-11.md).

## <a name="add-a-new-er-format"></a>Bæta við nýju sniði rafrænnar skýrslugerðar

Þegar skilgreiningu nýs sniðs rafrænnar skýrslugerðar er bætt við til að mynda skjal á útleið á Excel-vinnubókarsniði verður annaðhvort að velja **Excel**-gildið fyrir eigindina **Sniðsgerð** fyrir sniðið eða hafa eigindina **Sniðsgerð** auða.

- Ef **Excel** er valið er hægt að skilgreina sniðið til að mynda skjal á útleið aðeins á Excel-sniði.
- Ef eigindin er höfð auð er hægt að skilgreina sniðið til að mynda skjal á útleið á hvaða því sniði sem rafræna skýrslugerðin styður.

Til að skilgreina sniðsþátt rafrænnar skýrslugerðar skal velja **Hönnuður** á aðgerðasvæðinu og opna sniðsþátt rafrænnar skýrslugerðar fyrir breytingar í aðgerðarhönnuði rafrænnar skýrslugerðar.

![Skilgreiningasíða.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel-skrárþáttur

### <a name="manual-entry"></a>Handvirk færsla

Bæta þarf þætti **Excel\\-skráar** við skilgreint snið rafrænnar skýrslugerðar til að mynda skjal á útleið á Excel-sniði.

![Excel\skráarþáttur.](./media/er-excel-format-add-file-component.png)

Til að tilgreina útlit skjals á útleið skal hengja Excel-vinnubók með .xlsx skrárendingu við þátt **Excel\\-skrárinnar** sem sniðmát fyrir skjöl á útleið.

> [!NOTE]
> Þegar sniðmát er handvirkt hengt við þarf að nota [gerð skjals](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) sem hefur verið skilgreind í þeim tilgangi í [færibreytum rafrænnar skýrslugerðar](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

![Viðhengi bætt við Excel\skráarþátt.](./media/er-excel-format-add-file-component2.png)

Til að tilgreina hvernig viðhengt sniðmát er fyllt út þegar skilgreint snið rafrænnar skýrslugerðar er keyrt þarf að bæta við földuðum þáttum **vinnublaðs**, **sviðs** og **hólfs** í þætti **Excel\\-skráar**. Hver faldaður þáttur þarf að vera tengdur við Excel-vöru.

### <a name="template-import"></a>Sniðmátsinnflutningur

Hægt er að velja **Flytja inn úr Excel** á flipanum **Innflutningur** á aðgerðasvæðinu til að flytja nýtt sniðmát inn í autt snið rafrænnar skýrslugerðar. Í þessu dæmi er þáttur **Excel\\-skráar** stofnaður sjálfkrafa og innflutta sniðmátið verður hengt við hann. Allir nauðsynlegir þættir rafrænnar skýrslugerðar verða einnig stofnaðir sjálfkrafa, samkvæmt lista yfir greindar Excel-vörur.

![Val á „Flytja inn úr Excel“.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Ef stofna á valfrjálsa einingu fyrir **Vinnublað** á breytanlegu sniði rafrænnar skýrslugerðar þarf að stilla valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já**.

## <a name="sheet-component"></a>Vinnublaðsþáttur

Þátturinn **Vinnublað** gefur til kynna vinnublað viðhengdu Excel-vinnubókarinnar sem þarf að fylla út. Heiti vinnublaðs í Excel-sniðmáti er skilgreint í eiginleikanum **Vinnublað** fyrir þennan þátt.

> [!NOTE]
> Þessi þáttur er valfrjáls fyrir Excel-vinnubækur sem innihalda eitt vinnublað.

Á flipanum **Vörpun** í aðgerðarhönnuði rafrænnar skýrslugerðar er hægt að skilgreina eiginleikann **Virkt** fyrir þátt af gerðinni **Vinnublað** til að tilgreina hvort setja þurfi þátt í myndað skjal:

- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rétt** í keyrslu eða ef engin segð er skilgreind, verður viðeigandi vinnublað sett í myndaða skjalið.
- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu mun myndaða skjalið ekki innihalda vinnublað.

![Dæmi um vinnublaðsþátt.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Sviðsþáttur

Þátturinn **Svið** gefur til kynna Excel-svið sem þessi þáttur rafrænnar skýrslugerðar þarf að stýra. Heiti sviðsins er skilgreint í eiginleikanum **Excel-svið** fyrir þennan þátt.

### <a name="replication"></a>Gagnaspeglun

Eiginleikinn **Eftirlíkingarátt** tilgreinir hvort og hvernig svið verður endurtekið í mynduðu skjali:

- Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Engin eftirlíking** verður viðeigandi Excel-svið ekki endurtekið í myndaða skjalinu.
- Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Lóðrétt** verður viðeigandi Excel-svið endurtekið í myndaða skjalinu. Hvert endurtekið svið er sett undir upprunalega sviðið í Excel-sniðmáti. Fjöldi endurtekninga er skilgreindur af fjölda færslna í gagnagjafa af gerðinni **Færslulisti** sem er bundin þessum þætti rafrænnar skýrslugerðar.
- Ef eiginleikinn **Eftirlíkingarátt** er stilltur á **Lárétt** verður viðeigandi Excel-svið endurtekið í myndaða skjalinu. Hvert endurtekið svið er sett til hægri við upprunalega sviðið í Excel-sniðmáti. Fjöldi endurtekninga er skilgreindur af fjölda færslna í gagnagjafa af gerðinni **Færslulisti** sem er bundin þessum þætti rafrænnar skýrslugerðar.

Frekari upplýsingar um lárétta eftirlíkingu er að hægt að nálgast með því að fylgja skrefunum í [Nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum](tasks/er-horizontal-1.md).

### <a name="nested-components"></a>Hreiður íhlutir

Þátturinn **Svið** getur verið með aðra faldaða þætti rafrænnar skýrslugerðar sem eru notaðir til að færa inn gildi í viðeigandi Excel-svið.

- Ef þáttur í flokknum **Texti** er notaður til að færa inn gildi er gildið fært inn í Excel-svið sem textagildi.

    > [!NOTE]
    > Notið þetta mynstur til að sníða innfærð gildi út frá landsstaðlinum sem er skilgreindur í forritinu.

- Ef þátturinn **Hólf** í flokknum **Excel** er notaður til að færa inn gildi er gildið fært inn í Excel-svið sem gildi gagnagerðar sem er skilgreind af bindingum viðkomandi **Hólf**-þáttar (til dæmis **Strengur**, **Raunverulegt** eða **Heiltala**).

    > [!NOTE]
    > Notið þetta mynstur til að virkja Excel-forritið til að sníða innfærð gildi út frá landsstaðli tölvunnar sem opnar skjal á útleið.

### <a name="enabling"></a>Virkjar

Á flipanum **Vörpun** í aðgerðarhönnuði rafrænnar skýrslugerðar er hægt að skilgreina eiginleikann **Virkt** fyrir þátt af gerðinni **Svið** til að tilgreina hvort setja þurfi þátt í myndað skjal:

- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rétt** í keyrslu eða ef engin segð er skilgreind, verður viðeigandi svið sett í myndaða skjalið.
- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu, og ef þetta svið stendur ekki fyrir allar línur eða dálka, verður viðeigandi svið ekki fyllt út í mynduðu skjalið.
- Ef segð eiginleikans **Virkt** er skilgreind til að skila **Rangt** við keyrslu, og ef þetta svið stendur fyrir allar línur eða dálka, mun myndaða skjalið innihalda þessar línur og dálka sem faldar línur og falda dálka.

### <a name="resizing"></a>Breyta stærð

Þú getur stillt Excel sniðmátið þitt til að nota frumur til að kynna textagögn. Til að tryggja að allur textinn í reit sé sýnilegur í mynduðu skjali, getur þú stillt þann reit þannig að textinn vefji sjálfkrafa inn í það. Þú getur líka stillt línuna sem inniheldur þann reit þannig að hún stilli sjálfkrafa hæð hans ef vafinn texti er ekki að fullu sýnilegur. Nánari upplýsingar er að finna í hlutanum „Vefja texta í reit“ í [Lagaðu gögn sem eru skorin af í frumum](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e).

> [!NOTE]
> Vegna þekkts [Excel takmörkun](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353), jafnvel þótt þú stillir hólf til að vefja texta og þú stillir línurnar sem innihalda þær hólf þannig að þær stilli sjálfkrafa hæð þeirra þannig að þær passi umvafinn textann, gætirðu ekki notað **AutoFit** og **Vefja texta** Excel eiginleikar fyrir sameinaðar frumur og línurnar sem innihalda þær. 

Frá Dynamics 365 Finance útgáfu 10.0.23, getur þú þvingað ER til að reikna út, í mynduðu skjali, hæð hverrar línu sem var stillt þannig að hún passi sjálfkrafa við innihald hreiðraðra frumna þegar sú röð inniheldur að minnsta kosti einn sameinaðan reit sem var stilltur til að vefja textinn inni í því. Reiknuð hæð er síðan notuð til að breyta stærð línunnar til að tryggja að allar frumur í röðinni séu sýnilegar í mynduðu skjalinu. Til að byrja að nota þessa virkni þegar þú keyrir einhver ER snið sem voru stillt til að nota Excel sniðmát til að búa til skjöl á útleið skaltu fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar þýðingar**, í hlutanum **Tengdir tenglar**, skal velja **Færibreytur rafrænnar skýrslugerðar**.
3. Á **Rafrænar skýrslubreytur** síðu, á **Runtime** flipann, stilltu **Sjálfvirk raðhæð** valmöguleika til **Já**.

Þegar þú vilt breyta þessari reglu fyrir eitt ER-snið skaltu uppfæra drög að útgáfu þess sniðs með því að fylgja þessum skrefum.

1. Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.
2. Á síðunni **Skilgreiningar skýrslugerðar**, í hlutanum **Skilgreiningar**, skal velja **Skilgreiningar skýrslugerðar**.
3. Á **Stillingar** síðu, í stillingartrénu í vinstri glugganum, veldu ER stillingu sem er hannað til að nota Excel sniðmát til að búa til skjöl á útleið.
4. Í flýtiflipanum **Útgáfur** skal velja skilgreiningarútgáfuna sem er með stöðuna **Drög**.
5. Í aðgerðarúðunni skal velja **Hönnuður**.
6. Á **Sniðhönnuður** síðu, í sniðtrénu í vinstri glugganum, veldu Excel íhlutinn sem er tengdur við Excel sniðmát.
7. Á **Snið** flipa, í **Stilltu línuhæð** reit, veldu gildi til að tilgreina hvort ER ætti að neyða, á keyrslutíma, til að breyta hæð lína í skjali á útleið sem er búið til með breyttu ER sniði:

    - **Sjálfgefið** – Notaðu almennu stillinguna sem er stillt í **Sjálfvirk raðhæð** sviði á **Rafrænar skýrslubreytur** síðu.
    - **Já** – Hnekkja almennu stillingu og breyta línuhæð á keyrslutíma.
    - **Nei** – Hneka almennu stillingu og ekki breyta línuhæð á keyrslutíma.

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

## <a name="page-component"></a><a name="page-component"></a>Síðuþættir

### <a name="overview"></a>Yfirlit

Þú getur notað **Síðuþáttinn** þegar þú vilt að Excel fylgi rafrænu skýrslugerðarsniði og skipulagi síðuskiptingar í mynduðu skjali á útleið. Þegar snið rafrænnar skýrslugerðar keyrir íhluti sem heyra undir **Síðuþáttinn** er nauðsynlegum síðuskilum sjálfkrafa bætt við. Í þessu ferli er stærð myndaðs efnis, síðuuppsetning Excel-sniðmátsins og pappírsstærð sem er valin í Excel-sniðmátinu tekið til greina.

Ef þú verður að skipta mynduðu skjali í mismunandi hluta, sem hver er með mismunandi síðuskiptingu, getur þú stillt ýmsa **Síðuþætti** í hverjum [Vinnublaðsþætti](er-fillable-excel.md#sheet-component).

### <a name="structure"></a><a name="page-component-structure"></a>Skipulag

Ef fyrsti hlutinn undir **Síðuþættinum** er [Sviðsþáttur](er-fillable-excel.md#range-component) þar sem eiginleikinn **Eftirlíkingaráttin** er stillt á **Engin eftirlíking** er þetta svið álitið síðuhaus fyrir síðuskiptingu sem byggir á stillingunum á núverandi **Síðuþætti**. Excel-sviðið sem tengist þessum sniðsþætti er endurtekið efst á öllum síðum sem eru myndaðar með því að nota stillingarnar á núverandi **Síðuþætti**.

> [!NOTE]
> Fyrir rétta síðuskiptingu, ef sviðið [Línur til að endurtaka efst](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409) er stillt í Excel-sniðmátinu þínu, verður heimilisfang þessa Excel-sviðs að jafngilda heimilisfangi Excel-sviðsins sem tengist **Sviðsþættinum** sem var útskýrður hér áður.

Ef síðasti hlutinn undir **Síðuþættinum** er **Sviðsþáttur** þar sem eiginleikinn **Eftirlíkingaráttin** er stillt á **Engin eftirlíking** er þetta svið álitið síðufótur fyrir síðuskiptingu sem byggir á stillingunum á núverandi **Síðuþætti**. Excel-sviðið sem tengist þessum sniðsþætti er endurtekið neðst á öllum síðum sem eru myndaðar með því að nota stillingarnar á núverandi **Síðuþætti**.

> [!NOTE]
> Fyrir rétta síðuskiptingu ætti ekki að breyta stærð Excel-sviða, sem tengjast **Sviðsþáttum**, á keyrslutíma. Ekki er mælt með því að þú sníðir hólf af þessu sviði með því að nota **Orðskrið í hólfi** og **Aðlaga línuhæð sjálfkrafa** [valkosti](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84) Excel.

Þú getur bætt við mörgum öðrum **Sviðsþáttum** milli valfrjálsra **Sviðsþátta** til að tilgreina hvernig myndað skjal er fyllt út.

Ef safn faldaðra **Sviðsþátta** undir **Síðuþættinum** samræmist ekki fyrra útskýrða skipulagi kemur upp [villa](er-components-inspections.md#i17) á hönnunartíma í sniðshönnuði rafrænnar skýrslugerðar. Villuboðin upplýsa þig um að vandamálið getur valdið vandræðum á keyrslutíma.

> [!NOTE]
> Til að búa til rétt úttak skal ekki tilgreina bindingu fyrir neina **Sviðsþætti** undir **Síðuþættinum** ef eiginleikinn **Eftirlíkingarátt** fyrir **Sviðsþáttinn** sé stilltur á **Engin eftirlíking** og sviðið er stillt til að mynda síðuhausa og síðufætur.

Ef þú vilt að samlagning og talning sem tengist síðuskiptingu reikni út hlaupandi samtölur og samtölur á hverja síðu er mælt með að þú stilltir nauðsynlega gagnagjafann [Gagnasöfnun](er-data-collection-data-sources.md). Til að fræðast um hvernig á að nota **Síðuþáttinn** til að skipta mynduðu Excel-skjali á síður skal klára ferlin í [Hanna snið rafrænnar skýrslugerðar til að síðuskipta mynduðu skjali á Excel-sniði](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Takmarkanir

Þegar þú notar **Síðuþáttinn** fyrir síðuskiptingu Excel færðu ekki að vita endanlegan blaðsíðufjölda í mynduðu skjali fyrr en síðuskiptingunni er lokið. Þú getur þar af leiðandi ekki reiknað út heildarfjölda blaðsíðna með því að nota formúlur rafrænnar skýrslugerðar og prentað út réttan fjölda af blaðsíðum af mynduðu skjali á neinni blaðsíðu á undan síðustu síðunni.

> [!TIP]
> Til að fá út þessa niðurstöðu í síðuhaus eða síðufót Excel með því að nota sérstakt [snið](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) Excel fyrir síðuhausa og síðufætur.

Stilltir **Síðuþættir** eru ekki teknir til greina þegar þú uppfærir Excel-sniðmát á breytanlegu sniði í Dynamics 365 Finance útgáfu 10.0.22. Þessi virkni er tekin til greini í frekari útgáfum á Finance.

Ef þú stillir Excel-sniðmátið á að nota [skilyrt snið](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting) er ekki víst að það virka sem skyldi í einhverjum tilfellum.

### <a name="applicability"></a>Gildissvið

**Síðuþátturinn** virkar aðeins fyrir sniðsþátt [Excel-skráar](er-fillable-excel.md#excel-file-component) þegar sá þáttur er stilltur á að nota sniðmát í Excel. Ef þú [skiptir út](tasks/er-design-configuration-word-2016-11.md) Excel-sniðmátinu fyrir Word-sniðmát og keyrir svo breytanlegt rafrænt skýrslugerðarsnið verður **Síðuþátturinn** hunsaður.

**Síðuþátturinn** virkar aðeins þegar eiginleikinn **Virkja notkun á EPPlus-safni í rafrænum skýrslugerðarramma** er virkjaður. Undantekning kemur fram á keyrslutíma ef rafræn skýrslugerð reynir að vinna úr **Síðuþættinum** meðan slökkt er á þessum eiginleika.

> [!NOTE]
> Undantekning kemur fram á keyrslutíma ef snið rafrænnar skýrslugerðar vinnur úr **Síðuþættinum** fyrir Excel-sniðmát sem inniheldur a.m.k. eina formúlu sem vísar í hólf sem er ekki í gildi. Til að koma í veg fyrir keyrsluvillur skaltu laga Excel-sniðmátið eins og lýst er í [Hvernig á að leiðrétta #REF! villu](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

## <a name="footer-component"></a>Þáttur síðufótar

Þáttur **Síðufótar** er notaður til að fylla inn síðufætur neðst á mynduðu vinnublaði í Excel-vinnubók.

> [!NOTE]
> Hægt er að bæta þessum þætti við fyrir hvern þátt **Vinnublaðs** til að tilgreina mismunandi síðufætur fyrir mismunandi vinnublöð í myndaðri Excel-vinnubók.

Þegar stakt þáttur **Síðufótar** er skilgreindur, er hægt að nota eiginleikann **Útlit hauss/fótar** til að tilgreina síðurnar sem þátturinn er notaður fyrir. Eftirtalin gildi eru tiltæk:

- **Allar** – Keyrið skilgreindan þátt **Síðufótar** fyrir allar síður yfireiningar Excel-vinnublaðs.
- **Fyrsta** – Keyrið skilgreindan þátt **Síðufótar** fyrir aðeins fyrstu síðu yfireiningar Excel-vinnublaðs.
- **Sléttar** – Keyrið skilgreindan þátt **Síðufótar** fyrir aðeins síður sléttra talna í yfireiningu Excel-vinnublaðs.
- **Odda** – Keyrið skilgreindan þátt **Síðufótar** fyrir aðeins síður oddatölu í yfireiningu Excel-vinnublaðs.

Fyrir einn þátt **Vinnublaðs** er hægt að bæta við ýmsum þáttum **Síðufótar** sem hver hefur mismunandi gildi fyrir eiginleikann **Útlit hauss/fótar**. Á þennan hátt er hægt að mynda mismunandi síðufætur fyrir mismunandi gerðir af síðum í Excel-vinnublaði.

> [!NOTE]
> Gangið úr skugga um að hver þáttur **Síðufótar** sem bætt er við stakan þátt **Vinnublaðs** sem með mismunandi gildi fyrir eiginleikann **Útlit hauss/fótar**. Annars kemur upp [staðfestingarvilla](er-components-inspections.md#i16). Villuboðin sem birtast láta vita af ósamræminu.

Undir viðbættum þætti **Síðufótar** skal bæta við nauðsynlegum földuðum þáttum **Text\\String**, **Text\\DateTime** eða annarri gerð. Skilgreinið bindingarnar fyrir þessa þæti til að tilgreina hvernig fyllt er í síðufótinn.

Einnig er hægt að nota sérstaka [sniðskóða](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) til að sníða efni myndaðs síðufótar á réttan hátt. Til að fá frekari upplýsingar um þessa nálgun skal fylgja skrefunum í [Dæmi 1](#example-1) síðar í þessu efnisatriði.

> [!NOTE]
> Þegar snið rafrænnar skýrslugerðar er skilgreint skal hafa í huga [takmörk](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) Excel og hámarksfjölda stafa fyrir einn haus og fót.

## <a name="header-component"></a>Þáttur síðuhauss

Þáttur **Síðuhauss** er notaður til að fylla inn síðuhausa efst á mynduðu vinnublaði í Excel-vinnubók. Hann er notaður eins og þáttur **Síðufótar**.

## <a name="edit-an-added-er-format"></a>Breyta sniði rafrænnar skýrslugerðar sem bætt er við

### <a name="update-a-template"></a>Uppfæra sniðmát

Hægt er að velja **Uppfæra úr Excel** á flipanum **Innflutningur** á aðgerðasvæðinu til að flytja uppfært sniðmát inn í breytanlegt snið rafrænnar skýrslugerðar. Á meðan á þessu stendur er sniðmáti af valinni einingu **Excel\\skrá** skipt út fyrir nýtt sniðmát. Efni breytanlegs sniðs rafrænnar skýrslugerðar verður samstillt við efni með uppfærðs sniðmáts rafrænnar skýrslugerðar.

- Nýr sniðsþáttur rafrænnar skýrslugerðar verður sjálfkrafa stofnaður fyrir hvert Excel-heiti ef sniðsþáttur rafrænnar skýrslugerðar finnst ekki í breytanlega sniðinu.
- Öllum sniðsþáttum rafrænnar skýrslugerðar verður eytt úr breytanlegu sniði rafrænnar skýrslugerðar ef viðeigandi Excel-heiti finnst ekki fyrir það.

> [!NOTE]
> Stilla þarf valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já** ef stofna á valfrjálsa **Skjal** einingu á breytanlegu sniði rafrænnar skýrslugerðar.
>
> Ef breytanlegu sniði rafrænnar skýrslugerðar, var upphaflega í einingunum **Vinnublað** er mælt með því að stilla valkostinn **Stofna sniðseiningu Excel-vinnublaðs** á **Já** þegar flutt er inn uppfært sniðmát. Að öðrum kosti verða allar faldaðar einingar upprunalegu einingarinnar **Vinnublað** búnar til frá grunni. Af þeim ástæðum glatast allar bindingar endurstofnaðra sniðseininga í uppfærðu sniði rafrænnar skýrslugerðar.

![Valkosturinn „Stofna sniðseiningu Excel-vinnublaðs“ í svarglugganum Uppfæra úr Excel.](./media/er-excel-format-update-template.png)

Til að fá frekari upplýsingar um þennan eiginleika skal fylgja skrefunum í [Breyta rafrænum skýrslugerðarsniðum með því að endurnýta Excel-sniðmát](modify-electronic-reporting-format-reapply-excel-template.md).

## <a name="validate-an-er-format"></a>Villuleita snið rafrænnar skýrslugerðar

Þegar snið rafrænnar skýrslugerðar sem hægt er að breyta er sannprófað er samræmisathugun framkvæmd til að ganga úr skugga um að Excel-heitið sé til staðar í Excel-sniðmátinu sem er í notkun. Þú munt fá tilkynningu ef ósamræmi kemur upp. Boðið er upp á valkost til að lagfæra sum vandamál sjálfkrafa.

![Staðfestingarvilluboð.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>Stjórnun útreiknings Excel-formúla

Þegar skjal á útleið á Microsoft Excel -vinnubókarsniði er myndað kunna tiltekin hólf þessa skjals að innihalda Excel-formúlur. Þegar eiginleikinn **Virkja notkun á EPPlus-safni í rafrænum skýrslugerðarramma** er virkur getur þú stjórna hvenær formúlurnar eru reiknaðar út með því að breyta gildi **færibreytunnar** [Valkostir útreikninga](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) í Excel-sniðmátinu sem verið er að nota:

- Veljið **Automatic** til að endurreikna allar háðar formúlur í hvert sinn sem ný svið, hólf o.s.frv. er bætt við myndað skjal.

    >[!NOTE]
    > Þetta gæti valdið afkastavandamálum í Excel-sniðmátum sem innihalda margar tengdar formúlur.

- Veljið **Handvirk** til að forðast endurreikning formúlu þegar skjal er myndað.

    >[!NOTE]
    > Endurútreikningur formúlu er þvingaður handvirkt þegar myndað skjal er opnað í forskoðun með Excel.
    > Ekki nota þennan valkost ef áfangastaður rafrænnar skýrslugerðar er skilgreindur sem gerir ráð fyrir notkun á mynduðu skjali án forskoðunar þess í Excel (PDF-umbreyting, sending í tölvupósti o.s.frv.) vegna þess að skjalið sem var myndað inniheldur hugsanlega ekki gildi í hólfum sem innihalda formúlur.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Dæmi 1: Sníða efni síðufótar

1. Notið uppgefnar skilgreiningar rafrænnar skýrslugerðar til að [mynda](er-generate-printable-fti-forms.md) prentvænt reikningsskjal með frjálsum texta.
2. Farið yfir síðufót myndaðs skjals. Takið eftir að hann inniheldur upplýsingar um núverandi blaðsíðutal og fjölda blaðsíðna í skjalinu.

    ![Fara yfir síðufót myndaðs skjals á Excel-sniði.](./media/er-fillable-excel-footer-1.gif)

3. Í sniðshönnuði rafrænnar skýrslugerðar skal [opna](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) sýnishorn af rafrænu skýrslugerðarsniði til að fara yfir.

    Síðufótur vinnublaðsins **Reikningur** er myndað samkvæmt stillingum tveggja þátta **Strengs** sem er að finna undir þættinum **Síðufótur**:

    - Fyrsti **Strengjaþátturinn** fyllir í eftirfarandi sérstaka sniðskóða til að neyða Excel til að nota tiltekið snið:

        - **&C** – Miðjujafna neðanmálstexta.
        - **&"Segoe UI,Venjulegt"&8** – Sýna neðanmálstexta í leturgerðinni "Segoe UI Regular" í 8 punkta stærð.

    - Annar **Strengjaþátturinn** fyllir í textann sem inniheldur núverandi blaðsíðutal og heildarfjölda síðna í núverandi skjali.

    ![Fara yfir hlut síðufótar í rafrænu skýrslugerðarsniði á sniðshönnunarsíðunni.](./media/er-fillable-excel-footer-2.png)

4. Sérstillið sýnishorn af sniði rafrænnar skýrslugerðar til að breyta núverandi síðufæti:

    1. [Búið til](er-quick-start2-customize-report.md#DeriveProvidedFormat) afleiddan **sérstilltan reikning með frjálsum texta** fyrir rafrænt skýrslugerðarsnið sem byggir á sýnishorni rafræns skýrslugerðarsniðs.
    2. Bætið við fyrsta nýja parinu af **Strengjaþáttum** fyrir þátt **Síðufótar** á vinnublaðinu **Reikningur**:

        1. Bætið við **Strengjaþætti** sem jafnar heiti fyrirtækisins vinstra megin og sýnir það í 8 punkta stærð í leturgerðinni "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**).
        2. Bætið við **Strengjaþætti** sem fyllir í heiti fyrirtæksisin (**model.InvoiceBase.CompanyInfo.Name**).

    3. Bætið við seinna nýja parinu af **Strengjaþáttum** fyrir þátt **Síðufótar** á vinnublaðinu **Reikningur**:

        1. Bætið við **Strengjaþætti** sem jafnar úrvinnsludag hægra megin og sýnir það í 8 punkta stærð í leturgerðinni "Segoe UI Regular" (**"&R&"Segoe UI,Regular"&8"**).
        2. Bætið við **Strengjaþætti** sem fyllir í úrvinnsludaginn á sérstilltu sniði (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Þáttur síðufótar í rafrænu skýrslugerðarsniði á sniðshönnunarsíðunni yfirfarinn.](./media/er-fillable-excel-footer-3.png)

    4. [Ljúkið](er-quick-start2-customize-report.md#CompleteDerivedFormat) útgáfudrögum af afleidda rafræna skýrslugerðarsniðinu **Sérsniðinn reikningur með frjálsum texta (Excel)**.

5. [Skilgreinið](er-generate-printable-fti-forms.md#configure-print-management) prentstýringar til að nota afleidda rafræna skýrslugerðarsniðið **Sérstilltur reikningur með frjálsum texta (Excel)** í staðinn fyrir sýnishornið af sniði rafrænnar skýrslugerðar.
6. Búið til prentvænt reikningsskjal með frjálsum texta og skoðið síðufótinn á myndaða skjalinu.

    ![Síðufótur á mynduðu skjali skoðaður á Excel-sniði.](./media/er-fillable-excel-footer-4.gif)

## <a name="example-2-fixing-the-merged-cells-epplus-issue"></a><a name="example-2"></a> Dæmi 2: Lagað EPPlus vandamálið með sameinuðum frumum

Þú getur keyrt ER-snið til að búa til skjal á útleið á Excel vinnubókarsniði. Þegar **Virkjaðu notkun EPPlus bókasafns í rafrænum skýrslugerð** eiginleiki er virkur í **Eiginleikastjórnun** vinnurými, the [EPPlus bókasafn](https://www.nuget.org/packages/epplus/4.5.2.1) er notað til að búa til Excel úttak. Hins vegar vegna þekktra [Excel hegðun](https://answers.microsoft.com/msoffice/forum/all/deleting-a-range-of-cells-that-includes-merged/8601462c-4e2c-48e0-bd23-848eecb872a9) og takmörkun á EPPlus bókasafninu, gætirðu lent í eftirfarandi undantekningu: "Get ekki eytt/skrifað yfir sameinuð hólf. Svið er að hluta sameinað hinu sameinaða sviðinu.“ Til að læra hvers konar Excel sniðmát gætu valdið þessari undantekningu og hvernig þú getur lagað vandamálið skaltu klára eftirfarandi dæmi.

1. Í Excel skjáborðsforritinu skaltu búa til nýja Excel vinnubók.
2. Á vinnublaði **Blað 1**, bætið við **Titill skýrslu** heiti á frumu **A2**.
3. Sameina frumur **A1** og **A2**.

    ![Skoðaðu niðurstöður sameiningar reita A1 og A2 í hönnuðu Excel vinnubókinni í Excel skjáborðsforritinu.](./media/er-fillable-excel-example2-1.png)

3. Á **Stillingar** síða, [bæta við nýju ER sniði](er-fillable-excel.md#add-a-new-er-format) til að búa til útleið skjal á Excel vinnubókarsniði.
4. Á **Sniðhönnuður** síða, [flytja inn](er-fillable-excel.md#template-import) hönnuð Excel vinnubók í bætt ER sniði sem nýtt sniðmát fyrir skjöl á útleið.
5. Á **Kortlagning** flipann, stilltu bindinguna fyrir **Titill skýrslu** hluti af [Cell](er-fillable-excel.md#cell-component) tegund.
6. Keyrðu uppsett ER snið. Taktu eftir að eftirfarandi undantekning er hent: "Get ekki eytt/skrifað yfir sameinuð hólf. Svið er að hluta sameinað hinu sameinaða sviðinu.“

    ![Skoðaðu niðurstöðurnar af því að keyra uppsett ER sniðið á síðunni Format designer.](./media/er-fillable-excel-example2-2.png)

Þú getur lagað vandamálið á annan hvorn af eftirfarandi leiðum:

- **Auðveldara en ekki mælt með:** Í **Eiginleikastjórnun** vinnusvæði, slökktu á **Virkjaðu notkun á EPPlus bókasafni í rafrænum skýrslugerð** eiginleiki. Þó að þessi aðferð sé auðveldari gætirðu lent í öðrum vandamálum ef þú notar hana, vegna þess að sum ER-virkni er aðeins studd þegar **Virkjaðu notkun á EPPlus bókasafni í rafrænum skýrslugerð** eiginleiki er virkur.
- **Mælt með:** Fylgdu þessum skrefum:

    1. Í Excel skjáborðsforritinu skaltu breyta Excel vinnubókinni á einn af eftirfarandi leiðum:

        - Á vinnublaði **Blað 1**, taka frumur úr sameiningu **A1** og **A2**.
        - Breyttu tilvísuninni fyrir **Titill skýrslu** nafn frá **=Blað1!$A$2** til **=Blað1!$A$1**.

        ![Skoðaðu niðurstöður þess að breyta tilvísuninni í hönnuðu Excel vinnubókinni í Excel skjáborðsforritinu.](./media/er-fillable-excel-example2-3.png)

    2. Á **Sniðhönnuður** síða, [flytja inn](er-fillable-excel.md#template-import) breyttu Excel vinnubókinni í breytanlegt ER snið til að uppfæra núverandi sniðmát.
    3. Keyrðu breytta ER sniðið.

        ![Skoðaðu skjalið sem búið var til í Excel skjáborðsforritinu.](./media/er-fillable-excel-example2-4.png)

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit yfir rafræna skýrslugerð](general-electronic-reporting.md)

[Hanna skilgreiningu fyrir myndun skýrslna á OPENXML-sniði](tasks\er-design-reports-openxml-2016-11.md)

[Breyta rafrænum skýrslugerðarsniðum með því að endurnýta Excel-sniðmát](modify-electronic-reporting-format-reapply-excel-template.md)

[Nota svið sem má stækka lárétt til að bæta við dálkum gagnvirkt við í Excel skýrslum](tasks/er-horizontal-1.md)

[Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER](electronic-reporting-embed-images-shapes.md)

[Skilgreina rafræna skýrslugerð (ER) til að draga gögn inn í Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
