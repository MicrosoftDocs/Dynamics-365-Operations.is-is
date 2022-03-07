---
title: Hönnunarútgáfur og flokkar hönnunarafurðar
description: Þetta efnisatriði veitir upplýsingar um hugmyndina á bak við hönnunarútgáfur. Hönnunarútgáfur tryggja að mismunandi stöður afurðar og gögn hennar sé haldið uppfærðum og skýrum og að hægt sé að sjá þau í kerfinu.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgLookupDynastring, EngChgProductVersionNumberRule, EngChgEcmProductRoute, EngChgEcmRequestProducts, EngChgEcmProductRoute, EngChgEcmProductPreview,EngChgEcmProductBOMItemIdLookup, EngChgEcmProductBOMConsistOf, EngChgEcmProductCreate, EngChgEcmProductLookup, EngChgProductVersionPrCompany, ngChgProductTypeLookup, EngChgProductType, EngChgProductItemPart, EngChgProductItem, EngChgEcmCategory, EngChgEcmBomDesignerEditBom, EngChgEcmBomDesigner, EngChgEcmBOMCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 42faa9e5f073d718c18422e37212c2ae8a28b28d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572890"
---
# <a name="engineering-versions-and-engineering-product-categories"></a>Hönnunarútgáfur og flokkar hönnunarafurðar

[!include [banner](../includes/banner.md)]

Hönnunarafurðir þróast meðan á líftíma afurðanna stendur af mörgum ástæðum. Til dæmis gætu breytingar verið kynntar til sögunnar til að bæta þjónustustig afurðar, íhluta breytt vegna þess birginn býður ekki lengur upp á hann, sem svar við nýjum uppgötvunum eða til að laga mistök í upprunalegri hönnun. Einnig eru margar ástæður fyrir því hvers vegna eigi að geyma þessar breytingar sem hluti af núgildandi afurð, þannig að ekki verði skrifað yfir eldri gögn. Hér eru nokkrir af þeim ástæðum:

- Þú vilt fylgjast með afurðinni þar sem hún var framleidd og afhent viðskiptavinum þínum í fyrri líftímastöðum.
- Þú þarft afhendingartíma áður en þú samþykkir og setur breytingarnar á.
- Þú vilt fá tímastimpil á hverja breytingu og þú vilt geta afhent áður framleiddar afurðir aðskildar frá hinum.

*Hönnunarútgáfur* tryggja að ýmsar stöður afurðar og gögn hennar sé haldið uppfærðum og skýrum og að hægt sé að sjá þau í kerfinu. Þetta hugtak hjálpar til við að viðhalda samræmi, læsa uppskriftum fyrir afurð, koma í veg fyrir breytileika og bera kennsl á breytingar á auðveldan hátt.

Yfirleitt er reglan *Form-hæfi-virkni* notuð til að ákveða hvort breyting þurfi nýja afurð, nýja útgáfu eða uppfærslu á fyrirliggjandi útgáfu. Hvert þessa þriggja hugtaka í heiti þessarar reglu vísar til tiltekins hlutar, sem auðveldar hönnuðum að láta hluti passa við þarfir. Þessi form-hæfi-virkni regla eykur sveigjanleika hönnunarbreytinga vegna þess að aðeins þarf lágmarks skráningarvinnu og kostnað til að breyta hluta, svo lengi sem hæfi, form og virkni afurðar er viðhaldið.

- **Hæfi** vísar í getu hlutarins eða eiginleikans til að tengjast eða sameinast öðrum eiginleika eða hluta samsetningarinnar. Hæfið gerir hlutanum kleift að uppfylla nauðsynleg þolmörk samsetningarinnar þannig að hún verði nothæf.
- **Form** vísar í einkenni hlutar eða samsetningar, t.d. ytri lengdir, þyngd, stærð og sýnilega þætti. Form er sá þáttur sem verður fyrir mestum áhrifum af fagurfræðilegum ákvörðunum hönnuðar. Það felur í sér umgjörð, grind eða stjórnborð sem verður ytri „ásjóna“ afurðar.
- **Virkni** er skilyrði sem er uppfyllt þegar hluturinn framkvæmir á skilvirkan og áreiðanlegan hátt tilgang hans. Til dæmis getur virknin í raftæki verið háð efnislegum íhlutum sem eru notaðir og hugbúnaði eða fastbúnaði. Oft getur hún einnig farið eftir eiginleikum valdrar umgjarðar. Tvær algengustu ástæður þess að umgjörð uppfylli ekki skilyrði virkninnar, eru illa staðsett eða léleg stærð á tengjum og villandi merkingar eða þær vantar. 

