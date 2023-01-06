---
title: Endurmeta leigugreiðslur sem eru tengdar vaxtavísitölu
description: Þessi grein lýsir leiðréttingunni sem er gerð á leigusamningnum fyrir afnotarétt af eign þegar breytilegar leigugreiðslur breytast vegna breytinga í vaxtavísitölu.
author: moaamer
ms.date: 01/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRevaluation
audience: Application User
ms.reviewer: twheeloc
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 8dc2325e9f0651bea0d70d9f66e5d88b741009f8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903248"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Endurmeta leigugreiðslur sem eru tengdar vaxtavísitölu

[!include [banner](../includes/banner.md)]

Þessi grein lýsir leiðréttingunni sem er gerð á leiguskuldbindingu fyrir afnotarétt af eign þegar breytilegar leigugreiðslur breytast vegna breytinga í vaxtavísitölu. Leiguskuldbinding og afnotaréttur af eign verður breytt til samræmis við nýju greiðsluupphæðirnar. Samkvæmt efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) sem er staðall fyrir almennt samþykktar reikningsskilareglur í Bandaríkjunum (US GAAP) breytast einungis breytilegar greiðslur þegar greiðslur hækka eða lækka vegna breytinga á vaxtavísitölunni, að því undanskildu að frekari breytingar verði á sjóðstreymi. Slíkar frekari breytingar geta falið í sér breytingar á leigutíma sem tengist vöxtum. Frekari upplýsingar eru í ASC 842-10-55-225 og 42(b). gr. alþjóðlega reikningsskilastaðalsins 16 (IFRS 16).

## <a name="adjust-lease-payments"></a>Breyta leigugreiðslum

Fylgdu eftirfarandi skrefum til að endurmeta leigugreiðslur sem eru tengdar við vaxtavísitölu.

1. Til að keyra endurmatsferli vísitölu leigusamnings skal opna **Eignarleiga \> Reglubundið \> Endurmat á vísitölu**.

    Síðan **Endurmat á vísitölu** opnast og birtir öll fyrri endurmatsferli vísitölu leigusamnings sem hafa verið keyrð. Upplýsingarnar á þessari síðu innihalda auðkenni ferlisins sem var mynduð úr uppsetningu númeraraðar, lögaðilanum, fjöldi leigubóka sem voru leiðréttar, heildar skuldaleiðréttingu fyrir IFRS 16 leigusamninga og fjölda breytilegra greiðslna sem voru leiðréttar fyrir ASC 842 leigusamninga.

2. Veldu **Endurmat á vísitölu leigusamnings** á aðgerðasvæðinu til að keyra endurmatið.

    Svarglugginn **Færibreytur endurmats á vísitölu** opnast. Hér er hægt að sía úr og velja hvaða leigusamningar, leigusamningsflokkar eða önnur viðmið skal notað þegar þú velur leigusamninga til endurmats. Að auki á flipanum **Keyra í bakgrunni** getur þú sett upp endurmatsferli vísitölunnar til að keyra ferlið í runu.

4. Veldu síurnar til að velja leigusamninga sem skal taka með í bakgrunnsvinnslunni og smelltu síðan á **Í lagi**.

    Svarglugginn **Forskoðun endurmats á vaxtavísitölu** opnast og sýnir leigusamningana sem verða endurmetnir. Einnig birtist eignin og skuldaleiðréttingar eða leiðréttingar á breytilegu greiðslunni.

5. Til að koma í veg fyrir að leigusamningar séu endurmetnar skal velja leigusamningana **ætti** að endurmeta. Allir leigusamningar verða endurmetnir ef þú velur enga leigusamninga. Þegar þú hefur lokið þessu skal velja **Í lagi** til að endurmeta leigusamningana.
6. Til að skoða færslunar sem voru stofnaðar fyrir tiltekið endurmatsferli á vísitölu skal velja auðkenni vinnslunnar og síðan velja **Færslur**.

    Svargluggi birtist og sýnir upplýsingar um færslurnar sem voru stofnaðar við vinnslu.

> [!NOTE]
> Aðeins er hægt að endurmeta leigusamninga með endurmatsdagsetningu sem er á eða fyrir kerfisdagsetninguna. Kerfið hunsar sjálfkrafa alla leigusamninga sem eru með endurmatsdag sem er síðar en kerfisdagsetningin.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842-leigusamningar - Endurmat á vísitölu

Til að skoða áhrif endurmatsferli leigusamningsins á ASC 842-leigusamninga skal opna greiðsluáætlun leigusamnings. Síðan sýnir aðeins breytilegar greiðslur sem inntar hafa verið af hendi á eða eftir að endurmatsdagsetningu var breytt vegna endurmats á vísitölu. Afskriftirnar og afskriftaráætlanir haldast óbreyttar. Þegar þú býrð til reikning með breytilegri greiðslu, er breytilega greiðslan debetfærð á bókunarlykil breytilegrar greiðslu. Einnig er upphæð breytilegu greiðslunnar bætt við kreditfærsluna sem er bókuð beint á lánardrottinn, eða bókuð í bókunarlykil Glósur, miðað við uppsetningu leigubókarinnar.

Greiðsluáætlunarlínur á upplýsingasíðu leigusamningsins eru uppfærðar sjálfkrafa með nýrri línu sem tilgreinir nýju vaxtavísitöluna. Þar að auki sýnir dálkur hvort línan var búin til handvirkt eða með endurmatsferli vísitölunnar.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16-leigusamningar - Endurmat á vísitölu

Til að skoða áhrif endurmatsferlis leigusamnings á IFRS 16-leigusamninga, skal opna upplýsingar um leigusamning fyrir leiðréttan leigusamning. Svæðin **Leigutími** og **Nýtingartími eignar** hafa verið uppfærðir til að endurspegla tímann sem líður frá upphafsdegi eða leiðréttingardegi fram að endurmatsdagsetningunni. Þar að auki hafa greiðsluáætlunarlínur verið uppfærðar til að endurspegla nýjar greiðslur af leigusamningnum, nýju vaxtavísitöluna og hvernig línan var búin til.

Þú getur skoðað greiðsluáætlunina sem var mynduð og hefst á endurmatsdagsetningunni og sýnir uppfærða heildar greiðsluupphæð. Ný afskriftaráætlun leiguskuldbindingar og afskriftaráætlun eignar hefur einnig verið stofnuð til að endurspegla leiðrétta greiðsluáætlunina.

Bókarfærslan hefur sjálfkrafa bókað færslu leiðréttingabókarinnar í lykilinn fyrir breytinguna í leigugreiðslum sem tengjast endurmati vísitölunnar.

> [!NOTE]
> Ef valkosturinn **Sundurliðun greiðsluupphæðar** er virkur á síðunni **Almennt** á síðunni **Upplýsingar um leigu** og tengd bók er IFRS 16, mun endurmatsferli vísitölunnar sjálfkrafa bæta við skráningu í glugganum **Sundurliðun greiðsluupphæðar**. Upphæðin mun endurspegla þá breytingu sem gerð var á greiðslunni vegna endurmats vísitölu. Skráin verður merkt sem **Notuð við endurmat á IRFS 16 vísitölunni**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
