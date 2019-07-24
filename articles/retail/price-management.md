---
title: Stjórnun smásöluverðs
description: Þetta efnisatriði lýsir hugmyndum um stofnun og stjórnun á söluverðum í Microsoft Dynamics 365 for Retail.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: ShalabhjainMSFT
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 813547f522f5c69920eadf9df61e7f01b13ecd36
ms.sourcegitcommit: 7feb5d279adedd44f038195ce0f5e1c27d374049
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/10/2019
ms.locfileid: "1624790"
---
# <a name="retail-sales-price-management"></a>Retail-verðstjórnun

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir upplýsingar um ferlið við stofnun og stjórnun á söluverðum í Microsoft Dynamics 365 for Retail. Það leggur áherslu á hugmyndunum sem eru hluti af þessu ferli og áhrifin hinna ýmsu stillingamöguleika fyrir söluverð.

## <a name="terminology"></a>Orðalisti

Eftirfarandi hugtök eru notuð í þessu efnisatriði.

| Hugtak | Skilgreining, notkun og athugasemdir |
|---|---|
| Verð | Stök einingarupphæð sem vara selst fyrir á biðlara sölustaðar (POS) eða í sölupöntun. Í þessu efnisatriði vísar hugtakið *verð* alltaf til söluverðs, ekki birgðaverðs eða kostnaðarverðs. |
| Grunnverð | Verðið sem er sett í reitinn **Verð** á útgefinni vöru. |
| Verð viðskiptasamnings | Verðið sem sett er á vöru eða afbrigði með því að nota viðskiptasamning af gerðinni **Vara (sölur)**. |
| Besta verð | Þegar hægt er að beita fleiri en einu verði eða afslætti á vöru, minnstu verðupphæð og/eða mestu afsláttarupphæð sem býr til lægstu mögulegu nettóupphæð sem viðskiptavinurinn verður að greiða. Í þessu efnisatriði er hugmyndin á bak við besta verð alltaf vísað til sem „besta verðið“. Þetta besta verð er frábrugðið og ætti ekki að vera ruglað saman við upptalningargildið **Besta verð** fyrir samvinnslusnið. |

## <a name="price-groups"></a>Verðflokkar

Verðflokkar eru í kjarna verð- og afsláttarstjórnunar í Retail. Verðflokkar eru notaðir til að úthluta verðum og afsláttum til smásölueininga (það er rásum, vörulistum, fyrirtækjatengslum og vildarkerfum). Vegna þess að verðflokkar eru notaðir fyrir allar verðlagningar og afslætti er mjög mikilvægt að þú skipuleggir hvernig eigi að nota þá áður en þú byrjar.

Út af fyrir sig er verðflokkur bara heiti, lýsing og mögulega verðlagningarforgangur. Meginatriðið til að muna um verðflokkaK er að þeir eru notaðir til að stjórna margþættum samskiptum sem afslættir og verð eiga við smásölueiningar.

Eftirfarandi mynd sýnir hvernig verðflokkar eru notaðir. Taktu eftir, í þessari skýringarmynd, að „Verðflokkur“ er bókstaflega í miðju verðlagningar- og afsláttarstjórnunar. Smásölueiningarnar sem þú getur notað til að stjórna mismunarverði og afsláttum eru til vinstri og raunveruleg verð- og afsláttarfærslur eru til hægri.

![Verðflokkar](./media/PriceGroups.png "Verðflokkar")

Þegar verðflokkur er stofnaður ætti ekki að nota einn verðflokk fyrir margar gerðir smásölueininga. Annars getur verið erfitt að ákvarða hvers vegna tiltekið verð eða afsláttur er notaður á færslu.

Eins og rauða punktalínan á skýringarmyndinni sýnir, styður Retail kjarnavirkni Microsoft Dynamics 365 á verðflokki sem er settur beint á viðskiptavin. En í þessu tilviki færðu aðeins viðskiptasamninga söluverðs. Ef þú vilt nota verð sem eru sértæk viðskiptavini mælum við með að þú setjir ekki verðflokka beint á viðskiptavininn. Þess í stað ættir þú að nota fyrirtækjatengsl.

