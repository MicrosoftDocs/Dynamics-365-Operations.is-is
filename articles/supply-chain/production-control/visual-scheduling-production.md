---
title: Gantt-rit fyrir vinnsluröðun
description: Framleiðendur geta stjórnað og hámarkað framleiðsluáætlanir með Gantt-ritum.
author: johanhoffmann
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, ProdTable, ProdTableListPage, GanttColorTable, GanttReqExplosionColor, GanttReqExplosionSetup, GanttTable, GanttTimescaleSetup, GanttWrkCtr, GanttWrkCtrColor, GanttWrkCtrJobInfo, GanttWrkCtrLoadResources, GanttWrkCtrMoveJob, GanttWrkCtrSetup, GanttWrkCtrView
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 180fb7b31ea826c546aa8472a7ef4025a3b8865a783a5b662ed30b69f98acf92
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730203"
---
# <a name="gantt-chart-for-job-scheduling"></a>Gantt-rit fyrir vinnsluröðun

[!include [banner](../includes/banner.md)]

Gantt-línuritið er hannað til að gera framleiðsluskipuleggjendum kleift að stjórna og besta framleiðsluáætlun. Gantt-línuritið gerir aðgerðaflæðið gegnsætt og auðveldar framleiðsluröðun meðan hún tekur með í reikninginn skort á efni eða tilföngum. Þetta hjálpar skipuleggjendum að nota tiltæk tilföng á sem bestan hátt, lágmarka verk í vinnslu og bæta afköst tíma fyrir framleiðslupantanir.

Gantt-línurit er myndræn framsetning á áætluðum verkþáttum innan tilgreinds tímabils. Verkþættirnir raðast á tilföng með afkastaveitu sem er skilgreind í dagatali afkastagetu. Eftirfarandi gerðir aðgerða er hægt að sýna í gantt-línuritinu.

-   Vinnslur úr framleiðslupöntunum sem eru áætlaðar til vinnslu.
-   Vinnslur úr áætluðum framleiðslupöntunum.
-   Verkþættir með áætlaðri vinnslu af gerðinni Tímaspár.

Hægt er að opna Gantt-línuritið á tveimur skjám **Pantanayfirlit** og **Forðayfirlit**. Í **Pantanayfirlit** er virkni flokkuð undir framleiðslupöntunum. Þetta getur verið gagnlegt, til dæmis, ef óskað er að viðhalda yfirsýn yfir allar vinnslur sem tilheyra sömu pöntunum. Í **Yfirlit tilfanga** eru allar vinnslur flokkaðar í stök tilföng. Þetta yfirlit getur verið gagnlegt við hámörkun áætlunar á stigi framleiðslutilfanga, t.d. á vél eða flokki véla. Gantt-línuritin á skýringamyndunum fyrir neðan sýna **Yfirlit pantana** og **Yfirlit tilfanga** með þessum aðalþáttum:

1.  Verkþáttur Gantt-línurits
2.  Efnisskortur tákn
3.  Tákn tiltæks efnis
4.  Tákn afhendingardags pöntunar
5.  Afkastagetustika

## <a name="order-view"></a>Pantanayfirlit

[![Pantanayfirlit.](./media/orderview.png)](./media/orderview.png)

## <a name="resource-view"></a>Forðayfirlit
[![Forðayfirlit.](./media/resview.png)](./media/resview.png)

## <a name="activities"></a>Verkþættir
Verkþættir birtast sem súlur og er raðað upp í tímakvarðalínurit með áætlaðan upphafs- og lokatíma, sme gerir lengd á súlum hlutfallslega við þann tíma sem þarf að ljúka verkþættinum. Aðgerðir eru sýndar samkvæmt tímakvarða. Hægt er að leiðrétta tímakvarðann á valmyndinni þar sem valin er upphafs- og lokadagsetning og tímaeining, til dæmis klukkustundir eða dagar. Með því að aðlaga tímakvarðann má stilla áherslu á tímabil þar sem á að stjórna verkþætti. 

Til að ná betra yfirliti eru mismunandi valkostir til að stýra litum verkþátta. Hægt er að skilgreina stakan lit fyrir verkþætti, nota þemalitinn sem er almennt notaður fyrir forritið eða stilla lit til að stjórna með litakóða fyrir framleiðslupantanir. 