## <a name="engineering-versions"></a>Hönnunarútgáfur

Þegar hönnunarafurðir eru notaðar hefur hver afurð a.m.k. eina hönnunarútgáfu. Upprunalega hönnunarútgáfan er sjálfkrafa stofnuð þegar stofnuð er hönnunarafurð. Sérhver hönnunarútgáfa geymir gögnin sem tengjast hönnuninni sem á sérstaklega við þessa útgáfu. Hér eru nokkur dæmi um þessi gögn:

- Útgáfunúmerið og fyrra útgáfunúmer (ef við á)
- Gildisdagsetningarnar frá og til
- Virk staða hönnunarútgáfu, sem gefur til kynna hvort hægt sé að gefa út útgáfuna og nota hana í færslum (Frekari upplýsingar er að finna í [Undirbúningur afurðar](product-readiness.md).)
- Hönnunarfyrirtækið sem stofnaði og á afurðina (Frekari upplýsingar er að finna í [Hönnunarfyrirtæki og reglur um eignarétt gagna](engineering-org-data-ownership-rules.md).)
- Tengd hönnunarskjöl, t.d. samsetningarleiðbeiningar, notkunarleiðbeiningar, myndir og tenglar
- Hönnunareigindir (Frekari upplýsingar er að finna í [Hönnunareigindir og leit að hönnunareigind](engineering-attributes-and-search.md).)
- Uppskrift fyrir hönnunarafurðir
- Formúlur fyrir meðhöndlun á framleiðsluvörum
- Leiðir hönnunar

Hægt er að uppfæra þessi gögn í fyrirliggjandi útgáfu eða stofna nýja útgáfu með því að nota *pöntun hönnunarbreytingar*. (Frekari upplýsingar er að finna í [Stjórna breytingum á hönnunarafurðum](engineering-change-management.md).) Ef ný útgáfa afurðar er stofnuð, afritar kerfið öll gögn sem tengjast hönnuninni yfir í þessa nýju útgáfu. Síðan er hægt að breyta gögnunum fyrir þessa nýju útgáfu. Á þennan hátt er hægt að fylgjast með tilteknum gögnum fyrir hverja útgáfu fyrir sig. Til að bera saman muninn á samfelldum útgáfum hönnunar, skal skoða pöntun hönnunarbreytingar sem inniheldur gerð breytinga sem gefa til kynna allar breytingar.

Eins og hefur komið fram, upprunalega hönnunarútgáfan er sjálfkrafa stofnuð þegar stofnuð er hönnunarafurð. Útgáfunúmer þessarar útgáfu fylgir númerareglu útgáfu sem skilgreind er í hönnunartegund afurðarinnar. Til að skipta yfir í eftirfylgjandi útgáfu verður að bæta afurðinni við pöntun hönnunarbreytingar sem línu og stilla verður reitinn **Áhrif** á *Ný útgáfa*. Pöntun hönnunarbreytingar inniheldur upplýsingar breytingarinnar úr núverandi útgáfu í næstu útgáfu.

Athugið að hönnunarafurð getur aðeins verið í einni pöntun hönnunarbreytingar í einu. Þessi takmörkun tryggir nákvæmni gagna og hjálpar til við að koma í veg fyrir skörun eða mótsagnakenndar breytingar í afurðinni. Athugið einnig að reiturinn **Hönnun** í yfirlitinu **Haus** fyrir pöntun hönnunarbreytingar sýnir hönnuðinn sem ber ábyrgð á breytingapöntuninni. Ef hönnuðurinn tilheyrir teymi sem er skilgreint í kerfinu mun reiturinn **Ábyrgð** sýna stjórnanda þess teymis.

