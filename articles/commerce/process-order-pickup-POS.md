---
title: Vinna úr afhendingum pantana viðskiptavina á sölustað
description: Þetta efnisatriði útskýrir virkni sem er tiltæk í forriti sölustaðar til að vinna úr afhendingu viðskiptavinapantana.
author: Hhainesms
manager: annbe
ms.date: 01/06/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 2156542ed0932fab6fb4fa4035e009ad89eeb18f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003754"
---
# <a name="process-customer-order-pickups-in-pos"></a>Vinna úr afhendingum pantana viðskiptavina á sölustað

[!include [banner](includes/banner.md)]

Þegar [pöntun viðskiptavinar](customer-orders-overview.md) sem verður sótt í verslun er stofnuð getur notandi verslunar notað forrit sölustaðarins til að hefja tiltekt á birgðum. Sölustaður mun keyra lokagreiðsluna sem er sótt eftir þörfum. Hann lýkur einnig við birgðirnar og fjármálabókanir fyrir magningu sem er sótt.

Ef þú ert notandi verslunar geturðu framkvæmt tiltektina með því að nota annaðhvort aðgerðina **Afturkalla pöntun** eða aðgerðina **Uppfylling pöntunar** á sölustað. Til að gera aðgerðina **Sótt** aðgengilega þarf fyrst að fylgja einu af þessum skrefum:

- Til að nota aðgerðina **Endurkalla pöntun** skal leita að og velja pöntunina sem á að sækja.
- Til að nota aðgerðina **Uppfylling pöntunar** skal leita að og velja eina eða fleiri pöntunarlínur.

Ef valdar pantanir eða pöntunarlínur eru ekki skilgreindar fyrir afhendingu í þessari tilteknu verslun, eða búið er að taka saman pöntunina að fullu, verður aðgerðin **Sækja** ekki tiltæk.

![Afhendingaraðgerð](media/pickupoperation.png)

Í Microsoft Dynamics 365 Commerce útgáfu 10.0.17 og nýrri er hægt að kveikja á eiginleikanum **Bætt upplifun notanda fyrir úrvinnslu pöntunar sem er sótt á sölustað** í gegnum eiginleikastjórnun í Commerce Headquarters. Ef slökkt er á þessum eiginleika geta notendur ekki valið tiltektarmagn. Sjálfgefið er að fullt magn sem pantað var fyrir línuna er magnið sem verður sótt. Þessi upplifun getur verið til vandræða vegna þess að notendur gætu gleymt að velja sumar vörur fyrir tiltekt þegar þeir framkvæma tiltekt í gegnum pöntunaruppfyllingu.

Eiginleikinn **Bætt upplifun notanda fyrir úrvinnslu pöntunar sem er sótt á sölustað** veitir notendum meiri stjórn yfir val á afurðum sem verða sóttar og magn þessara afurða sem verða sóttar. Notendur þurfa ekki að velja allar línur sölupöntunar á síðu pöntunaruppfyllingar áður en þeir velja **Sækja**. Allar vörur sem hægt er að sækja eru sýndar. Notendur geta tilgreint margar tiltektarlínur jafnvel þótt aðeins ein afurðarlína sé valin.

Þegar kveikt er á eiginleikanum **Bæta upplifun notanda fyrir úrvinnslu pöntunar sem er sótt á sölustað** og aðgerðin **Sækja** er valin mun svarglugginn **Sækja** birtast. Þar er hægt að velja vörur og magn sem verður sótt. Sjálfgefið er að allt pantað magn sem er með birgðir í stöðu tiltektar eða pökkunar er álitið hæft til tiltektar. Sjálfgefið er að magnið er stillt sem tiltektarmagn. Hægt er að breyta magninu sem var slegið inn, að því gefnu að magnið sé ekki 0 (núll) og fari ekki yfir samtölu opins (þ.e. ekki reikningsfærðs) magns fyrir valda línu.

![Svargluggi afhendingar](media/pickupselect.png)

Þegar búið er að velja magnið sem verður sótt um og síðan valið **Sækja** birtist færslusíðan. Ef kveikt er á eiginleikanum [greiðslur omni-rásar](omni-channel-payments.md) og til eru fyrirframheimilaðar kreditkortagreiðslur á skrá, þarf að nota greiðsluna.

Á færslusíðunni reiknar kerfið út upphæðirnar sem eru á gjalddaga með því að reikna samtöluna sem er á gjalddaga fyrir valdar tiltektarvörur og dregur síðan frá allar áður notaðar inneignir eða heimilaðar kreditkortagreiðslur. Vinna þarf úr greiðslu til að ljúka tiltektarfærslu. Ef [skjáútlit](pos-screen-layouts.md) færslusíðunnar er skilgreint þannig að það feli í sér aðgerðina **Ljúka við færslu** og engin upphæð er gjaldfallin, er hægt að ljúka við færsluna án þess að velja greiðslumáta. Ef aðgerðin **Ljúka við færslu** er ekki í boði er hægt að velja tengilinn **$0,00 upphæð til greiðslu** í glugganum **Samtölur** til að ljúka við færsluna án þess að þurfa að velja greiðslumáta.

![Færslusíða fyrir tiltektarfærslu viðskiptavinapöntunar](media/pickupcart.png)

## <a name="changing-pickup-lines-or-quantities"></a>Tiltektarlínum eða -magni breytt

Ef breyta þarf tiltektarmagni eftir að búið er að velja vörurnar sem verða sóttar skal velja **Stilla magn**. Ekki er hægt að stilla tiltektarmagnið á **0** (núll) eða hækka það upp í gildi sem fer yfir óreikningsfært magn sem eftir er fyrir pöntuðu línuna. Til að fjarlægja tiltektarlínu úr færslukörfunni skal velja **Ógilda færslu**. Núverandi færsla verður stöðvuð og ferlið fyrir aðgerðina **Sækja** verður sett aftur af stað.

Ef kveikt er á eiginleikanum **Bætt upplifun notanda fyrir úrvinnslu á sóttri pöntun á sölustað** geta fyrirtæki bætt hnappi fyrir aðgerðina **Breyta afhendingarlínum** við skjáútlit færslusíðunnar. Þegar búið er að búa til færslukörfu afhendingar á sölustað og velja vörurnar, er hægt að velja **Breyta afhendingarlínum** ef þarf að breyta afhendingarvörum en ekki ógilda alla færsluna. Í svarglugganum **Breyta afhendingarlínum** sem birtist er hægt að breyta afhendingarvörum og magni. Færslukarfan er síðan uppfærð til að endurspegla breytingarnar.

![Svargluggi fyrir breytingu á sóttum vörum](media/pickupchange.png)
