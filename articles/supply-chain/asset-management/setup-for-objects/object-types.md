---
title: Eignagerðir
description: Þetta efni útskýrir hvernig á að stofna eignagerðir í eignastýringu. Það lýsir einnig þeim þáttum sem tengjast eignategundum.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783354"
---
# <a name="asset-types"></a>Eignagerðir

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Þetta efnisatriði útskýrir hvernig á að stofna eignagerðir. Það lýsir einnig þeim þáttum sem tengjast eignategundum. Tegundir eigna eru notaðar sem almennir flokkar eigna. Sem dæmi má nefna CNC vélar, mælitæki og vélar vörubíla. Eignategundir eru notaðar til að stjórna starfstegundunum (viðhaldsverkefnum), eignalífsferli, eignamælingum, eignareiginleikum, sniðmátum fyrir ástandsmat og eignalíkön sem hægt er að velja fyrir eign. Þegar eign er stofnuð verður að tilgreina eignagerð.

Fyrir hverja eignategund er hægt að búa til afbrigði af skipulagi eignategundarinnar. Til dæmis, ef þú ert með eignategund sem er nefnd **Vörubílar**, geturðu búið til afbrigði af þeirri eignategund fyrir mismunandi eignaframleiðendur og eignamódel. Þú getur bætt við tilskildum varahlutum og viðhaldsáætlunum við hverja uppsetningu eigna.

Í fyrsta lagi setur þú upp nauðsynlegar eignategundir. Næst býrð þú til eignamódelin sem ættu að tengjast eignategundunum. Að lokum, á **Sjálfgefin tegund eigna** síðu, þú býrð til öll afbrigði af eignategundum sem þarf fyrir búnaðinn þinn.

## <a name="create-an-asset-type"></a>Stofna eignagerð

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignagerðir** \> **Eignagerðir**.
2. Veldu **Nýtt** til að búa til eignategund.
3. Í **Tegund eigna** reit, slærðu inn kenni eignategund.
4. Færið inn lýsandi nafn í reitinn **Heiti**.
5. í reitnum **Líftímalíkan eignar** velurðu líftímalíkan eignar. Nánari upplýsingar um líftímastöður eigna og líftímalíkön eigna, sjá [Líftímastöður eigna](object-stages.md).
6. Stilltu **Samtals** kostur á **Já** ef reikna ætti samanlögð gildi lykilafkastamælikvarða (KPI) fyrir eignir sem eru með þessa eignategund.
7. Veljið **Vista**.
8. Á flýtiflipanum **Gerðir eigna** veldu þá starfsgerðir sem eiga að tengjast eignagerðinni:

    - Til að velja starfstegund skaltu velja það í **Eftirstandandi starfstegundir** reitinn og veldu síðan hægri örvarhnappinn ![Hægri örvarhnappur](media/29-setup-for-objects.png) til að færa það til **Vinnutegundir valdar** kafla.
    - Til að velja allar tiltækar starfstegundir velurðu hnappinn ![Áfram allar örvar](media/30-setup-for-objects.png). Allar tegundir starfa eru fluttar frá reitnum **Eftirstandandi starfstegundir** reit í reitinn **Vinnutegundir valdar**.
    - Til að hætta við valið á starfstegund skaltu velja hana í **Valdar starfstegundir** reitinn og veldu síðan vinstri örvarhnappinn ![Vinstri örvarhnappur](media/31-setup-for-objects.png) til að færa hana í reitinn **Eftirstandandi Vinnutegundir**.

