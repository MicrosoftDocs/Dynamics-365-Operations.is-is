---
title: Birgðastaðsetning
description: Þessi grein veitir upplýsingar um stefnumótandi birgðastaðsetningu, sem felur í sér að auðkenna aftengingarpunkta í aðfangakeðjunni þinni, þar sem þú getur byggt upp á lager til að hjálpa til við að þjappa saman afgreiðslutíma og taka á móti áföllum í aðfangakeðjuna þína.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: ReqGroup, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 847108575cbf7207282db00d731363c8cfad883a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689539"
---
# <a name="inventory-positioning"></a>Birgðastaðsetning

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Stefnumótuð birgðastaða felur í sér að bera kennsl á aftengingarpunkta í aðfangakeðjunni þinni, þar sem þú getur byggt upp birgðir fyrir hendi. Þessi nálgun er aðallega notuð til að hjálpa til við að þjappa leiðtíma og taka á móti áföllum í aðfangakeðjuna þína. Það gerir þér kleift að draga úr „bullwhip-áhrifum“ vegna þess að breytileiki eftirspurnar fer ekki alla leið niður aðfangakeðjuna. (The *bullwhip áhrif* vísar til þess hvernig litlar sveiflur í eftirspurn á smásölustigi geta valdið sífellt meiri sveiflum í eftirspurn hjá heildsölu-, dreifingaraðila-, framleiðanda- og hráefnisbirgðastigi.)

Birgðastaða er fyrsta skrefið í Demand Driven Materials Resource Planning (DDMRP).

## <a name="inventory-positioning-for-manufacturing"></a>Birgðastaða fyrir framleiðslu

Þessi hluti gefur dæmi sem sýnir hvernig á að taka ákvarðanir um staðsetningu birgða ef þú framleiðir dæmigerða koddavöru. Púðinn er með fjölþrepa efnisskrá (BOM), eins og sýnt er á eftirfarandi mynd.

![Dæmi um fjölþrepa efnisskrá (BOM) fyrir koddavöru.](media/ddmrp-bom-example.png "Dæmi um fjölþrepa efnisskrá (BOM) fyrir koddavöru")

### <a name="choose-your-decoupling-points"></a>Veldu aftengingarpunktana þína

Þegar þú ert að velja hvar á að setja aftengingarpunktana þína skaltu íhuga alla eftirfarandi þætti hvers atriðis í uppskriftinni sem viðmið:

- Ytri breytileiki
- Birgðaáhrif og sveigjanleiki
- Mikilvæg rekstrarvernd
- Umburðarlyndistími viðskiptavina
- Sýnilegur sjóndeildarhringur sölupöntunar
- Markaðsmögulegur afgreiðslutími

Í koddadæminu gætirðu sett fyrsta aftengingarpunktinn þinn á *froðublöð* af eftirfarandi ástæðum:

- Það er erfitt að fá efnin sem eru notuð til að búa til froðuplöturnar og framboðið er óstöðugt. Þess vegna er *ytri breytileiki* skilyrði er uppfyllt.
- Hægt er að skera froðuplöturnar í margar mismunandi gerðir og stærðir til að búa til froðuinnlegg fyrir aðrar vörur sem þú framleiðir, auk koddans. Þess vegna er *birgðaskiptingu og sveigjanleika* skilyrði er uppfyllt.

Þú gætir þá sett næsta aftengingarpunkt þinn á *dúkasett*, sem er forklippt koddaefni. Þú gætir valið þennan punkt vegna þess að þú ert aðeins með eina dúkaskurðarvél. Þess vegna er *mikilvæg rekstrarvernd* skilyrði er uppfyllt.

Að lokum gætirðu sett síðasta aftengingarpunktinn þinn á fullunna góða koddahlutinn. Þú gætir valið þennan punkt vegna þess að þú ert með mjög lágt *þoltími viðskiptavina* á sölu, og vegna þess að þinn *sýnileikasvið sölupöntunar* er frekar stutt. Þess vegna viltu tryggja að þú hafir tiltækar birgðir til að mæta pöntunum sem berast. Þú getur líka sett hærra verð með því að hafa afgreiðslutímann svona stuttan, sem er það sem er *markaðsmögulegur leiðtími* viðmið vísar til.

