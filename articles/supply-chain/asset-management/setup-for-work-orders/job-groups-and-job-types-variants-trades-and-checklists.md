---
title: Flokkar viðhaldsverkgerðar og viðhaldsverkgerðir, afbrigði viðhaldsverkgerðar, viðskipti viðhaldsvinnslu og viðhaldsgátlistar
description: Þetta efni lýsir tegundaflokkum viðhaldsverka og gerðum viðhaldsverka, afbrigðum viðhaldsverkgerða, viðskipti viðhaldsvinnslu og viðhaldsgátlistum í Eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetJobTypeDefaultForecast, EntAssetJobTrade, EntAssetJobTypeDefaultCopy, EntAssetChecklistVariableValueLookup, EntAssetChecklistTemplateCreate, EntAssetJobVariant, EntAssetJobTypeDefaultReference, EntAssetJobTypeDefaultChecklist, EntAssetJobTypeDefault, EntAssetJobType, EntAssetJobTypeDefaultChecklistCopy, EntAssetChecklistTemplate, EntAssetJobTypeDefaultDescription, EntAssetJobTypeLookup, EntAssetJobTypeDefaultToolCopy, EntAssetJobTypePreviewPart, EntAssetJobTypeDefaultTool, EntAssetJobTypeDefaultForecastCopy, EntAssetChecklistTemplateLookup, EntAssetJobGroup, EntAssetChecklistVariable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8bf7c53a6150a2beeca5c6e9b5ab4ea98584158d
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889076"
---
# <a name="maintenance-job-type-categories-and-maintenance-job-types-maintenance-job-type-variants-maintenance-job-trades-and-maintenance-checklists"></a>Flokkar viðhaldsverkgerðar og viðhaldsverkgerðir, afbrigði viðhaldsverkgerðar, viðskipti viðhaldsvinnslu og viðhaldsgátlistar

[!include [banner](../../includes/banner.md)]

 

Eignategund er fest við hverja eign. Eignategundir skilgreina gerðir viðhaldsstarfa (og þar með viðhaldsstörf) sem hægt er að framkvæma á eignum. Þegar þú stofnar verkbeiðni verður að velja gerð viðhaldsverks. Þú getur aðeins valið gerðir viðhaldsverka sem eru tengdar uppsetningunni á eignategundinni sem er notuð fyrir eignina.

Fyrir myndrænt yfirlit yfir eignir og gerðir viðhaldsverka og tengsl þeirra við verkbeiðnir skal sjá [Virkar staðsetningar og eignir](../overview/functional-locations-and-objects.md).

Hægt er að setja upp tegundaafbrigði viðhaldsverka á viðhaldsstegundargerð. Tegundaafbrigði viðhaldsverka skilgreina afbrigði af starfsgerð, svo sem stærðir (lítið, meðalstórt eða stórt), tímabil (vikulegt, tveggja vikna, mánaðarlegt eða þriggja mánaða) og stillingar (lágur staðall, sveigjanlegt eða mikil afköst).

Viðskipti viðhaldsverka veita upplýsingar um fagviðskipti, svo sem vél-, rafmagns- og vökvaviðskipti. Hægt er að setja upp hæfniskröfur í viðskiptum með viðhaldsverk. Hægt er að nota öll viðskipti með viðhaldsverk í tengslum við allar gerðir viðhaldsverka. Val á tegundaafbrigði af viðhaldsverkum og/eða viðskiptum með viðhaldsverk í verkbeiðni er valfrjálst.

Fyrir hverja gerð viðhaldsverks er hægt að búa til afbrigði af tegundauppsetningu viðhaldsverksins. Til dæmis ef þú ert með tegund viðhaldsverks sem er nefnd **Þjónusta** geturðu búið til eftirfarandi afbrigði fyrir þá tegund viðhaldsverks: **Vörubílar 30.000 km**, **Bílar 30.000 km** og **Sendiferðabílar 30.000 km**.

Tegundaflokkar viðhaldsverka eru notaðir til að safna hópi tegunda viðhaldsverka í yfirlitsskyni. Dæmi um tegundaflokka viðhaldsverka geta verið **Kvörðun**, **Skoðun**, **Yfirferð** og **Tæki**.

Sniðmát viðhaldsgátlista og færibreytur viðhaldsgátlista eru notuð til að setja upp viðhaldsgátlista. Viðhaldsgátlistar eru settir upp á tegundum viðhaldsverka og notaðir verkbeiðnir.

