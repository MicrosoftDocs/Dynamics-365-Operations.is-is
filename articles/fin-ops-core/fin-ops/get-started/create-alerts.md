---
title: Stofna viðvörunarreglur
description: Þessi grein veitir upplýsingar um viðvaranir og útskýrir hvernig á að búa til viðvörunarreglu.
author: RichdiMSFT
ms.date: 10/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: a420c5b2a036ac63a1a179f93462d152c3941fda
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2022
ms.locfileid: "9124225"
---
# <a name="create-alert-rules"></a>Stofna viðvörunarreglur

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Hafist handa

Áður en þú setur upp viðvörunarreglu skaltu ákveða hvenær eða í hvaða aðstæðum þú vilt fá viðvaranir. Þegar þú veist hvaða atvik þú vilt fá tilkynningu um skaltu finna síðuna með gögnunum sem eru þess valdandi að atvikið birtist. Atvikið getur verið dagsetning sem kemur eða tilteknar breytingar sem eiga sér stað. Þess vegna verður þú að finna síðuna þar sem dagsetningin er tilgreind eða hvar reiturinn er sem breytist eða hvar nýja færslan birtist sem er búin til. Eftir að þú hefur þessar upplýsingar er hægt að búa til viðvörunarregluna.

Þegar þú býrð til viðvörunarreglu skilgreinirðu skilyrðin sem þarf að uppfylla áður en kveikt er á viðvörun. Skilyrði eru í grundvallaraðtriðum samsvörun milli tilviks sem á sér stað og uppfyllingar á tilgreindum skilyrðum. Þegar tilvik á sér stað byrjar kerfið að framkvæma eftirlit samkvæmt skilyrðum sem sett eru upp.

## <a name="ensure-the-alert-batch-jobs-are-running"></a>Gakktu úr skugga um að viðvörunarrunuvinnslur séu í gangi

Runuvinnslur fyrir gagnabreytingar og tilkynningar um gjalddaga þurfa að vera í gangi til að viðvörunarskilyrði séu afgreidd og tilkynningarnar sendar. Til að keyra runuvinnslur ferðu í **Kerfisstjórnun** > **Reglubundin verk** > **Viðvaranir** og bætir við nýrri runuvinnslu fyrir **Viðvaranir vegna breytinga** og/eða **Skiladagsviðvaranir**. Ef þörf er á langri runuvinnslu sem keyrir oft skaltu velja **Endurtekning** og stilla **Engin lokadagsetning** með **Endurtekningarmynstur** á **Mínútur** og **Talning** á **1**.

## <a name="events"></a>Tilvik

Tilvikið sem kveikir á viðvörunarreglu getur verið dagsetning sem kemur eða tiltekin breyting sem á sér stað. Kveikjur fyrir tilvik eru skilgreindar á flýtiflipanum **Láta mig vita þegar** í svarglugganum **Búa til viðvörunarreglu**. Tilvikin sem eru tiltæk fyrir tiltekinn reit fer eftir kveikjunni sem er valin.

Til dæmis, ef þú ert að setja upp viðvörunarreglu fyrir reitinn **Upphafsdagur** eru tilvik lokadags við hæfi. Þess vegna er gerð tilviksins `is due in` í boði fyrir þann reit. Hins vegar, fyrir reit eins og **Kostnaðarstaður** er lokadagur tilviks ekki viðeigandi. Þess vegna er gerð tilviksins `is due in` er í boði. Þessi í stað er `has changed` atviksgerð í boði.

## <a name="event-types"></a>Gerð tilvika

Þrjár gerðir af tilvikum geta komið fram:

- **Tilvik af gerðinni búa til og eyða** - Þessi tilvik kveikja á viðvörun þegar færsla er búin til eða henni eytt.
- **Tilvik af gerðinni uppfærsla** - Þessi tilvik kveikja á viðvörun þegar gögn í tilteknum reit breytast.
- **Tilvik af gerðinni lokadagur** - Þessi tilvik kveikja á viðvörun þegar dagsetning kemur.
    
Breytingar sem eiga sér stað geta byrjað af notanda. Til dæmis breytir notandi afhendingardegi á innkaupapöntun. Að öðrum kosti geta breytingar komið fram sem hluti af ferli. Til dæmis breytist reiturinn **Staða** á síðu til að endurspegla líftíma mismunandi ferla í kerfinu.

## <a name="conditions"></a>Skilyrði

Á flýtiflipanum **Láta mig vita um** í svarglugganum **Stofna viðvörunarreglu** er hægt að nota skilyrði til að stjórna því þegar þú færð viðvörðun um tilvik.

Til dæmis getur þú tilgreint að kerfið eigi að láta þig vita þegar staða innkaupapantana breytist, en aðeins ef staðan passar við tiltekið safn skilyrða. Þú vilt sérstklega fá viðvörun þegar staða innkaupapöntunar er stillt á **Móttekin**. Þessi breyting á stöðu er tilvikið sem kallar fram viðvörunina.

Næst verður þú að ákveða hvaða innkaupapantanir þú vilt fá viðvaranir um. Til dæmis getur þú valið einn af eftirtöldum valkostum. Þessir valkostir skilgreina skilyrðin á viðvörunarreglunni.

