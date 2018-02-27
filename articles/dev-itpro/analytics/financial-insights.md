---
title: "Fjármálainnsýn"
description: "Fjármálainnsýn notar Microsoft Power BI til að koma saman fjárhagslegum afkastavísum (KPI), gröfum og fjárhagsskýrslum."
author: kweekley
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106233
ms.assetid: 517e6a88-e7a1-4398-9971-b22fa83306ba
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 8075abccdcdde21df967dcc9948a738895f35cef
ms.openlocfilehash: 3da5344ec6edec0af28aa21d45af962307231e67
ms.contentlocale: is-is
ms.lasthandoff: 01/25/2018

---

# <a name="financial-insights"></a>Fjármálainnsýn

[!include[banner](../includes/banner.md)]

**Fjármálainnsýn** notar Microsoft Power BI til að koma saman fjárhagslegum afkastavísum (KPI), gröfum og fjárhagsskýrslum. Power BI er fellt inn í Microsoft Dynamics 365 Finance and Operations, Enterprise Edition.
**Fjármálainnsýn** leggur áherslu á greiningarskýrslu. Persónur þvert yfir fyrirtæki geta skoðað, rannsakað, skilið og aðhafst. 

**Fjármálainnsýn** sameinar gögn frá fjárhag og undirbók til að fá betri heildarmynd af fjárhagslegri heilsu fyrirtækis.

> [!NOTE] 
> Þetta skjal notar eftirfarandi Power BI hugtök:                                                                           
**Skýrsla** - Einföld .pbix skrá sem öll myndefni á öllum flipum eru vistaðar á.                                                          
**Síða** - Flipi í einni .pbix skrá. Hver síða getur innihaldið eitt eða fleiri myndefni.                                                     
**Myndefni** - Stök uppspretta af gögnum, svo sem kort, KPI, graf, fylki eða fjárhagsskýrslu. Síðan sem hefur fjárhagsskýrslu sem myndefni getur ekki haft önnur myndefni vegna stærðar þeirra gagna sem er verið að birta.


Eins og er, er **Fjármálainnsýn** notað til að skoða gögn fyrir annaðhvort virka lögaðila eða alla lögaðila. Í framtíðarútgáfum mun vinnusvæðið þróast í svæði þar sem þú getur notað Power BI til að breyta og búa til myndefni.

Vinnusvæði **CFO-yfirlits** sýnir sömu myndefni og **Fjármálainnsýn**, en leggur áherslu á að leyfa þér að skoða og sía gögnin á núverandi skýrslum. Í framtíðarútgáfum muntu geta bætt við nýju myndefni við vinnusvæði **Fjármálainnsýnar**. Nýja myndefnið gæti einnig verið tiltækt á vinnusvæðum sem leggja áherslu á önnur hlutverk, svo sem verkefnastjóra eða stjóra viðskiptaskulda. Vinnusvæði **CFO-yfirlits** heldur áfram að sýna gögn fyrir alla lögaðila, óháð lögaðilunum sem hlutverkið hefur aðgang að.

## <a name="finance-and-operations-setup"></a>Uppsetning Finance and Operations
**Fjárhagur**

Aðallykilgerðin og aðallyklaflokkar eru notaðir til að fylla í viðeigandi sjálfgefna aðallykla á fjárhagsskýrslu **efnahagsreikningsins** og ýmissa fjárhagsskýrsla **rekstrarreikninga** í **Fjármálainnsýn**.

Á síðu **aðallykils** verður þú að skilgreina aðallykilinn þinn svo að ein af eftirfarandi gerðum verði úthlutað til þín:

• Tekjur

• Kostnaður

• Eignir

• Skuldir

• Eigið fé

Ekki úthluta aðallyklinum þínum annarri aðallyklagerð, svo sem **Efnahagsreikning** eða **Hagnaður og tap**. Skráning getur ekki ákvarðað gerð aðallykils þegar aðrar aðallyklagerðir eru úthlutaðar vegna þess að þær eru ekki nógu kornóttar. Tegund aðallykils verður að vera ákveðin til að sýna skuldir og tekjur sem jákvæðar upphæðir á fjárhagsskýrslum.

