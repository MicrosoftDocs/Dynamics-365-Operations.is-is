---
title: Vinna með birtingarhópa
description: Þetta efnisatriði lýsir eiginleikum birtingarhópa í Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-12-12
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d757f34d3e16850e4f5de122f63b2b3342f612e49f07c7cf6585362999f03c02
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717673"
---
# <a name="work-with-publish-groups"></a>Vinna með birtingarhópa

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum birtingarhópa í Microsoft Dynamics 365 Commerce.

Vefsíður rafrænna viðskipta eru stöðugt uppfærðar með nýju efni allt árið. Uppfærslur eru oft gefnar út í runum í kringum upptekna viðburði netverslana eins og frídaga, árstíðabundnar markaðsherferðir eða kynningar. Þessar uppfærslur krefjast þess oft að hópar innihalds á vefsíðu (til dæmis síður, myndir, brot og sniðmát) séu stigsettir, staðfestir og gefnir út samtímis í einni aðgerð.

Getan til að flokka hluti í rökleg sett sem birta hluti saman, þar sem hvert sett hefur sína eigin líftíma, veitir höfundum marga kosti. Í Commerce eru þessi röklegu sett þekkt sem útgáfuhópar. Þau gera höfundum síðunnar kleift að rekja mengi uppfærslna sem eigin stillanlegar, prófanlegar og birtanlegar einingar.

Höfundar geta forskoðað uppfærslur í sviðsettum útgáfuhópi án þess að hafa áhrif á lifandi vefinn eða aðra sjálfstæða útgáfuhópa. Höfundar geta síðan tímasett útgáfuaðgerðina til að birta samtímis öll atriðin í útgáfnahópnum á lifandi vefinn. Getan til að flokka, forskoða og tímasetja uppfærslur er mikilvæg fyrir mörg fyrirtækjastig fyrirtækisins sem skila talsverðum árlegum tekjum í kringum tímamótabundna uppfærslu á vefsvæðum.

Fyrirtæki geta stofnað til kostnaðar vegna hægfara eða ógildrar útfærslu efnis sem gengur ekki vel. Úgtáfuhópar hjálpa til við að tryggja að ræsingar séu skipulagðar, staðfestar og gefnar út á réttum tíma. Hvort sem þeir eru stórir eða litlir, þá eru útgáfuhópar með dýrmæt verkfæri sem hjálpar höfundum að skipuleggja og einfalda áframhaldandi uppfærsluverk vefsvæða.

## <a name="when-to-use-publish-groups"></a>Hvenær á að nota útgáfuhópa

Þú getur notað útgáfuhópa hvenær sem þú verður að stigsetja og birta mörg skjöl saman. Til dæmis, ef vefsíðan þín uppfærir efni á hverju tímabili, getur þú búið til útgáfuhópa fyrir þessar árstíðabundnu markaðsáætlanir. Útgáfuflokkurinn „Haustárstíðabundin uppfærsla“ gæti innihaldið nýjar árstíðabundnar myndir, brot sem eru með árstíðabundin markaðsskilaboð, síður sem innihalda árstíðabundin vörusöfn eða aðrar árstíðabundnar uppfærslur á vefsíðum.

Kosturinn við útgáfuhópa er að þú getur stigsett margar uppfærslur samhliða. Til dæmis, skömmu eftir uppfærslu fyrir útgáfuhópinn „Haustárstíðabundin uppfærsla“ gæti verið innihaldsuppfærsla fyrir tiltekna fríhelgi. Í þessu tilfelli geturðu stigsett efni fyrir útgáfuhópinn „Haustárstíðabundin uppfærsla“ á sama tíma og þú stigsetur efni fyrir síðari útgáfuhóp „Haustfrísuppfærsla“. Hver útgáfuflokkur inniheldur sitt eigið einkvæma sett af blaðsíðum, myndum, brotum, sniðmátum og svo framvegis. Þú getur stigsett, forskoðað og staðfest þessa tvo útgáfuhópa sjálfstætt en samtímis. Síðan er hægt að áætla hvern útgáfuflokk til að birtast á vefsvæðinu á ákveðnum dagsetningum og tímum.

## <a name="turn-on-the-publish-groups-feature"></a>Kveikt á eiginleika útgáfuhópa

Aðgerðin sem birtir hópa er valfrjáls og kveikja verður á henni fyrir vefsvæðið.

