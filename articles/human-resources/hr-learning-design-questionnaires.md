---
title: Búa til spurningalista
description: Þessi skrá lýsir ferlinu við stofnun spurningalista. Fyrsta skrefið er að hanna spurningalista. Þegar spurningalisti er hannaður þarf ekki aðeins að skrifa spurningar og svör, heldur einnig að stofna skipulag sem leyfir að svör séu skráð og sett upp í töflu.
author: andreabichsel
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KCMCollectionType, KMAnswerCollection, KMCollection, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 17341
ms.assetid: b27e2f12-c7a0-4a54-b8d8-17819f8a1c72
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 3f7f7d68caf12c33059d2f871fe3f4a036c89f35
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115127"
---
# <a name="create-questionnaires"></a>Búa til spurningalista

Þessi skrá lýsir ferlinu við stofnun spurningalista. Fyrsta skrefið er að hanna spurningalista. Þegar spurningalisti er hannaður þarf ekki aðeins að skrifa spurningar og svör, heldur einnig að stofna skipulag sem leyfir að svör séu skráð og sett upp í töflu. 

Vandlega hannaður spurningalisti eykur gæði gagnanna sem er safnað. Með vandlegri hönnun er betur hægt að velja viðeigandi valkosti á viðeigandi tíma fyrir spurningalista. Eftirfarandi punktar geta hjálpað þér að áætla skilvirkan spurningalista:

-   Skilgreindu skýrt tilgang spurningalistans til að aðstoða við að tryggja að spurningar styðji tilganginn.
-   Ákvarðaðu hvaða einstaklingur eða hópur fólks á að ljúka spurningalistanum.
-   Skrifaðu spurningar sem birtist á spurningalistanum og hafðu svarmöguleika með, ef við á.
-   Vertu viss spurningalistinn streymi röklega, svo að svarendur haldi sig við efnið.
-   Raðaðu spurningum og svörum í pöntun sem þeir skulu sýndir sem svarendur í.
-   Ákeddu hvort meta skuli niðurstöðurnar, ef þá á við.
-   Ákveddu hvort frekari aðgerðir þurfi. Til dæmis þarf að ákvarða hvort og hvernig eigi að flokka niðurstöður, hvort tímamarka sé krafist eða hvort allar spurningar verða að vera skylda.

Hönnunaráfanginn inniheldur fjórar gerðir verkafna sem ljúka verður við í þessari röð:

1.  Settu upp forsendur, eins og þarf.
2.  Settu upp svarflokka og svör, ef við á.
3.  Settu upp spurningar og tengsl þeirra við svarflokka.
4.  Settu upp spurningalistann sjálfan og tengdu spurningar við hann.

## <a name="prerequisites"></a>Skilyrði
Sumar forsendur verða að vera til staðar áður en hægt er að stofna spurningalista, svör og spurningar. Hins vegar eru ekki allar forsendur áskildar fyrir fulla virkni.

### <a name="required"></a>Áskilið

| Skilyrði        | Lýsing                |
|---------------------|----------------------------|
| Gerðir spurningalista | Flokka spurningalista. |
| Gerðir spurninga      | Flokka spurningar.      |

### <a name="optional"></a>Valfrjálst

| Skilyrði             | Lýsing                                                    |
|--------------------------|----------------------------------------------------------------|
| Spurningalistafæribreytur | Breyttu grunnstýringum og sjálfgefnum stillingum fyrir spurningalista. |

### <a name="questionnaire-types"></a>Gerðir spurningalista

Gerðir spurningalista eru nauðsynlegar og verður að vera úthlutað þegar spurningalisti er stofnaður. Gerðir spurningalista hjálpa við að stjórna og flokka spurningalista á auðveldari hátt. Notaðu gerðir spurningalista til að flokka spurningalista og aðgreina þá sundur. Til dæmis, ef um marga mismunandi spurningalista er að ræða er hægt að auðvelda leit að ákveðnum spurningalista með því að sía þá eftir gerðum. Hér eru nokkur dæmi um gerðir spurningalista:

-   Þróun mannauðsstjórnunar
-   Viðskiptavinakannanir
-   Endurskoðunarferli

### <a name="question-types"></a>Gerðir spurninga

Gerðir spurninga eru nauðsynlegar og verður að vera úthlutað þegar spurning er búin til. 

Notaðu gerðir spurninga til að flokka spurningar fyrir skýrslugerð. Gerðir spurninga auðvelda einnig að finna spurningar, þar sem hægt er að nota gerðir sem síur á síðunni **Spurningar**. Hér eru nokkur dæmi um gerðir spurninga:

