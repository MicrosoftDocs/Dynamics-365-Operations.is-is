---
title: Birgðavirðisskýrslur
description: Þetta efnisatriði útskýrir hvernig á að setja upp, búa til og nota birgðavirðisskýrslur. Þessar skýrslur veita upplýsingar um efnislegt og fjárhagslegt magn og magn birgða þinna.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 4f710ff308bac42a284cd506143dd0ae21ff2ec7
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8676160"
---
# <a name="inventory-value-reports"></a>Birgðavirðisskýrslur

[!include [banner](../includes/banner.md)]

Birgðavirðisskýrslur veita upplýsingar um efnislegt og fjárhagslegt magn og fjárhæðir birgða þinna. Þú getur skoðað skýrslurnar á marga mismunandi vegu. Til dæmis er hægt að sýna samtölur eða færslur, eða sía eftir hlutum eða tímabili. Þú getur skoðað kostnað seldra vara (COGS) gildi eða vinnu í vinnslu (WIP) gildi og stillt aðra valkosti.

Birgðavirðisskýrslur gera þér kleift að framkvæma eftirfarandi verkefni:

- Gerðu afstemmingu á milli aðalbókar og birgða.
- Skoðaðu birgðahald og verðmæti fyrir tiltekið tímabil.
- Búðu til skýrslustillingar sem eru sérsniðnar að ákveðnum tilgangi.
- Vistaðu skýrslustillingar þannig að hægt sé að nota þær mörgum sinnum.
- Bættu við sviðum til að sía gögn þegar þú keyrir skýrslu.

## <a name="types-of-inventory-value-report"></a>Tegundir skýrslu um birgðavirði

Það eru tvær tegundir af skýrslum um birgðavirði: **Birgðaverðmæti** (staðlaða skýrslan) og **Geymsla birgðavirðisskýrslu**.

### <a name="standard-inventory-value-report"></a>Skýrsla um staðlað birgðavirði

Staðallinn **Birgðaverðmæti** skýrsla er einföld skýrsla sem gerir þér kleift að velja upplýsingarnar sem fylgja með og sýna þær síðan á skjánum. Það bjargar ekki niðurstöðunum. Það býður heldur ekki upp á gagnvirka eiginleika til að sía, bora niður, vafra eða flytja út. Af þessum ástæðum mælum við með að þú notir **Geymsla birgðavirðisskýrslu** tilkynna þess í stað í flestum tilfellum.

### <a name="inventory-value-report-storage-report"></a>Geymsluskýrsla um birgðaverðmæti

The **Geymsla birgðavirðisskýrslu** skýrsla veitir úttak annað hvort sem gagnvirka síðu í Microsoft Dynamics 365 Supply Chain Management eða sem útflutt skjal á einu af nokkrum sniðum.

Þegar þú skoðar skýrsluna í vafranum þínum eru dálkar og samanlagðri stöðu er breytt á kvikan hátt, miðað við skipulagið sem þú hefur grunnstillt. Þú getur flokkað niðurstöðurnar, síað þær, borað niður í gögnin og fleira.

Niðurstöður skýrslunnar eru vistaðar í gagnaeiningu **Birgðavirðis**. Þar af leiðandi getur þú síað og flutt niðurstöðurnar út á sniði eins og á CSV-skrá eða Microsoft Excel-sniði.

The **Geymsla birgðavirðisskýrslu** skýrsla er gagnleg þegar úttakið inniheldur margar línur. Til dæmis hefur þú 50.000 vörur og 300 verslanir hafa verið stofnaðar sem vöruhús. Í þessu tilfelli, ef þú biður um lokastöður birgða eftir vöru, síðu og vöruhúsi, mun úttakið innihalda margar línur.

