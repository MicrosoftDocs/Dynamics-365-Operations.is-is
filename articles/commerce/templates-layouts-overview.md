---
title: Yfirlit yfir sniðmát og útlit
description: Þessi grein fjallar um sniðmát og útlit í Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 12/12/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: adf1585e418ca2d09065db03de72cb1bbfb3e614
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844621"
---
# <a name="templates-and-layouts-overview"></a>Yfirlit yfir sniðmát og útlit


[!include [banner](includes/banner.md)]

Sniðmát eru grunneiningar Microsoft Dynamics 365 Commerce síðulíkans. Ef markmið þitt er að hámarka skilvirkni og samræmi í vinnuferlum höfundar er mikilvægt að þú kynnir þér hvernig þú getur nýtt þér sniðmát fyrir vefsíðuna. Snemmbærar ákvarðanir um uppbyggingu sniðmáts eru mikilvægar og geta haft veruleg áhrif á kostnað og snerpu við daglegar, árstíðabundnar og vefsvæðis vörumerkisuppfærslur. Vel skipulögð sniðmát hafa líka aðra kosti. Til dæmis hjálpa þau til við að bæta stig á SEO (SEO) og lágmarka fjölda galla.

Góð leið til að byrja að vinna með sniðmát er að skilja virkan ávinning sniðmáta og skipulags, muninn þar á milli og stigveldi.

Eftirfarandi mynd sýnir stilgveldi síðulíkans á bak við útgefna vefsíðu.

![Skýringarmynd síðulíkans.](../commerce/media/page-model-diagram.png)

| Eining        | Grunnaðgerð |
|---------------|----------------|
| Sniðmát      | Sniðmát skilgreina einingavalkostina og grunnvinnupalla fyrir safn skipuags og síðutilvika. |
| Útlit        | Skipulag skilgreinir endanlegt val og skipulag eininga fyrir síðu eða hóp af síðum. |
| Síðutilvik | Síðutilvik skilgreina gögn og efni fyrir tilteknar síður. |

## <a name="templates"></a>Sniðmát

Sniðmát eru efst á Dynamics 365 Commerce stigveldi síðulíkans og eru mikilvæg snemmtæk skref fyrir stillingu vefsvæðisins. Hugmyndafræðilega hjálpar sniðmát til að stjórna samræmi milli fjölskyldu undirupplýsinga og síðna með því að skilgreina grunnbyggingu og höfundarvalkosti fyrir útlitssköpun og verkflæði til að búa til síður. Sniðmát geta hjálpað til við að einfalda höfundarferlið með fyrirfram skilgreindum, miðstýrðum þáttum (svo sem fyrirsögnum og síðufótum) og leiðsögn höfundastreymis sem hjálpar til við að tryggja að val á einingastillingum er á vörumerkinu.

### <a name="controlling-consistency"></a>Stjórna samræmi

Þegar þú hannar sniðmát er stærsta viðskiptaákvörðunin sem þú verður að taka hversu mikil stjórn sniðmátið ætti að hafa yfir sköpunarferlinu. Sniðmát sem skilur allt eftir fyrir höfundi í forstreymi er auðveldasta gerð sniðmáts til að búa til, en það gæti haft langtímaafleiðingar fyrir viðhald síðna sem eru búnar til úr því. Vel skrifað sniðmát veitir leiðbeiningar og straumlínulagaða höfundareynslu, en það veitir höfundum einnig nægan sveigjanleika svo þeir geti klárað verkefni sitt. Allir þessir þættir eru háðir því stjórnunarstigi sem sniðmátið framfylgir.

Sniðmát geta hjálpað höfundum efnisins að vera skilvirkari og vera á vörumerki á eftirfarandi hátt:

- Takmarka einingarnar sem hægt er að nota á síðu.
- Stinga upp á sjálfgefnum einingum og stillingum.
- Gerðu skýrlega nokkrar val á einingum og stillingum sem stjórnað er á sniðmátstigi. Þetta ferli er einnig þekkt sem *læsa* stillingu.

Eftirfarandi dæmi sýnir hvernig hægt er að stilla grunnsniðmát (sniðmát X):

