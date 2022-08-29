---
title: Leitaðu að gögnum með því að nota Warehouse Management farsímaforrit krókaleiðir
description: Þessi grein lýsir því hvernig á að stilla gagnafyrirspurnir í valmyndarhlutum farsíma og nota þau sem hluta af krókaleiðum.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: cc013e962b4da803764f16e451b1d433666e75c2
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336606"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Leitaðu að gögnum með því að nota Warehouse Management farsímaforrit krókaleiðir

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Eiginleikakynning

Með því að bjóða upp á strikamerkjaskönnunargetu gefur Warehouse Management farsímaforritið þér auðvelda og nákvæma leið til að fanga gögn sem hluta af vöruhúsaferlum þínum. Hins vegar eru strikamerki stundum skemmd og verða ólæsileg, eða nauðsynlegar gagnaupplýsingar gætu ekki verið til sem strikamerki í viðskiptaferlinu þínu. Í þessum tilfellum getur handvirk innsláttur gagna tekið langan tíma og getur jafnvel valdið því að rangar upplýsingar eru teknar. Árangurinn getur verið minni skilvirkni og lægra þjónustustig.

Með því að nota sveigjanlegt gagnafyrirspurnarferli geta starfsmenn auðveldlega flett upp nauðsynlegum upplýsingum sem hluta af innbyggða vöruhúsastjórnun farsímaforritinu og beitt síunarvalkostum þannig að aðeins viðeigandi gögn séu sýnd. Þess vegna er handvirkt val hraðara og nákvæmara.

Til dæmis, í móttökuflæði innkaupapöntunar, þarf innkaupapöntunarnúmer til að passa við komandi birgðir. Sem hluti af þessu ferli geturðu auðveldlega stillt valmyndaratriði til að gefa upp kortalista yfir viðkomandi innkaupapöntunarnúmer. Á þennan hátt geturðu haldið áfram móttökuflæðinu með því að nota fljótlega punkt-til-velja nálgun. Þessi grein veitir dæmi um atburðarás, en virknina er einnig hægt að nota í einhverju eða öllum vöruhúsastjórnun farsímaforritinu þínu.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Kveiktu á gagnafyrirspurnarflæðiseiginleikanum og forsendum hans

Áður en þú getur notað virknina sem lýst er í þessari grein verður þú að ljúka eftirfarandi ferli til að kveikja á nauðsynlegum eiginleikum.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**. (Til að fá frekari upplýsingar um hvernig á að nota **Eiginleikastjórnun** vinnurými, sjá [Yfirlit yfir eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) .)
1. Ef þú ert að keyra Supply Chain Management útgáfu 10.0.28 eða eldri, kveiktu á eiginleikanum sem er skráður á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Leiðbeiningar fyrir skref vöruhúsaforrits*

    Þessi eiginleiki er forsenda fyrir *Fyrirspurnarflæði vöruhúsastjórnunarapps* eiginleiki. Frá og með Supply Chain Management útgáfu 10.0.29 er það skylda og ekki hægt að slökkva á henni. Frekar upplýsingar um eiginleikann *Leiðbeiningar fyrir skref vöruhúsaforrits* er að finna í [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management ](mobile-app-titles-instructions.md).

1. Kveiktu á eiginleikanum sem er skráður á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Hjáleiðir forrits vöruhúsakerfis*

    Þessi eiginleiki er forsenda fyrir *Fyrirspurnarflæði vöruhúsastjórnunarapps* eiginleiki. Frá og með Supply Chain Management útgáfu 10.0.29 er sjálfgefið kveikt á henni. Fyrir frekari upplýsingar um *Vöruhússtjórnun app krókaleiðir* eiginleiki, sjá [Stilltu krókaleiðir fyrir skref í valmyndaratriðum farsíma](warehouse-app-detours.md).