-   Starfsmannahald
-   Fyrirtækjastjórnun
-   Námskeiðamat

### <a name="questionnaire-parameters"></a>Spurningalistafæribreytur

Færibreytur spurningalista eru valfrjálsir. Þær eru hugsanlega ekki notaðar, eftir þörfum fyrirtækisins. 

Færibreytur spurningalista skilgreina nafnleysi, númeraraðakóða og tilvísunargerðir spurningalista. Þegar fyrirtæki dreifir spurningalista getur valkosturinn að leyfa svarendum að halda nafnleysi valdið áhyggjum. 

Númeraraðakóðar eru notaðir til að skipuleggja spurningar og svör. Samkvæmt þessum kóða númeraraða er gildum sjálfkrafa úthlutað á vörur. 

Þú ættir að skilgreina allar færibreytur áður en þú byrjar að stofna gögnin þín. Hægt er að breyta færibreytustillingum spurningalista hvenær sem er.

## <a name="questionnaire-components"></a>Íhlutir spurningalista
Spurningalistar snúast um þrjú aðalatriði: svarflokka sem innihalda svör fyrir spurningar með mörgum svarmöguleikum, spurningar og spurningalistann sjálfan. Einnig er hægt að flokka spurningar í spurningalista í niðurstöðuflokk. Niðurstöðuflokkar gera kleift að flokka spurningar og veita frekari greiningu á spurningalistanum. 

[![QuestionnaireComponents](./media/questionnairecomponents-1024x615.png)](./media/questionnairecomponents.png)

### <a name="answer-groups-and-answers"></a>Svarflokkar og svör

Til eru tvær leiðir fyrir svarendur að svara spurningu, eftir efni spurningarinnar:

-   Opnar spurningar krefjast ekki svara á sérstöku sniði. Svarendur geta fært svar inn sem texta, tölu eða dagsetningu og tíma. Þessar spurningar krefjast þess yfirleitt að svarandinn veiti huglægar upplýsingar í svörum sínum, eins og álit, lýsingu, mat eða áætlun.
-   Lokaðar spurningar krefjast að svarandi velji svar úr lista af mögulegum réttum svörum.

Til að sjá lista yfir möguleg svör fyrir lokaðar spurningar, er hægt að stofna svörin á síðunni **Svarflokkar**. 

Svarflokkar og svör eru íhlutir sem mynda meginmál upplýsinga sem spurningar eru stofnaðar úr. Eftir að þú stofnar svarflokk geturðu tengt svarflokkinn við spurningu í reitnum **Svarflokkur** á síðunni **Spurningar**. 

Hægt er að nota svarflokk fyrir fleiri en eina spurningu í sama spurningalista og einnig í einum eða fleiri spurningalistum. 

> [!NOTE]
> Ef breytt er svartexta í svarflokki sem hefur þegar verið notaður í fullkláruðum spurningalistum getur orðið erfitt að meta gögn og niðurstöður spurningalista gætu verið ekki lengur gildar. Ef breyta verður svarflokki skal athuga að stofna nýjan svarflokk í stað þess að breyta fyrirliggjandi flokki. Ekki er hægt að eyða svarflokkum sem eru tengdir spurningu eða svari eða sem hefur verið svarað.

### <a name="questions"></a>Spurningar

Spurningalisti verður að innihalda spurningar. Spurningar geta verið opnar eða lokaðar.

-   Svör við opnum spurningum er ekki stjórnað og svarendur geta slegið inn svör sín.
-   Lokaðar spurningar krefjast lista yfir fyrirfram skilgreinda valkosti svara og hægt er að byggja spurningarnar upp svo að svarandinn velji mörg svör. Spurningarnar ætti að hanna til fá fram ákveðnar upplýsingar frá svaranda og verða að vera tengdar svarflokki sem veitir svarmöguleika fyrir hverja lokaða spurningu. 

    > [!NOTE]
    > Áður en hægt er að setja upp lokaðar spurningar, verður að stofna svarflokk og svör.

Hægt er að raða spurningum í skilyrðisbundið spurningastigveldi svo að aukaspurningar velta á svarinu sem svarandi velur fyrir fyrri spurningu. Hægt er að skrifa spurningar fyrst og raða þeim í stigveldi síðar.

## <a name="setting-up-questionnaires"></a>Uppsetning spurningalista

> [!NOTE]
> Áður en hægt er að setja upp spurningalista, verður að setja upp svör, spurningar og forsendur. 

Fyrir hvern spurningalista er hægt að tilgreina eftirfarandi upplýsingar:

-   Heildartími eða tímamörk til að svara skylduspurningum.
-   Hvort allar spurningar eru áskildar.
-   Hvort reikna eigi punkta í spurningalista.
-   Hvernig á að flokka niðurstöður.
-   Hvort spurningalistinn verður tiltækur fyrir takmarkaðan hóp svarenda.
-   Hvort að skjámyndarsniðmát sé sýnt sem bakgrunnur fyrir aftan hverja síðu í spurningalistanum.
-   Hvort viðbótarathugasemda er krafist til að útskýra markmið spurningalistans fyrir svarendum.
-   Hvort birta eigi spurningar í fastri röð eða velja þær af handahófi úr spurningasafni.
-   Hvort spurninga verði aðeins spurt ef tiltekin svör eru gefin út fyrir fyrri svör.

### <a name="set-up-a-questionnaire"></a>Setja upp spurningalista

Aðalsíðan sem er notuð til að setja upp spurningalista er síðan **Spurningalistar**. Til að setja upp spurningarlista skal ljúka eftirfarandi verkum:

1.  Stofna spurningalista.
2.  Fylgið einu af þessum skrefum til að tengja spurningar við spurningalista:
    -   Ef verið er að nota niðurstöðuflokka er hægt að tengja spurningar við spurningalista með niðurstöðuflokkum. Fyrst skal setja upp niðurstöðuflokka fyrir spurningalista og bæta síðan spurningunum við niðurstöðuflokkana.
    -   Ef ekki er verið að nota niðurstöðuflokka er hægt að tengja spurningar beint við spurningalistann.

3.  Settu upp skilyrðisbundið spurningastilgveldi, ef með þarf.
4.  Prófa spurningalistann.

Á síðunni **Spurningalistar** er smellt á **Sannprófa** til að prófa hvort spurningalistinn sé settur rétt saman. Hins vegar er einnig góð hugmynd að ljúka spurningalistanum og prófa hann sjálfur áður en honum er dreift.

### <a name="modify-a-questionnaire"></a>Breyta spurningalista

Á síðunni **Spurningalistar** er hægt að ljúka eftirfarandi verkum:

-   Breyttu upplýsingum í spurningalistanum, eins og niðurstöðuflokki og spurningum.
-   Eyða og bæta við spurningum.
-   Gera breytingar á niðurstöðuflokki og raðnúmeri. 

> [!CAUTION]
> Farið varlega þegar breytingar eru gerðar á spurningalistum sem þegar hefur verið svarað. Breytingar geta dregið úr nákvæmni upplýsinga og þess vegna gert þær að lélegum grunni fyrir mat. Betra getur verið að útbúa nýja spurningu en að breyta spurningu sem þegar hefur verið svarað.

Í spurningalista er ekki hægt að eyða eftirfarandi gerðum spurninga:

-   Spurningar sem eru tengdar við lista
-   Spurningum sem þegar hefur verið svarað og birtast þar af leiðandi í svarglugganum **Svör**.

### <a name="result-groups"></a>Niðurstöðuflokkar

Niðurstöðuflokkar eru valfrjálsir þegar spurningar eru tengdar við spurningalista. 

Niðurstöðuflokkur er notaður til að reikna stig og flokka niðurstöður spurningalista. Ef þú notar niðurstöðuflokka er hægt að framkvæma eftirfarandi verk:

-   Meta niðurstöður spurningalista sem byggja á stigagögnum.
-   Meta stigafjölda svaranda fyrir hvern niðurstöðuflokk sem er settur upp.
-   Mynda talnagögn fyrir hvern niðurstöðuflokk til að hjálpa til við að greina niðurstöður.
-   Prenta skýrslu sem sýnir niðurstöður fyrir hvern niðurstöðuflokk og einnig valfrjáls stig/textar sem byggjast á stigum sem fengin eru í hverjum niðurstöðuflokki.

> [!NOTE]
> Áður en hægt er að setja upp niðurstöðuflokka, verður að ljúka eftirfarandi verkum:

-   Settu upp lokaðar spurningar. Fyrir lokaða spurningu verður inntakið á síðunni **Spurningar** að vera **Gátreitur**, **Aukahnappur** eða **Samsettur gluggi**.
-   Skilgreindu stig fyrir svörin í svarflokkunum sem eru úthlutaðir hverri spurningu.
-   Setja upp spurningalista.

Til að tengja spurningar við spurningalista með niðurstöðuflokkum þarf fyrst að setja upp niðurstöðuflokka fyrir spurningalista og bæta síðan spurningunum við niðurstöðuflokkana. Ef niðurstöðuflokkar eru ekki notaðir er hægt að tengja spurningar beint við spurningalistann. 

