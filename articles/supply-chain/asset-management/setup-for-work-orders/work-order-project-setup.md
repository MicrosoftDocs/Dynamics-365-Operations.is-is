---
title: Verkuppsetning verkbeiðni
description: Þetta efni útskýrir uppsetningu verka verkbeiðna í eignastýringu.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjectSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bb897ca0a7e9c45ee55244189bb1b487fbddf0714ad3ea0cac26eb7bac36a07f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754084"
---
# <a name="work-order-project-setup"></a>Verkuppsetning verkbeiðni

[!include [banner](../../includes/banner.md)]

 

Í einingunni **Eignastýring** er verkvensla krafist fyrir hvert verk verkbeiðni. Verkefnið sem er tengt verkbeiðniverki gerir þér kleift að fylgjast með kostnaði við ýmis verkefni sem tengjast eignastýringu, svo sem innri viðhaldsverkefnum, þjónustustjórnunarverkum og fjárfestingarverkefnum. 

## <a name="project-setup-for-a-work-order-job"></a>Verkuppsetning fyrir verkbeiðniverk

Þegar þú býrð til verkbeiðniverk í verkbeiðni ákvarða verkuppsetningin í einingunni **Verkefnisstjórnun og bókhald** og verkuppsetning verkbeiðni í einingunni **Eignastýring** hvernig hægt er að nota verk til að stjórna kostnaði á eigninni sem er valin í því verkbeiðniverki. Þessi hluti lýsir eftirtöldum hlutum verkuppsetningarinnar sem notaðar eru í verkbeiðni: yfirverkið (kenni verksins), tegund verkefnis, verkþættir og fjárhagsvíddir:

- Þegar þú býrð til verkbeiðniverk í verkbeiðni eru einkvæmt auðkenni verks og tengdir verkþættir sjálfkrafa stofnaðir fyrir hana. Hins vegar, ef nokkur verkbeiðniverk í verkbeiðni innihalda sömu eign er sama verkkenni notað fyrir þau. Með öðrum orðum er eitt verkefnisauðkenni stofnað fyrir hverja eign í verkbeiðni.

    - Yfirverkið (verkkennið) fyrir verkbeiðniverk er að finna í uppstillingu yfirverks. (Nánari upplýsingar um skipulag yfirverka, sjá næsta kafla.) Til dæmis, ef þú tengir viðskiptavin eða virka staðsetningu við tiltekið yfirverk, er yfirverkið notað í hvert skipti sem þú býrð til verkbeiðnir fyrir þann viðskiptavin eða þessa virku staðsetningu. Ef þú tengir ekki tiltekið verkkenni við, til dæmis, virka staðsetningu er næsta viðeigandi yfirverk í verkbeiðnauppsetningunni notað.
    - Verkgerð er nauðsynleg fyrir hvert verkkenni. Verkkennið er að finna í uppsetningu verkefnahópsins. (Nánari upplýsingar um uppsetningu verkefnahópsins er að finna í næsta kafla.) Ef enga samsvörun er að finna í uppsetningu verkefnahópsins er uppsetning verkefnahópsins á yfirverkinu notuð.
    - Uppsetningin til að krefjast verkþátta á spám og færslubókum er afrituð úr yfirverkinu yfir í verkbeiðniverkið. Ef valkostirnir **Klukkustund**, **Kostnaður** og **Liður** eru stilltir á **Já** fyrir verkið sem er notað sem yfirverk er verkþáttur skylda í spám og færslubókum. (Til að fá aðgang að þessum valkostum, velurðu **Verkefnisstjórnun og bókhald** \> **Verk** \> **Öll verk** og síðan verkið sem er notað sem yfirverk. Valkostirnir eru í hlutanum **Krefjast verkþátta í færslubókum** á flýtiflipanum **Uppsetning**.)

- Fjárhagsvíddir eru afritaðar úr eigninni og sameinaðar yfirverkinu.

Næsti hluti útskýrir hvernig á að setja upp yfirverk og verkefnahópa. Yfirverk og yfirhópar eru notaðir til að stjórna verkbeiðnum. Þau eru einnig notuð til að tilkynna um verkbeiðnir.

## <a name="set-up-work-order-projects"></a>Setja upp verkbeiðniverk

Áður en byrjað er að búa til verkbeiðnir verður þú að setja upp verkbeiðniverk. Síðan **Uppsetning verkbeiðniverks** (**Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Uppsetning verks**) inniheldur tvo flipa: **Yfirverk** og **Verkefnahópur**.

Á flipanum **Yfirverk** er hægt að setja upp verkefnatengsl sem hægt er að nota ef ekkert verkefni er sett upp á eigninni sem er valin í verkbeiðniverkið. Uppsetning yfirverks er ekki krafist ef fyrirtæki þitt notar eignaverkefni. Það skiptir aðeins máli ef þú vilt nota verkbeiðniverk í stað eignaverkefna. Í því tilfelli verður þú að setja upp að minnsta kosti eitt yfirverk.

Á flipanum **Verkefnahópur** geturðu sett upp verkefnahópa sem geta verið tengdir gerðum verkbeiðna, eignategundum og eignum.

Hægt er að nota verkefnahópa til að búa til ákveðna flokka (hópa) sem eru notaðir til að stjórna kostnaði. Til dæmis með því að búa til verkefnahópa fyrir sérstakar eignategundir eða tegundir verkbeiðna er hægt að gera nákvæmar mælingar á viðhaldskostnaði eftir tegundum.

