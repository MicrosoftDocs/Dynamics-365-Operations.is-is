---
title: Microsoft Office-notendaviðmót í viðskiptaskjalastjórnun (inniheldur myndband)
description: Þessi grein útskýrir hvernig á að nota nýja notendaviðmótið í viðskiptaskjalastjórnunareiginleika rafrænnar skýrslugerðar (ER) ramma.
author: v-anamir
ms.date: 01/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 208cfc91f11d4893785538ce4874e85a5725e993
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109261"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Notandaviðmót Microsoft Office-stíls í Stjórnun viðskiptaskjala

[!include [banner](../includes/banner.md)]

Stjórnun viðskiptaskjala er gerir fyrirtækjanotendum kleift að breyta sniðmátum viðskiptaskjala með því að nota Microsoft Office 365 þjónustu eða viðeigandi Microsoft Office skjáborðsforrit. Breytingar gætu innihaldið hönnunarbreytingar eða nýjar dreifingar, eða notendur gætu bætt við frátökutákni til að innihalda viðbótargögn án þess að þurfa að breyta kóðanum. Nánari upplýsingar um hvernig á að vinna með skjalastjórnun viðskipta, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).

Nýja notendaviðmótið (UI) er skýrara og þægilegra í notkun. The **Viðskiptaskjal** svæði sýnir aðeins sniðmát sem eru í eigu núverandi [virkur](tasks/er-configuration-provider-mark-it-active-2016-11.md)[veitanda](general-electronic-reporting.md#Provider) og staðsett í núverandi tilviki Dynamics 365 Finance. Í fyrra notendaviðmóti var **Sniðmát** flipi listi öll sniðmát sem voru tiltæk fyrir hvaða þjónustuaðila sem er. Hann sýndi einnig öll sniðmát sem voru búin til og breytt af öllum notendum í sama hlutverkinu.

Þú getur notað **Nýtt skjal** hnappinn í **Stjórnun viðskiptaskjala** vinnusvæði til að búa til og breyta sniðmáti í [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) sniði [uppsetningu](general-electronic-reporting.md#Configuration) sem er veitt af annarri veitu og staðsettur í núverandi Finance tilviki, eða til að hlaða upp nýju sniðmáti úr Excel vinnubók. Að auki, í útgáfu 10.0.25 og nýrri, geturðu notað **Nýtt skjal** hnappinn til að búa til og breyta sniðmáti í ER sniði sem er geymt í [Alþjóðleg geymsla](general-electronic-reporting.md#Repository).

Í dæmunum í þessari grein er virki veitandinn Contoso og þú notar það til að búa til sniðmát sem er byggt á sniðmáti sem er útvegað af Microsoft. Einnig er hægt að stofna sniðmát með því að hlaða upp eigin sniðmáti á Excel sniði.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

The [Búðu til nýtt viðskiptaskjal með því að nota viðskiptaskjalastjórnun](https://youtu.be/gAIYl-mM_pw) myndbandið (sýnt hér að ofan) er innifalið í [lagalista um fjármál og rekstur](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) í boði á YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gerðu nýja skjalið UI í viðskiptaskjalastjórnun tiltækt

Til að byrja að nota nýja skjalið UI í viðskiptaskjalastjórnun verður þú að kveikja á eiginleikanum **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á vinnusvæðinu **Stjórnun eiginleika**.

Fylgdu þessum skrefum til að kveikja á þessum eiginleika fyrir alla lögaðila.

1. Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Allt**, velurðu eiginleikann **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á listanum.
2. Veldu **Virkja núna** til að kveikja á völdum eiginleika.
3. Endurnýjaðu síðuna til að fá aðgang að nýja eiginleikanum.

## <a name="add-or-activate-a-provider"></a>Bættu við eða virkjaðu þjónustuveitu

Hvert sniðmát viðskiptaskjals er geymt í ER-sniði sem er merkt sem í eigu ákveðinnar stillingaveitu. Þegar þú býrð til nýtt sniðmát er ný ER-sniðsstilling búin til til að halda því. Þess vegna verður að auðkenna þjónustuaðila fyrir þá stillingu. Virkur veitandi ER ramma er notaður í þessu skyni. Ef það er enginn veitandi í ER geturðu búið til einn. Ef það er nr *virkur* veitanda geturðu virkjað eina af núverandi veitendum. Gluggi til að bæta við eða virkja veitu opnast þegar þess er þörf á meðan þú byrjar að bæta við nýju sniðmáti.

### <a name="add-a-new-provider"></a>Bættu við nýjum þjónustuaðila

Til að búa til nýja þjónustuveitu skaltu fylgja þessum skrefum á **Stillingarveita** valmynd:

1.  Á **Veldu stillingarveitu** flipa, í **Nafn** reit, sláðu inn nafn nýja þjónustuveitunnar.
2.  Í **Netfang** reit, sláðu inn netfang (URL) nýju þjónustuveitunnar. 
3.  Veldu **Í lagi**.

    ![Að búa til nýjan þjónustuaðila í viðskiptaskjalastjórnun.](./media/bdm_create_provider.png)

Þjónustuveitan sem bætt er við verður sjálfkrafa virkjuð.

### <a name="activate-a-provider"></a>Virkjaðu þjónustuaðila

Til að virkja þjónustuveitu skaltu fylgja þessum skrefum á **Stillingarveita** valmynd:

1.  Á **Veldu stillingarveitu** flipa, í **Stillingarveita** reit, veldu þjónustuveituna.
2.  Veldu **Í lagi**.

    ![Að virkja veitu í viðskiptaskjalastjórnun.](./media/bdm_choose_provider.png)

Valin veitandi verður virkjuð.

> [!NOTE]
> Hvert viðskiptaskjalastjórnunarsniðmát er staðsett í ER-sniði sem vísar til veitunnar sem höfundar stillinga. Þess vegna þarf virkan veitanda fyrir hvert sniðmát.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Breyttu sniðmáti sem er í eigu annarrar þjónustuveitu

Þetta dæmi sýnir hvernig á að nota **Nýtt skjal** hnappinn í **Stjórnun viðskiptaskjala** vinnusvæði til að búa til og breyta sniðmáti í ER sniðstillingu sem er veitt af annarri þjónustuveitu og staðsett í núverandi Finance tilviki. Í þessu dæmi er virki veitandinn Contoso, sem notar ER-sniðsstillinguna sem er veitt af Microsoft. Eftir að þú hefur valið **Nýtt skjal**, hinn **Veldu** flipann á **Búðu til nýtt sniðmát** síða sýnir öll sniðmát núverandi Finance-tilviks sem eru í eigu núverandi veitanda og annarra veitenda. Veldu sniðmát til að opna það. Þú getur síðan búið til nýtt breytanlegt eintak af sniðmátinu. Breytta sniðmátið er geymt í nýrri ER sniðstillingu sem er sjálfkrafa mynduð.

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala.](./media/BDM_overview_new_template1.png)

2. Á **Búðu til nýtt sniðmát** síðu, á **Veldu** flipann, veldu skjalið sem á að nota sem sniðmát og veldu síðan **Búðu til skjal**.

    ![Gluggi viðskiptaskjala.](./media/BDM_overview_new_template2.png)

3. Í nýja glugganum, í reitnum **Titill**, breytirðu titlinum eins og þú þarfnast. Titiltextinn er notaður til að nefna nýju skilgreiningu ER-sniðsins sem er sjálfkrafa búin til. Drög að þessari skilgreiningu (**Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)**) sem munu innihalda breytt sniðmát og verða notuð til að keyra þetta ER-snið fyrir núverandi notanda. Hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.
4. Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður sjálfkrafa stofnað.
5. Í reitnum **Athugasemd** skaltu uppfæra athugasemdinar fyrir breytanlega endurskoðun sem verður sjálfkrafa stofnuð.
6. Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

    ![Stofngluggi skjalagerðar.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Hladdu upp sniðmáti sem notar núverandi Excel vinnubók

Þetta dæmi sýnir hvernig á að nota **Nýtt skjal** hnappinn í **Stjórnun viðskiptaskjala** vinnusvæði til að búa til og breyta sniðmáti í ER sniði, byggt á tiltækri Excel vinnubók. Í þessu dæmi er virki veitandinn Contoso og þú notar ER [gagnalíkan](er-overview-components.md#data-model-component) og ER [módelkortlagningu](er-overview-components.md#model-mapping-component) stillingar sem eru veittar af Microsoft. Eftir að þú hefur valið **Nýtt skjal**, veldu **Hlaða upp** flipann á **Búðu til nýtt sniðmát** síðu. Þar geturðu tilgreint upplýsingar um upphleðslu Excel vinnubókar. Eftir að þú hleður upp Excel vinnubókinni er henni breytt í viðskiptaskjalasniðmát sem er opnað til að breyta. Breytta sniðmátið verður geymt í nýrri ER sniðstillingu sem er sjálfkrafa mynduð.

Fylgið þessum skrefum til að veita nauðsynlegar upplýsingar áður en sniðmáti er hlaðið upp.

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.
2. Á síðunni **Búa til nýtt sniðmát**, í flipanum **Hlaða upp**, í flipanum **Sniðmát**, skal velja **Fletta** til að finna og velja Excel-skrána sem á að nota sem sniðmát. Í hlutanum **Sniðmát** er sjálfkrafa fyllt inn í reitina **Titill** og **Lýsing**. Þeir tilgreina heiti og lýsingu á nýrri skilgreiningu rafræns skýrslugerðarsniðs sem er sjálfkrafa búið til. Hægt er að breyta þessum reitum eftir þörfum.
3. Í hlutanum **Skjalagerð**, í reitnum **Heiti**, skal tilgreina gerð viðskiptaskjalsins. Þetta gildi verður notað til að leita að réttri gagnaveitu (þ.e. skilgreiningu rafræns skýrslugerðarlíkans).

    ![Sniðmát flipinn á Hlaða upp flipanum á síðunni Búa til nýtt sniðmát.](./media/BDM_overview_new_UI_import_21.jpg)

4. Í flipanum **Gagnaveita**, í flýtiflipanum **Sía**, skal velja **Nota síu**. Í hlutanum **Gagnaveita**, er fyllt inn sjálfkrafa í reitinn **Heiti** eða hægt er að velja gildi handvirkt. Hægt er að nota síuna til að leita að viðeigandi heiti gagnaveitu eftir heiti, lýsingu, lands-/svæðiskóða og gerð viðskiptaskjals.

    ![Gagnagjafi flipinn á Hlaða upp flipanum á síðunni Búa til nýtt sniðmát.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Flýtiflipinn **Sía** er notuð til að leita að réttri gagnaveitu (þ.e. skilgreiningu rafræns skýrslugerðarlíkans). Hægt er að breyta öllum síureitum til að finna hentugustu gagnaveituna fyrir skjalið sem hlaðið er upp.
    > 
    > Skilyrðin í flýtiflipanum **Sía** eru notuð sem **EÐA** skilyrði.

5. Í flipanum **Vörpun** skal velja **Greina sjálfvirkt**. Reiturinn **Skilgreining rótar** er sjálfkrafa fylltur út eða hægt er að velja gildi handvirkt. Þessi flipi sýnir endavörpun eininganna úr sniðmátinu og líkaninu.

    ![Kortlagningarflipi á Upphleðsluflipanum á síðunni Búa til nýtt sniðmát.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Vörpunin í hlutanum **Skipulag sniðmáts** notar fulla samsvörun á merkjum eða lýsingum í gagnaveitunni á tungumáli notanda og í heiti hólfs í sniðmátinu.

6. Veljið **Stofna skjal** til að staðfesta að ætlunin sé að stofna sniðmát og hefja breytingarferlið.

Fyrir frekari upplýsingar, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Hladdu upp sniðmáti frá alþjóðlegu geymslunni

Þetta dæmi sýnir hvernig á að nota **Nýtt skjal** hnappinn í **Stjórnun viðskiptaskjala** vinnusvæði til að búa til og breyta sniðmáti í ER-sniði sem er útvegað af Microsoft og staðsett í alþjóðlegu geymslunni. Í þessu dæmi er virki veitandinn Contoso, sem notar ER-sniðsstillinguna sem er veitt af Microsoft. Eftir að þú hefur valið **Nýtt skjal**, hinn **Flytja inn úr alþjóðlegri geymslu** flipann á **Búðu til nýtt sniðmát** síða sýnir öll viðskiptaskjalasniðmát sem eru geymd í alþjóðlegu geymslunni en vantar í núverandi Finance tilviki. Eftir að þú hefur valið sniðmát er það flutt inn úr alþjóðlegu geymslunni í núverandi Finance tilvik til að búa til nýtt breytanlegt eintak. Breytta sniðmátið er geymt í nýrri ER sniðstillingu sem er sjálfkrafa mynduð.

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.
2. Á **Búðu til nýtt sniðmát** síðu, á **Flytja inn úr alþjóðlegri geymslu** flipann, veldu skjalið sem á að nota sem sniðmát og veldu síðan **Búðu til skjal**.

    ![Flytja inn úr alþjóðlegri geymslu flipanum á síðunni Búa til nýtt sniðmát.](./media/BDM_overview_new_template22.png)

3. Veldu í skilaboðareitnum **Já** til að staðfesta að þú viljir flytja inn valið skjal úr alþjóðlegu geymslunni í núverandi Finance tilvik. Ef þú ert beðinn um heimild skaltu fylgja leiðbeiningunum á skjánum.
4. Í nýja glugganum, í reitnum **Titill**, breytirðu titlinum eins og þú þarfnast. Titiltextinn er notaður til að nefna nýju skilgreiningu ER-sniðsins sem er sjálfkrafa búin til. Drög að útgáfu þessarar stillingar (**Innheimtubréfabréf (Excel) Afrit**) mun innihalda breytta sniðmátið og verður notað til að keyra þetta ER snið fyrir núverandi notanda. Hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.
5. Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður sjálfkrafa stofnað.
6. Í reitnum **Athugasemd** skaltu uppfæra athugasemdinar fyrir breytanlega endurskoðun sem verður sjálfkrafa stofnuð.
7. Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