Fylgdu þessum skrefum til að kveikja á útgáfuhópum fyrir vefsvæðið í höfundatækjum Commerce.

1. Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.
1. Undir **Svæðisstillingar** velurðu **Eiginleikar**.
1. Stilltu valkostinn **Útgáfuhópar** **Kveikt**.

## <a name="create-a-publish-group"></a>Stofna útgáfuflokk

Til að stofna útgáfuflokk fyrir vefsvæðið í höfundatólum Commerce skaltu fylgja þessum skrefum.

1. Í vinstri stýriglugganum velurðu **Útgáfuflokkar**.
1. Á efstu skipanastikunni velurðu **Nýtt**.
1. Í valmyndinni **Stofna útgáfuflokk**, undir **Birta heiti flokks**, slærðu inn lýsandi heiti. Veljið síðan **Í lagi**.

## <a name="set-the-publish-group-authoring-context"></a>Veldu samhengi höfundar útgáfuhópsins

Í Commerce er sjálfgefið höfundarsamhengi samhengi lifandi vefsvæðis. Samhengi höfundar við lifandi vefsvæði er sjálfgefið útlit þar sem þú getur skoðað og gert breytingar beint á vefsíðuna án þess að nota útgáfuhóp. Það táknar nýjustu beinar uppfærslur á birtri útgáfu af vefsíðunni. Ef samhengisstjórnun undir **Útgáfuflokkar** í vinstri stýriglugganum sýnir heitið **Lifandi síða** ertu að vinna í samhengi höfundar við lifandi vefsvæði. **Lifandi síða** er sjálfgefið heiti samhengistjórnunar. Annars sýnir samhengistjórnun nafn útgáfuhóps.

Til að vinna í útgáfuhópi verðurðu að skipta yfir í höfundaritunarútgáfuna fyrir það. Fylgdu einu af þessum skrefum til að stilla samhengi útgáfuhópsins.

- Í vinstri stýriglugganum velurðu samhengisstjórnunina beint undir **Útgáfuflokkar** og velur síðan heiti útgáfuflokksins af listanum yfir valkosit sem birtist. Samhengistjórnuninni er gefið nýtt heiti og sýnir heiti útgáfuhópsins.
- Í vinstri stýriglugganum velurðu **Útgáfuhópar** og síðan, undir **Útgáfuhópar**, velurðu heiti útgáfuhópsins. Samhengistjórnuninni er gefið nýtt heiti og sýnir heiti útgáfuhópsins.

Eftir að þú hefur valið samhengi höfundar við útgáfuhópa vinnur þú í því samhengi við birtingu hópsins þegar þú forskoðar og breytir innihaldi síðunnar.

Veldu samhengistjórnun til að fara aftur í sjálfgefið samhengi höfundaréttar með höfundarétti og síðan **Lifandi síða**.

## <a name="add-pages-or-other-items-to-a-publish-group"></a>Bættu síðum eða öðrum hlutum við útgáfuhóp

Eftir að þú hefur valið samhengi höfundar við höfundarútgáfu og samhengistjórnun í vinstri stýriglugganum sýnir nafn þess geturðu búið til efni alveg eins og þú gerir í sjálfgefnu samhengi lifandi vefsvæða. Þú getur líka bætt við núverandi síðum eða öðrum hlutum frá öðrum útgáfuflokkum eða frá samhengi lifandi vefsvæða.

Fylgdu þessum skrefum til að afrita núverandi síður í birtan hóp.

1. Veldu höfundarsamhengi sem á að afrita, og veldu síðan í vinstri stýriglugganum **Síður**.
1. Veldu síðuna til að bæta við útgáfuhóp.
1. Veldu á skipanastikunni **Afrita í útgáfuhóp**.
1. Í valmyndinni **Velja útgáfuhóp** velurðu útgáfuhópinn sem á að bæta síðunni við og veldu síðan **Í lagi**.

Þú getur notað sömu grunnskrefin til að búa til sérsniðnar vörusíður, vefslóðir, sniðmát, skipulag, brot og margmiðlunarbókareignir, eða til að bæta núverandi hluti af þessum gerðum við útgáfuhóp.

## <a name="validate-a-publish-group"></a>Staðfesta útgáfuflokk

Til að ganga úr skugga um að öll ósjálfstæði í efni birta hópa sé fullnægt og að öll staðfesting sé liðin geturðu keyrt staðfestingu til að bera kennsl á öll mál sem þarf að taka á áður en þú áætlar útgáfuaðgerð.