> [!NOTE]
> The **Geymsla birgðavirðisskýrslu** skýrsla inniheldur ekki undirsamtölur sem eru skilgreindar í skýrsluútlitinu. Það inniheldur heldur ekki stöður í aðalbók, jafnvel þótt þessar stöður séu skilgreindar í skýrsluútlitinu. Afstemming við Fjárhag verður að fara fram með því að nota prófjöfnuð. Hins vegar staðallinn **Birgðaverðmæti** skýrslan inniheldur þessar undirsamtölur og stöður.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Kveiktu eða slökktu á geymslueiginleika birgðavirðisskýrslu

Frá og með Supply Chain Management útgáfu 10.0.25 er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að *Geymsla birgðavirðisskýrslu* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a> Skilgreindu birgðagildisskýrslustillingar

Nota **Birgðavirðisskýrslur** síðu til að setja upp innihaldið sem er innifalið í mismunandi gerðum birgðavirðisskýrslu. Þú getur skilgreint hvaða fjölda skýrslugerða sem er. Í hvert sinn sem þú býrð til aðra hvora tegund birgðavirðisskýrslu velurðu skýrslugerð.

1. Fara til **Kostnaðarstjórnun \> Uppsetning reikningsskilaaðferða birgða \> Birgðavirðisskýrslur**.
1. Fylgið einu af eftirfarandi skrefum:

    - Til að breyta fyrirliggjandi skýrslu velurðu hana á listaglugganum og velur síðan **Breyta** á aðgerðasvæðinu.
    - Til að búa til nýja skýrslu skaltu velja **Nýtt** á aðgerðasvæðinu.

1. Í haus nýju eða valda skýrslunnar skaltu stilla eftirfarandi reiti:

    - **auðkenni** – Sláðu inn stutt auðkenni fyrir skýrsluna. Þetta gildi verður að vera einstakt meðal allra birgðagildisskýrslustillinga. Ekki er hægt að breyta því eftir að þú hefur vistað nýja stillingu.
    - **Nafn** – Sláðu inn lýsandi heiti fyrir skýrsluna.

1. Ef þú ert að búa til nýja skýrslustillingu skaltu velja **Vista** á aðgerðarrúðunni til að gera þá reiti sem eftir eru tiltækir.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Dagsetningarbil** – Veldu fyrirfram skilgreint dagsetningarbil. Þú getur hnekið þessu dagsetningarbili þegar þú keyrir skýrsluna.
    - **Svið** – Veldu annað hvort *Birtingardagur* eða *Viðskiptatími*, allt eftir dagsetningu og tíma sem ætti að nota þegar færslur eru sóttar fyrir skýrsluna.
    - **Málsett** – Veldu sett af víddum til að keyra gögnin fyrir. (Værðirnar eru skilgreindar í aðalbókinni.) Til dæmis gætir þú keyrt gögnin fyrir *Aðalreikningur* eða fyrir *Aðalreikningur + Viðskiptaeining*. Víddarsettið sem þú velur má ekki hafa fleiri en tvær víddir. Fyrir frekari upplýsingar, sjá [Fjárhagsvíddarsett](../../finance/general-ledger/financial-dimension-sets.md).

