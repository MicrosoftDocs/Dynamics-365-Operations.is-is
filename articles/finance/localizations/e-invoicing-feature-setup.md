---
title: Vinna með eiginleikauppsetningar
description: Þetta efnisatriði útskýrir hvernig á að setja upp eiginleika rafrænna reikninga.
author: dkalyuzh
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 41ffc9c7009291a55392e50c5e490d3288d122bc
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371922"
---
# <a name="work-with-feature-setups"></a>Vinna með eiginleikauppsetningar

[!include [banner](../includes/banner.md)]

Til að setja upp myndun rafrænna skráa og önnur vinnsluþrep (til dæmis stafræna undirritun skráa, senda þær á vefþjónustu ríkisins og fá svar eða geyma þær), setja upp vinnsluleiðslan, nothæfisreglur og breytur fyrir rafrænt. reikningseiginleikar.

Uppsetningarupplýsingarnar eru sameinaðar í *uppsetningu eiginleika* hugmynd, og hægt er að búa til, eyða, breyta. Fyrir fullgerðar útgáfur af eiginleikum rafrænna reikninga er einnig hægt að skoða upplýsingarnar.

Þú getur búið til eins marga eiginleika uppsetningarhluta og þú þarft til að skilgreina mismunandi aðstæður til að búa til, vinna og taka á móti rafrænum skrám. Þrátt fyrir að þessir eiginleikauppsetningaratriði hafi sjálfstæðar vinnsluaðgerðir og framkvæmdarskilyrði, eru þeir búnir til sem hluti af einum rafrænum reikningseiginleika og erfa lífsferil hans og dreifingarferli.

## <a name="add-a-feature-setup"></a>Bættu við eiginleikauppsetningu

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á **Eiginleikar rafrænna reikninga** síðu, veldu eiginleika útgáfu rafrænna reikninga sem hefur stöðuna **Drög**.
4. Á **Uppsetningar** flipa, veldu **Bæta við**.
5. Í **Búðu til eiginleikauppsetningu** fellivalmynd, í **Nýtt** reitahópur, veldu einn af eftirfarandi valkostum:
 
    - **Sérsniðin uppsetning** – Búðu til nýja eiginleikauppsetningu sem hefur tómar rásir, tóman vinnsluleiðslulista, tóman hluta fyrir gildandi reglur og sjálfgefið sett af breytum, allt eftir uppsetningargerðinni.
    - **Frá uppsetningu eiginleika** – Búðu til afrit af annarri eiginleikauppsetningu innan umfangs núverandi eiginleika rafrænna reikninga.

6. Ef þú valdir **Sérsniðin uppsetning** valmöguleika í síðasta skrefi, sláðu inn heiti og lýsingu á eiginleikauppsetningaratriðinu og síðan í **Gerð uppsetningar** reitahópur, veldu einn af eftirfarandi valkostum:

    - **Vinnsluleiðsla** – Veldu þennan valkost til að búa til og vinna úr rafrænum skjölum á útleið. Fyrir þessa uppsetningargerð býr kerfið til tóman vinnsluleiðslulista, tóman hluta fyrir gildandi reglur og sjálfgefið sett af breytum. Þú munt ekki geta unnið með rásirnar fyrir rafræn skjöl á heimleið.
    - **Gagnarás** – Veldu þennan valkost til að setja upp ferlið við að taka á móti rafrænum skjölum á heimleið frá einni af skilgreindum rásum og senda þau beint til Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management án frekari aðgerða. Fyrir þessa uppsetningargerð býr kerfið til fyrirfram skilgreindan lista yfir færibreytur fyrir gagnarásirnar, tóman hluta fyrir gildandi reglur og sett af sjálfgefnum breytum. Þú munt ekki geta bætt við neinum aðgerðum í vinnslupípunni.
    - **Gagnarás og vinnsluleiðsla** – Þessi uppsetningargerð líkist **Gagnarás** gerð uppsetningar. Hins vegar, áður en rafrænt skjal á heimleið er sent til fjármála- eða birgðakeðjustjórnunar, er hægt að setja upp viðbótaraðgerðir í vinnslupípunni.