Fylgdu þessum skrefum til að staðfesta útgáfuhópinn þinn áður en þú áætlar hann.

1. Í vinstri stýriglugganum velurðu **Útgáfuflokkar**.
1. Veldu útgáfuhópinn sem á að staðfesta.
1. Á efstu skipanastikunni velurðu **Staðfesta**.

Fullgilding er keyrð á öllu efni í útgáfuhópnum. Öll vandamál sem koma í veg fyrir birtingu aðgerða birtast í tilkynningareit sem birtist efst til hægri.

> [!NOTE]
> Villuleit er alltaf keyrð sjálfkrafa þegar útgáfnahópur er áætlaður. Hins vegar er hnappurinn **Staðfesta** á skipanastikunni gagnlegur vegna þess að hann hjálpar til við að bera kennsl á vandamál sem verður að laga áður en þú reynir að áætla útgáfuhóp til að fara í gang.

## <a name="schedule-a-publish-group-to-go-live"></a>Áætla útgáfuhóp til að fara í gang

Fylgdu þessum skrefum til að áætla útgáfuhóp til að fara í gang á síðunni þinni.

1. Í vinstri stýriglugganum velurðu **Útgáfuflokkar**.
1. Undir **Útgáfuhópar** velurðu útgáfuhópinn sem á að áætla.
1. Á efstu skipanastikunni velurðu **Breyta áætlun**. Valmyndin **Breyta áætlun** birtist.
1. Veldu dagsetningu og tíma þegar útgáfuhópurinn ætti að fara í gang og veldu síðan **Í lagi**.

Fylgdu sömu skrefum til að taka útgáfuhóp úr áætlun, en veldu **Taka útgáfuhóp úr áætlun** í valmyndinni **Breyta áætlun**.

> [!NOTE]
> Mjög stórir útgáfuflokkar geta tekið allt að mínútu eða tvær til að verða gefnir út þegar áætlunartími þeirra rennur upp. Hafðu í huga að útgáfuaðgerð er ekki samstundis og að minni útgáfuflokkar verða gefnir út hraðar.

## <a name="publish-groups-faq"></a>Algengar spurningar um birtingarhópa

**Hve mörg atriði geta verið í útgáfuhóp?**

Eins og er eru takmörk upp á 2.000 atriði á hvern útgáfuhóp. Hafðu í huga að mjög stórir útgáfuflokkar geta tekið nokkrar mínútur til að verða gefnir út þegar áætlunartími þeirra rennur upp.

**Eru að útgáfuhópar eins og „kóðagreinar“ í hugbúnaðarþróun hugtakanna?**

Já og nei. Hægt er að hugsa um að útgáfuhópa sem kvíslgreindar útgáfur af síðunni. Þannig virka þeir eins og greinar. Hins vegar er ekkert hugtak um sameiningu á stigi einstakra atriða. Atriðið sem birt er síðast skrifar bara yfir það sem áður var og nýjasta útgáfuaðgerðin kemur alltaf í stað fyrri útgáfuaðgerða.

**Get ég tímasett tvo útgáfuhópa til að fara í gang á sama tíma?**

Nei. Vegna afkasta og árekstra mun kerfið neyða þig til að dreifa áætlaðum útgáfuhópum með að minnsta kosti fimm mínútna millibili.

**Get ég notað útgáfuhópa til að skipuleggja alhliða þjónustu á bakvinnslu vara, svo sem afslátt og vöruuppfærslur?**

Eins og stendur styður eiginleiki útgáfuhópa aðeins innihald vefsíðu. Hins vegar Microsoft er meðvitað um að samþætting við bakvinnslu á smásöluaðstæðum getur verið dýrmæt fyrir samhæfingu og sjálfvirkni alhliða kynningarherferðar.

## <a name="additional-resources"></a>Frekari upplýsingar

[Leiðir til að bæta við efni](add-manage-content.md)

[Orðalisti síðulíkans](page-elements-overview.md)

[Staða og líftími skjala](document-states-overview.md)

[Virkja og nota deilingu milli rása](cross-channel-sharing.md)

[Vinna með einingar](work-with-modules.md)

[Vinna með brot](work-with-fragments.md)

[Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md)

[Sérstilla yfirlit svæðis](customize-site-navigation.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
