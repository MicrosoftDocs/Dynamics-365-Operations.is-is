---
title: Líftímastöður verkbeiðni
description: Þetta efni útskýrir hvernig á að raða líftímastöðum verkbeiðna í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderLifecycleState, EntAssetWorkOrderLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6e96f2f6b324ffe44e8684d9bd2a42fb52d0aed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430388"
---
# <a name="work-order-lifecycle-states"></a>Líftímastöður verkbeiðni


[!include [banner](../../includes/banner.md)]

 

Líftímastöður verkbeiðna skilgreina þær stöður sem verkbeiðni getur farið í gegnum. Sem dæmi má nefna **Stofnað**, **Raðað**, **Í vinnslu** og **Lokið**. Hægt er að uppfæra líftímastöður verkbeiðni handvirkt í verkbeiðni, eða þær geta verið uppfærð sjálfkrafa (til dæmis meðan á tímasetningu verkbeiðni stendur).

Líftímastöður verkbeiðna sem krafist er fyrir verkbeiðnirnar verða að vera festar við samsvarandi verkefnastig á síðunni **Verkefnisstjórnun og bókhaldsbreytur** (**Verkefnisstjórnun og bókhald** \> **Verkefnisstjórnun og bókhaldsbreytur**). Þú settir fyrst upp verkefnisstig í verkefnastjórnun og bókhaldi. Þú setur síðan upp líftímastöður verkbeiðni og líkön fyrir líftímalíkön verkbeiðni í eignastjórnun.

Eftirfarandi tafla lýsir valkostunum í hlutunum **Verkbeiðni** og **Tímasetja** á flýtiflipanum **Almennt** á síðunni **Líftímastaða verkbeiðna** (**Eignastýring** \> **Uppsetning** \> **Verkbeiðnir** \> **Líftímastöður**).

![Síðan Líftímastaða verkbeiðni](media/09-setup-for-work-orders.png)