Byggt á þessari greiningu sýnir eftirfarandi mynd hvernig koddauppskriftin mun líta út. Gul birgðatákn auðkenna aftengingarpunktana.

![Dæmi um uppskrift með aftengingarpunktum auðkenndum.](media/ddmrp-bom-decoupling-example.png "Dæmi um uppskrift með aftengingarpunktum auðkenndum")

### <a name="calculate-your-decoupled-lead-time"></a>Reiknaðu aftengdan leiðtíma þinn

Þessi hluti sýnir hvernig á að reikna út nýja afgreiðslutíma eftir að þú hefur kynnt aftengingarpunkta.

Í eftirfarandi mynd fyrir koddadæmið sem byrjað var í fyrri hlutanum eru afgreiðslutímar sýndir í gráum kössum efst til vinstri á hverjum uppskriftarhluta. Kassar sem eru með rauðum útlínum gefa til kynna atriði sem reka uppsafnaðan afgreiðslutíma (summa lengsta afgreiðslutíma á hverju stigi uppskriftarinnar). Þessi afgreiðslutími er 21 dagur þegar byrjað er frá grunni.

![Dæmi um uppskrift með afgreiðslutíma.](media/ddmrp-bom-lead-times-example.png "Dæmi um uppskrift með afgreiðslutíma")

Hins vegar, ef þú notar aftengingarpunktana sem þú valdir áður, verða aftengdu vörurnar alltaf til á lager. Þess vegna munu þeir hafa afgreiðslutíma 0 (núll). Nýr afgreiðslutími fyrir koddann er nú aðeins fimm dagar: tveir dagar til að kaupa þráðinn og þrír dagar til að framleiða koddann. Þessi leiðtími er þekktur sem *aftengdur leiðtími*.

![Dæmi um ótengdan leiðtíma.](media/ddmrp-bom-decoupled-lead-time-example.png "Dæmi um ótengdan leiðtíma")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Stefnumótandi birgðastaða í smásölumódeli

Vegna þess að smásalar geyma aðeins fullunnar vörur eru uppskriftir ekki vandamál. Hins vegar geta smásalar enn notað DDMRP með því að stilla stefnumótandi birgðastöðu og biðminni út frá geymslustöðum í dreifikerfinu.

Eftirfarandi mynd sýnir dæmi um fyrirtæki sem er með dreifingarmiðstöð í Seattle og verslanir í Boston, Atlanta og Portland.

![Aftengingarpunktar byggðir á staðsetningu í smásölulíkani.](media/ddmrp-retail-decoupl-points-example.png "Aftengingarpunktar byggðir á staðsetningu í smásölulíkani")

Þú gætir ákveðið að flutningstíminn til að flytja teppi vöru á milli dreifingarmiðstöðvar og verslana brjóti í bága við þinn *þoltími viðskiptavina*, vegna þess að viðskiptavinir þínir búast við að teppið sé til á lager þegar þeir heimsækja. Í þessu tilviki muntu setja upp aftengingarpunkt fyrir teppihlutinn í hverri af verslununum þremur. Hver verslun mun hafa mismunandi biðminni, byggt á afgreiðslutíma hennar, eftirspurnarmynstri og svo framvegis.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Innleiða birgðastaðsetningu í Dynamics 365 Supply Chain Management

Þessi hluti lýsir því hvernig á að innleiða birgðastaðsetningarstefnu þína í Microsoft Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Settu upp vöruþekjuhópa sem búa til aftengingarpunkta

