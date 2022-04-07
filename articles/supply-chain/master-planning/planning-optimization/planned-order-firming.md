---
title: Staðfesta áætlaðar pantanir
description: Þetta efnisatriði útskýrir hvernig áætlaðar pantanir eru staðfestar. Þegar fyrirhugaðar pantanir eru staðfestar breytast þær í raunverulegar innkaupapantanir, millifærslupantanir eða framleiðslupantanir.
author: t-benebo
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 30f3ee656b97e0337b6e3e78f0acb2300d7d85dc
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468469"
---
# <a name="firm-planned-orders"></a>Staðfesta áætlaðar pantanir

[!include [banner](../../includes/banner.md)]

Áætlaðar pantanir verða að vera *staðfestar* (þ.e. útgefnar) sem hluti af ferli aðaláætlanagerðar. Þegar fyrirhugaðar pantanir eru staðfestar breytast þær í raunverulegar innkaupapantanir, millifærslupantanir eða framleiðslupantanir. Þessar pantanir eru einnig kallaðar *losaðar pantanir* eða *opnar pantanir*.

Þrjár aðferðir eru við staðfestingu á pöntunum:

- **Handvirk staðfesting** – Veljið ákveðnar áætlaðar pantanir úr lista og hefjið svo ferlið handvirkt.
- **Sjálfvirk staðfesting** – Skilgreinið sjálfgefin tímamörk fyrir þekjuflokka, einstaka hluti og samsetningar hluta og aðaláætlana. Því næst, á meðan aðaláætlanagerð keyrir, verða áætlaðar pantanir sjálfkrafa staðfestar ef dagsetning pöntunar er innan tiltekinna tímamarka fyrir staðfestingu.
- **Staðfesting byggð á fyrirspurn** – Skilgreinið fyrirspurn til að velja áætlaðar pantanir út frá eiginleikum þeirra. Hægt er að setja upp runuvinnslu til að keyra fyrirspurnina og staðfesta samsvarandi pantanir reglulega.

Í þessu efnisatriði er hverri aðferð lýst nákvæmlega.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>Virkja eiginleikana sem er lýst í þessu efnisatriði

Flestir eiginleikar áætlaðra pantana eru í boði í öllum hefðbundnum uppsetningum Microsoft Dynamics 365 Supply Chain Management sem notar fínstillingu áætlanagerðar. Hins vegar þarf að kveikja á nokkrum af þeim eiginleikum sem lýst er í þessu efnisatriði í eiginleikastjórnun áður en hægt er að nota þá.

### <a name="turn-parallelized-firming-of-planned-orders-on-or-off"></a>Kveiktu eða slökktu á samhliða staðfestingu fyrirhugaðra pantana

