---
title: Um keyrslu á meðalkostnaðarverði
description: Birgðalokunarferlið jafnar úthreyfingafærslur við innhreyfingafærslur samkvæmt birgðamatsaðferð sem er valin í birgðalíkanaflokki vörunnar. Áður en birgðalokun er keyrð reiknar kerfið samt sem áður út hlaupandi meðalkostnaðarverð sem er í flestum tilvikum notað við bókun úthreyfingafærslna.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d91422dfece5af70abbcf9f051ec5706517d0155
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231937"
---
# <a name="running-average-cost-price"></a>Um keyrslu á meðalkostnaðarverði

[!include [banner](../includes/banner.md)]

Birgðalokunarferlið jafnar úthreyfingafærslur við innhreyfingafærslur samkvæmt birgðamatsaðferð sem er valin í birgðalíkanaflokki vörunnar. Áður en birgðalokun er keyrð reiknar kerfið samt sem áður út hlaupandi meðalkostnaðarverð sem er í flestum tilvikum notað við bókun úthreyfingafærslna.

Kerfið metur þetta meðalkostnaðarverð vöru með því að nota eftirfarandi formúlu: 

Áætlað verð = (efnisleg upphæð + fjárhagsleg upphæð) / (efnislegt magn + fjárhagslegt magn)

## <a name="using-the-running-average-cost-price"></a>Að nota meðalkostnaðarverð
Eftirfarandi tafla sýnir hvenær kerfið bókar birgðafærslur með því að nota meðalkostnaðarverð og hvenær kerfið notar kostnaðarverð sem er skilgreint í aðalfærslu vöru.

| Skilyrði                                               | Kerfið notar áætlað meðalkostnaðarverð | Kerfið notar kostnaðarverð sem er skilgreint í aðalfærslunni |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Bæði teljari\* og nefnari\*\* eru jákvæðir.  | Já                                                      | Ekkert                                                                |
| Teljarinn\*, nefnarinn\*\* eða hvorir tveggja eru neikvæðir. | Ekkert                                                       | Já                                                               |
| Nefnarinn\*\* er 0 (núll).                        | Ekkert                                                       | Já                                                               |

\* Teljari = (efnisleg upphæð + fjárhagslegt magn) \*\* Nefnari = (efnislegt magn + fjárhagslegt magn) 

**Athugasemd:** Ef valkosturinn **Taka með efnislegt virði** er ekki valinn fyrir vöru notar kerfið notar 0 (núll) fyrir bæði efnislega upphæð og efnislegt magn. Sjá upplýsingar um þennan valkost í [Taka með efnislegt virði](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Að forðast verðmögnun
Af og til verðleggur kerfið margar úthreyfingar áður en nægilega margar innhreyfingar eru komnar sem byggja má verð á. Þær aðstæður geta valdið ofmati á hlaupandi meðaltali kostnaðarverðs. Þó eru ráðstafanir sem má gera til að forðast vandamálið eða minnka áhrif þess ef það kemur upp. **Aðstæður** Eftirfarandi færslur eiga sér stað fyrir vöru sem valkosturinn **Taka með efnislegt virði** hefur verið valinn fyrir:

1.  Fjárhagslegt móttökumagn er 100 á USD 100,00.
2.  Fjárhagsleg úthreyfingamagn er 200.
3.  Raunverulegt móttökumagn er 101 á USD 202,00.

Þegar skoðað er áætlað meðalkostnaðarverð vörunnar er búist við kostnaðarverðinu USD 1,51. Þess í stað er að finna áætlað meðalverð upp á USD 102,00, sem byggist á eftirfarandi formúlu: Áætlað verð = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 Þessi verðmögnun á sér stað vegna þess að þegar vörurnar 200 eru hreyfðar út fjárhagslega í skrefi 2, verður kerfið að verðleggja 100 af vörunum áður en neinar samsvarandi innhreyfingar koma til. Þessar aðstæður orsaka neikvæðar birgðir. Kerfið áætlar síðan einingarverðið USD 1,00, sem við má búast. Hins vegar þegar samsvarandi 100 innhreyfingar koma, eru þær á einingarverðinu USD 2,00 hver. 

**Athugið:** Þó að úthreyfingarnar leiði af sér neikvæðar birgðir eru birgðir jákvæðar þegar úthreyfingarverðið er reiknað. Þess vegna er meðalkostnaðarverð notað í staðinn fyrir verð í aðalvörufærslunni. Þegar hér er komið hefur kerfið birgðavirðisjöfnun sem er USD 100,00. Og meðan sú jöfnun var byggð upp yfir 100 stykki þar sem það var á USD 1,00 hvern, höfum við nú aðeins eitt stykki í birgðum. Þess vegna er jöfnuðu tapi upp á USD 100,00 er úthlutað á þetta eina stykki. Niðurstaðan er ofhækkun á áætluðu kostnaðarverði. 

**Athugið:** Til samanburðar má sjá að ef skrefum 2 og 3 er snúið við í dæminu hér að framan verða 200 vörur hreyfðar út á einingarverðinu USD 1,51, og eitt stykki verður eftir á einingarverðinu USD 1,51. Þar sem þetta verðmögnunartilfelli getur komið upp þegar um neikvæðar birgðir er að ræða er erfitt að forðast eftirfarandi tilfelli:

-   Meta verður úthreyfingaverð á lagerbirgðavirði og magni.
-   Leiðrétta verður virði lagerbirgða og magn á út- og innhreyfingum.
-   Viðskiptalíkanið leyfir útsendingu eða verðlagningu fleiri stykkja en eru fyrir hendi.
-   Samþykkja verður allt innhreyfingarvirði og magn sem er sent.

Samt sem áður, ef viðskiptalíkanið leyfir eftirfarandi venjur geta þær hjálpað til við að forðast neikvætt magn sem getur skapað verðmögnun:

-   Ef valkosturinn **Taka með efnislegt virði** er valinn fyrir vöru, skal hreinsa gátreitinn **Efnislega neikvæðar birgðir** á síðunni **Vörulíkanaflokkar**.
-   Ef *ekki* er valinn valkosturinn **Taka með efnislegt virði** fyrir vöru, skal hreinsa valkostinn **Fjárhagslega neikvæðar birgðir** á síðunni **Vörulíkanaflokkar**.

Hafið einnig í huga að hámarksjöfnunin á efnislegu birgðavirði er takmörkuð af fjölda efnislegra færslna og mismun milli efnislegs og fjárhagslegs verðs. Svo lengi sem allar efnislegar færslur eru að lokum uppfærðar fjárhagslega getur efnislegt virði ekki hækkað óstjórnlega. Að lokum skal minnt á að mögnunaráhrifin minnka verulega þegar samanlagða jöfnunin dreifist á nokkur stykki í lagerbirgðum en ekki bara eitt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]