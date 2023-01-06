---
title: Vinna með uppsetningu eiginleika
description: Þessi grein útskýrir hvernig á að setja upp eiginleiki rafrænnar reikningsfærslu.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 0d64757871c12ae914f7ace4cc0121a08a32a9d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272247"
---
# <a name="work-with-feature-setups"></a>Vinna með uppsetningu eiginleika

[!include [banner](../includes/banner.md)]

Til að setja upp myndun rafrænna skráa og önnur vinnsluskref (til dæmis undirrita skrár stafrænt, senda þær inn á vefþjónustu yfirvalda og fá svar, eða geyma þær) skal setja upp sölukeðju úrvinnslu, reglur um gildistíma og breytur fyrir eiginleika rafrænnar reikningsfærslu.

Upplýsingar um uppsetningu eru sameinaðar í *eiginleikauppsetningu* og er hægt að búa til, eyða, breyta. Fyrir tilbúnar útgáfur af eiginleikum rafrænnar reikningsfærslu er einnig hægt að skoða upplýsingarnar.

Hægt er að búa til eins mörg atriði eiginleikauppsetningar og þörf er á til að skilgreina mismunandi aðstæður til að mynda, vinna úr og taka á móti rafrænum skrám. Þótt þessi atriði eiginleikauppsetningar séu með sjálfstæðar vinnsluaðgerðir og sérstök skilyrði fyrir framkvæmd eru þau búin til sem hluti af einum eiginleika rafrænnar reikningsfærslu og erfa stuðningstíma hans og uppsetningarferli.

## <a name="add-a-feature-setup"></a>Bæta við uppsetningu eiginleika

1. Skráðu þig inn á RCS-reikninginn þinn.
2. Á vinnusvæðinu **Altækur eiginleiki**, í hlutanum **Eiginleikar**, skal velja reitinn **Rafræn reikningsfærsla**.
3. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleikaútgáfu rafrænnar reikningsfærslu sem er með stöðuna **Uppkast**.
4. Í flipanum **Uppsetningar** skal velja **Bæta við**.
5. Í fellilistanum **Stofna uppsetningu eiginleika**, í reitahópnum **Nýtt**, skal velja einn af eftirfarandi valkostum:
 
    - **Sérsniðin uppsetning** – Búðu til nýja uppsetningu eiginleika sem er með tómum rásum, tómum lista yfir vinnslukeðju, auðan hluta fyrir reglur um gildissvið og sjálfgefið safn af færibreytum, eftir því hver gerð uppsetningarinnar er.
    - **Úr uppsetningu eiginleika** – Búðu til afrit af annarri eiginleikauppsetningu í umfangi núverandi eiginleika rafrænnar reikningsfærslu.

6. Ef þú valdir valkostinn **Sérsniðin uppsetning** í síðasta skrefi skaltu slá inn nafn og lýsingu á atriði eiginleikauppsetningar og síðan í reitahópnum **Gerð uppsetningar** skaltu velja einn af eftirfarandi valkostum:

    - **Vinnslukeðja** – Veldu þennan valkost til að búa til og vinna úr rafrænum skjölum á útleið. Fyrir þessa gerð uppsetningar býr kerfið til tóman lista yfir vinnslukeðju, auðan hluta fyrir reglur um gildissvið og sjálfgefið safn af færibreytum. Þú getur ekki unnið með rásirnar fyrir rafræn skjöl á innleið.
    - **Gagnarás** – Veldu þennan valkost til að setja upp ferlið fyrir að taka á móti rafrænum skjölum á innleið úr einni af skilgreindu rásunum og senda þau beint til Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management án frekari aðgerða. Fyrir þessa gerð uppsetningar býr kerfið til fyrirframskilgreindan lista yfir færibreytur fyrir gagnarásirnar, auðan hluta fyrir reglur gildissviðs og safn af sjálfgefnum færibreytum. Þú getur ekki bætt við neinum aðgerðum í vinnslusölukeðjunni.
    - **Gagnarás og pípuvinnsla** – Þessi uppsetningargerð líkist uppsetningargerðinni **Gagnarás**. Áður en rafrænt skjal á innleið er sent áfram til Finance eða Supply Chain Management geturðu hins vegar sett upp viðbótaraðgerðir í vinnslukeðjunni.