1. Ef *Vöruhússtjórnun app krókaleiðir* eiginleiki var ekki þegar kveikt á, uppfærðu reitnöfnin í vöruhúsastjórnun farsímaforritinu með því að fara á **Vöruhússtjórnun \> Uppsetning \> Farsímatæki \> Reitaheiti vöruhúsaapps** og velja **Búðu til sjálfgefna uppsetningu**. Endurtaktu þetta skref fyrir hvern lögaðila (fyrirtæki) þar sem þú notar vöruhúsastjórnun farsímaforritið. Frekari upplýsingar eru í [Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis](configure-app-field-names-priorities-warehouse.md).
1. Kveiktu á eiginleikanum sem er skráður á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Eiginleikaheiti:** *Fyrirspurnarflæði vöruhúsastjórnunarapps*

    Þessi eiginleiki er sá sem lýst er í þessari grein.

## <a name="example-scenarios"></a>Dæmi um aðstæður

Þessi grein notar dæmi atburðarás til að sýna hvernig þú getur notað *Fyrirspurnarflæði vöruhúsastjórnunarapps* eiginleika til að bæta innkaupakvittunarflæðið. Aðstæðurnar nota staðlað sýnishornsgögn, sem innihalda flæði sem er nefnt *Kaup fá*. Þetta flæði byrjar á því að hvetja starfsmenn til að auðkenna innkaupapöntunarnúmer sem þeir fá á móti. Til að auðvelda starfsmönnum að bera kennsl á innkaupapöntunina muntu bæta fyrstu síðu flæðisins með því að bæta við eftirfarandi nýjum fyrirspurnarvalkostum sem [krókaleiðir](warehouse-app-detours.md):

- **Leitaðu að innkaupapöntunum eftir söluaðila** – Opnaðu síðu sem biður starfsmenn um að slá inn nafn lánardrottins eða hluta af nafni lánardrottins. Hægt er að nota jokerstafi. Til dæmis, ef starfsmaður á von á afhendingu á heimleið í dag frá seljanda sem inniheldur *Snúður* í nafni þess geta þeir farið inn **Hala\*** til að skoða kortasett fyrir opnar innkaupapantanir sem innihalda þennan texta. Hvert kort hefur nokkra reiti sem veita upplýsingar um hverja innkaupapöntun. Auk nafns lánardrottins er hægt að hanna kortin þannig að þau sýni reikningsnúmer lánardrottins, afhendingardag og skjalastöðu.
- **Leitaðu að söluaðilum í dag** – Opnaðu síðu sem biður starfsmenn ekki um að slá inn gögn en sýnir í staðinn forstilltar síur (eins og dagsetningu í dag). Síðan sýnir síðan sett af spilum sem passa við síuna. Starfsmenn halda áfram með því að velja kort fyrir innkaupapöntunina sem þeir vilja skrá birgðavörur á.
- **Flettu upp pöntunum eftir hlut** - Opnaðu síðu sem biður starfsmenn um að skanna strikamerkið fyrir hvaða hlut sem er í komandi birgðum. Flæðið listar síðan allar opnar innkaupapantanir sem innihalda línur fyrir skannað vörunúmer. Til að ná yfir aðstæður þar sem strikamerki er ekki hægt að lesa, geturðu bætt annarri krókaleit við þessa síðu sem gerir starfsmönnum kleift að leita að vörunúmerum innan ákveðinnar innkaupapöntunar.

Í hverju tilviki auðkennir starfsmaðurinn innkaupapöntun með því að velja kort og er síðan farið aftur á fyrstu síðu sem sýnir valið innkaupapöntunarnúmer. Starfsmaðurinn getur síðan haldið áfram skráningarflæði birgðavöru á innleið.

## <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að vinna í gegnum dæmið atburðarás sem lýst er í þessari grein verður þú að vera á kerfi þar sem staðalinn [kynningargögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp. Að auki verður þú að velja *USMF* lögaðila (fyrirtæki) áður en þú byrjar.

## <a name="configure-the-mobile-device-menu-items"></a>Stilltu valmyndaratriði fartækisins

