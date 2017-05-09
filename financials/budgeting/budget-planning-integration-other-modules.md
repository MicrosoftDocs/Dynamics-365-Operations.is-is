---
title: "Samþættingu fjárhagsáætlunargerðar við aðrar kerfiseiningar"
description: 
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: d64f9228c538a08a2fc938bc6ff4ce11278b6fed
ms.openlocfilehash: 4b516e3460f58ef1c7f4a76357371eefde1bae49
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-integration-with-other-modules"></a>Samþættingu fjárhagsáætlunargerðar við aðrar kerfiseiningar

[!include[banner](../includes/banner.md)]




<a name="periodic-processes-for-generating-budget-plans"></a>Reglubundnar vinnslur til að mynda fjárhagsáætlanir
----------------------------------------------

Hægt er að mynda fjárhagsáætlanir úr eftirfarandi tilföngum:

-   Fjárhagsfærslur
-   Eignir
-   Spástöður
-   Áætlanir verka
-   Birgðaspár
-   Eftirspurnarspár
-   Færslur í fjárhagsáætlunarskrá
-   Aðrar fjárhagsáætlanir

Grunneiningar reglubundins ferlis eru þau sömu fyrir öll ferli. Flipar leyfa skilgreiningu á uppruna gagna, markeiginda (fjárhagsáætlunargerð) og valkosti til að keyra ferlið í bakgrunni sem runuvinnslu. Síðari hlutunum þessa þekkingarskráar lýsa vörur sem gætu verið óljósar í hverri vinnslu.

### <a name="actions"></a>Aðgerðir

Fyrir hvert myndunarferli eru þrjár aðgerðir í boði:

-   **Búa til nýja fjárhagsáætlun** – Stofna nýja áætlun hefur eigindir sem eru valdar í **Mark **hluta. Þessar eigindir þurfa ekki að vera einkvæmar. Þess vegna geta tvær áætlanir haft sama heiti og önnur gildi.
-   **Skipta út fyrirliggjandi aðstæðum fjárhagsáætlunargerðar** eyðir öllum gögnum í fjárhagsáætlun marks í völdum aðstæðum fjárhagsáætlunargerðar og stofnar nýjar línur sem nota gögn valinnar upprunastöðu.
-   **Uppfæra fyrirliggjandi aðstæður fjárhagsáætlunargerðar og bæta nýjum gögnum við** uppfærir fyrirliggjandi línur í markáætlun sem samsvarar upprunalínum og bætir við nýjum línum fyrir ný gögn. Samsvörunin er byggð á fjárhagslykli, dagsetningu, fjárhagsáætlunarklasa og ýmsum öðrum reitum. Til dæmis þegar fjárhagsáætlanir eru myndaðar úr spástöðum er staðsetningarnúmer mikilvægur reitur. Allar línur sem hafa staðsetningarnúmer sem samsvarar stöðu uppruna er skipt út fyrir nýjar línur úr frumkóða.

### <a name="source"></a>Uppruni

Fyrir öll ferli sem **Uppruna** flipanum gerir kleift að sía gögn við **Síu** hnappinn. Að sjálfgefnu tiltekin svæði er bætt við síu fyrir hverju ferli. Til dæmis, fyrir í **Mynda fjárhagsáætlun úr fjárhag** ferlið í **fjárhagslykil** og **aðallykils** tegundir eru tiltækar og birtast á síðu myndun. Öllum reitum sem er bætt við síuna er einnig bætt við síðuna, ásamt öllum skilyrðum sem er bætt við.

### <a name="target"></a>Mark

Valkosturinn **Sögulegt** valkostinn á flipanum **Mark** gerir það mögulegt að nota dagsetningar úr upprunagögnum sem gildisdagsetningu í fjárhagsáætlun. Yfirleitt verður gildisdagsetningin að vera innan fjárhagsáætlunarferlis áætlunarinnar. Þegar valkosturinn **Sögulegt** er stilltur á **Já** er dagsetning (jafnvel árið) uppruna notuð, þannig að hægt er að nota fyrri gögn sem grunnur fyrir samanburð. Ekki er hægt að breyta sögulegum gögn í fjárhagsáætlunargerð og áætlun er stillt á stöðuna samþykkt í verkflæði. Hins vegar er hægt að endurstilla stöðu ef aðrar aðstæður í áætluninni krefjast breytinga.