Eftirfarandi kaflar veita frekari upplýsingar um smásölueiningar sem hægt er að nota til að stilla sérstök verð þegar verðflokkarnir eru notaðir. Skilgreiningar á verðum og afsláttum fyrir allar þessar einingar er tveggja skrefa ferli. Hægt er að framkvæma þessi skref í hvorri röð sem er. Hins vegar er rökrétt röð að stilla verðflokkana á einingarnar fyrst vegna þess að þetta skref er líklega uppsetning sem er gerð aðeins einu sinni við innleiðingu. Þar sem verð og afslættir eru búnir til er því hægt að stilla hvern verðflokk fyrir sig fyrir verðin og afslættina.

### <a name="channels"></a>Rásir

Í smásölubransanum er dæmigert að hafa mismunandi verð á mismunandi rásum. Tveir helstu þættirnir sem hafa áhrif á verð sem eru sérstæk fyrir rásir eru kostnaður og staðbundnar markaðsaðstæður.

- **Kostnaður** - Því lengra í burtu sem rás er frá uppruna vöru, því meira kostar að setja vöru í birgðir. Til dæmis hafa ferskar afurðir takmarkaðan endingartíma og sérstakar kröfur til framleiðslu (til dæmis árstíðarbundin uppskera). Á veturna kostar ferskt salat líklega meira á norðurslóðum en á suðrænum slóðum. Ef þú stillir verð fyrir rásir yfir stórt landsvæði, viltu líklega setja mismunandi verð á mismunandi rásum.
- **Staðbundnar markaðsaðstæður** - Verslun sem hefur beinan keppinaut hinum megin götunnar verður mun viðkvæmari fyrir verðum en verslun sem hefur ekki beinan samkeppnisaðila í nágrenninu.

### <a name="affiliations"></a>Fyrirtækjatengsl

Almenn skilgreining á fyrirtækjatengslum er tengill eða tengsl við flokk. Í Retail eru fyrirtækjatengsl flokkar viðskiptavina. Fyrirtækjatengsl eru miklu sveigjanlegri tól fyrir verðlagningu og afsláttum viðskiptavina en kjarnahugmynd Microsoft Dynamics 365 um viðskiptavina- og afsláttarflokka. Í fyrsta lagi er hægt að nota tengsl fyrir bæði verð og afslætti, en verðlagning á því sem snýr ekki að smásölu er með annan flokk fyrir hverja gerð af afslætti og verði. Viðskiptavinur getur tilheyrt margvíslegum tengslum en getur aðeins tilheyrt einum flokki sem snýr ekki að smásölu af hverri gerð. Að lokum, þótt hægt sé að setja upp tengsl svo þau tengist viðskiptavini, þarf það ekki að vera svo. Hægt er að nota sértæk tengsl fyrir nafnlausa viðskiptavini á POS. Dæmigert dæmi um nafnlaus afsláttartengsl er afsláttur fyrir eldri borgara eða nemanda þar sem viðskiptavinur getur fengið afslátt bara með því að sýna meðlimakort.

Þrátt fyrir að tengsl séu oftast tengd við afslætti er einnig hægt að nota þau til að stilla mismunaverðlagningu. Til dæmis, þegar smásali selur til starfsmanns gæti hann viljað breyta söluverðinu í stað þess að nota afslátt ofan á venjulega verðið. Sem annað dæmi gæti smásali sem selur bæði neytendum og viðskiptamönnum boðið viðskiptamönnum betri verð, byggt á magninu sem þeir kaupa. Tengsl gera báðar þessar aðstæður mögulegar.

### <a name="loyalty-programs"></a>Vildarkerfi

Í tengslum við verð og afslætti eru vildarkerfi í grundvallaratriðum bara tengsl sem hafa sérstakt nafn. Bæði er hægt að stilla verð og afslætti fyrir vildarkerfi, eins og hægt er að gera fyrir tengsl. Hins vegar leiðin sem viðskiptavinir fá vildarverðlagningu á viðskiptum eða pöntunum er frábrugðið því hvernig þeir fá tengslaverðlagningu. Viðskiptavinir geta aðeins fengið vildarverðlagningu ef vildarkorti er bætt við viðskipti. Þegar vildarkorti er bætt við viðskipti er vildarkerfinu einnig bætt við. Vildarkerfið virkjar þá sérstök verð og afslætti.