| Heiti valkosts                   | Lýsing |
|-------------------------------|-------------|
| Í gangi                        | Stilltu þennan möguleika á **Já** ef verkbeiðnin ætti að vera virk meðan hún er í þessari líftímastöðu. |
| Bæta við línu                      | Stilltu þennan möguleika á **Já** ef hægt er að bæta við verkbeiðniverkum við verkbeiðni sem er í þessari líftímastöðu. |
| Eyða                        | Stilltu þennan möguleika á **Já** ef hægt er að eyða verkbeiðni meðan hún er í þessari líftímastöðu. |
| Eyða línu                   | Stilltu þennan möguleika á **Já** ef hægt er að eyða verkbeiðniverkum úr verkbeiðni sem er í þessari líftímastöðu. |
| Leyfa áætlanagerð              | Stilltu þennan möguleika á **Já** ef hægt er að tímastilla verkbeiðni meðan hún er í þessari líftímastöðu. |
| Stilla raunverulegt upphaf              | Stilltu þennan möguleika á **Já** ef notandi ætti að vera beðinn um að velja raunverulegan upphafsdag og tíma fyrir verkbeiðni þegar hann er uppfærður í þessa líftímastöðu. |
| Stilla raunveruleg lok                | Stilltu þennan möguleika á **Já** ef notandi ætti að vera beðinn um að velja raunverulegan lokadag og -tíma fyrir verkbeiðni þegar hann er uppfærður í þessa líftímastöðu. |
| Bóka færslubækur                 | Stilltu þennan möguleika á **Já** ef hægt er að bæta við færslubækur verkbeiðna skulu bókaðar sjálfvirkt þegar verkbeiðni er uppfærð í þessa líftímastöðu. Ef villa kemur upp við bókun færslubókar birtast skilaboð og hætt er við uppfærslu á líftímastöðu verkbeiðni. Til að skoða færslubókarlínurnar fyrir verkbeiðnina velurðu **Eignastjórnun** \> **Sameiginlegt** \> **Verkbeiðnir** \> **Allar verkbeiðnir**, **Virkar verkbeiðnir** eða **Mínar virku verkbeiðnir**, veldu verkbeiðnina af listanum og veldu síðan **Færslubækur**. Þessi uppsetning á sjálfvirkri færslubókarbókun verkbeiðni í tiltekinni líftímastöðu er sú saman og þegar þú velur **Bóka færslubækur** á síðunni **Færslubækur verkbeiðna**.<p>**Athugasemd:** Ef þú stillir þennan möguleika á **Já** eru færslubækur sjálfkrafa settar upp ef ekkert samþykktarverkflæði hefur verið sett upp. Ef fyrirtækið notar samþykktaruppsetningu færslubóka sem er skilgreind á síðunni **Færslubókarsamþykkt** (**Verkefnisstjórnun og bókhald** \> **Uppsetning** \> **Færslubækur** \> **Færslubókarsamþykkt**), verður stjórnandi eða starfsmaður að staðfesta og bóka skráningar á notkun.</p> |
| Vinna úr viðhaldsgátlista | Stilltu þennan valkost á **Já** ef allir viðhengdir viðhaldsgátlistar skulu unnir þegar verkbeiðni er uppfærð í þessa líftímastöðu. Sem hluti af þessari vinnslu eru allar teljaraskráningar sem gerðar voru á viðhaldsgátlista bókaðar og niðurstöður alls viðhaldsgátlistans eru metnar. Viðhaldsgátlistalínur sem hafa niðurstöðurnar **Stóðst** og **Tókst ekki** og ef að minnsta kosti ein lína tekst ekki er allur viðhaldsgátlistinn merktur sem **Tókst ekki** í eignastýringu. |
| Tilbúið                         | Stilltu þennan valkost á **Já** ef röðunarstaða verkbeiðniverks fyrir öll verkbeiðniverk sem eru stofnuð í verkbeiðni skulu sjálfkrafa vera uppfærð í **Tilbúið** þegar verkbeiðnin er uppfærð í þessa líftímastöðu. |
| Ræsa                         | Stilltu þennan valkost á **Já** ef röðunarstaða verkbeiðniverks fyrir öll verkbeiðniverk sem eru stofnuð í verkbeiðni skulu sjálfkrafa vera uppfærð í **Hófst** þegar verkbeiðnin er uppfærð í þessa líftímastöðu. |
| Ljúk.                           | Stilltu þennan valkost á **Já** ef röðunarstaða verkbeiðniverks fyrir öll verkbeiðniverk sem eru stofnuð í verkbeiðni skulu sjálfkrafa vera uppfærð í **Lokið** þegar verkbeiðnin er uppfærð í þessa líftímastöðu. |
| Eyða áætlunarlínum         | Stilltu þennan valkost á **Já** ef röðun á öllum verkbeiðniverkum sem er stofnuð í verkbeiðni sem hefur þegar verið raðað skal sjálfkrafa vera uppfærð í Tilbúið þegar verkbeiðnin er uppfærð í þessa líftímastöðu. Með öðrum orðum, frátekinni afkastagetu á eigninni, tengdum viðhaldsstarfsmanni og tengdum verkfærum verður eytt. Til dæmis stillir þú þennan valkost á **Já** á líftímastöðu verkbeiðni sem er nefnd **Áætlað**. Þegar verkbeiðni er færð til baka í þessa líftímastöðu þar sem endurröðunar er krafist er hægt að eyða endurröðun á þeirri verkbeiðni. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Settu upp verkefnisstig og líftímastöður verkbeiðna

1. Veldu **Verkefnastjórnun og bókhald** \> **Uppsetning** \> **Verkefnastjórnun og bókhaldsfæribreytur**.
2. Á flipanum **Verkstigi**, fyrir hvert stig sem þú vilt nota skaltu velja gátreitinn fyrir hverja gerð verkefna sem þarf til fyrir verkbeiðnirnar. Verkgerðirnar skilgreina reglur um fjárhagsleg verk sem leyfð eru. Dæmi um fjárhagsleg verk eru stofnun á spá, stofnun á mati og stofnun á upphafsstöðum.

    > [!IMPORTANT]
    > Ef verkstig er ekki valið fyrir verkgerð, en verkstigið er notað fyrir líftímastöðu verkbeiðnar verða verkbeiðnaverkin ekki uppfærð á viðeigandi hátt.

3. Lokaðu síðunni **Verkefnastjórnun og bókhaldsfæribreytur**.
4. Veldu **Eignastýring** \> **Uppsetning** \> **Verkbeiðnir** \> **Líftímastöður**.
5. Veldu **Nýtt** til að stofna líftímastöðu verkbeiðni.
6. Í reitinn **Líftímastöðu** slærðu inn kenni líftímastöðunnar.
7. Færið inn lýsandi nafn í reitinn **Heiti**.

    Á flýtiflipanum **Upplýsingar** sýnir reiturinn **Líftímalíkön** fjölda líftímalíkana verkbeiðna sem nota þessa líftímastöðu.