Reiturinn **Steypa saman samtölu eftir** efst á síðunni ákvarðar einnig dagsetninguna sem er notuð. Þessi reitur leggur saman upphæðir og stillir einnig gildisdagsetningu á fyrsta dag fjárhagsársins eða fjárhagstímabili. 

Margir reitir á flipanum **Mark** verða breytanlegir eða aðeins til lestrar, eftir hvaða aðgerð er valin á flipanum. Þegar er breytt úr stofnun nýrrar fjárhagsáætlunar í uppfærslu fyrirliggjandi áætlunar verður reiturinn **Heiti fjárhagsáætlunar** óvirkur og reitir sem eru tengdir vali á fyrirliggjandi áætlun verða tiltækir. Bæði á flipanum **Mark** og **flipanum **Uppruni , er reiturinn **Fjárhagur** alltaf óvirkur, þar sem gildið er ákvarðað af valið ferli fjárhagsáætlunargerðar. 

Reiturinn **Fjárhagsáætlunarklasi** gerir kleift að stilla línur fjárhagsáætlunar sem annaðhvort kostnaðarfærslur eða tekjufærslur. Yfirleitt eru tekjufærslur kreditfærslur í fjárhagslykil og eru þar af leiðandi geymd sem neikvæðar upphæðir. Yfirleitt birtast þessar færslur einnig sem neikvæðar upphæðir í fjárhagsáætlun. Hins vegar, með því að bæta við fjárhagsáætlunarklasanum sem reit í útliti áætlunar, er hægt að virkja tekjur birtist sem upphæðir í jákvætt.

### <a name="generation-rules"></a>Myndunarreglur

Þrjú svæði veita viðbótaraðgerðir: **Stuðull**, **Lágmarks**, og **Sléttun** **reglu**. 

Gildið í reitnum **Stuðull** er margfaldað með upprunaupphæð til að stilla upphæð í fjárhagsáætlun. Síðan er hægt að gera leiðréttingar þegar línur fjárhagsáætlunar eru stofnaðar. Til dæmis er hægt að færa inn **1,03** fyrir 3 prósent hækkun. Stuðullinn verður að vera jákvæð tala. 

Reiturinn **Lágmark** gerir kleift að stilla þröskuldsupphæð til að stofna línu fjárhagsáætlunar. Ef upprunaupphæðin er lægri en þessi tala er fjárhagsáætlunarlína ekki stofnuð. Virði upp á **0,00** leyfir allar upphæðir en takmarkar ekki línur við jákvæðar upphæðir. (Ekkert gildi takmarkar línur við jákvæðar upphæðir. Neikvæðar upphæðir eru alltaf með og standa yfirleitt fyrir kreditfærslur.)

Reiturinn **Sléttunarregla** gerir kleift að stilla nákvæmni fjárhagsáætlunarlínanna sem eru stofnaðar. Hægt er að slétta upphæðir í næstu 1,00, 10,00, 100,00 og svo framvegis, í gjaldmiðli.

## <a name="notes-for-specific-processes"></a>Athugasemdir fyrir tilteknar vinnslur
### <a name="generate-budget-plan-from-general-ledger"></a>Mynda fjárhagsáætlun úr fjárhag

Þegar stofnaðar eru fjárhagsáætlanir úr fjárhagsgögnum verður að stilla reitinn **Steypa saman samtölu eftir** á **Fjárhagsár** ef valkosturinn **Sögulegt** er stilltur á **Nei**. Tímabil og dagsetningar í uppruna gæti passa ekki við tímabilin í dagsetningar í marki. Þar sem ferlið hefur engar áreiðanlega leið til að varpa þessi gildi, verður að takmarka það ferli að fyrsta ársins. 

Í markinu er reiturinn **Fjárhagsáætlunarklasi** stilltur á annaðhvort **Kostnaður** eða **Tekjur**. Þessi stilling er notuð til að velja eigindina **Fjárhagsáætlunargerð** fyrir línur sem eru stofnaðar þegar aðallykillinn í línu er ekki með í **Tekjur** eða **Kostnaðarskýrslu** gerð.

### <a name="generate-budget-plan-from-fixed-assets"></a>Mynda fjárhagsáætlun úr eignum

