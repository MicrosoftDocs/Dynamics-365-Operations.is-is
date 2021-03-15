---
title: Niðurstöður vélnámslíkana (forskoðun)
description: Í þessu efnisatriði er fjallað um fylkisrugling, flokkunarvandamál og nákvæmni í vélnámslíkönum. Markmiðið er að auka skilning á nákvæmni í niðurstöðum vélnámsspár.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-14
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 5223bdfbc0f5828b5dccac30362783075ce8157f
ms.sourcegitcommit: f59df61799915f6a79aec7e3e8664c02df6597da
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/22/2021
ms.locfileid: "5044373"
---
# <a name="results-of-machine-learning-models-preview"></a>Niðurstöður vélnámslíkana (forskoðun)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er fjallað um fylkisrugling, flokkunarvandamál og nákvæmni í vélnámslíkönum. Markmiðið er að auka skilning á nákvæmni í niðurstöðum vélnámsspár. Markhópurinn er meðal annars hönnuðir, greinendur og stjórnendur sem vilja auka þekkingu sína og hæfni í gagnafræðum.

## <a name="confusion-matrix"></a>Fylkisruglingur
Þegar stýrt vélnámsvandamál er þjálfað í safni af sögulegum gögnum er það prófað með því að nota gögn sem haldið er frá þjálfunarferlinu. Á þennan hátt er hægt að bera saman spár þjálfaða líkansins við raunveruleg gildi. Fylkisruglingur er leið til að meta hversu árangursríkt flokkunarvandamál er og hvar mistök eru gerð (þ.e. hvar „ruglingur“ á sér stað).

Til dæmis getur markmiðið verið að spá fyrir um hvort gæludýr sé hundur eða köttur byggt á líkamlegum eigindum og hegðunarmáta. Ef þú ert með tilraunagagnasafn sem inniheldur 30 hunda og 20 ketti, gæti ruglingsfylkið verið í líkingu við eftirfarandi mynd.

![Dæmi um spá á tegund](media/species-prediction-matrix.png)

Tölurnar í grænu reitunum tákna réttar spár. Eins og sjá má spáði líkanið hærri prósentu af raunverulegum köttum rétt. Auðvelt er að reikna út heildarnákvæmni líkansins. Í þessu tilvikum er það 42 ÷ 50 eða 0,84.

### <a name="multi-class-classifiers-in-a-confusion-matrix"></a>Fjölflokka flokkari í ruglingsfylki

Flestar umræður um ruglingsfylkið snúast um tvíundarflokkara eins og í fyrrgreindu dæmi. Þetta tilfelli er sérstakt tilfelli þar sem hægt er að hafa í huga aðrar mælingar, t.d. næmni og afturköllun.

Næst athugum við flokkunarvandamál fyrir fjármálaaðstæður sem er með þrjár stöður. Líkanið spáir fyrir um hvort reikningur viðskiptavinar verði greiddur tímanlega, of seint eða mjög seint. Sem dæmi, af 100 prufureikningum eru 50 greiddir á tíma, 35 of seint og 15 mjög seint. Í þessu tilfelli gæti líkan framleidd ruglingsfylki sem svipar til eftirfarandi myndar.

![Gerð 1](media/payment-prediction-matrix.png)]

Ruglingsfylki veitir umtalsvert meiri upplýsingar en einföld nákvæmnismæling. Það er samt sem áður frekar auðvelt að skilja það. Ruglingsfylki segir til um hvort þú sért með gagnasafn í jafnvægi þar sem úttaksklasarnir eru með svipaða fjölda. Fyrir aðstæður margra klasa segir það til um hversu langt frá spáin var þegar úttaksklasarnir eru raðnúmer, eins og í fyrrgreindu dæmi um greiðslur viðskiptavinar.

## <a name="model-accuracy"></a>Nákvæmni líkans 
Mismunandi nákvæmnismælingar hafa þann kost að magngreina gæði líkansins. 

Vegna þess að nákvæmni er auðveld mæling til að skilja, er hún góður upphafspunktur til að útskýra líkan fyrir öðrum, sérstaklega notendum líkansins sem eru ekki gagnasérfræðingar. Enginn skilningur á tölfræði er nauðsynlegur til að skilja nákvæmni líkansins. Þegar ruglingsfylki er í boði, veitir það frekari innsýn í afköstu líkansins.

Til að fá dýpri þekkingu eru hinsvegar nokkrar áskoranir sem tengjast nákvæmni sem þarf að hafa í huga. Notagildi mælingarinnar fer eftir eðli vandamálsins. Spurning sem kemur oft upp í sambandi við afköst líkansins er: „Hversu gott er líkanið?“ En þeirri spurningu er ekki auðsvarað. Íhugið eftirfarandi ruglingsfylki (líkan 2).