Tímabil fyrir verkþætti sem hafa bakgrunnslit. Tímabil með hvítum skerm gefa til kynna tímabil með skilgreindri afkastagetu á tilfangi fyrir verkþáttinn, en tímabil með gráum skerm gefa til kynna tímabil með enga afkastagetu skilgreinda. 

Vinstra megin á línuritinu eru aukaupplýsingar um verkþáttinn, til dæmis tilföngin þar sem verkþátturinn er áætlaður og framleiðslunúmer pöntunar. Tenging á milli vinnsla sem tilheyra sömu röð er sýnd með ör. 

Hægt er að nálgast frekari upplýsingar um verkþátt í svarglugga verkþáttarins. Til að opna svarglugga er tvísmellt á verkþætti eða valin valmyndin **Upplýsingar**. Í svarglugga verkþáttarins er hægt að áætlaðar upphafs- og lokadagsetningar og tímaupplýsingar um þau efni sem áætlað er að verkþátturinn noti. 

Hægt er að flokka verkþætti í Samansafn stig. Flokkun stig eru stigveldis og hægt er að nota til að gera rök flokkun verkþátta. Til dæmis, ef útlit þar sem framleiðsla verkþættir eru flokkaðir eftir Svæði, framleiðslueiningar Tilfangið flokkana og Tilföng, nota Flokkun stig til að flokka verkþætti samkvæmt þeirri útlit. Flokkunarstigin má stækka og fella saman annaðhvort á stigi staks samansafns eða fyrir öll stig í línuriti með því að nota í **Víkka allt** og **Fella allt** hnappa í valmyndinni. Einnig er hægt að skilgreina flokkunarstig til að víkka út flokkana eða fella þá saman þegar línuritið er opnað.

### <a name="material-availability"></a>Tiltækt efni

Hægt er að setja upp Gantt-línuritið til að veita skipuleggjandanum nákvæmar upplýsingar um efnisstöðu fyrir staka verkþætti. Til dæmis, getur þetta verið gagnlegt ef efni seinkar og það hefur áhrif á framleiðsluáætlunina. Í þessu tilfelli verða efnisvandamálin undirstrikuð í Gantt-línuriti til að auðvelda skipuleggjara að skilja afleiðingar og gera nauðsynlegar leiðréttingar. 

Vinnsla birtist með tákn efnisskorts ef upphafsdagsetning röðunar er síðar en dagsetning efnisframboð fyrir efnið sem var notað í vinnslunni. Efnisframboðsdagsetningin er reiknuð á grundvelli upplýsinga um þarfarakningu í kvikri aðaláætlun. Efnisskortstáknið birtist til dæmis í vinnslu sem er að nota efni sem er þarfarakið gagnvart innkaupapöntun sem hefur móttöku sem er síðar en áætlaður upphafsdagur vinnslu.

### <a name="indicator-of-material-availability-date"></a>Vísir um dagsetningu efnisframboðs

Þegar línurit er sett til að sýna vinnslur með efnisskort er einnig hægt að sýna tákn fyrir dagsetningu efnisframboðs fyrir vinnsluna. Táknið verður einungis sýnt ef efnisframboð er innan tilgreinds tímabils í línuritinu. Ef dagsetning efnisframboðs liggur utan tilgreinds tímabils, er hægt að sækja ítarlegri upplýsingar um efnisframboð úr efnislistanum í svarglugganum vinnslu. Í listanum er einnig tákn sem sýnir seinn efni fyrir vinnslu. Hægt er að endurraða vinnslu með því að nota dagsetningu efnisframboðs sem upphafsdagsetningu.

### <a name="indicator-of-order-delivery-date"></a>Vísir fyrir afhendingardag pöntunar

Þetta tákn tilgreinir afhendingardagsetningu fyrir framleiðslupöntun. Táknið er aðeins sýnilegt í Yfirliti pöntunar.

### <a name="capacity-bar"></a>Afkastagetustika