Hlutir verða aftengingarpunktar þegar þeir tilheyra þekjuhópi sem er stilltur með a **Umfjöllunarkóði** verðmæti á *Aftengingarpunktur*. Þess vegna er fyrsta skrefið í því að setja upp DDMRP að ákveða hvaða þekjuhópa þú verður að innleiða fyrir DDMRP stefnu þína og búa þá til með því að fylgja þessum skrefum.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> þekjuflokkar**.
1. Á aðgerðarrúðunni velurðu **Nýtt** að búa til umfjöllunarhóp.
1. Sláðu inn upplýsingar sem auðkenna umfjöllunarhópinn og veldu síðan dagatalið sem á að nota.
1. Á **Almennt** flipann, stilltu **Umfjöllunarkóði** sviði til *Aftengingarpunktur*. Þessi stilling mun valda því að allir hlutir sem tilheyra þessum þekjuhópi verða meðhöndlaðir sem aftengingarpunktar fyrir DDMRP. Það gerir einnig allar DDMRP stillingar virkar fyrir þennan hóp, eins og lýst er síðar í þessari aðferð.
1. Á **Annað** flipa, í **DDMRP breytur** kafla, stilltu eftirfarandi reiti:

    - **Leiðslutími þáttur** – Tilgreindu þátt (sem aukastaf á milli 0 og 1) til að stjórna áhrifunum sem afgreiðslutími ætti að hafa þegar lágmarks- og hámarksbirgðir eru reiknaðar fyrir vörur í þessum þekjuflokki. Almennt séð, því lengri afgreiðslutími sem vara hefur, því lægri ætti afgreiðslutímastuðull hennar að vera. Lægri afgreiðslutímastuðull framleiðir lægri lágmarks- og hámarksbirgðir og veldur því minni og tíðari pöntunum. DDMRP aðferðafræði mælir með gildi á milli 0,20 og 0,40 fyrir vörur sem hafa langan afgreiðslutíma, á milli 0,41 og 0,60 fyrir vörur sem hafa miðlungs afgreiðslutíma og á milli 0,61 og 1,00 fyrir vörur sem hafa stuttan afgreiðslutíma. Fyrir frekari upplýsingar, sjá [Stuðpúðarsnið og stig](ddmrp-buffer-profile-and-levels.md).
    - **Breytileikastuðull** – Tilgreindu þátt (sem aukastaf á milli 0 og 1) til að stjórna áhrifunum sem mismunandi eftirspurn ætti að hafa þegar lágmarksbirgðastaða er reiknuð fyrir vörur í þessum þekjuflokki. Almennt séð, því breytilegri sem eftirspurn vöru er, því hærri ætti breytileikastuðull hans að vera. Hærri breytileikastuðull gefur af sér hærra lágmarksbirgðir. DDMRP aðferðafræði mælir með gildi á milli 0,00 og 0,40 fyrir vörur sem hafa litla breytileika, á milli 0,41 og 0,60 fyrir vörur sem hafa miðlungs breytileika og á milli 0,61 og 1,00 fyrir vörur sem hafa mikla breytileika. Fyrir frekari upplýsingar, sjá [Stuðpúðarsnið og stig](ddmrp-buffer-profile-and-levels.md).
    - **Lágm., hámark og endurpöntunarpunktatímabil** - Tilgreindu hversu oft á að reikna biðminni gildi (*Daglega* eða *Vikulega*).