Til að búa til hvern og einn af nýju fyrirspurnarvalkostunum sem þú þarft að bæta við fyrstu síðu flæðisins verður þú að setja það upp sem valmyndaratriði fyrir farsíma. Síðar muntu gera fyrirspurnarmöguleikana tiltæka sem krókaleiðir að *Kaup fá* flæði.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Búðu til valmyndaratriðið „Flita inn pöntunum eftir söluaðila“

Búðu til **Leitaðu að innkaupapöntunum eftir söluaðila** valmyndaratriði með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við valmyndaratriði fyrir farsíma.
1. Stilltu eftirfarandi gildi fyrir nýja valmyndaratriðið:

    - **Heiti valmyndaratriðis:** *Leitaðu að innkaupapöntunum eftir söluaðila*
    - **Titill:** *Leitaðu að innkaupapöntunum eftir söluaðila*
    - **Stilling:** *Óbein*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Virknikóði:** *Gagnafyrirspurn*
    - **Notaðu aðferðarleiðbeiningar:** *Já* (Þetta gildi er sjálfkrafa valið.)
    - **Nafn töflu:** *PurchTable* (Þú vilt fletta upp innkaupapöntunarnúmerum úr þessari töflu.)

1. Á aðgerðarrúðunni velurðu **Breyta fyrirspurn** til að skilgreina fyrirspurn sem er byggð á valinni grunntöflu (í þessu tilviki innkaupapantanatöfluna).
1. Í fyrirspurnaritlinum, á **Svið** flipanum skaltu bæta eftirfarandi línum við ristina.

    | Tafla | Afleidd tafla | Reitur | Skilyrði |
    |---|---|---|---|
    | Innkaupapantanir | Innkaupapantanir | Staða innkaupapöntunar | Opin pöntun |
    | Innkaupapantanir | Innkaupapantanir | Afhendingardagur | (dagasvið(-10,10)) |
    | Innkaupapantanir | Innkaupapantanir | Nafn lánardrottins | |

1. Veldu **Í lagi**.

    Í þessu dæmi er nýja valmyndaratriðið stillt til að finna opnar innkaupapantanir sem búist er við að berist hvenær sem er á milli 10 daga í fortíðinni og 10 daga í framtíðinni.

    Í fyrirspurninni er **Viðmið** dálkur fyrir *Nafn söluaðila* hefur verið skilið eftir autt. Þess vegna munu starfsmenn geta tilgreint þetta gildi á meðan þeir nota vöruhúsastjórnun farsímaforritið.

    Ef þú vilt tilgreina hvernig listinn verður flokkaður geturðu sett upp flokkunina á **Flokkun** flipa.

1. Auk þess að skilgreina fyrirspurnina þarf að velja hvaða reitir verða sýndir á spjöldum á fyrirspurnarlistasíðunni. Því skaltu velja á aðgerðarrúðunni **Vallarlisti**.
1. Á **Vallarlisti** síðu, stilltu eftirfarandi gildi:

    - **Sýnareit 1:** *PurchId* (Þessi reitur verður sýndur sem haus fyrir hvert kort.)
    - **Sýnareit 2:** *Staða kaups*
    - **Sýnareit 3:** *PurchName*
    - **Sýnareit 4:** *OrderAccount*
    - **Sýnareit 5:** *Afhendingardagur*
    - **Sýnareit 6:** *sýnaDocumentStatus()* (Þetta gildi er birtingaraðferð eins og „()“ í lokin gefur til kynna.)

1. Í aðgerðarúðunni skal velja **Vista**. Því næst skal loka síðunni.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Búðu til valmyndaratriðið „Flita inn pöntunum í dag“

Búðu til **Leitaðu að söluaðilum í dag** valmyndaratriði með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við valmyndaratriði fyrir farsíma.
1. Stilltu eftirfarandi gildi fyrir nýja hlutinn:

    - **Heiti valmyndaratriðis:** *Leitaðu að söluaðilum í dag*
    - **Titill:** *Leitaðu að söluaðilum í dag*
    - **Stilling:** *Óbein*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Virknikóði:** *Gagnafyrirspurn*
    - **Notaðu aðferðarleiðbeiningar:** *Já* (Þetta gildi er sjálfkrafa valið.)
    - **Nafn töflu:** *PurchTable* (Þú vilt fletta upp innkaupapöntunarnúmerum úr þessari töflu.)

