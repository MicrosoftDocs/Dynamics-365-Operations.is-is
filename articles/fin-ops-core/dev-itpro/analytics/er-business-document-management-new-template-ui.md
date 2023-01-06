---
title: Notandaviðmót Microsoft Office-stíls í Stjórnun viðskiptaskjala (inniheldur myndskeið)
description: Í þessari grein er útskýrt hvernig á að nota nýja notandaviðmótið í eiginleika viðskiptaskjalastjórnunar í ramma rafrænnar skýrslugerðar.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109261"
---
# <a name="microsoft-office-style-user-interface-in-business-document-management"></a>Notandaviðmót Microsoft Office-stíls í Stjórnun viðskiptaskjala

[!include [banner](../includes/banner.md)]

Stjórnun viðskiptaskjala er gerir fyrirtækjanotendum kleift að breyta sniðmátum viðskiptaskjala með því að nota Microsoft Office 365 þjónustu eða viðeigandi Microsoft Office skjáborðsforrit. Breytingar gætu innihaldið hönnunarbreytingar eða nýjar dreifingar, eða notendur gætu bætt við frátökutákni til að innihalda viðbótargögn án þess að þurfa að breyta kóðanum. Nánari upplýsingar um hvernig á að vinna með skjalastjórnun viðskipta, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).