1. Á **Dálkar** Flýtiflipi, stilltu eftirfarandi reiti. Þessir reitir stjórna dálkunum sem skýrslan þín inniheldur og hvaða gagnategundir þessir dálkar innihalda.

    - **Birgðir** – Stilltu þennan valkost á *Já* til að sýna birgðagildin. Þú getur síðan samræmt þessi gildi við stöður fjárhagsreiknings.
    - **WIP** – Stilltu þennan valkost á *Já* til að sýna WIP gildin. Þú getur síðan samræmt þessi gildi við WIP reikningsjöfnuð í fjárhag. Þegar þú stillir þennan valkost á *Já*, mun skýrslan aðeins sýna líkamlegt magn og magn birgða sem hafa WIP stöðu. Framleiðslupantanir sem hafa WIP stöðu hafa verið tíndar eða tilkynntar sem lokið, en þeim hefur ekki verið lokið.
    - **Frestað COGS** – Stilltu þennan valkost á *Já* til að birta dálk sem sýnir efnislegt magn og magn birgða fyrir frestað COGS. Frestað COGS er sýnt með því að nota líkamlegt magn og magn, vegna þess að það vegur upp á móti magni og magni fylgiseðla.
    - **COGS** – Stilltu þennan valkost á *Já* til að birta dálk sem sýnir fjárhagslegt magn og upphæðir fyrir COGS. COGS er sýnt með því að nota fjárhagslegt magn og fjárhæðir, vegna þess að það jafnar upp á reikningsmagn og upphæðir.
    - **Hagnaður og tap** – Stilltu þennan valkost á *Já* til að birta dálk sem sýnir fjárhæðina sem var bókuð á rekstrarreikninga fyrir birgðahald.
    - **Prentaðu uppsöfnuð reikningsgildi til samanburðar** – Stilltu þennan valkost á *Já* til að birta dálk sem sýnir stöðu fjárhagsreiknings. Þannig þarftu ekki að athuga jafnvægið á slóðinni. Þessi valkostur virkar aðeins með staðlinum **Birgðaverðmæti** skýrslu, ekki með **Geymsla birgðavirðisskýrslu** skýrslu. Eftir að þú stillir þennan valkost á *Já*, þú verður að nota eftirfarandi reiti til að tilgreina hvern fjárhagsreikning sem þú vilt skrá, allt eftir **Fjárhagsstaða** valkostir sem þú hefur virkjað.

        > [!NOTE]
        > Ef þú velur a *alls* gera grein fyrir einhverjum af þessum reitum, bæði upphæð hvers birgðareiknings sem er innifalin í heildarreikningnum og upphæð heildarreiknings verða sýnd.

        - **Birgðareikningur** – Tilgreindu fjárhagsreikninginn til að sýna birgðaupplýsingar fyrir. (Bæði **Birgðir** valmöguleika og **Prentaðu uppsöfnuð reikningsgildi til samanburðar** valkostur verður að vera stilltur á *Já* .)
        - **WIP reikningur** – Tilgreindu fjárhagsreikninginn til að sýna WIP upplýsingar fyrir. (Bæði **WIP** valmöguleika og **Prentaðu uppsöfnuð reikningsgildi til samanburðar** valkostur verður að vera stilltur á *Já* .)
        - **Frestað COGS reikningur** – Tilgreindu fjárhagsreikninginn til að sýna frestað COGS upplýsingar fyrir. (Bæði **Frestað COGS** valmöguleika og **Prentaðu uppsöfnuð reikningsgildi til samanburðar** valkostur verður að vera stilltur á *Já* .)
        - **COGS reikning** – Tilgreindu fjárhagsreikninginn til að sýna COGS upplýsingar fyrir. (Bæði **COGS** valmöguleika og **Prentaðu uppsöfnuð reikningsgildi til samanburðar** valkostur verður að vera stilltur á *Já* .)

    - **Taktu saman líkamleg og fjárhagsleg gildi** – Stilltu þennan valkost á *Já* til að birta dálk sem sýnir heildarbirgðamagn og birgðaupphæð (yfirlit yfir bæði efnisleg og fjárhagsleg birgðagildi). Ef þessi valkostur er stilltur á *Nei*, mun skýrslan sýna bæði efnisleg og fjárhagsleg birgðagildi.
    - **Hafa ekki bókað í höfuðbók** Stilltu þennan valkost á *Já* til að birta dálk sem sýnir þær færslur sem aldrei voru bókaðar í fjárhag. Færslur fyrir eftirfarandi tegundir vara eru hugsanlega ekki bókaðar í fjárhag:

        - Mótteknar og ekki enn reikningsfærðar vörur þegar **Bókaðu efnislegar birgðir** valkostur er hreinsaður fyrir viðkomandi vörulíkanaflokk.
        - Mótteknar og ekki enn reikningsfærðar vörur þegar **Bókaðu innhreyfingu vöru í höfuðbók** valkostur er hreinsaður á **Vörukvittun** Flýtiflipi á **Almennt** flipi á **Færibreytur viðskiptaskulda** síða (**Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**).

    - **Reiknaðu meðaleiningakostnað** – Stilltu þennan valkost á *Já* til að birta dálk sem sýnir meðaleiningakostnað. Meðaleiningakostnaður er heildarupphæð deilt með heildarmagni.
    - **Heildarmagn og verðmæti** – Stilltu þennan valkost á *Já* til að birta dálka sem sýna heildarmagn efnislegra birgða (og fjárhagslegt magn) og heildarupphæð efnislegra birgða (og fjárhagsupphæða). Þú getur stillt þennan valkost á *Já* aðeins ef **Taktu saman líkamleg og fjárhagsleg gildi** valkostur er stilltur á *Nei*.
    - **Birgðastærðir** – Í þessu rist, veldu **Útsýni** gátreit fyrir hverja vídd sem þú vilt sýna í skýrslunni. Aðeins stærðir þar sem **Fjárhagsskrá** valkosturinn er virkur mun sýna gildi á skýrslunni. Aðrar stærðir sýna aðeins auða dálka. Fyrir þær stærðir sem þú velur að sýna geturðu valið **Samtals** gátreit til að innihalda samtölur líka.
    - **Auðkenni auðlindar** – Stilltu **Útsýni** valmöguleika til *Já* til að birta dálk sem auðkennir hlutinn fyrir hverja línu. Stilltu **Samtals** valmöguleika til *Já* að taka með heildartölur líka. Það fer eftir tegund hlutar sem er skráð í hverri röð, dálkurinn sýnir eina af eftirfarandi tegundum upplýsinga:

        - **Efni** – Dálkurinn sýnir`ItemID` reitgildi fyrir viðkomandi efnisskrá.
        - **Vinnuafl** – Dálkurinn sýnir`WorkCenterID` reitgildi fyrir viðkomandi vinnuaflsskrá.
        - **Óbeinn kostnaður** – Dálkurinn sýnir`CodeID` reitgildi fyrir viðkomandi kostnaðarskrá.

        Ef **Útsýni** valkostur er stilltur á *Nei* fyrir bæði **Auðkenni auðlindar** sviði og **Auðlindahópur** reit, muntu sjá aðeins heildarbirgðagildi sem er byggt á birgðavíddunum sem þú valdir.

    - **Auðlindahópur** – Stilltu **Útsýni** valmöguleika til *Já* til að birta dálk sem auðkennir tilfangahópinn fyrir hverja línu. Stilltu **Samtals** valmöguleika til *Já* að taka með heildartölur líka. Það fer eftir tegund hlutar sem er skráð í hverri röð, dálkurinn sýnir eina af eftirfarandi tegundum upplýsinga:

        - **Efni** – Dálkurinn sýnir`ItemGroup` reitgildi fyrir viðkomandi efnisskrá.
        - **Vinnuafl** – Dálkurinn sýnir`WorkcenterGroup` reitgildi fyrir viðkomandi vinnuaflsskrá.
        - **Óbeinn kostnaður** – Dálkurinn sýnir`CostGroup` reitgildi fyrir viðkomandi kostnaðarskrá. (The`CostGroupType` gildi verður að vera *Óbeint* .)

        Ef **Útsýni** valkostur er stilltur á *Nei* fyrir bæði **Auðkenni auðlindar** sviði og **Auðlindahópur** reit, muntu sjá aðeins heildarbirgðagildi sem er byggt á birgðavíddunum sem þú valdir.