8. Á flýtiflipanum **Almennt**, í hlutanum **Verkbeiðni**, velurðu aðgerðir sem skulu vera tiltækar fyrir þessa líftímastöðu með því að stilla viðeigandi valkosti á **Já**. Lýsingar á valkostunum er að finna í töflunni fyrr í þessu efnisatriði.
9. Í hlutanum **Verk**, í reitnum **Stig** veldu verkefnastigið sem ætti að tengjast þessari líftímastöðu.
10. Í hlutanum **Verk** stillirðu valkostinn **Lokunarverkþætti** á **Já** ef verkþáttum sem tengjast hverju verkbeiðniverki skal sjálfkrafa lokað þegar verkbeiðnin er í þessari líftímastöðu.

    > [!NOTE]
    > Til að finna fjölda verkþátta sem tengjast verkbeiðni verki velurðu **Eignastjórnun** \> **Sameiginlegt** \> **Verkbeiðnir** \> **Allar verkbeiðnir**, **Virkar verkbeiðnir**, eða **Mínar virku verkbeiðnir**. Opnaðu verkbeiðnina og veldu síðan verkbeiðniverkið. Verkþáttanúmerið er sýnt í reitnum **Verkþáttanúmer** í hlutanum **Verk** á flipanum **Almennt** á flýtiflipanum **Línuupplýsingar**.

11. Í hlutanum **Spá** stillirðu valkostinn **Afrita tímaspá**, **Afrita vöruspá**, og/eða **Afrita kostnaðarspá** á **Já** ef sjálfkrafa ætti að afrita spár verkbeiðniverka í færslubækur verkbeiðna þegar verkbeiðnin er í þessari líftímastöðu.
12. Í hlutanum **Tímastilla** stillirðu einn af valkostunum á **Já** ef uppfæra skal röðunarstöðu fyrir verkbeiðniverk þegar verkbeiðnin er í þessari líftímastöðu. Fyrir lýsingar á valkostunum **Tilbúið**, **Hefja**, **Ljúka** og **Eyða röðunarlínum** skal sjá töfluna fyrr í þessu efni.

    > [!NOTE]
    > Til að skoða röðunarlínur sem tengjast verkbeiðniverkum velurðu **Eignastjórnun** \> **Sameiginlegt** \> **Verkbeiðnir** \> **Allar verkbeiðnir**, **Virkar verkbeiðnir**, eða **Mínar virku verkbeiðnir**. Opnaðu verkbeiðnina, veldu verkbeiðniverkið á flýtiflipanum **Verkbeiðniverk** og skoðaðu tengdar upplýsingar á flýtiflipanum **Línuupplýsingar**. Reiturinn **Staða** á flipanum **Tímasetja** sýnir stöðu verkbeiðniverksins. Reitinn **Stöðu** má stilla á eftirfarandi gildi: **Raðað**, **Tilbúið**, **Hafið**, **Stöðvað**, og **Lokið**.

