---
title: Um keyrslu á meðalkostnaðarverði
description: Birgðalokunarferlið jafnar úthreyfingafærslur við innhreyfingafærslur samkvæmt birgðamatsaðferð sem er valin í birgðalíkanaflokki vörunnar. Áður en birgðalokun er keyrð reiknar kerfið samt sem áður út hlaupandi meðalkostnaðarverð sem er í flestum tilvikum notað við bókun úthreyfingafærslna.
author: JennySong-SH
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d324324312ce9e47b07de8e3de952b8d7c53647
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672179"
---
# <a name="running-average-cost-price"></a>Um keyrslu á meðalkostnaðarverði

[!include [banner](../includes/banner.md)]

Birgðalokunarferlið jafnar úthreyfingafærslur við innhreyfingafærslur samkvæmt birgðamatsaðferð sem er valin í birgðalíkanaflokki vörunnar. Áður en birgðalokun er keyrð reiknar kerfið samt sem áður út hlaupandi meðalkostnaðarverð sem er í flestum tilvikum notað við bókun úthreyfingafærslna.

Kerfið metur þetta meðalkostnaðarverð vöru með því að nota eftirfarandi formúlu:

Áætlað verð = (efnisleg upphæð + fjárhagsleg upphæð) / (efnislegt magn + fjárhagslegt magn)

## <a name="default-item-cost"></a>Sjálfgefinn vörukostnaður

Hægt er að skilgreina sjálfgefinn vörukostnað fyrir útgefna afurð á tvennan hátt á síðunni með **Upplýsingar um losaðar afurðir**:

- Búðu til staðalkostnað með því að velja **Vöruverð** í flokknum **Setja upp** í flipanum **Stjórnun kostnaðar** á aðgerðasvæðinu. Ef þú notar þessa aðferð verður þú að nota hefðbundna kostnaðarútgáfu og virkja kostnaðinn.
- Skilgreindu sjálfgefið kostnaðarverð vöru fyrir útgefna afurð með því að slá inn gildi í reitinn **Verð** í flýtiflipann **Stjórnun kostnaðar**.

Til viðbótar við að slá inn eða búa til verð er hægt að velja gátreitinn **Nota síðasta kostnaðarverð** í flýtiflipanum **Stjórnun kostnaðar** á síðunni **Upplýsingar um losaðar afurðir**. Í slíku tilfelli mun kerfið sjálfkrafa uppfæra reitinn **Verð** þegar þú bókar fjárhagsuppfærslu. Ef þú til dæmis bókar reikning vegna innkaupapöntunar verður reiturinn stilltur á innkaupsverð frá þeim reikningi.

Ef þú ert með kostnaðarverð í virkri kostnaðarútgáfu og slær verðið inn í flýtiflipann **Stjórnun kostnaðar** mun kerfið nota verðið úr virkri kostnaðarútgáfu áður en það notar verðið sem skilgreint er í flýtiflipanum **Stjórnun kostnaðar**.

## <a name="using-the-running-average-cost-price"></a>Að nota meðalkostnaðarverð

Eftirfarandi tafla sýnir hvenær kerfið bókar birgðafærslur með því að nota meðalkostnaðarverð og hvenær kerfið notar kostnaðarverð sem er skilgreint í aðalfærslu vöru.

| Skilyrði | Kerfið notar áætlað meðalkostnaðarverð | Kerfið notar sjálfgefið kostnaðarverð vöru |
| --- | --- | --- |
| Bæði teljari\* og nefnari\*\* eru jákvæðir. | Já | Nr. |
| Teljarinn\*, nefnarinn\*\* eða hvorir tveggja eru neikvæðir. | Nei | Já |
| Nefnarinn\*\* er 0 (núll). | Nei | Já |

\* Teljari = (efnisleg upphæð + fjárhagsupphæð)  
\*\* Nefnari = (efnislegt magn + fjárhagslegt magn)

