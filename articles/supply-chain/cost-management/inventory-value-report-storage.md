---
title: Birgðavirðisskýrslur
description: Þessi grein útskýrir hvernig á að setja upp, búa til og nota birgðavirðisskýrslur. Þessar skýrslur gefa upplýsingar um efnislegar birgðir, fjárhagslegt magn og upphæðir.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: f97b5bd228c6f769438d50bb27950b8d8fbda3e8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334926"
---
# <a name="inventory-value-reports"></a>Birgðavirðisskýrslur

[!include [banner](../includes/banner.md)]

Birgðavirðisskýrslur gefa upplýsingar um efnislegar birgðir, fjárhagslegt magn og upphæðir. Hægt er að skoða skýrslurnar á marga mismunandi vegu. Til dæmis er hægt að sýna samtölur eða færslur eða sía eftir vörum eða tímabilum. Þú getur skoðað virði seldra vara (KSV) eða verka í vinnslu (VÍV) og stillt aðra valkosti.

Birgðavirðisskýrslur leyfa þér að framkvæma eftirfarandi verk:

- Gera afstemmingu milli fjárhags og birgða.
- Leita í lagerbirgðum og gildum að tilteknu tímabili.
- Stofna skýrsluskilgreiningar sem eru sniðnar að ákveðnum tilgangi.
- Vista skýrslustillingar svo hægt sé að nota þær mörgum sinnum.
- Bæta við sviðum til að sía gögn þegar skýrsla er keyrð.

## <a name="types-of-inventory-value-report"></a>Gerðir birgðavirðisskýrslna

Birgðavirðisskýrslur eru af tveimur gerðum: **Birgðavirðisskýrsla** (stöðluð skýrsla) og **Geymsla birgðavirðisskýrslu**.

### <a name="standard-inventory-value-report"></a>Stöðluð birgðavirðisskýrsla

Staðlaða **Birgðavirðisskýrslan** er einföld skýrsla sem gerir þér kleift að velja þær upplýsingar sem fylgja með og sýnir síðan þær upplýsingar á skjánum. Hún vistar ekki niðurstöðurnar. Það býður ekki heldur upp á gagnvirka eiginleika til að sía, kafa niður, fletta eða flytja út. Af þessum ástæðum er í flestum tilvikum mælt með því að nota **Geymsluskýrsla birgðavirðisskýrslu** í staðinn.

### <a name="inventory-value-report-storage-report"></a>Geymsluskýrsla birgðavirðisskýrslu

**Geymsluskýrsla birgðavirðisskýrslu** gefur úttak annaðhvort sem gagnvirk síða í Microsoft Dynamics 365 Supply Chain Management eða sem útflutt skjal á einu af mörgum sniðum.

Þegar þú skoðar skýrsluna í vafranum þínum eru dálkar og samanlagðri stöðu er breytt á kvikan hátt, miðað við skipulagið sem þú hefur grunnstillt. Þú getur flokkað niðurstöðurnar, síað þær, borað niður í gögnin og fleira.

Niðurstöður skýrslunnar eru vistaðar í gagnaeiningu **Birgðavirðis**. Þar af leiðandi getur þú síað og flutt niðurstöðurnar út á sniði eins og á CSV-skrá eða Microsoft Excel-sniði.

Skýrslan **birgðavirði í geymslu** er gagnleg þegar úttakið inniheldur margar línur. Til dæmis hefur þú 50.000 vörur og 300 verslanir hafa verið stofnaðar sem vöruhús. Í þessu tilfelli, ef þú biður um lokastöður birgða eftir vöru, síðu og vöruhúsi, mun úttakið innihalda margar línur.

> [!NOTE]
> Skýrslan **Geymsla birgðavirðisskýrslu** mun ekki innihalda millisamtölur sem eru skilgreindar í skýrsluútliti. Hún mun heldur ekki fela í sér fjárhagsstöður, jafnvel ekki þegar slíkar stöðurskýrslan eru skilgreindar í útliti skýrslu. Afstemming við Fjárhag verður að fara fram með því að nota prófjöfnuð. Hins vegar felur hefðbundin skýrsla um **Birgðavirði** ekki í sér þessar millisamtölur og stöður.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>Slökkva eða kveikja á Geymslueiginleika birgðavirðisskýrslu

