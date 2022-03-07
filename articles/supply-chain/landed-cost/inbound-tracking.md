---
title: Rekja ferðir á innleið og ferðir gáma
description: Þetta efnisatriði útskýrir hvernig hægt er að nota rakningarsíðuna á innleið til að fylgjast með framvindu ferðanna og gámaleiðum.
author: sherry-zheng
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMContainerActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 94754447b3f363716595de4902f48188c4ebbda9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022014"
---
# <a name="track-inbound-voyages-and-shipping-container-journeys"></a>Rekja ferðir á innleið og ferðir gáma

[!include [banner](../../includes/banner.md)]

Á síðunni **Rakning á innleið** er hægt að fylgjast með framvindu ferðanna og gámaleiðum. Hver ferð og leiðangur eru sundurliðuð í *verkþætti* sem hver um sig er með sína eigin línu á síðunni. Hægt er að nota síðuna til að skoða og færa inn áætlaðar dagsetningar og raundagsetningar eftir verkþáttum.

Yfirleitt, eftir því hver uppsetningin er í [Stjórnstöð rakningar](delivery-information-setup.md#tracking-control-center), sýna þessir verkþættir sjálfkrafa áætlaða dagsetningu þegar komið er á lokaáfangastað. Einnig, allt eftir uppsetningunni, uppfærir lokadagsetningin yfirleitt afhendingardaginn eða staðfesta dagsetningu innkaupapöntunarlínanna. Fyrir flutningspöntunarlínur er hægt að stilla kerfið á að uppfæra móttökudagsetningu.

Til að opna síðuna **Rakning á innleið** skal fara í **Heildarkostnaður \> Rakning \> Rakning á innleið**.

## <a name="filter-the-activities-list"></a>Sía verkþáttarlista

Hægt er að nota reitina **Ferð** og **Gámur** efst á síðunni **Rakning á innleið** til að sía síðuna þannig að hún sýni aðeins verkþætti sem tengjast valdri ferð og/eða gámi.

## <a name="update-tracking-information"></a>Uppfæra rakningarupplýsingar

Til að uppfæra áætlunina fyrir ferð eða leiðangur skal færa inn upphafsdagsetningu fyrsta verkþáttarins. Áætlaður lokadagur síðasta verkþáttar er þá uppfærður. Uppsetning fyrir hvern legg og sniðmát ferðar í [Stjórnstöð rakningar](delivery-information-setup.md#tracking-control-center) sker úr um áætlaða afhendingartíma. Áætlaðar lokadagsetningar nota afhendingartíma frá upphafsdagsetningu verkþáttar. Síðan, þegar raunveruleg lokadagsetning er skráð, er upphafsdagsetning næsta verkþáttar uppfærð í sömu dagsetninguna og fyrri raunveruleg lokadagsetning verkþáttarins. Raunverulegur afhendingartími er uppfærður þannig að hægt sé að gera samanburð og greiningu. Hægt er að færa inn viðbótarathugasemdir í reitinn **Athugasemd**.

Röð verkþátta í hnitanetinu ákvarðast af röð leggjanna í viðeigandi sniðmáti ferðar. Ef röð leggja í viðhengdri ferð breytist, breytist rakningarstjórnunin einnig.

Hægt er að uppfæra dagsetningarnar fyrir alla gáma með því að velja **Uppfæra upphafsdagsetningu** eða **Uppfæra raunverulega lokadagsetningu** á aðgerðasvæðinu. Að öðrum kosti er hægt að færa inn dagsetningar fyrir hvern gám í sendingunni. Þessi nálgun eykur sveigjanleika vegna þess að hægt er að skipta gámum í umhverfi með mörgum ferðum.

## <a name="buttons-on-the-action-pane"></a>Hnappar á aðgerðasvæðinu

Hægt er að nota hnappana á aðgerðasvæði síðunnar **Rakning á innleið** til að vinna með ferðir og leiðangra á innleið. Eftirfarandi tafla lýsir hnöppunum sem eru í boði.

| Hnappur | lýsing |
|---|---|
| Breyta | Breytið ferð eða leiðangri gáms. |
| Nýjar | Stofnið nýja ferð eða leiðangur gáms. |
| Eyða | Eyðið valdri ferð eða leiðangri gáms. |
| Uppfæra upphafsdag | Uppfæra upphafsdagsetningu verkþáttar fyrir alla gáma í ferð. Þegar upphafsdagsetning tiltekins verkþáttar eða leggs á ferð er uppfærð verða áætlaðar upphafsdagsetningar sem fylgja uppfærðar út frá uppgefnum afhendingartíma. |
| Uppfæra raunverulega lokadagsetningu | Uppfæra lokadagsetningu verkþáttar fyrir alla gáma í ferð. Þegar lokadagsetning tiltekins verkþáttar er uppfærð verða verkþættir sem fylgja uppfærðir út frá uppgefnum afhendingartíma. |
| Bæta við verkþáttum | Bæta verkþætti handvirkt við ferð. Til dæmis væri hægt að bæta við verkþætti svælingar. Viðbótin gæti orðið til þess að staðfestur afhendingardagur varanna í skipinu eða ferðinni breytist. Þegar verkþætti er bætt við leiðangurinn eru áætlaðir dagar ekki færði inn fyrr en upphafsdagsetning á legg leiðangurs er uppfærð. |

## <a name="information-and-settings-on-the-overview-tab"></a>Upplýsingar og stillingar í yfirlitsflipanum

Flipinn **Yfirlit** sýnir lista yfir alla verkþætti sem tilheyra ferð og/eða gámi sem er valið efst á síðunni. Eftirfarandi tafla lýsir svæðunum sem eru tiltæk fyrir hverja aðgerð.

| Svæði | lýsing |
|---|---|
| Leggur | Auðkenni leggs fyrir verkþáttinn eins og það er skilgreint í sniðmáti ferðar. |
| Afhendingarmáti | Væntanlegur afhendingarmáti fyrir verkþáttinn. |
| Aðgerð | Þessi reitur auðkennir venjulega vinnsluna eða verkið sem tengist verkþættinum. Algeng dæmi eru t.d. *Sigling* og *Rýming*. |
| lýsing | Lengri lýsing á aðgerðinni. |
| Upphafsdagsetning | Þessi reitur sýnir upphaflega áætlaða upphafsdagsetningu verkþáttarins. En eftir að búið er að færa inn fyrri raunverulega lokadagsetninguna, sýnir hann raunverulega upphafsdagsetningu. Þessi svæði er notað til að ákvarða áætlaðan lokadag, byggt á afhendingartíma. |
| Áætluð lokadagsetning | Gildi þessa reits er reiknað út frá upphafsdegi og afhendingartíma. Yfirleitt er gildinu ekki breytt með beinum hætti. |
| Raunverulegur lokadagur | Notandi ætti að uppfæra þennan reit eins fljótt og auðið er eftir að verkþátturinn hefur átt sér stað. Raunverulegur afhendingartími er síðan uppfærður. |
| Áætlaðir dagar | Áætlaður tími (í dögum) sem þarf til að ljúka verkþættinum. |
| Raundagar | Raunverulegur tími (í dögum) sem þarf til að ljúka verkþættinum. |
| Nóta | Notið þennan reit til að bæta við ýmsum athugasemdum og upplýsingum um verkþáttinn. |

## <a name="information-and-settings-on-the-general-tab"></a>Upplýsingar og stillingar í almenna flipanum

Flipinn **Almennt** sýnir upplýsingar um legginn sem er valinn í flipanum **Yfirlit**. Þótt hann endurtaki sumar upplýsingarnar sem birtast í flipanum **Yfirlit** inniheldur hann einnig frekari upplýsingar um valinn legg.