7. Ef þú valdir **Gagnarás** eða **Gagnarás og vinnsluleiðsla** valmöguleika í síðasta skrefi, í **Veldu gagnarás** reit, verður þú að velja rásina til að samþætta við.
8. Velja **Stofna**.

Eftir að eiginleikauppsetning hefur verið búin til geturðu valið **Breyta** til að stilla það.

## <a name="edit-a-feature-setup"></a>Breyttu eiginleikauppsetningu

Það fer eftir tegund eiginleikauppsetningar, þú getur stillt ferlið við að búa til rafrænar skrár á útleið og senda þær á ytri rásir, eða taka á móti skjölum á heimleið og senda þau í fjármála- eða framboðskeðjustjórnunarforritið þitt.

### <a name="data-channel"></a>Gagnarás

A *gagnarás* tekur rafrænu skrána og annað hvort vinnur úr henni eða sendir hana beint til fjármála- eða birgðakeðjustjórnunar. Þessi valkostur er ekki í boði fyrir eiginleikauppsetningar á **Vinnsluleiðsla** tegund.

Til að setja upp gagnarás skaltu slá inn heiti rásarinnar. Skilgreindu síðan færibreyturnar, byggt á valinni rásargerð. Gagnarásaauðkennið verður að vísa til breytunnar sem er búið til sérstaklega til að auðkenna gagnarásina. Það verður notað sem viðmið í fjármála- eða framboðskeðjustjórnun.

Á **Viðhengissía** flipa, ættir þú að skilgreina sett af síum til að fá sérstakar skrár frá rásinni. Þú getur búið til nokkrar línur ef þú býst við að skrár muni hafa mismunandi skráarheiti, eða ef vinnsla verður á skrám á annan hátt eftir skráarnafninu. Hér eru helstu breytur:

- **Nafn** – Sláðu inn nafn skráarinnar sem kerfið mun vísa til við vinnslu. Í umsóknum um fjármála- og framboðskeðjustjórnun muntu geta séð skrárnar í innsendingarskránni.
- **Sía** - Skilgreindu síuna til að velja skrár.
- **Valfrjálst** – Ef gátreiturinn er hreinsaður er skráin nauðsynleg. Í þessu tilviki mun kerfið sýna villuboð ef rásirnar innihalda ekki skrár sem samsvara síunni. Þessi færibreyta á við um tölvupóst.

Ef rásin er pósthólf og tölvupóstur á heimleið inniheldur nokkur viðhengi, geturðu stillt reglur til að skilgreina hvernig þjónustan á að meðhöndla viðhengi. Þjónustan getur litið á hvert viðhengi sem sérstakan rafrænan reikning eða farið með eitt viðhengi sem aðalreikning og öll önnur viðhengi sem viðbætur.

### <a name="processing-pipeline"></a>Pípuvinnsla

A *vinnsluleiðslu* er sett af *aðgerðir* sem eru keyrðar í röð þar til þeim er lokið. Hægt er að nota vinnsluleiðslu til að setja upp ferlið til að búa til rafrænar skrár og framkvæma önnur skref (td undirrita skrár stafrænt, senda þær til ytri vefþjónustu og flokka svarið og taka á móti og vinna úr skjölum á heimleið).

Listi yfir aðgerðir er fyrirfram skilgreindur. Þú getur notað **Nýtt** og **Eyða** hnappa til að tilgreina samsetningu aðgerða sem rökrétt skilgreinir nauðsynlegt ferli til að senda inn eða taka á móti skjölum.

Röð aðgerða er mikilvæg. Þú getur breytt röðinni með því að nota **Upp** og **Niður** hnappa.

Hver aðgerð hefur sett af breytum sem þú getur stillt eða stillt. Sérstakt sett af breytum fer eftir tegund aðgerða.