1. Á aðgerðarrúðunni velurðu **Breyta fyrirspurn** til að skilgreina fyrirspurn sem er byggð á valinni grunntöflu (í þessu tilviki innkaupapantanatöfluna).
1. Í fyrirspurnaritlinum, á **Svið** flipanum skaltu bæta eftirfarandi línum við ristina.

    | Tafla | Afleidd tafla | Reitur | Skilyrði |
    |---|---|---|---|
    | Innkaupapöntun | Innkaupapöntun | Staða innkaupapöntunar | Opin pöntun |
    | Innkaupapöntun | Innkaupapöntun | Afhendingardagur | (Dagur (0)) |

1. Veldu **Í lagi**.

    Í þessu dæmi er nýja valmyndaratriðið stillt til að finna opnar innkaupapantanir sem búist er við að berist í dag.

    Ef þú vilt tilgreina hvernig listinn verður flokkaður geturðu sett upp flokkunina á **Flokkun** flipa.

1. Auk þess að skilgreina fyrirspurnina þarf að velja hvaða reitir verða sýndir á spjöldum á fyrirspurnarlistasíðunni. Því skaltu velja á aðgerðarrúðunni **Vallarlisti**.
1. Á **Vallarlisti** síðu, stilltu eftirfarandi gildi:

    - **Sýnareit 1:** *PurchName* (Þessi reitur verður sýndur sem haus fyrir hvert kort.)
    - **Sýnareit 2:** *PurchId*
    - **Sýnareit 3:** *Staða kaups*
    - **Sýnareit 4:** *DlvMode*
    - **Sýnareit 5:** *DlvTerm*
    - **Sýnareit 6:** *OrderAccount*
    - **Sýnareit 7:** *VendorName()* (Þetta gildi er birtingaraðferð eins og „()“ í lokin gefur til kynna.)

1. Í aðgerðarúðunni skal velja **Vista**. Því næst skal loka síðunni.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Búðu til valmyndaratriðið „Flita inn pöntunum eftir atriði“

Búðu til **Flettu upp pöntunum eftir hlut** valmyndaratriði með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á aðgerðarrúðunni velurðu **Nýtt** til að bæta við valmyndaratriði fyrir farsíma.
1. Stilltu eftirfarandi gildi fyrir nýja hlutinn:

    - **Heiti valmyndaratriðis:** *Flettu upp pöntunum eftir hlut*
    - **Titill:** *Flettu upp pöntunum eftir hlut*
    - **Stilling:** *Óbein*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Virknikóði:** *Gagnafyrirspurn*
    - **Notaðu aðferðarleiðbeiningar:** *Já* (Þetta gildi er sjálfkrafa valið.)
    - **Nafn töflu:** *PurchLine* (Þú vilt fletta upp innkaupapöntunarnúmerum byggt á vörunúmeri í gegnum línugögnin.)

1. Á aðgerðarrúðunni velurðu **Breyta fyrirspurn** til að skilgreina fyrirspurn sem er byggð á völdum grunntöflu (í þessu tilviki, innkaupapöntunarlínutöfluna, en þú getur notað hvaða gildi sem tengjast hausnum með því að tengja við *PurchTable*).
1. Í fyrirspurnaritlinum, á **Svið** flipanum skaltu bæta eftirfarandi línum við ristina.

    | Tafla | Afleidd tafla | Reitur | Skilyrði |
    |---|---|---|---|
    | Innkaupapöntunarlínur | Innkaupapöntunarlínur | Staða línu | Opin pöntun |
    | Innkaupapöntunarlínur | Innkaupapöntunarlínur | Afhendingardagur | (dagasvið(-10,10)) |
    | Innkaupapöntunarlínur | Innkaupapöntunarlínur | Vörunúmer | |