1. Á **Raðir** Flýtiflipi, stilltu eftirfarandi reiti. Þessir reitir gera þér kleift að bæta samsvarandi WIP-tengdum undirköflum við skýrsluna eða fjarlægja þá.

    - **Efni** – Stilltu þennan valkost á *Já* að sýna upplýsingar um efni. *Efni* er sjálfgefin tilfangagerð vegna þess að efni verður að vera með í öllum skýrslustillingum til að búa til áreiðanlegt úttak.
    - **Vinnuafl** – Stilltu þennan valkost á *Já* til að sýna launakostnað við WIP.
    - **Óbeinn kostnaður** – Stilltu þennan valkost á *Já* til að sýna óbeinan kostnað við WIP.
    - **Bein útvistun** – Stilltu þennan valkost á *Já* til að sýna beinan útvistunarkostnað WIP. Þessar upplýsingar eru gagnlegar fyrir undirverktaka.
    - **Detail Level** – Veldu útsýnisvalkost fyrir skýrsluna:

        - *Viðskipti* - Skoðaðu allar viðeigandi færslur á skýrslunni. Athugaðu að þú gætir fundið fyrir frammistöðuvandamálum þegar þú skoðar skýrslur sem innihalda mikið magn af færslum. Þess vegna, ef þú vilt nota þennan útsýnisvalkost, mælum við með því að þú notir **Geymsla birgðavirðisskýrslu** skýrslu.
        - *Samtals* - Skoðaðu heildarniðurstöðuna.

    - **Hafa upphafsjöfnuð með** – Stilltu þennan valkost á *Já* til að sýna upphafsjafnvægið. Þessi valkostur er aðeins í boði þegar **Upplýsingar stig** reiturinn er stilltur á *Viðskipti*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Búðu til geymsluskýrslu um birgðagildi