Hægt er að skilgreina línurit til að sýna afkastaveitustiku tilfanga. Þetta strikamerki veitir yfirlit yfir verkþátt afkastagetu tilfanga eftir tilgreint tímabil í línuritinu. Afkastaveitustikan er ekki sýnd fyrir tímabil fyrir þann tíma þegar tilföngin eru ekki bókuð. Á tímabilum þar sem tilfangið er bókað á afkastagetu, er afkastaveitustikan sýnt sem heil stika. Á tímabilum þar sem tilfangið er ofbókað birtist stikan sem þykkari og í rauðum lit. Til dæmis ef tvær vinnslur skarast sýnir afkastaveitustikan ofbókun á tímabilinu þar sem skörun finnst. Afkastaveitustikan er uppfærð á kvikan hátt þegar vinnslu er raðað. Afkastaveitustikan er virkjuð í valmyndinni **Sýna afkastaveitustiku**. Aðeins er hægt að sýna hana í **Yfirliti tilfanga**. Ef þú vilt fá nákvæmara yfirlit yfir álag á tilföng skaltu nota línuritið **Álag** sem hægt er að opna úr valmyndinni eða samhengisvalmyndinni fyrir valinn verkþátt.

## <a name="job-scheduling-in-the-gantt-chart"></a>Vinnsluröðun í Gantt-línuriti
Gantt-línuritið býður mismunandi valkosti fyrir leiðréttingu á framleiðsluáætlun. Í Gantt-línuriti er hægt að endurraða verkþáttum sem tengslin dragið og sleppið eða úr valmyndinni greiðsluáætlun. Í áætlanagerðinni er hægt að taka afkastaveitu tilfanga, afkastagetu tilfanga og efnisskorður inn í myndina.

### <a name="schedule-a-job-as-a-drag-and-drop-interaction"></a>Raða vinnslu sem tengslin draga og sleppa röðun

Síðan er hægt að endurraða vinnslu innan tiltekins tímabils sem tengslin draga og sleppa. Aðeins er hægt að endurraða vinnslu á sama tilfangið og aðeins er hægt að raða einni vinnslu í einu.

### <a name="schedule-a-job-from-the-menu"></a>Raða vinnslu úr valmynd

Í valmyndinni **Raða vinnslum** er hægt að raða einum eða fleiri völdum vinnslum í línuriti samkvæmt röðunarstefnum og dagsetningu röðunartíma. Þrjár mismunandi áætlunarstefnur eru mögulegar.

-   Áfram frá dagsetningu röðunar
-   Afturábak frá röðunardagsetningu
-   Áframsenda frá dagsetningu framboðs efnis

Ekki er mögulegt að áætla vinnslu utan tilgreinds tímabils Gantt-línuritsins. Ef það er ekki gert verður vinnslan höfð óröðuð og notandi fær villuboðin „Ekki var hægt að raða vinnslu innan hlaðins tímabils.“

### <a name="schedule-previous-jobs"></a>Raða fyrri vinnslum

Í neti verkþátta, eins og vinnslum sem tilheyra sömu framleiðslupöntun, er hægt að nota aðgerðina **Raða fyrri vinnslum** til að raða fyrri vinnslum hlutfallslega við valda vinnslu í netinu. Í eftirfarandi dæmi er auðkenndur verkþáttur valin vinnsla. Skýringarmyndin birtist áður en fyrri vinnsla er áætluð og eftir að síðari vinnsla er áætluð. 

[![Raða fyrri vinnslu.](./media/schprevjob3.png)](./media/schprevjob3.png)

### <a name="schedule-next-jobs"></a>Raða næstu vinnslum

Hægt er að nota aðgerðina **Raða næstu vinnslum** til að raða næstu vinnslum hlutfallslega við valda vinnslu í neti verkþátta. Í eftirfarandi dæmi er auðkenndur verkþáttur valin vinnsla. Skýringarmyndin birtist áður en næsta vinnsla er áætluð og eftir að næsta vinnsla er áætluð. 

[![Raða næstu vinnslu.](./media/schnxtjob.png)](./media/schnxtjob.png)

### <a name="schedule-around-job"></a>Raða kringum starf

