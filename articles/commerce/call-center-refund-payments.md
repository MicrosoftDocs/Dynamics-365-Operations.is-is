---
title: Úrvinnsla endurgreiðslu í símaverum
description: Þetta efnisatriði útskýrir hvernig endurgreiðslur eru gerðar gegnum símaver þegar skil eru stofnuð eða þegar hætt er við pantanir eða pöntunarlínur.
author: hhainesms
manager: annbe
ms.date: 01/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3f98fbc14fc2946499a9c003eb0bd0edb7f2017e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991416"
---
# <a name="refund-payment-processing-in-call-centers"></a>Úrvinnsla endurgreiðslu í símaverum

Þetta efnisatriði útskýrir hvernig endurgreiðslur eru gerðar gegnum símaver þegar skil eru stofnuð eða þegar hætt er við pantanir eða pöntunarlínur.

Notandi sem stofnar skilapöntun fyrir viðskiptavin sem notandi símavers í höfuðstöðvum Microsoft Dynamics 365 Commerce notar síðuna **Skilapöntun** til að stofna upprunalega vöruskilaheimild. Vöruskilaheimildin skilgreinir afurðirnar sem viðskiptavinurinn vill skila eða skipta og hún stofnar tengda skilasölupöntun sem er með pöntunargerðina **Skilapöntun**. Þessi tengda skilapöntun er notuð til að rekja bókun á skiluðum birgðum og öllum kreditnótum eða endurgreiðslum sem eru bókaðar.

Ef valkosturinn **Virkja lok pöntunar** er stilltur á **Já** fyrir rás símavers verður notandi símaversins sem stofnar vöruskilaheimildina að keyra vinnsluflæði pöntunarloka með því að velja **Ljúka** á síðunni **Skilapöntun**. Aðgerðin **Ljúka** veitir útreiknaða samantekt skila sem sýnir upphæð endurgreiðslunnar sem þarf að greiða. Auk þess, þegar hún er rétt skilgreind, býr hún til á skipulagðan hátt endurgreiðslulínu á móti skilapöntuninni.

Regla símavers ákvarðar greiðslumáta fyrir endurgreiðslulínuna út frá greiðslumátanum sem notaður var fyrir upprunalegu pöntunina. Ef skilapöntunin sem er stofnuð er ekki tengd við upprunalega pöntun er sjálfgefinn greiðslumáti sem tekinn er frá kerfisfæribreytu notaður.

## <a name="how-a-call-center-determines-which-payment-method-to-apply-to-a-return-order"></a>Hvernig símaver ákvarðar hvaða greiðslumáta á að nota fyrir skilapöntun

Símaverið notar greiðslumáta upprunalegrar pöntunar til að ákvarða greiðslumáta sem á að nota fyrir skilapöntun. Svona virkar þetta ferli fyrir eftirfarandi upprunalega greiðslumáta:

- **Venjulegur** (reiðufé) eða **Ávísun** – Þegar skilapöntun sem er stofnuð vísar í upprunalega pöntun sem var greidd með því að nota venjulega greiðslugerð (reiðufé) eða ávísun, vísar forrit símaversins í skilgreiningar á síðunni **Endurgreiðslumátar símavers**. Þessi síða gerir fyrirtækjum kleift að skilgreina, eftir gjaldmiðli pöntunar, hvernig á að endurgreiða viðskiptavinum fyrir pantanir sem voru upprunalega greiddar með því að nota venjulegu greiðslugerðina eða ávísun. Síðan **Endurgreiðslumátar símavers** gerir fyrirtækjum líka kleift að velja hvort kerfismynduð endurgreiðsluávísun er send til viðskiptavinarins eða hvort inneign á viðskiptavinareikning er búin til á móti innri reikningsstöðu viðskiptavinar. Í þessum aðstæðum vísar regla símavers í gjaldmiðil skilapöntunar og notar síðan gildið **Greiðslumáti fyrir smásölu** fyrir þann gjaldmiðil til að búa til endurgreiðslulínu á skilasölupöntuninni. Síðar meir er greiðslubók viðskiptakrafna viðskiptavinar sem notar varpaðan greiðslumáta viðskiptakrafna tengdur við gjaldmiðilinn.

    Eftirfarandi mynd sýnir skilgreininguna fyrir aðstæður þar sem viðskiptavinur skilar afurðum úr sölupöntun sem er tengd við Bandaríkjadal og sem var upphaflega greidd með því að nota venjulegu greiðslugerðina eða ávísun. Í þessum aðstæðum fær viðskiptavinur endurgreitt í gegnum kerfismyndaða endurgreiðsluávísun. Greiðslumátinn **REF-CHK** fyrir viðskiptakröfur hefur verið skilgreindur sem greiðslugerð endurgreiðsluávísunar.

    ![Skilgreining endurgreiðslumáta símavers fyrir upprunalegar greiðslur sem voru venjulegar eða með ávísun](media/callcenterrefundmethods.png)

- **Kreditkort** – Þegar skilapöntun sem er stofnuð vísar í upprunalega pöntun sem var greidd með kreditkorti, notar regla símavers um endurgreiðslur sama upprunalega kreditkortið á skilapöntunina.
- **Vildarkort** – Þegar skilapöntun sem er stofnuð vísar í upprunalega pöntun sem var greidd með vildarkorti viðskiptavinar, notar regla símavers um endurgreiðslur sama vildarkortið fyrir endurgreiðsluna.
- **Gjafakort** (innra) – Þegar skilapöntun sem er stofnuð vísar í upprunalega pöntun sem var greidd með gjafakorti sem var gefið út af Dynamics 365 Commerce (aðgerð innra gjafakorts), notar regla símavers um endurgreiðslur sama upprunalega gjafakortsnúmerið.
- **Gjafakort** (ytra) – Þegar skilapöntun sem er stofnuð vísar í upprunalega pöntun sem var greidd með ytra gjafakorti þriðja aðila, notar regla símavers um endurgreiðslur sjálfgefinn greiðslumáta sem er skilgreindur í flipanum **Vöruskilaheimild/skil** á síðunni **Færibreytur símavers**.

Ef greiðslugerð upprunalegrar pöntunar er óþekkt af einhverri ástæðu, eða ef margir greiðslumátar voru notaðir til að greiða fyrir upprunalegu pöntunina, notar regla símavers sjálfgefinn endurgreiðslumáta sem er skilgreindur í flipanum **Vöruskilaheimild/skil** á síðunni **Færibreytur símavers**.

Eftirfarandi mynd sýnir reitinn **Greiðslumáti** í flipanum **Vöruskilaheimild/skil** á síðunni **Færibreytur símavers**.

![Reitur greiðslumáta í flipa vöruskilaheimildar/skila á færibreytusíðu símavers](media/callcenterrefundparameters.png)

> [!NOTE]
> Reglur um úrvinnslu endurgreiðslu sem lýst var hér á undan eiga einnig við um pantanir eða pöntunarlínur sem notandi símavers hættir við í Commerce Headquarters. Ef afturköllun pöntunar eða tiltekinna pöntunarlína veldur ofgreiðslum, verða sömu reglur notaðar til að búa til endurgreiðslulínur.

Yfirleitt fer skilapöntun fram í gegnum staðlað ferli þar sem birgðir eru mótteknar (eða rýrnaðar), fylgiseðill er bókaður á móti skilapöntuninni og síðan er bókunarferli reiknings keyrt fyrir skilasölupöntunina. Skilasölupöntun er tengd og mynduð á kerfisbundinn hátt sem hluti af ferlinu við að stofna skilapöntunina. Í dæmigerðum aðstæðum fá viðskiptavinir ekki endurgreitt fyrr en reikningurinn fyrir söluskilapöntunina hefur verið bókaður.