Vildarkerfi geta verið marglaga og afslættir geta verið mismunandi á milli mismunandi laga. Þannig geta smásalar gefið tíðum viðskiptavinum meiri umbun án þess að þurfa að setja þessa viðskiptavini handvirkt inn í sérstakan flokk.

Vildarkerfi hafa viðbótarvirkni fyrir utan verð og afslætti. Hvað varðar verðlagningu og afslætti er hún hins vegar sú sama og fyrir tengsl.

### <a name="catalogs"></a>Vörulistar

Sumir smásalar nota efnislega eða sýndavörulista til að markaðssetja vörur og verðleggja fyrir ákveðna hópa viðskiptavina. Sem hluti af viðskiptamódeli þeirra til að tækla markaðssetningu með vörulista, geta smásalarnir sett mismunandi verð á mismunandi vörulista þeirra. Microsoft Dynamics 365 styður þennan möguleika með því að leyfa skilgreiningu á afsláttum og verðum sem eru sértæk fyrir vörulista, eins og hægt er að skilgreina afslætti sem eru sértækir fyrir rásir og tengsl. Þegar vörulista er breytt er hægt að tengja verðflokka við hann, líkt og hægt er að tengja hann við rás, tengsl eða vildarkerfi.

### <a name="best-practices-for-price-groups"></a>Bestu venjur fyrir verðflokka

Ekki nota verðflokk fyrir margar gerðir smásölueininga. Í staðinn skal nota eitt sett af verðflokkum fyrir rásir, mismunandi sett af verðflokkum fyrir tengsl eða vildarkerfi, og svo framvegis. Þú getur notað forskeyti eða viðskeyti í heiti verðflokksins til að sjónrænt flokka hinar ýmsu gerðir verðflokka sem þú notar.

Forðastu að setja verðflokka beint á viðskiptavin. Notaðu tengsl í staðinn. Þannig er hægt að úthluta öllum gerðum verðs og afslátta til viðskiptavina, ekki aðeins viðskiptasamningum söluverðs.

## <a name="pricing-priority"></a>Verðlagningarforgangur

Út af fyrir sig er verðlagningarforgangur bara tala og lýsing. Hægt er að nota verðlagningingarforgang á verðflokka eða hægt er að nota þá beint á afslætti. Þegar verðlagningarforgangur er notaður, leyfa þeir smásöluaðila að hnekkja meginreglunni um besta verðið með því að stjórna röðinni sem verð og afslættir eru notaðir á vörur. Stærra númer verðlagningarforgangs er metið á undan lægra númeri verðlagningarforgangs. Að auki, ef verð eða afsláttur finnst í hvaða forgangsnúmeri sem er, þá eru öll verð eða afslættir sem eru með lægra forgangsnúmeri hunsuð.

Verð og afsláttur getur komið frá tveimur mismunandi verðlagningarforgöngum vegna þess að þeir gilda um verð og afslætti óháð hvor öðrum.

Til að nota verðlagningarforgang fyrir verð þarf að úthluta honum á verðflokk og síðan búa til viðskiptasamning söluverðs fyrir þennan verðflokk.

Eiginleikinn verðlagningarforgangur var kynntur til að styðja við atburðarás þar sem smásali vill setja á hærri verð í tilteknu safni verslana. Til dæmis hefur smásali skilgreint svæðisbundin verð fyrir austurströnd Bandaríkjanna en vill hærra verð fyrir sumar vörur í verslunum í New York því það kostar meira að selja sumar vörur í borginni og/eða vegna þess að staðbundni markaðurinn er með hærri verð.

Eins og lýst var í kaflanum „Besta verð“ í þessu efnisatriði, velur verðlagningarvél smásölu venjulega lægra verðið milli tveggja verða. Þess vegna er vanalega komið í veg fyrir að smásalinn geti notað hærra verðið af tveimur verðum í verslun sem hefur bæði verðflokka austurstrandar og New York. Til að leysa þetta mál áður en eiginleiki verðlagningarforgangs var kynntur til sögunnar þurfti smásalinn að skilgreina verð fyrir hverja vöru tvisvar sinnum og ekki úthluta báðum verðflokkum. Að auki þurfti smásalinn að búa til fleiri verðflokka til að einangra vörurnar sem eru með hærra verð frá vörum sem eru með venjulegu, lægri verðin.