- Allt undirskipulag sniðmáts X verður að hafa fyrirsagnargám, meginmálsgám og síðufótargám.
- Í sniðmáti X eru stillingar fyrirsagnargámsins læstar og aðeins hægt að breyta þeim í sniðmáti X sjálfu. Allt undirskipulag og síður eru alltaf með þessa fyrirsögn.
- Meginmálsgámur þarf að minnsta kosti eina einingu og að hámarki tíu einingar. Þessar einingar eru skilgreindar af forstreymisskipulagi og -síðum.
- Fyrir meginmálsgáminn eru einingarnar hetja, eiginleiki, hringekja og borði í boði.
- Síðufótargámur er stilltur í sniðmáti X, en honum er hægt að hnekkja með forstreymisskipulagi og -síðum.

Sniðmátið í þessu dæmi skilgreinir einfalda uppbyggingu og mengi valkosta fyrir höfunda forstreymisefnis. Taktu eftir að sumir hlutar síðu (í þessu tilfelli fyrirsögnin) eru að fullu skilgreindir og læstir í sniðmátinu og ekki er hægt að breyta þeim af forstreymishöfunda. Hægt er að skilgreina aðra hluti (í þessu tilfelli meginhlutann) af forstreymishöfundum innan sérstakra leiðbeininga (í þessu tilfelli, lágmarksfjölda og hámarksfjölda eininga af tilteknum gerðum). Og aðrir hlutar (í þessu tilfelli, síðufóturinn) eru skilgreindir í sniðmátinu en þeim getur verið hnekkt af forstreymishöfundum.

Mikilvægt upphafsskref fyrir umsjónarmenn vefsvæða og vörumerkis er að ákvarða rétt jafnvægi milli takmarkana og sveigjanleika fyrir undirskipulag og síðuhöfunda. Þegar sniðmát eru notuð er þetta jafnvægi algerlega stillanlegt. Það hefur áhrif á hvort síðuþættir eru miðlægt uppfærðir (læstir í sniðmátinu) eða látnir eftir einstöka undirstigum sem eru neðar í síðustigveldinu.

Til að byrja að nota sniðmát, [Vinna með sniðmát](work-with-templates.md).

## <a name="layouts"></a>Útlit

Skipulag er næsta stig í stigveldi síðulíkana, fyrir neðan sniðmát. Meðan sniðmát skilgreinir allar einingar sem leyfðar eru fyrir síðu, er skipulag skýrt val og fyrirkomulag eininga. Síður eru næsta stig í stigveldi síðulíkana, fyrir neðan skipulag. Þær skilgreina staðbundið efni fyrir einingarnar sem eru valdar í skipulaginu.

Eftirfarandi dæmi byggir á sniðmátsdæminu úr fyrri hlutanum og sýnir hvernig hægt er að stilla grunnskipulag:

- Yfirsniðmát skipulags krefst þess að meginmálsgámurinn hafi á milli einnar og tíu eininga. Þessar einingar geta aðeins verið hetja, eiginleiki, hringekja og borðaeiningar. Þess vegna getur skipulagið skilgreint eftirfarandi val og tilhögun eininga:

    - Fyrsta einingin í meginmálsgámnum er borðaeining og henni er fylgt eftir með hetjueiningunni og tveimur eiginleikaeiningum.
    - Fyrsta eiginleikaeiningin er vinstrijöfnuð og önnur eiginleikaeiningin er hægrijöfnuð.

- Jafnvel þó að sjálfgefinn síðufótur sé arfur úr yfirsniðmátinu lét sniðmátshöfundur síðufótinn vera opinn. Þess vegna er hægt að hnekkja skipulaginu með því að skilgreina annað síðufótarbrot.

Skipulagið í þessu dæmi skilgreinir lokafyrirkomulag eininga fyrir undirsíður. Eins og sniðmát getur skipulag skilgreint sjálfgefna eða læsta einingareiginleika sem munu alltaf erfast af undirsíðum (til dæmis, aðlögun eiginleikaeininganna). Raunverulegt innihald eða gögn fyrir hverja einingu í skipulaginu er síðan skilgreint lengra niður í stigveldið, í hverju undirsíðutilviki. Mikilvægur greinarmunur hér er að skipulag inniheldur ekki beint staðbundið efni en undirsíður þess gerir það. Aðalhlutverk útlitsins er að skilgreina lokafyrirkomulag og sjálfgefna stillingu eininga fyrir undirsíður þess.

