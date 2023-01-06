---
title: Sjálfvirknivæða fjárhagsjafnanir
description: Í þessari grein er að finna upplýsingar um sjálfvirknivæðingu fjárhagsjafnanna.
author: abruer
ms.date: 9/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: b43eeeefa581b5d8b40dc2cf0187c7c781b18be3
ms.sourcegitcommit: 27ce4fc706100b626b81c3a1023238acd872e76c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2022
ms.locfileid: "9707761"
---
# <a name="automate-ledger-settlements"></a>Sjálfvirknivæða fjárhagsjafnanir

[!include [banner](../includes/banner.md)]

Í Microsoft Dynamics 365 Finance, útgáfu 10.0.31, er eiginleikinn  **Sjálfvirknivæða ferli fjárhagsjafnana** í boði á  **Eiginleikastjórnun** vinnusvæðinu. Aðeins er hægt að virkja eiginleikann **Sjálfvirknivæða ferli fjárhagsjafnana** ef eiginleikinn **Munurinn á fjárhagsjöfnun og árslokalokun** hefur verið virkjaður.

Fjárhagsjöfnun er ferlið við að jafna debet- og kreditfærslur í fjárhagnum. Fyrirtæki sem framkvæma aðgerðir fjárhagsjafnana samkvæmt endurtekinni áætlun geta nú gert ferlið sjálfvirkt. Meðan á sjálfvirka fjárhagsjöfnunarferlinu stendur er aðeins hægt að jafna debetfærslu og kreditfærslu sjálfkrafa ef upphæðir þeirra í bókhaldsgjaldmiðlinum eru jafnar.Til dæmis er hægt að tengja debetupphæðina $1,00 sjálfkrafa við kreditupphæð $1,00. Hins vegar getur debetgildi að verðmæti $ 1,00 ekki sjálfkrafa samsvarað tveimur kreditfærslum að verðmæti $0,50 hvor. Samsvörun fjárhagsfærslupphæða að hluta er ekki studd.

Sjálfvirkni fjárhagsjöfnunar skilgreinir eftirfarandi upplýsingar:

- Þegar fjárhagsjafnanir eru keyrðar
- Hvaða viðmið eru notuð til að stemma við debetfærslur og kreditfærslur sem hægt er að jafna sjálfkrafa
- Í hvaða röð eru upplýsingar um fjárhagsjöfnun unnar?

## <a name="define-the-occurrence-of-ledger-settlements"></a>Skilgreina tilvik fjárhagsjafnanna

Sjálfvirkni fjárhagsjöfnunar notar „Meðhöndla sjálfvirkniramma“. Mismunandi viðskiptaferli nota þennan ramma til að skilgreina endurtekningu á völdu ferli. Fyrir fjárhagsjafnanir skal fara í  **Kerfisstjórnun \> Uppsetning \> Sjálfvirkni ferlis** eða **Fjárhagur \> Fjárhagsuppsetning \> Sjálfvirkni ferlis**.

Fyrst velur þú valkostinn  **Stofna nýja sjálfvirkni ferlis** og síðan  **Fjárhagsjafnanir**. Leiðsagnarforrit leiðir notandann í gegnum ferlið þegar verið er að setja upp sjálfvirknina.

## <a name="general-page"></a>Almenna síðan

Á síðunni  **Almennt**  í leiðsögninni skal slá inn heiti tilviks fjárhagsjöfnunarinnar sem verið er að búa til. Ef samsvarandi debet- og kreditfærslur eru fjárhagsjafnaðar á mánudegi skal slá inn lýsandi heiti eins og  **Fjárhagsjöfnun\_Mán**. Heitið sem þú slærð inn er sýnt í dálkinum **Sjálfvirkniregla** á síðunni  **Fjárhagsjafnanir** .

Eftirstandandi stillingar á síðunni eru almennar og skilgreina endurtekningarmynstur þessarar útgáfu af fjárhagsjöfnunum. Til dæmis, ef tilfelli er fyrir mánudag er hægt að skilgreina það þannig að það keyri vikulega og hægt er að velja mánudag sem þann dag vikunnar þegar það er keyrt. Einnig er hægt að færa inn snemmbúna tímaáætlun, t.d. 02:00, þannig að sjálfvirkniferlinu verði lokið fyrir upphaf næsta viðskiptadags. Mælt er með því að tímasetja sjálfvirkni ferlisins þannig að hún sé framkvæmd utan venjulegs vinnutíma. Þannig hjálpar þú til við að draga úr álagi á bókhaldsdeildina á vinnudeginum.

Frekari upplýsingar um aðra reiti á síðunni  **Almennt**  er að finna í fylgiskjölum sjálfvirkniferlisins.

