---
title: Stofna endurtekna innkaupapöntun
description: Þessi grein sýnir hvernig á að stofna endurtaka innkaupapöntunina (PO) með því að afrita línur úr eldri innkaupapöntunarskjalinu í nýja Innkaupapöntun eða fyrirliggjandi Innkaupapantana.
author: GalynaFedorova
ms.date: 09/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, PurchCopying
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 335461d60fa0bc92e9711806c6e42643a3f75d02
ms.sourcegitcommit: 073604c07116e0a87f78ab2c76cb89ae83ebba3c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2022
ms.locfileid: "9608112"
---
# <a name="create-a-repeat-purchase-order"></a>Stofna endurtekna innkaupapöntun

[!include [banner](../../includes/banner.md)]

Þessi grein sýnir hvernig á að stofna endurtaka innkaupapöntunina (PO) með því að afrita línur úr eldri innkaupapöntunarskjalinu í nýja Innkaupapöntun eða fyrirliggjandi Innkaupapantana. Það eru tvær aðferðir til þess að stofna endurtakar pantanir. Hægt er að nota aðgerðirnar sem eru tiltækar á stigi skjalsins úr Aðgerðarúðunni, eða hægt er að nota aðgerðir línuupplýsingar. Aðgerðir á skjalastigi eru ætlaðar til að stofna nýja innkaupapöntun með því að bæta upplýsingum úr haus og línum úr annarri pöntun, meðan aðgerð línuupplýsinga er aðallega til að bæta línum við fyrirliggjandi pöntun. Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins. Þetta verk myndi venjulega vera framkvæmt af innkaupaaðila.

## <a name="create-a-new-repeat-purchase-order"></a>Stofna nýja endurtekna innkaupapöntun

1. Í skoðunarrúðunni ferðu í **Kerfiseiningar \> Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**. Fyrst reynum við valkostinn að afrita upplýsingar á nýju pöntun.  
1. Veljið **Nýtt**.
1. Í svæðinu **Lánardrottnalykill** skal slá inn `US-101`.
1. Veldu **Í lagi**.
1. Á aðgerðasvæðinu skal opna flipann **Innkaupapöntun** og í hópnum **Afrita** skal velja **Úr öllu**. Svarglugginn **Afrita úr öðrum skjölum** opnast. Þaðan er hægt að afrita úr fyrirliggjandi pöntunum í pöntunina þína. Mismunandi valmöguleikar eru til staðar hvernig línur eru afritaðar, og mismunandi gerðir af skjölum sem hægt er að afrita úr. Fyrst skoðum við valkosti fyrir því hvernig línur eru afritaðar.
1. Flýtiflipinn **Greiðslur** er stækkaður.

    - Reiturinn **Magnstuðull** er gagnlegur ef nauðsynlegt er að nota magn sem er annað en það sem er í pöntuninni sem verið er að afrita úr. Til dæmis, ef óskað er að panta tvöfalt magnið sem er í línunum sem verið er að afrita úr væri fært inn „2” í þessu svæði og síðan bætir kerfið við línum þar sem upphaflegt magn hefur verið tvöfaldað.  
    - Reiturinn **Snúa við formerki** styður líka við breytingu á pöntuðu magni með því að breyta formerki magns fyrir pöntunarlínur sem er bætt við. Þetta gæti verið gagnleg ef nauðsynlegt er að bakfæra færsluna, með því að stofna pöntunarlínur sem ógilda færsluna. Þessi valkostur er valinn sjálfvirkt þegar síðan er opnað úr aðgerðina **Stofna kreditnótu**.  
    - Valkosturinn **Afrita gjöld** leyfir þér að afrita gjöld yfir í nýja pöntunina úr skjalinu þaðan sem verið er að afrita pöntunarlínur.  
    - Valkosturinn **Endurreikna verð** notar gildandi verð og afslátt frekar en að afrita þær úr skjalinu sem verið er að afrita aðrar upplýsingar úr.  
    - Valkosturinn **Afrita nákvæmlega** afritar gildin úr nokkrum reitum í pöntunarhausnum og línum. Ef þessi valkostur er ekki valinn verða sjálfgefin gildi notuð fyrir marga af reitunum sem tengjast lánardrottni og afurðum, rétt eins og þegar ný pöntun er stofnuð handvirkt. Ef þú stillir til dæmis **Afrita nákvæmlega** á *Já* og afritar pöntun sem hnekkir sjálfgefnum reikningslykli fyrir lánardrottin verður sami reikningslykillinn afritaður í nýju pöntunina. Ef þú stillir **Afrita nákvæmlega** á *Nei* verður sjálfgefinn reikningslykill fyrir lánardrottin notaður í nýju pöntunina í staðinn. Gildi fyrir eftirfarandi reiti eru afrituð þegar **Afrita nákvæmlega** er stillt á *Já*:
        - Tungumál
        - Greiðsluskilmálar
        - Greiðsluháttur
        - Greiðsluupplýsingar
        - Númeraraðaflokkur
        - Staðgreiðsluafsláttur
        - Afsláttarprósenta
        - Gjaldmiðill
        - Afhendingarskilmálar
        - Afhendingarmáti
        - Vídd
        - VSK-flokkur
        - Hnekkja virðisaukaskatti
        - Verð eru með virðisaukaskatti
        - Flutningur
        - Afh.staður
        - Vinnsla talnagagna
        - Sniðmátskenni
        - Afhendingarheiti
        - Póstaðsetur
        - Tilvísun
        - Kenni tilvísunartöflu
    - Valkosturinn **Eyða innkaupalínum** eyðir öllum innkaupapantanalínum sem þegar eru til staðar á innkaupapöntuninni sem verið er að afrita í, áður en nýju línurnar eru notaðar. Notið þennan valkost varlega, þar sem hann eyðir öllum fyrirliggjandi línum án frekari viðvörun .  
    - Ef þú notar valkostinn **Afrita pöntunarhaus** þarftu ekki að stofna hausupplýsingar handvirkt í nýju pöntunina. Þessi valkostur veldur því að notuð eru sjálfgefnum gildum fyrir svæðin sem eru tengdar við lánardrottinn. Ef skjalið sem verið er að afrita úr hefur ósjálfgefin gildi sem á að afrita skal líka nota valkostinn **Afrita nákvæmlega**.
    - Til eru mismunandi upprunar skjala sem hægt er að afrita úr, og hver hefur sérstakan hluta á þessari síðu. Til dæmis gerir kaflinn **Innkaupapantanir** þér kleift að afrita úr fyrirliggjandi innkaupapantanir.  