7. Ef þú valdir valkostinn **Gagnarás** eða **Gagnarás og vinnslukeðja** í síðasta skrefi þarftu í reitnum **Velja gagnarás** að velja rásina til að samþætta við.
8. Velja **Stofna**.

Eftir að búið er að stofna eiginleikauppsetninguna er hægt að velja **Breyta** til að skilgreina hana.

## <a name="edit-a-feature-setup"></a>Breyta uppsetningu eiginleika

Í samræmi við gerð eiginleikauppsetningar er hægt að stilla ferlið við að búa til rafrænar skrár á útleið og senda þær inn á ytri rásir eða taka á móti skjölum á innleið og senda þau til Finance eða Supply Chain Management.

### <a name="data-channel"></a>Gagnarás

*Gagnarás* tekur við rafrænu skránni og annaðhvort vinnur úr henni eða sendir hana beint í Finance eða Supply Chain Management. Þessi valkostur er ekki í boði fyrir gerðina **Pípuvinnsla**.

Til að setja upp gagnarás er heiti rásarinnar slegið inn. Skilgreinið síðan færibreyturnar, byggðar á valinni rásartegund. Auðkenni gagnarásar verður að vísa til breytunnar sem er búin til sérstaklega til að bera kennsl á gagnarásina. Það verður notað sem tilvísun í Finance og Supply Chain Management.

Í flipanum **Viðhengjasía** ættirðu að skilgreina safn af síum til að fá tilteknar skrár úr rásinni. Hægt er að búa til nokkrar línur ef gert er ráð fyrir að skrár séu með mismunandi skráarendingar eða ef vinna þarf úr skrám á mismunandi hátt eftir því hvert skráarheitið er. Hér eru aðalfæribreyturnar:

- **Heiti** – Færa skal inn heiti skrárinnar sem kerfið mun vísa til meðan á vinnslu stendur. Í Finance og Supply Chain Management geturðu séð skrárnar í innsendingarkladdanum.
- **Sía** – Skilgreina síu til að velja skrár.
- **Valfrjálst** – Ef gátreiturinn er skráin nauðsynleg. Í þessu tilviki mun kerfið sýna villuboð ef rásir innihalda ekki skrár sem samsvara síunni. Þessi færibreyta á við um tölvupósta.

Ef rásin er pósthólf og tölvupóstur á innleið inniheldur nokkur viðhengi er hægt að stilla reglur til að skilgreina hvernig þjónustan á að meðhöndla viðhengi. Þjónustan getur litið á hvert viðhengi sem sérstakan rafrænan reikning eða hún getur meðhöndlað eitt viðhengi sem meginreikning og öll önnur viðhengi sem viðbætur.

### <a name="processing-pipeline"></a>Pípuvinnsla

*Vinnslukeðja* er safn *aðgerða* sem eru keyrðar hver á eftir annarri þar til þeim er lokið. Hægt er að nota vinnslukeðju til að setja upp ferli til að búa til rafrænar skrár og framkvæma önnur skref (til dæmis undirrita skrár með stafrænum hætti, senda þær til utanaðkomandi vefþjónustu og greina svarið og taka á móti og vinna úr skjölum á innleið).

Listi yfir aðgerðir er fyrirfram skilgreindur. Hægt er að nota hnappana **Nýtt** og **Eyða** til að tilgreina samsetningu aðgerða sem skilgreina á rökréttan hátt ferlið sem þarf til að senda inn eða taka á móti skjölum.

Röð aðgerða er mikilvæg. Hægt er að breyta röðinni með því að nota **Upp** og **Niður** hnappana.

Hver aðgerð er með sett af færibreytum sem þú getur stillt eða breytt. Röð færibreyta fer eftir tegund aðgerðarinnar.