- **Aðgerð** – Veldu gerð aðgerða.
- **Heiti aðgerða** – Sláðu inn heiti aðgerðarinnar. Þetta nafn mun birtast í innsendingarskrám og í skilaboðum í fjármála- og framboðskeðjustjórnunarforritum.
- **Lýsing** – Gefðu frekari upplýsingar um tilgang aðgerðarinnar í ferlinu.
- **Virkja tilraun aftur** – Ef þú velur þennan gátreit geturðu valið aðgerð í **Reyndu aftur aðgerðir** reit og stilla viðbótarfæribreytur á **Reyndu færibreytur aftur** flipa.

    Reyna aftur virkni gerir þér kleift að stilla hegðun þjónustunnar ef ekki er hægt að keyra ákveðna aðgerð. Til dæmis, ef ytri vefþjónustan sem þú ert að reyna að tengjast við svarar ekki geturðu tilgreint hversu oft kerfið ætti að reyna aftur tenginguna, með hvaða millibili og frá hvaða aðgerð í vinnslupípunni.

- **Flytja út niðurstöður** – Þú getur valið þennan gátreit fyrir *einn* aðgerðir í vinnslu. Rafrænu skrána sem aðgerðin framleiðir í Finance eða Supply Chain Management forritinu er síðan hægt að flytja út úr **Innsendingarskrá rafrænna skjala** síðu.

### <a name="applicability-rules"></a>Gildissviðsreglur

*Gildisreglur* eru stillanleg ákvæði sem veita samhengi til að keyra eiginleika rafrænna reikninga í gegnum rafræna reikningsgetu.
Viðskiptaskjöl sem eru send frá fjármála- eða birgðakeðjustjórnun til rafrænnar reikninga bera ekki skýra tilvísun sem gerir rafrænni reikningsgetu kleift að hringja í tiltekna útgáfu rafrænna reikningaeiginleika og tiltekinn eiginleika uppsetningarhluta til að vinna úr innsendingunni. Hins vegar, þegar viðskiptaskjal er rétt stillt, inniheldur það nauðsynlega þætti sem gera rafræna reikninga kleift að ákvarða hvaða útgáfu rafrænna reikningaeiginleika og vinnsluleiðsla verður að velja og keyra.

Gildisreglur gera rafrænum reikningaþjónustu kleift að finna nákvæmlega rafræna reikningseiginleika sem þarf að nota til að vinna úr skilum. Til að finna réttu eiginleikana, **Samhengi** reitir úr innsendu viðskiptaskjali eru jafnaðir við ákvæði úr gildandi reglum.

Þú getur unnið með gildandi reglur á eftirfarandi hátt:

- Veldu **Nýtt** að bæta nýju ákvæði við sett af gildandi reglum.
- Veldu **Eyða** að eyða ákvæði.
- Veldu nokkrar færslur og notaðu **Hópur** eða **Taka úr hópi** hnappinn til að búa til blöndu af hlutum eða rökréttum fullyrðingum. Veldu til dæmis línurnar sem þú vilt flokka og veldu síðan **Hópákvæði**. Þegar ákvæði eru flokkuð er nýjum dálki bætt við hnitanetið. Þessi dálkur tilgreinir rökræna rekstraraðilann fyrir flokkaða setninguna. Eftirfarandi gerðir rekstraraðila eru studdar:

    - Equal
    - Not equal
    - Stærra en/minna en
    - Stærra en eða jafnt og/minna en eða jafnt og
    - Contains
    - Byrja á

    > [!NOTE]
    > Þegar flokkun ákvæðis er afturkölluð skal alltaf byrja á innsta flokkunarstiginu.

### <a name="variables"></a>Breytur

*Breytur* gefa þér meiri sveigjanleika þegar þú setur upp vinnsluleiðslu og gagnaflæði á milli aðgerða. Þú getur vísað til breytu í sumum aðgerðabreytum til að geyma gögn eða rafrænar skrár tímabundið. Sumar breytur eru notaðar til að koma gögnum á milli fjármála- eða framboðskeðjustjórnunarforrita og rafrænnar reikningaþjónustu.

Kerfið býr til nokkrar breytur sjálfgefið. Til dæmis, the **BusinessDocumentDataModel** breyta inniheldur viðskiptagögn í JavaScript Object Notation (JSON) uppbyggingu sem kemur í símtalinu frá tengda forritinu meðan á innsendingarferlinu stendur.