Hægt er að nota aðgerðina **Raða með vinnslu** til að raða næstu vinnslu og fyrri vinnslu hlutfallslega við valda vinnslu í neti verkþátta. Í eftirfarandi dæmi er auðkenndur verkþáttur valin vinnsla. Skýringarmyndin birtist áður en vinnsla er áætluð og eftir að vinnsla er áætluð. 

[![Raða kringum vinnslu.](./media/scharoundjob1.png)](./media/scharoundjob1.png)

### <a name="arrange-jobs"></a>Raða störfum

Hægt er að nota aðgerðina **Raða** til að hagræða völdum verkþætti á sama tilfang. Þessar aðgerðir geta verið innan sama nets verkþátta, en geta einnig tilheyrt mismunandi netum. Þegar röðunaraðgerðin er notuð er tímaeyðum á milli valinna verkþátta sleppt. Hægt er að nota þessa aðgerð til að bæta nýtingu afkastaveitu tilfanga. Skýringarmyndin birtist áður en vinnsla er áætluð og eftir að vinnsla er áætluð. 

[![Raða vinnslu.](./media/arrangejobs1.png)](./media/arrangejobs1.png)

### <a name="reassign-activities-from-one-resource-to-another"></a>Endurúthluta verkþáttum úr einum tilföngum í önnur

Hægt er að endurúthluta verkþáttum úr einum tilföngum í önnur. Þetta getur verið gagnlegt í aðstæðum þar sem vél er biluð eða ofbókuð og nauðsynlegt er að finna önnur tiltæk tilföng sem geta gert vinnsluna.

### <a name="reassigning-an-activity-as-a-drag-and-drop-interaction"></a>Endurúthlutun verkþáttar sem draga og sleppa tengslin

Í yfirlitinu **Tilföng** er hægt að endurúthluta verkþætti á annað tilfang í Gantt-línuritinu og dragið og sleppið tengslin. Þetta er hægt að gera með því að velja línuna sem verkþátturinn er áætlaður. Eftir að línan er valin er hægt að draga línu tilfangsins í línuritinu flokkuð undir flokkun á mismunandi tilfanga.

### <a name="reassigning-an-activity-from-the-schedule-jobs-menu"></a>Endurúthlutun verkþáttar úr valmyndinni Áætla vinnslur

Hægt er að endurúthluta vinnslu úr svarglugganum **Áætla vinnslu** sem opnast úr valmyndinni **Áætla vinnslu**. Frá þessari valmynd einungis hægt að endurúthluta vinnslu á tilföng sem er þegar til staðar í gantt-línuritinu. Ef aðeins ein vinnsla er valin verður síðan sleppa niður fyrir tilföng verður raðað eftir viðeigandi tilföng. Ef frekari vinnslur eru síðan valdar verða engar upplýsingar um viðeigandi tilföng af listanum tilfanga.

## <a name="load-additional-resources-to-the-gantt-chart"></a>Hlaða viðbótartilföngum í gantt-riti
Í **Yfirlit tilfanga** hefurðu valkost um að hlaða viðbótartilföngum í gantt-línuritið. Þetta getur verið gagnlegt ef ætlunin er að finna önnur tilföng fyrir vinnslu sem raðað er í vél sem er ofbókuð eða biluð. Á síðunni **Hlaða viðbótartilföngum** færðu lista yfir tilföng sem eru dagsetningu skilvirkar dagsetningu listi er opnaður. Viðeigandi tilföng miðað við valda vinnslu í gantt-línurit verða skráð fyrst. Ef margar vinnslur eru valdar áður en listinn er opnaður verður enginn vísir um viðeigandi tilföng eru sýndur. Á síðunni **Hlaða viðbótartilföngum** er hægt að velja eitt eða fleiri tilföng, sem verður hlaðið í gantt-ritinu þegar valið er staðfest. Ef engar vinnslur eru áætlaðar á valið tilfang á völdu tímabili í gantt-línuritinu verður tilfangið sett inn undir tilfanga flokkun stigi í framleiðsluferlinu neðst á listann yfir aðgerðir í gantt-ritinu.

### <a name="access-the-gantt-chart"></a>Fara í Gantt-línuritið

Hægt er að opna gantt-línurit úr eftirfarandi síðum.