Hins vegar gerir eiginleiki verðlagningarforgangs smásalanum kleift að búa til verðlagningarforgang fyrir verð í verslunum sem er hærra en verðlagningarforgangur svæðibundinna verða. Að auki getur smásalinn búið til verðlagningarforgang eingöngu fyrir verð í verslunum og haft svæðisbundin verð á sjálfgefnum verðlagningarforgangi, sem er 0 (núll). Báðar uppsetningar hjálpa til við að tryggja að verð í verslunum verði alltaf notað á undan svæðisbundnum verðum.

### <a name="pricing-priority-example"></a>Dæmi um verðlagningarforgang

Við skulum skoða dæmi þar sem verð í verslun hnekkir öðrum verðum.

Innlendur smásali stillir flest verð á hvert svæði fyrir sig og það eru fjögur svæði: norðaustur, suðaustur, miðvestur og vestur. Hann hefur tekið eftir nokkrum mörkuðum með háu verðlagi sem þola hærra verð. Þessar markaðir eru í New York, Chicago og San Francisco.

Fyrir þetta dæmi munum við skoða nánar svæðið norðaustur. Verslun 1 er í Boston og verslun 2 er á Manhattan. Fyrir verslunina í Boston eru tveir verðflokkar tengdir rásinni: norðaustur og verslun 1. Í versluninni á Manhattan eru þrír verðflokkar tengdir rásinni: norðaustur, New York og verslun 2.

Smásalinn setur upp tvo verðlagningarforganga: hár kostnaður er með forgangsnúmer 5 og verð verslunar er með forgangsnúmer 10. (Mundu að sjálfgefinn verðlagningarforgangur er 0 \[núll\] og verð eða afsláttur sem hefur hærra forgangsnúmer er notað á undan verði eða afslætti sem hefur lægra forgangsnúmer.) Fyrir verðflokkinn norðaustur er verðlagningarforgangur settur á sjálfgefna gildið **0** (núll). Fyrir New York er verðlagningarforgangur stilltur á **5** vegna þess að New York er markaður með háu verðlagi. Fyrir verðflokka verslunar 1 og verslunar 2 er verðlagningarforgangur stilltur á **10**.

Tvær vörur sem smásalinn selur eru vara 1, stuttermabolur, og vara 2, tískugallabuxur.

| Afurð | Verð í norðaustri | Verð í New York | Verð verslunar |
|---|---|---|---|
| Stuttermabolur | $15 | Ekki valin | Ekki valin |
| Tískugallabuxur | $50 | $70 | Ekki valin |

Stuttermabolurinn selst fyrir sama verð (það er $15) hjá bæði verslunum Boston og Manhattan vegna þess að aðeins eitt verð er stillt í verðflokki norðausturs sem tengist báðum rásum. Tískugallabuxur seljast fyrir $50 í versluninni í Boston vegna þess að þetta verð er eina verðið sem er í boði í þeirri verslun. Hins vegar í versluninni á Manhattan eru tvö verð í boði: $50 og $70. Vegna þess að verðlagningarforgangurinn 5 fyrir verðflokk New York er hærri en verðlagningarforgangur upp á 0 (núll) fyrir norðaustur verðflokkinn, verður verðið hækkað upp í $70 í sölustaðarkerfinu.

> [!NOTE]
> Fyrir hvern verðlagningarforgang er krafist að farið sé að fullu í gegnum rökfræði verðlagningarvélar smásölu. Til að viðhalda afköstum verð- og afsláttarútreikninga ætti þess vegna að nota verðlagningarforgang sparlega.

## <a name="types-of-prices"></a>Tegundir verða

Í Microsoft Dynamics 365 er hægt að stilla vöruverð á þremur stöðum:

- Beint á vöruna (grunnverð)
- Í viðskiptasamningi söluverðs
- Í verðleiðréttingu

Grunnverð og verð viðskiptasamnings eru hluti af kjarna Microsoft Dynamics 365 og eru fáanleg jafnvel þótt Retail sé ekki notað. Virkni verðleiðréttingar er aðeins í boði í Retail. Næsti kafli veitir frekari upplýsingar um hvern þessara valkosta til að stilla verð og útskýrir hvernig valkostirnir virka saman.

