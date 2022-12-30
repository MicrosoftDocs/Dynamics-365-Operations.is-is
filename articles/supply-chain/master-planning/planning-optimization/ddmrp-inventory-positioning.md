---
title: Birgðastaðsetning
description: Þessi grein veitir upplýsingar um birgðastaða samkvæmt áætlun, sem felur í sér að auðkenna aftengingarpunkta í aðfangakeðjunni þinni, þar sem þú getur byggt upp birgðir á lager til að þjappa afhendingartími og draga úr áföllum í aðfangakeðjunni þinni.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689539"
---
# <a name="inventory-positioning"></a>Birgðastaðsetning

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Birgðastaða samkvæmt áætlun felur í sér að finna aftengingarpunktur í birgðakeðjunni þinni þar sem þú getur byggt upp birgðir á lager. Þessi aðferð er aðallega notuð til að þjappa afhendingartími og draga úr áföllum í aðfangakeðjunni. Það gerir þér kleift að draga úr „svipuáhrifunum“, vegna þess að breytileiki eftirspurnar berst ekki alla leið niður aðfangakeðjuna. (*Svipuáhrifin* vísa til þess hvernig litlar sveiflur í eftirspurn á smásölustigi geta valdið smám saman stærri sveiflum í eftirspurn á heildsölu-, dreifingar-, framleiðanda- og hráefnisbirgjastigi).

Birgðastaðsetning er fyrsta skrefið í eftirspurnardrifinni áætlunargerð tilfanga (DDMRP).

## <a name="inventory-positioning-for-manufacturing"></a>Staðsetning birgða fyrir framleiðslu

Í þessum hluta er dæmi sem sýnir hvernig á að taka ákvarðanir um staðsetningu birgða ef þú framleiðir dæmigerða koddavöru. Koddinn hefur fjölþrepa uppskrift, eins og sýnt er á eftirfarandi skýringamynd.

![Dæmi um fjölþrepa uppskriftir (BOM) fyrir kodda.](media/ddmrp-bom-example.png "Dæmi um fjölþrepa uppskriftir (BOM) fyrir kodda")

### <a name="choose-your-decoupling-points"></a>Veldu aftengingarpunkta

Þegar þú velur hvar þú setur aftengingarpunktana skaltu líta á eftirfarandi atriði fyrir hverja vöru í uppskrift sem viðmið:

- Ytri breytileiki
- Vogun og sveigjanleiki birgða
- Vernd mikilvægrar aðgerðar
- Tímaþol viðskiptavina
- Sýnileikatími sölupantana
- Mögulegur afhendingartími markaðssvæðis

Í dæminu um koddann kunna eftirfarandi ástæður að vera fyrir því að þú setjir fyrsta aftengingarpunkt við *svamphlutana*:

- Það er erfitt að finna uppsprettu þeirra efna sem eru notuð til að gera svampbútana og tiltækileiki er óstöðugt. Þar af leiðir er skilyrðum um *ytri breytileika* uppfyllt.
- Svamphlutana er hægt að skera í mörg mismunandi form og stærðir til að búa til svampinnlegg fyrir aðrar vörur sem þú framleiðir, til viðbótar við koddann. Því skilyrði um *Vogun og sveigjanleiki birgða* er fullnægt.

Þú gætir þá sett næsta aftengingarpunkt þinn við *efnissettið*, sem er fyrirfram sniðið koddaefni. Þú gætir valið þennan punkt af því að þú átt aðeins eina vél til að klippa niður efni. Því er skilyrðinu um *Vernd mikilvægrar aðgerðar* fullnægt.

Að lokum gætirðu sett síðustu aftengingarpunktinn á koddavöru fullunnu vörunnar. Þú gætir valið þetta atriði vegna þess að þú ert með mjög lágt *tímaþol viðskiptavina* á sölu, og vegna þess að *sýnileikatími sölupantana* er mjög stuttur. Þess vegna, þú vilja tryggja að þú hefur á hendi lagerbirgðir til að uppfylla komandi pantanir. Þú getur einnig stillt hærra verð með því að halda afhendingartími svona stuttum, sem er það sem viðmiðið fyrir *mögulegur afhendingartími markaðssvæðis* vísar til.