13. Í hlutanum **Viðhaldsbeiðnir**, í reitnum **Líftímastöðu** velurðu líftímasöðu viðhaldsbeiðni sem tengdar viðhaldsbeiðnir skulu uppfærðar í. Þessi uppfærsla á sér stað sjálfkrafa. Hana er aðeins hægt að gera ef líftímastaða viðhaldsbeiðni er valin í líftímalíkani viðhaldsbeiðni sem er notað fyrir viðhaldsbeiðnina.
14. Í hlutanum **Eign** stillirðu valkostinn **Uppfæra uppskrift eignar** á **Já** ef allir hlutir sem eru notaðir í vinnupöntun ættu sjálfkrafa að vera uppfærðir á síðunni **Uppskrift eignar** þegar verkbeiðnin er uppfærð í þessa líftímastöðu. Þessi stilling gæti skipt máli ef til dæmis líftímastaða verkbeiðni skilgreinir verkbeiðnina sem lokið eða lokið.
15. Í hlutanum **Verkbeiðnisafn** stillirðu valkostinn **Eyða safntilvísun** á **Já** ef verkbeiðnum sem eru í þessari líftímastöðu skal sjálfkrafa eytt úr verkbeiðnisöfnum.
16. Á flýtiflipanum **Staðfesta** velurðu staðfestingargerðirnar sem skulu virkjaðar í þessari líftímastöðu með því að stilla viðeigandi valkosti á **Já**. Síðan, í reitnum **Gerð** fyrir hverja villuleitargerð sem þú velur, velurðu þá gerð skilaboða sem skal sýna ef lögboðnir reitir sem tengjast villuleitargerðinni hafa ekki verið staðfestir. Ef þú velur **Villa** er hætt við uppfærslu á líftímastöðu verkbeiðni þangað til að tengdir reitir hafa verið uppfærðir á verkbeiðninni.

    - Valkostirnir **Niðurtími vegna viðhalds**, **Viðhaldsgátlisti**, **Bilunareinkenni**, **Bilunarorsök**, og **Bilunarúrræði** tengjast valkostunum í hlutanum **Skylda** á síðunni **Verkbeiðnigerðir** (**Eignastjórnun** \> **Uppsetning** \> **Verkbeiðnir** \> **Verkbeiðnigerðir**). Til að virkja þessar staðfestingar verður einnig að stilla tengda valkosti **Já** á verkbeiðnigerðinni sem er notuð fyrir verkbeiðnina.
    - Ef valkosturinn **Viðhaldsgátlisti** er stilltur á **Já** fyrir líftímastöðuna sem verkbeiðni er uppfærð í er staðfesting gerð til að sannreyna að viðhaldsgátlistalínur sem eru merktar sem **Skylda** hafa verið skráðar sem hvorki **Villuleitað** né **Á ekki við**. Ef hvorug þessara skráninga hefur verið gerð á lögboðnum línum birtast upplýsinga-, villu- eða viðvörunarskilaboð þegar verkbeiðnin er uppfærð í þessa líftímastöðu.
    - Ef valkosturinn **Ráðstafaður kostnaður** er stilltur á **Já** fyrir líftímastöðuna sem verkbeiðni er uppfærð í er heildarfjárhæð ráðstafaðs kostnaðar (það er, heildarupphæð kostnaðar sem lögaðilinn hefur skuldbundið sig til að greiða) er reiknuð fyrir hvert verkbeiðniverk. Skeyti eru sýnd ef upphæð ráðstafaðs kostnaðar er hærri en 0 (núll). Þú velur þær tegundir kostnaðarráðstafana sem fylgja með á flýtiflipanum **Kostnaðarráðstafanir** á flipanum **Kostnaðarstýring** á síðunni **Verkefnisstjórnun og bókhaldsbreytur** (**Verkefnisstjórnun og bókhald** \> **Uppsetning** \> **Verkefnisstjórnun og bókhaldsbreytur**).
    - Ef valkosturinn **Niðurtími vegna viðhalds** er stilltur á **Já** fyrir líftímastöðuna sem verkbeiðni er uppfærð í er villuleitun niðurtíma vegna viðhalds gerð á eigninni sem er tengd verkbeiðninni. Ef skráning niðurtíma vegna viðhalds hefur verið gerð en það er engin skráning **Lokið** eru skilaboð sýnd þegar verkbeiðnin er uppfærð í þessa líftímastöðu.
    - Ef venjuleg verkuppsetning inniheldur ekki öll stigin sem þú þarfnast fyrir uppstillingu á eignastjórnun geturðu sett upp notendaskilgreind verkefnastig á flipanum **Verkstig** á síðunni **Verkefnisstjórnun og bókhaldsfæribreytur**. Eftirfarandi mynd sýnir flipann **Verkstig** á síðunni **Verkefnisstjórnun og bókhaldsfæribreytur**.

    ![Síðan Setja upp verkstig fyrir ýmsar verkgerðir](media/10-setup-for-work-orders.png)

> [!NOTE]
> Ef líftímastaðan sem þú uppfærir verkbeiðni í er óvirk, er færslubókum sem tengjast verkbeiðninni en hafa ekki enn verið bókaðar sjálfkrafa eytt. Þessi hegðun hjálpar til við að tryggja sjálfvirka hreinsun ónotaðra gagna. (Líftímastaða er óvirk ef valkosturinn **Virkt** fyrir hana stilltur á **Nei** á flýtiflipanum **Almennt** á síðunni **Líftímastaða verkbeiðni**.)
>
> Hinsvegar, ef þú stillir verkbeiðni þannig að hún sé óvirk, er færslubókum sem tengjast verkbeiðninni en hafa ekki enn verið bókaðar **ekki** sjálfkrafa eytt. (Til að gera verkbeiðni óvirka handvirkt veluðu **Eignastjórnun** \> **Sameiginlegt** \> **Verkbeiðnir** \> **Allar verkbeiðnir** eða **Virkar verkbeiðnir**. Opnaðu verkbeiðnina og skiptu yfir í sýnina **Haus**. Á flýtiflipanum **Almennt** velurðu **Breyta** og stillir síðan valkostinn **Virkt** á **Nei** .)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Vensl á milli og líftímalíkana verkbeiðna, verkbeiðnigerða og líftímastaða verkbeiðna.