## <a name="setting-prices"></a>Verðstillingar

### <a name="base-price"></a>Grunnverð

Auðveldasta staðurinn til að stilla verð fyrir vöru er beint á vöruna. Gildið sem þú setur beint á vöru er oft nefnt grunnverð vörunnar. Grunnverðið er stillt í reitnum **Verð** í flipanum **Selja** á síðunni **Upplýsingar um losaðar afurðir**. Gildið sem slegið er inn er í gjaldmiðli fyrirtækisins. Sjálfgefið verð er fyrir magn upp á 1 af mælieiningunni sem er stillt í reitnum **Eining** í flipanum **Sala**. Raunverulegt verð á hverja vörueiningu er byggt á mælieiningunni, verð á magni og gjaldmiðlinum.

Ef vara hefur eitt verð fyrir alla, býður grunnverðið upp á skilvirkustu leiðina til að stjórna verð vörunnar. Jafnvel þótt notaðir séu viðskiptasamningar til að setja verð, gætir þú einnig sett grunnverð á vöru. Ef þú notar síðan ekki **Allt** viðskiptasamning, þá ertu með varaverð sem er notað þegar engin viðskiptasamningur gildir.

Ef gjaldmiðill smásölurásar er frábrugðinn gjaldmiðli fyrirtækis, er grunnverðið í þeirri smásölurás ákvarðað með því að nota umreikning gjaldmiðils á verðið sem er sett á vöruna.

Þótt verðeiningin sé ekki algeng uppákoma smásölu er hún studd af verðlagningarvél smásölunnar. Ef verðeiningin er stillt á annað gildi en **0** (núll) er verð á hverja einingu jafnt og Verð ÷ Verðeining. Til dæmis ef verð vöru er $10,00 og verðeiningin er 50, er verð fyrir einn í magni $0,20 (= $10,00 ÷ 50).

### <a name="sales-price-trade-agreement"></a>Viðskiptasamningur söluverðs

Með því að nota færslubók viðskiptasamnings er hægt að búa til viðskiptasamninga söluverðs fyrir hverja vöru. Í Microsoft Dynamics 365 eru þrjú svið viðskiptavina fyrir viðskiptasamninga söluverðs: **Tafla**, **Flokkur** og **Allt**. Viðskiptavinasviðið ákvarðar viðskiptavinina sem tiltekinn viðskiptasamningur söluverðs á við um.

**Tafla** viðskiptasamnings söluverðs er fyrir einn viðskiptavin sem er settur beint á viðskiptasamninginn. Þessi atburðarás er ekki dæmigerð smásöluviðskipti til neytanda. Hins vegar, ef það gerist, notar verðlagningarvél smásölunnar viðskiptasamninginn **Tafla** þegar hún ákveður verð.

**Flokkur** viðskiptasamnings söluverðs er sú gerð sem oftast er notuð við smásöluvirkni. Utan Retail, **Flokkur** viðskiptasamnings söluverðs er fyrir einfaldan viðskiptavinaflokk. Hins vegar, í Retail, hefur hugtakið viðskiptavinaflokkur verið víkkað út þannig að það er orðið að almennari smásöluverðsflokki. Hægt er að tengja verðflokk við smásölurás, tengsl, vildarkerfi eða vörulista. Nánari upplýsingar um verðflokka er að finna í kaflanum „Verðflokkar“ fyrr í þessu efnisatriði.

> [!NOTE]
> Verð viðskiptasamnings er alltaf notað á undan grunnverðinu.

### <a name="price-adjustment"></a>Verðleiðrétting

Eins og nafnið gefur til kynna er verðleiðrétting notuð til að breyta verði sem var annaðhvort sett beint á vöruna eða sett með því að nota viðskiptasamning. Verðleiðréttingu er aðeins hægt að nota til að lækka verðið, ekki hækka það. Verðleiðrétting er ráðlagða leiðin fyrir smásala til að búa til, fylgjast með og stjórna verðlækkunum á vörum með tímanum.