> [!NOTE]
> Ef valkosturinn **Taka með efnislegt virði** er ekki valinn fyrir vöru notar kerfið notar 0 (núll) fyrir bæði efnislega upphæð og efnislegt magn. Sjá upplýsingar um þennan valkost í [Taka með efnislegt virði](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Að forðast verðmögnun

Af og til verðleggur kerfið margar úthreyfingar áður en nægilega margar innhreyfingar eru komnar sem byggja má verð á. Þær aðstæður geta valdið ofmati á hlaupandi meðaltali kostnaðarverðs. Þó eru ráðstafanir sem má gera til að forðast vandamálið eða minnka áhrif þess ef það kemur upp.

**Aðstæður:** Eftirfarandi færslur eiga sér stað fyrir vöru sem valkosturinn **Taka með efnislegt virði** hefur verið valinn fyrir:

1. Fjárhagslegt móttökumagn er 100 á USD 100,00.
2. Fjárhagsleg úthreyfingamagn er 200.
3. Raunverulegt móttökumagn er 101 á USD 202,00.

Þegar skoðað er áætlað meðalkostnaðarverð vörunnar er búist við kostnaðarverðinu USD 1,51. Þess í stað finnur þú áætlað hlaupandi meðaltal upp á 102,00 USD sem er byggt á eftirfarandi formúlu:

Áætlað verð = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

Þessi hækkun verðlags gerist vegna þess að þegar 200 vörur eru fjárhagslega losaðar í skrefi 2 verður kerfið að verðleggja 100 af þessum vörum áður en það er komið með einhverjar samsvarandi innhreyfingar. Þessar aðstæður orsaka neikvæðar birgðir. Kerfið áætlar síðan einingarverðið USD 1,00, sem við má búast. Hins vegar þegar samsvarandi 100 innhreyfingar koma, eru þær á einingarverðinu USD 2,00 hver.

> [!NOTE]
> Þó að úthreyfingarnar leiði af sér neikvæðar birgðir eru birgðir jákvæðar þegar úthreyfingarverðið er reiknað. Þess vegna er meðalkostnaðarverð notað í staðinn fyrir verð í aðalvörufærslunni. Þegar hér er komið hefur kerfið birgðavirðisjöfnun sem er USD 100,00. Og meðan sú jöfnun var byggð upp yfir 100 stykki þar sem það var á USD 1,00 hvern, höfum við nú aðeins eitt stykki í birgðum. Þess vegna er jöfnuðu tapi upp á USD 100,00 er úthlutað á þetta eina stykki. Niðurstaðan er ofhækkun á áætluðu kostnaðarverði.
>
> Til samanburðar má sjá að ef skrefum 2 og 3 er snúið við í dæminu hér að framan verða 200 vörur hreyfðar út á einingarverðinu USD 1,51, og eitt stykki verður eftir á einingarverðinu USD 1,51. Þar sem þetta verðmögnunartilfelli getur komið upp þegar um neikvæðar birgðir er að ræða er erfitt að forðast eftirfarandi tilfelli:
>
> - Meta verður úthreyfingaverð á lagerbirgðavirði og magni.
> - Leiðrétta verður virði lagerbirgða og magn á út- og innhreyfingum.
> - Viðskiptalíkanið leyfir útsendingu eða verðlagningu fleiri stykkja en eru fyrir hendi.
> - Samþykkja verður allt innhreyfingarvirði og magn sem er sent.

Samt sem áður, ef viðskiptalíkanið leyfir eftirfarandi venjur geta þær hjálpað til við að forðast neikvætt magn sem getur skapað verðmögnun:

- Ef valkosturinn **Taka með efnislegt virði** er valinn fyrir vöru, skal hreinsa gátreitinn **Efnislega neikvæðar birgðir** á síðunni **Vörulíkanaflokkar**.
- Ef **ekki** er valinn valkosturinn **Taka með efnislegt virði** fyrir vöru, skal hreinsa valkostinn **Fjárhagslega neikvæðar birgðir** á síðunni **Vörulíkanaflokkar**.

Hafið einnig í huga að hámarksjöfnunin á efnislegu birgðavirði er takmörkuð af fjölda efnislegra færslna og mismun milli efnislegs og fjárhagslegs verðs. Svo lengi sem allar efnislegar færslur eru að lokum uppfærðar fjárhagslega getur efnislegt virði ekki hækkað óstjórnlega. Að lokum skal minnt á að mögnunaráhrifin minnka verulega þegar samanlagða jöfnunin dreifist á nokkur stykki í lagerbirgðum en ekki bara eitt.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Koma í veg fyrir núll kostnaðarverð í vandamálum

Þegar valkosturinn **Bæta við efnislegu virði** er ekki valinn á síðunni **Vörulíkanaflokkur** getur innhreyfing frá birgðum verið með núll í kostnaðarverði ef engar fjárhagslega uppfærðar innhreyfingar eru í birgðum. Til að koma í veg fyrir þessar aðstæður skaltu íhuga eftirfarandi valkosti:

- Veldu valkostinn **Taka með efnislegt virði** á síðunni **Vörulíkanaflokkur**. Þessi valkostur kemur í veg fyrir núll í kostnaðarverði í innhreyfingu að því gefnu að innhreyfingin sé uppfærð efnislega. Ef þú leyfir ekki neikvæðar efnislegar birgðir munu innhreyfingar reikna út hlaupandi meðaltal úr efnislega uppfærðum færslum.
- Búðu til sjálfgefið kostnaðarverð vöru með því að virkja kostnaðarútgáfuna sem er með staðalkostnað eða sláðu inn verðið í flýtiflipann **Stjórnun kostnaðar** á síðunni **Upplýsingar um losaðar afurðir**. Þessi valkostur er bestur þegar valkosturinn **Taka með efnislegt virði** er ekki valinn á síðunni **Vörulíkanaflokkur** því að kerfið mun alltaf vera með varaverð til að nota.
- Veldu aðgerðina **Nota síðasta kostnaðarverð** í flýtiflipanum **Stjórnun kostnaðar** á síðunni **Upplýsingar um losaðar afurðir**. Þessi valkostur mun halda reitnum **Verð** uppfærðum í hvert skipti þegar innhreyfing er uppfærð fjárhagslega. Ef þessi kostur er valinn, en þú slærð ekki inn sjálfgefið verð eða virkjar kostnað í hefðbundinni útgáfu, getur kostnaðurinn samt orðið núll á vandamáli.

Ef þú átt í vandræðum með færslur sem hafa engan kostnað mun *Birgðir - Lokun og leiðrétting* leiðrétta kostnaðarverðið með því að útbúa leiðréttingu eftir að kvittanirnar hafa verið uppfærðar. Hafðu í huga að fjárhagslega tímabilið þegar þessi uppfærsla á sér stað gæti verið frábrugðið fjárhagslega tímabilinu þegar hlutirnir voru mótteknir eða gefnir út.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