Líftímalíkön vísa til verkflæða og líftímastöður eru valdar í líftímalíkani í raðbundinni röð. Líftímalíkön eru sett upp eftir tegundum verkbeiðna. Gerðir verkbeiðna ákvarða stærð eða umfang verkflæða og vinnuferla. Til dæmis, gæti **Viðhald** sem er venjuleg gerð verkbeiðni tengst líftímalíkani verkbeiðni sem hefur margar líftímastöður. Aftur á móti gætirðu haft verkbeiðnigerðina **Leiðrétting** sem er notuð fyrir verkbeiðnir sem ekki hafa verið áætlaðar, eða fyrir verkbeiðnir þar sem verkinu er lokið áður en verkbeiðnin er gerð vegna brýnna aðstæðna. Þessi tegund verkbeiðna kann að tengjast líftímalíkani verkbeiðni sem hefur aðeins nokkrar líftímastöður.

Ástæðan fyrir notkun á gerðum er að þegar gerð er til dæmis skilgreind á verðbeiðni eða eign eru tengdir vinnuferlar (líftímastöður) sjálfkrafa skilgreindir. Nánari upplýsingar um hvernig setja skal upp gerðir verkbeiðna er að finna í [Gerðir verkbeiðna](../setup-for-work-orders/work-order-types.md).

> [!NOTE]
> Líftímastöður, líftímalíkön og gerðir eiga við um virkar staðsetningar, eignir og viðhaldsbeiðnir, auk verkbeiðna.

Eftirfarandi mynd sýnir tengsl milli verkbeiðnigerða, líftímalíkana og líftímastaða.

![Síðan Verkbeiðnigerð samanborið við síðuna Líftímalíkön verkbeiðna](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Líftímalíkön verkbeiðni

Þegar þú hefur stofnað líftímastöður verkbeiðni sem nauðsynlegar eru fyrir verkbeiðnir þínar er hægt að skipta þeim í líftímalíkön verkeiðna. Að lágmarki ættir þú að búa til eitt staðlað líftímalíkan.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Verkbeiðnir** \> **Líftímalíkön**.
2. Veldu **Nýtt** til að stofna líftímalíkön verkbeiðni.
3. Í **Líftímalíkan** reitinn, sláðu inn kenni líftímalíkansins.
4. Færið inn lýsandi nafn í reitinn **Heiti**.

    Á flýtiflipanum **Upplýsingar** sýnir reiturinn **Líftímastöður** fjölda líftímastaða eigna sem eru valin í þessu líftímalíkani eigna. Reiturinn **Gerðir verkbeiðna** sýnir fjölda gerða verkbeiðna sem nota líftímalíkanið.

5. Á flýtiflipanum **Líftímastöður** velurðu þær líftímastöður sem ætti að vera með í líftímalíkani:

    - Til að hafa líftímastöðu með fyrir líftímalíkanið skaltu velja það í **Eftirstandandi líftímastöður** kafla og veldu síðan hægri örvarhnappinn ![Hægri ör](media/12-setup-for-work-orders.png) til að færa það til **Valdar líftímastöður**.
    - Til að hafa allar tiltækar líftímastöður með fyrir líftímalíkanið velurðu hnappinn **Velja öll tiltæk stig** ![Velja öll tiltæk stig](media/13-setup-for-work-orders.png). Allar líftímastöður eru fluttar í hlutann **Valdar líftímastöður**.
    - Til að fjarlægja líftímastöðu úr líftímalíkani skaltu velja það í **Valdar líftímastöður** kafla og veldu síðan vinstri örvarhnappinn ![Vinstri ör](media/14-setup-for-work-orders.png) til að færa það til **Eftirstandandi líftímastöður**.

6. Veldu **Uppfærslur á líftímastöðu** til að skilgreina líftímastöður sem geta fylgt valinni líftímastöðu.
7. Á flýtiflipanum **Uppfærslur**, í reitnum **Röðuð staða**, velurðu líftímastöðu sem alltaf ætti að vera valin fyrir verkbeiðnina sem þú hefur lokið röðun verkbeiðna fyrir, óháð fyrri líftímastöðu verkbeiðni.
8. Í reitinn **Óröðuð líftímastaða** velurðu líftímastöðu sem alltaf ætti að vera valin fyrir verkbeiðni ef tímasetningu verkbeiðni er eytt.
9. Vistaðu líftímalíkan verkbeiðni.

![Síðan Líftímalíkön verkbeiðna](media/15-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]