Þetta stigveldi er öflugt af tveimur ástæðum. Í fyrsta lagi er farið með skipulag sem deilir sama yfirsniðmáti sem samhæft fyrir skipulagsskiptaaðstæður. Þess vegna er hægt að breyta skipulagi fyrir hverja síðu í annað skipulag úr sama stigveldi sniðmáta án þess að krefjast þess að innihald síðustigs verði endurheimt. Þú getur nýtt þér þessa getu til að gera árstíðabundnar hönnunaruppfærslur, gera tilraunir eða gera varanlega endurhönnun á vefnum. Í öðru lagi er skipulag aðrar leiðir til að breyta miðlægum þáttum fyrir hóp af síðum miðlægt án þess að þurfa uppfærslur á einstökum síðum. Til dæmis, ef vöruflokkur er með 1.000 síður sem deila sama skipulagi, er hægt að endurskipuleggja einingarnar í skipulaginu og þessi breyting mun strax koma fram á öllum 1.000 undirsíðum.

Með því að skilja þetta stigveldi geturðu skilað lipri og skilvirkri uppbyggingu vefsins sem hjálpar til við að spara kostnað, er kvarðanleg og skilar betri árangri þegar vefurinn þróast með tímanum.

### <a name="preset-and-custom-layouts"></a>Forstillt og sérsniðið skipulag

Skipulag á vefsvæðinu getur verið annaðhvort *forstillt* eða *sérsniðið*:

- **Forstillt skipulag** gerir ráð fyrir verkflæði síðustofnunar þar sem allar einingar eru nú þegar valdar og raðað og aðeins þarf að slá inn gögn. Þessi nálgun getur hjálpað til við að spara tíma þegar margar síður verða að vera höfundar sem hafa sömu skipulagskröfur. Forstillt skipulag hefur eitt til margt vensl við undirsíður sínar. Þess vegna er hægt að nota eitt forstillt skipulag til að stjórna einingafyrirkomulaginu miðlægt fyrir hundruð eða þúsundir undirsíðna.
- **Sérsniðið skipulag** eru í meginatriðum einnota skipulag sem eru felldar inn á eina síðu. Þeir eru ekki afhjúpaðir sem valkostur þegar aðrar nýjar síður eru búnar til eða í skipulagsskiptiaðstæðum. Ávinningurinn af þessari nálgun er að höfundur getur gert tilraunir með því að skrifa síðu sem notar sérsniðið skipulag. Síðan, ef höfundur vill endurnýta skipulag fyrir aðrar síður, er auðvelt að breyta því í forstillt skipulag. Nýja forstillta skipulagið er síðan afhjúpað sem valkostur í verkferlum síðusköpunar og í skipulagsskiptaaðstæðum fyrir síður úr sama stigveldi sniðmáta. Hins vegar er hægt að flokka forstillt skipulag í sérsniðið skipulag. Á þennan hátt getur höfundur brotið síðu frá forstilltu skipulagi og búið til nýtt sérsniðið einnota skipulag. (Þetta nýja sérsniðna skipulag er ennþá bundið af öllum takmörkunum í yfirsniðmátinu.)

Forstillta skipulag og sérsniðnar skipulag er breytt í mismunandi hlutum höfundatækjasafnsins. Vegna þess að sérsniðið skipulag er ekki háð öðrum síðum er þeim breytt beint í ritlinum. Í þessu tilfelli er tilvist skipulags að mestu gegnsæ fyrir notandann og birtist aðeins í eiginleikum á síðustigi og með aðgerðum fyrir skipulagsvalkosti. Vegna þess að breytingar á forstilltu skipulagi geta haft áhrif á margar yfirsíður verður að breyta þeim í ritstjóraritlinum, þar sem birtar aðgerðir líta svo á að öll áhrif neðri hluta undirsíðna séu.

Eftirfarandi myndir sýna atburðarás fyrir forstillt og sérsniðið skipulag.

![Forstilltar og sérsniðnar skipulagsaðstæður.](../commerce/media/template-figure1.png)

Til að byrja að nota forstilltar skipulag, sjá [Vinna með forstillt skipulag](work-with-layouts.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Vinna með sniðmát](work-with-templates.md)

[Vinna með forstillt útlit](work-with-layouts.md)

[Unnið með birta hópa](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]