Það eru til þrjár gerðir af verðleiðréttingum: hlutfall af, upphæð af og verð. Verðleiðrétting af gerðinni hlutfall af eða upphæð af er alltaf notuð við sölufærslu. Hins vegar er verðleiðrétting af gerðinni verð aðeins notað ef leiðrétt verð er lægra en það verð sem sett var með því að nota grunnverðið eða verð viðskiptasamnings. Þess vegna, ef verðið sem er sett í verðleiðréttingu er meira en óleiðrétt verð, er verðleiðréttingin ekki notuð.

## <a name="determining-price-for-a-product-in-a-transaction"></a>Ákvörðun á verði fyrir vöru í viðskiptum

Útreikningur á verði og afslætti á viðskiptum notar meginregluna um að finna besta verðið fyrir viðskiptavininn. Samkvæmt þessari meginreglu er lægsta verðið notað ef meira en eitt verð finnst. Að auki er samsetning afslátta sem býr til mestu afsláttarupphæðina fyrir viðskiptin í heild sinni notaður. Í sumum tilfellum þarf að nota minni afslátt á einni vöru til að hægt sé að bæta við viðbótarafslætti á aðrar vörur í viðskiptunum.

Eina undantekningin frá meginreglunni um að finna besta verðið fyrir viðskiptavininn er valkostur um að blanda saman ódýrustu afsláttunum. Þessi valkostur virkjar ódýrustu afslættina sem er hagstætt smásalanum þegar vörur eru valdar og flokkaðar. Þannig að þegar viðskiptin innihalda fleiri vörur en þarf til að uppfylla kröfur um ódýrasta afsláttinn, velur verðlagningarvél smásölunnar vörurnar sem búa til minnstu mögulegu afsláttarupphæðina fyrir viðskiptavininn.

Verðlagningarvél smásölunnar skilar þremur verðum fyrir hverja vöru: grunnverði, verði viðskiptasamnings og virku verði.

Grunnverðið er aðeins eiginleiki á vörunni og er það sama fyrir alla alls staðar.

Í viðskiptasamningi söluverðs, ef valkosturinn **Finna næsta** er stilltur á **Já**, er lægsta verðið sem finnst fyrir viðeigandi viðskiptasamning söluverðs notað sem verð viðskiptasamningsins. Hægt er að finna viðskiptasamninga með því að nota verðflokka eða **ALLT** lykilkóðann. Að öðrum kosti er hægt að úthluta viðskiptasamningum beint til viðskiptavinar. Ef valkosturinn **Finna næsta** er stilltur á **Nei** er fyrsta verð viðskiptasamnings sem finnst notað. Ef engir viðskiptasamningar söluverðs finnast er verð viðskiptasamnings sett sem jafnt og grunnverðið.

Virka verðið er reiknað með því að taka verð viðskiptasamnings og beita stærstu verðleiðréttingunni sem gildir um vöruna. Ef engar verðleiðréttingar finnast eða ef reiknað virkt verð er meira en verð viðskiptasamningsins er virka verðið sett sem jafnt og verð viðskiptasamnings. Mundu að þú getur ekki hækkað verð á vöru með því að nota verðleiðréttingu. Viðeigandi verðleiðréttingar eru aðeins að finna með því að nota verðflokka sem eru úthlutaðir á rás, vörulista, tengsl eða vildarkerfi.

## <a name="category-price-rules"></a>Verðreglur tegundar

Eiginleikinn verðreglur tegundar í Retail gefur þér auðvelda leið til að búa til nýja viðskiptasamninga fyrir allar vörur í tegund. Þessi eiginleiki leyfir þér einnig sjálfkrafa að finna fyrirliggjandi viðskiptasamninga fyrir vörurnar í tegundinni og fella þá úr gildi.

Þegar þú velur möguleikann á að fella úr gildi fyrirliggjandi viðskiptasamninga, stofnar kerfið nýja færslubók viðskiptasamnings fyrir vörurnar í tegundinni sem eru með virkan viðskiptasamning. Hins vegar verður færslubókin að vera bókuð handvirkt. Auk þess geta verðreglur tegundar fundið fyrirliggjandi viðskiptasamninga aðeins ef notuð er sama verðreglan (það er ef þú býrð til nýja verðreglu sem notar sömu tegundina sem var áður). Ef þú notar ekki sömu verðregluna munu núverandi viðskiptasamningar ekki falla úr gildi.

