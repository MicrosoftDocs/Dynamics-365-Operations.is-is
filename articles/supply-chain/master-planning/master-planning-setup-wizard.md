---
title: Leiðsagnarforrit fyrir uppsetningu áætlanagerðar
description: Þetta efni lýsir ýmsum mikilvægum áætlunum og breytum sem eru notaðar til að setja upp aðaláætlanagerð.
author: t-benebo
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 770800e63de73c60e0e811734d4273ff2392620f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829691"
---
# <a name="master-planning-setup-wizard"></a>Leiðsagnarforrit fyrir uppsetningu áætlanagerðar

[!include [banner](../includes/banner.md)]

Þetta efni veitir leiðbeiningar fyrir **Leiðsagnarforrit fyrir uppsetningu áætlanagerðar**. Það útskýrir hvernig færibreytutillögur eru reiknaðar og einnig eru dæmi sem sýna hvernig mismunandi fyrirtæki setja upp aðalskipulagningu, byggt á viðskiptaþörf þeirra.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3YnSB]

[Leiðsagnarforrit fyrir uppsetningu áætlanagerðar í Dynamics 365 Supply Chain Management](https://youtu.be/c-e6n-8rZb4) (sýnt hér að ofan) er innifalið í [Finance and Operations spilunarlista](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) sem er tiltækur í YouTube.


## <a name="specific-requirements-of-your-company"></a>Sérstakar kröfur fyrirtækisins

Á fyrstu síðu leiðsagnarforritsins er spurt um sérstakar kröfur fyrirtækisins. Svör þín við þessum spurningum þurfa ekki að vera nákvæm, heldur ættir þú að geta gefið grófa áætlun um fjölda atriða og fyrirhugaðar pantanir fyrir lögaðila. Svör þín eru notuð til að stilla breytur sem eiga við lögaðila þína, ekki bara aðalskipulagið sem þú valdir. Eftirfarandi hlutar lýsa breytunum sem eru reiknaðar og formúlunum sem notaðar eru.

### <a name="number-of-threads"></a>Fjöldi þráða

- **Ef þú framleiðir einhverjar af vörunum:** Fjöldi þráða = Fjöldi pantanatillaga ÷ 1.000
- **Ef þú framleiðir engar af vörunum:** Fjöldi þráða = Fjöldi vara ÷ 1.000

Ef fjöldi þráða sem reiknaður er yfir 75 prósent af fyrirliggjandi fjölda þráða er það hámarkað 75 prósent af fjölda þráða sem er í boði fyrir hvern viðskiptavin. (Fjöldi fyrirliggjandi þráða verður ákvarðaður fyrir hvern viðskiptavin.)

Nánari upplýsingar er að finna í [Fjöldi þráða](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).

### <a name="bundle-size"></a>Búntastærð

Stærð búntsins verður stillt á **1**. Þetta gildi er oft besta gildi, vegna þess að það hjálpar til við að bæta afköst aðalskipulagningar.

Sjá frekari upplýsingar í [Fjöldi verka í hjálparverkbúnti](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).

### <a name="firming-bundle-size"></a>Staðfesting búntstærðar

- **Ef þú framleiðir eitthvað af hlutunum:** Staðfest búntstærð verður stillt á stærra þessara tveggja gilda: **10** og búntútreikninginn
- **Ef þú framleiðir enga af hlutunum:** Staðfest búntstærð verður stillt á stærra þessara tveggja gilda: **50** og búntútreikninginn

Útreikningur á búnti = (Fjöldi fyrirhugaðra pantana × (girðingartími girðingar ÷ Tími girðingar) ÷ Fjöldi þráða) ÷ 10

### <a name="cache-size"></a>Stærð skyndiminnis

Stærð skyndiminnis verður stillt á **Hámark**. Þetta gildi er oft besta gildi, vegna þess að það hjálpar til við að bæta afköst aðalskipulagningar.

Sjá frekari upplýsingar í [Úthlutun tíma á vinnslur í vinnslubúnti](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).

### <a name="manufacturing-setup"></a>Framleiðsluuppsetning

Ef þú framleiðir hluti, mun síðan **Framleiðsluuppsetning** birtast seinna í leiðbeiningaforritinu.

## <a name="scope-of-the-current-plan"></a>Umfang núverandi áætlunar

Á síðunni **Umfang núverandi áætlunar** í leiðbeiningaforritinu svarar þú spurningum sem tengjast því hversu langt í framtíðinni ýmsar kröfur verða teknar til greina og reiknaðar út í aðalskipulagningu. Hver spurning spyr hvort þú viljir nota eiginleika og hvernig þú vilt stilla hann.

Til dæmis, fyrir spááætlunaraðgerðina, spyr leiðbeiningaforritið: "Viltu nota spááætlun í aðalskipulagningu svo að fyrirhugaðar pantanir verði lagðar til að uppfylla spáða eftirspurn?"

Eftirtaldir valkostir eru í boði:

- **Nei** - Skipulag áætlunarinnar mun ekki leggja til fyrirhugaðar pantanir til að uppfylla spá. Á flipanum **Tímamörk** á síðunni **Aðaláætlanir** (**Aðalskipulagning \> Uppsetning \> Áætlanir \> Aðaláætlanir**) mun leiðbeiningaforritið stilla valkostinn **Spá áætlun (tímamörk)** á **Já** og stilla fjölda daga á **0** (núll). Þessi skipulag mun hnekkja tímamörkunum sem eru tilgreind í umfjöllunarhópnum. Vegna þess að fjöldi daga er stilltur á **0** (núll), aðgerðin verður ekki notuð.
- **Já, eins og skilgreint er í þessu aðalskipulagi** - Reitur verður aðgengilegur, þar sem þú getur fært inn þann fjölda daga sem aðalskipulagningin leggur til fyrirhugaðar pantanir til að uppfylla spáða eftirspurn. Leiðsagnarforritið mun stilla valkostinn **Spáð áætlun (tímamörk)** á **Já** og stilla fjölda daga á þann fjölda daga sem er skráður í reitinn **Spáð áætlun** á flipanum **Tímamörk** á síðunni **Aðaláætlanir**. Þessi skipulag mun hnekkja gildunum sem eru stillt í þekjuhópunum.
- **Já, eins og skilgreint er í þekjunni** - Leiðsagnarforritið mun stilla valkostinn **Spá áætlun (tímamörk)** á **Nei**. Tímamörkin sem eru tilgreind í þekjuhópnum verða notaðar til að tilgreina hve lengi þú ætlar að spá fyrir um.

Eftirstandandi spurningar á þessari síðu og svör þeirra fylgja sama stef:

- **Nei** - Valkosturinn **Spá áætlun (tímamörk)** verður stilltur á **Já**, og fjöldi daga verður stilltur á **0** (núll).
- **Já, eins og skilgreint er í þessari aðaláætlun** - Valkosturinn **Spá áætlun (tímamörk)** verður stilltur á **Já**. Fjöldi daga sem þú slærð inn verður notaður og mun hnekkja gildunum sem eru sett í þekjuhópunum.
- **Já, eins og skilgreint er í þekjuhópnum** - Valkosturinn **Spá áætlun (tímamörk)** verður stilltur á **Nei**.

Sjá [Vinnsluröðun](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling) fyrir frekari upplýsingar um vinnsluröðun.

## <a name="scheduling-options"></a>Valkostir tímaskráningar

Síðan **Tímasetningarvalkostir** birtist aðeins ef þú svaraðir **Já** við „Framleiðir þú eitthvað af fyrirhuguðum hlutum?“ spurningunni á fyrstu síðu leiðsagnarforritins.

Svar þitt við fyrstu spurningunni á þessari síðu ("Þarftu að skipuleggja aðgerðir skipt upp í einstök störf?") ákvarðar tímasetningaraðferðina á flipanum **Almennt** á síunni **Aðaláætlanir**.

- **Já** - Vinnsluröðun verður notuð.
- **Nei** - Aðgerðaröðun verður notuð.

Nánari upplýsingar er að finna í [Aðgerðaröðun](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) og [Vinnsluröðun](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).

## <a name="updates-of-demand-and-supply"></a>Uppfærslur eftirspurnar og framboðs

Spurningarnar á síðunni **Uppfærslur á eftirspurn og framboði** tengjast styrkingu, aðgerðarskilaboðum og töfum.

Uppbygging aðalskipulagsins verður uppfærð út frá svörum þínum samkvæmt sama skema og lýst er í fyrri hlutanum:

- **Nei** - Valkosturinn **Tímamörk** á síðunni **Aðaláætlanir** verður stilltur á **Já**, og fjöldi daga verður stilltur á **0** (núll).
- **Já, eins og skilgreint er í þessari aðaláætlun** - Valkosturinn **Tímamörk** verður stilltur á **Já**. Fjöldi daga sem þú slærð inn verður notaður og mun hnekkja gildunum sem eru sett í þekjuhópunum.
- **Já, eins og skilgreint er í þekjuhópnum** - Valkosturinn **Tímamörk** verður stilltur á **Nei**.

Fyrir reiknaðar tafir munu svör þín við spurningum í leiðsagnarforritinu uppfæra samsvarandi breytur á flipanum **Reiknaðar tafir** á síðunni **Aðaláætlanir**.

## <a name="summary-of-your-changes"></a>Samantekt um breytingarnar

Síðasta síðan í leiðsagnarforritinu sýnir þær breytingar sem mælt er með miðað við svör þín. Það sýnir bæði gildi í uppsetningu þinni (**Núverandi skipulag**) og gildi sem leiðsagnarforritið mælir með (**Ný stilling**).

Þú getur einnig breytt breytunum í nýju stillingunum. Færibreyturnar eru aðgreindar í breytur sem eiga við lögaðila þína og breytur sem eiga aðeins við aðalskipulagið sem þú valdir. Veldu til að skoða allar uppsetningarfæribreytur sem hægt er að breyta með leiðsagnarforritinu **Sýna allar breytur** neðst á síðunni. Þú getur síðan breytt breytunum.

Að lokum, þegar þú velur **Klára** er nýju stillingunni beitt. Ef þú velur **Hætta við** er engum af breytingunum beitt.

## <a name="examples"></a>Dæmi

Þessi hluti lýsir uppsetningu tveggja skáldaðra fyrirtækja til að sýna hvernig skipulagið getur breyst í samræmi við þarfir hvers fyrirtækis.

### <a name="example-1-contoso-manufacturer"></a>Dæmi 1: Framleiðandi Contoso

Contoso Framleiðandi er framleiðslufyrirtæki sem framleiðir hátalara. Það kaupir hin ýmsu hráefni og íhluti sem eru notaðir fyrir lokahátalara frá ýmsum birgjum. Hér eru nokkur einkenni framboðs og framleiðslu þess:

- Lokahlutirnir sem fyrirtækið framleiðir eru með efnisreikning (BOM) uppbyggingu.
- Allir lokahlutir og íhlutir eru skipulagðir með aðalskipulagningu. Handvirk skipulagning er ekki gerð.
- Aðgerðarleið er skilgreind fyrir framleiðslu hvers lokaafls.
- Framleiðslustöðin framleiðir lokahlutina. Það hefur skilgreindan fjölda malunar- og borvéla sem eru notaðar til að vinna úr íhlutunum. Þessar vélar verða að vinna úr hinum ýmsu íhlutum.
- Það eru margir birgjar. Meðalafgreiðslutími fyrir hluti er ein vika. Hópur af vörum frá sama birgi mun hafa sjö vikna afgreiðslutíma.

Í leiðsagnarforritinu eru eftirfarandi gildi færð fyrir Contoso framleiðanda:

- **Þekja:**

    - **Spurning:** "Viltu tilgreina fjölda daga áætlunarhorfsins þíns?"
    - **Svar:** "Já, eins og skilgreint er í þekjuhópunum."

    Vegna þess að afgreiðslutími fyrir hluti er mjög mismunandi þarf Contoso ekki að skipuleggja allar vörur fyrir sama tímabil í framtíðinni. Þekjuhópar fyrir vörurnar eru búnir til. Vörur sem hafa svipaðan líftíma er úthlutað til sama þekjuhóps. Skipulagshorfur fyrir hvern þekjuhóp (það er tímamörk þekju) er um það bil afgreiðslutími plús framlegð einnar viku. Aðalskipulag tryggir síðan að vörurnar séu fyrirhugaðir fyrirfram, byggt á afgreiðslutíma þeirra.

    Þess vegna verða tveir þekjuhópar stofnaðir fyrir þetta dæmi. Einn þekjuhópur mun hafa tveggja vikna tímamörk þekju og hinn mun hafa átta vikna tímamörk þekju.

    Ef **Já, eins og skilgreint er í þessu aðalskipulagi** er valið sem svar, fjöldi daga sem sleginn er inn ætti að vera meiri en lengsti afgreiðslutími allra varanna. Hins vegar, vegna þess að ekki þarf að skipuleggja margar vörur svo langt fyrirfram, verða margar fyrirhugaðar pantanir reiknaðar út en aldrei notaðar. Þess vegna mun keyrslutími aðaláætlanagerðar aukast.

- **Áætlanagerð:**

    - **Spurning:** "Þarftu að skipuleggja starfsemi skipt í einstök störf?"
    - **Svar:** "Já."

    Framleiðsla Contoso verður að skipuleggja og skipuleggja einstök störf sem unnin verða á verslunargólfinu. Þess vegna mun það nota vinnsluröðun.

- **Afkastaveita:**

    - **Spurning:** "Viltu tímaáætlun með því að nota afkastaveitu tilfanganna?"
    - **Svar:** "Já, eins og skilgreint er í þessu aðalskipulagi." **10 dagar** er slegið inn.

    Fjöldi fræsinga og borvéla er takmarkaður. Framleiðsluáætlun verður að taka mið af þessari takmörkun og raða störfum í tíma eftir afkastaveitu tilfanganna. Með öðrum orðum, störfin sem eru áætluð verða enduráætluð miðað við takmarkanir tilfanganna. Skipulagning mun nota afgreiðslutímann til viðbótar tímabilinu sem er skilgreint. (Fyrirhugaðar framleiðslupantanir geta skarast.) Vegna þess að framleiðslutími framleiðsluhlutanna fyrir hlutina er sjö dagar, verður afkastageta fjármagnsins til aðalskipulags í huga á 10 dögum.

- **Röðun:**

    - **Spurning:** "Viltu raða skipulögðum pöntunum með raðagildum vörunnar?"
    - **Svar:** "Já, eins og skilgreint er í þekjuhópunum."

    Aðgerðarleið er skilgreind fyrir framleiðslu hverrar lokavöru. Þess vegna mun aðalskipulag tímasetja pantanir í tíma samkvæmt skilgreindum leiðum.

- **Niðurbrot:**

    - **Spurning:** "Viltu skipuleggja pantanir fyrir alla þætti í uppskrift (áætlun fyrir yfir- og allar undirvörur)?"
    - **Svar:** "Já, eins og skilgreint er í þekjuhópunum."

    Skipuleggja verður allar vörur sem eru notaðir við framleiðsluna. Vegna þess að vörurnar hafa mjög mismunandi afgreiðslutíma mun aðalskipulagning hafa betri árangur þegar hún notar þekjuhópa. Aftur er hægt að færa inn vikuframlegð og hægt er að gera sprengingu á sama tíma og þekjan er.

### <a name="example-2-contoso-retailer"></a>Dæmi 2: Contoso smásala

Contoso smásala er dreifingarfyrirtæki í tískuiðnaðinum. Það notar aðalskipulagningu til að reikna út hvenær innkaupapantanir eiga að vera settar út frá spá þess sem velta hefur. Hér eru nokkur einkenni þess:

- Smásali Contoso notar eftirspurnarspá til að spá fyrir um sölu. Innkaupapantanir verða skipulagðar samkvæmt spánni.
- Verslanir nota beiðnir um áfyllingu.
- Afgreiðslutími frá aðalvörugeymslu í hverja verslun er um það bil tvær vikur fyrir allar vörur.

Í leiðsagnarforritinu eru eftirfarandi gildi færð fyrir Contoso smásala:

- **Spáreftirspurn:**

    - **Spurning:** "Viltu nota spááætlun í aðalskipulagningu svo að fyrirhugaðar pantanir verði lagðar til að uppfylla spáða eftirspurn?"
    - **Svar:** "Já, eins og skilgreint er í þessu aðalskipulagi."

    Contoso hefur látið fylgja eftirspurnarspá til að spá fyrir um sölu þess. Þess vegna verður aðalskipulagning að mæla með fyrirhuguðum pöntunum til að uppfylla spána.

- **Staðfesting:**

    - **Spurning:** "Viltu að aðaláætlun festi áætlaðar pantanir sjálfkrafa í pöntunargögn, til dæmis framleiðslu- eða innkaupapantanir?"
    - **Svar:** "Já, eins og skilgreint er í þessu aðalskipulagi." **1 dagur** er slegið inn.

    Þar sem Contoso smásali mun búa til innkaupapantanir beint úr fyrirhuguðum innkaupapöntunum er það gagnlegt ef fyrirhugaðar innkaupapantanir eru sjálfkrafa styrktar. Vegna þess að fyrirtækið rekur aðaláætlun á hverjum degi munu styrkjandi tímamörk upp á einn dag sjálfkrafa festa allar pantanir sem þarf til næsta dags.

- **Samþykktar beiðnir:**

    - **Spurning:** "Viltu láta fylgja eftirspurn frá viðurkenndum beiðnum um að bæta við verslanir?"
    - **Svar:** "Já, eins og skilgreint er í þessu aðalskipulagi." **1 dagur** er slegið inn.

    Contoso notar samþykktar kröfur frá verslunum sínum til að búa til fyrirhugaðar innkaupapantanir til að bæta við þær verslanir. Þar sem aðalskipulagning er rekin á hverjum degi, verða beiðnir frá síðasta degi með í skipulagningu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]