### <a name="what-happens-when-an-invoice-is-posted-on-a-return-sales-order"></a>Þegar reikningur er bókaður á skilasölupöntun:

Eftirfarandi aðstæður útskýra hvað gerist þegar reikningur er bókaður á skilasölupöntun:

- Ef endurgreiðsla skilapöntunar er fyrir kreditkort er viðbótarregla kölluð fram þegar reikningurinn er bókaður. Þessi regla kallar á greiðsluvinnsluna til að endurgreiða inn á kreditkort viðskiptavinar. Fylgiskjal endurgreiðslu viðskiptavinar er líka búið til og bókað af kerfinu á móti reikningi viðskiptavinarins. Þessi greiðslubók verður jöfnuð á móti fylgiskjali fyrir kreditnótu skilapöntunar.
- Ef endurgreiðslan sem þarf að greiða er fyrir ávísun er fylgiskjal viðskiptavinagreiðslu sem notar greiðslumáta viðskiptakrafna stofnað og verður að bóka það handvirkt eða prenta áður en hægt er að bóka greiðslufylgiskjal á móti reikningi viðskiptavinarins. Til að vinna úr ávísun endurgreiðslunnar geta notendur notað annaðhvort síðuna **Greiðslubók viðskiptavinar** í viðskiptakröfum eða sérhæfðu síðuna **Vinnsla á endurgreiðsluávísun** í Smásala og viðskipti.
- Ef endurgreiðslan sem þarf að gefa út er fyrir greiðslugerð innra gjafakorts eða vildarkorts, þegar skilapöntun er reikningsfærð, er fylgiskjal endurgreiðslu stofnað og bókað á móti reikningi viðskiptavinar. Reikningsfærsluskrefið bætir einnig endurgreiðsluupphæðinni aftur við innri rakta stöðu gjafakorts eða vildarpunktastöðu viðskiptavinarins.
- Ef greiðslumáti sem notar aðgerðina **Viðskiptavinur** (t.d. viðskiptavinareikningur) er tengdur við skilasölupöntun eru takmarkanir lánamarka hunsaðar þegar greiðslan er unnin. Engin greiðslufylgiskjöl eru stofnuð eða bókuð í þessu samhengi. Þegar greiðslugerð viðskiptavinar er notuð á skilapöntun þjónar fylgiskjal kreditnótunnar, sem bókunarferli reikningsins stofnar, sem kreditfylgiskjal viðskiptavinar og gefur til kynna endurgreiðslu inn á stöðu viðskiptakrafna viðskiptavinar.

## <a name="advance-credit"></a>Fyrirframkredit

Þegar notandi vinnur úr skilapöntunum sem notandi símavers þar sem valkosturinn **Virkja lok pöntunar** er stilltur á **Já** getur átt sér stað undantekning á fyrra útskýrða ferlinu fyrir bókun endurgreiðslu ef notandi símaversins sem stofnar skilapöntunina stillir valkostinn **Fyrirframkredit** á **Já** í flipanum **Vöruskilaheimild/skil** á síðunni **Færibreytur símavers**. Í þessu tilfelli gerist endurgreiðslan strax eftir að skilapöntunin hefur verið send inn með því að nota aðgerðina **Senda inn** á síðunni **Samantekt skila**. Kerfið stofnar þegar í stað fylgiskjal fyrir fyrirframgreidda viðskiptavinagreiðslu fyrir skilavirðinu, jafnvel þótt söluskilapöntunin sjálf hafi ekki enn verið reikningsfærð. Þessa nálgun er hægt að nota í kringumstæðum þar sem fyrirtæki verður að gefa út endurgreiðslur til viðskiptavina fyrirfram út af málum er varða viðskiptavinaþjónustu og það vill ekki krefjast þess að skilaðar birgðir séu mótteknar áður en endurgreiðslan er gefin út.