Til að koma fram á fjárhagsskýrslu og vera með í ýmsum öðrum myndefnum, svo sem KPI, verður að úthluta hverjum aðallykli aðallyklategund. Helstu tegundir aðallykla hafa verið endurbættir þannig að þær innihaldi birtingarfyrirmæli. Skjámyndaröðin er notuð sérstaklega á fjárhagsskýrslum í **Fjármálainnsýn**. Eftir að þú hefur breytt eða bætt við nýrri tegund aðallykils getur þú breytt gildi **skjámyndaraðarinnar** til að skilgreina röðina sem tegundir aðallykla ættu að birtast á fjárhagsskýrslu. Ef þú verður að breyta skjámyndaröðinni fyrir margar tegundir aðallykl, geturðu notað Open í Excel til að breyta fljótt og birta breytingarnar aftur í Finance and Operations.


## <a name="entity-store"></a>Einingaverslun
Gögnin fyrir **Fjármálainnsýn** eru tekin úr einingaversluninni (**Kerfisstjórnun** > **Uppsetning** > **Einingaverslun**). Ef þú opnar **CFO-yfirlitið** eða vinnusvæði **Fjármálainnsýnar** og eftirfarandi viðvörunarboð birtast í myndefnunum, verður þú að uppfæra einingarnar.
 
![Viðvörun](./media/Cantdisplay.png)

Þú verður að uppfæra eftirfarandi einingar til að sjá gögn í **Fjármálainnsýn** og vinnsvæði **CFO-yfirlits**:

• CustCollectionsBIMeasurements

• FinancialReportingOtherData

• FinancialReportingReferenceData

• FinancialReportingTransactionData

• LedgerCovLiquidityMeasurement

• Innkaupateningur

• Söluteningur

Í fyrri útgáfunni voru LedgerActivityMeasure og VendPaymentBIMeasure einingarnar notaðar fyrir gögn á vinnusvæði **CFO-yfirlitinu**. Hins vegar eru þær ekki lengur notaðar í núgildandi útgáfu.

Þú getur skilgreint endurtekna runu til að uppfæra reglulega gögnin í einingunum. Þar sem hver eining er endurreist frá grunni á meðan á uppfærslu stendur skal velja tíma og tíðni uppfærslna á einingum vandlega. Aðaleiningin sem er notuð í fjárhagsskýrslum er FinancialReportingTransactionData einingin. Því gætir þú ákveðið að uppfæra þessa einingu oftar.

## <a name="security"></a>Öryggi
Eins og er þá er ekki hægt að takmarka innfelldu gögnin í Power BI skýrslum við lögaðila sem notandinn hefur aðgang að. Þess vegna eru innfelldu Power BI skýrslurnar stýrðar með skyldum í öryggisuppsetningunni. Skyldurnar sem eru skilgreindar leyfa aðgang að gögnum fyrir annaðhvort alla lögaðila eða aðeins virka fyrirtækið. Eftirfarandi tafla sýnir skyldur sem eru til staðar og hlutverkunum sem þeim er úthlutað. Skyldur geta verið fjarlægðar eða þeim úthlutað mismunandi hlutverkum, byggt á kröfum fyrirtækisins.

| **Gjald**                     | **Hlutverk**                                       | Lýsing                     |
|------------------------------|-------------------------------------------------|-----------------|
| Skoða vinnusvæði CFO-yfirlits  | Fjármálastjóri                         | • Þessi skylda veitir aðgang að vinnusvæði CFO-yfirlits. • Að sjálfgefnu er virka fyrirtækið notað sem sía. Þú getur þó bætt við öllum lögaðilum, óháð því hvort notandinn hefur aðgang að hinum lögaðilunum.               |
| Skoða fjármálainnsýn í núgildandi fyrirtæki | • Endurskoðandi • Aðalbókari • Bókhaldsstjóri • Endurskoðandi • Umsjónarmaður fjárhagsáætlunar • Forstjóri • Fjármálastjóri • Eftirlitsmaður fjármála  |   • Þessi skylda veitir aðgang að Fjármálainnsýn. • Að sjálfgefnu er virka fyrirtækið notað sem sía. Þú getur ekki bætt við öðrum lögaðilum.            |
| Skoða fjármálainnsýn þvert á fyrirtæki   | • Í Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3, er þessari skyldu ekki falið hlutverki. • Í næstu útgáfu verður þessari skyldu úthlutað hlutverki fjármálastjóra. | • Þessi skylda veitir aðgang að valmyndaratriði fyrir vinnusvæði CFO-yfirlits. •    Að sjálfgefnu er virka fyrirtækið notað sem sía. Þú getur þó bætt við öllum lögaðilum, óháð því hvort notandinn hefur aðgang að hinum lögaðilunum.             |