Hægt er að setja upp marga niðurstöðuflokka til að meta stig sem svarandi nær í hverjum flokki. Þegar spurningalista er lokið er hægt að skoða punkta sem hefur verið náð fyrir hvern niðurstöðuflokk. 

> [!TIP]
> Til að meta spurningalista með því að nota stig en ekki aðskilda flokka, er hægt að bæta öllum spurningum við í einn niðurstöðuflokk. 

Fyrir hvern niðurstöðuflokk er einnig hægt að setja upp ein eða fleiri punktabyggð skilaboð sem svarendur fá eftir að þeir ljúka við spurningalista. Textinn sem birtist getur verið breytilegur eftir þeirri einkunn sem svarandinn nær í niðurstöðuflokki. Til að nota punktabyggð skilaboð verður að skilgreina punktabil og lýsingu á hverju bili. Þegar svarandi nær stigi á tilteknu bili er textinn fyrir það bil innifalinn í niðurstöðuskýrslunni. 

Þar sem niðurstöðuflokkur tengist stigum sem eru tengd við tiltekið safn spurninga í spurningalista er aðeins hægt að nota tiltekinn niðurstöðuflokk fyrir spurningalista.

#### <a name="example-pointstexts-for-result-group-3"></a>Dæmi: Stig/textar fyrir niðurstöðuflokk 3

Verið er að nota spurningalista fyrir leiðtogapróf með 15 spurningum í þremur flokkum. Þú stofnar þrjá niðurstöðuflokka og bætir fimm spurningum við hvern niðurstöðuflokk. Stig eru svo lögð saman í flokkunum þremur. Niðurstöðuflokkarnir þrír eru eftirfarandi:

-   Sköpunarhæfni
-   Leiðtogahæfni
-   Tæknileg hæfni

Til að nota stigabyggð skilaboð þarf að setja upp textabil fyrir hvern niðurstöðuflokk. Hverri spurningu er úthlutað tveimur stigum. Því er hámarksfjölda stigasamtölu í hverjum niðurstöðuflokki 10. 

Eftirfarandi tafla sýnir stigabyggð skilaboð sem eru skilgreind fyrir niðurstöðuflokkinn „leiðtogahæfni“.

| Stigabil | Texti                                       |
|----------------|--------------------------------------------|
| 1 til 3         | Þú hefur meðalleiðtogahæfni.     |
| 4 til 7         | Þú hefur góða leiðtogahæfni.        |
| 8 til 10        | Þú hefur framúrskarandi leiðtogahæfni. |

Hægt er að setja upp bil stiga og texta fyrir hvern niðurstöðuflokk á spurningalista. Textar sem samsvara stigafjölda hvers svaranda eru birtir fyrir hvern niðurstöðuflokk. 

> [!NOTE]
> Gera má breytingar á bilum og textum. Ef spurningalistinn hefur hins vegar verið útfylltur geta breytingar valdið misræmi milli eldri og nýrri niðurstöðuskýrslna.

### <a name="conditional-question-hierarchies"></a>Skilyrðisbundin spurningastilgveldi

Skilyrðisbundin spurningastilgveldi eru valfrjáls þegar spurningarlisti er settur upp. 

> [!NOTE]
> Áður en hægt er að stofna skilyrðisbundið spurningastigveldi þarf þegar að vera búið að tengja spurningar sem svaraflokkum er úthlutað á við spurningalistann. 

Til að nota skilyrtar spurningar til að stofna spurningastigveldi í spurningalista verður að gera röðina sem spurningar eru settar fram í háða því hvaða svar var valið við fyrri spurningu. Með því að byggja spurningaröð á svaravali svaranda er hægt að breyta spurningalistann á meðan svarandinn lýkur honum.

#### <a name="examples"></a>Dæmi

Lögaðili býður bæði vörur og þjónustu fyrir viðskiptavini sína. Eins og á sér yfirleitt stað í slíkum tilfellum, kaupa sumir viðskiptavinir aðeins vörur, sumir kaupa aðeins þjónustu og sumir kaupa bæði vörur og þjónustu. Ef fyrirtækið vill dreifa ánægjukönnun er hægt að nota skilyrðisbundið skipulag fyrir spurningalistann til þess að koma í veg fyrir að viðskiptavinir sem einungis kaupa þjónustu þurfi að svara spurningum um vörur. 

Einnig er hægt að setja upp spurningalista þannig að ef svarandi velur svar A fyrir spurningu 1, er spurning 2 næst í spurningaröðinni. Einnig er hægt að setja upp spurningalista þannig að ef svarandi velur svar A við spurningu 1, er spurning 5 næst.

[!INCLUDE[footer-include](../includes/footer-banner.md)]