Til að nota þennan eiginleika þarf að kveikja á honum fyrir kerfið þitt. Sem hluti af Supply Chain Management, útgáfa 10.0.25, er sjálfgefið kveikt á þessum eiginleika. (Frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á honum.) Ef þú ert að keyra útgáfu sem er eldri en 10.0.29, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Birgðavirði* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>Skilgreina stillingar birgðavirðisskýrslu

Notið síðuna **Birgðavirðisskýrslur** til að setja upp það efni sem er í mismunandi tegundum birgðavirðisskýrslna. Hægt er að skilgreina ótakmarkaðan fjölda skýrslugerða. Í hvert sinn sem þú býrð til aðra hvora tegund birgðavirðisskýrslu velur þú skýrslugerð.

1. Farið í **Kostnaðarstjórnun \> Uppsetning á reglum birgðabókhalds \> Birgðavirðisskýrslur**.
1. Fylgið einu af eftirfarandi skrefum:

    - Til að breyting fyrirliggjandi skýrslu skal velja hann úr listasvæðinu og síðan velja **Breyta** á aðgerðasvæðinu.
    - Til að stofna nýja skýrsla er valið **Ný** á aðgerðasvæðinu.

1. Í haus nýju eða völdu skýrslunnar skal stilla eftirfarandi gildi:

    - **Auðkenni** – Færið inn stutt kenni fyrir skýrsluna. Þetta gildi verður að vera einkvæmt meðal allra stillinga birgðavirðisskýrslna. Ekki er hægt að breyta henni eftir að þú vistar nýja stillingu.
    - **Heiti** - Færið inn lýsandi heiti á skýrslunni.

1. Ef þú ert að búa til nýja stillingu skýrslu, veldu **Vista** á aðgerðasvæði til að gera þá reiti sem eftir eru tiltæka.
1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Dagsetningabil** – Veldu fyrirfram skilgreint dagsetningabil. Hægt er að hnekkja þetta dagsetningabili þegar skýrslan er keyrð.
    - **Svið** – Veldu annað hvort *Bókunardagsetningu* eða *Færslutíma*, eftir því hvaða dagsetningu og tíma á að nota þegar skrár eru sóttar fyrir skýrsluna.
    - **Víddasamstæða** – Veldu víddarsamstæður til að keyra gögnin fyrir. (Stærðirnar eru skilgreindar í fjárhag). Til dæmis, þú gætir keyrt gögnin fyrir *Aðallykilinn* eða fyrir *Aðallykil + Viðskiptaeiningu*. Víddasamstæða sem þú velur má ekki vera fleiri en tvær víddir. Frekari upplýsingar eru í [Fjárhagsvíddarsamstæður](../../finance/general-ledger/financial-dimension-sets.md).