## <a name="replacement-orders"></a>Skiptipantanir

Þegar skilapöntun er gefin út er hægt að nota aðgerðina **Skiptipöntun** til að búa til nýja sölupöntun fyrir viðskiptavininn. Þessa leið er hægt að nota þegar verið er að skipta. Aðgerðin **Skiptipöntun** stofnar aðra sölupöntun fyrir nýju vörurnar sem þarf að senda, en millivísunartengill í flipanum **Vöruskilaheimild/skil** á síðunni **Færibreytur símavers** tengir skilapöntunina, vöruskilaheimildina og skilaðri sölupöntun.

Þegar greiðslur á skiptipöntun eru meðhöndlaðar hafa fyrirtæki tvo valmöguleika:

- Endurgreiðið viðskiptavininum vegna skilapöntunarinnar samkvæmt upprunalegum greiðslumáta og rukkið síðan aðskilda greiðslu fyrir skiptipöntunina. Engin viðbótarskilgreining er nauðsynleg til að nota þennan valkost.
- Stillið valkostinn **Nota kredit** á **Já** í flipanum **Vöruskilaheimild/skil** á síðunni **Færibreytur símavers**. Í þessu tilfelli er greiðslumáta viðskiptavinar kerfisbundið notaður fyrir bæði skilapöntun og skiptipöntun. Þessi valkostur getur komið í veg fyrir að ytri endurgreiðsla sé gefin út. Hann getur líka komið í veg fyrir greiðsluvinnslur fyrir færsluna. Hann getur reynst gagnlegur í kringumstæðum þar sem jöfn skipti fara fram og fyrirtækið kýs að nota kreditfylgiskjal sem er búið til þegar skilapöntunin er reikningsfærð til að greiða fyrir reikninginn sem er búinn til af skiptipöntuninni. Þegar valkosturinn **Nota kredit** er stilltur á **Já** verður fyrirtækið að jafna kreditnótuna handvirkt á móti reikningi skiptipöntunarinnar þegar búið er að búa til bæði fjárhagsskjölin.

Stillingin **Já** fyrir valkostinn **Nota kredit** er aðeins í boði þegar skilapöntunin verður tengd við skiptipöntun. Í þessu tilfelli verður greiðslumáti viðskiptavinar, sem verður notaður til að greiða á kerfisbundinn hátt fyrir skila- og skiptipöntun, skilgreindur af reitnum **Nota kreditgreiðsluaðferð** í flipanum **Vörskilaheimild/skil** á síðunni **Færibreytur símavers**. Aðeins er hægt að velja greiðslu af greiðslugerðinni **Viðskiptavinur** í þessum reit.

> [!NOTE]
> Fyrir skilapöntun sem er ekki með tengda skiptipöntun mun stilling á **Já** fyrir valkostinn **Nota kredit** ekki hafa nein áhrif á greiðslureglu skilapöntunar vegna þess að þessi stilling á aðeins við um skiptipantanir.

![Nota reit kreditgreiðsluaðferðar í flipa vöruskilaheimildar/skila á færibreytusíðu símavers](media/callcenterrefundparameters1.png)

> [!IMPORTANT]
> Ef notendur sem stofna áætlun skiptipantana til að nota valkostinn **Nota kredit**, ættu þeir ekki að keyra aðgerðina **Ljúka** fyrir skilapöntunina fyrr en þeir stilla valkostinn **Nota kredit** á **Já**. Þegar aðgerðin **Ljúka** er keyrð, er endurgreiðslan reiknuð út og notuð í skilasölupöntuninni. Allar tilraunir til að stilla valkostinn **Nota kredit** á **Já** þegar útreikningur og notkun endurgreiðslu setur ekki af stað endurútreikning endurgreiðslunnar og greiðslumátinn sem er valinn í reitnum **Nota kreditgreiðsluaðferð** verður ekki notaður. Ef nota þarf valkostinn **Nota kredit** í þessu samhengi, verður notandinn að eyða skiptipöntuninni og vöruskilaheimildinni og byrja síðan upp á nýtt og stofna nýja vöruskilaheimild. Að þessu sinni þarf notandinn að ganga úr skugga um að valkosturinn **Nota kredit** sé stilltur á **Já** áður en aðgerðin **Ljúka** er keyrð.

