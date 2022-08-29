---
title: Setja upp og stjórna myndum fyrir Modern POS (MPOS)
description: Þessi grein útskýrir þrepin sem á þarf að halda fyrir uppsetningu og umsjón með myndum fyrir hinar ýmsu einingar sem koma fram í Modern POS (MPOS).
author: josaw1
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.industry: Retail
ms.search.form: RetailChannelProfile, RetailMediaGallery, RetailImages,
ms.openlocfilehash: f282c163ef5a74283231492e499201c6d4619115
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287512"
---
# <a name="set-up-and-manage-images-for-modern-pos-mpos"></a>Setja upp og stjórna myndum fyrir Modern POS (MPOS)

[!include [banner](includes/banner.md)]

Þessi grein útskýrir þrepin sem á þarf að halda fyrir uppsetningu og umsjón með myndum fyrir hinar ýmsu einingar sem koma fram í Modern POS (MPOS).

## <a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>Setja upp Grunnvefslóð miðla og skilgreina miðlasniðmát til að skilgreina snið fyrir Vefslóðir mynda

Myndir sem birtast í Modern POS (MPOS) verður að vera hýst í ytra kerfi, utan Commerce. Yfirleitt, eru þær hýst í efnisstýringarkerfi, efnisafhendingarneti (CDN) eða miðlaþjóni. MPOS sækir síðan og birtir myndir fyrir viðeigandi aðila, eins og afurðir og vörulista, með því að opna markvefslóðina. Til að ná í þessar myndir hýstar ytra, krefst MPOS rétt snið Vefslóðar fyrir myndirnar. Hægt er að skilgreina áskilið snið Vefslóðar fyrir myndirnar með því að setja upp gildi fyrir **grunnvefslóð Miðla** í rásarforstillingin og nota **Skilgreina sniðmát miðla** aðgerðir fyrir hverja einingu. Einnig er hægt að skrifa yfir staðlaða snið Vefslóðar fyrir hlutmengi einingar með því að nota **Breyta í Excel** virkni.

> [!IMPORTANT]
> Í núgildandi útgáfu af Commerce er ekki lengur hægt að setja upp snið fyrir vefslóð með því að nota XML eigindina **Mynd** fyrir MPOS í eigindaflokknum **Sjálfgefið** fyrir einingar. Ef þú þekkir Microsoft Dynamics AX 2012 R3 og er nú að nota gildandi útgáfu af Commerce gangið úr skugga að nota alltaf nýja **Skilgreina sniðmát miðla** aðgerðir til að setja upp myndir. Ekki nota eða breyta **Mynd** eiginda í á **Sjálfgefin** eigindaflokkur fyrir neinar einingar, þar á meðal afurðir. Breytingar sem gerðar beint í í **Sjálfgefin** eigindaflokkur fyrir myndir munu ekki endurspeglast. Þessi valkostur verður gerð óvirk í framtíðarútgáfu.

Í eftirfarandi ferli eru myndir settar upp fyrir eininguna Vörulisti sem dæmi. Þessar aðgerðir hjálpar tryggja að rétt slóð fyrir ákvörðunarstað myndar er stillt skilyrðislaust fyrir allar myndir vörulista sem nota sameiginlega slóð. Til dæmis, ef búið er að setja upp miðlaþjón eða CDN ytra, og myndir eiga að birtast í MPOS fyrir tiltekið verslun, hjálpar **Skilgreina sniðmát miðla** virkni til við að stilla slóðina þar sem MPOS getur fletta upp og sækja myndirnar.

> [!NOTE]
> Fyrir þessi sýnigögn er miðlaþjónninn virkjaður á Commerce Scale Unit. Hins vegar er hægt að hafa það hvar sem er utan Commerce.

### <a name="set-up-the-media-base-url-for-a-channel"></a>Setja upp Grunnvefslóð miðla fyrir rás

1. Opna Commerce-gátt höfuðstöðvar.
2. Smellið á **Retail og Commerce** &gt; **Rásaruppsetning** &gt; **Forstillingar rásar**.

    [![Fletting.](./media/channel-profile1.png)](./media/channel-profile1.png)