1. Veldu **Í lagi**.

    Í þessu dæmi er nýja valmyndaratriðið stillt til að finna opnar innkaupapöntunarlínur sem búist er við að berist hvenær sem er á milli 10 daga í fortíðinni og 10 daga í framtíðinni.

    Í fyrirspurninni er **Viðmið** dálkur fyrir *Vörunúmer* hefur verið skilið eftir autt. Þess vegna munu starfsmenn geta tilgreint þetta gildi á meðan þeir nota vöruhússtjórnun farsímaforritið.

    Ef þú vilt tilgreina hvernig listinn verður flokkaður geturðu sett upp flokkunina á **Flokkun** flipa.

1. Auk þess að skilgreina fyrirspurnina þarf að velja hvaða reitir verða sýndir á spjöldum á fyrirspurnarlistasíðunni. Því skaltu velja á aðgerðarrúðunni **Vallarlisti**.
1. Á **Vallarlisti** síðu, stilltu eftirfarandi gildi:

    - **Sýnareit 1:** *PurchId* (Þetta svæðisgildi verður notað sem haus fyrir hvert kort.)
    - **Sýnareit 2:** *VendAccount*
    - **Sýnareit 3:** *KaupMagn*
    - **Sýnareit 4:** *PurchUnit*
    - **Sýnareit 5:** *Staða kaups*

1. Í aðgerðarúðunni skal velja **Vista**. Því næst skal loka síðunni.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Bættu nýju valmyndaratriðum fartækisins við valmynd

Þrír nýju valmyndaratriðin þín fyrir farsíma eru nú tilbúin til að bæta við valmynd farsímans. Þessu verkefni verður að ljúka áður en hægt er að nota valmyndaratriðin sem hluta af krókaferli. Í þessu dæmi muntu búa til nýja undirvalmynd og bæta nýjum valmyndaratriðum við hana.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Stilltu eftirfarandi gildi í haus nýju færslunnar:

    - **Nafn:** *Spyrjið*
    - **Lýsing:** *Spyrjið*

1. Í **Valmyndir og valmyndir í boði** lista, veldu fyrsta valmyndaratriði farsíma sem þú bjóst til. Veldu síðan hægri örvarhnappinn til að færa hlutinn í **Uppbygging matseðils** lista.
1. Endurtaktu fyrra skrefið fyrir hina tvo nýju valmyndaratriðin.
1. Í listaglugganum vinstra megin velurðu **Aðal** matseðill.
1. Í **Valmyndir og valmyndir í boði** listann, skrunaðu niður að **Matseðlar** kafla og veldu nýja **Spyrjið** matseðill. Veldu síðan hægri örvarhnappinn til að færa hlutinn í **Uppbygging matseðils** lista.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Stilltu krókaleiðir í skrefum farsímans þíns

Til að ljúka uppsetningunni verður þú nú að nota krókastillingu á **Skref fyrir farsíma** síðu til að bæta þremur nýju valmyndaratriðum farsíma við núverandi innkaupapöntunarauðkenningarskref í *Kaup fá* flæði.