Verðin má hækka eða lækka með því að nota reitina **Verðreglur** og **Verðgrunnur** í verðreglum tegundar.

- Í reitnum **Verðreglu** skal velja gerð verðbreytingar sem á að nota:

    - **Álagning** - Hlutfall af verðgrunni er notað til að reikna út söluverð. Til dæmis vara sem kostar 10,00 og selst á 15,00 er með 50 prósent álagningu.
    - **Framlegð** - Hlutfall af söluverði sem er notað til að reikna út upphæð hagnaðar. Til dæmis vara sem kostar 10,00 og selst á 15,00 er með 33,3 prósent framlegð.
    - **Föst upphæð** - Upphæð sem er bætt við verðgrunn er notuð til að reikna út söluverð. Til dæmis vara sem kostar 10,00 og selst á 15,00 hefur fasta upphæð 5,00.

- Í reitnum **Verðgrunnur** skal velja gerð verðs sem á að breyta:

    - **Grunnkostnaður** - Upphæðin sem smásalinn greiddi til birgja.
    - **Grunnverð** - Söluverð áður en viðskiptasamningar og verðleiðréttingar eru teknar með.
    - **Núverandi verð** - Söluverð eftir að viðskiptasamningar og verðbreytingar eru teknar með.

Til að geta auðveldlega uppfært verð á ýmsum vörum frá mismunandi vörutegundum er hægt að notað viðbótarvörutegundirnar ásamt verðreglum tegundar.

## <a name="best-practices"></a>Bestu venjur

Microsoft SQL Server Express er oft notaður fyrir gagnagrunnarásir vegna kostnaðar (ókeypis). Hafðu í huga að SQL Server Express hefur takmarkanir á vélbúnaði og takmarkaða á gagnastærð. Ef þú skipuleggur ekki rétt, getur þú fljótt náð upp í takmarkanir gagnastærðar SQL Server Express. Þessi umfjöllun gildir ekki aðeins um verðlagningu heldur líka á öðrum sviðum vörunnar. Hér eru nokkrar bestu venjur sem geta hjálpað þér að draga úr stærð gagna:

- Ef þú notar viðskiptasamninga og verð breytast, ættir þú að fella gamla viðskiptasamninga úr gildi með því að setja á lokadagsetningu. Með tímanum hjálpar þessi nálgun að draga úr fjölda viðskiptasamninga sem eru geymdir í gagnagrunnarásum. Það hjálpar einnig að draga úr gagnamagninu sem reiknirit verðútreikninga verður að vinna með.
- Ef verð eru breytileg eftir vöruafbrigði skaltu íhuga að nota grunnverð vörunnar sem verð á algengasta afbrigðinu. Notaðu síðan viðskiptasamninga aðeins fyrir verðafbrigði sem eru undantekningar. Þessi nálgun hjálpar til við að draga úr fjölda færslna viðskiptasamninga. Vegna þess að það er hæglega hægt að flytja inn gögn í Microsoft Dynamics 365 gætirðu freistast til að flytja inn viðskiptasamning fyrir hvert afbrigði af hverri vöru. Hins vegar getur þessi nálgun búið til marga viðskiptasamninga sem hafa sama gildið. Þess vegna getur það aukið stærð gagna að óþörfu.
- Smásöluferli raða breytilegum sértækum verðum í röð frá mest sértækt til minnst sértækt. Ef vöruvídd hefur ekki áhrif á verðið þarftu ekki að skilgreina viðskiptasamninga fyrir það. Til dæmis er vara í boði í þremur litum og fjórum stærðum en verðið breytist aðeins eftir stærðinni. Ef þú skilgreinir viðskiptasamning fyrir hvert afbrigði býrðu til 12 færslur. Þess í stað getur þú skilgreint viðskiptasamning bara fyrir hverja stærð og skilið litavíddina eftir auða. Í þessu tilfelli framleiðir þú aðeins fjórar færslur.

    Að öðrum kosti, ef ekki öll gildi víddar búa til mismunandi verð, getur þú skilgreint einn viðskiptasamning fyrir vörusniðmát og skilið allar vöruvíddir eftir auðar. Síðan skilgreina aðskilinn viðskiptasamning bara fyrir hvert víddargildi sem býr til mismunandi verð. Til dæmis ef XXL-stærðin hefur hærra verð, en allar aðrar stærðir eru með sama verð þarf aðeins tvo viðskiptasamninga: einn fyrir vörusniðmát og einn fyrir XXL-stærðina.