## <a name="payment-overrides-for-call-center-returns"></a>Greiðsluhnekkingar fyrir skil símavers

Þó svo að regla símavers ákvarðar á kerfisbundinn hátt greiðslumáta endurgreiðslu eins og lýst er fyrr í þessu efnisatriði, gætu notendur stundum viljað hnekkja þessum greiðslum. Til dæmis gæti notandi breytt eða fjarlægt fyrirliggjandi endurgreiðslulínur og sett inn nýjar greiðslulínur. Aðeins notandi, sem er með réttar hnekkingarheimildir, getur breytt endurgreiðslum sem kerfið reiknar út. Þessar heimildir geta verið skilgreindar á síðunni **Hnekkingarheimildir** í Smásala og viðskipti. Til að hnekkja endurgreiðslu verður notandinn að vera tengdur við öryggishlutverk þar sem valkosturinn **Leyfa aðra greiðslu** er stilltur á **Já** á síðunni **Hnekkingarheimildir**.

![Leyfa annan greiðslukost á síðu hnekkingarheimilda](media/overridepermissions.png)

Annars getur fyrirtækið stillt valkostinn **Leyfa að hnekkja greiðslu** á **Já** í flipanum **Vöruskilaheimild/skil** á síðunni **Færibreytur símavers**. Í þessu tilfelli verður að velja hnekkingarkóða öryggis í reitnum **Hnekkingarkóði öryggis**. Hnekkingarkóði öryggis er kóði úr bók- og tölustöfum sem þarf að stýra utan frá vegna þess að notendur geta ekki skoðað hann í Commerce Headquarters þegar hann hefur verið stilltur. Hnekkingarkóði öryggis á aðeins að vera á vitorði fárra traustra lykilstarfsmanna í fyrirtæki. Þegar valkosturinn **Leyfa að hnekkja greiðslu** er stilltur á **Já**, ef einhverjir notendur sem ekki eru með réttar hlutverkaheimildir reyna að breyta greiðslumáta skilapöntunar, munu þeir hafa möguleikann á því að slá inn hnekkingarkóða öryggis. Ef þeir vita hann ekki, eða ef yfirmaður eða umsjónaraðili geta ekki slegið hann inn á tilheyrandi síðu, verður ekki hægt að hnekkja greiðslumáta endurgreiðslunnar.

> [!NOTE]
> Ef hnekkingarkóði öryggis er týndur eða gleymdur þarf fyrirtækið að endurstilla hann með því að skilgreina nýjan hnekkingarkóða öryggis í reitnum **Hnekkingarkóði öryggis** í flipanum **Vöruskilaheimild/skil** á síðunni **Færibreytur símavers**.

![Færibreytur fyrir hnekkingu greiðslumáta í flipa vöruskilaheimildar/skila á færibreytusíðu símavers](media/overridepaymentparameter.png)

> [!IMPORTANT]
> Áður en fyrirtæki reyna að hnekkja endurgreiðslum sem nota kreditkort sem greiðslugerð, ættu þau að ganga úr skugga um að þjónustuaðili kreditkorta leyfi ótengd skil. Margir þjónustuaðilar krefjast þess að endurgreiðslur verði bókaðar aftur á upprunalegt kort. Allar tilraunir til að gefa út endurgreiðslu á kort sem ekki er með fyrri úthlutanir getur valdið villum við bókun hjá þjónustuaðilanum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Greiðslumátar í símaverum](work-with-payments.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]