Fyrst seturðu upp nauðsynlega tegundaflokka viðhaldsverka, tegundaafbrigði viðhaldsverka og viðskipti viðhaldsvinnslu. Síðan býrðu til tegundir viðhaldsstarfa. Að lokum, á síðunni **Sjálfgefin tegund viðhaldsverka** býrðu til öll afbrigði af tegundum viðhaldsverka sem þarf fyrir búnaðinn. Á þeirri síðu geturðu einnig sett upp spár, viðhaldslista og verkfæri fyrir blöndu af tegundum viðhaldsverka.

> [!NOTE]
> Gerð viðhaldsverkefna má aðeins vera tengd einum tegundaflokki viðhaldsverkefna.

## <a name="create-a-maintenance-job-type-category"></a>Búðu til tegundaflokk viðhaldsverks

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Vinnslur** \> **Tegundaflokkar viðhaldsverka**.
2. Veljið **Nýtt**.
3. Í reitnum **Tegundaflokkur viðhaldsverka** skaltu slá inn auðkenni fyrir tegundaflokk viðhaldsverka.
4. Færið inn lýsandi nafn í reitinn **Heiti**.

    Eftir að þú hefur tengt tegundaflokka viðhaldsverka við gerðir viðhaldsverka sýnir reiturinn **Vinnslugerðir** fjölda tegunda viðhaldsverka sem tengjast þessum tegundaflokkum viðhaldsverka.