3. Í forstilling rásar sem verslunin notar fyrir MPOS, uppfærðu **grunnvefslóð Miðla** reitinn með Grunnvefslóð miðlaþjónsins eða CDN. Grunnvefslóð (url) er fyrsti hluti Vefslóð sem eru sameiginlegar öllum myndamöppur úr mismunandi einingum.

    [![Notandasíða rásar.](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>Skilgreina sniðmát miðla fyrir einingu

1. Smellið á **Retail og Commerce** &gt; **Vörulistastjórnun** &gt; **Vörulistamyndir**.
2. Á **Vörulistamyndir** síðuna á Aðgerðasvæðinu skal smellt **Skilgreina sniðmát miðla**. á **Skilgreina sniðmát miðla** svarglugganum í **Einingar** svæðinu ætti **Vörulista** að vera valinn að sjálfgefnu.
3. Á við **slóð Miðils** flýtiflipa, færið inn eftirstandandi slóð staðsetningar myndar. Slóð miðils styður **LanguageID** sem breytu. Fyrir sýnigögn er til dæmis hægt að stofna **Vörulista** möppu fyrir allar vörulistamyndir undir grunnvefslóð miðils fyrir miðlaþjón (`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`). Hægt er að hafa möppu fyrir hvert tungumál eins og is-IS eða fr-FR og afrita viðeigandi myndir í hverri möppu. Ef þú ert ekki með mismunandi myndir fyrir mismunandi tungumálum, er hægt að sleppa **LanguageID** breytu úr möppuskipulag- og vísa beint í Vörulistamöppuna sem inniheldur myndir vörulista.

    > [!NOTE]
    > Ábending: gildandi útgáfu af Commerce styður táknið **{LanguageId}** fyrir einingar Vörulista, Afurðar og Tegundar. (**{LanguageID}** tákn er ekki stutt fyrir einingar Viðskiptavinur og Starfsmaður, samkvæmt staðli sem hefur verið virkur frá Microsoft Dynamics AX 6.x.)

4. Fyrir Myndir er skrárheitissniðið harðkóðaða í heiti vörulista og ekki er hægt að breyta. Þess vegna skal endurnefna myndir þannig að þeir hafi viðeigandi vörulistanöfn til að aðstoða við að tryggja að MPOS annast þær rétt.
5. Í **Nafnauka skrár** skal velja áætluð nafnauka skrár, eftir gerð myndir sem þú ert með. Til dæmis, í sýnigögnum, eru myndir í vörulista stillt á nafnauka .jpg. (Myndaskrár eru einnig endurnefnd þannig að þeir hafa nöfn vörulista).
6. Smellið á **Í lagi**.
7. Til að staðfesta að sniðmát miðla fyrir myndum hefur verið vistuð rétt, á **Vörulistamyndir** síðunni er smellt á **Skilgreina sniðmát miðla** aftur. Til að villuleita sniðmát án þess að loka **Skilgreina sniðmát miðla** svarglugganum, er hægt að nota **Mynda Myndvefslóðir fyrir Excel** flýtiflipi. Athuga útlit útlit og myndvefslóðar, og staðfesta að vefslóð samræmist staðlaða sniðmátið sem var áður nefnd. **Skilgreina sniðmát miðla** svarglugga hefur nú sett slóð mynda skilyrðislaust fyrir allar vörulistamyndir sem nota þessa sameiginlegu Vefslóð (url). Þessari Vefslóð (url) á við allar myndir vörulista nema skrifað sé yfir hana. Fyrsti hluti myndaslóð er sótt í Grunnvefslóð miðla sem er skilgreind í forstillingu rásar. Eftirstandandi hluta slóð er sótt úr slóðina sem var skilgreint í sniðmáti miðla. Hlutarnir tveir eru eige eingöngu að veita þér staðsetningar fulla vefslóð myndar . Til dæmis er vörulista í sýnigögnin sem nefnist Fabrikam Grunnvörulista. Þess vegna þarf heiti myndar að vera Fabrikam grunnvörulisti.jpg þannig að það notar heiti vörulista og .jpg skrárendingu sem er skilgreindur í sniðmátinu. Eftir samtengingu verður vefslóðin `https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`.
8. Keyra samstillingarvinnslu til að færa nýja sniðmátið í gagnagrunn rásar þannig að MPOS geti notað sniðmátið til að fá aðgang að myndirnar.
9. Til að uppfæra miðlasniðmát fyrir vörulistamyndir rásarmegin skal gæta þess að keyra **Vörulistavinnsla 1150** úr **Upplýsingatækni í Retail og Commerce** &gt; **Dreifingaráætlun**.

    [![Skilgreina svarglugga fyrir sniðmát miðla.](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Forskoðun myndar af stigi einingar

1. Frá síðunni fyrir vörueiningu í HQ (höfuðstöðvar) er hægt að forskoða mynd sem notar vefslóð myndar sem er fengin úr sniðmáti miðla. Í þessu dæmi skal fara á viðeigandi vörulista og síðan, í aðgerðasvæðinu, smella á **Miðlar** &gt; **Myndir**. Nota fellilistanum til að velja mismunandi verslanir sem gætu haft mismunandi forstillingar rásar .
2. Til að breyta eða fjarlægja óbeina sniðmát miðla, verður að fara aftur í **Skilgreina sniðmát miðla** svarglugga fyrir **Vörulista myndir** síðu.
3. Hægt er að nota **Bæta við** og **Fjarlægja** hnappana til að breyta handvirkt slóðin sem er byggð á óbeina sniðmátinu og notað fyrir tiltekna mynd. Nánari upplýsingar er að finna í hlutanum [Skrifa yfir sniðmát miðils fyrir afurðaeiningar](#overwriting-the-media-template-for-entity-items) síðar í þessari grein.
4. Eftir hefur verið lokið forskoðun myndar og gera breytingar sem þarf, byrja MPOS tilvik fyrir viðkomandi verslun og sjá hvort myndir í vörulista eru sýndar.

    [![Svargluggi mynda.](./media/catalog4.png)](./media/catalog4.png)

> [!NOTE]
> Hægt er að nota sömu aðferð fyrir allar fimm einingar sem eru studdar: Starfsmann, Viðskiptavin, Vörulista, Tegund og Afurðir. "vörulistaafurðir" (afurðir sem eru sett á stigi vörulista) og "Rásarafurða" (afurðir sem eru sett á stigi rásar) nota sniðmát miðilsins sem er sett upp fyrir Afurðareiningar. Fyrir Afurðasniðmát miðla er hægt að velja fjölda afurðamynda til að sýna fyrir hverja afurð. Einnig er hægt að stilla sjálfgefna mynd fyrir tiltekna vöru. Á þennan hátt er hægt að koma í veg fyrir að autt myndir í MPOS og hjálp til að stjórna hvaða mynd er notað sem sjálfgefin mynd fyrir afurðavara. Í eftirfarandi dæmi hefur hverja afurð fimm myndir og fyrsta mynd er stillt sem sjálfgefin mynd. Afurðarafbrigði eru meðhöndlaðar á sama hátt og aðalafurð. Skrárheiti myndskráa ættu að byggja á afurðarnúmer. Sumir stafir eru einnig ekki hafðir með á meðan skrárheiti er mynduð. Því er gott að staðfesta skrárheiti með því að nota **Mynda Vefslóðir mynda fyrir Excel** hluta. Sjá kaflann [Yfirskrifa með því að nota Breyta í Excel](#overwrite-by-using-edit-in-excel) síðar í þessari grein.

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Samstillingarvinnslur til að senda sniðmát miðla í hlið rásar

Fyrir allar fimm studdar einingar (Starfsmann, Viðskiptavin, Vörulista, Tegund og Afurðir), ætíð þegar svarglugginn **Skilgreina sniðmát miðla** er uppfærður til að setja upp mynd, gangið þá úr skugga um að vörulistavinnslan (1150) er keyrð úr **Upplýsingatækni Retail og Commerce** &gt; **Dreifingaráætlun**. Þessi vinnsla virkjar uppfærða miðla sniðmátið sem á að vera samstillt við rásina og notað af MPOS. Keyra Vörulistavinnslu (1150) eftir að þú gera eitthvað af eftirfarandi breytingum:

- Þú uppfærir miðlasniðmát Vörulistamyndar úr **Vörulistamyndir** &gt; **Skilgreina sniðmát miðla**.
- Þú uppfærir miðlasniðmát starfsmannamyndar úr **Starfsmannamyndir** &gt; **Skilgreina sniðmát miðla**.
- Þú uppfærir miðlasniðmát viðskiptavinamyndar úr **Viðskiptavinamyndir** &gt; **Skilgreina sniðmát miðla**.
- Þú uppfærir miðlasniðmát afurðarmyndar úr **Afurðarmyndir** &gt; **Skilgreina sniðmát miðla**.
- Þú uppfærir miðlasniðmát tegundamyndar úr **Tegundamyndir** &gt; **Skilgreina sniðmát miðla**. Einnig verður að birta rásina.

## <a name="overwriting-the-media-template-for-entity-items"></a>Skrifa yfir miðlasniðmát fyrir afurðareiningu

Eins og þú lærðir í fyrri hluta, styður miðlasniðmát fyrir tiltekna einingu aðeins einn sameiginlega slóð. Þessi slóð er byggð á Grunnvefslóð miðla sem er skilgreindur og miðils slóð sem er skilgreint. Hins vegar í mörgum tilvikum vill smásali geta notað myndir úr öðrum uppruna fyrir hlutmengi vara í einingu. Til dæmis notar verslun miðlaþjón sem hún hýsir sjálf fyrir eitt safn vörulistamynda en notar Vefslóðir CDN fyrir annað safn. Til að skrifa yfir Vefslóðir mynda sem eru byggð á sniðmáti miðla fyrir einingamyndir á stigi einingar, getur þú notað Breyta í Excel og handvirka breytieiginleika úr **Forskoðun** síðu.

### <a name="overwrite-by-using-edit-in-excel"></a>Yfirskrifa með því að nota Breyta í Excel

1. Smellið á **Retail og Commerce** &gt; **Vörulistastjórnun** &gt; **Vörulistamyndir**.
2. Á **Vörulistamyndir** síðuna skal smellt **Skilgreina sniðmát miðla**. Í **Skilgreina sniðmát miðla** svarglugganum í **Einingar** svæðinu, ætti að vera valinn **Vörulista** .
3. Á **slóð Miðils** flýtiflipi, athugið staðsetningu myndar.
4. Á við **Mynda Vefslóðir Myndar fyrir Excel** flýtiflipa, smellið á **Mynda**.

    > [!IMPORTANT]
    > Hvenær sem sniðmát miðils er breytt þarf að smella á **Mynda** áður en hægt er að nota Breyta í Excel eiginleika.

    Nú sérðu forskoðun á vefslóðum mynda sem voru búnir til samkvæmt síðasta vistaða miðla sniðmáti.

    [![Búa til vefslóðir myndar fyrir Excel flýtiflipa eftir að Búa til hefur verið valið.](./media/excel2.png)](./media/excel2.png)

    > [!NOTE]
    > Vefslóðir sem eru myndaðar fyrir Excel nota slóð og reglur sniðmáts fyrir miðil sem er skilgreindur. Þessar reglur eru innihalda reglur fyrir skrárheiti. Ætlast er til að þú hafir setja upp efnislegar myndir utan Commerce, og myndirnar er hægt að sækja úr Vefslóðir sem eru fengin úr sniðmáti miðla sem eru skilgreindar áður. Hægt er að skrifa yfir þessar afleiddar Vefslóðir með því að nota Breyta í Excel eiginleikann.

5. Smella á **Breyta í Excel**.
6. Eftir að Microsoft Excel vinnublaðið er opnað, er smellt á **Kveikja á breytingu** þegar um er beðið.
7. Þegar um er beðið, smellið á **Treysta þessari viðbót** í hægri rúðunni og bíða eftir að viðbótin ljúka uppsetningunni.

    [![Treysta þessari innbót.](./media/excel4.jpg)](./media/excel4.jpg)

8. Ef beðið er um á innskráningu, færið inn skilríki sem er notuð til að skrá sig í HQ (höfuðstöðvar).

    [![Kvaðning um innskráningu.](./media/excel5.png)](./media/excel5.png)

9. Eftir að skrá inn ætti að vera unnt að sjá lista yfir Vefslóðir mynda fyrir mismunandi færslur í vörulista.
10. Þú breyta, bæta við og fjarlægja vefslóðir mynda fyrir ýmsar einingaafurðir.
11. Fyrir allar einingar nema Afurðir er hægt að yfirskrifa Vefslóðir mynda. Breyta fyrirliggjandi Vefslóð myndar , þannig að það notar nýja áfangastað Vefslóðar myndarinnar og uppfæra skrárheiti með nýja skráarnafn fyrir myndaskrá. Skrárnafn verður að vera einkvæmt til að aðstoða við að tryggja að færslan sé einkvæm.

    [![Skrifa yfir Vefslóðir myndar í Excel.](./media/excel6.jpg)](./media/excel6.jpg)

    > [!NOTE]
    > Þegar skrifað er yfir myndir vefslóða fyrir afurðaeiningar með því að nota Breyta í Excel-virkni eða síðuna vörueining, sýnir MPOS alltaf vefslóðir mynda miðlasniðmáts ásamt yfirskrifuðum vefslóðum mynda.

12. Eftir að lokið hefur verið við breytingar skal smella á **Birta í Excel** til að stofna nýja skilyrðislausa teningarfærslu.
13. Fara aftur í HQ og smella á **í lagi**.
14. Keyra viðeigandi samstillingarvinnslu fyrir eininguna og athuga forskoðun á einingarsíðu eða MPOS.

#### <a name="creating-new-records"></a>Nýjar færslur stofnaðar

Hægt er að stofna nýjar færslur í Excel. Hins vegar skal tryggja að veita réttum upplýsingum. Til dæmis til að stofna nýja færslu fyrir vörulista, gangið úr skugga um að Kenni vörulista og heiti vörulista séu rétt og veittu einnig einkvæmt skráarheiti. Einkvæmt skráarheiti er mjög mikilvægt, þar sem einkvæmni færslna í Excel eru villuleitaður við birtingu. Fyrst skal afrita upplýsingar úr vörulista sem á að stofna nýja færslu fyrir, og afrita færslunni. Einungis þarf að uppfæra skráarheitið og SLÓÐIN, þar sem aðrar upplýsingar verða sama. Til að stofna nýjar færslur fyrir afurðareiningar, notarðu sömu grunn aðferð . Úr Excel-vinnublað skal afrita úr fyrirliggjandi skrá fyrir afurðina sem á að stofna nýja færslu fyrir, og skipta síðan út SLÓÐ myndar og skrárheiti. Gangið úr skugga um að heiti skrárinnar sé einkvæmt.

#### <a name="deleting-an-existing-record"></a>Eyðir fyrirliggjandi færslu

Aðeins færslur yfirskrifað Vefslóð myndar er hægt að eyða. Eftir að mynd hefur verið eytt og samstillingu er lokið, mynd verður ekki lengur birtast á **Forskoðun** síðu eða MPOS. Ekki hægt að eyða skrám fyrir vefslóðir mynda sem eru leiddar af miðlasniðmát þar sem þessar skrár eru fengin úr miðlasniðmáti í hvert skipti.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Skrifa yfir úr forskoðunarsíðu á stigi einingar

Fyrir allar einingar nema Afurðir er hægt að yfirskrifa vefslóð myndar fyrir tiltekna afurðareiningu á stigi afurðareiningar úr **Forskoðunar** síðu. Fyrir Vörur má nota einingarsíða "Vörulistavörur". Þetta dæmi sýnir hvernig á að skrifa yfir vörulistamynd.

1. Smellið á **Vörulista** &gt; **Miðla** &gt; **Myndir**, og velja vörulistamynd til að uppfæra.
2. Smellið á **Bæta við**, og færið inn Vefslóð myndar til að skrifa yfir vefslóð miðlasniðmáts.
3. Ef þessari mynd á að birtast í MPOS fyrir vörulistinn, er hægt að setja hana sem sjálfgefna mynd.
4. Smelltu á **Í lagi**. Vefslóð myndar uppfærist fyrir þessa vörulistamynd og forskoðun birtist.

    [![Vefslóð uppfærð í svarglugga nýrrar myndar.](./media/preview3.png)](./media/preview3.png)

5. Einnig er hægt að skoða forskoðun myndar fyrir öll yfirskrifað Vefslóðir myndar á **Vörulistamyndir** galleríssíðu.

    [![Vörulistamyndir galleríssíðu.](./media/preview-4.png)](./media/preview-4.png)

> [!NOTE]
> Eins og er birtir galleríið ekki forskoðun myndar fyrir miðilssniðmát fyrir vefslóðir myndar. Fyrir einingar Vörulista, Starfsmaður, Viðskiptavinur og Tegund , ef notandinn veitir sérstaklega Vefslóð með þessari síðu er mælt með því að tilgreina hvaða mynd er sjálfgefna myndin, þar sem biðlarar Commerce Scale Unit sýna aðeins eina mynd fyrir hvern Vörulista, Viðskiptavinur, Starfsmann og Tegund. Ef notanda ekki tilgreina sjálfgefna mynd, kerfið ákvarðar sjálfgefna mynd og senda hana til kallara Commerce-þjónustu (MPOS eða Ecommerce).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Skrifa yfir vefslóð myndar fyrir myndir vörulistaafurðarinnar frá síðunni Forskoðun

Til að Skrifa yfir vefslóð myndar fyrir myndir vörulistaafurðarinnar, verður að nota síðuna **Forskoðun** Ekki er hægt að nota eiginleikann Breyta í Excel

1. Til að skrifa yfir mynd afurðar á stigi vörulista, veljið vörulista og veljið svo að afurð til að skrifa yfir myndina fyrir.
2. Smellið á **Eigindir**.
3. Á næstu síðu, veldu **mynd**, og smelltu svo á **Breyta**. **Forskoðun** síðan opnast sem sleðasvarglugga.
4. Smellið á **Bæta við**, og skrifa yfir vefslóð myndar með nýja vefslóð.
5. Smelltu á **Í lagi**. Þú sérð nú forskoðun á ný mynd og hægt er að stilla hana sem sjálfgefna mynd.

    [![Forskoðun á mynd í svarglugga nýrrar myndar.](./media/cat3.png)](./media/cat3.png)

> [!NOTE]
> Eftir myndtengingu við flokk verður að birta rás og keyra Rásarvinnsluna til að aðstoða við að tryggja að breytingarnar séu birtar í gagnagrunn rásar.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Setja upp myndir sem birtast í ótengdri stillingu fyrir MPOS

MPOS hægt er að keyra í Nettengda stillingu (þegar MPOS er tengt við Commerce Scale Unit) eða ótengd stilling (þegar það er engin Commerce Scale Unit eða nettenging og færslur eru vistaðar í staðbundna ótengdan gagnagrunn). Þegar MPOS keyrir í ótengdum ham, getur hann ekki fá myndir frá ytri myndþjóni til að birta úr Commerce scale Unit þar sem tengingar hafa glatast. Hins vegar hægt samt að setja upp myndir þannig að þær séu sýndar þegar MPOS er keyrt án tengingar.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>Setja upp myndir til að birtast í Ótengda stillingu fyrir MPOS

Myndir afurðar sem þarf að nota í ótengdum ham má setja upp með því að hlaða upp efnislegum myndum sem krafist er í grunnmyndir afurðar.

1. Smellið á **upplýsingastjórnun afurða** &gt; **Afurðir** &gt; **Afurðir**.
2. Veljið afurð til að stilla ótengda mynd fyrir.
3. Smellið á **Breyta**, og smellið síðan á ör í hægri horninu til að sýna á hægri rúðunni.
4. Á **mynd Afurðar** flýtiflipi, smellið á **breyta mynd**, og hlaða upp efnislegt mynd sem nota á fyrir valda afurð í Ótengda stillingu.
5. Vistið og lokið síðunni.
6. Á meðan MPOS er í tengdum ham, keyrðu vörulistavinnslu í HQ til að tryggja að gögnin séu send að minnsta kosti einu sinni í ótengdur gagnagrunnur
7. Setja MPOS í Ótengda stillingu. Þú ættir að sjá mynd sem hlaðið er upp fyrir tiltekna vöru í HQ.

    [![Mynd afurðar í stillingu án tengingar.](./media/offline1.png)](./media/offline1.png)

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Setja upp myndir vörulista, tegund, starfsmanna og viðskiptavina sem birtast í Ótengda stillingu fyrir MPOS

myndir Vörulista, tegund, starfsmanni og viðskiptavinarins sem verður notaður í ótengdum ham má setja upp með því að bæta við tengli í staðsetningu í galleríi og myndin er stillt sem sjálfgefin mynd fyrir valda einingu.

1. Farið í vörulistann, og smeillið á **Miðill** &gt; **Myndir** á aðgerðarúðunni.
2. Fylgið skrefunum í hlutanum [Yfirskrift úr forskoðunarsíða á stigi einingar](#overwrite-from-the-entity-level-preview-page) til að bæta við ytri vefslóð myndar.
3. Merkja þennan mynd sem sjálfgefna mynd fyrir vörulista með því að velja gátreitinn gagnvart Myndina í hnitanetinu.
4. Keyra vörulistavinnslu. Þessi mynd verður nú notuð Ótengd mynd fyrir þennan vörulista í MPOS.
5. Fylgja svipuð ferli fyrir aðrar einingar eins og Tegunda, Starfsmanna og Viðskiptavina.

    [![Mynd án nettengingar.](./media/offline2.png)](./media/offline2.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