9. Þú getur einnig valið eignamælingarnar sem ættu að tengjast eignategundinni. Á flýtiflipanum **Eignamælingar**, gerðu val þitt með því að nota aðferðirnar sem lýst er fyrir starfstegundir í þrepi 8. Nánari upplýsingar um uppsetningu eignamælinga, sjá [Mælingar á viðhaldseignum](counters.md).
10. Þú getur einnig valið eigindagerðir sem ættu að tengjast eignategundinni. Á flýtiflipanum **Eigindagerðir**, gerðu val þitt með því að nota aðferðirnar sem lýst er fyrir starfstegundir í þrepi 8. Til að búa til ákjósanlegustu röð eigindategunda skaltu velja eigindategundina **Valdar eigindagerðir** reitinn og notaðu upp örina og örvatakkana til að færa hann. Röð eigindagerða verður sýnd á eignum sem nota þessa eignategund. Nánari upplýsingar um eignareigindirnar, sjá [Gerðir viðhaldseiginda](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Þegar þú bætir við nýjum eigindategundum á flýtiflipanum **Eigindagerðir**, núverandi eignir eru sjálfkrafa uppfærðar með þeim upplýsingum.

11. Þú getur einnig valið sniðmát ástandsmats sem ættu að tengjast eignategundinni. Á flýtiflipanum **Ástandsmat**, gerðu val þitt með því að nota aðferðirnar sem lýst er fyrir starfstegundir í þrepi 8. Fyrir frekari upplýsingar um sniðmát fyrir mat á ástandi og skráningu, sjá [Ástandsmat](../setup-for-objects/condition-assessment.md).
12. Flýtiflipinn **Eignalíkan** sýnir allar samsetningar eignaframleiðenda og gerða sem eru sett upp á völdum eignategundum. Veldu til að sjá samsetningar skiptar eftir framleiðanda **Eignalíkan** til að opna síðuna **Eignalíkan**.

    Á síðunni **Eignalíkan** er hægt að bæta við samskiptum eignalíkana – eignategunda. Að auki, á **Gerðir eigna** síðu er hægt að bæta samskiptum eignaframleiðanda við eignir beint við eignategund. Að lokum, á **Eignalíkan** síðu (**Eignastýring** \> **Uppsetning** \> **Eignir** \> **Eignalíkan**), getur þú búið til nýja eignatilbúnað framleiðanda – eignamódel - eignatengsl. Þess vegna eru þrjár leiðir til að setja upp og breyta eignum framleiðanda - eignalíkani - eignatengsl. Allar tiltækar samsetningar eru sýndar frá mismunandi sjónarhornum og þú getur valið valinn aðgangsstað þegar þú vinnur með uppsetninguna.

> [!NOTE]
> - Ef þú velur eignamælingar á eignategund eru valin uppfærð sjálfkrafa á **Eignaaðgerðir** síðu (**Eignastýring** \> **Uppsetning** \> **Eignir** \> **Gerðir eigna** \> **Eignamælingar**).
> - Reitirnir í **Upplýsingar** kafla á flýtiflipanum **Almennt** sýnir fjölda starfstegunda, eignamælingar, eiginleika og svo framvegis sem eru sett upp á valda eignategund.

Venjulega eru verkbeiðnir sem eru búnar til handvirkt tengdar leiðréttandi viðhaldi, en vinnupantanir sem eru búnar til sjálfkrafa tengjast fyrirbyggjandi viðhaldi. Þegar þú býrð til verkbeiðnir handvirkt eru aðeins þær tegundir starfa sem valdar eru á flýtiflipanum **Starfagerðir** á **Gerðir eigna** síðu er hægt að nota. Samt sem áður, sjálfkrafa stofnaðar vinnupantanir geta notað allar þær tegundir starfa sem þú býrð til á **Starfagerðir** síðu (**Eignastýring** \> **Uppsetning** \> **Störf** \> **Starfagerðir**).

## <a name="create-asset-type-setup-lines"></a>Búðu til uppsetningarlínur fyrir eignategund

1. Veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Eignagerðir** \> **Uppsetning eignagerðar**. Að öðrum kosti, veldu **Eignastýring** \> **Uppsetning** \> **Eignir** \> **Gerðir eigna** \> **Gerðir eigna**, veldu eignategund og veldu síðan **Uppsetning eignagerða**.
2. Í fyrsta skipti sem þú notar **Uppsetning eigna** síðu gætirðu fundið **Stofna samsetningar** hnappur gagnlegur. Þú getur notað þennan hnapp til að búa til fljótt allar samsetningar eignalíkans á eignategund. Veldu **Stofna samsetningar**, veldu eignategundina sem á að búa til samsetningar fyrir og veldu síðan **Í lagi**.

    > [!NOTE]
    > Ef þú munt ekki nota allar samsetningar samsetningar eigna sem voru búnar til sjálfkrafa geturðu eytt uppsetningu með því að velja hana og síðan velja **Eyða**.

3. Veldu **Nýtt** til að stofna handvirkt uppsetningu eignategundar.
4. Það fer eftir því hversu sérstök uppsetning eignagerða skal vera en veldu í reitunum **Tegund eigna**, **Framleiðandi**, og **Líkan**.
5. Ef ábyrgðarsamningur tengist eignategundinni skaltu velja samninginn í **Ábyrgð seljanda** og **Ábyrgð viðskiptavina**. 
6. Á flýtiflipanum **Varahlutir**, veldu **Bæta við** til að bæta við varahlutum við valda uppsetningu eigna.
7. Til að samþykkja varahluti skaltu velja varahlutalínuna og síðan **Samþykkja**. Þú getur valið margar línur til samþykktar.
8. Til að sjá hvort varahlutir eru notaðir annars staðar í eignastýringu (til dæmis í sambandi við eignir og vinnupantanir), veldu varahlutalínuna og veldu síðan **Hlutur þar sem hann er notaður** til að opna **Hlutur þar sem hann er notaður** síðu. Til að sjá alla virka varahluti á listanum velurðu **Virkur** gátreitinn. Veldu aðeins til að sjá viðurkennda varahluti **Samþykkt** gátreitinn.
9. Á flýtiflipanum **Viðhaldsáætlanir**, veldu **Bæta við** til að bæta við viðhaldsáætlunum við valda uppsetningu eigna.
10. Til að afrita uppsetningu eigna í aðra uppsetningu er hægt að nota afritunaraðgerðina. Veldu uppsetningu eigna sem á að afrita uppsetningu á, veldu **Afrita uppsetningu**, og veldu þá gerð eigna sem á að afrita uppsetninguna frá. Stillingar hinna ýmsu valkosta ákvarða hversu miklar upplýsingar fylgja. Þegar því er lokið skaltu velja **í lagi** til að afrita uppsetninguna.

> [!NOTE]
> Ef þú ert með margar varahlutalínur og viðhaldsáætlunarlínur sem þú munt endurnýta, gerir afritunaraðgerðin kleift að setja upp gögn fljótt og auðveldlega fyrir margar uppsetningarsamsetningar eigna.

## <a name="spare-parts-on-the-asset-type-setup"></a>Varahlutir í uppsetningu eignategundarinnar

Eins og lýst var í hlutanum „Búa til uppsetningarlínur fyrir eignategund“ eru varahlutir settir upp á eignarmódelum á **Uppsetning eigna** síðu. Þess vegna, þegar þú opnar **Uppsetning eigna** síðu sérðu aðeins varahlutina sem tengjast völdum samsetningu eigna tegundar, eignaframleiðanda og eignalíkans. Til að sjá lista yfir allar varahlutaskrár skaltu opna **Auka hlutir** síðu (**Eignastýring** \> **Fyrirspurnir** \> **Varahlutir**).

Á **Varahlutir** síðu, þú getur líka búið til nýja varahluti fyrir núverandi samsetningar af eignategund, eignaframleiðanda og eignalíkani. Þú getur ákveðið hvort þú viljir búa til varahlutaskrár á **Uppsetning eigna** síðu eða **Varahlutir** síðu. The **Uppsetning eignagerðar** á síðunni er yfirlit yfir gögn um valda samsetningu eigna tegundar, eignaframleiðanda og eignamódel, en **Varahlutir** síðu veitir fullkomið yfirlit yfir allar uppsetningarlínur eignategunda. Ef **Varahlutir** síðu inniheldur margar skrár, **Uppsetning eigna** síðu gæti gefið þér betri yfirsýn.

Til að sjá hvort varahlutur á valinni línu eru notaðir annars staðar í eignastýringu (til dæmis í sambandi við eignir og vinnupantanir), veldu varahlutalínuna og veldu síðan **Hlutur þar sem hann er notaður** til að opna **Hlutur þar sem hann er notaður** síðu. 