|                                                 <strong>Síða</strong>                                                  |                                                                                                                                                                                                                                                            <strong>Lýsing</strong>                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|                                   <strong>Pantanalisti og -upplýsingar framleiðslu</strong>                                    | Á síðunni <strong>Pantanalisti og -upplýsingar framleiðslu</strong> er hægt að opna gantt-línurit úr einni eða fleiri völdum pöntunum. Ef línurit er opnað úr valmyndaratriðinu <strong>gantt-línuritið</strong> hlaðast allar vinnslur sem tengjast valinni framleiðslu pantanir, heldur einnig vinnslur úr öðrum framleiðslupantanir sem eru bókaðar á sama tilföng. Ef línuritið er opnað úr valmyndaratriðinu <strong>gantt-línuritið – Flýtiyfirlit</strong> hlaðast einungis vinnslur sem tengjast völdum framleiðslupöntunum. Í þessu yfirliti, er ekki hægt að áætla vinnslur. |
|                                               <strong>Tilföng</strong>                                                |                                                                                                                                                        Á síðunni <strong>Tilföng</strong> síðu er hægt að opna gantt-línurit úr valmyndaratriði <strong>gantt-línuritið</strong>. Þegar valið hlaðast allar vinnslur sem eru áætlaðar í tilföngum valins tímabils í línuritið.                                                                                                                                                         |
|                                            <strong>Tilfangaflokkur</strong>                                             |                                                                                                                                                 Á síðunni <strong>Tilfangahópur</strong> er hægt að opna gantt-línurit úr valmyndaratriði <strong>gantt-línuritið</strong>. Þegar valið verða allar vinnslur sem eru áætlaðar í tilföngum í tilfangahópnum sýndar á völdu tímabili.                                                                                                                                                 |
|                                             <strong>Gantt-línurit</strong>                                              |                                                                                 Á síðunni <strong>Gantt-línurit</strong> er hægt að skilgreina Gantt gröf tilföng og tilfangið flokkana. T.d. ef óskað er að stjórna framleiðsluverkþætti fyrir tiltekið svið tilfangið flokkana eða tilföng, þá er hægt að gera einstaka afbrigði þær á þá <strong>Gantt-línurit</strong> síðu. Síðan er hægt að opna gantt-línurit úr hverri skilgreiningu.                                                                                 |
|                                       <strong>Tímaspár</strong> (verk)                                        |                                                                                                                              Verkþáttum af gerðinni <strong>Tímaspár</strong> er hægt að vinnsluraða á tilföng. Á <strong>Tímaspá</strong> síðunni á <strong>Röðun</strong> valmyndinni er hægt að opna Gantt-línuritið á pöntun til að sjá tímaspá fyrir vinnsluröðun verkþátta.                                                                                                                               |
|           <strong>Vinnslur til að ljúka</strong> (Listann <strong>Framleiðslu hæð stjórnun</strong> vinnusvæði)            |                                                                                               Vinnusvæðið <strong>Vinnslur á listann í gólf stjórnun</strong> sýnir störf framleiðslu- og rununúmer pantana sem eru í gangi í völdu tilföng fyrir það. Á valmyndatriðinu <strong>gantt-línuritið</strong> er hægt að opna gantt-ritinu, þar sem allar vinnslur sem eru valin í listanum eru settar í línuritinu.                                                                                               |
| <strong>Framleiðslupantanir til að losa</strong> (Opnuð á <strong>Framleiðslu hæð stjórnun</strong> vinnusvæði) |                                                                                                                                         Síðan Framleiðslupantanir til að losa er opnuð á vinnusvæðinu <strong>Framleiðslu hæð stjórnun</strong>. Þessi síða sýnir áætlaðar framleiðslu- og runupantanir sem bíða útgáfu. Á þessari síðu er hægt að opna gantt-rit fyrir valdar framleiðslupantanir.                                                                                                                                          |

## <a name="additional-resources"></a>Frekari upplýsingar  
[Sjónrænar áætlanir með Gantt-línuritum fyrir framleiðslu og runupantanir (myndskeið)](https://youtu.be/BtbuShkGj4I)

[Sjónræn áætlun fyrir framleiðslu (sýniútgáfa)](/dynamics/s-e/)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]