1. Á flýtiflipanum **Dálkar** skal stilla eftirfarandi reiti. Þessir reitir stýra dálkunum sem skýrslan inniheldur og gagnagerðum sem þeir dálkar innihalda.

    - **Birgðir** - Stilltu þennan valkost á *Já* til að sýna birgðavirði. Þú getur síðan samræmt þessi gildi við reikningsstöðu fjárhags.
    - **VÍV** - Stilltu þennan valkost á *Já* til að sýna aðeins VÍV-tölur. Síðan er hægt að afstemma þessi gildi við innistæður á VÍV-reikningi í fjárhagnum. Þegar þessi valkostur er stilltur á *Já* mun skýrslan aðeins sýna efnislegt magn og upphæðir birgða með VÍV-stöðu. Framleiðslupantanir með VÍV-stöðu hafa verið teknar til eða tilkynntar sem tilbúnar en þeim hefur ekki verið lokið.
    - **Frestaður kostnaður seldra vara** – Stillið þennan valkost á *Já* til að birta dálk sem sýnir efnislegt magn og upphæðir birgða fyrir frestaðan kostnaður seldra vara. Frestaður kostnaður seldra vara er sýnd með því að nota efnislegt magn og upphæðir, vegna þess að það jafnar magn og upphæðir fylgiseðla.
    - **Kostnaður seldra vara** – Stillið þennan valkost á *Já* til að birta dálk sem sýnir fjárhagslegt magn og upphæðir kostnaður seldra vara. Kostnaður seldra vara er sýnd með því að nota efnislegt magn og upphæðir, vegna þess að það jafnar magn og upphæðir reiknings.
    - **Hagnaður og tap** – Stillið þennan valkost á *Já* til að birta dálk sem sýnir fjárhagslega upphæð sem var birt á rekstrarreikningi fyrir birgðir.
    - **Prenta samanlögð lykilgildi til samanburðar** – Stillið þennan valkost á *Já* til að birta dálk sem sýnir stöðu fjárhagslykils. Á þennan hátt þarftu ekki að athuga endurskoðunarstöðu. Þessi valkostur virkar aðeins með hefðbundinni **Birgðavirðisskýrslu**, ekki með **Geymsluskýrsla birgðavirðisskýrslu**. Eftir að þú hefur stillt þennan valkost á *Já* verður þú að nota eftirfarandi reiti til að tilgreina hvern fjárhagslykil sem þú vilt skrá miðað við valkosti **Fjárhagsstöðu** sem þú hefur virkjað.

        > [!NOTE]
        > Ef þú velur *heildarreikning* fyrir einhvern þessara reita kemur fram bæði upphæð hvers birgðarreiknings sem er innifalinn í heildarreikningnum og heildarupphæð heildarreikningsins.

        - **Birgðarreikningur** – Tilgreinið fjárhagslykil til að sýna birgðarupplýsingar fyrir. (Stilla verðu bæði valkostinn **Birgðir** og valkostinn **Prenta samanlögð bókhaldsgildi fyrir samanburð á birgðum og fjárhag** á *Já*).
        - **VÍV-reikningur** – Tilgreinið fjárhagslykil til að sýna upplýsingar um VÍV. (Stilla verðu bæði valkostinn **VÍV** og valkostinn **Prenta samanlögð bókhaldsgildi fyrir samanburð á birgðum og fjárhag** á *Já*).
        - **Frestaður lykill kostnaðar seldra vara** – Tilgreinið fjárhagslykil til að sýna upplýsingar um kostnaður frestaðrar seldra vara. (Stilla verðu bæði valkostinn **Frestaður kostnaður seldra vara** og valkostinn **Prenta samanlögð bókhaldsgildi fyrir samanburð á birgðum og fjárhag** á *Já*).
        - **Kostnaður seldra vara reikningur** – Tilgreinið fjárhagslykil til að sýna upplýsingar um kostnaður seldra vara. (Stilla verðu bæði valkostinn **Kostnaður seldra vara** og valkostinn **Prenta samanlögð bókhaldsgildi fyrir samanburð á birgðum og fjárhag** á *Já*).

    - **Taka saman efnisleg og fjárhagsleg gildi** – Stillið þennan valkost á *Já* til að birta dálk sem sýnir heildarmagn birgða og birgðamagn (samantekt yfir bæði efnisleg og fjárhagsleg gildi). Ef þessi valkostur er stilltur á *Nei* mun skýrslan sýna bæði gildi efnislegra og fjárhagslegra birgða.
    - **Hafa með það sem ekki er bókað í fjárhag**. Stilltu þennan möguleika á *Já* til að birta dálk sem sýnir færslurnar sem voru aldrei bókaðar í fjárhag. Ekki er víst að færslur vegna eftirfarandi vara séu bókaðar í fjárhag:

        - Mótteknir og ekki enn reikningsfærðar vörur þegar valkosturinn **Bóka efnislegar birgðir** er hreinsaður fyrir viðkomandi vörulíkanasamstæðu.
        - Móttekin og ekki enn reikningsfærðar vörur þegar valkosturinn **Bóka innhreyfingarskjal afurða í fjárhag** er hreinsuð á flýtiflipanum **Innhreyfingarskjal** á flipanum **Almennt** á síðunni **Færibreytur fjárhags** (**Fjárhagur \> Uppsetning \> Færibreytur fjárhags**).

    - **Reikna meðalkostnað einingar** – Stillið þennan valkost á *Já* til að birta dálk sem sýnir meðalkostnað einingar. Meðalkostnaður vöru er heildarupphæð deilt með heildarmagninu.
    - **Heildarmagn og virði** – Stillið þennan valkost á *Já* til að birta dálka sem sýna heildarmagn efnislegra birgða (og fjárhagslegt magn) og heildarmagn efnislegra birgða (og fjárhagslegt magn). Þú getur aðeins stillt valkostinn á *Já* ef valkosturinn **Taka saman efnisleg og fjárhagsleg gildi** er stilltur á *Nei*.
    - **Birgðavíddir** – Í þessu hnitaneti, veljið gátreitinn **Skoða** fyrir hverja vídd sem á að sýna í skýrslunni. Aðeins víddir þar sem valkosturinn **Fjárhagslegar birgðir** er virkur sýna gildi í skýrslunni. Aðrar víddir sýna aðeins auða dálka. Fyrir þær víddir sem þú velur að sýna er hægt að velja gátreitinn **Samtals** til að sýna samtölur einnig.
    - **Tilfangakenni** – Stillið valkostinn **Skoða** á *Já* til að birta dálk sem auðkennir vöruna í hverri línu. Stillið valkostinn **Samtala** æa *Já* til að hafa samtölur líka með. Háð tegund vörunnar sem er skráður í hverri línu, dálkurinn sýnir eina af eftirfarandi tegundum upplýsinga:

        - **Efni** – Dálkurinn sýnir `ItemID` reitargildið fyrir viðkomandi efnisfærslu.
        - **Laun** – Dálkurinn sýnir reitargildi `WorkCenterID` fyrir viðeigandi færslu launa.
        - **Óbeinn kostnaður** – Dálkurinn `CodeID` sýnir reitagildi fyrir viðkomandi kostnaðarfærslu.

        Ef valkosturinn **Skoða** er stilltur á *Nei* fyrir bæði reitinn **Tilfangakenni** og reitinn **Tilfangaflokk** sérðu aðeins heildarbirgðavirði sem er byggt á birgðavíddunum sem þú valdir.

    - **Tilfangaflokkur** – Stilltu valkostinn **Skoða** á *Já* til að birta dálk sem auðkennir tilfangaflokkinn fyrir hverja línu. Stillið valkostinn **Samtala** æa *Já* til að hafa samtölur líka með. Háð tegund vörunnar sem er skráður í hverri línu, dálkurinn sýnir eina af eftirfarandi tegundum upplýsinga:

        - **Efni** – Dálkurinn sýnir `ItemGroup` reitargildið fyrir viðkomandi efnisfærslu.
        - **Laun** – Dálkurinn sýnir reitargildi `WorkcenterGroup` fyrir viðeigandi færslu launa.
        - **Óbeinn kostnaður** – Dálkurinn `CostGroup` sýnir reitagildi fyrir viðkomandi kostnaðarfærslu. (`CostGroupType`-gildið verður að vera *Óbeint*.)

        Ef valkosturinn **Skoða** er stilltur á *Nei* fyrir bæði reitinn **Tilfangakenni** og reitinn **Tilfangaflokk** sérðu aðeins heildarbirgðavirði sem er byggt á birgðavíddunum sem þú valdir.

