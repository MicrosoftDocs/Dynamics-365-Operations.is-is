---
title: Áætlanagerð farms flutningsleiðir með mörgum stöðvun
description: Þessi grein lýsir mismunandi einingunum sem er notuð til að áætla flutningsleiðir í Dynamics 365 Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSHubMaster, TMSLoadBuildTemplates, TMSRateRouteWorkbench, TMSRouteGuide, TMSRoutePlan, TMSRouteWorkbench, WHSLoadTemplate, TMSRouteSchedule, TMSRouteRateDetail
audience: Application User
ms.reviewer: kamaybac
ms.custom: 90013
ms.assetid: 50d6f58c-f1c8-4321-9e83-8445cec57a85
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3d316b5bed67e84fdd5cec8b518069c053436d
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671592"
---
# <a name="plan-freight-transportation-routes-with-multiple-stops"></a>Áætlanagerð farms flutningsleiðir með mörgum stöðvun

[!include [banner](../includes/banner.md)]

Þessi grein lýsir mismunandi einingunum sem er notuð til að áætla flutningsleiðir í Dynamics 365 Supply Chain Management.

Hægt er að nota leiðaráætlanir og leiðarleiðbeiningar fyrir flóknar flutningsleiðir sem hafa mörg stöðvar. Ef á að nota sömu leið reglulega hægt að setja upp áætlaðan leið.

## <a name="route-plans"></a>Leiðaráætlanir
Áætlun leið inniheldur hlutum leiðar sem veita upplýsingar um stöðvar sem eru heimsótt á leið og farmflytjendur sem notaðir eru fyrir hvern hluta. Skilgreina verður stöðvanir í leiðinni sem stöðvar. Stöðvar getur verið lánardrottinn, vöruhús, viðskiptavin eða jafnvel umhleðslustað þar sem breyta flutningsaðila. Fyrir hvern hluta er hægt að skilgreina "stundartaxta" fyrir ýmis gjöld. Hér eru nokkur dæmi:

-   Gjöld fyrir ferðalög á tiltekinn hluta
-   Gjöld fyrir sækja vörur
-   Gjöld til að afhenda vörum

Leiðaráætlun hvern verður að vera tengdur leiðarleiðbeiningar.

## <a name="route-guides"></a>Leiðarleiðbeiningar
Leiðarleiðbeiningar skilgreinir skilyrði fyrir samsvörun við hleðslu á áætlun fyrir tiltekna leið. Til dæmis er hægt að tilgreina uppruna stöðvar og áfangastöð, takmörk rúmmál gáms eða þyngd, og farmflytjanda, þjónustu, eða flokk. Leiðarleiðbeiningar eru tiltækar á **Taxta vinnusvæði leiðar** síðuna þar sem farmar hægt er að jafna í leiðum handvirkt eða sjálfvirkt. Ef leiðarleiðbeiningarnar er fyrir áætlaða leið, er einnig tiltæk á **hleðsluáætlun vinnusvæði** síðu.

## <a name="scheduled-routes"></a>Áætlaðar leiðir
Áætluð leið er forskilgreint leiðaráætlun með áætlun fyrir sendingar dagsetningar. Áætlað leiðir og leiðir ekki áætluð er munandi á þann hátt sem farmar þeim er úthlutað. Ef ekki áætluð leið úthlutað með vinnusvæði Taxta leiðar er eingöngu farm og leiðarleiðbeiningarnar samþykktar. Ef áætluð leið úthlutað, dagsetningar og aðsetur úr pöntunum og stöðvum og dagsetning leiðaráætlun eru einnig talin. Þarf ekki að nota síðuna vinnusvæði Taxta leið til að úthluta handvirkt hleðslur áætlaða leið. Þess í stað nota hleðsluáætlun vinnusvæði til að leggja til farmar byggt upp á grundvelli aðsetur viðskiptavinar og afhendingardagsetningar úr sölupöntunum fyrir tiltekna áætlaða leið. Fyrir raðaðar leiðir, leiðaráætlun verður með fastan stöðvum uppruna og áfangastaðar. Yfirleitt, farmflytjanda og þjónusta verður að vera það sama fyrir alla hluta, en þeir geta verið mismunandi. Áfangastaður stöðvum eru stofnaðar með því að nota póstnúmer viðskiptavina sem eru heimsótt á leiðinni. Hægt er að skilgreina nokkrum leiðaráætlunum fyrir eina leiðaráætlun. Leiðaráætlun verður að vera tengdur leiðarleiðbeiningar. Hins vegar fyrir raðaðar leiðir áætlunina má tengja aðeins eitt leiðarleiðbeiningar. Áætlun leið er aðeins notað til að stofna raunverulega leiðir á **leiðaráætlun** síðu. Hægt er að nota sjálfgefið sniðmát hleðslu þegar að leggja til hleðslu á hleðsluáætlun vinnusvæði.

## <a name="load-building-workbench"></a>Hlaða sniðmáti hleðslu
Hleðsluáætlun vinnusvæði notar aðsetur viðskiptavinar og afhendingardagsetningar frá sölupöntunum og raðaðar leiðir sem eru tiltækar til að leggja til hleðslu. Sjálfgefið gildi úr leið eru færðar inn í vinnslusvæði. Hins vegar er hægt að velja „frá“ dagsetningu sem er fyrr en"frá"dagsetning á leiðinni. Þegar farmur er lagt til, afhendingaraðsetri og afhendingardagsetningu allar opnar sölupantanir athugað. Ef póstnúmer afhendingaraðseturs samsvarar póstnúmer stöðvar í áætlun um leið og ef afhendingardagsetningin er innan marka sem er valin fyrir forsendur, er sölupöntun stungið upp fyrir farminn. Einnig er tekið tillit til afkastagetu hleðslusniðmátsins. Einungis einn farm er lögð til í einu. Ef sölupöntun er ekki með, gæti þurft að nota annað hleðslusniðmát (t.d. farmsniðmát fyrir hærri vörubíl eða gám) eða áætla aukalegar afhendingar.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]