- **Aðgerð** – Veljið þessa gerð aðgerðar.
- **Aðgerðarheiti** – Færið inn heiti aðgerðarinnar. Þetta heiti mun birtast í innsendingarklöddum og í skilaboðum í Finance og Supply Chain Management.
- **Lýsing** – Veittu frekari upplýsingar um tilgang aðgerðarinnar í ferlinu.
- **Virkja aðra tilraun** – Ef þessi gátreitur er valinn er hægt að velja aðgerð í reitnum **Reyna aðgerð aftur** og stilla viðbótarfæribreytur í flipanum **Færibreytur tilraunar**.

    Aðgerðin að reyna aftur gerir þér kleift að stilla hegðun þjónustunnar ef ekki er hægt að keyra tiltekna aðgerð. Til dæmis ef ytri vefþjónustan sem þú ert að reyna að tengjast svarar ekki geturðu tilgreint hversu oft kerfið ætti að reyna tenginguna aftur, með hvaða millibili og úr hvaða aðgerð í vinnslukeðjunni.

- **Flytja út niðurstöður** – Þú getur valið þennan gátreit fyrir *eina* aðgerð í pípuvinnslunni. Þá er hægt að flytja út rafrænu skrána sem aðgerðin framleiðir í Finance eða Supply Chain Management úr síðunni **Innsendingarkladdi rafrænna skjala**.

### <a name="applicability-rules"></a>Gildissviðsreglur

*Gildissviðsreglur* eru stillanleg ákvæði sem veita samhengi til að keyra eiginleika rafrænnar reikningsfærslu í gegnum safn af möguleikum rafrænnar reikningsfærslu.
Viðskiptaskjöl sem eru send úr Finance eða Supply Chain Management til rafrænnar reikningsfærslu bera ekki með sér sérstaka tilvísun sem gerir safn af möguleikum rafrænnar reikningsfærslu kleift að kalla fram tiltekna útgáfu af eiginleika rafrænnar reikningsfærslu og tiltekið atriði eiginleikauppsetningar til að vinna úr innsendingunni. Þegar viðskiptaskjal er stillt á réttan hátt inniheldur það hins vegar nauðsynlegar einingar sem gera rafrænni reikningsfærslu kleift að ákvarða hvaða eiginleikaútgáfu rafrænnar reikningsfærslu og vinnslukeðju þarf að velja og keyra.

Gildissviðsreglur gera rafrænni reikningsfærsluþjónustu kleift að finna nákvæmlega þá eiginleika rafrænnar reikningsfærslu sem þarf að nota til að vinna úr innsendingunni. Til að finna réttu eiginleikana eru reitirnir **Samhengi** úr innsendu viðskiptaskjali samsvaraðir við ákvæði úr gildisssviðsreglunum.

Hægt er að vinna með gildissviðsreglu á eftirfarandi hátt:

- Veljið **Nýtt** til að bæta nýju ákvæði við reglur um gildissvið.
- Veljið **Eyða** til að eyða ákvæði.
- Veldu nokkrar færslur og notaðu hnappinn **Flokka** eða **Afflokka** til að búa til samsetningu atriða eða rökrétt yfirlit. Til dæmis skal velja línurnar sem á að flokka saman og velja svo **Flokka ákvæði**. Þegar ákvæði eru flokkuð er nýjum dálki bætt við hnitanetið. Þessi dálkur tilgreinir rökvirkinn fyrir flokkað ákvæði. Eftirfarandi stjórnendangerðir eru studdar:

    - Equal
    - Not equal
    - Stærra en/minna en
    - Stærra en eða jafnt og/minna en eða jafnt og
    - Contains
    - Byrja á

    > [!NOTE]
    > Þegar flokkun ákvæðis er afturkölluð skal alltaf byrja á innsta flokkunarstiginu.

### <a name="variables"></a>Breytur

*Breytur* gefa þér meiri sveigjanleika þegar þú setur upp vinnslukeðju og gagnaflæði á meðal aðgerða. Hægt er að vísa í breytu í sumum færibreytum aðgerðar til að geyma tímabundið gögn eða rafrænar skrár. Sumar breytur eru notaðar til að senda gögn milli Finance eða Supply Chain Management og rafrænnar reikningsfærsluþjónustu.