![Síðan Tegundaflokkar viðhaldsverka](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Búðu til tegundaafbrigði viðhaldsverks

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Vinnslur** \> **Tegundaafbrigði viðhaldsverka**.
2. Veljið **Nýtt**.
3. Í reitnum **Tegundaafbrigði viðhaldsverka** skaltu slá inn auðkenni fyrir tegundaafbrigði viðhaldsverka.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Á flýtiflipanum **Tegundir viðhaldverka** skaltu velja **Bæta við** til að bæta við gerð viðhaldsverks.
6. Í reitnum **Tegund viðhaldsverka** skaltu velja gerð viðhaldsverka.
7. Endurtaktu skref 5 til 6 til að bæta við fleiri tegundum viðhaldsverka við tegundaafbrigði viðhaldsverka.

    Á flýtiflipanum **Upplýsingar** sýnir reiturinn **Vinnslugerðir** fjölda tegunda viðhaldsverka sem hefur verið bætt við þetta tegundafbrigði viðhaldsverka.

![Síðan Tegundaafbrigði viðhaldsverka](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Stofnaðu viðskipti viðhaldsverks

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Vinnslur** \> **Viðskipti viðhaldsverka**.
2. Veljið **Nýtt**.
3. Í reitinn **Viðskipti** skal slá inn auðkenni fyrir viðskipti með viðhaldsverk.
4. Í reitnum **Lýsing** skal færa inn lýsingu.
5. Á flýtiflipanum **Færni** velurðu **Bæta við** til að bæta við nýrri færni sem ætti að tengjast viðskiptum með viðhaldsverk.
6. Í reitnum **Færni** skal velja færni.
7. Í reitnum **Stig** skal velja stig.
8. Endurtaktu skref 5 til 7 til að bæta við færni í viðskiptum með viðhaldsverk.

    Á flýtiflipanum **Upplýsingar** sýnir reiturinn **Færni** fjölda færni sem hefur verið bætt við þessi viðskipti með viðhaldsverk.

9. Á flýtiflipanum **Vottorð** velurðu **Bæta við** til að bæta við skírteini við viðskipti með viðhaldsverk.
10. Í reitnum **Gerð vottorðs** skal velja vottorðið.
11. Endurtaktu skref 9 til 10 til að bæta við fleiri vottorðum við viðskipti með viðhaldsverk.

    Á flýtiflipanum **Upplýsingar** sýnir reiturinn **Vottorð** fjölda vottorða sem hefur verið bætt við þessi viðskipti með viðhaldsverk.

![Síðan Viðskipti viðhaldsverka](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Búðu til breytu fyrir viðhaldsgátlista

Þegar þú býrð til viðhaldsgátlistalínur í sjálfgefinni gerð viðhaldsverks verður þú að velja gerð viðhaldsgátlista. **Breyta** er ein tegund viðhaldsgátlista. Hún er notuð til að skilgreina mögulega útkomu í sviðinu á viðhaldsgátlistalínu sem tengist verkbeiðnilínu. Með breytu er hægt að búa til safn af fyrirframskilgreindum niðurstöðum án þess að þurfa að gera nákvæmar mælingar.

**Dæmi 1:** Þú getur mælt olíustig með því að skilgreina þrjú gildi: **Stig of hátt**, **Stig of lágt** og **Stig innan marka**. Fyrir hvert gildi skilgreinirðu hvort niðurstaðan sé **Staðið**, **Fall** eða **Ekkert**.

**Dæmi 2:** Þú gerir sjónræna skoðun á búnaði til að meta slit.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Viðhaldsgátlistar** \> **Breytur viðhaldsgátlista**.
2. Veljið **Nýtt**.
3. Í reitinn **Breyta** skal slá inn auðkenni fyrir breytu viðhaldsgátlista.
4. Færið inn lýsandi nafn í reitinn **Heiti**.
5. Á flýtiflipanum **Almennt** velurðu **Bæta við** til að bæta við línu fyrir breytu.

    Raðlínunúmer er sjálfvirkt sett inn í reitinn **Línunúmer**. Eftir að þú hefur bætt öllum línunum við geturðu breytt línunúmerum eins og þú þarft. Þegar þú velur línu og ýttu síðan á lykilinn **Ör niður** er næsta númer í röðinni sjálfkrafa slegið inn í næstu línu.

6. Í reitnum **Gildi** skal slá inn gildislýsingu.
7. Í reitnum **Niðurstaða** skal velja niðurstöðu fyrir línuna.

![Síðan Breytur viðhaldsgátlista](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Búðu til sniðmát fyrir viðhaldsgátlista

Sniðmát viðhaldsgátlista er hægt að nota sem sameiginlegan hóp verka sem starfskraftur þarf að framkvæma til að ljúka verkbeiðni rétt. Vísað er til sniðmátanna í viðhaldsgátlistalínum við sjálfgefna gerð viðhaldsverksins. Hægt er að vísa í sniðmát yfir margar sjálfgefnar tegundalínur viðhaldsverkefna. Þess vegna getur þú auðveldlega endurnýtt safn af sameiginlegum verkmm viðhaldsgátlista. Dæmi um sniðmát viðhaldsgátlista innihalda almennar öryggisleiðbeiningar og lista yfir hluti og aðstæður sem þarf að athuga á ákveðinni dælu eða svipuðum gerðum af færibandi.

1. Veldu **Eignastýring** \> **Uppsetning** \> **Viðhaldsgátlistar** \> **Sniðmát viðhaldsgátlista**.
2. Veljið **Nýtt**.

    Auðkenni sniðmáts er sjálfkrafa slegið inn í reitinn **Sniðmát viðhaldsgátlista**.

3. Í reitinn **Heiti** skal færa inn heiti fyrir sniðmát viðhaldsgátlista.
4. Á flýtiflipnum **Viðhaldsgátlistalínur** velurðu **Bæta við** til að bæta við sniðmátalínu.

    Raðlínunúmer er sjálfvirkt sett inn í reitinn **Línunúmer**. Eftir að þú hefur bætt öllum línunum við geturðu breytt línunúmerum eins og þú þarft. Þegar þú velur línu og ýttu síðan á lykilinn **Ör niður** er næsta númer í röðinni sjálfkrafa slegið inn í næstu línu.

5. Í reitnum **Gerð** velurðu gerð fyrir viðhaldsgátlistalínuna. Fyrir hverja gerð viðhaldsgátlista sýnir flýtiflipinn **Línuupplýsingar** tengda reiti. Eftirtalin gildi eru tiltæk:

    - **Texti** - Línan er með texta sem lýsir hvað á að gera. Notaðu þessa gerð viðhaldsgátlista ef þú vilt að starfsmaður athugi eða skoði eitthvað en þú býst ekki við ákveðinni (mælanlegri) niðurstöðu. Eftir að þú hefur valið þessa tegund skaltu slá inn nafn eða fyrirsögn í reitinn **Heiti**. Í reitinn **Leiðbeiningar** skal slá inn lýsingu á því sem þarf að gera. Ef skrefið er skylda fyrir viðhaldsgátlistann skaltu stilla valkostinn **Skylda** á **Já**.
    - **Haus** - Línan er notuð sem fyrirsögn til að flokka viðhaldsgátlistalínurnar sem birtast fyrir neðan hana. Þessi tegund er gagnleg ef þú ert með nokkrar viðhaldsgátlistalínur sem hægt er að skipta í ákveðin svæði. Hausar veita yfirlit fyrir starfskraftinn sem mun fylla út viðhaldsgátlista yfir viðhald sem hefur margar línur viðhaldsgátlista. Eftir að þú hefur valið þessa tegund skaltu slá inn lýsandi heiti í reitinn **Heiti**.
    - **Sniðmát** - Línan er notuð til að vísa í fyrirliggjandi sniðmát. Eftir að þú hefur valið þessa tegund skaltu slá inn heiti á sniðmátinu í reitinn **Heiti**. Í reitnum **Sniðmát** velurðu sniðmátið.
    - **Breyta** - Línan er notuð til að skilgreina hugsanlega niðurstöðu á svið. Nánari upplýsingar um hvernig á að setja upp breytur viðhaldsgátlista er að finna í kaflanum [Stofna breytu fyrir viðhaldsgátlista](#create-a-maintenance-checklist-variable). Eftir að þú hefur valið þessa tegund skaltu slá inn lýsandi heiti á breytunni í reitinn **Heiti**. Í reitnum **Breyta** skal velja breytuna. Í reitinn **Leiðbeiningar** skal slá inn lýsingu á því sem þarf að gera. Ef skrefið er skylda fyrir viðhaldsgátlistann skaltu stilla valkostinn **Skylda** á **Já**.
    - **Mæling** - Línan er notuð til að skrá ákveðna mælingu. Þú getur sett upp mælinguna sem ætti að tengjast fyrirframskilgreindum teljara. Eftir að þú hefur valið þessa tegund skaltu slá inn heiti á sniðmátinu í reitinn **Heiti**. Ef þetta skref er skylda fyrir viðhaldsgátlistann skaltu stilla valkostinn **Skylda** á **Já**. Ef þú vilt nota mælilínuna sem gagnaskráningu skaltu velja teljarann í reitnum **Teljari**. Tengdi reiturinn **Eining** er sjálfkrafa uppfærður. Ef þú hefur valið teljara skaltu velja uppfærsluaðferðina í reitnum **Gildi**. Í reitunum **Lágm.gildi** og **Hám.gildi** skal slá inn leyfilegt gildissvið. Í reitinn **Leiðbeiningar** skal slá inn lýsingu á því sem þarf að gera.

        > [!NOTE]
        > Allir línur af gerðinni **Mæling** sem eru ekki með teljarauppsetningu eru meðhöndlaðar sem sjálfstæð mælingaskráning sem engin sjálfvirk eftirfylgni er með í eignastjórnun. Sömuleiðis, ef valin teljarategund er ekki til staðar á eigninni sem er tengd verkbeiðninni, er viðhaldsgátlistaverkið meðhöndlað sem sjálfstæð mæling. Hægt er að breyta teljaragildinu mörgum sinnum. Það er ekki sent fyrr en [líftímastöðu verkbeiðni](work-order-lifecycle-states.md) er breytt í stöðu þar sem valkosturinn **Vinnsla viðhaldsgátlista** er stilltur á **Já**.

    Á flýtiflipanum **Upplýsingar** sýnir reiturinn **Athuganir** heildarfjölda gátlistalína í sniðmátinu þínu. Þetta númer inniheldur ívafðar línur í öllum fyrirliggjandi sniðmátum sem þú hefur vísað í í sniðmátinu.

![Síðan Sniðmát viðhaldsgátlista](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Stofnaðu gerð viðhaldsverks

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Vinnslur** \> **Gerðir viðhaldsverka**.
2. Veljið **Nýtt**.
3. Í reitnum **Gerð viðhaldsverks** skal slá inn auðkenni fyrir gerð viðhaldsverks.
4. Færið inn lýsandi nafn í reitinn **Heiti**.

    Flýtiflipinn **Upplýsingar** sýnir yfirlit yfir fjölda afbrigða af viðhaldsverkum, færni, vottorða, verka sem heppnast og eignategunda sem eru búnar til á þessari gerð viðhaldsverka. Reiturinn **Uppsetningarlínur** sýnir fjölda sjálfgefinna lína af gerð viðhaldsverka sem settar hafa verið upp á þessari gerð viðhaldsverka. Reiturinn **Eignir** sýnir fjölda virkra eigna sem eru að nota þessa tegund viðhaldsverka.

5. Á flýtiflipanum **Almennt** í reitnum **Tegundaflokkur viðhaldsverka** skaltu velja auðkenni fyrir tegundaflokk viðhaldsverka.
6. Stilltu valkostinn **Aðgerðir niðurtíma vegna viðhalds** á **Já** ef gerð viðhaldsverksins krefst viðhaldsstöðvunar á búnaði áður en hægt er að vinna verkið.
7. Á flýtiflipanum **Lýsing** skaltu slá inn lýsingu á gerð viðhaldsverka.
8. Á flýtiflipanum **Tegundaafbrigði viðhaldsverka** er hægt að bæta við afbrigðum fyrir tegund viðhaldsverka.
9. Á flýtiflipunum **Nauðsynleg færni** og **Nauðsynleg vottorð** geturðu bætt við kröfur um færni og vottorð við gerð viðhaldsverks.
10. Ef tiltekin gerð viðhaldsverks verður að vera framkvæmd næst skal bæta henni við á flýtiflipanu **Verk sem ná árangri**. Þú getur einnig sett upp afbrigði af gerð viðhaldsverka og viðskipti sem tengjast gerð viðhaldsverksins. Ef verk sem ná árangri á að hefjast ákveðnum dagafjölda fyrir eða eftir að verkið sem notar þessa gerð viðhaldsverkefnis er hafið skaltu slá inn fjölda daga í reitinn **Seinkun í dögum**. Jákvæðar tölur tákna daga eftir upphaf tengdra verka og neikvæðar tölur tákna daga fyrir áætlað upphaf tengds verks. Til dæmis ef þú slærð inn **5** mun verk sem nær árangri hefjast fimm dögum eftir upphaf verksins sem tengist gerð viðhaldsverksins. Ef þú slærð inn **-3** mun verk sem nær árangri hefjast þremur dögum á undan áætluðu upphafi verksins sem tengist gerð viðhaldsverksins.

    > [!NOTE]
    > Ef þú bætir við fleiri en einni viðhaldsverkefnalínu, gefur röð línanna til kynna röðina sem þær ættu að vera framkvæmdar í. Röðin byrjar efst á listanum.

11. Á flýtiflipanum **Gerðir eigna** geturðu bætt eignategundum við gerð viðhaldsverka.

![Síðan Gerðir viðhaldsverka](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Búðu til sjálfgefnar tegundir viðhaldsverka og tengdar spár, gátlista viðhalds, verkfæri, lýsingu og viðhengi

1. Veldu **Eignastjórnun** \> **Uppsetning** \> **Vinnslur** \> **Sjálfgefin tegund viðhaldsverka**.

    – eða –

    Veldu **Eignastjórnun** \> **Uppsetning** \> **Verk** \> **Gerðir viðhaldsverka**, veldu gerð viðhaldsverks og veldu síðan **Sjálfgefin tegund viðhaldsverka**.

2. Veljið **Nýtt**.
3. Í reitunum **Virk staðsetning**, **Gerð eignar**, **Framleiðandi**, **Tegund** og **Eign** skaltu velja viðeigandi gildi, allt eftir því hve sértæk sjálfgefin tegund viðhalds skal vera.
4. Í reitnum **Gerð viðhaldsverks** skaltu velja gerð viðhaldsverks ef hún var ekki sjálfkrafa valin.
5. Í retinum **Tegundaafbrigði viðhaldsverka** og **Viðskipti** skal velja tegundaafbrigði viðhaldsverka og viðskipti með viðhaldsverk eins og þú þarft.
6. Veldu **Spá**.
7. Á síðunni **Sjálfgefin spá um gerð viðhaldsverka** geturðu gert spár um klukkustundir, vörur og útgjöld. Á viðeigandi flipum velurðu **Bæta við** og gerir val til að stofna nauðsynlegar spár fyrir gerð viðhaldsverksins.
8. Á flipanum **Vöruspá** er hægt að velja birgðavíddir sem ætti að sýna á vörulínunni. Veldu **Birgðir** \> **Víddir**, veldu víddirnar sem á að sýna, stilltu valkostinn **Vista uppsetningu** á **Já** og veldu síðan **Í lagi**.
9. Á flipanum **Vöruspá** velurðu **Notkunarstaður vöru** til að fá yfirlit yfir hvar í eignastýringu varan í völdum línum er notuð eignastjórun, í tengslum við eignir, sjálfgefna gerð viðhaldsverka, varahluti og verkbeiðnir. 

    Flýtiflipinn **Viðhaldsspá samtals** sýnir yfirlit yfir heildarspár. Yfirlit þetta nær yfir heildarfjölda klukkustunda og spálínur sem hafa verið búnar til.

    > [!NOTE]
    > Til að afrita spáuppsetninguna úr annarri gerð viðhaldsverka skaltu velja **Afrita spá** og velja síðan gerð viðhaldsverksins sem á að afrita uppsetninguna úr.

11. Veldu **Vista** til að vista breytingarnar.
12. Lokaðu síðunni **Sjálfgefin spá um gerð viðhaldsverka** til að fara aftur á síðuna **Sjálfgefin tegund viðhaldsverka**.
13. Veldu **Viðhaldsgátlista**.
14. Á síðunni **Sjálfgefinn gátlisti fyrir gerð viðhaldsverka** er hægt að bæta línum viðhaldsgátlista við valið sjálfgildi gerðar viðhaldsverka. Á flýtiflipnum **Viðhaldsgátlistalínur** velurðu **Nýtt** til að bæta við viðhaldsgátlistalínu.

    Línunúmer eru sjálfkrafa færð inn í reitinn **Línunúmer** til að sýna röðina á viðhaldsgátlistalínunum. Þú getur breytt línunúmerum eins og þú vilt. Þegar þú hefur búið til fyrstu viðhaldsgátlistalínuna skaltu velja línuna og ýta síðan á lykilinn **Ör niður** til að bæta við línu fyrir neðan það. Einnig er hægt að velja viðhaldsgátlistalínu og síðan velja **Nýtt**. Í þessu tilfelli er nýrri línu bætt við fyrir ofan valda gátlistalínu viðhalds.

15. Í reitnum **Gerð** skaltu velja línugerðina og bættu síðan við upplýsingum sem tengjast gerð viðhaldsgátlistans. Sjá lýsingu á fyrirliggjandi gerðum og tengdum reitum í kaflanum [Stofna sniðmát viðhaldsgátlista](#create-a-maintenance-checklist-template).

    > [!NOTE]
    > Til að afrita uppsetningu á viðhaldsgátlista úr annarri gerð viðhaldsverka skaltu velja **Afrita viðhaldsgátlista** og velja síðan gerð viðhaldsverksins sem á að afrita uppsetninguna úr.
    >
    > Auðvelt er að stofna nýtt sniðmát eða velja úr fyrirliggjandi viðhaldsgátlistum. Þú getur síðan endurnýtt sniðmátið í mörgum gátlistum fyrir viðhald. Nýja sniðmátið verður nákvæmt afrit af virkum viðhaldsgátlista. Veldu **Stofna sniðmát** og færðu síðan inn heiti fyrir sniðmátið. Til að skipta um fyrirliggjandi gátlista fyrir viðhald fyrir eina línu sem vísar í nýja sniðmátið skaltu stilla valkostinn **Skipta um** á **Já**. Þú getur skoðað innihald sniðmátsins á upplýsingasíðunni **Sniðmát viðhaldsgátlista**.

16. Veldu **Vista** til að vista breytingarnar.
17. Farðu aftur á síðuna **Sjálfgefin tegund viðhaldsverka**.
18. Veldu **Verkfæri**.
19. Á síðunni **Sjálfgefin verkfæri fyrir gerð viðhaldsverka** er hægt að bæta við verkfærunum (tilföngunum) sem ætti að nota við gerð viðhaldsverks. Veldu **Nýtt** og veldu síðan verkfærið í reitnum **Tilföng**.

    > [!NOTE]
    > Til að afrita verkfærauppsetninguna úr annarri gerð viðhaldsverka skaltu velja **Afrita verkfæri** og velja síðan gerð viðhaldsverksins sem á að afrita uppsetninguna úr.

20. Veldu **Vista** til að vista breytingarnar.
21. Farðu aftur á síðuna **Sjálfgefin tegund viðhaldsverka**.
22. Veldu **Verklýsing**.
23. Á síðunni **Vinnulýsing** velurðu **Breyta** og bætir síðan við lýsingu sem er tengd við sjálfgefna gerð viðhaldsverka eins og þú þarft.
24. Veldu **Vista** til að vista lýsinguna.

    Ef þú bætir við vinnulýsingu hérna hnekkir hún öllum lýsingum sem eru settar upp fyrir gerð viðhaldsverka á síðunni **Gerðir viðhaldsverka**. Ef þú bætir ekki við vinnulýsingu hér er notast við þá lýsingu sem er sett upp fyrir gerð viðhaldsvera. Lýsingar eru sjálfkrafa færðar yfir í verkbeiðnir sem nota gerð viðhaldsverka eða sjálfgefna gerð viðhaldsverka.

25. Farðu aftur á síðuna **Sjálfgefin tegund viðhaldsverka**.
26. Til að setja upp viðhengi á valda sjálfgefna línu gerðar viðhaldsverka velurðu **Hengja skjöl við**. Viðhengi sem eru sett upp á sjálfgefinni línu gerðar viðhaldsstarfa eru sjálfkrafa innifalin í verkbeiðnilínum sem nota þá sjálfgefnu línu gerðar viðhaldsverka.
27. Smelltu á **Nýtt** og veldu síðan skjalagerð.
28. Settu skjalið eða skrána inn.
29. Stilltu reitina á síðunni **Viðhengi**. Viðhengisuppsetningin notar venjulega skjalauppsetningarvirkni.
30. Veldu **Vista** til að vista viðhengið.

    > [!NOTE]
    > Viðhengi við sjálfgefna línu viðhaldsverka eru prentuð ásamt verkbeiðniskýrslu ef skjalagerðir viðhengjanna eru valin á flipanum **Gerðir skjala** á síðunni **Færibreytur eignastjórnunar** (**Eignastjórnun** \> **Uppsetning** \> **Færibreytur eignastjórnunar**). Dæmi um viðhengi eru leiðbeiningar sem útskýra hvernig á að ljúka tiltekinni vinnslu eða fyrirframskilgreindur viðhaldsgátlisti (ef þú notar ekki viðhaldsgátlistavirkni fyrir sjálfgefnar línur gerða viðhaldsverka).

    Á síðunni **Sjálfgefin tegund viðhaldsverka** sýnir hver lína fjölda spáðra klukkustunda og einnig fjölda lína sem hafa verið búnar til fyrir vörur, útgjöld, viðhaldsgátlista og verkfæri. Reiturinn **Eignir** sýnir fjölda virkra eigna sem eru tengdar sjálfgefinni línu gerðar viðhaldsverka.

31. Til að afrita sjálfgefna gerð viðhaldsverka yfir í aðra sjálfgefna gerð viðhaldsverka skaltu velja sjálfgefna línu gerðar viðhaldsverka til að afrita aðra uppsetningu, velja **Afrita uppsetningu** og veldu síðan sjálfgefna gerð viðhaldsverkefna sem á að afrita.
32. Til að skoða lista yfir eignir, viðhaldsáætlanir eða viðhaldsumferðir sem eru að nota sjálfgefna línu gerðar viðhaldsverka skaltu velja þá línu og síðan **Notað af**.

![Síðan Tegundasjálfgildi viðhaldsverka](media/07-setup-for-work-orders.png)

Þegar kerfið velur fyrirliggjandi gerðarsjálfgildi viðhaldsverks sem ætti að nota í verkbeiðnilínu er valið byggt á eigninni og tengdri uppstillingu eignagerðar. Eignastýring fer í gegnum allar sjálfgefnar færslur viðhaldsverka sem eru tengdar þeirri gerð viðhaldsverka sem tengist eignategundinni til að leita að mögulegri samsvörun. Það athugar alltaf sértækustu samsetninguna fyrst. Með öðrum orðum, til að finna sértækustu samsetninguna leitar Eignastjórnun fyrst að hugsanlegri samsvörun fyrir reitinn **Viðskipti**. Ef engin samsvörun er fundin, skoðar hún hvort samsvörun sé fyrir reitinn **Afbrigði af viðhaldsstörfum**. Ef engin samsvörun finnst leitar hún að samsvörun fyrir reitinn **Tegund viðhaldsverks**, og svo framvegis (**Viðskipti**, síðan **Tegundaafbrigði viðhaldsverka**, síðan **Gerð viðhaldsverks**, síðan **Eignir**, síðan **Tegund**, síðan **Framleiðandi** og loks **Gerð eigna**). Ef engin samsvörun finnst er sjálfgefna skráin þar sem aðeins gerð viðhaldsverkefna er valin notuð.

Auðkenni verkefna er sjálfkrafa tengt við hverja sjálfgefna línu viðhaldsverka sem þú býrð til. Verkþátturinn er stofnaður í spáverkinu sem er valin í reitnum **Verk viðhaldsspár** á flipanum **Eignir** á síðunni **Færibreytur eignastjórnunar**. Tilgangurinn með verkþættinum er að stjórna spám um klukkustundir, vörur og útgjöld í tengslum við verkbeiðnir. Spár um gerðir viðhaldsverka eru sjálfkrafa færðar yfir í verkbeiðnilínuna og þær eru afritaðar úr spáverkefninu yfir í verkbeiðniverkefnið sem er búið til fyrir verkbeiðnilínuna. Tilgangurinn með verkþættinum er að stjórna spám í tengslum við verkbeiðnir.

Þú getur sett upp runuvinnslu til að uppfæra sjálfgefnar tilvísanir í gerð viðhaldsverka með reglulegu millibili, eða þú getur keyrt starfið handvirkt. Til að stofna runuvinnslu eða keyra handvirka uppfærslu skaltu velja **Eignastjórnun** \> **Reglubundið** \> **Fyrirbyggjandi viðhald** \> **Uppfæra sjálfgefnar tilvísanir í gerðir viðhaldsverka**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Yfirlit yfir gerðir viðhaldsverka sem tengjast eignum

Eftir að þú hefur búið til nauðsynlegar sjálfgefnar samsetningar á gerðum viðhaldsverka geturðu notað síðuna **Allar eignir** til að fá yfirlit yfir núverandi sjálfgildi gerðar viðhaldsverka sem tengist tiltekinni eign. Yfirlitið sýnir allar sjálfgefnar samsetningar á gerðum viðhaldsverka sem hægt er að nota á eignategundina sem er valin fyrir eignina. Þessar samsetningar innihalda samsetningar sem hafa afbrigði af tegundaafbrigðum viðhaldsverka og viðskipta með viðhaldsverk.

1. Veldu **Eignastýring** \> **Sameiginlegt** \> **Eignir** \> **Allar eignir** eða **Virkar eignir**.
2. Á listanum velurðu eign til að sjá yfirlit yfir tegundasamsetningar á viðhaldsverkum fyrir.
3. Á aðgerðarrúðunni, á flipanum **Almennt**, í hópnum **Tengdar upplýsingar** skaltu velja **Gerðir viðhaldsverka**.

    Vinstri rúðan á síðunni **Gerðir viðhaldsverka eigna** sýnir lista yfir allar samsetningar á gerðum viðhaldsverka sem tengjast völdum eignum.

4. Veldu samsetningu á gerð viðhaldsverka til að sjá tengda uppsetningu fyrir viðhaldsgátlista, spár og verkfæri. Kaflinn **Upplýsingar** á flýtiflipanum **Sjálfgefin tegund viðhaldsverka** sýnir fjölda tengdra gátlista viðhalds, spáðra klukkustunda, vara og svo framvegis, sem tengjast valinni samsetningu á gerðum viðhaldsverka.
5. Til að skoða upplýsingar um valda gerð viðhaldsverka velurðu **Gerðir viðhaldsverka**.

![Síðan Gerðir eignaviðhaldsverka](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Sjálfvirk uppfærsla á spám um gerðir viðhaldsverka

Í eignastjórnun geturðu sjálfkrafa uppfært allar breytingar á spám um gerðir viðhaldsverka fyrir kostnað á klukkustund, vörukostnað og útgjöld sem hafa verið uppfærð í öðrum einingum. Með þessu móti hjálpar þú við að tryggja að spár þínar um gerðir viðhaldsverka noti alltaf nýjasta kostnaðarverðið.

1. Veldu **Eignastjórnun** \> **Reglubundið** \> **Spá** \> **Uppfærðu spá um gerð viðhaldsverka**.
2. Í valmyndinni **Uppfæra spá um gerð viðhaldsverka** á flýtiflipanum **Færslur til að hafa með** er hægt að bæta við vali fyrir sérstakar viðhaldsgerðir, eftir þörfum. Veldu **Sía** og veldu síðan **Velja** til að gera valið.
3. Á flýtiflipanum **Keyra í bakgrunni** geturðu sett upp sjálfvirka uppfærslu sem runuvinnslu, eftir þörfum.
4. Veldu **Í lagi** til að hefja uppfærslu á spá.