Samkvæmt þessari greiningu sýnir eftirfarandi skýringarmynd hvernig uppskrift koddans mun líta út. Gul birgðatákn merkja aftengingarpunkta.

![Dæmi um uppskrift með merktum aftengingarpunktum.](media/ddmrp-bom-decoupling-example.png "Dæmi um uppskrift með merktum aftengingarpunktum")

### <a name="calculate-your-decoupled-lead-time"></a>Reikna út aftengdan afhendingartíma

Þessi hluti sýnir hvernig eigi að reikna út nýja afhendingartíma eftir að þú hefur sett inn aftengingarpunkta.

Á eftirfarandi mynd fyrir koddadæmið sem byrjað var á hlutanum hér á undan eru afhendingartímar sýndir í gráum reitum efst til vinstri í hverri einingu uppskriftar. Kassar sem hafa rauða útlínur tilgreina vörur sem keyra uppsafnaðan afhendingartími (summa lengstu afhendingartíma á hverju uppskriftarstigi). Þessi afhendingartími er 21 dagur þegar þú byrjar frá grunni.

![Dæmi um uppskrift með afhendingartíma.](media/ddmrp-bom-lead-times-example.png "Dæmi um uppskrift með afhendingartíma")

Ef þú hins vegar notar aftengingarpunktana sem þú valdir áður verða aftengdu hlutirnir alltaf til á lager. Því munu þeir hafa afhendingartímann 0 (núll). Nýi afhendingartími fyrir koddann nú aðeins fimm dagar: tveir dagar til að kaupa tvinna og þrír dagar til að framleiða koddann. Þessi afhendingartími er þekktur *aftengdi afhendingartíminn*.

![Dæmi um aftengdan afhendingartíma.](media/ddmrp-bom-decoupled-lead-time-example.png "Dæmi um aftengdan afhendingartíma")

## <a name="strategic-inventory-positioning-in-a-retail-model"></a>Birgðastaða samkvæmt áætlun í smásölulíkani

Uppskriftir eru ekki úthreyfingar vegna þess að smásalar eru aðeins með fullunnar vörur á lager. Hins vegar geta smásalar enn notað DDMRP með því að stilla áætlaða staðsetningu birgða og stig öryggisbirgða sem byggjast á geymslustöðum í dreifikerfinu.

Eftirfarandi skýringarmynd sýnir dæmi um fyrirtæki sem er með dreifingarmiðstöð í Seattle og verslanir í Boston, Atlanta og Portland.

![Aftengingarpunktar miðað við staðsetningu í smásölulíkani.](media/ddmrp-retail-decoupl-points-example.png "Aftengingarpunktar miðað við staðsetningu í smásölulíkani")

Þú gætir ákveðið að flutningstími til að færa teppavöru á milli dreifingarmiðstöðvarinnar og verslana brjóti í bága við *tímaþol viðskiptavinar* þíns vegna þess að viðskiptavinir þínir búast við því að teppið sé til á lager þegar þeir koma í heimsókn. Í því tilviki er settur upp aftengingarpunktur fyrir teppið í hverri af verslununum þremur. Í hverri verslun eru mismunandi magn öryggisbirgða, miðað við endingartíma, eftirspurnarmynstur og svo framvegis.

## <a name="implement-inventory-positioning-in-dynamics-365-supply-chain-management"></a>Innleiða birgðarstöðu í Dynamics 365 Supply Chain Management

Í þessum kafla er lýst hvernig á að framkvæma áætlun um birgðarstaðsetningar í Microsoft Dynamics 365 Supply Chain Management.

### <a name="set-up-item-coverage-groups-that-create-decoupling-points"></a>Setja upp vöruþekjuflokka sem búa til aftengingarpunkta