![Dæmi um greiðsluspá með stærra sýni](media/payment-prediction-matrix-2.png)

Skyndiútreikningur sýnir að nákvæmni þessa líkans er (70 + 10 + 3) ÷ 100 eða 0,83. Á yfirborðinu virðist þessi útkoma vera betri en niðurstöður fyrir fyrra fjölflokka líkanið (líkan 1) sem var með nákvæmni upp á 0,73. En er þetta betra?

Til að reyna að svara þessari spurningu þarf að skoða nákvæmni á einfaldri ágiskun. Fyrir flokkunarvandamál mun einfalt gisk alltaf spá algengasta klasanum. Fyrir líkan 1 mun sú ágiskun verða „á réttum tíma“ og mun nákvæmnin verða 0,50. Ágiskunin fyrir líkan 2 verður einnig „á réttum tíma“ og mun nákvæmnin verða 0,80. Vegna þess að líkan 1 bætir við blinda ágiskun um 0,73 – 0,50 = 0,23, en líkan 2 bætir við blindu ágiskunina um 0,83 – 0,80 = 0,03, líkan 1 er betra líkan, jafnvel þótt það sé með minni nákvæmni. Útreikningurinn sýnir að virkt mat á gæði líkans krefst meira samhengis en nákvæmnisgildið.

Annan þátt er vert að skoða. Sjáið fyrir ykkur aðstæður þar sem læknisfræðilegt próf er notað til að greina sjúkdóm hjá sjúklingi. Þetta vandamál er flokkunarvandamál með tveimur útkomum þar sem jákvæð niðurstaða gefur til kynna að sjúklingurinn er með sjúkdóminn. Í þessu tilfelli verður að hugsa um áhrif eftirfarandi villna:

- Rangar jákvæðar greiningar, þar sem prófið segir að sjúklingur sé með sjúkdóminn, en hann er ekki með hann í raun
- Rangar neikvæðar greiningar, þar sem prófið segir að sjúklingur sé ekki með sjúkdóminn, en hann er í raun með hann

Augljóslega eru báðar gerið villu óæskilegar, en hvor er það verri? Aftur, það veltur á ýmsu. Ef um er að ræða lífshættulegan sjúkdóma sem þarfnast snöggrar meðferðar, fær lágmörkun á röngum neikvæðum greiningum (vonandi fylgt eftir með frekari prófum) forgang. Í öðrum, ekki eins mikilvægum aðstæðum, gætu hönnuðir líkansins vilja lágmarka rangar jákvæðar greiningar í staðinn. Burtséð frá því, þá er ásættanleg niðurstaða sú að til að ákvarða gæði líkansins á árangursríkan hátt þarf að fá meiri upplýsingar en nákvæmnismæling veitir.

### <a name="recommendations"></a>Ráðleggingar

Nákvæmni er mikilvægt verkfæri til að eiga samskipti við lénasérfræðinga sem ekki eru vanir tölfræði. Til að gera upplýsingarnar gagnlegar er hinsvegar áríðandi að viðbótarsamhengi sé gefið upp ásamt nákvæmnisgildinu.

Fyrir aðstæður greiðsluspár er hægt að stilla markmið fyrir vélnámslíkanið sem inniheldur þætti í mismunandi greiðsluhegðunum. Markiðmiðið er að líkanið eigi að bæta sig þegar blind ágiskun er gerð með því að draga úr fjölda rangra svara um að minnsta kosti 50 prósent. Með öðrum orðum er ætlunin að ná nákvæmni sem skiptir muninum á milli nákvæmni blindrar ágiskunar og 100 prósent.

Eftirfarandi tafla tekur saman þessa reglu fyrir ruglingsfylkin í þessu efnisatriði.

| Tegund   | Blind ágiskun | Mark | Nákvæmni líkans | Er markmiðum náð?                                          |
|---------|-------------|--------|----------------|-----------------------------------------------------------|
| Gerð 1 | 0.50        | 0.75   | 0.73           | Næstum. Þetta líkan bætir sig verulega við ágiskunina. |
| Gerð 2 | 0.80        | 0.90   | 0.83           | Nei. Betrumbætur eru nauðsynlegar.                              |

## <a name="classification-f1-accuracy"></a>Nákvæmni F1 flokkunar

Það sem þarf að hafa í huga að lokum í þessu efnisatriði er ítarlegri mæling á afköstum vélnámsflokkunar sem er þekkt sem F1 nákvæmni.