## <a name="how-financial-statements-work"></a>Hvernig fjárhagsskýrslur virka
Þótt **Fjármálainnsýn** innihaldi fjárhagsskýrslur kemur það ekki í staðinn fyrir fjárhagsskýrslugerð í Finance and Operations. Sjálfgefna fjárhagsskýrslurnar í **Fjármálainnsýn** eru takmarkaðar í umfangi og innihalda ekki allar gerðir fjárhagsskýrslna. Fjárhagsskýrslugerð er enn aðalverkfærið til að hanna, búa til og stofna lögbundnar fjárhagsskýrslur.

Til viðbótar við myndefnin frá upphaflega vinnusvæði **CFO-yfirlitsins**, ný KPI, gröf og fjárhagsskýrslur eru nú í boði. Eftirfarandi fjárhagsskýrslur eru í boði:

• Prófjöfnuður

• Efnahagsreikningur

• Rekstrarreikningur eftir svæðum

• Rekstrarreikningur raunverulegur í samanburði við áætlaðan

• Rekstrarreikningur með frávikum

• 12 mánaða þróun rekstrarreiknings

• Kostnaður þriggja ára þróun

• Útgjöld lánardrottins

• Sala viðskiptavina

## <a name="edit-visuals"></a>Breyta myndrænum þáttum
Í upphaflegri útgáfu á **Fjármálainnsýn** er ekki hægt að breyta myndrænum þáttum. Í næstu útgáfum munu notendur sem hafa viðeigandi öryggi geta búið til nýtt myndefni, afritað núverandi myndefni og breytt myndefni. Þó að .pbix skrár sem innihalda skýrslurnar séu tiltækar sem tilföng mælum við með því að þú breytir ekki sjálfgegnum skýrslum. Viðbótarupplýsingar um breytingar verða gerðar á gagnalíkaninu, sjálfgefnum skýrslum og sérsniðnum fjárhagsskýrslum sem eru notaðar til að búa til fjárhagsskýrslur. Til þess að nýta nýjar aðgerðir og breytingar á gagnalíkaninu í næstu útgáfu verður þú að endurtaka allar breytingar sem þú gerðir á sjálfgefnum skýrslum með Microsoft Power BI Desktop.


## <a name="filtering"></a>Afmörkun
Notendur geta afmarkað skýrsluna með því að nota **Síu** gluggann til vinstri. Þessi gluggi er sami glugginn og er í boði í gegnum Power BI Desktop.
Það eru mismunandi stig afmörkunar, sum þeirra eru kannski ekki í boði, fer allt eftir því sem þú hefur valið á síðu (flipa) eða hvort þú notar borunarmöguleika:

• **Síur á skýrslustigi** - Þessar síur eru notaðar á allt myndefnið á öllum síðum (flipum).

• **Síur á síðustigi** - Þessar síur eru notaðar á allar myndir á virka flipanum. Þessar síur eru notaðar ofan á síurnar á skýrslustiginu.

• **Síur á myndrænu stigi** - Þessar síur eru aðeins notaðar á valið myndefni. Þessar síur eru notaðar ofan á síur á síðustigi.

• **Borunarsía** - Þessi sía afmarkar "uppsprettu" myndefnis sem er beitt á núgildandi myndefni þegar þú kafar frá uppsprettu myndefnisins til núverandi myndefnis.

![Sía](./media/filter.png)


Til að fjarlægja tiltekið síugildi velurðu strokleðurtáknið við hliðina á því. Ekki fjarlægja síu með því að velja X. Ef þú velur X verður svæðið sem þú ert að sía á fjarlægt sem síuvalkostur. Ef þú fjarlægir óvart svæði frá síunni skaltu loka vinnusvæðinu og opna það síðan aftur. Sjálfgefnar stillingar síu verða aftur settar á.

Að sjálfgegnu, þegar þú opnar vinnusvæði fyrst, er virkur lögaðili notaður sem sía á skýrslustigi. Það fer eftir öryggi þeirra, þar sem notendur kunna að geta bætt við öðrum lögaðilum eða breyta sjálfgefnum lögaðila sem er valinn í síunni.