## <a name="ledger-settlements-match-criteria-page"></a>Síða skilyrða fyrir samsvörun fjárhagsjafnana

Næsta síða í leiðsagnarforritinu er síðan  **Síða skilyrða fyrir samsvörun fjárhagsjafnana** . Hún er notuð til að skilgreina aðallykla sem eru innifaldir í tilfellum sjálfvirkni ferlis og skilyrðið sem notað er til að ákvarða samsvarandi debet- og kreditfærslur.

### <a name="account-selection"></a>Val á lykli

Aðallyklarnir sem voru áður skilgreindir sem fjárhagsjöfnunarlyklar fyrir lögaðilann eru sýndir. (Aðallyklar eru skilgreindir sem fjárhagsjöfnunarlyklar í **Fjárhagur \> Fjárhagsuppsetning \> Almennar fjárhagsfæribreytur \> Fjárhagsfæribreytur**.)

### <a name="main-account-and-posting-layer"></a>Aðallykill og bókunarlag

Gildin  **Aðallykill** og **Bókunarlag** eru nauðsynleg skilyrði fyrir samsvörun. Gildin **Aðallykill** og **Bókunarlag** fyrir debet- og kreditfærslu fjárhagsins verða að stemma í sjálfvirku jöfnunarferli fjárhags.

### <a name="posting-type"></a>Bókunargerð

Veljið valkostinn **Bókunargerð** ef debet- og kreditfærslur fjárhags verða að hafa sömu bókunargerðir til að samsvörun eigi sér stað á sjálfvirka reikningsuppgjörsferlinu.

### <a name="financial-dimensions"></a>Fjárhagsvíddir

Veljið valkostinn **Fjárhagsvíddir** ef debet- og kreditfærslur fjárhags verða að hafa sömu fjárhagsvíddir til að samsvörun eigi sér stað í sjálfvirka fjárhagsjöfnunarferlinu. Þegar þessi valkostur er valinn verður að velja skilyrði fyrir fjárhagsvíddargildin í listanum **Tiltækar fjárhagsvíddir**. Listinn **Tiltækar fjárhagsvíddir** inniheldur ekki vídd aðallykils því að hann er sjálfkrafa áskilinn sem hluti af skilyrði fyrir samsvörun.

## <a name="view-the-results-of-a-ledger-settlement-automation"></a>Skoða niðurstöður sjálfvirkni fjárhagsjöfnunar

Þegar röð sjálfvirkni fjárhagsjöfnunar er búin til birtast tilfelli hverrar fjárhagsjöfnunar í vikulegu yfirliti sjálfvirkniferlisins. Þar að auki er staða hvers tilviks sýnd. Eftirfarandi stöður eru notaðar:

- **Áætlað**  – Sjálfvirknin er áætluð, en hún hefur ekki verið keyrð.
- **Keyrir** – Sjálfvirknin er í gangi.
- **Villa**  – Sjálfvirknin hefur verið keyrð en villa kom upp. Hægt er að skoða villurnar með því að velja hnappinn  **Skoða niðurstöður** .
- **Lokið** – Það tókst að keyra sjálfvirknina. Hægt er að skoða niðurstöður jöfnunar á síðunni **Fjárhagsjöfnun**.

Opnið **Fjárhagur \> Reglubundin verkefni \> Fjárhagsjafnanir** til að sjá samsvarandi niðurstöður. Svæðið **Sjálfvirkniregla** á síðunni **Fjárhagsjafnanir** sýnir heiti áætlaðs verks sjálfvirkrar fjárhagsjöfnunar sem var notað til að jafna færsluna. Árangurslausar jöfnunartilraunir uppfæra ekki gildi **Sjálfvirkniregla**. Ef færsla sem var áður jöfnuð af sjálfvirka ferlinu er bakfærð handvirkt verður gildið **Sjálfvirkniregla** fjarlægt.

Reiturinn **Dagsetning jöfnunar** fyrir jafnaðar færslur sýnir dagsetninguna þegar sjálfvirka ferlið var framkvæmt.

## <a name="editing-a-ledger-settlement-automation"></a>Breytingar á sjálfvirkni fjárhagsjöfnunar

Með ramma sjálfvirkniferlisins er hægt að breyta röðinni og tilfellunum sem eru stofnuð fyrir fjárhagsjöfnunina. Hægt er að breyta röðinni annaðhvort á síðunni  **Sjálfvirkniferli**  eða í vikulegu yfirliti sjálfvirkniferlisins. Til dæmis, ef yfirmaður ákveður að framkvæma fjárhagsjöfnun á miðvikudegi í stað mánudags, getur hann fundið tilfellið í vikuyfirlitinu og valið  **Skoða/breyta - Röð**.

