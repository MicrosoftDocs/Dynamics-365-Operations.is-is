---
title: Frestuð vinnsla vöruhúsavinnu
description: Þetta efnisatriði lýsir virkni sem gerir frestaða vinnslu vörugeymsluaðgerða tiltæka í Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkProcessingPolicy, WHSWorkDeferredPutProcessingTask
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-6-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc8321c55bc867db065af0cddf356fb497a956e8
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430671"
---
# <a name="deferred-processing-of-warehouse-work"></a>Frestuð vinnsla vöruhúsavinnu

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir virkni sem gerir frestaða vinnslu vörugeymsluaðgerða tiltæka í Dynamics 365 Supply Chain Management.

Frestuð vinnsluvirkni gerir vöruhússtarfsmönnum kleift að halda áfram að vinna önnur verk meðan aðgerðin er unnin í bakgrunni. Frestuð vinnsla er gagnleg þegar vinna þarf margar vinnulínur og starfsmaðurinn getur látið vinna þá vinnu ósamstillta. Það er einnig gagnlegt þegar netþjónninn getur haft tilfallandi eða óáætlaða aukningu á vinnslutíma og aukinn vinnslutími getur haft áhrif á framleiðni notandans.

Bakgrunnsvinnslu er náð með því að nota SysOperation ramma. Frekari upplýsingar eru í [Yfirlit yfir SysOperation-ramma](https://docs.microsoft.com/dynamicsax-2012/developer/sysoperation-framework-overview).

## <a name="configuring-the-work-processing-policies"></a>Stilla vinnsluskilmála vinnu

Til að nota frestaða vinnslu verður þú að stilla og nota vinnslustefnu vinnu.

Reglur eru stilltar á síðunni **Reglur um verkvinnslu**. Eftirfarandi tafla lýsir reitum á þeirri síðu.

| Svæði                           | Lýsing |
|---------------------------------|-------------|
| Heiti reglu vinnuferla     | Heiti á reglu verkvinnslu. |
| Gerð verkpöntunar                 | Verkbeiðnigerðin sem stefnunni er beitt á. |
| Aðgerð                       | Aðgerðin sem er unnin með því að nota stefnuna. |
| Aðferð vinnuferlisins          | Aðferðin sem notuð er til að vinna verklínuna. Ef aðferðin er stillt á **Strax** líkist hegðunin hegðuninni þegar engar verkvinnslureglur eru notaðar til að vinna línuna. Ef aðferðin er stillt á **Frestað** er frestuð vinnsla sem notar lotu ramma notuð. |
| Þröskuldur fyrir frestað ferli   | Gildi **0** (núll) gefur til kynna að enginn þröskuldur sé til staðar. Í þessu tilfelli er frestuð vinnsla notuð ef hægt er að nota hana. Ef sérstakur þröskuldur útreiknings er undir viðmiðunarmörkum, er tafarlausa aðferðin notuð. Annars er frestuð aðferð notuð ef hægt er að nota hana. Fyrir sölu og flutningstengda vinnu er þröskuldurinn reiknaður sem fjöldi tilheyrandi upphleðslulína sem eru í vinnslu vegna verksins. Fyrir endurnýjunarvinnu er þröskuldurinn reiknaður sem fjöldi vinnulína sem verið er að endurnýja af verkinu. Með því að setja þröskuld á t.d. **5** fyrir sölu munu smærri verk sem eru með færri en fimm upphafsleðslulínur ekki nota frestaða vinnslu, en stærri verk munu nota það. Þröskuldurinn hefur aðeins áhrif ef vinnuvinnsluaðferðin er stillt á **Frestað**. |
| Frestun vinnslu á runuhóp |Runuhópurinn sem er notaður við úrvinnslu. |

Við frestaða söluvinnslu eru eftirfarandi verkbeiðnigerðir studdar: sölupöntun, útgáfu flutningspöntunar og endurnýjun.

## <a name="assigning-the-work-creation-policy"></a>Að úthluta stefnu um sköpun vinnu

Hægt er að úthluta vinnusköpunarstuðlinum í breytur vöruhúsastjórnunar. Það er einnig hægt að úthluta þeim á stigi einstakra vöruhúsa. Ef stefnunni er úthlutað til vörugeymslu gildir hún aðeins um vinnu sem er búin til fyrir það vöruhús. Ef engri stefnu er úthlutað á vörugeymslustigi er stefnunni miðað við breytur vörugeymslu beitt.

## <a name="viewing-the-deferred-put-processing-tasks"></a>Skoðað frestuðu verkvinnsluverkefnum

Þú getur skoðað frestað verkvinnsluverkefni á síðunni **Frestuð verkefni vegna vinnslu**.

Sjálfgefið er að verk með stöðuna **Lokið** eru sýnd.

| Svæði            | Lýsing |
|------------------|-------------|
| Staða           | Staða verksins. |
| Staða runuvinnslu | Staða tengds runuverks. Ef runuvinnslan hefur verið unnin, þá inniheldur runuferillinn notkunarskrá og upplýsingar úr runuvinnslunni. |

Hér eru skýringar fyrir hugsanlegar stöður:

- **Beðið eftir** - Tilheyrandi runuvinnsla bíður afgreiðslu á runuþjóninum.
- **Mistókst** - Úrvinnsla mistókst. Hægt er að endurvinna verkefnið með því að nota aðgerðina **Ferli frestað** eða hægt er að hætta við það með því að nota aðgerðina **Hætta við frestaða sendingu**.
- **Lokið** - Starfinu var lokið.

## <a name="impact-on-closed-work-dates"></a>Áhrif á lokaða vinnudaga

Þegar frestað púlsvinnsla er notuð er lokaður vinnudagur dagsettur sem stofnaður dagsetning / tími frestaðra vinnsluverkefna. Lokaður vinnudagur er notaður vegna þess að það er besta matið fyrir hvenær söluaðgerðinni var lokið.

## <a name="reprocessing-a-failed-task"></a>Endurvinnsla á verki sem tókst ekki

Þú getur endurunnið verk sem tókst ekki með því að velja það á síðunni og síðan velja **Ferli frestað**. Endurvinnsla samsvarar aðstæðum þar sem notandinn lýkur brottvísuninni úr farsímanum eins og hann væri stilltur á tafarlausa vinnslu.

## <a name="canceling-failed-tasks"></a>Hætt við verk sem tókust ekki

Aðeins er hægt að hætta við verk sem tókust ekki. Þegar þú hættir við verk geturðu úthlutað því til nýs notanda. Að öðrum kosti getur verkið áfram verið úthlutað til notandans sem afgreiddi verkið. Afpöntun samsvarar aðstæðum þar sem verkið er fært aftur í farsímann eins og síðasta skrefi í frágangi væri nýlokið og það verður að koma verkinu í burtu. Hins vegar mun notandinn geta ákvarðað að verkið er „öðruvísi“ vegna þess að það mun aðeins hafa til brottfalls og staðsetningin samsvarar þeim stað sem fyrsti notandinn sem afgreiddi verkið hafði sem lokasetningu.

Þegar verki er aflýst er verkinu ekki lengur lokað af ástæðu frestunar púlsvinnslu. Það er hægt að endurtaka það með því að nota farsímann.

Verkefnalistanum er eytt þegar verkefninu var lokað.

## <a name="configuring-the-mobile-device-menu-to-skip-the-deferred-processing-policy"></a>Stilla valmynd farsíma til að sleppa frestuðu vinnslustefnunni

Þú getur stillt valmyndaratrið farsíma þannig að frestað vinnslustefna er ekki notuð. Verkið er síðan unnið eins og það er þegar engin frestað vinnslustefna er notuð. Þessi virkni gerir yfirmanni kleift að nota tiltekinn valmyndarlið þar sem frestun er ekki notuð. Til að stilla það, stillirðu reitinn **Frestað söluvinnslustefna** á **Hnekkja stillingum og vinna úr samstillingu**. 

## <a name="restrictions-when-the-deferred-put-processing-isnt-applied"></a>Takmarkanir þegar frestaðri söluvinnslu er ekki beitt

Það eru nokkrar aðstæður þar sem frestuðum söluvinnslum er ekki beitt jafnvel þó að stefnan sé sett upp. Hér eru nokkur dæmi:

- Handvirk vinnulok eru notuð.
- Vinnunni er lokið með því að nota sjálfvirka útfyllingu.
- Endurskoðunarsniðmát eru notuð.


## <a name="monitoring-the-deferred-processing-tasks-from-the-outbound-work-monitoring-workspace"></a>Vöktun á frestuðum vinnsluverkefnum frá vinnusviði vöktunar á vinnu á útleið

Vinnusvæðið **Vöktun á útleið** hefur tvo reiti sem hjálpa þér að fylgjast með frestuðum verkefnavinnslu:

- **Mistókst við frestun verkefnavinnslu** - Þessir reitir sýna fjölda verka sem ekki tókust. Ef það eru mistök, verður vörugeymslustjórinn annaðhvort að vinna úr þeim eða hætta við þá, þar sem þau verða ekki endurunnin sjálfkrafa.
- **Beðið eftir frestuðum verkefnavinnsluverkefnum** - Þessi reitur sýnir fjölda verkefna sem hafa verið í **Beðið eftir** stöðu lengur en 10 mínútur. Ef reiturinn sýnir tölu gæti það bent til þess að vandamál hafi komið upp við runuvinnslu. Þú getur handvirkt afgreitt **Beðið eftir** verkefni. Ef runuvinnsla fyrir verkefni er unnin seinna mun hún bara mistakast vegna þess að hún hefur þegar verið unnin. Það verða engin áhrif.

## <a name="deleting-completed-tasks"></a>Eyðing á loknum verkum

Þú getur eytt frestuðum verkefnavinnu sem lokið hefur verið með því að velja þau og eyða þeim á síðunni.