1. Á **Annað** flipa, í **Dagleg meðalnotkun** kafla, stilltu eftirfarandi reiti:

    - **Dagleg meðalnotkun miðað við** – Veldu hvaða tímabil útreikningur á meðaltali daglegrar notkunar (ADU) ætti að byggja á. Veljið eitt af eftirfarandi gildum:

        - *Fortíð* – Horfðu aðeins á fyrri notkun fyrir þann fjölda daga sem tilgreindir eru í **Síðasta tímabil (dagar)** sviði. ADU er reiknað sem heildareftirspurn eftir vöru á útreikningstímabilinu (í birgðaeiningum) deilt með fjölda daga á útreikningstímabilinu.
        - *Áfram* – Horfðu aðeins á áætluð framtíðarnotkun (þar á meðal spár) fyrir þann fjölda daga sem tilgreindir eru í **Framvirkt tímabil (dagar)** sviði. ADU er reiknað sem heildareftirspurn eftir vöru á útreikningstímabilinu (í birgðaeiningum) deilt með fjölda daga á útreikningstímabilinu. 
        - *Blandað* – Horfðu á bæði fortíð og framtíðarnotkun. Stillingar fyrir **Síðasta tímabil (dagar)** sviði, the **Framvirkt tímabil (dagar)** reit og blöndunarvalkostir eiga allir við. 

            *Blandað ADU* = (\[*Fyrri vigtun* ×*Fyrri ADU*\] + \[*Áframvigtun* ×*Áfram ADU*\]) ÷ (*Fyrri vigtun* + *Áframvigtun*)

    - **Síðasta tímabil (dagar)** – Sláðu inn fjölda liðinna daga (til og með deginum í dag) sem kerfið ætti að hafa í huga þegar það reiknar út ADU hluta í þessum þekjuhópi. Þessi stilling á aðeins við þegar **Dagleg meðalnotkun miðað við** reiturinn er stilltur á *Fortíð* eða *Blandað*.
    - **Framvirkt tímabil (dagar)** – Sláðu inn fjölda framtíðardaga (frá deginum í dag og fram að tilgreindum degi) sem kerfið ætti að hafa í huga þegar það reiknar út ADU fyrir hluti í þessum þekjuhópi. Þessi stilling á aðeins við þegar **Dagleg meðalnotkun miðað við** reiturinn er stilltur á *Áfram* eða *Blandað*.
    - **Hlutfallsleg þyngd liðins tímabils fyrir blönduð daglega meðalnotkun** – Sláðu inn þyngdina (sem hlutfall) sem á að gilda um síðasta tímabil þegar blandað ADU er reiknað út. Þessi stilling á aðeins við þegar **Dagleg meðalnotkun miðað við** reiturinn er stilltur á *Blandað*.
    - **Hlutfallslegt vægi framvirkt tímabils fyrir blönduð meðaltal daglegrar notkunar** – Sláðu inn þyngdina (sem hlutfall) sem á að gilda um framvirka tímabilið þegar blandað ADU er reiknað. Þessi stilling á aðeins við þegar **Dagleg meðalnotkun miðað við** reiturinn er stilltur á *Blandað*.

1. Fyrir alla aðra flipa og reiti skaltu slá inn ítarlegar stillingar sem eru notaðar til að reikna út kröfur fyrir hlutina sem eru tengdir þessum þekjuhópi.

### <a name="set-an-item-as-a-decoupling-point"></a>Stilltu hlut sem aftengingarpunkt

Til að stilla hlut sem aftengingarpunkt skaltu fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finndu og veldu útgefið atriði sem þú vilt setja upp fyrir DDMRP.
1. Á aðgerðarrúðunni, á **Áætlun** flipa, veldu **Vöruumfjöllun**.
1. Á **Vöruumfjöllun** síðu, gætu nokkrar vöruþekjufærslur þegar verið skráðar, sem hver um sig á við um mismunandi samsetningu geymslu- og vörustærða. Þú getur valið fyrirliggjandi vöruþekjufærslu sem á við um víddir þar sem þú vilt stofna aftengingarpunkt. Að öðrum kosti geturðu valið **Nýtt** á aðgerðarrúðunni til að búa til nýja vöruþekjufærslu.
1. Settu upp vöruþekjuskrá eins og venjulega. Að minnsta kosti verður þú að tilgreina síðuna og vöruhús þar sem aftengingarpunkturinn á við.
1. Á meðan viðeigandi skráning er enn valin skaltu velja **Almennt** flipa.
1. Veldu **Notaðu sérstakar stillingar** gátreit.
1. Stilltu **Umfjöllunarhópur** reit til umfjöllunarhóps sem er settur upp til að búa til aftengingarpunkta (eins og lýst er í fyrri hlutanum).
1. Hluturinn er nú stilltur sem aftengingarpunktur. Venjulega, þegar þú notar DDMRP, muntu einnig stilla stillingar hér sem hafa áhrif á biðminni og endurpöntunarmagn. Hins vegar geturðu lokið þeirri stillingu síðar. Fyrir frekari upplýsingar um stillingarnar, sjá [Settu upp biðminni fyrir hlut aftengingarpunkts](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Til að skipuleggja hluti sem eru ekki aftengingarpunktar skaltu fylgja sömu skrefum og þú fylgir þegar staðlað efnisþörf áætlanagerð (MRP) er notuð.