Ferlið **Mynda fjárhagsáætlun úr eignum** hefur engan valkost fyrir söfnun eftir degi eða tímabili. Einnig er enginn valkostur til að stilla áætlunina sem sögulega. Hægt er að nota reglubundna ferlið með áætlaðar færslur fyrir eignir í þínu fjárhagsáætlunargerðar.

### <a name="generate-budget-plan-from-forecast-positions"></a>Mynda fjárhagsáætlun úr spástöðum

Ferlið **Mynda fjárhagsáætlun úr spástöðum** úthlutar spástöðu uppruna á línu fjárhagsáætlunar. Hægt er að skoða stöðuna með því að bæta spástöðu við sem línu í fjárhagsáætlunarútlit eða nota fyrirspurnina **Fjárhagsáætlunarlínur**. Ef þú vilt ekki að spárstöðunni sé úthlutað á fjárhagsáætlunarlínu, skal stilla valkostinn **Hafa stöðu í línu fjárhagsáætlunargerðar** á **Nei**.

Línur í fjárhagsáætlunargerð eru lagðar saman eftir fjárhagslykli og stöðu. Hins vegar er hægt að útiloka staðsetningarnúmer, svo sem línur eru lagðar saman eftir fjárhagslyklum eingöngu. Á flipanum **Mark** skal stilla valkostinn **Hafa stöðu í línu fjárhagsáætlunargerðar** á **Nei**.

Í reitnum **FTE-aðstæður fjárhagsáætlunar** er hægt að velja aðstæður sem fela í sér fjölda fullt ígildi þess (starfsmanna í fullu starfi) í fjárhagsáætlun. Þessi reitur takmarkast við áætlanir af gerðinni magn sem eru innifaldar í útliti markfjárhagsáætlunar. Ef FTE-aðstæður eru valdar verður einnig að tilgreina aðallykil FTE. Þessi lykill er notaður til að stofna fjárhagsáætlunarlínur fyrir magn. 

Ferli og aðstæður fjárhagsáætlunargerðar sem eru valdar í uppruna ákvarða ferli og aðstæður fjárhagsáætlunargerðar markaðstæðna. Þar sem eigindunum er úthlutað á spástöður verða þau að vera samstillt við fjárhagsáætlunina. Þess vegna er ekki hægt að breyta þessum eigindum á markinu.

### <a name="generate-budget-plan-from-project-forecasts"></a>Mynda fjárhagsáætlun úr verkspám

Ferlið **Mynda fjárhagsáætlun úr verkspá**, eins og ferlið **Mynda fjárhagsáætlun úr spástöðum**, hefur valkost til að hafa með magn verks (tími, útgjöld og vörur) í magni aðstæðna. Tvö ferli hafa einnig svipaðar síur fyrir dálka í fjárhagsáætlunarútlit. 

Á flipanum **Uppruna** ákvarða þrír valkostir í hlutanum **Taka yfirlit með** hvaða línur fjárhagsáætlunar eru stofnaðar. Þessir valkostir eru þeir sömu og þeir valkostir sem eru tiltækir þegar færslur fjárhagsáætlunarskrár er stofnuð beint úr verkspá. Stilltu valkostinn **Hagnaður og tap** á **Já** til að stofna línur fyrir kostnað og tekjur. Setja skal **VÍV** valkosturinn að **Já** til að stofna vinnu í vinnslu á færslum. Stilltu valkostinn **Launaúthlutun** á **Já** til að stofna línur fyrir kostnað og tímafærslur. 

Það er enginn reitur **fjárhagsáætlunarklasa** þar sem fjárhagsáætlunarklasinn (**Kostnaður** eða **Tekjur**) er ákvarðaður eftir uppruna. 

Hægt er að nota fjárhagsáætlanir verks sem uppruna með því að velja spárlíkanið sem inniheldur upphæðir verkáætlunar. Munið að fjárhagsáætlanir stofna spárfærslur verks um leið og þær eru samþykktar.

Til að velja aðeins kostnað eða tekjur fyrir línur fjárhagsáætlunar skal nota síuna til að velja **Áætlunaruppfærslur: gerð upphæðar = Kostnaður**. Til að velja aðeins eina gerð spár skal nota síuna til að velja **Áætlunaruppfærslur: Færslugerð = *xxx***. 

