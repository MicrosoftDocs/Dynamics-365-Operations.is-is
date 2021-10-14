---
title: Stjórnun uppfærslu staðalkostnaðar
description: Hægt er að stýra uppfærslum á staðalkostnaðargögnum með því að nota tvær mismunandi nálganir - einnar útgáfu nálgun og tveggja útgáfu nálgun.
author: AndersGirke
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 942b144c78176e9a00cdc12101e2948e8aa4685e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579761"
---
# <a name="manage-standard-cost-updates"></a>Stjórnun uppfærslu staðalkostnaðar

[!include [banner](../includes/banner.md)]

Hægt er að stýra uppfærslum á staðalkostnaðargögnum með því að nota tvær mismunandi nálganir - einnar útgáfu nálgun og tveggja útgáfu nálgun.

Eins útgáfu nálgun notar eina kostnaðarútgáfu sem inniheldur allar kostnaðarfærslur. Þessar færslur innifela upprunalegan kostnað og öllum kostnaðaruppfærslum.

Tveggja útgáfu nálgun notar eina kostnaðarútgáfu sem inniheldur færslur upprunalegs kostnaðar og hin útgáfan inniheldur skráningar á öllum kostnaðaruppfærslum. Aðalkosturinn við nálgunina tvær útgáfur er skýr útlistun og rakning kostnaðaruppfærslna í mismunandi útgáfum kostnaðarútreiknings án þess að upprunalega útgáfa kostnaðarútreikningsins verði fyrir áhrifum af því. Tveggja útgáfu nálgun er hægt að nota til að skilgreina margar stigvaxandi uppfærslur, þar sem hver stigvaxandi uppfærsla hefur sína eigin útgáfu kostnaðarútreiknings sem inniheldur stigvaxandi kostnaðarfærslurnar.

## <a name="example"></a>Dæmi

Eftirfarandi dæmi sýnir hvernig hægt er að nota einnar útgáfu og tveggja-útgáfu nálganir fyrir uppfærslu staðalkostnaðar í framleiðsluumhverfi. Til dæmis uppfærslur sem endurspegla nýjar vörur eða leiðréttingar á villum. Gefum okkur að stök útgáfa kostnaðarútreiknings standi fyrir staðalkostnað núverandi árs. Kenni fyrir þessa útgáfu er 2020 STD. Útgáfa 2020 STD inniheldur núgildandi virkan kostnað fyrir allar vörur. Hún inniheldur allar leiðartengdar kostnaðartegundir og útreikningsformúlur stjórnunarkostnaðar sem þekktust í byrjun árs 2020. 2020-STD er upprunalega kostnaðarútgáfan.