Sía **Fjárhagsdagatals** er nauðsynleg svo rétt dagatal sé notað fyrir myndefni. Að sjálfgefnu er sía á skýrslustigi stillt á fjárhagsdagatal virka lögaðilans. Ef þú breytir síunni í fjárhagsdagatal sem hefur aðra upphafs- eða lokadagsetningu verður upphafsstaða ekki innifalinn. Þess vegna mun fjárhagsskýrsla **Efnahagsreikningsins** þíns ekki sýna rétta stöðu. Ef þú velur auka fjárhagsdagatal í síunni verður þú með viðbótar sett af dálkum. Hvert viðbótar sett af dálkum sýnir upphæðina fyrir mismunandi fjárhagsdagatal.

Sía **Bókunarlags** er einnig nauðsynleg. Að sjálfgefnu er sían stillt á Núgildandi. Þú getur valið fleiri bókunarlög í síunni til að sýna samanlagða upphæð.

Síur eru einnig í boði fyrir svið **Dagsetningu** og **Fjárhagsdagatals**. Venjulega eru þessar síur sóttar á síðustigi. Að sjálfgefnu notar sía **Dagsetningar** til að nota tengsladagsetningu sem þú getur breytt. Þú getur einnig fjarlægt síu tengsladagsetningar og notað síu **Fjárhagsdagatals** í staðinn.

## <a name="currency"></a>Gjaldmiðill

Allt myndefni sem greinir frá fjárhagsgögnum sýnir upphæðir í bókhaldsgjaldmiðlinum. Þannig að þegar þú síar lögaðilann verður þú að gæta þess að taka aðeins til lögaðila sem hafa sama bókhaldsgjaldmiðil. Annars safnarðu gögnum í mismunandi gjaldmiðlum.

Allt myndefni sem greinir frá gögnum undirbókar svo sem myndefni **Sjóðstreymisspár** og **Topp 10**, sýna upphæðir í gjaldmiðli kerfisins. Gjaldmiðill kerfisins og gerð gengis í kerfinu er skilgreint á síðu **Kerfisfæribreytu**.

Myndefni fyrir **Stöðu eftir bankareikningi** notar upphæð í gjaldmiðli bankareikninga.

## <a name="dimensions"></a>Víddir

Sjálfgefnar fjárhagsskýrslur fela ekki í sér fjárhagsvíddir heldur er áherslan lögð á aðallykilinn. Stuðningur við fjárhagsvíddir verður í boði í næstu útgáfum, þegar hægt verður að breyta skýrslunum. Fyrirtæki munu þá geta síað fjárhagsvíddargildi.

Sumar fjárhagsskýrslur fela í sér víddir sem eru byggðar á færslum undirbókar. Markmið nýju fjárhagsskýrslanna er að gera kleift að sía víddir sem ekki eru settar upp sem fjárhagsvíddir. Til dæmis getur sjálfgefinn kostnaður samkvæmt skýrslu lánardrottins gert þér kleift að víkka út umfram aðallykilinn þannig að þú getir séð sundurliðaða stöðu lánardrottna. Lánardrottinn er ekki settur upp sem fjárhagsvídd. Í staðinn fer kerfið aftur til upprunalegu færslu undirbókarinnar til að finna lánardrottin.

Eftirfarandi víddir eru notaðar á sjálfgefnum skýrslum. Ekkert af þessum víddum er fjárhagsvíddir.

• Lánardrottinn

• Lánardrottnaflokkar

• Viðskiptavinur

• Flokkur viðskiptavina

• Land/svæði

• Ríki/héraði

• Borg

> [!IMPORTANT] 
> Ef þú tekur saman færslur fyrir marga lánardrottna eða viðskiptavini í einu fylgiskjali með því að nota fjárhagsfærslubækur, verða gögnin ekki rétt. Skráning getur ekki ákvarðað hvaða lánardrottinn eða viðskiptavinur tengist tilteknum fjárhagslykli í bókarfærslu vegna þess að þessum upplýsingum er ekki viðhaldið hvar sem er. Þess vegna mælum við ekki með því að þú sláir inn marga lánardrottna, eignir eða verk í eitt fylgiskjal.

## <a name="drill-on-data"></a>Bora í gögn

Mismunandi boranir eru í boði í gegnum Power BI. Hvert stig hefur annað heiti og mismunandi virkni. Þú getur líka bora í línur og dálkur. Í þessum kafla er fjallað um mismunandi valkosti með því að nota fjárhagsskýrslu **Prófjafnaðar** sem dæmi og sýna hvernig hægt er að bora í línurnar. Sama virkni er til fyrir dálka. Þú verður bara að breyta **Kafa í** stillingunni.

Í eftirfarandi myndum er yfirlýsing **Prófjafnaðar** dregin saman í hæsta stigveldi línunnar, aðalyklagerðina.