Kerfið býr til nokkrar breytur sjálfgefið. Til dæmis inniheldur breytan **BusinessDocumentDataModel** viðskiptagögn í skipulagi JavaScript Object Notation (JSON) sem kemur í kalli frá tengda forritinu í innsendingarferlinu.

Eftirfarandi gerðir breyta standa til boða:

- **Stöðugt** – Geymsla fyrir tímabundin gögn sem eru notuð í aðgerðum pípuvinnslu.
- **Frá biðlara** - Efni breytunnar er fengið frá biðlara Dynamics 365 þegar innsendingarferlið er keyrt.
- **Til biðlara** - Efni breytunnar er gert aðgengilegt fyrir innflutning af biðlara Dynamics 365 þegar innsendingarferlið er keyrt.
- **Gagnagerð** – Veldu gagnagerð upplýsinganna sem eru geymdar í breytunni.

### <a name="parameters"></a>Færibreytur

Valkosturinn **Gera viðskiptagagnaminnkun óvirka** er notaður til að fínstilla skipulagið fyrir innihald viðskiptagagna sem kemur úr Finance eða Supply Chain Management við innsendingu rafræns skjals. Fínstilling hjálpar til við að fækka gögnum sem fara í rafræna reikningsfærsluþjónustu til frekari umbreytinga í nauðsynlega rafræna skrá. Sjálfgefið gildi er **Nei**.

- **Já** – Finance eða Supply Chain Management mun senda JSON-skrá af skipulaginu **Reikningslíkan** eða **Fjárhagslíkan** (fyrir Brasilíu) sem er skilgreint í einingunni **Rafræn skýrslugerð**. Allar einingar líkansins eru fylltar út með viðskiptagögnum forritsmegin burtséð frá lokaskipulagi rafrænnar skráar. Líkön innihalda yfirleitt meiri viðskiptagögn en skipulag markskráarinnar krefst og hægt er að krefjast lengri tíma til að búa til þessi gögn í forritinu. Gildið **Já** fyrir þennan valkost er nauðsynlegur sjaldgæfum tilfellum þar sem þú vilt búa til mismunandi úttaksskrár í einum eiginleika rafrænnar reikningsfærslu og eiginleikauppsetningu. Gildið **Já** er gagnlegt þegar þú úrræðaleitar aðstæðurnar, skipulag rafrænna skráa og heilleika viðskiptagagnanna.
- **Nei** – Finance eða Supply Chain Management kalla fyrst á þjónustuna án viðskiptagagna. Tilgangur kallsins er að fá upplýsingar um skilgreiningu rafrænnar skýrslugerðar sem verður notuð fyrir umbreytingu rafrænnar skráar í vinnslukeðjunni. Þessum upplýsingum er skilað til forritsins sem notar þær til að ákvarða undirsafn viðskiptagagna sem eiga að vera í JSON-skránni fyrir skipulagið **Reikningslíkan** eða **Fjárhagslíkan** (fyrir Brasilíu). Gildið **Nei** fyrir þennan valkost hjálpar til við að minnka magn viðskiptagagna sem forritið sendir inn til þjónustunnar vegna þess að forritið getur aðeins sent inn viðskiptagögn sem krafist er til að geta búið til rafræna skrá.

### <a name="validate-a-feature-setup"></a>Villuleita uppsetningu eiginleika

Hægt er að keyra villuleit til að kanna samræmi allrar skilgreiningarinnar. Ef til dæmis tiltekin færibreyta fyrir aðgerð er áskilin en gildi hennar er autt, ber villuleitin kennsl á þetta ósamræmi og upp kemur villa.

- Á síðunni **Uppsetning á útgáfu eiginleika**, á aðgerðasvæðinu, skal velja **Villuleita**.

## <a name="delete-a-feature-setup"></a>Eyða uppsetningu eiginleika

1. Á síðunni **Eiginleikar rafrænnar reikningsfærslu** skal velja eiginleikaútgáfu rafrænnar reikningsfærslu sem er með stöðuna **Uppkast**.
2. Í flipanum **Uppsetningar** skal velja **Eyða**.
3. Veljið **Já** í skilaboðaglugganum sem opnast til að staðfesta að ætlunin sé að eyða uppsetningu eiginleikans.