1. Fara til **Vöruhússtjórnun \> Uppsetning > Farsímatæki \> Skref fyrir farsíma**.
1. Í **Sía** reit, slá inn *PONum*. Veldu síðan *Skref auðkenni: "PONum"* í fellilistanum.
1. Á meðan skráin sem finnst er valin í hnitanetinu skaltu velja **Bættu við þrepastillingu** á aðgerðasvæðinu. Í fellivalmyndinni sem birtist skaltu stilla **Valmyndaratriði** sviði til *Kaup móttaka*. Veldu síðan **Allt í lagi** til að loka glugganum.
1. Á upplýsingasíðunni fyrir nýju skrefastillinguna (**Móttaka kaup: PONum**), á **Tiltækar krókaleiðir (valmyndaratriði)** Flýtiflipi, veldu **Bæta við** á tækjastikunni.
1. Í **Bæta við krók** valmynd, finndu og veldu **Leitaðu að innkaupapöntunum eftir söluaðila** valmyndaratriði sem þú bjóst til áður.
1. Veldu **Allt í lagi** til að loka glugganum og bæta völdum valmyndaratriði við krókalistann.
1. Veldu nýju hjáleiðina og veldu síðan **Veldu reiti til að senda** á tækjastikunni.
1. Í **Veldu reiti til að senda** valmynd, ekki bæta neinu við **Senda frá kaupum fá** kafla, vegna þess að þú vilt ekki senda nein gildi yfir í krókavalmyndaratriðið. Hins vegar, í **Komdu til baka frá því að fletta upp pöntunum eftir söluaðila** kafla, stilltu eftirfarandi gildi fyrir tómu línuna sem þegar hefur verið bætt við þar:

    - **Afritaðu frá Leitaðu að innkaupapöntunum eftir söluaðila:** *Pöntun*
    - **Límdu í innkaupamóttöku:** *Pöntun*

1. Veldu **Í lagi** til að loka svarglugganum.
1. Endurtaktu skref 4 til 9 fyrir hina tvo nýju valmyndaratriðin (**Leitaðu að söluaðilum í dag** og **Flettu upp pöntunum eftir hlut**). Hvað varðar **Leitaðu að innkaupapöntunum eftir söluaðila** valmyndaratriði, þú vilt ekki senda nein gögn á þessar krókaleiðir, en þú vilt skila innkaupapöntunarnúmeri.
1. Lokið síðunni.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Prófaðu innkaupamóttökuflæði sem hefur gagnafyrirspurn sem hluta af krók

Fylgdu þessum skrefum til að prófa nýja uppsetningu farsímaforritsins.

1. Stofna nokkrar innkaupapantanir sem hafa línur fyrir vöruhús 51.
1. Farðu í fartæki eða hermi sem keyrir farsímaforrit vöruhúsakerfis og skráðu þig inn í vöruhús 51 með því að nota *51* sem notandakenni og *1* sem aðgangsorð.
1. Veldu í valmynd farsímaforritsins **Á heimleið** og svo **Kaup fá**.

    Þú ættir að sjá eftirfarandi síðu, sem inniheldur þrjú nýju valmyndaratriðin.

    ![Móttaka kaups með því að nota innkaupanúmer.](media/wma-purchase-receive-po-num-with-detours.png "Móttaka kaups með því að nota innkaupanúmer")

1. Prófaðu mismunandi möguleika og taktu eftir því að þú getur sent innkaupapöntunarnúmer til baka með því að velja eitt af kortunum á listanum.

    ![Móttaka innkaupa með því að nota PO leit eftir söluaðila, dæmi 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Móttaka innkaupa með því að nota PO leit eftir söluaðila, dæmi 1")

    ![Móttaka innkaupa með því að nota PO leit eftir söluaðila, dæmi 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Móttaka innkaupa með því að nota PO leit eftir söluaðila, dæmi 2")

> [!TIP]
> Í stað þess að keyra móttökuflæðið með því að fletta frá **Kaup fá** valmyndaratriði, þú getur byrjað á fyrirspurnarflæði (**Aðal \> Spyrjið \> Leitaðu að innkaupapöntunum eftir söluaðila**) og kalla fram hjáleið til að keyra æskilegt flæði með því að velja eitt af spilunum á listanum. Til að nota þessa nálgun geturðu skilgreint krók á **Skref fyrir farsíma** síðu fyrir skrefið sem hefur a **Skref auðkenni** verðmæti á *GenericDataInquiryList*. Vegna þess að þetta flæði er krókaflæði er ekki hægt að kalla fram fleiri krókaleiðir frá því. Þess vegna, þegar þú kemst á innsláttarskjá vörunúmers, til dæmis, verður uppflettingin ekki tiltæk á honum, vegna þess að kerfið styður sem stendur aðeins eitt stig af krókaleiðum.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