Verkefnahópar eru ekki skylda. Ef þú setur ekki upp verkefnahópa er yfirverkið notað til að ákvarða verkefnahópinn og undirverk er búið til úr verkefnahóp yfireiningarinnar.

Uppsetningin gerir ráð fyrir fullkominni samþættingu við eininguna **Verkefnisstjórnun og bókhald**. Þess vegna getur þú fylgst með kostnaði sem er tengdur verkbeiðnum í tengdum verkefnum. Eftirfarandi ferli lýsir uppsetningunni á verkbeiðniverkum.

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Verkuppsetning**.
2. Á flipanum **Yfirverk** velurðu **Bæta við**.
3. Í reitunum **Gerð verkbeiðni**, **Virk staðsetning**, **Gerð eigna**, og **Eign** velurðu gildi eftir þörfum. Fyrir hverja línu sem þú bætir við geturðu stillt bara einn reit eða marga reiti. Fjöldi reita sem þú stillir ákvarðar samsetningu sem er notuð þegar verkefnisauðkenni er valið í Eignastjórnun. 

    Ef þú velur virka staðsetningu eru viðkomandi undirstaðsetningar sjálfkrafa innifaldar. Ef þú velur eign geturðu búið til fleiri verkbeiðniverksuppsetningarlínur fyrir sömu eign, en þú getur valið mismunandi verk fyrir þá eign.

4. Í reitnum **Verkkenni** velurðu verkið sem ætti að tengjast uppsetningunni sem þú bjóst til í 3. þrepi.
5. Ef verkuppsetning skal aðeins vera gild í takmarkaðan tíma skal velja lokadagsetningu í reitnum **Lokadagsetning**. Að öðrum kosti skal velja **Ekkert**.

    Sjálfgefið er að upphafsdagsetningin sé dagsetningin þegar þú bætir verkbeiðniverkinu við síðuna. Því er stjórnað af reitnum **Gildir frá** sem er falinn sjálfgefið. Til að sýna reitinn **Gildir frá** velurðu **Skoða** \> **Allt**. Þú getur síðan notað reitinn **Gildir frá** ásamt reitnum **Lokadagsetning** til að setja upp takmarkaðan gildistíma verkbeiðnaverksins.

    ![Síða fyrir verkuppsetningu verkbeiðni.](media/17-setup-for-work-orders.png)

6. Á flipanum **Verkefnahópur** velurðu **Bæta við**.
7. Í reitnum **Verkbeiðni** velurðu gerð verkbeiðni.
8. Ef þú vilt að tenging verkefnahópsins sé nákvæmari skaltu velja eignategundina í reitnum **Gerð eigna** eða eign í reitnum **Eign**.
9. Í reitnum **Verkefnahópur** velurðu verkefnahópinn sem ætti að tengjast gerð verkbeiðninnar. Til dæmis kann gerð verkbeiðni sem er nefnd **Forvirkt viðhald** verið tengd verkefnahópi sem er nefndur **Fyrra viðh.** eða **Innra**. Að öðrum kosti, kann gerð verkbeiðni **Fjárfesting** sem er notuð við verkbeiðnir sem tengjast fjárfestingum og fastafjármunum að tengjast verkefnahópi sem nefndur er **Fjárfesta** eða **Fjárfesting**.
10. Veldu **Vista**.

![Síða fyrir verkuppsetningu verkbeiðni, Bæta við verkbeiðni.](media/18-setup-for-work-orders.png)

> [!NOTE]
> Í hvert skipti sem verkbeiðnilína er búin til leitar Eignastjórnun að verkefnahópi sem ætti að tengjast verkbeiðniverkefninu. Leitin er byggð á uppsetningunni sem lýst er í þessu efni. Sérhver verkefnahópur er með tilheyrandi verkefnisgerð. Verkefnahópar sem hafa verkgerðina **Tími og efni** eða **Fast verð** gilda aðeins fyrir eignir sem tengjast viðskiptamannareikningi.
>
> Fyrir yfirverk og verkefnahópa, þegar kerfið velur fyrirliggjandi verkþáttarverk eða verkefnahóp, er valið byggt á skrám sem þú stofnaðir með því að nota fyrra ferli. Eignastýring fer í gegnum skrár sem tengjast verkbeiðnaverki til að leita að mögulegri samsvörun. Það athugar alltaf sértækustu samsetninguna fyrst. Með öðrum orðum, fyrir yfirverk verkbeiðninnar kannar Eignastjórnun fyrst hvort möguleg samsvörun finnist fyrir reitinn **Eign**. Ef engin samsvörun finnst leitar hún að samsvörun fyrir reitinn **Eignagerð**. Ef engin samsvörun finnst leitar hún að samsvörun fyrir reitinn **Virk staðsetning** og svo framvegis. Eins og þú sérð á skipulagi síðunnar **Verkuppsetning verkbeiðni** þýðir þessi hegðun að til að finna sértækustu samsetninguna, þá velur eignastjórnun hverja skrá frá hægri til vinstri fyrir leik. Ef engin samsvörun finnst er sjálfgefna skráin þar sem aðeins verkkenni er valið notuð. Ferlið til að finna tengdan verkefnahóp er svipað. Eignastýring leitar fyrst að mögulegri samsvörun við reitinn **Eign**, síðan reitinn **Gerð eigna** og síðan reitinn **Gerð verkbeiðni**. Ef engin samsvörun finnst er sjálfgefna skráin þar sem aðeins verkhópur er valinn notuð.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]