Vörur verða aftengingarpunktar þegar þeir tilheyra þekjuflokki sem er stilltur með gildi **Þekjukóða** fyrir *Aftengingarpunkt*. Því er fyrsta skrefið í ferlinu að setja upp DDMRP að ákveða hvaða þekjuflokka þú verður að innleiða fyrir DDMRP áætlunina og búa þá síðan til með því að fylgja þessum skrefum.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> þekjuflokkar**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að búa til þekjuflokkur.
1. Sláðu inn upplýsingar sem auðkenna þekjuflokkinn og veldu síðan dagatalið sem á að nota.
1. Á flipanum **Almennt** er reiturinn **Þekjukóði** stilltur á *Aftengingarpunktur*. Þessi stilling mun valda því að allar vörur sem tilheyra þessum þekjuflokki verða meðhöndlaðir sem aftengingarpunktar fyrir DDMRP. Það virkjar einnig allar DDMRP-stillingar fyrir þennan flokk eins og lýst er síðar í þessu ferli.
1. Á flipanum **Annað** í hlutanum **DDMRP færibreytur** skal stilla eftirfarandi reiti:

    - **Stuðull afhendingartíma** – Tilgreindu stuðul (sem tugabrot á milli 0 og 1) til að stjórna því hvaða áhrif afhendingartími á að hafa þegar reiknað er út lágmark birgðastöðu fyrir vörur í þessum þekjuflokki. Almennt gildir að því lengri sem afhendingartími vöru er því lægri á afhendingartími hennar að vera. Lægri stuðull afhendingartíma hefur í för með sér lægra lágmark og hámark á birgðastöðu og leiðir því til minni og tíðari pantana. DDMRP aðferðafræðin mælir með gildi á bilinu 0,20 til 0,40 fyrir vörur sem hafa langan afhendingartími, á bilinu 0,41 til 0,60 fyrir vörur sem hafa meðallangan afhendingartíma og á bilinu 0,61 til 1,00 fyrir vörur sem hafa stuttan afhendingartíma. Frekari upplýsingar eru í [Forstilling öryggisbirgða og gildi](ddmrp-buffer-profile-and-levels.md).
    - **Breytileikastuðull** – Tilgreindu stuðul (sem tugabrot á milli 0 og 1) til að stjórna því hvaða áhrif breytileg eftirspurn á að hafa þegar reiknað er út lágmark birgðastöðu fyrir vöruna í þessum þekjuflokki. Almennt gildir að því breytilegri sem eftirspurn eftir vöru er því hærri ætti breytileikastuðullinn að vera. Meiri breytileikastuðull leiðir til hærra lágmarks birgðastöðu. Aðferðafræði DDMRP mælir með gildi á bilinu 0,00 til 0,40 fyrir vörur með lítinn breytileika, á bilinu 0,41 til 0,60 fyrir vörur með miðlungs breytileika og á bilinu 0,61 til 1,00 fyrir vörur með mikinn breytileika. Frekari upplýsingar eru í [Forstilling öryggisbirgða og gildi](ddmrp-buffer-profile-and-levels.md).
    - **Lágmark, hámark og endurpöntunarmark** - Tilgreinið hversu oft á að reikna öryggisbirgðir (*Daglega* eða *Vikulega*).