Samhliða staðfesting stuðlar að hraðara staðfestingarferli með því að gera hana samhliða í mörgum þráðum. Þessi nálgun getur verið gagnleg þegar margar pantanir eru staðfestar. Til að nota þessa virkni, *Samhliða staðfesting á fyrirhuguðum pöntunum* kveikt verður á eiginleikanum fyrir kerfið þitt. Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geturðu kveikt eða slökkt á þessari virkni með því að fara á [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og að leita að *Samhliða staðfesting á fyrirhuguðum pöntunum* eiginleiki.

### <a name="enable-planned-order-firming-with-filtering"></a>Virkja staðfestingu áætlaðrar pöntunar með síu

Staðfesting áætlaðrar pöntunar með síun gerir kleift að skilgreina rökleg skilyrði við val á hvaða áætlaðar pantanir eigi að staðfesta. Einnig er hægt að forskoða hvaða áætlaðar pantanir voru valdar, keyra ferlið í bakgrunninum og/eða tímasetja þær sem runuvinnslu.

Frá og með Supply Chain Management útgáfu 10.0.25 er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að *Skipulögð pöntunarstyrking með síun* eiginleiki í [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

### <a name="enable-auto-firming-for-planning-optimization"></a>Virkja sjálfvirka staðfestingu fyrir fínstillingu áætlanagerðar

Sjálfvirk staðfesting gerir kleift að staðfesta áætlaðar pantanir sem hluti af ferli aðaláætlanagerðar innan tímamarka staðfestingar. Sjálfvirk staðfesting er alltaf studd fyrir áætlunarvélina sem er innbyggð í Supply Chain Management. Hins vegar þarf að kveikja á eiginleikanum til að nota hana með fínstillingu áætlanagerðar.

Til að gera þessa virkni aðgengilega í kerfinu skal fara í [Eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eiginleikanum *Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar*. (Frá og með Supply Chain Management útgáfu 10.0.21 er sjálfgefið kveikt á þessum eiginleika.)

## <a name="manually-firm-planned-orders"></a>Staðfesta áætlaðar pantanir handvirkt

Til að staðfesta áætlaðar pantanir handvirkt skal finna og velja áætlaðar pantanir sem ætlunin er að staðfesta og síðan staðfestingarferlið sett í gang á handvirkan hátt.

1. [Opna einhverja listasíðu áætlaðra pantana](approved-planned-order.md#view-planned-orders).
1. Notið reitinn **Sía**, reitinn **Áætlun** og dálkahausa til að sía og raða listanum þannig að hægt sé að finna áætlaðar pantanir sem leitað er að.
1. Veljið gátreitinn fyrir hverja áætlaða pöntun sem ætlunin er að staðfesta. Ef staðfesta á allar áætlaðar pantanir sem eru nú skráðar á síðunni (bygt á notuðum síum) skal sleppa þessu skrefi.
1. Á aðgerðasvæðinu skal velja einn eftirfarandi hnapp:

    - **Staðfesta** – Staðfesta aðeins valdar áætlaðar pantanir.
    - **Staðfesta allar** - Staðfestið allar áætlaðar pantanir sem eru skráðar á síðunni (miðað við síurnar sem voru notaðar), óháð gátreitum sem eru valdir. Þessi valkostur er gagnlegur ef verið að er staðfesta margar áætlaðar pantanir.

1. Í svarglugganum **Staðfesting** í flýtiflipanum **Færibreytur** skal stilla eftirfarandi reiti. (Margir þessara reita taka sjálfgefin gildi úr flipanum **Hefðbundin uppfærsla** á síðunni **Færibreytur aðaláætlanagerðar**.)

    - **Uppfæra merkingu** - Veljið merkingarreglu á birgðum sem nota á þegar áætlaðar pantanir eru staðfestar.
    - **Stöðva staðfestingu ef villa kemur upp** – Stillið þennan valkost á *Já* til að stöðva staðfestingu allra valinna áætlaðra pantana ef villa kemur upp í einhverri þeirra. Stilla verður þennan valkost á *Nei* ef valkosturinn **Gera staðfestingu samhliða** er stilltur á *Já*.
    - **Gera staðfestingu samhliða** – Þessi valkostur er aðeins í boði ef kveikt er á [*Samhliða staðfesting á áætluðum pöntunum* eiginleikanum](#enable-features) í kerfinu og ef tvær eða fleiri áætlaðar pantanir hafa verið valdar fyrir staðfestingu. Stilltu það á *Já* til að keyra staðfestingarferlin samhliða. Samhliða staðfesting getur bætt afköst.
    - **Fjöldi þráða** – Þessi valkostur er eingöngu í boði ef kveikt er á [*Samhliða staðfesting á áætluðum pöntunum* eiginleikanum](#enable-features) í kerfinu og ef valkosturinn **Gera staðfestingu samhliða** er stilltur á *Já*. Færið inn fjölda þráða sem á að nota til að gera staðfestingarferlið samhliða. Frekari ráðleggingar um hvernig á að nota þennan valkost í aðaláætlanagerð er að finna í [Bæta frammistöðu aðaláætlunargerðar](../master-planning-performance.md#number-of-threads).

        > [!NOTE]
        > Gildið *0* (núll) fyrir reitinn **Fjöldi þráða** lengir keyrslutíma aðaláætlanagerðar. Þess vegna mælum við með því að stilla alltaf gildið fyrir þennan reit á hærra en 0.

    - **Flokka eftir lánardrottnum** – Stillið þennan valkost á *Já* til að flokka áætlaðar innkaupapantanir og stofna eina innkaupapöntun á hvern lánardrottin við staðfestingu. Að öðrum kosti er hægt að stofna eina innkaupapöntun sem er með eina línu fyrir hverja áætlaða pöntun.
    - **Flokka eftir kaupendaflokki** – Stillið þennan valkost á *Já* til að flokka áætlaðar innkaupapantanir og stofna eina innkaupapöntun sem sameinar lánardrottin og kaupendaflokk. Til að nota þennan valkost verður einnig að stilla valkostinn **Flokka eftir lánardrottnum** á *Já*.
    - **Flokka eftir innkaupasamningi** – Stilltu þennan valkost á *Já* til að flokka áætlaðar innkaupapantanir sem eru með sama lánardrottin og fyrirliggjandi innkaupasamningar og stofna eina innkaupapöntun fyrir hvern innkaupasamning. Þessi valkostur er sjálfkrafa virkur þegar **Flokka eftir lánardrottnum** er virkur. Til að nota **Flokka eftir innkaupasamningi** verður að stilla **Finna innkaupasamning** á *Já* á síðunni **Færibreytur aðaláætlanagerðar**.
    - **Flokka eftir tímabili** (í hlutanum **Innkaupapantanir**) – Velja tímabilið sem flokka á áætlaðar innkaupapantanir eftir. Til að nota þennan valkost verður einnig að velja valkostinn **Flokka eftir lánardrottnum**.
    - **Flokka eftir tímabili** (í hlutanum **Flutningar**) – Veljið tímabilið sem flokka á áætlaðar flutningspantanir eftir. Pantanirnar verða flokkaðar samkvæmt gildunum **Frá vöruhúsi** og **Til vöruhúss**.

    > [!NOTE]
    > Hver og einn valmöguleikar „Flokka eftir“ veldur því að kerfið umbreytir hverri fyrirhugaðri pöntun í línu í einni innkaupapöntun sem verður til úr flokkuninni.

    ![Flýtiflipi færibreyta í svarglugga staðfestingar.](./media/manual-firming.png "Flýtiflipi færibreyta í svarglugga staðfestingar")

1. Í flýtiflipanum **Keyra í bakgrunni** skal setja upp vinnsluna þannig að hún keyri í runustillingu. Hins vegar er ekki skynsamlegt að setja upp endurtekna áætlun við handvirka staðfestingu. Reitirnir virka rétt eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management. Við handvirka staðfestingu vinnur runuvinnslan aðeins úr völdum áætluðum pöntunum. Það mun ekki vinna neinar pantanir sem passa við síurnar sem eru notaðar á síðunni.
1. Veldu **Í lagi** til að gera stillingarnar virkar og búa til staðfestu pantanirnar.

## <a name="auto-firm-planned-orders"></a>Staðfesta sjálfvirkt áætlaðar pantanir

Sjálfvirk staðfesting gerir kleift að staðfesta áætlaðar pantanir sem hluta af ferli aðaláætlanagerðar. Hægt er að skilgreina ákveðin tímamörk fyrir þekjuflokka, einstaka vörur og samsetningu vara og aðaláætlanir. Því næst, á meðan aðaláætlanagerð keyrir, verða áætlaðar pantanir sjálfkrafa staðfestar ef dagsetning pöntunar er innan tiltekinna tímamarka fyrir staðfestingu. Áætlaðar pantanir sem myndaðar eru með fínstillingu áætlanagerðar og innbyggðri aðgerð aðaláætlanagerðar meðhöndla pöntunardagsetninguna (þ.e. upphafsdaginn) á annan hátt.

> [!NOTE]
> Sjálfvirk staðfesting á áætluðum innkaupapöntunum getur aðeins átt sér stað fyrir vörur sem tengjast lánardrottni.
> 
> Afleiddar pantanir (þ.e. innkaupapantanir undirverktaka) sem eru staðfestar munu fá stöðuna *Í endurskoðun* ef kveikt er á breytingarrakningu.

> [!IMPORTANT]
> Áður en hægt er að nota eiginleikann sem er lýst í þessum hluta með fínstillingu áætlanagerðar verður að kveikja á eiginleikanum [*Sjálfvirk staðfesting fyrir fínstillingu áætlanagerðar*](#enable-features) í kerfinu eins og lýst er í upphafi þessa efnisatriðis. Alltaf er hægt að nota sjálfvirka staðfestingu með innbyggðri aðaláætlunarvél.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Sjálfvirk staðfesting með fínstillingu áætlanagerðar í samanburði við innbyggða áætlunarvél

Bæði er hægt að nota fínstillingu áætlanagerðar og innbyggða áætlunarvél til að staðfesta sjálfvirkt áætlaðar pantanir. Þó er til staðar mikilvægur munur. Til dæmis notar fínstilling áætlanagerðar pöntunardagsetninguna (þ.e. upphafsdaginn) til að ákveða hvaða áætlaðar pantanir eigi að staðfesta, á meðan innbyggða áætlunarvélin notar dagsetningu þarfa (þ.e. lokadaginn). Eftirfarandi tafla dregur saman mismuninn.

| Eiginleiki | Fínstilling áætlanagerðar | Innbyggð áætlunarvél |
|---|---|---|
| **Grunndagsetning** | Sjálfvirk staðfesting byggist á pöntunardegi (upphafsdegi). | Sjálfvirk staðfesting byggist á þarfadagsetningu (lokadegi). |
| **Afhendingartími** | Vegna þess að pöntunardagsetningin (upphafsdagsetningin) kallar á staðfestingu þarftu ekki að líta á afhendingartímann sem hluta af tímamörkum staðfestingar. | Til að hjálpa til við að tryggja að pantanir séu tímanlega staðfestar verða tímamörk staðfestingar að vera lengri en afhendingartíminn. |
| **Pantanir fyrir yfirstandandi viku** | Til að staðfesta allar pantanir sem verða að byrja í þessari viku, verða tímamörk staðfestingar að vera ein vika. | Til að staðfesta allar pantanir sem verða að byrja í þessari viku, verða tímamörk staðfestingar að vera afhendingartíminn plús ein vika. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Setja upp tímamörk sjálfvirkrar staðfestingar og staðfestingar

Hægt er að kveikja á sjálfvirkri staðfestingu með því að úthluta tímamörkum sjálfvirkrar staðfestingar á viðeigandi þekjuuppsetningu eins og lýst verður síðar í þessu efnisatriði. Ef ekki er kveikt á sjálfvirkri staðfestingu fyrir neina þekjuuppsetningu eða ef áætlanagerð hefst á tiltekinni síðu, t.d. síðunni **Nettóþarfir** fyrir útgefna afurð, verður ferli sjálfvirkrar staðfestingar sleppt.

Valkostir fyrir flokkun og merkingar fyrir sjálfvirka staðfestingu taka gildin úr flipanum **Hefðbundin uppfærsla** á síðunni **Færibreytur aðaláætlanagerðar**.

Tímamörk sjálfvirkrar staðfestingar eru skilgreind eftir fjölda daga sem sleginn er inn fyrir tilheyrandi þekjuuppsetningu. Hægt er að kveikja á sjálfvirkri staðfestingu og stjórna tímamörkum staðfestingar á eftirfarandi hátt:

- Til að skilgreina sjálfgefinn girðingartíma girðingar fyrir umfjöllunarhóp ferðu í **Aðaláætlunargerð \> Uppsetning \> Þekja \> Þekjuhópar** og veldu þekjuhóp. Síðan, á flýtiflipanum **Annað**, í reitinn **Sjálfvirk tímamörk staðfestinga (dagar)**, sláðu inn fjölda daga.
- Til að skrifa yfir tímamörk staðfestingar sem eru skilgreind fyrir þekjuflokkinn fyrir tiltekna vöru er farið í **Afurðarupplýsingastjórnun \> Útgefnar afurðir**. Á aðgerðasvæðinu skal velja **Vörur** og svo **Vöruþekja**. Á flipanum **Almennt** velurðu **Hnekkja tímamörkum** og svo í reitinn **Sjálfvirk tímamörk staðfestinga (dagar)** slærðu inn fjölda daga.
- Til að skrifa yfir þau tímamörk staðfestingar sem eru skilgreind fyrir þekjuhópinn og vöruþekju fyrir tiltekið aðalskipulag **Aðaláætlunargerð \> Uppsetning \> Aðaláætlanir** og velur aðalskipulag. Síðan, í flýtiflipanum **Tímamörk í dögum** skal stilla valkostinn **Staðfesting** á *Já* og slá inn dagafjöldann.

Ef öll áðurnefnd tímamörk eru stillt á *0* (núll) verður slökkt á sjálfvirkri staðfestingu fyrir viðeigandi vörur.

## <a name="firm-planned-orders-by-using-a-query"></a>Staðfesta áætlaðar pantanir með fyrirspurn

Staðfesting byggð á fyrirspurn gerir kleift að áætla staðfestingu byggt á skilyrði sem er skilgreint fyrirfram. Ólíkt sjálfvirkri staðfestingu leyfir staðfesting sem byggð er á fyrirspurn sjálfvirka staðfestingu á mismunandi undirsöfnum pantana á ólíkum tímapunktum. Auk þess er hægt að nota annaðhvort handvirkar eða sjálfvirkar aðgerðir til að staðfesta mismunandi gerðir áætlaðra pantana. Einnig er hægt að forskoða hvaða staðfestar pantanir eru valdar samkvæmt stillingunum þínum. Þess vegna er hægt að staðfesta að valið uppfylli væntingar þínar.

Hægt er að sameina sjálfvirka staðfestingu við staðfestingu sem byggir á fyrirspurn. Til dæmis hefur staðfestingarverk sem byggir á fyrirspurn framvirk tímamörk sem eru ekki lengri en tímamörk fyrir samsvarandi skilgreiningu á umfangi sjálfvirkrar staðfestingar. Því mun staðfestingarverk sem byggir á fyrirspurn vinna úr áætluðum pöntunum áður en sjálfvirk staðfesting er sett í gang. Hægt er að nýta sér þessa hegðun til að tímasetja pantanir fyrir tiltekna lánardrottna á annan hátt en pantanir fyrir svipaðar afurðir frá öðrum lánardrottnum.

> [!IMPORTANT]
> Áður en hægt er að nota eiginleikann sem lýst er í þessu efnisatriði verður að kveikja á [*Staðfesting áætlaðrar pöntunar með síun* eiginleikanum](#enable-features) í kerfinu eins og lýst er í upphafi þessa efnisatriðis.

Fylgið eftirfarandi skrefum til að staðfesta áætlaða pöntun með staðfestingarferli sem byggir á fyrirspurn.

1. Farið í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Staðfesting áætlaðrar pöntunar**.
1. Í svarglugganum **Staðfesting áætlaðrar pöntunar**, í flýtiflipanum **Færibreytur**, skal stilla valkosti grunnvinnslu, merkingar og flokkunar. Þessir valkostir virka rétt eins og þeir gera í svarglugganum **Staðfesting**. (Sjá fyrri hlutann fyrir lýsingar.) Því næst, í hlutanum **Áætlun**, skal stilla eftirfarandi reiti sem eru einkvæmir svarglugganum **Staðfesting áætlaðrar pöntunar**:

    - **Áætlun** – Veljið aðaláætlun sem á að nota við staðfestingu áætlaðra pantana sem þessi fyrirspurn finnur.
    - **Staðfesting tímamarka í dögum fram í tíma** – Veljið hversu langt fram í tímann á að reikna samkvæmt aðaláætlanagerð ýmsar kröfur og annað sem þarf að hafa í huga.
    - **Staðfesting tímamarka í dögum aftur í tíma** – Veljið hversu langt aftur í tímann á að reikna samkvæmt aðaláætlanagerð ýmsar kröfur og annað sem þarf að hafa í huga.

    ![Flýtiflipi færibreyta í svarglugga staðfestingar áætlaðrar pöntunar.](./media/planned-order-firming-main-1.png "Flýtiflipi færibreyta í svarglugga staðfestingar áætlaðrar pöntunar")

1. Til að tilgreina hvaða færslur á að hafa með í pöntuninni skal velja hnappinn **Sía** í flýtiflipanum **Færslur til að taka með**. Hefðbundin svargluggi fyrirspurnar birtist þar sem hægt er að skilgreina valskilyrði, röðunarskilyrði og tengingar. Reitirnir virka á sama hátt og fyrir aðrar gerðir fyrirspurna í Supply Chain Management. Reitir hér eru skrifvarðir og sýna gildi sem tengjast fyrirspurninni.

    ![Færslur til að taka með í flýtiflipanum í svarglugga fyrir staðfestingu áætlaðrar pöntunar.](./media/planned-order-firming-main-2.png "Færslur til að taka með í flýtiflipanum í svarglugga fyrir staðfestingu áætlaðrar pöntunar")

1. Veljið **Forskoða** til að forskoða innihald staðfestrar pötntunar sem byggir á stillingunum fram að þessu. Listi yfir áætlaðar pantanir sem verða staðfestar birtist sem skilaboð. Síðan er hægt að laga stillingar eins og þörf er á þar til forsýningin sýnir staðfesta pöntun eins og ætlast var.

    ![Dæmi um forskoðun staðfestrar pöntunar.](./media/planned-order-firming-preview.png "Dæmi um forskoðun staðfestrar pöntunar")

    > [!WARNING]
    > Þessi eiginleiki staðfestir allar áætlaðar pantanir sem uppfylla síuskilyrðin. Of víðtæk staðfesting áætlaðra pantana getur leitt til þess að mikill fjöldi óþarfa innkaupa-, flutnings- og framleiðslupantana verði stofnaðar. Áður en haldið er áfram skal ávallt nota hnappinn **Forskoða** til að staðfesta færslurnar sem verða hafðar með.

1. Í flýtiflipanum **Keyra í bakgrunni** skal setja upp vinnsluna þannig að hún keyri í runustillingu og/eða setja upp endurtekna áætlun. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Í lagi** til að gera stillingarnar virkar og búa til staðfestu pantanirnar.

## <a name="track-firmed-orders"></a>Rekja staðfestar pantanir

Fylgja skal eftirfarandi skrefum til að rekja áætlaða pöntun sem var staðfest.

1. [Opna einhverja listasíðu áætlaðra pantana](approved-planned-order.md#view-planned-orders).
1. Opnið eða veljið áætluðu pöntunina sem á að rekja.
1. Á aðgerðasvæðinu, í flipanum **Yfirlit**, í flokknum **Yfirlit**, skal velja **Staðfestingarsaga**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