- **Núverandi valin færsla** - Þú færð viðvörun þegar staða tiltekinnar innkaupapöntunar breytist í **Móttekin**.
- **Allar færslur** - Þú færð viðvörun þegar staða innkaupapöntunar breytist fyrir vöru á virka síðuyfirlitinu. Þú getur notað ítarlegu síuna sem er tiltæk á síðunni til að búa til reglur fyrir tiltekið safn af færslum. Til dæmis getur þú búið til viðvörun sem kviknar á fyrir allar innkaupapantanir fyrir viðskiptavini í tilteknum viðskiptavinaflokki.
    
## <a name="expiry-of-rule"></a>Fyrning reglu

Á flýtiflipanum **Láta mig vita þangað til** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina hversu lengi viðvörunarreglan á að vera virk.

## <a name="alert-contents"></a>Efni viðvörunar

Á flýtiflipanum **Láta mig vita með** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina efnistexta og textaskilaboð sem viðvörunarskilaboðin eiga að nota.

## <a name="user-id"></a>Kenni notanda

Á flýtiflipanum **Láta mig vita með** í svarglugganum **Búa til viðvörunarreglu** er hægt að tilgreina hvaða notandi eigi að fá viðvörunarskilaboðin. Að sjálfgefnu er notandakenni þitt valið. Hæfni til að breyta notanda sem fær viðvörun er takmörkuð við stjórnendur fyrirtækja.

## <a name="alerts-as-business-events"></a>Viðvaranir sem viðskiptatilvik

Hægt er að senda viðvaranir út með ramma viðskiptatilvika. Þegar þú býrð til viðvörun skaltu stilla **Í öllu fyrirtækinu** á **Nei** og stilla **Senda að utan** á **Já**. Þegar viðvörunin hefur komið viðskiptatilvikinu af stað er hægt að virkja flæði sem er innbyggt í Power Automate með virkjanum **Þegar viðskiptatilvik á sér stað** í tengi fjármála- og reksturs eða senda tilvikið beint á endastöð viðskiptatilvika í gegnum **Lista yfir viðskiptatilvik**.

## <a name="create-an-alert-rule"></a>Búa til viðvörunarreglu

0. Gakktu úr skugga um að viðvörunarrunuvinnslur séu í gangi (sjá hér að ofan).
1. Opnaðu síðuna sem inniheldur gögnin sem á að fylgjast með.
2. Á aðgerðasvæðinu, á flipanum **Valkostir**, í flokknum **Deila** skal velja **Búa til viðvörunarreglu**.
3. Í svarglugganum **Búa til viðvörunarreglu**, í reitnum **Reitur** skal velja reitinn sem á að fylgjast með.
4. Í reitnum **Tilvik** skal velja gerð tilviks.
5. Á flýtiflipanum **Láta mig vita af** skal velja æskilegan valkost. Ef senda á viðvörun sem viðskiptatilvik skal stilla gildið **Í öllu fyrirtækinu** á **Nei**.
6. Ef viðvörunarreglan verður óvirk á tilteknum degi skaltu velja lokadag á flýtiflipanum **Láta mig vita þangað til**.
7. Á flýtiflipanum **Láta mig vita með**, í reitnum **Efni** skal samþykkja sjálfgefna fyrirsögn efnis fyrir tölvupóstinn eða færa inn nýtt efni. Textinn verður efni fyrirsagnar tölvupóstskilaboðanna sem berast þegar viðvörun er ræst. Ef þú vilt senda viðvörunina sem viðskiptatilvik skaltu stilla **Senda að utan** á **Já**.
8. Í reitnum **Skilaboð** skal færa inn valfrjáls skilaboð. Textinn verður skilaboðin sem berast þegar viðvörun er gefin.
9. Veldu **Í lagi** til að vista stillingarnar og búa til viðvörunarregluna.

## <a name="limitations-and-workarounds"></a>Takmarkanir og hjáleiðir

### <a name="workaround-for-creating-alerts-for-the-secondary-data-sources-of-a-form"></a>Hjáleiðir til að búa til viðvaranir fyrir aukalega gagnagjafa skjámyndar
Ekki er hægt að búa til viðvaranir fyrir suma aukalega gagnagjafa á eyðublöðum. Til dæmis, þegar viðvaranir eru búnar til í bókunarregluskjámyndum viðskiptavinar og lánardrottins, eru aðeins reitirnir í hausnum (CustLedger or VendLedger) tiltækir en ekki víddarlyklarnir. Hjáleið þessarar takmörkunar er að nota **SysTableBrowser** til að opna þessa töflu sem aðalgagnagjafa. 
1. Opnið töfluna í skjámyndinni **SysTableBrowser**.
    ```
        https://<EnvironmentURL>/?cmp=USMF&mi=SysTableBrowser&TableName=<TableName>
    ```
2. Stofnið viðvörun úr skjámyndinni SysTableBrowser.

### <a name="change-based-alerts-do-not-work-for-batch-status-changes"></a>Viðvaranir vegna breytinga virka ekki fyrir breytingar á runustöðu
Viðvaranir vegna breytinga virka ekki með breytingum á runustöðu vegna þess að slökkt er á þeim vegna frammistöðu. Þess í stað ætti að setja upp **Runuviðvörun**. Frekari upplýsingar er að finna í [Setja upp viðvaranir fyrir skjámynd runuviðbótar](../../dev-itpro/sysadmin/alerts.md#set-up-alerts-for-batch-enhanced-forms).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