1. Á flipann **Annað**, í hlutanum **Meðaltal daglegrar notkunar**, skal stilla eftirfarandi reiti:

    - **Dagleg meðalnotkun samkvæmt** – Velja skal tímabil sem útreikningur daglegrar meðalnotkunar (ADU) skal byggjast á. Veljið eitt af eftirfarandi gildum:

        - *Fyrri notkun* – Skoðaðu aðeins fyrri notkun fyrir þann dagafjölda sem tilgreindur er í reitnum **Liðið tímabil (dagar)**. Dagleg notkun að meðaltali (ADU) er reiknuð sem heildareftirspurn eftir vörunni á tímabili útreiknings (í birgðaeiningum) deilt með fjölda daga á tímabili útreiknings.
        - *Framvirkt* – Skoðið aðeins áætlaða framtíðarnotkun (þ.m.t. spá) fyrir dagafjölda sem tilgreindur er í reitnum **Framvirkt tímabil (dagar)**. Dagleg notkun að meðaltali (ADU) er reiknuð sem heildareftirspurn eftir vörunni á tímabili útreiknings (í birgðaeiningum) deilt með fjölda daga á tímabili útreiknings. 
        - *Blandað* – Skoðaðu notkun í fortíð og framtíð. Stillingar fyrir reitinn **Liðið tímabil (dagar)**, reitinn **Framvirkt tímabil (dagar)** og blöndunarvalkostir eiga allir við. 

            *Blandað meðaltal daglegrar notkunar* = (\[*Fyrri vigtun* × *Fyrra meðaltal daglegrar notkunar*\] + \[*Framvirk vigtun* × *Framvirkt meðaltal daglegrar notkunar*\]) ÷ (*Fyrri vigtun* + *Framvirk vigtun*)

    - **Liðið tímabil (dagar)** - Sláðu inn fjölda undanfarinna daga (frá og með deginum í dag) sem kerfið ætti að hafa í huga við útreikning á daglega notkun að meðaltali í þessum þekjuflokki. Þessi stilling á aðeins við þegar reiturinn **Dagleg meðalnotkun samkvæmt** er stilltur á *Afturvirkt* eða *Blandað*.
    - **Framvirkt tímabil (dagar)** - Sláðu inn fjölda daga í framtíð (frá og með deginum í dag að tilgreindum degi) sem kerfið ætti að hafa í huga við útreikning á daglega notkun að meðaltali í þessum þekjuflokki. Þessi stilling á aðeins við þegar reiturinn **Meðaltal daglegrar notkunar miðað við** er stilltur á *Framvirkt* eða *Blandað*.
    - **Hlutfallslegt vægi liðins tímabils fyrir blandaða daglega meðalnotkun** – Sláðu inn þyngd (sem prósentuhlutfall) sem á við um undangengið tímabil þegar blandaða ADU er reiknað. Þessi stilling á aðeins við þegar reiturinn **Dagleg meðalnotkun samkvæmt** er stilltur á *Blandað*.
    - **Hlutfallslegt vægi ókomins tímabils fyrir blandaða daglega meðalnotkun** – Sláðu inn þyngd (sem prósentuhlutfall) sem á við framvirk tímabilið þegar blandaða ADU er reiknað. Þessi stilling á aðeins við þegar reiturinn **Dagleg meðalnotkun samkvæmt** er stilltur á *Blandað*.

1. Á öllum öðrum flipum og reitum eru færðar inn ítarlegar stillingar sem eru notaðar til að reikna út þörf á vörum sem eru tengdar þekjuflokknum.

### <a name="set-an-item-as-a-decoupling-point"></a>Velja atriði sem aftengingarpunkt

Til að stilla vöru sem aftengingarpunkt skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Finna og velja losað atriði sem á að setja upp fyrir DDMRP.
1. Á aðgerðasvæðinu, í flipanum **Áætlun** skal velja **Vöruþekja**.
1. Á síðunni **Vöruþekja** gætu þegar verið skráðar nokkrar þekjufærslur vöru, sem hver um sig á við um mismunandi samsetningu geymslu- og vöruvídda. Þú getur valið fyrirliggjandi þekjufærsla vöru sem á við um víddirnar þar sem þú vilt búa til aftengingarpunkt. Einnig er hægt að velja **Nýtt** á aðgerðasvæðinu til að búa til nýja vöruþekjufærslu.
1. Setja upp þekjufærsla vöru eins og venjulega. Að minnsta kosti verður að tilgreina svæðið og vöruhúsið þar sem aftengingarpunkturinn á við.
1. Á meðan viðeigandi færsla er enn valin skal velja flipann **Almennt**.
1. Merkið í gátreitinn **Nota sérstakar stillingar**.
1. Stilla reit **Þekjuflokkur** á þekjuflokk sem er settur upp til að búa til aftengingarpunkta (eins og lýst er í fyrri hluta).
1. Varan er nú stillt sem aftengingarpunktur. Venjulega, þegar þú notar DDMRP, munt þú einnig stilla stillingar hér sem hafa áhrif á stærðir öryggisbirgða og endurraða magni. Þú getur þó lokið þeirri stillingu síðar. Nánari upplýsingar um stillingar eru í [Setja upp öryggisbirgðir fyrir vöru aftengingarpunkts](ddmrp-buffer-profile-and-levels.md#set-up-buffers).

> [!NOTE]
> Til að áætla vörur sem ekki eru aftengingarpunktar skaltu fylgja sömu skrefum og þú fylgir þegar hefðbundin efnisþarfaáætlun (MRP) er notuð.