## <a name="track-versions-in-transactions"></a>Rekja útgáfu í færslum

Þegar notuð er hönnunarbreytingastjórnun eru aðalgögn afurðar alltaf með eina eða fleiri hönnunarútgáfur. Í uppsetningu á hönnunarafurðum er hægt að velja hvort hönnunarútgáfan er einnig hluti af *flutningsfærslum*. (Frekari upplýsingar er að finna í hlutanum [Setja upp flokka hönnunarafurðar](#product-category) seinna í þessu efnisatriði.) Ef flutningsáhrifin eiga við, eru þau mismunandi fyrir hverja afurð og fyrirtæki. Stundum er aðeins notuð nýjasta útgáfa afurðarinnar. Þar af leiðandi er ekki lengur hægt að nota eldri útgáfu þegar ný útgáfa er gefin út. Í öðrum tilvikum er fyrri útgáfa áskilin í flutningsfærslum til að yfirstíga eftirfarandi áskoranir:

- Vörustjórnunardeildin verður að senda tvö stykki af afurð til viðskiptavinar. Í þessu tilviki þarf að ákveða hvort þú viljir eða vilt leyfa að senda tvær ólíkar útgáfur.
- Seinna er tekið eftir því að vandamál kemur upp og að það tengist tiltekinni breytingu. Í þessu tilviki gæti verið gagnlegt að ákveða nákvæmlega hvaða útgáfa var send í hverri pöntun.
- Fyrirtæki vilja yfirleitt senda gamlar útgáfur fyrst, til að klára birgðir þeirra. Sérstaklega fyrir vörur sem lítið fer af, er oft hægt að stjórna þessar nálgun með því að ákveða gildisdagsetningar á nýju útgáfunni í tengslum við spár um það hvenær birgðir eldri útgáfunnar muni klárast. Stundum gæti hinsvegar ekki verið hægt að gera þennan samanburð, eða þér gæti fundist óvissuþáttur fyrir spá um birgðastöðu vera of hár.

Ákvörðunin um hvort gera eigi útgáfur sýnilegar í birgðum veltur á þáttum á borð við þá sem áður voru nefndir, auk venjum fyrirtækisins og annarra þátta sem eiga sérstaklega við fyrir hvert fyrirtæki fyrir sig. Hægt er að tilgreina hegðunina fyrir *flokk hönnunarafurðar*. Hún gildir þá um allar afurðir sem búnar eru til úr þeim flokki, fyrir öll fyrirtæki sem afurðin er gefin út í.

Fyrir afurðir sem eru settar upp þannig að þær hafi áhrif á vörustjórnun, þarf að tilgreina hönnunarútgáfuna fyrir hverja færslu. Þótt kerfið stingi upp á *síðustu virku útgáfu* geturðu valið á milli allra virku útgáfanna sem eru í boði fyrir fyrirtækið. Fyrir afurðir sem eru settar upp þannig að þær hafi ekki áhrif á vörustjórnun, er hönnunarútgáfan ekki tilgreind fyrir færslur. Hins vegar notar kerfið nýjustu virku útgáfuna. Til dæmis þegar afurð er bætt við framleiðsluuppskrift verður nýjasta útgáfan notuð og þegar aðaláætlanagerð er keyrð verður gert ráð fyrir nýjustu útgáfunni.

## <a name="set-up-engineering-product-categories"></a><a name="product-category"></a>Setja upp flokka hönnunarafurða

Flokkur hönnunarafurðar býður upp á grunn til að stofna tiltekna hönnunarafurð. Hver flokkur setur upp safn af sjálfgefnum gildum og stefnum. Þess vegna, þegar stofnuð er hönnunarafurð, er flokkurinn fyrst valinn til að stofna hana úr.

Athugið að ný gerð tegundastigveldis (*afurðastigveldi hönnunar*) er sjálfkrafa uppsett fyrir þig. Hægt er að stofna flokkana handvirkt með því að fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Upplýsingar um flokk hönnunarafurðar**.

Hver flokkur hönnunarafurðar ákveður sjálfgefna hegðun hönnunarafurðanna sem eru stofnaðar út frá þeim flokki. Þegar búið er að stofna hönnunarafurð, er ekki hægt að breyta flokki hennar. Ef þú hinsvegar velur rangan flokk, geturðu eytt afurðinni og stofnað hana aftur.

Þegar flokkur hönnunarafurðar er stofnaður, geturðu ekki breytt eftirfarandi stillingum:

- Hönnunarfyrirtæki
- Gerð afurðar
- Undirgerð afurðar
- Afurðavíddaflokkur
- Afbrigðistækni
- Númeraregla útgáfu

Aðrar stillingar gætu fengið sjálfgefin gildi sem eru sett upp fyrir flokk hönnunarafurðar. Samkvæmt reglum kerfisins geta þessi gildi hinsvegar breyst.

Til að vinna með flokka hönnunarafurðar skal fara í **Umsjón hönnunarbreytinga \> Uppsetning \> Upplýsingar um flokk hönnunarafurðar**. Fylgið svo einu af eftirfarandi skrefum.

- Til að stofna nýjan flokk skal velja **Nýr** á aðgerðasvæðinu og síðan stilla reitina eins og lýst er í eftirfarandi undirköflum.
- Til að breyta fyrirliggjandi flokki skal velja hann úr listasvæðinu, velja **Breyta** á aðgerðasvæðinu og síðan stilla reitina eins og lýst er í eftirfarandi undirköflum.
- Til að eyða fyrirliggjandi flokki skal velja hann úr listasvæðinu og síðan velja **Eyða** á aðgerðasvæðinu.

### <a name="header"></a>Haus

Stillið eftirfarandi reiti í hausnum fyrir flokk hönnunarafurðar.

| Svæði | lýsing |
|---|---|
| Nafn | Færið inn heiti fyrir flokk hönnunarafurðar. |
| Hönnunarfyrirtæki | Veljið hönnunarfyrirtækið þar sem hægt er að stofna afurðir í þessum flokki hönnunarafurðar og þar sem unnið verður með þær. |

### <a name="details-fasttab"></a>Upplýsingar flýtiflipa

Stillið eftirfarandi reiti í flýtiflipanum **Upplýsingar** í flokki hönnunarafurðar.

| Svæði | lýsing |
|---|---|
| Gerð afurðar | Veljið hvort flokkurinn eigi við um afurðir eða þjónustu. |
| Gerð framleiðslu | Þetta svæði birtist aðeins þegar þú hefur virkjað [breytingastjórnun formúlu](manage-formula-changes.md) í kerfinu. Veldu þá gerð framleiðslu sem þessi hönnunarafurðategund á við um:<ul><li>**Áætlunarvara** – Notaðu þennan hönnunarflokk til að gera breytingastjórnun formúlu fyrir skipulagsatriði. Áætlunarvörur nota formúlur. Þau líkjast formúluatriðum en eru eingöngu notuð til að framleiða aukaafurðir og hliðarafurðir, ekki lokaafurðir. Formúlur eru notaðar við framleiðsluferlið.</li><li>**Uppskrift** – Notaðu þennan hönnunarflokk til að hafa umsjón með hönnunarafurðum sem nota ekki formúlur og innihalda yfirleitt (en ekki endilega) uppskriftir.</li><li>**Formúla** – Notaðu þennan hönnunarflokk til að gera breytingastjórnun formúlu fyrir tilbúnar afurðir. Þessir hlutir verða með formúlu en ekki uppskrift. Formúlur eru notaðar við framleiðsluferlið.</li></ul> |
| Þyngd afurðar | Þessi valkostur birtist aðeins þegar þú hefur virkjað [breytingastjórnun formúlu](manage-formula-changes.md) í kerfinu. Hann er aðeins tiltækur þegar reiturinn **Framleiðslugerð** er stilltur á *Áætlunarvöru* eða *Formúlu*. Stilltu þennan valkost á *Já* ef þú ætlar að nota þennan hönnunarflokk til að hafa umsjón með vörum sem þurfa stuðning framleiðsluþyngdar. |
| Rekja útgáfu í færslum | Veljið hvort stimpla eigi útgáfu afurðarinnar í öllum færslum (áhrif á vörustjórnun). Ef þú til dæmis rekur útgáfuna í færslum mun hver sölupöntun sýna hvaða tiltekna útgáfa afurðarinnar var seld í þeirri sölupöntun. Ef útgáfan er ekki rakin í færslum mun sölupöntun ekki sýna hvaða tiltekna útgáfa var seld. Þess í stað sýna þær alltaf nýjustu útgáfuna.<ul><li>Ef þessi valkostur er stilltur á *Já* verður afurðarsniðmát stofnað fyrir afurðina og sérhver útgáfa afurðarinnar verður afbrigði sem notar afurðarvíddina *útgáfa*. Reiturinn **Undirgerð afurðar** er sjálfkrafa stilltur á *Afurðarsniðmát* og í reitnum **Afurðavíddaflokkur** þarf að velja afurðavíddaflokk þar sem vídd *útgáfunnar* er virk. Aðeins afurðavíddaflokkar þar sem *útgáfa* er virk vídd verða sýndir. Hægt er að stofna nýja afurðarvíddaflokka með því að velja hnappinn **Breyta** (blýantstákn).</li><li>Ef þessi valkostur er stilltur á *Nei* verður afurðarvíddin *útgáfa* ekki notuð. Þú getur síðan valið hvort þú vilt búa til afurð eða afurðarsniðmát sem notar aðrar víddir.</li></ul><p>Þessi valkostur er oft notaður fyrir afurðir sem hafa kostnaðarmismun á milli útgáfna, eða afurðir þar sem mismunandi skilyrði eiga við í samanburði við viðskiptavininn. Þess vegna er mikilvægt að gefa til kynna hvaða útgáfa var notuð í hverri færslu.</p> |
| Undirgerð afurðar | Veljið hvort flokkurinn geymi afurðir eða afurðarsniðmát. Fyrir afurðarsniðmát verða afurðarvíddir notaðar.
| Afurðavíddaflokkur | Stillingin **Rekja útgáfur í færslum** auðveldar þér að velja afurðarvíddaflokk. Ef þú gafst upp að þú vildir rekja útgáfu í færslum, verða afurðavíddaflokkar þar sem víddin *útgáfa* er notuð sýndir. Annars verða aðeins sýndir afurðavíddaflokkar þar sem víddin *útgáfa* er ekki notuð. |
| Líftímastaða afurðar við stofnun | Setjið upp sjálfgefna líftímastöðu afurðar sem hönnunarafurð á að vera með þegar hún er fyrst stofnuð. Frekari upplýsingar er að finna í [Líftímastöður afurðar og færslur](product-lifecycle-state-transactions.md). |
| Númeraregla útgáfu | Velja skal númeraregla útgáfunnar sem á við um flokkinn:<ul><li>**Handvirkt** – Notandi velur útgáfunúmerið fyrir hverja nýja útgáfu.</li><li>**Sjálfvirkt** – Kerfið stillir útgáfunúmerið samkvæmt sniði sem notandi skilgreinir. Þegar sniðið er sett upp skal nota númeratákn (\#) til að tákna gildi og einhvern annan staf til að tákna fast gildi. Ef þú til dæmis skilgreinir sniðið sem *V-\#\#*, verður fyrsta útgáfan „V-01“, seinni útgáfan verður „V-02“ og svo framvegis.</li><li>**Listi** – Kerfið tekur næsta númer úr fyrirframgefnum lista yfir sérsniðin gildi sem eru skilgreind.</li></ul> |
| Framfylgja virkni | Veljið hvort gildisdagsetningar hönnunarútgáfanna verði að vera samfelldar eða hvort megi vera bil á milli og skaranir. Þessi stilling hefur áhrif á það hvernig hægt er að nota reitina **Gildir frá** og **Gildir til** fyrir hverja hönnunarútgáfu þar sem flokkurinn á við.<ul><li>Ef þessi valkostur er stilltur á *Já* verður gildið **Gildir frá** að vera tilgreint fyrir hverja útgáfu og hvorki skaranir né bil eru leyfð milli útgáfa. Dagsetningabilið fyrir hverja hönnunarútgáfu er tengt beint við fyrri og næstu hönnunarútgáfur ef þær eru til. Í þessu dæmi er nýjasta útgáfan alltaf notuð og eldri útgáfur eru ekki lengur notaðar.</li><li>Ef þessi valkostur er stilltur á **Nei** eru engar takmarkanir á reitum gildisdagsetninga fyrir hönnunarútgáfur og bæði bil og skaranir eru leyfð. Í þessu dæmi geta margar útgáfur verið virkar á sama tíma og hægt er að vinna með allar virkar útgáfur.</li></ul><p>Þessi valkostur hefur einnig áhrif á uppskriftir og leiðir sem eru tengdar við útgáfu afurðar. Frekari upplýsingar er að finna í kaflanum [Tengja uppskrift og leiðir við útgáfur hönnunar](#boms-routes) seinna í þessu efnisatriði.</p> |
| Nota nafnakerfi númerareglu | Stillið þennan valkost á *Já* til að virkja reglur til að skilgreina afurðarnúmer með því að nota númeraraðir, heiti hönnunareiginda og gilda, og texta sem hluta. Til að stofna eða breyta reglum skal velja hnappinn **Breyta**. |
| Nota nafnakerfi heitisreglu | Stillið þennan valkost á *Já* til að virkja reglur til að skilgreina heiti með því að nota heiti hönnunareiginda, gildi hönnunareiginda og texta sem hluta. Til að stofna eða breyta reglum skal velja hnappinn **Breyta**. |
| Nota nafnakerfi lýsingarreglu | Stillið þennan valkost á *Já* til að virkja reglur til að skilgreina lýsinguna með því að nota heiti hönnunareiginda, gildi hönnunareiginda og texta sem hluta. Til að stofna eða breyta reglum skal velja hnappinn **Breyta**. |

### <a name="attributes-fasttab"></a>Flýtiflipi fyrir eigindir

Nota skal hnitanetið í flýtiflipanum **Eigindir** til að setja upp hönnunareigindir sem eiga við um afurðir sem tilheyra þessum flokki. Upplýsingar um hvernig á að búa til hönnunareigindir er að finna í [Hönnunareigindir og leit að hönnunareigind](engineering-attributes-and-search.md).

Nota skal hnappana í flýtiflipanum **Eigindir** til að bæta við, fjarlægja og raða eigindum í hnitanetið.

Ef val á eigindum er breytt fyrir hönnunarflokk og afurðir eru þegar til staðar sem byggja á þeim flokki, þarf að ákveða hvort eigi að gera þessar breytingar á þeim afurðum. Ef ætlunin er að fyrirliggjandi afurðir endurspegli breytingarnar, skal velja **Uppfæra fyrirliggjandi afurðir** í flýtiflipanum **Eigindir**.

Fyrir hverja línu sem bætt er við hnitanetið skal stilla eftirfarandi reiti.

| Svæði | lýsing |
|---|---|
| Nafn | Velja eigindina sem bæta á við. |
| Virði | Veljið sjálfgefið gildi fyrir eigindina. |
| Skylda | Fyrir eigindir af gerðinni *Boole-gildi*, ef þessi valkostur er stilltur á *Já*, þurfa notendur að stilla eigindina á *Já*. Ef þessi valkostur er stilltur á *Nei* geta notendur stillt eigindina annaðhvort á *Já* eða *Nei*. Fyrir aðrar gagnagerðir er stillingin fyrir þennan valkost bara til upplýsinga. |
| Runueigind | Veljið hvort dreifa eigi eigindinni í gegnum runuvirknina. |

### <a name="readiness-policy-fasttab"></a>Flýtiflipi undirbúningsreglu

Notaðu reitinn **Undirbúningsregla afurðar** til að velja undirbúningsregluna sem á að nota fyrir afurðir sem eru búnar til samkvæmt þessum hönnunarflokki. Frekari upplýsingar er að finna í [Undirbúningur afurðar](product-readiness.md).

> [!NOTE]
> Reiturinn **Undirbúningsregla afurðar** virkar örlítið öðruvísi ef kveikt hefur verið á eiginleikanum *Undirbúningsathuganir afurðar* í kerfinu. (Sá eiginleiki gerir kleift að nota undirbúningsreglur fyrir staðlaðar afurðir \[aðrar en hönnunarafurðir\]). Frekari upplýsingar eru í [Tilgreindu undirbúningsreglur fyrir hefðbundnar afurðir og hönnunarafurðir](product-readiness.md#assign-policy).

### <a name="release-policy-fasttab"></a>Flýtiflipi útgáfureglu

Notið reitinn **Útgáfuregla afurðar** til að velja útgáfuregluna sem á við um afurðir sem tilheyra þessum flokki. Frekari upplýsingar er að finna í [Skipulag afurðarútgáfu](release-product-structure.md).

## <a name="connect-boms-and-routes-to-engineering-versions"></a><a name="boms-routes"></a>Tengja uppskriftir og leiðir við hönnunarútgáfur

Stillingin á valkostinum **Framfylgja virkni** er mikilvæg fyrir tengingu uppskrifta og leiða við hverja hönnunarútgáfu. Aðeins er hægt að virkja margar uppskriftir eða leiðir á hverja afurð ef munur er á einhverjum eftirfarandi stillingum:

- Afurðarvídd
- Magn
- Vefsvæði
- Gildisdagsetningar

Hönnunaruppskriftir og leiðir eru stofnaðar í hönnunarútgáfunni þar sem þær eiga við. Hægt er að þekkja þær á gátmerkinu í gátreitnum **Stjórnað af hönnun**. Þegar unnið er með hönnunaruppskriftir og leiðir, hannarðu þær yfirleitt ekki með því að nota mismunandi magn. Þú munt einnig yfirleitt ekki hanna mismunandi uppskriftir á hvert svæði. Að auki, fyrir hönnunaruppskriftir og leiðir, eru gildisdagsetningar alltaf teknar frá hönnunarútgáfunni. Þess vegna verður hönnunarútgáfa, uppskrift hennar og leiðir með sömu gildisdagsetningarnar.

Fyrir afurðir þar sem notuð er afurðarvíddin *útgáfa* (ásamt vörustjórnunaráhrifum á færslurnar), er útgáfunni einnig bætt við uppskriftir og leiðir. Þessi hegðun hjálpar til við að aðgreina uppskriftir og leiðir samfelldra útgáfa, burtséð frá stillingunni **Framfylgja virkni**.

Fyrir afurðir þar sem ekki er notuð afurðarvíddin *útgáfa* (án vörustjórnunaráhrifa á færslurnar), er útgáfunni ekki bætt við uppskriftir og leiðir. Þess vegna verður enginn munur á uppskriftunum og leiðunum í samfelldum útgáfum. Í þessu tilfelli mælum við með því að valkosturinn **Framfylgja virkni** verði stilltur á *Já*. Á þennan hátt er hægt að koma í veg fyrir að hönnunarútgáfur skarist og einnig er hægt að virkja uppskrift og leið nýrrar útgáfu án þess að þurfa fyrsta að gera uppskriftina og leiðina óvirka í fyrri útgáfu. Ef valkosturinn **Framfylgja virkni** er stilltur á *Já* í þessu tilfelli, þarf fyrst að gera uppskriftir og leiðir í eldri útgáfum óvirkar handvirkt áður en hægt er virkja nýjustu útgáfuna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
