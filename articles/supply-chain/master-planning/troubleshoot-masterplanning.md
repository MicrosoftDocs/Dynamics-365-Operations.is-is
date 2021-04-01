---
title: Úrræðaleit fyrir aðaláætlanagerð
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með aðaláætlanagerð.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: db336946873fa1b5cc3f669823541af8cab4115b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216106"
---
# <a name="troubleshoot-master-planning"></a>Úrræðaleit fyrir aðaláætlanagerð

Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með aðaláætlanagerð.

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a>Niðurbrot uppskriftar hegðar sér á annan hátt fyrir staðfestar framleiðslupantanir og fyrir áætlaðar framleiðslupantanir fyrir vinnu sem er búið að stofna handvirkt.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar framleiðslupöntun er staðfest eru vörurnar ekki brotnar niður þegar þú brýtur uppskriftirnar niður. Hins vegar þegar þú stofnar verkbeiðni handvirkt og áætlar síðan framleiðslupöntunina eru vörurnar brotnar niður.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Kerfið virkar eins og búist var við. Niðurbrotið sem verður þegar framleiðslupöntunin er staðfest vísar á áætlaða pöntun en áætlaða pöntunin virðist ekki vera staðfest í þessu tilviki. Ef framleiðslupöntunin hefur hins vegar verið metin er niðurbrotið ræst af útgefnu framleiðslupöntuninni þegar engin áætluð pöntun er til staðar.

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a>Seinkunargildið er ekki uppfært þegar ég enduráætla áætlaða pöntun.

Til að uppfæra seinkun á áætluðum pöntunum skal opna svargluggann **Endurröðun** fyrir áætluðu pöntunina. Á flýtiflipanum **Niðurbrot** skal ganga úr skugga um að **Framkvæma niðurbrot eftir að endurröðunarvalkosturinn** er stilltur á *Já*.

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a>Framleiðsluröðun tekur ekki til greina öryggismörk sem eru stillt á vöruþekju fyrir fest framboð.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Aðaláætlanagerð áætlar öryggismörk. Hins vegar eru öryggismörk hunsuð um leið og áætlaðar framleiðslupantanir eru áætlaðar.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Aðeins er tekið tillit til marka við aðaláætlanagerð, ekki við handvirka áætlanagerð. Mörk eiga að gegna hlutverki biðminnis við áætlunarferlið til að setja tiltekin „mörk“ fyrir raunverulega ferlið.

Til að fá æskilega útkomu er hægt að fjarlægja framlegðina. Síðan verður að uppfæra leiðina þannig að hún innihaldi tímann sem óskað er eftir (til dæmis, sem biðtími). Bæði aðaláætlanagerð og handvirk röðun ættu þá að búa til sömu niðurstöður.

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a>Áætlaðar pantanir eru myndaðar þrátt fyrir að vörur séu á lager og framleiðslupantanir séu þegar til fyrir þær.

Hugsanlega er hægt að laga vandamálið með því að auka gildið **Jákvæðir dagar** fyrir viðeigandi flokka á síðunni **Þekjuflokkur**. Þessi breyting veldur því að kerfið ákveður hvort hægt er að nota lagerbirgðir til að anna eftirspurn. Þá verður ný áætluð pöntun ekki mynduð fyrir vörurnar sem eru í birgðum.

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a>Aðaláætlanagerð virðist ekki taka mið af takmörkunum afkastagetu og áætlar meira en tiltæk afkastageta.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar aðgerðaröðun er notuð þar sem takmörkuð afkastageta er til staðar og leiðin tilgreinir blöndu af kröfum bæði tilfangaflokks og einstakra tilfanga er möguleiki á ofbókun vegna aðferðarinnar sem algrím notar til að villuleita árekstra í afkastagetu. Þessi ofbókun getur átt sér stað þegar hjálpartæki eru notuð til að keyra aðaláætlanagerð. Líklegra er að slíkt hendi þegar mörg verk með hlutfallslega stutta keyrslu eru til staðar.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þegar nauðsynlegt að engin ofbókun eigi sér stað við aðgerðaröðun er hægt að gera áætlanahluta aðaláætlanagerðarinnar að stökum þræði með því að kveikja á valkostinum **Nákvæm takmörkuð geta fyrir aðgerðaröðun** á síðunni **Færibreytur aðaláætlanagerðar**. Þessi valkostur er ekki tiltækur sjálfgefið. Þú verður að bæta henni handvirkt við síðuna með því að nota sérstillingar. Þegar þessi valkostur er notaður verður áætlanagerð keyrð hægar því samhliða keyrsla er ekki til staðar.

## <a name="planned-orders-take-a-long-time-to-update"></a>Það tekur langan tíma að uppfæra áætlaðar pantanir.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar þarfamagn og/eða afhendingardagsetning áætlaðrar pöntunar er uppfært tekur a.m.k. 30 sekúndur að vista uppfærsluna á pöntun.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta er þekkt vandamál með innbyggðri aðaláætlunarvél. Slíkt stafar af undirliggjandi, sjálfvirku niðurbroti í skipulagi uppskriftarinnar á meðan breytingar eru gerðar. Slíkt vandamál er leyst með fínstillingu skipulagningar, þar sem áætlun getur uppfært og samþykkt viðeigandi pantanir og þegar þess er óskað, keyrt uppfærslu áætlaðra pantana fyrir undirliggjandi skipan uppskrifta.

Ein leið til að auka afköst með innbyggðri aðaláætlunarvél er að gera eftirfarandi:

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Velja áætlun.
1. Víkka út flipann **Tímamörk í dögum**.
1. Stilltu **Niðurbrot** á *Já* og stilltu svæðið fyrir neðan þessa stillingu á 0 (núll).

> [!NOTE]
> Slíkt takmarkar framkvæmdartímabil niðurbrota fyrir þessa aðaláætlun við einn dag.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]