- **Einnar útgáfu nálgun við uppfærslu kostnaðargagna** − Í Einnar útgáfu nálgun inniheldur upprunalega kostnaðarútgáfa 2020-STD allar kostnaðarfærslur. Kostnaðaruppfærslur skráðar í 2020-STD-CHANGES og eru stillt á stöðuna „Í Bið“. Hægt er að færa biðstöðukostnaðinn handvirkt inn fyrir nýju keyptu vörurnar eða þá að hægt væri að reikna hann út fyrir framleidda vörur til að endurspegla leiðréttingar. Þegar ein útgáfa er notuð gera uppskriftarútreikningar ekki kröfu um varaútgáfu af því að allur virkur kostnaður er innan útgáfu kostnaðarútreikningsins. Eftir að búið er að virkja biðstöðukostnaðinn inniheldur upprunalega útgáfa kostnaðarútreikningsins 2020-STD aftur allan núgildandi virkan kostnað.
- **Tveggja útgáfu nálgun á uppfærslur kostnaðargagna** − tveggja útgáfu nálgunin krefst viðbótar kostnaðarútgáfu sem inniheldur aðeins kostnaðaruppfærslur. kennimerki fyrir þessa útgáfu er 2020-STD-CHANGES Kostnaðaruppfærslur eru skráðar í 2020-STD-CHANGES og eru stillt á stöðuna "Í Bið." Í tveggja útgáfu nálguninni þarf uppskriftarútreikningur kostnaðar í bið fyrir framleiddar vörur varaútgáfu. Þetta er vegna þess að viðbótar kostnaðarútgáfu 2020-STD-CHANGES inniheldur aðeins hlutmengi kostnaðargagna. Hægt er að birta vararegluna sem virka kostnaðinn eða kostnaðarútgáfu 2020-STD vegna þess að bæði tilgreina uppruna kostnaðargagnanna þegar hann er ekki innifalinn í 2020-STD-CHANGES. Eftir að búið er að virkja biðstöðukostnaðinn inniheldur kostnaðarútgáfan 2020-STD-CHANGES núgildandi virka kostnaðinn sem endurspeglar uppfærslurnar á meðan upprunalega kostnaðarútgáfan 2020-STD helst óbreytt. Þegar tveggja útgáfu nálgunin er notuð ætti að setja upp lokunarreglur fyrir upprunalegu kostnaðarútgáfuna til koma í veg fyrir uppfærslur. Alveg eins lokunarreglur ætti að setja upp fyrir aukalegu kostnaðarútgáfuna, nema fyrir tilgreinda frá-dagsetningu og valfrjálsri notkun lokunarreglna til að gera uppfærslur leyfilegar. Uppfæra ætti dagsetninguna sem tilgreint er frá með hverri breytingarunu til að endurspegla áætlaða virkjunardagsetningu.

Þetta dæmi notaði eina aukaútgáfu kostnaðarútgáfu við stjórnun uppfærslna í gegnum árið 2020. Fleiri en eina aukaútgáfu kostnaðarútgáfu er hægt að nota, eins og aðskilda útgáfu fyrir hverja uppfærslurunu. Þegar fleiri en ein viðbótar kostnaðarútreikningur er notað, verður varaútgáfan að vera sýnd sem virka kostnaðinn, af því virkan kostnað eru dreifast yfir margar kostnaðarútgáfur.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Fjárhagsvíddir fyrir endurmat staðalkostnaðar

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Ef nýtt staðlað verð er virkjað verður birgðavirði yfirleitt endurmetið með endurmatsfærslum staðalkostnaðar. Yfirleitt eru fjárhagsvíddir vörunnar þá bókaðar í færslunum. Ef hins vegar vilji er til þess að stjórna því hvort og hvernig fjárhagsvíddir eru bókaðar skal nota [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum sem heitir *Valmöguleikar á að gera fjárhagsvíddir sjálfgefnar fyrir endurmat á staðalkostnaði birgða*. Þegar þessi eiginleiki hefur verið virkjaður skal opona **Kostnaðarstjórnun > Skipulag á reglum birgðabókhalds > Færibreytur** og stilla nýja fellilistann **Uppruni fjárhagsvíddar** á eitt af eftirfarandi gildum:

- **Engar** – Engar fjárhagsvíddir eru bókaðar í færslum endumats. Ef lykilskipulagið felur í sér áskilda fjárhagsvídd mun endurmatsferlið halda keyrslu áfram, en mun stofna bókhaldsfærslur sem eru ekki með neinar fjárhagsvíddir. Í slíku tilfelli koma fyrst upp viðvörunarboð þannig að hægt sé að hætta við endurmatið ef nauðsyn krefur.
- **Tafla** - Fjárhagsvíddir vörunnar eru bókaðar í endurmatsfærslunum. Þetta er sjálfgefin stilling og er í samræmi við upprunalega virkni kerfisins án þess að kveikt sé á eiginleikanum *Valmöguleikar á að gera fjárhagsvíddir sjálfgefnar fyrir endurmat á staðalkostnaði birgða*.
- **Bókun** - Fjárhagsvíddir færslunnar sem verið er að endurmeta eru bókaðar á endurmatsfærslurnar. Sjálfgefið er að fjárhagsvíddir upprunalega birgðarreiknings færslunnar séu notaðar bæði fyrir birgðarreikninginn og endurmatsreikninginn.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]