Hægt er að nota aðeins eitt áætlunarlíkan til að mynda aðstæður fjárhagsáætlunargerðar. Ef keyrt er ferli fyrir eitt spálíkan og síðan gerð uppfærsla og reynt að tilgreina annað líkan, verður skrifað yfir fyrsta líkanið ef verið er að nota sama verk og fjárhagslykla. Til að mynda aðstæður fjárhagsáætlunar úr fleiri en einu spálíkani, mynda í mismunandi aðstæður fjárhagsáætlunargerðar og valkosti fyrir úthlutun er notuð til að bæta við þær saman í öðrum aðstæðum. 

Ferlið **Mynda fjárhagsáætlun úr spástöðum** úthlutar einnig upprunaverkefni á línu fjárhagsáætlunar.

### <a name="generate-budget-plan-from-supply-forecast"></a>Mynda fjárhagsáætlun úr birgðaspá

Upprunasíuvalkostirnir í ferlinu **Mynda fjárhagsáætlun úr birgðaspá** voru mótaðir eftir valkostunum í eftir aðgerðinni **Flytja innkaupaáætlun í fjárhag** vegna líkingar milli ferlis og aðgerðinni.

### <a name="generate-budget-plan-from-demand-forecast"></a>Mynda fjárhagsáætlun úr eftirspurnarspám

Fyrir ferlið **Mynda fjárhagsáætlun úr eftirspurnarspá** er hægt að stilla valkostinn **Sölupöntun** á **Já** til að mynda tekjulínur í fjárhagsáætlunargerð, stilla **Notkun** á **Já** til að stofna kostnaðarlínur eða stilla báða valkosti á **Já**.

### <a name="generate-budget-plan-from-budget-register-entries"></a>Mynda fjárhagsáætlun úr færslum fjárhagsáætlunarskráar

Fyrir ferlið **Mynda fjárhagsáætlun úr færslum áætlunarskráar** verður uppruninn að tilgreina eitt undirlíkan, einn fjárhagsáætlunarkóða og eitt færslunúmer. Með öðrum orðum er hægt að stofna línur fjárhagsáætlunargerðar fyrir eina færslu fjárhagsáætlunarskrár í einu. Hægt er að nota fleiri færslur í sama fjárhagsáætlunargerð með því að keyra einu sinni fyrir hverja færslu uppruna ferlið.

### <a name="generate-budget-plan-from-budget-plan"></a>Mynda fjárhagsáætlun úr fjárhagsáætlun

Fyrir ferlið **Mynda fjárhagsáætlun úr fjárhagsáætlun** gerir aukasafn valkosta á flipanum **Mark** það mögulegt að tengja nýjar fjárhagsvíddir. Ef fjárhagsvídd er valin verður það gildi notað fyrir allar línur fjárhagsáætlunar. Þess vegna er hægt að nota eina fjárhagsáætlun sem grunn fyrir aðrar fjárhagsáætlanir, en einnig má úthluta, til dæmis, mismunandi deild eða kostnaðarstað á nýjar fjárhagsáætlanir.

## <a name="looking-back-from-the-budget-plan"></a>Flett aftur úr fjárhagsáætlunargerð
### <a name="budget-plans-by-dimension-set-inquiry"></a>Fjárhagsáætlanir eftir fyrirspurn víddasamstæðu

Fyrirspurnin **Fjárhagsáætlanir eftir víddasamstæðum** inniheldur nokkra valkosti sem gera kleift að keyra fyrirspurn til að finna gögn fjárhagsáætlunar. 

Veldu línu og smelltu á hnappinn **Fjárhagsáætlunarlínur** til að keyra fyrirspurnina **Fjárhagsáætlunarlínur**. Niðurstöðurnar eru síaðar fyrir víddargildi völdu línunnar. Síðan er hægt að nota viðbótarfæribreytur. 

Nota skal hnappana **Birgðaspá** og **Eftirspurnarspá** til að keyra þessar fyrirspurnir. Í báðum tilvikum leitar fyrirspurnin að spálínum sem gætu hafa stofnað línur fjárhagsáætlunar. 

Viðbótarskýrslur sem eru tiltækar innihalda skýrsluna **Spástöður eftir fjárhagsáætlun**. Þessi skýrsla er sérlega gagnleg þegar á að ákvarða hvort stöðu hafi verið rétt úthlutað á fjárhagsáætlanir.