1. Á flýtiflipanum **Línur** skal stilla eftirfarandi reiti. Með þessum reitum getur þú bætt við viðeigandi VÍV-tengdum undireiningum við skýrsluna eða fjarlægt þá.

    - **Efni** - Stilltu þennan valkost á *Já* til að sýna upplýsingar um efni. *Efni* er sjálfgefin tilfangagerð vegna þess að efni verður að vera innifalið í öllum skýrslustillingum til að búa til áreiðanlegt úttak.
    - **Laun** – Stilltu þennan valkost á *Já* til að sýna aðeins launakostnað VÍV.
    - **Óbeinn kostnaður** – Stilltu þennan valkost á *Já* til að sýna aðeins óbeinan kostnað VÍV.
    - **Bein útvistun** – Stillið þennan valkost á *Já* til að sýna bein útvistun VÍV. Þessar upplýsingar eru gagnlegar fyrir úthýsingu.
    - **Upplýsingastig** – Veldu skoðunaryfirlit fyrir skýrsluna:

        - *Færslur* – Skoða allar viðeigandi færslur í skýrslunni. Athugaðu að þú gætir lent í vandræðum með afköst þegar þú skoðar skýrslur sem innihalda mikið magn af færslum. Ef þú vilt nota þennan yfirlitsvalkost, mælum við því með því að þú notir **Geymsluskýrsla birgðavirðisskýrslu**.
        - *Samtölur* – Skoða heildarniðurstöðu.

    - **Taka með upphafsstaða** - Stilltu þennan valkost á *Já* til að sýna aðeins upphafsstaða. Þessi valkostur er aðeins tiltækur þegar reiturinn **Upplýsingastig** er stillt á *Færslur*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Stofna skýrslu um birgðarvirði í geymslu