## <a name="prices-that-include-tax-vs-prices-that-exclude-tax"></a>Verð með sköttum á móti verðum án skatta

Þegar þú setur söluverð í Microsoft Dynamics 365, tilgreinir þú ekki hvort verðgildið sem þú setur inn sé með eða án skatta. Gildið er aðeins verðið. Hins vegar gerir stillingin **Verð með söluskatti** á smásölurásunum þér kleift að skilgreina smásölurásir þannig að verðin eru annaðhvort með eða án skatta. Þessi stilling er sett í rásinni og getur breyst, jafnvel í einu fyrirtæki.

Ef þú vinnur með bæði innifaldar og undanskildar gerðir af sköttum er mjög mikilvægt að setja rétt verð vegna þess að heildarupphæðin sem viðskiptavinurinn greiðir mun breytast ef stillingin **Verð með söluskatti** á rásinni er breytt.

## <a name="differences-between-retail-pricing-and-non-retail-pricing"></a>Mismunur á smásöluverði og verði sem snýr ekki að smásölu

Ein verðlagningarvél er notuð til að reikna smásöluverð yfir allar rásir: símaver, smásöluverslun og vefverslanir. Þetta hjálpar til við að virkja atburðarásir sameinaðra viðskipta.

Retail verðlagning er hönnuð til að vinna með smásölueiningar í stað eininga sem snúa ekki að smásölu. Nánar tiltekið er hún hönnuð til að setja verð eftir verslun, ekki eftir vöruhúsi.

Verðlagningarvél smásölunnar styður ekki eftirfarandi verðlagningareiginleika:

- Setja verð með því að nota geymsluvíddir svæðis og vöruhúss
- Eigindatengd verðlagning
- Farið í gegnum afslátt lánardrottins

Að auki **aðeins** verðlagningarvél smásölu styður eftirfarandi verðlagningareiginleika:

- Verð er byggt á vöruvíddum, raðað frá mest sértæka verðafbrigðinu til minnst sértæka verðafbrigðisins á verði vörusniðmáts. Verð sem er stillt með því að nota tvær vöruvíddir (t.d. lit og stærð) er notað á undan verð isem er stillt með því að nota aðeins eina vöruvídd (t.d. stærð).
- Hægt er að nota sama verðflokk til að stjórna verðlagningu og afsláttum.

## <a name="pricing-api-enhancements"></a>Verðlagning á API-endurbótum

Verð er einn mikilvægasti þátturinn sem stýrir ákvörðun á innkaupum að gera fyrir marga viðskiptavini, og margir viðskiptavinir bera saman verð á ýmsum síðum áður en þeir kaupa nokkuð. Til að tryggja að söluaðilar bjóði upp á samkeppnishæf verð verða þeir að fylgjast grannt með samkeppnisaðilum og auglýsa oft sig. Til að auðvelda þessum söluaðilum að laða að viðskiptavini, er mjög mikilvægt að afurðaleit, vafraeiginleikinn, listar og upplýsingasíða afurðar sýni nákvæmustu verðin.

Í væntanlegri útgáfu Retail, mun forritunarviðmótið (API) **GetActivePrices** skila verðum sem innihalda einfalda afslætti (t.d. staka línuafslætti sem eru ekki háðir öðrum vörum í körfunni). Á þennan hátt eru verðin sem eru sýnd nálægt raunverulegri upphæð sem viðskiptavinur greiðir fyrir vörurnar. Þetta API mun innihalda allar gerðir af einföldum afsláttum sem miðast við: afslætti tengsla, hollustu, vörulista og rásar. Að auki skilar API upplýsingum um heiti og gjaldgengi notaðra afslátta svo söluaðilar geti boði upp á ítarlegri lýsingar á verðinu og skapað óþreyju ef gjaldgengur afsláttur rennur brátt út.