Ef röð er breytt er notandi beðinn um að tilgreina hvort breytinguna eigi að gera á öllum fyrirliggjandi tilvikum eða aðeins nýjum tilvikum. Eldri tilvikum sem eru komin með stöðuna **Lokið**, eða þar sem kom upp staðan  **Villa** , verður ekki breytt.

Einnig er hægt að bæta við nýju tilviki eða breyta fyrirliggjandi tilviki. Til dæmis er áætlað að keyra næsta tilvik fjárhagsjöfnunar miðvikudaginn 1. janúar, en þessi dagsetning er frídagur. Hægt er að breyta tilvikinu annaðhvort á síðunni  **Sjálfvirkniferli**  eða í vikulegu yfirliti sjálfvirkniferlisins. Síða opnast sem sýnir upplýsingar áætlunar og skilyrði fyrir samsvörun. Hér er hægt að breyta áætluðum tíma og dagsetningu. Einnig er hægt að breyta skilyrðum fyrir samsvörun, ef breytingar eru nauðsynlegar. 

Einnig er hægt að óvirkja tilvik eða röð tilvika. Til að gera tilvik óvirkt og fresta úrvinnslu þess skal velja það í vikulegu yfirliti sjálfvirkniferlisins og síðan velja  **Gera óvirkt**. Hægt er að slökkva á röð á síðunni **Sjálfvirkniferli** .

## <a name="security-for-ledger-settlement-automation"></a>Öryggi fyrir sjálfvirkni fjárhagsjöfnunar

Aðgangsheimildinni **Vinna með stillingar á röð sjálfvirkra fjárhagsjafnana** hefur verið bætt við hlutverk bókhaldsstjóra og bókhaldsyfirmanns og aðgangsheimildinni **Skoða stillingar á röð sjálfvirkra fjárhagsjafnana** hefur verið bætt við hlutverk endurskoðanda, bókhaldsstjóra og bókhaldsyfirmanns fyrir sjálfvirkni fjárhagsjöfnunar. Þessi gjöld eru sjálfgefnar öryggisstillingar en hægt er að breyta þeim eftir þörfum fyrirtækisins.

## <a name="general-ledger-parameters-for-ledger-settlement-automation"></a>Fjárhagsfæribreytur fyrir sjálfvirkni í fjárhagsjöfnun

Reiturinn **Dæmigerð staða jöfnunar** gefur til kynna röðina sem sjálfvirk fjárhagsjöfnun verður unnin í. Til að setja upp eða skoða gildið **Dæmigerð staða jöfnunar** skal fara í **Fjárhagur \> Uppsetning \> Almennar fjárhagsfæribreytur** og velja flipann **Fjárhagsjafnanir**.

Þegar **Debet** er valið hefst sjálfvirka fjárhagsjöfnunarferlið debetmegin og leitar að samsvarandi kreditfærslu. Ef **Kredit** er valið hefst sjálfvirka fjárhagsjöfnunarferlið kreditmegin og leitar að samsvarandi debetfærslum. Þessi valkostur ætti að endurspegla dæmigerða stöðu aðallykilsins.

## <a name="processing-a-ledger-settlement-automation"></a>Sjálfvirkni við vinnslu fjárhagsáætlunar

Þegar sjálfvirkni er keyrð velur kerfið fjárhagsfærslur fyrir aðallyklana sem skilgreindir eru fyrir sjálfvirka röð ferlis. Það raðar færslunum eftir dagsetningu með því að nota dagsetningarbil frá upphafi reikningsársins til dagsetningarinnar þegar sjálfvirka ferlið er keyrt. Samsvörunin er byggð á tilgreindum samsvörunarskilyrðum. Nákvæm gildi fyrir upphæðir bókhaldsgjaldmiðils í debet- og kreditfærslu verða að stemma til að vera jafnaðar.

Á meðan aðallykill er í vinnslu vegna tilviks frá sjálfvirkri fjárhagsjöfnun er ekki hægt að birta hann á síðunni **Fjárhagsjafnanir**. Þú verður að bíða þar til sjálfvirkniferlinu er lokið. Mælt er með því að tímasetja sjálfvirkni ferlisins til að keyra utan vinnutíma til að koma í veg fyrir árekstra.

Sjálfvirkniferlið mun innihalda allar færslur sem uppfylla skilyrðið, nema færslur sem hafa verið merktar handvirkt fyrir jöfnun á síðunni **Fjárhagsjafnanir**.

## <a name="reversal-of-transactions-that-are-settled-by-the-automation-process"></a>Bakfærsla færslna sem eru afgreiddar með sjálfvirkniferlinu

Þú getur bakfært jöfnun sem var gerð sjálfvirku jöfnunarferli. Þegar færsla sem var jöfnuð af sjálfvirka ferlinu er bakfærð verður gildið **Sjálfvirkniregla** fjarlægt.