Fylgdu þessum skrefum til að búa til og geyma **Geymsla birgðavirðisskýrslu** skýrslu.

1. Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla skýrslu fyrir birgðavirði í geymslu**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í **Birgðaverðmæti** valmynd, á **Færibreytur** Flýtiflipi, stilltu eftirfarandi reiti:

    - **Nafn** – Sláðu inn einstakt heiti fyrir skýrsluna.
    - **auðkenni** – Veldu [Uppsetning birgðavirðisskýrslu](#report-configuration) til að nota fyrir skýrsluna. Uppsetningin setur valmöguleika fyrir dálkana og raðir sem verða með í skýrslunni þinni.
    - **Dagsetningarbil** – Notaðu reitina í þessum hluta til að skilgreina hvaða færslur eru með í skýrslunni. Til að tilgreina dagsetningabilið geturðu annað hvort valið forstillt svið (miðað við hvenær skýrslan var búin til) í svæðinu **Kóði dagsetningabils** eða valið ákveðin dagsetningar í reitunum **Frá dagsetningu** og **Til dagsetningar**.

1. Á **Skrár til að hafa með** Flýtiflipi, settu upp síur og takmarkanir til að skilgreina hvaða gögn eru innifalin í skýrslunni. Veldu **Sía** til að opna staðlaðan fyrirspurnarglugga, þar sem hægt er að skilgreina valviðmið, flokkunarviðmið og sameiningar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Supply Chain Management. Allar þessar síur verða notaðar á birgðafærslurnar en ekki á fjárhagsstöðu. Hafðu þessa hegðun í huga þegar þú setur upp síurnar þínar. Annars gætirðu séð misræmi á milli birgða og fjárhags.
1. Á flýtiflipanum **Keyra í bakgrunni** skaltu tilgreina hvernig, hvenær og hversu oft á að búa skýrsluna til. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.

    > [!NOTE]
    > Þessi skýrsla er alltaf keyrð sem hluti af runuvinnslu.

1. Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum.

Eftir að runuvinnslunni er lokið birtist skýrslan á síðu **Skýrslu um birgðarvirði í geymslu**. Hugsanlega verður að endurhlaða síðuna til að skýrslan birtist.

> [!IMPORTANT]
> Í völdum uppsetningu birgðavirðisskýrslu gætirðu fengið ranga upphafsstöðu ef þú velur sömu dagsetningu í báðum **Frá dags** sviði og **Hingað til** reit, og ef þú stillir líka **Hafa upphafsjöfnuð með** valmöguleika til *Já*.

## <a name="explore-an-inventory-value-report-storage-report"></a>Skoðaðu geymsluskýrslu um birgðagildi

Eftir að þú hefur búið til skýrslu geturðu opnað og skoðað hana hvenær sem er með því að fylgja þessum skrefum.

1. Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla skýrslu fyrir birgðavirði í geymslu**.
1. Veldu skýrslu á listanum. Síðan sýnir upplýsingar um [Uppsetning birgðavirðisskýrslu](#report-configuration) sem var notað til að búa til valda skýrslu.
1. Á aðgerðarrúðunni velurðu **Skoða smáatriði** til að sýna innihald skýrslunnar.
1. Skoðaðu skýrsluna með því að fylgja einhverjum af þessum skrefum:

    - Eins og á við um flestar staðlaðar síður í Supply Chain Management geturðu valið næstum hvaða dálk sem er til að raða eða sía hnitanetið eftir gildunum í þeim dálki.
    - Notaðu svæðið **Sía** til að sía skýrsluna eftir hvaða gildi sem er í nokkrum tiltækum dálkum.
    - Notaðu valmyndina Skoða (fyrir ofan svæðið **Sía**) til að vista og hlaða inn eftirlætis samsetningum flokkunar- og síuvalkosta.

## <a name="export-an-inventory-value-report-storage-report"></a>Flytja út birgðavirðisskýrslu geymsluskýrslu

Hver skýrsla sem þú býrð til er geymd í gagnaeiningunni **Birgðavirði**. Þú getur notað staðlaða eiginleika gagnastjórnunar fyrir Supply Chain Management til að flytja út gögn frá þessari einingu til allra studdra gagnasniða, eins og CSV- eða Excel-sniða.

Eftirfarandi dæmi sýnir hvernig á að flytja út **Geymsla birgðavirðisskýrslu** skýrslu.

1. Opnaðu **Kerfisstjórnun \> Vinnusvæði \> Gagnastjórnun**.
1. Í hlutanum **Flytja inn / Flytja út** velurðu reitinn **Flytja út**.
1. Á síðunni **Útflutningur** sem birtist seturðu upp útflutningsverkið. Færið fyrst inn heiti hóps fyrir verkið.
1. Í hlutanum **Valdar einingar** velurðu **Bæta við einingu**.
1. Í svarglugganum sem birtist, skal velja eitt af eftirfarandi svæðum:

    - **Heiti einingar** – Veldu *Birgðarvirði*.
    - **Markmiðsgagnasnið** - Veldu sniðið sem á að flytja gögn út á.

1. Smelltu á **Bæta við** til að bæta við nýju línunni og smelltu síðan á **Loka** til að loka glugganum.
1. Venjulega muntu flytja út eina skýrslu í einu. Til að flytja út eina skýrslu skaltu setja upp síu fyrir línuna sem þú varst að bæta við í svarglugganum **Fyrirspurn**. Á þennan hátt geturðu skilgreint hvaða skýrslu frá einingunni **Birgðavirði** er innifalinn í útflutningi þínum. Fylgdu þessum skrefum til að stilla eftirfarandi síuvalkosti til að flytja út eina skýrslu:

    1. Veldu **Bæta við** til að bæta við röð á flipanum **Svið**.
    2. Stilltu svæðið **Tafla** á *Birgðavirði*.
    3. Stilltu svæðið **Afleidd tafla** á *Birgðavirði*.
    4. Stilltu svæðið **Svæði** á svæðið sem þú vilt sía eftir. Yfirleitt notarðu svæðið **Keyrsluheiti** og/eða svæðið **Keyrslutími**.
    5. Stilltu svæðið **Skilyrði** á gildi sem þú vilt leita að í valda svæðinu. (Ef þú valdir svæðið **Keyrsluheiti** í fyrra skrefi verður þetta gildi heiti skýrslunnar. Ef þú valdir svæðið **Keyrslutími** verður það tíminn sem skýrslan var búin til.)
    6. Bættu við eins mörgum línum við flipann **Svið** eins og þú þarft, þar til þú hefur borið einkvæm kennsl á skýrsluna sem þú ert að leita að.

1. Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.
1. Veldu **Vista** til að vista uppsetningu á útflutningi.
1. Á flipanum **Valkostir útflutnings** velurðu **Flytja út núna** til að búa til útflutningsskrána.
1. Á **Yfirlitssíðu keyrslu** sem birtist geturðu skoðað stöðu útflutningsverksins þíns og lista yfir allar einingar sem voru fluttar út. Í hlutanum **Vinnslustaða einingar** velurðu **Birgðavirði** á listanum og smellir á **Hlaða niður skrá** til að hlaða niður gögnum sem flutt voru út frá þeirri einingu.

Nánari upplýsingar um hvernig á að nota gagnastjórnun til að flytja út gögn er að finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

## <a name="generate-a-standard-inventory-value-report"></a>Búðu til staðlaða skýrslu um birgðavirði

Notaðu eftirfarandi aðferð til að búa til staðal **Birgðaverðmæti** skýrslu.

1. Fara til **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Birgðabókhald - stöðuskýrslur \> Birgðaverðmæti**.
1. Í **Birgðavirðisskýrsla** valmynd, á **Færibreytur** Flýtiflipi, stilltu eftirfarandi reiti:

    - **Nafn** – Sláðu inn einstakt heiti fyrir skýrsluna.
    - **auðkenni** – Veldu [Uppsetning birgðavirðisskýrslu](#report-configuration) til að nota fyrir skýrsluna. Uppsetningin setur valmöguleika fyrir dálkana og raðir sem verða með í skýrslunni þinni.
    - **Dagsetningarbil** – Notaðu reitina í þessum hluta til að skilgreina hvaða færslur eru með í skýrslunni. Til að tilgreina dagsetningabilið geturðu annað hvort valið forstillt svið (miðað við hvenær skýrslan var búin til) í svæðinu **Kóði dagsetningabils** eða valið ákveðin dagsetningar í reitunum **Frá dagsetningu** og **Til dagsetningar**.

1. Á **Skrár til að hafa með** Flýtiflipi, settu upp síur og takmarkanir til að skilgreina hvaða gögn eru innifalin í skýrslunni. Veldu **Sía** til að opna staðlaðan fyrirspurnarglugga, þar sem hægt er að skilgreina valviðmið, flokkunarviðmið og sameiningar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Supply Chain Management.
1. Á flýtiflipanum **Keyra í bakgrunni** skaltu tilgreina hvernig, hvenær og hversu oft á að búa skýrsluna til. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum. Skýrslan birtist.

## <a name="reading-inventory-value-reports"></a>Að lesa skýrslur um birgðavirði

Þessi hluti veitir nokkrar leiðbeiningar um hvernig eigi að lesa og skilja skýrslu um birgðavirði.

Aðfangakeðjustjórnun styður eftirfarandi tvö mikilvæg hugtök sem tengjast birgðastöðu:

- **Fjárhagslegt uppfært** – Þetta hugtak gefur til kynna að birgðafærslurnar séu þegar reikningsfærðar. Fyrir framleiðslupantanir gefur það til kynna lok framleiðslupöntunar.
- **Líkamlega uppfært** – Þetta hugtak gefur til kynna að birgðafærslurnar hafi ekki enn verið reikningsfærðar, en þær hafa verið mótteknar eða sendar. Fyrir framleiðslupantanir gefur það til kynna að efni hafi verið tínt eða framleiðslupöntun hefur verið tilkynnt sem lokið.

Þegar þú skilur þessi tvö hugtök ætti að vera auðvelt að skilja eftirfarandi dálka í skýrsluúttakinu:

- **Birgðir: Fjármagn** – Magnið sem hefur verið uppfært fjárhagslega.
- **Birgðir: Fjárhæð** – Upphæðarvirði birgða sem hefur verið fjárhagslega uppfært.
- **Birgðir: Líkamlegt magn sett inn** – Magnið sem hefur verið líkamlega uppfært.
- **Birgðir: Líkamleg upphæð skráð** – Upphæðargildi birgða sem hefur verið líkamlega uppfært.
- **Birgðir: Líkamlegt magn ekki skráð** – Magnið sem hefur birgðafærslur en hefur ekki verið bókað í fjárhag. Til dæmis ertu með vörulíkanahóp þar sem **Bókaðu efnislegar birgðir** og **Bókaðu fjárhagsskrá** valkostir eru hreinsaðir og þú ert með hlut sem er tengdur við þann hóp. Þú býrð síðan til innkaupapöntun, færð hana og reikningsfærðir. Á þessum tímapunkti, ef þú skoðar birgðavirðisskýrsluna fyrir vöruna, muntu sjá að magnið og verðmæti innkaupapöntunarinnar eru sýnd í **Birgðir: Líkamlegt magn ekki skráð** og **Birgðir: Líkamleg upphæð ekki bókuð** dálkar.
- **Birgðir: Líkamleg upphæð ekki bókuð** – Þú getur sett upp skýrslurnar þínar þannig að þær sýni óbókaðar upphæðir. Hins vegar, ef þú ert að nota skýrsluna fyrir birgðaafstemmingu skaltu ekki nota þetta gildi. Annars er upphæðin ekki bókuð í fjárhag.
- **Birgðir: Magn** – Heildarmagn allra magndálka í skýrslunni.
- **Birgðir: Magn** – Heildarmagn allra upphæðadálka í skýrslunni. Þegar þú gerir birgðaafstemmingu skaltu ekki nota þennan dálk ef skýrslan þín inniheldur **Birgðir: Líkamleg upphæð ekki bókuð** dálki. Í þessu tilviki verður þú að útiloka **Birgðir: Líkamleg upphæð ekki bókuð** upphæð frá heildarupphæð.
- **Meðaleiningakostnaður** – Heildarupphæð deilt með heildarmagni.

Venjulega muntu nota birgðavirðisskýrslu til að skoða birgðaverðmæti og magn. Hins vegar sýnir skýrslan stundum ekki allar viðeigandi birgðavíddir. Ef þú sérð ekki stærðirnar sem þú býst við skaltu staðfesta eftirfarandi stillingar:

- Skoðaðu vörugeymslu- og rakningarvíddarhópana. Aðeins stærðir þar sem **Fjárhagsskrá** valkosturinn er virkur er hægt að sýna á skýrslunni.
- Fara til **Kostnaðarstjórnun \> Uppsetning reikningsskilaaðferða birgða \> Birgðavirðisskýrslur**, veldu skýrslustillinguna sem þú notaðir til að búa til skýrsluna og vertu viss um að nauðsynlegar birgðavíddir séu valdar í **Útsýni** dálki.

Til dæmis ertu með vöru sem hefur vörunúmerið *A0001*. Í geymsluvíddarhópnum er aðeins vefsvæðið virkt fyrir fjárhagslegar birgðir. Staðurinn og vöruhúsið eru bæði virkjuð fyrir efnislegar birgðir. Í rakningarvíddarhópnum er rununúmerið virkt fyrir efnislegar birgðir en ekki fyrir fjárhagslegar birgðir. Þú notar síðan skýrslustillingu þar sem svæði, vöruhús og lotunúmer eru öll valin. Þegar þú skoðar skýrsluna sérðu aðeins gildi fyrir síðuna. Dálkarnir fyrir vöruhús og lotunúmer eru auðir. Eins og þetta dæmi sýnir geta birgðavirðisskýrslur aðeins sýnt birgðavídd sem eru virkjuð fyrir fjárhagslegar birgðir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