Áður en hægt er að skilgreina F1 nákvæmni þarf að kynna tvo frekari mælikvarða: samkvæmni og endurkall. Samkvæmni gefur til kynna hversu mörgum af heildarfjölda spáa sem eru tilgreindar sem jákvæðar eru rétt úthlutaðar. Þessi mæling er einnig þekkt sem jákvætt spágildi. Afturköllun er heildarfjöldi raunverulegum jákvæðum málum sem var spáð rétt. Þessi mæling er einnig þekkt sem næmni.

[![Réttar niðurstöður vs. rangar niðurstöður](./media/tn-fn.png)](./media/tn-fn.png)

Í ruglingsfylkinu í fyrrgreindri mynd eru þessar mælingar reiknaðar á eftirfarandi hátt:

- Nákvæmni = TP ÷ (TP + FP)
- Afturkalla = TP ÷ (TP + FN)

F1-mælingin sameinar samkvæmni og afturköllun. Niðurstaðan er þýtt meðaltal gildanna tveggja. Það er reiknað á eftirfarandi hátt:

- F1 = 2 × (samkvæmni × afturköllun) ÷ (samkvæmni + afturköllun)

Lítum á dæmi. Fyrr í þessu efnisatriði kom fram dæmi um líkan sem spáði því hvort dýr væri hundur eða köttur. Myndin er endurtekin hér.

[![Dæmi um spá á tegund (endurtekið)](./media/species-prediction-matrix.png)](./media/species-prediction-matrix.png)

Hér eru niðurstöðurnar ef „hundur“ er notaður sem jákvæða svarið.

- Nákvæmni = 24 ÷ (24 + 2) = 0,9231
- Afturkalla = 24 ÷ (24 + 6) = 0,8
- F1 = 2 × (0,9231 × 0,8) ÷ (0,9231 + 0,8) = 0,8572

Eins og sjá má er F1-gildið á milli gildanna fyrir samkvæmni og afturköllun.

Þrátt fyrir að ekki sé eins auðvelt að skilja F1-nákvæmni, bætir hún blæbrigðum við grunntölu nákvæmninnar. Hún getur einnig hjálpað til við ójafnað gagnasafn eins og eftirfarandi umræður sýna.

Hlutinn [Nákvæmni líkans](#model-accuracy) í þessu efnisatriði bar saman eftirfarandi tvö ruglingsfylki. Þrátt fyrir að fyrsta líkanið hafði lægri nákvæmni var það gagnlegra líkan vegna þess að það sýndi meiri framför en sjálfgefin ágiskun um greiðslu á réttum tíma.

![Dæmi um greiðsluspá í samanburði við rauntölur](media/payment-prediction-matrix.png)

![Dæmi um greiðsluspá með stærra sýni (endurtekið)](media/payment-prediction-matrix-2.png)

Við skulum skoða mismun þessara tveggja líkana þegar F1 stig er notað. F1-stigaþátturinn í samkvæmni og afturköllun fyrir hvert stig og F1-fjölvareikningurinn finnur meðaltal F1-stiga fyrir allar stöðurnar til að ákveða heildarstig F1. Til eru önnur F1-afbrigði, en hagstæðara er að taka tillit til fjölvaútgáfunnar, ef öllum þremur stigunum er gefið jafnmikið vægi.

Til að einfalda útreikningana voru sýnisfylki smíðuð til að passa við raungildin og spágildin. Þessi fylki nota sklearn-mælingarsafn úr Python til að reikna út gildin. Hér er sjálfgildið.

| Tegund   | Blind ágiskun | Nákvæmni | F1 fjölvi |
|---------|-------------|----------|----------|
| Gerð 1 | 0.5         | 0.73     | 0.67     |
| Gerð 2 | 0.80        | 0.83     | 0.66     |

Frekari upplýsingar um hvernig þessi útreikningur virkar er að finna í sklearn.metrics flokkunarskýrslunni fyrir líkan 1. Stigin þrjú: „Á réttum tíma“, „Seint“ og „Mjög seint“ eru sýnd í línunum sem eru merktar 1, 2 og 3. Fjölvameðaltalið er aðeins meðaltalið í dálknum „f1-stig“.

|           | nákvæmni | afturkalla   | F1-stig |
|-----------|-----------|----------|----------|
| **1**     | 0.83      | 0.80     | 0.82     |
| **2**     | 0.68      | 0.71     | 0.69     |
| **3**     | 0.50      | 0.50     | 0.50     |

Eins og þessar niðurstöður sýna eru líkönin tvö með næstum sömu nákvæmnisstigin fyrir F1-fjölva. Í þessu og mörgum öðrum tilvikum veitir F1 nákvæmni betri vísbendingu um getu líkans. Hvað varðar nákvæmni, túlkun niðurstaðanna krefst þess að þú skiljir hvað er mikilvægast að hafa í huga í líkaninu.

#### <a name="privacy-notice"></a>Tilkynning um persónuvernd
Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]