Nýja notendaviðmótið (UI) er skýrara og þægilegra í notkun. Svæðið **Viðskiptaskjal** sýnir aðeins sniðmátin sem eru í eigu núverandi [virkrar](tasks/er-configuration-provider-mark-it-active-2016-11.md) [veitu](general-electronic-reporting.md#Provider) og til staðar í núverandi tilviki af Dynamics 365 Finance. Í eldra notandaviðmóti sýndi flipinn **Sniðmát** öll sniðmátin sem voru í boði fyrir alla þjónustuaðila. Hann sýndi einnig öll sniðmát sem voru búin til og breytt af öllum notendum í sama hlutverkinu.

Hægt er að nota hnappinn **Nýtt skjal** í **Stjórnun viðskiptaskjala** vinnusvæðinu til að búa til og breyta sniðmáti í [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) snið [stilling](general-electronic-reporting.md#Configuration) sem annar veitandi veitir og er staðsett í Finance-tilviki eða til að hlaða upp nýju sniðmáti úr Excel-vinnubók. Að auki í útgáfu 10.0.25 eða nýrri er hægt að nota hnappinum **Nýtt skjal** til að búa til og breyta sniðmáti í skilgreiningu sniðs rafrænnar skýrslugerðar (ER) sem er geymt í [Altæk geymsla](general-electronic-reporting.md#Repository).

Í dæmunum í þessari grein er virki veitandinn Contoso og þú notar hann til að búa til sniðmát sem byggja á sniðmáti sem Microsoft býður upp á. Einnig er hægt að stofna sniðmát með því að hlaða upp eigin sniðmáti á Excel sniði.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RWAVQg]

Myndbandið [Búa til nýtt viðskiptaskjal með stjórnun viðskiptaskjala](https://youtu.be/gAIYl-mM_pw) (sýnt hér að ofan) er að finna í [fjármála- og reksturs spilunarlistanum](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er aðgengilegur í YouTube.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>Gerðu nýja skjalið UI í viðskiptaskjalastjórnun tiltækt

Til að byrja að nota nýja skjalið UI í viðskiptaskjalastjórnun verður þú að kveikja á eiginleikanum **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á vinnusvæðinu **Stjórnun eiginleika**.

Fylgdu þessum skrefum til að kveikja á þessum eiginleika fyrir alla lögaðila.

1. Á vinnusvæðinu **Stjórnun eiginleika**, á flipanum **Allt**, velurðu eiginleikann **Office-lík notandaviðmótsreynsla fyrir skjalastjórnun** á listanum.
2. Veldu **Virkja núna** til að kveikja á völdum eiginleika.
3. Endurnýjaðu síðuna til að fá aðgang að nýja eiginleikanum.

## <a name="add-or-activate-a-provider"></a>Bæta við eða virkja veitu

Hvert sniðmát viðskiptaskjals er geymt í skilgreiningu rafræns skýrslugerðarsniðs sem er merkt sem í eigu tiltekinnar skilgreiningarveitu. Þegar nýtt sniðmát er búið til er ný skilgreining rafræns skýrslugerðarsniðs stofnuð til að geyma það. Því verður að finna veitu fyrir þá skilgreiningu. Virk veita fyrir ramma rafrænnar skýrslugerðar er notuð í þessum tilgangi. Ef það er enginn veita í rafrænni skýrslugerð er hægt að stofna hann. Ef engin *virk* veita er til staðar er hægt að virkja eina af fyrirliggjandi veitum. Svargluggi til að bæta við eða virkja veitu er opnaður þegar þess gerist þörf en þú byrjar að bæta við nýju sniðmáti.

### <a name="add-a-new-provider"></a>Bæta við nýrri veitu

Til að stofna nýja veitu skaltu fylgja þessum skrefum í glugganum **Skilgreiningarveita**:

1.  Á flipanum **Velja skilgreiningarveitu** í reitnum **Heiti** skal slá inn heiti nýju veitunnar.
2.  Í reitinn **Veffang** skal færa inn vefslóð nýju veitunnar. 
3.  Veldu **Í lagi**.

    ![Stofna nýja veitu í Stjórnun viðskiptaskjala.](./media/bdm_create_provider.png)

Viðbætt veita verður sjálfkrafa virk.

### <a name="activate-a-provider"></a>Virkja til veitu

Til að virkja veitu skal fylgja þessum skrefum í glugganum **Skilgreiningarveita**:

1.  Í flipanum **Velja skilgreiningarveitu**, í reitnum **Skilgreiningarveita**, skal velja veituna.
2.  Veldu **Í lagi**.

    ![Að virkja veitu í Stjórnun viðskiptaskjala.](./media/bdm_choose_provider.png)

Valinn veita verður virkjuð.

> [!NOTE]
> Hvert sniðmát viðskiptaskjalastjórnunar er staðsett í skilgreiningu rafræns skýrslugerðarsniðs sem vísar í veituna sem höfundur skilgreiningar. Því er krafist virkrar veitu fyrir hvert sniðmát.

## <a name="edit-a-template-that-is-owned-by-another-provider"></a>Breyta sniðmáti sem er í eigu annarrar veitu

Þetta dæmi sýnir hvernig á að nota hnappinn **Nýtt skjal** á vinnusvæðinu **Stjórnun viðskiptaskjala** til að búa til og breyta sniðmáti í skilgreiningu snið rafrænnar skýrslugerðar sem er frá annarri veitu og stað í núverandi tilvik Finance. Í þessu dæmi er virka veitan Contoso, sem notar skilgreiningu rafræns skýrslugerðarsniðs sem Microsoft býður upp á. Þegar þú hefur valið **Nýtt skjal** sýnir flipinn **Velja** á síðunni **Búa til nýtt sniðmát** öll sniðmát núverandi tilviks af Finance sem eru í eigu núverandi veitu og annarra veitna. Velja sniðmát til að opna það. Hægt er að búa til nýtt afrit af sniðmátinu sem hægt er að breyta. Breytta sniðmátið er geymt í nýrri skilgreiningu á ER-sniði sem er sjálfkrafa mynduð.

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.

    ![Vinnusvæðið Yfirlit yfir stjórnun viðskiptaskjala.](./media/BDM_overview_new_template1.png)

2. Á **Stofna nýtt sniðmát** síðunni á **Velja** skal velja skjalið til að nota sem sniðmát og síðan velja **Stofna skjal**.

    ![Gluggi viðskiptaskjala.](./media/BDM_overview_new_template2.png)

3. Í nýja glugganum, í reitnum **Titill**, breytirðu titlinum eins og þú þarfnast. Titiltextinn er notaður til að nefna nýju skilgreiningu ER-sniðsins sem er sjálfkrafa búin til. Drög að þessari skilgreiningu (**Afrit af skýrslu viðskiptamannareiknings með frjálsum texta (GER)**) sem munu innihalda breytt sniðmát og verða notuð til að keyra þetta ER-snið fyrir núverandi notanda. Hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.
4. Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður sjálfkrafa stofnað.
5. Í reitnum **Athugasemd** skaltu uppfæra athugasemdinar fyrir breytanlega endurskoðun sem verður sjálfkrafa stofnuð.
6. Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

    ![Stofngluggi skjalagerðar.](./media/BDM_overview_new_template3.png)

## <a name="upload-a-template-that-uses-an-existing-excel-workbook"></a>Hlaða upp sniðmáti sem notar fyrirliggjandi Excel-vinnubók

Þetta dæmi sýnir hvernig á að nota hnappinn **Nýtt skjal** á vinnusvæðinu **Stjórnun viðskiptaskjala** til að búa til og breyta sniðmáti í skilgreiningu rafræns skýrslugerðarsniðs samkvæmt tiltækri Excel-vinnubók. Í þessu dæmi er virka veitan Contoso og skilgreiningar fyrir [gagnalíkan](er-overview-components.md#data-model-component) og [líkanavörpun](er-overview-components.md#model-mapping-component) rafrænnar skýrslugerðar eru notaðar sem Microsoft býður upp á. Eftir að þú hefur valið **Nýtt skjal** skaltu velja flipann **Hlaða upp** á síðunni **Búa til nýtt sniðmát**. Þar er hægt að tilgreina upplýsingar um upphleðslu Excel vinnubókar. Eftir að þú hleður upp Excel-vinnubókinni er henni umbreytt í sniðmát viðskiptaskjals sem er opnað fyrir breytingar. Síðan verður breytt sniðmátið geymt í nýju sniði skilgreiningar rafrænnar skýrslugerðar sem er sjálfkrafa myndað.

Fylgið þessum skrefum til að veita nauðsynlegar upplýsingar áður en sniðmáti er hlaðið upp.

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.
2. Á síðunni **Búa til nýtt sniðmát**, í flipanum **Hlaða upp**, í flipanum **Sniðmát**, skal velja **Fletta** til að finna og velja Excel-skrána sem á að nota sem sniðmát. Í hlutanum **Sniðmát** er sjálfkrafa fyllt inn í reitina **Titill** og **Lýsing**. Þeir tilgreina heiti og lýsingu á nýrri skilgreiningu rafræns skýrslugerðarsniðs sem er sjálfkrafa búið til. Hægt er að breyta þessum reitum eftir þörfum.
3. Í hlutanum **Skjalagerð**, í reitnum **Heiti**, skal tilgreina gerð viðskiptaskjalsins. Þetta gildi verður notað til að leita að réttri gagnaveitu (þ.e. skilgreiningu rafræns skýrslugerðarlíkans).

    ![Sniðmátsflipi á upphleðsluflipanum á síðunni Búa til nýtt sniðmát.](./media/BDM_overview_new_UI_import_21.jpg)

4. Í flipanum **Gagnaveita**, í flýtiflipanum **Sía**, skal velja **Nota síu**. Í hlutanum **Gagnaveita**, er fyllt inn sjálfkrafa í reitinn **Heiti** eða hægt er að velja gildi handvirkt. Hægt er að nota síuna til að leita að viðeigandi heiti gagnaveitu eftir heiti, lýsingu, lands-/svæðiskóða og gerð viðskiptaskjals.

    ![Gagnagjafaflipi á upphleðsluflipanum á síðunni Búa til nýtt sniðmát.](./media/BDM_overview_new_UI_import_31.jpg)

    > [!NOTE]
    > Flýtiflipinn **Sía** er notuð til að leita að réttri gagnaveitu (þ.e. skilgreiningu rafræns skýrslugerðarlíkans). Hægt er að breyta öllum síureitum til að finna hentugustu gagnaveituna fyrir skjalið sem hlaðið er upp.
    > 
    > Skilyrðin í flýtiflipanum **Sía** eru notuð sem **EÐA** skilyrði.

5. Í flipanum **Vörpun** skal velja **Greina sjálfvirkt**. Reiturinn **Skilgreining rótar** er sjálfkrafa fylltur út eða hægt er að velja gildi handvirkt. Þessi flipi sýnir endavörpun eininganna úr sniðmátinu og líkaninu.

    ![Vörpunarflipi á upphleðsluflipanum á síðunni Búa til nýtt sniðmát.](./media/BDM_overview_new_UI_import_41.jpg)

    > [!NOTE]
    > Vörpunin í hlutanum **Skipulag sniðmáts** notar fulla samsvörun á merkjum eða lýsingum í gagnaveitunni á tungumáli notanda og í heiti hólfs í sniðmátinu.

6. Veljið **Stofna skjal** til að staðfesta að ætlunin sé að stofna sniðmát og hefja breytingarferlið.

Fyrir frekari upplýsingar, sjá [Yfirlit yfir stjórnun viðskiptaskjala](er-business-document-management.md).

## <a name="upload-a-template-from-the-global-repository"></a>Hlaða upp sniðmáti úr altækri geymslu

Þetta dæmi sýnir hvernig á að nota hnappinn **Nýtt skjal** á vinnusvæðinu **Stjórnun viðskiptaskjala** til að búa til og breyta sniðmáti í skilgreiningu rafræns skýrslugerðarsniðs sem Microsoft býður upp á og er staðsett í altæku geymslunni. Í þessu dæmi er virka veitan Contoso, sem notar skilgreiningu rafræns skýrslugerðarsniðs sem Microsoft býður upp á. Þegar **Nýtt skjal** er valið sýnir flipinn **Flytja inn úr altækri geymslu** á síðunni **Búa til nýtt sniðmát** öll sniðmát viðskiptaskjala sem eru geymd í altæku geymslunni en vantar í núverandi Finance-tilviki. Eftir að þú hefur valið sniðmát er það flutt úr altæku geymslunni og inn í núverandi Finance-tilvik til að búa til nýtt breytanlegt afrit. Breytta sniðmátið er geymt í nýrri skilgreiningu á ER-sniði sem er sjálfkrafa mynduð.

1. Í vinnusvæðinu **Stjórnun viðskiptaskjala** velurðu **Nýtt skjal**.
2. Á síðunni **Stofna nýtt sniðmát** á flipanum **Flytja inn úr altækri geymslu** skal velja skjalið til að nota sem sniðmát og síðan velja **Stofna skjal**.

    ![Flytja inn af flipa altækrar geymslu á síðunni Búa til nýtt sniðmát.](./media/BDM_overview_new_template22.png)

3. Í skilaboðaglugganum skal velja **Já** til að staðfesta að þú viljir flytja inn valið skjal úr altæku geymslunni í núverandi Finance-tilvik. Ef þú ert beðinn um heimild skaltu fylgja leiðbeiningunum á skjánum.
4. Í nýja glugganum, í reitnum **Titill**, breytirðu titlinum eins og þú þarfnast. Titiltextinn er notaður til að nefna nýju skilgreiningu ER-sniðsins sem er sjálfkrafa búin til. Drög að þessari skilgreiningu (**Afrit innheimtubréfi (Excel)**) sem munu innihalda breytt sniðmát og verða notuð til að keyra þetta ER-snið fyrir núverandi notanda. Hið óbreytta upprunalega sniðmát úr grunnstillingu ER-sniðsins notað til að keyra þetta ER-snið fyrir alla aðra notendur.
5. Í reitnum **Heiti** breytirðu heiti fyrstu endurskoðunar á breyttu sniðmátinu sem verður sjálfkrafa stofnað.
6. Í reitnum **Athugasemd** skaltu uppfæra athugasemdinar fyrir breytanlega endurskoðun sem verður sjálfkrafa stofnuð.
7. Veldu **Í lagi** til að staðfesta upphaf breytingarferilsins.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