Fylgdu þessum skrefum til að búa til og geyma skýrslu um **Birgðarvirði í geymslu**.

1. Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla skýrslu fyrir birgðavirði í geymslu**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í svarglugganum **Birgðavirði** á flýtiflipanum **Færibreytur**, skal stilla eftirfarandi reiti:

    - **Heiti** – Sláðu inn einkvæmt heiti fyrir skýrslan.
    - **Auðkenni** – Velja [stillingar birgðavirðisskýrslu](#report-configuration) sem nota á fyrir skýrsluna. Stillingarnar bjóða upp á valkosti fyrir dálkana og línurnar sem eru teknar með í skýrslunni þinni.
    - **Dagsetningabil** – Notið reitina í þessum hluta til að skilgreina hvaða skrár eru í skýrslunni. Til að tilgreina dagsetningabilið geturðu annað hvort valið forstillt svið (miðað við hvenær skýrslan var búin til) í svæðinu **Kóði dagsetningabils** eða valið ákveðin dagsetningar í reitunum **Frá dagsetningu** og **Til dagsetningar**.

1. Á flýtiflipanum **Færslur til að taka með** skaltu setja upp síur og takmarkanir til að skilgreina hvaða gögn á að taka með í skýrslunni. Veldu **Sía** til að opna hefðbundinn svargluggi fyrirspurnar þar sem hægt er að skilgreina valskilyrði, röðunarskilyrði og tengingar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Supply Chain Management. Allar þessar síur verða notaðar á birgðafærslurnar en ekki fjárhagsstöðuna. Hafðu þessa hegðun í huga þegar þú setur upp síurnar. Annars gætir misræmis á milli birgða og fjárhags.
1. Á flýtiflipanum **Keyra í bakgrunni** skaltu tilgreina hvernig, hvenær og hversu oft á að búa skýrsluna til. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.

    > [!NOTE]
    > Þessi skýrsla er alltaf keyrð sem hluti af runuvinnslu.

1. Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum.

Eftir að runuvinnslunni er lokið birtist skýrslan á síðu **Skýrslu um birgðarvirði í geymslu**. Hugsanlega verður að endurhlaða síðuna til að skýrslan birtist.

> [!IMPORTANT]
> Í valinni stillingu birgðavirðisskýrslu gætir þú fengið ranga upphafsstöðu ef þú velur sömu dagsetningu bæði í reitnum **Frá dagsetningu** og **Til dagsetningar** og ef þú stillir einnig valkostinn **Taka með upphafsstöðu** á *Já*.

## <a name="explore-an-inventory-value-report-storage-report"></a>Skoða skýrslu um birgðarvirði í geymslu

Eftir að þú hefur búið til skýrslu geturðu opnað og skoðað hana hvenær sem er með því að fylgja þessum skrefum.

1. Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Geymsla skýrslu fyrir birgðavirði í geymslu**.
1. Veldu skýrslu á listanum. Síðan sýnir upplýsingar um [stillingar birgðavirðisskýrslunnar](#report-configuration) sem var notuð til að mynda valda skýrsluna.
1. Veldu **Skoða upplýsingar** á aðgerðasvæðinu til að sýna efni skýrslunnar.
1. Skoðaðu skýrsluna með því að fylgja einhverjum af þessum skrefum:

    - Eins og á við um flestar staðlaðar síður í Supply Chain Management geturðu valið næstum hvaða dálk sem er til að raða eða sía hnitanetið eftir gildunum í þeim dálki.
    - Notaðu svæðið **Sía** til að sía skýrsluna eftir hvaða gildi sem er í nokkrum tiltækum dálkum.
    - Notaðu valmyndina Skoða (fyrir ofan svæðið **Sía**) til að vista og hlaða inn eftirlætis samsetningum flokkunar- og síuvalkosta.

## <a name="export-an-inventory-value-report-storage-report"></a>Flytja út skýrslu um birgðarvirði í geymslu

Hver skýrsla sem þú býrð til er geymd í gagnaeiningunni **Birgðavirði**. Þú getur notað staðlaða eiginleika gagnastjórnunar fyrir Supply Chain Management til að flytja út gögn frá þessari einingu til allra studdra gagnasniða, eins og CSV- eða Excel-sniða.

Eftirfarandi dæmi sýnir hvernig á að flytja út skýrslu um **Birgðarvirði í geymslu**.

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

## <a name="generate-a-standard-inventory-value-report"></a>Búa til staðlaða birgðavirðisskýrslu

Notið eftirfarandi ferli til að búa til staðlaða skýrslu um **Birgðavirði**.

1. Fara í **Kostnaðarstjórnun \> Fyrirspurnir og skýrslur \> Birgðabókhald – stöðuskýrslur \> Birgðavirði**.
1. Í svarglugganum **Birgðavirðisskýrsla** í flýtiflipanum **Færibreytur** skal stilla eftirfarandi reiti:

    - **Heiti** – Sláðu inn einkvæmt heiti fyrir skýrslan.
    - **Auðkenni** – Velja [stillingar birgðavirðisskýrslu](#report-configuration) sem nota á fyrir skýrsluna. Stillingarnar bjóða upp á valkosti fyrir dálkana og línurnar sem eru teknar með í skýrslunni.
    - **Dagsetningabil** – Notið reitina í þessum hluta til að skilgreina hvaða skrár eru í skýrslunni. Til að tilgreina dagsetningabilið geturðu annað hvort valið forstillt svið (miðað við hvenær skýrslan var búin til) í svæðinu **Kóði dagsetningabils** eða valið ákveðin dagsetningar í reitunum **Frá dagsetningu** og **Til dagsetningar**.

1. Á flýtiflipanum **Færslur til að taka með** skaltu setja upp síur og takmarkanir til að skilgreina hvaða gögn á að taka með í skýrslunni. Veldu **Sía** til að opna hefðbundinn svargluggi fyrirspurnar þar sem hægt er að skilgreina valskilyrði, röðunarskilyrði og tengingar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Supply Chain Management.
1. Á flýtiflipanum **Keyra í bakgrunni** skaltu tilgreina hvernig, hvenær og hversu oft á að búa skýrsluna til. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi** til að beita stillingum þínum og loka svarglugganum. Þá birtist skýrslan.

## <a name="reading-inventory-value-reports"></a>Lestur birgðavirðisskýrslna

Í þessum hluta eru leiðbeiningar um hvernig á að lesa og skilja birgðavirðisskýrslu.

Supply Chain Management styður eftirfarandi tvö mikilvæg hugtök sem tengjast birgðastöðu:

- **Fjárhagslegar færslur uppfærðar** – Þetta hugtak gefur til kynna að birgðafærslurnar séu þegar reikningsfærðar. Fyrir framleiðslupantanir gefur það til kynna lok framleiðslupöntunar.
- **Efnislegt uppfært** – Þetta hugtak gefur til kynna að birgðafærslurnar hafi ekki enn verið reikningsfærðar, en þær hafa verið mótteknar eða sendar. Fyrir framleiðslupantanir gefur það til kynna að efnið hafi verið tekið til eða framleiðslupöntunin hafi verið tilkynnt sem tilbúin.

Þegar þú skilur þessi tvö hugtök ætti að vera auðvelt að skilja eftirfarandi dálka í úttaki skýrslunnar:

- **Birgðir: Fjárhagslegt magn** – Magnið sem hefur verið uppfært fjárhagslega.
- **Birgðir: Fjárhagsleg upphæð** - Verðmæti birgða sem hafa verið uppfærðar fjárhagslega.
- **Birgðir: Efnislegt magn bókað** – Það magn sem hefur verið efnislega uppfært.
- **Birgðir: Bókuð efnisleg upphæð** – Verðmæti birgða sem hefur verið efnislega uppfærð.
- **Birgðir: Efnislegt magn ekki bókað** – Það magn sem er með birgðafærslur en hefur ekki verið bókað í fjárhaginn. Til dæmis, þú ert með vörulíkanshóp þar sem valkostir fyrir **Efnislegar birgðir** og **Bóka fjárhagslegar birgðir** eru hreinsaðar og þú ert með vöru sem er tengd við þann hóp. Þá stofnar maður innkaupapöntun, fær hana senda og reiknar hana út. Á þessum tímapunkti, ef þú skoðar birgðavirðisskýrslu vörunnar, sérðu að magnið og virðið á innkaupapöntuninni kemur fram í dálkunum **Birgðir: Efnislegt magn ekki bókað** og **Birgðir: Efnisleg upphæð ekki bókuð**.
- **Birgðir: Efnisleg upphæð ekki bókuð-** Hægt er að setja upp skýrslurnar þannig að þær sýni óbókaðar fjárhæðir. Ef þú ert hins vegar að nota skýrsluna til að afstemmingu birgða skaltu ekki nota þetta gildi. Annars er upphæðin ekki bókuð í fjárhaginn.
- **Birgðir: Magn** – Heildarmagn allra magndálka skýrslunnar.
- **Birgðir: Upphæð** – Heildarmagn allra upphæðardálka á skýrslunni. Þegar þú afstemmir birgðir skaltu ekki nota þennan dálk ef skýrslan inniheldur dálkinn **Birgðir: Efnisleg upphæð ekki bókuð**. Í því tilviki þarf að undanskilja **Birgðir: Efnisleg upphæð ekki bókuð** upphæðina frá heildarupphæðinni.
- **Meðal vörukostnaður** – Heildarupphæð deilt með heildarmagninu.

Venjulega notarðu birgðavirðisskýrslu til að skoða birgðavirðið og magnið. Hins vegar sýnir skýrslan þó ekki allar viðeigandi birgðavíddir. Ef þú sérð ekki víddirnar sem þú gerir ráð fyrir skaltu villuleita eftirfarandi stillingar:

- Farið yfir geymslu- og rakningarvíddaflokka vörunnar. Aðeins er hægt að sýna víddir þegar valkosturinn **Fjárhagslegar birgðir** er virkur í skýrslunni.
- Farið í **Kostnaðarstjórnun \> Uppsetning á reglum birgðabókhalds \> Birgðavirðisskýrslur**, veldu stillingu skýrslu sem þið notuðuð til að búa til skýrsluna og gangið úr skugga um að áskildar birgðavíddir séu valdar í dálkinum **Skoða**.

Til dæmis gæti verið vara sem hefði vörunúmerið *A0001*. Í hópnum fyrir birgðageymsluvíddir er aðeins svæðið virkjað fyrir fjárhagslegar birgðir. Vefsvæðið og vöruhúsið eru bæði virkjuð fyrir efnislegar birgðir. Í rakningarvíddarflokknum er rununúmerið virkt fyrir efnislegar birgðir en ekki fjárhagslegar birgðir. Þá er hægt að nota skýrsluuppsetningu þar sem svæði, vöruhús og rununúmer eru öll valin. Þegar skýrslan er skoðuð sést gildi aðeins fyrir vefsvæðið. Dálkarnir fyrir vöruhúsið og rununúmer eru auðir. Eins og þetta dæmi sýnir geta skýrslur um birgðavirði aðeins sýnt birgðavídd sem er virk fyrir fjárhagslegar birgðir.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