1. Í kaflanum **Innkaupapantanir** velurðu línurnar sem þú vilt afrita á klemmuspjaldið þitt. Hægt er að velja frekari innkaupapöntunarlínur úr öðrum innkaupapöntunum og afrita þær líka í pöntunina. Einnig er hægt að bæta við línum úr annars konar innkaupaskjölum. Næstu skref skoða mismunandi valkostir.  
1. Útvíkkaðu kaflann **Staðfesting**. Hér er hægt að velja staðfestingar á innkaupapöntunum til að afrita úr. Staðfestingar á innkaupapöntunum eru auðkenndar með viðkomandi innkaupabókarkenni eða kenni innkaupapöntunar.  
1. Útvíkkaðu kaflann **Innhreyfingarskjal afurða**. Hér er hægt að velja færslubækur innhreyfingarskjala til að afrita úr. Færslubækur innhreyfingarskjala eru auðkenndar með fylgiskjali innhreyfingarskjala eða kenni innkaupapöntunar.
1. Útvíkkaðu kaflann **Reikningar**. Hér er hægt reikningur lánardrottins sem afrita á úr. Reikningarnir eru auðkenndar með fylgiskjali reikningsins eða kenni innkaupapöntunar.
1. Útvíkkaðu kaflann **Valdar línur eða haus til afrituna**. Þetta yfirlit sýnir samantekt yfir öll skjöl og línur sem hafa verið valdar til afritunar í þína pöntunina.
1. Veljið **Í lagi**. Línurnar sem þú valdir hafa verið afritaðar í nýju innkaupapöntunina.

## <a name="copy-lines-to-an-existing-purchase-order"></a>Afrita línur í fyrirliggjandi innkaupapöntun  

Frekar en að Afrita heila pöntun, er algengara að stofna nýja innkaupapöntun og klára upplýsingarnar í haus innkaupapöntunar, og afrita einstakar línur úr fyrirliggjandi pöntunum.  

1. Veldu línuna **Innkaupapöntun**.
1. Veldu **Úr öllu**. Síða sem opnast er eins og sú sem var sýnd áður, en mismunandi valkostir eru valdir þegar hún er opnuð úr yfirliti pöntunarlína. Endurskoðum nú færibreyturnar.
1. Útvíkkaðu hlutann **Færibreytur**.

    - Valkosturinn **Eyða innkaupalínum** er ekki valinn. Þetta þýðir að hægt er að afrita nýjar línur í pöntunina án þess að fjarlægja fyrirliggjandi línur.
    - Valkosturinn **Afrita pöntunarhaus** er ekki heldur valinn, þar sem aðeins er verið að bæta fleiri línum í pöntun.
    - Í þessu dæmi munum við afrita línur úr fyrirliggjandi innkaupapöntun.

1. Veldu línu fyrir æskilega innkaupapöntun. Athugið að staka pöntunarlínan sem er í þessari innkaupapöntun er einnig valin.  
1. Veljið **Í lagi**. Viðbótar pöntunarlínan hefur verið bætt við innkaupapöntun.  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]