![Prófjöfnuður](./media/trial-balance.png)

 
Til að skoða næsta stig stigveldisins, tegundir aðallykla, getur þú stillt **Kafa í** reitinn sem **Línur** og valið síðan **Stækka** hnappinn (þriðji hnappurinn eftir Kafa í reitinn). Þú sérð nú allar helstu tegundir aðallykla stækkaðar. Eins og er leyfir Power BI þér ekki að stækka aðeins eina línu eða dálk en sjá samt allar aðrar línur eða dálka.
 
![Prófjöfnuður](./media/trial-balance2.png)
 
  
Til að víkka út til aðallykla allra línanna geturðu aftur notað **Stækka** hnappinn. Hins vegar, til að bora niður í aðallyklana fyrir aðeins eina línu skaltu fyrst velja **Bora í** hnappinn (staka örin sem bendir niður hægra megin í glugganum) og veldu síðan línuna til að bora niður í. Eftirfarandi mynd sýnir niðurstöðurnar þegar línan **Sölur** er valin eftir að **Bora niður** hnappurinn hefur verið valinn.

![Prófjöfnuður](./media/trial-balance3.png)

Eftir að þú hefur borað niður í einni línu þarf að smella oft til að fara aftur í fullan prófjöfnuð. **Kafa upp** hnappurinn (fyrsti hnappurinn eftir **Kafa** í svæði) kafar aðeins upp í samhengi við **Sölu** flokkinn, eins og sýnt er á eftirfarandi mynd.
 
![Prófjöfnuður](./media/trial-balance4.png)
 
 
Þú getur haldið áfram að nota **Kafa upp** hnappinn til að fara aftur á hæsta stigi samantektar í línum.

Power BI hefur einnig hnapp sem leyfir þér að fara á næsta stig í stigveldinu (seinni hnappurinn eftir **Kafa niður** reitinn). Áhrif þessa hnapps eru frábrugðin áhrifum **Stækka** hnappsins (þriðja hnappurinn eftir **Kafa í** reitinn), sem er notaður til að stækka stigveldið. Þegar þú dregur út stigveldið er stigveldinu viðhaldið í skýrslunni. Til dæmis, eins og sýnt var áður, ef dregur út aðallyklagerðina, sérðu enn helstu aðallyklagerðir í skýrslunni. Hins vegar, þegar þú ferð á næsta stig í stigveldinu, sýnir skýrslan ekki lengur yfireininguna í stigveldinu, eins og sýnt er í eftirfarandi mynd.

![Prófjöfnuður](./media/trial-balance5.png)

 
Til að sjá færsluupplýsingar um samanteknar stöður á bak, getur þú valið sumar fjárhæðir til að bora aftur í Financial and Operations.

Bora-aftur frá fjárhagsskýrslunni sendir þig til skoðun upprunalykils (ASE), ekki til færslur fylgiskjala. ASE sýnir ekki bara bókhaldsfærslur í fjárhagnum. Í staðinn sýnir það upplýsingar um færslur undirbókar. Þess vegna færðu mun nánari upplýsingar um uppruna færslna og getur notað þær til greiningar. Til dæmis geturðu séð hver var lánardrottinn eða viðskiptavinur, hvað viðskiptavinurinn keypti eða lánardrottinn seldi og jafnvel hvað verk var á færslunni.

Eftirfarandi síur úr fjárhagsskýrslunni eru sendar til ASE, þannig að ASE sýnir færslurnar sem eru samanlagt:

Nauðsynlegir reitir fyrir síun:

  - Lögaðili
 
  - Fjárhagsdagatal
 
  - Ár
 
  - Kenni aðallykils

Valfrjáls svæði fyrir síun:

  - Ársfjórðungur

  - Mánuður

  - Tímabil

Ef þú víkkar ekki nógu langt niður í línu, virkar köfunin ekki. Til dæmis, ef þú víkkar aðeins niður til tegundar aðallykils getur þú ekki borað niður í ASE á stöðunni því aðallykillinn er nauðsynlegur reitur til að sía í ASE.

Ef þú víkkar of langt niður í línu eru viðbótar síurnar í fjárhagsskýrslunni ekki sendar til ASE. Þess vegna gætir þú séð mun á tölunum þínum. Til dæmis, ef þú víkkar niður í landið eða svæðið í línum rekstrarreiknings með svæði fjárhagsskýrslu, er landið eða svæðið ekki innifalið sem sía í ASE.