Eftirfarandi gerðir af breytum eru fáanlegar:

- **Stöðugt** – Gámur til að geyma tímabundin gögn sem eru notuð við vinnslu leiðsluaðgerða.
- **Frá viðskiptavini** – Innihald breytunnar er sótt frá Dynamics 365 biðlara þegar innsendingarferlið er keyrt.
- **Til viðskiptavinar** – Innihald breytunnar er gert aðgengilegt fyrir innflutning af Dynamics 365 biðlara þegar innsendingarferlið er keyrt.
- **Gagnategund** – Veldu gagnategund upplýsinganna sem eru geymdar í breytunni.

### <a name="parameters"></a>Færibreytur

The **Slökktu á minni viðskiptagagna** valmöguleikinn er notaður til að hámarka uppbyggingu viðskiptagagnamagns sem kemur frá Finance eða Supply Chain Management forritinu við rafræna skjalaskil. Hagræðing hjálpar til við að draga úr gögnum sem fara inn í rafræna reikningaþjónustu til frekari umbreytingar í nauðsynlega rafræna skrá. Sjálfgefið gildi er **Nei**.

- **Já** – Fjármál eða birgðakeðjustjórnun mun senda JSON skrá yfir **Reikningslíkan** eða **Fjárhagslíkan** (fyrir Brasilíu) uppbyggingu sem er skilgreind í **Rafræn skýrslugerð** mát. Allir þættir líkansins eru fylltir með viðskiptagögnum á umsóknarhlið, óháð endanlegri rafrænni skráargerð. Líkön innihalda venjulega fleiri viðskiptagögn en skráaruppbyggingin krefst og það getur þurft lengri tíma til að búa til þessi gögn í forritinu. Verðmæti á **Já** fyrir þennan valkost er krafist í þeim sjaldgæfum tilfellum að þú viljir búa til mismunandi úttaksskrár í einni rafrænni innheimtueiginleika og eiginleikauppsetningu. Verðmæti á **Já** er gagnlegt þegar þú bilar aðstæður þínar, uppbyggingu rafrænna skráa og heilleika viðskiptagagnanna.
- **Nei** – Fjármála- eða birgðakeðjustjórnun mun hringja í fyrsta sinn í þjónustuna án nokkurra viðskiptagagna. Tilgangur þessa símtals er að fá upplýsingar um rafræna skýrslugerð (ER) stillingar sem verða notaðar fyrir rafræna skráarbreytingu í vinnslupípunni. Þessum upplýsingum er skilað til forritsins sem notar þær til að ákvarða undirmengi viðskiptagagna sem ætti að vera með í JSON skránni í **Reikningslíkan** eða **Fjárhagslíkan** (fyrir Brasilíu) uppbyggingu. Verðmæti á **Nei** fyrir þessi valkostur hjálpar til við að draga úr magni viðskiptagagna sem umsóknin sendir til þjónustunnar, vegna þess að umsóknin getur aðeins sent inn þau viðskiptagögn sem þarf til að búa til rafræna skrá.

### <a name="validate-a-feature-setup"></a>Staðfestu eiginleikauppsetningu

Þú getur keyrt löggildingu til að athuga samkvæmni allrar uppsetningar. Til dæmis, ef lögboðin færibreyta fyrir aðgerð hefur verið skilin eftir auð, greinir staðfestingin þetta ósamræmi og þú færð viðvörunarskilaboð.

- Á **Uppsetning eiginleikaútgáfu** síðu, á aðgerðarrúðunni, veldu **Staðfesta**.

## <a name="delete-a-feature-setup"></a>Eyða eiginleikauppsetningu

1. Á **Eiginleikar rafrænna reikninga** síðu, veldu eiginleika útgáfu rafrænna reikninga sem hefur stöðuna **Drög**.
2. Á **Uppsetningar** flipa, veldu **Eyða**.
3. Í skilaboðareitnum sem birtist skaltu velja **Já** til að staðfesta að þú viljir eyða eiginleikauppsetningunni.