> [!NOTE]
> Þú getur borað lengra niður á línum eða dálkum fjárhagsskýrslna heldur en það sem ASE styður eins og er fyrir síun sía. Þess vegna, í sumum tilfellum, mun summan af ítarlegum færslum í ASE ekki passa við stöðuna sem þú ert að bora eftir. Þessi virkni verður áfram aukin í framtíðinni.

## <a name="hierarchies"></a>Stigveldi

Sjálfgefnar fjárhagsskýrslur nota tvö stigveldi til að bora í og útvíkka gögnin. Eitt stigveldið er fyrir línurnar og hitt stigveldið er fyrir dálkana. Bæði stigveldin eru fyrirfram skilgreind í hönnun fjárhagsskýrslunnar. Í flestum fjárhagsskýrslum er stigveldi línu **Aðallyklagerð** > **Aðallyklategundir** > **Aðallykill**. Hins vegar hafa sumar skýrslur fleiri reiti, svo sem land og svæði. Viðbótarhnútar stigveldisins eru byggðar á gögnum undirbókar fyrir hverja færslu.

Fyrir dálkana er leggur stigveldið áherslu á lögaðilana og fjárhagstímabil. Í flestum fjárhagsskýrslum er stigveldisdálkurinn **Lögaðili** > **Fjárhagsdagatal** > **Fjárhagsár** > **Ársfjórðungur** > **Tímabil**.

Eins og er styðja fjárhagsskýrslurnar ekki stigveldi fyrirtækis, sem gerir þér kleift að safna saman gögnum.

## <a name="data-limitations"></a>Takmarkanir á gögnum
Myndefni fjárhagsskýrslna hefur takmörk á fjölda lína sem hægt er að sýna. Nú er hámarkið stillt á 30.000. Ef þú ert yfir þessum mörkum mun myndefnið sýna viðvörunartákn til að tilkynna þér um þetta ástand.
 
![Takmarkanir á gögnum](./media/data-limit.png)


Ef farið er yfir hámarkið verða samtölurnar sem birtast í fjárhagsskýrslunni rangar, því ekki voru allar línurnar hlaðnir inn í myndefnið.

### <a name="empty-rows"></a>Tómar línur
Power BI veitir ekki möguleika á að fela og sýna tómar línur. Ef lína er ekki með neinum gögnum birtist línan ekki í myndefni.

## <a name="what-is-coming-in-future-releases"></a>Hvað mun koma í næstu útgáfum?
Haldið verður áfram að bæta nýju vinnusvæðin og fjárhagsskýrslurnar sem nota Power BI. Hér eru nokkrir af nýju eiginleikunum sem verið er að skoða fyrir framtíðarútgáfur:

 - Getan til að afrita, breyta, eyða og búa til myndefni, jafnvel fjárhagsskýrslur                                                  
 - Viðbótar sjálfgefnar skýrslur                                                                                                            
    - Stuðningur við viðbótargögn undirbókar                                                                                            
 - Stuðningur við skýrslugjaldmiðil                                                                                                      
 - Bæta við sérsniðnum útreikningum fyrir línur og dálka                                                                                          
 - Getan til að flytja fjárhagsskýrslur yfir í Microsoft Excel                                                                     
   - Halda sniði fjárhagsskýrslu á meðan á flutningi út stendur.                                                                          
   - Greina gögn í Excel með því að búa til breytanlega töflu sem notar upplýsingar myndræna þáttarins.                                              
 - Staðfærður stuðningur                                                                                                                        
 - Getan til að skilgreina skráð stigveldi, svo þú getir skilgreint stigveldi aðallykils eða stigveldi fyrirtækis sem hægt er að nota í fjárhagsskýrslu fyrir hönnun, síun og öryggi.                                                                    
 - Stuðningur við prentun

Nýju eiginleikarnir verða sendar í gegnum vefsíðu vegvísis þar sem vinnan er hafin: https://roadmap.dynamics.com/.

## <a name="additional-resources-for-power-bi"></a>Frekari tilföng fyrir Power BI

Upplýsingarnar í eftirfarandi tilföngum eru ekki nauðsynlegar til að virkja innfelldar skýrslur fyrir vinnusvæði **CFO-yfirlitið** eða **Fjármálainnsýnar** í framleiðsluumhverfi. Þess í stað eru þær gagnlegar fyrir dev box og ef þú vilt fella þína eigin Power BI skráningu inn í Finance and Operations.

https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/

https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/add-analytics-tab-workspaces
