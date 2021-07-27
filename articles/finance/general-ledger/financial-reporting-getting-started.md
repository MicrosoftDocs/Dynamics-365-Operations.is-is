---
title: Yfirlitssíða fjárhagsskýrslugerðar
description: Þetta efnisatriði lýsir hvar á að opna fjárhagslegar skýrslugerð í Microsoft Dynamics 365 Finance og hvernig á að nota getu fjárhagsskýrslugerðar.
author: aprilolson
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf07b12d83221952aefb80ab6a5b651bb4ef3762
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/03/2021
ms.locfileid: "6338158"
---
# <a name="get-started-with-financial-reporting"></a>Hafist handa með Financial Reporting 

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvar á að opna fjárhagslegar skýrslugerð og hvernig á að nota möguleika fjárhagsskýrslugerð. Það inniheldur einnig lýsingu á sjálfgefið fjárhagsskýrslur sem er veitt.

## <a name="accessing-financial-reporting"></a>Aðgangur að fjárhagsskýrslugerð

Hægt er að finna **Fjárhagskýrslugerð** valmyndina á eftirfarandi stöðum:

-   **Fjárhagur** &gt; **Fyrirspurnir og skýrslur**
-   **Fjárhagsgerð** &gt; **Fyrirspurnir og skýrslur** &gt; **grunnáætlanagerð**
-   **Fjárhagsáætlun** &gt; **Fyrirspurnir og skýrslur** &gt; **Fjárhagsáætlunargerð**
-   **Fjárhagsáætlun** &gt; **Fyrirspurnir og skýrslur** &gt; **Fjárhagsáætlunarstýring**
-   Samstæður

Til að stofna og búa til fjárhagsskýrslur fyrir lögaðila, verður að setja upp eftirfarandi upplýsingar fyrir lögaðilann:

-   Fjárhagsdagatal
-   Ledger
-   Bókhaldslykill
-   Gjaldmiðill
-   Bóka færslu á að minnsta kosti einum reikningi
-   MainAccount er skráð í völdum dálki í **Fjárhagur > Uppsetning fjárhags > Uppsetning fjárhagsskýrslugerðar**

## <a name="granting-security-access-to-financial-reporting"></a>Veita öryggisaðgang að Financial Reporting
Fjárhagsleg skýrslugerð aðgerðir eru tiltækar fyrir notendur sem hafa fengið viðeigandi réttindi og skyldur úthlutað gegnum öryggishlutverk þeirra. Eftirfarandi kaflar telja upp þessi réttindi og skyldur, ásamt tengdum hlutverkum.

### <a name="duties"></a>Skyldur

| Merki skyldu                            | Lýsing                                                             | AOT-heiti                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna og framkvæma stjórnunarverk. | FinancialReportsSecurityMaintain |
| Vinna með fjárhagsskýrslur            | Hanna og vinna með fjárhagsskýrslur.                                  | FinancialReportsMaintain         |
| Mynda fjárhagsskýrslur            | Mynda og uppfæra fjárhagsskýrslur.                                 | FinancialReportsGenerate         |
| Yfirfara fjárhagslega frammistöðu          | Yfirfara og greina fjárhagslega frammistöðu.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Heimildir

| Merki réttinda                       | Lýsing                                                             | AOT-heiti                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna og framkvæma stjórnunarverk. | FinancialReportsSecuritySystemMaintain |
| Vinna með fjárhagsskýrslur            | Hanna og vinna með fjárhagsskýrslur.                                  | FinancialReportsMaintainReports  |
| Mynda fjárhagsskýrslur            | Mynda og uppfæra fjárhagsskýrslur.                                 | FinancialReportsGenerateReports  |
| Skoða fjárhagsskýrslur                | Skoða fjárhagsskýrslur.                                                 | FinancialReportsView             |

### <a name="roles"></a>Hlutverk

| Merki réttinda                       | Tollar                                  | Hlutverk                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna | Öryggisstjóri                                                          |
| Vinna með fjárhagsskýrslur            | Vinna með fjárhagsskýrslur            | Aðalbókari, yfirmaður bókhalds, fjármálastjóri, stjórnandi fjárhagsáætlunar |
| Mynda fjárhagsskýrslur            | Mynda fjárhagsskýrslur            | Forstjóri, framkvæmdastjóri, bókhaldari                                                            |
| Skoða fjárhagsskýrslur                | Yfirfara fjárhagslega frammistöðu          | Ekki úthlutað                                                                   |

Eftir að°notanda er bætt við eða hlutverki er breytt, á notandinn að geta opnað fjárhagsskýrslugerð innan nokkrar mínútur. 

> [!NOTE]
> Hlutverkið sysadmin er bætt við öll hlutverk í fjárhagsskýrslugerð.

## <a name="report-deletions-and-expirations"></a>Tilkynna eyðingu og fyrningu
Notendur sem búa til skýrslu geta eytt eigin skýrslum. Notendur með skylduna **Vinna með öryggi fjárhagsskýrslna** geta eytt skýrslum annarra. 

Í útgáfu 10.0.8 var hugtakið lokadagar kynnt. Nýr nauðsynlegur eiginleiki er virkur á síðunni **Allt** á vinnusvæði eiginleikastjórnunar. Eiginleikinn **Varðveislureglur fjárhagsskýrslu** inniheldur eftirfarandi breytingar:
* Þegar skýrslur eru myndaðar er lokadagsetning sjálfkrafa merkt sem 90 dögum frá myndun þeirra.
* Lokadagur allra fyrirliggjandi skýrslna áður en eiginleikinn var settur upp er 90 dagar. Dagsetningin kann að birtast auð í stuttan tíma þar til þjónustan fjárhagsskýrslugerð er í gangi, skýrsla er búin til og þjónustan framkvæmir uppfærsluna á fyrirliggjandi skýrslum með auðan lokadag. 
* Notendur sem **Vinna með öryggi fjárhagsskýrslna** hafa aðgang að þessum eiginleika. Sérhver notandi í skyldunni **Vinna með fjárhagsskýrslu** sem er veitt réttindin **Vinna með gildistíma fjárhagsskýrslu** munu einnig geta breytt gildistíma. Eins og stendur eru tveir valkostir varðandi varðveislu í boði: 
  * Gildistími 90 dagar.
  * Valkostur til að stilla skýrsluna þannig að hún falli aldrei úr gildi.
  
Þegar gildistími, t.d. 90 dagar, er valinn, gildir hann í 90 daga frá deginum í dag. Þetta er öðruvísi en 90 dagarnir frá upprunalegum myndunardegi sem er settur þegar skýrslan var búin til. 
  
Aukavalkostir verða teknir til greina fyrir virknina í framtíðinni. Gildistíminn í 90 daga verður sjálfgefið og notendur með viðeigandi heimildir geta hnekkt sjálfgefna tímanum á listasíðunni **Fjárhagsskýrslur**.    

## <a name="default-reports"></a>Sjálfgefnar skýrslur
Fjárhagsskýrslugerð veitir 22 sjálfgefnar fjárhagsskýrslur. Sérhver skýrsla notar sjálfgefna aðalreikningaflokka. Hægt er að nota þessar skýrslur eins og þær eru eða sem byrjunarreit fyrir fjárhagsskýrslugerð. Auk venjulegra fjárhagsskýrslna svo sem tekjuyfirlits og efnahagsreikninga, innihalda þessar sjálfgefnu skýrslur sem sýna mismunandi gerðir af fjárhagsskýrslum sem hægt er að stofna. 

<!--Each report in the following table links to an Office Mix presentation about the report.-->

| Sjálfgefin skýrsla                                                                                         | Lýsing                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 12 mánaða rúlla tekjuyfirlit í einum dálki – Sjálfgefið | Skoða arðsemisgreiningu fyrirtækis síðustu 12 mánuði í einum dálki.                                                                                                                                                                                                                                      |
| 12 mánaða Leitni Tekjuyfirlits – Sjálfgefið                 | Skoða arðsemisgreiningu°fyrirtækis síðustu 12 mánuði, hvern mánuð fyrir sig. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                             |
| Rauntölur samanb. v. áætlun - Sjálfgefið                                | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla fyrir upprunalega fjárhagsáætlun°og bera saman endurskoðaða fjárhagsáætlun við rauntölur sem hefur frávik.                                                                                                                                                                          |
| Endurskoðun upplýsinga - Sjálfgefið                                  | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir debet og kredit stöður í skýrslugjaldmiðli og innlendum gjaldmiðli með nánari færsluupplýsingar eins og auðkenni, notanda sem síðast breytti gögnum, dagsetning síðustu breytingar og auðkenni færslubókarinnar. |
| Stöðulisti - sjálfgefið                                   | Skoða°upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir opnunar- og lokunarstöður, og debet og kredit stöður fyrir gildandi tímabil og ár með nánari færsluupplýsingar eins og fylgiskjal.                                                                    |
| Efnahagsreikningur - Sjálfgefið                                   | Skoða fjárhagslega stöðu fyrirtækisins fyrir árið.                                                                                                                                                                                                                                                             |
| Efnahagsreikningur og Tekjuyfirlit Hlið við Hlið - Sjálfgefið | Skoða fjárhagslega stöðu fyrirtækisins og arðsemi ársins hlið við hlið.                                                                                                                                                                                                                              |
| Sjóðstreymi - Sjálfgefið                                       | Fá yfirlit yfir lausafé sem er að koma inn og fara út úr fyrirtækinu.                                                                                                                                                                                                                                   |
| Ítarleg JE og TB yfirlit– Sjálfgefið                      | Skoða opna stöðu og verkþáttar upplýsingar fyrir alla lykla.                                                                                                                                                                                                                                                      |
| [Ítarlegur prófjöfnuður - Sjálfgefið](trial-balance-financial-reports.md)| Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa debet- og kreditfærslur og nettó stöðu þessara færslna ásamt færsludagsetningu, fylgiskjali og lýsingu færslubókar.                                                                                                                                  |
| Útgjöld þriggja ára á ársfjórðungslegum grundvelli – Sjálfgefið             | Fá innsýn í kostnað fyrir síðustu 12 ársfjórðungar síðustu þriggja ára.                                                                                                                                                                                                                                   |
| Fjárhagstextar JE og TB yfirlit – Sjálfgefið            | Sjá°yfirlit yfir fjárhagstexta varðandi stöður og verkþætti fyrir eign, skuld, eigið fé eiganda, tekjur, kostnaður, hagnaður eða tap.                                                                                                                                                                           |
| [Rekstrarreikningur – Sjálfgefin](income-statement-financial-report.md)| Skoða arðsemi fyrirtækisins fyrir gildandi tímabil og°ár til dagsetningar.                                                                                                                                                                                                                                   |
| Fjárhagshreyfingalisti - Sjálfgefið                        | Skoða upplýsingar um ítarlega stöðu fyrir alla lykla. Þessi skýrsla sýnir debet og kredit stöður, með nánari færsluupplýsingar eins og færsludagsetningu, færslubókarnúmer, fylgiskjal, bókunargerð og rakningarnúmer.                                                                            |
| Hlutfallstölur – Sjálfgefin                                          | Skoða greiðsluþol,arðsemi og skilvirkni fyrirtækisins fyrir gildandi ár.                                                                                                                                                                                                                           |
| Samantekt á útgjöldum 12 mánaða - Sjálfgefið                       | Fá innsýn í útgjöld fyrir hvern af síðustu 12 mánuðum. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                                       |
| Samantekt á tekjuyfirliti ársfjórðungs - Sjálfgefið               | Skoða arðsemisgreiningu fyrirtækisins ársfjórðungslega á síðastliðnu ári og einnig ári til dagsetningar.                                                                                                                                                                                                                   |
| Efnahagsreikningur hlið við Hlið – Sjálfgefin                      | Skoða fjárhagslega stöðu fyrirtækisins fyrir árið. Þessi skýrsla sýnir eignir og skuldir og eigið fé hluthafa hlið við hlið.                                                                                                                                                                                |
| [Samantekt á prófjöfnuði - Sjálfgefið](trial-balance-financial-reports.md)| Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa opnun og lokun stöður og debet og kredit stöður með nettó mismun þeirra.                                                                                                                                                                  |
| [Samantekt á Prófjöfnuði Ári til Árs – Sjálfgefin](trial-balance-financial-reports.md)| Skoða upplýsingar um stöðu fyrir alla reikninga sem hafa opnun- og lokun stöður og debet og kredit stöður með nettó mismun þeirra yfir núgildandi ár og fyrra ár.                                                                                                                           |
| Vikulegar Sölur- og Afslættir - Sjálfgefið                     | Fá innsýn í sölu- og afslætti fyrir hverja viku í mánuði. Þessi skýrsla inniheldur fjögurra vikna samtölu.                                                                                                                                                                                                              |
| Fjármagn fjárhagsáætlunar tiltækt - sjálfgefinn                         | Skoða sundurliðað samanburður af endurskoðað fjárhagsáætlun, raunútgjöld, frátekt fjárhagsáætlunar og fjármagn fjárhagsáætlunar tiltækt fyrir allir reikningar                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>Opna fjárhagsskýrslur
Þegar **Fjárhagsskýrslugerð** valmyndin er valin birtist listi yfir sjálfgefnar fjárhagsskýrslur fyrir fyrirtækið. Síðan er hægt að opna og breyta skýrslu. Velja heiti skýrslu til að opna sjálfgefnu skýrslurnar. Í fyrsta sinn sem skýrsla er opnað, er hún sjálfvirkt mynduð fyrir fyrri mánuð. Til dæmis, ef skýrsla er opnuð í fyrsta sinn í Ágúst 2019 er hún mynduð fyrir 31. Júlí 2019. Eftir að skýrsla er opnuð er hægt að hefja skoðun á henni með þvi að kafa niður í sértæka gagnahluta og breyta valkostum skýrslu.

## <a name="creating-and-modifying-financial-reports"></a>Stofna og breyta fjárhagsskýrslum
Af listanum yfir fjárhagsskýrslur er hægt að stofna nýja skýrslu eða breyta fyrirliggjandi skýrslu. Ef notandi hefur viðeigandi heimildir, er hægt að stofna nýja fjárhagsskýrslu með því að velja **Nýtt** í Aðgerðarúðunni. Skýrsluhönnunarforriti er hlaðið niður á tækið og opnast síðan. Eftir að skýrsluhönnun opnast er hægt að stofna nýja skýrslu. Þegar búið er að vista nýja skýrslu birtist hún í lista yfir fjárhagsskýrslur. Listinn sýnir einungis skýrslur sem voru stofnaðar fyrir fyrirtæki sem verið er að nota í Dynamics 365 Finance. 

## <a name="reporting-tree-definitions"></a>Skilgreiningar skipurits 
Einn af íhlutunum sem eru notaðir til að búa til fjárhagsskýrslur er skilgreining skipurits. skipuritsskilgreining aðstoðar við að skilgreina byggingu og stigveldi fyrirtækisins þíns. Hún er þvervíddarlegt stigveldi sem byggist á víddarvenslum innan fjárhagsgagnanna. Hún veitir upplýsinga á stigi einingar skipuritsins og á stigi samantektarinnar fyrir allar einingar í trénu.

Hægt er að stofna ótakmarkaðan fjölda af skipuritum til að sýna gögn fyrirtækisins á mismunandi vegu. Hvert skipurit getur innihaldið hvaða samsetningu af deildum og samantektareiningum sem er en skýrsluskilgreining getur haft tengil á aðeins eitt skipurit í einu. 


## <a name="troubleshooting-issues-opening-report-designer"></a>Úrræðaleit vegna vandamála við opnun skýrsluhönnunar
Nokkur algeng vandamál eru til staðar sem geta valdið vandræðum þegar Skýrsluhönnun er opnuð. Þessi vandamál og skrefin til að leysa úr þeim eru eftirfarandi.

Vandamál 1: Skýrsluhönnun hefst ekki þegar valið er **Nýtt** eða **Breyta**.

* Í Internet Explorer, veljið **Stillingar**, síðan skal velja **Internetvalkostir**. Velja skal flipann **Öryggi**. Veljið Traust vefsvæði og veljið síðan **Vefsvæði**. Í **Bæta þessu vefsvæði við svæði**, skal færa inn „\*\.dynamics.com“ (án gæsalappa) og síðan velja **Bæta við**. 
* Í Internet Explorer, veljið **Stillingar**, síðan skal velja **Internetvalkostir**. Velja skal flipann **Öryggi**. Veljið Traust vefsvæði. Á svæðinu sem merkt er Öryggisstig fyrir þetta svæði skal breyta valkostinum í **Miðlungs-lágt**.
* Slökkvið á sprettigluggavörninni í vafranum.
* Vinnutölvur eru nauðsynlegar til að setja upp Microsoft .NET Framework 4.6.2 eða nýrri. Hægt er að sækja og setja upp þessa útgáfu af Microsoft .NET Framework úr [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=53345).
* Ef verið er að nota Chrome vafra, verður að setja upp ClickOnce-viðauka til að sækja skýrslu Report Designer. Ef verið er að nota Chrome í huliðsstillingu skal ganga úr skugga um að ClickOnce viðbót sé einnig virkur fyrir huliðsstillingu. Frekari upplýsingar um Chrome ClickOnce viðbótina er að finna í [Kerfisskilyrði fyrir uppsetningu í skýi](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Ef notað er Microsoft Edge með Chrome-vafra þarf ekki að setja upp ClickOnce viðbót fyrir Edge Chromium. Hins vegar verður að kveikja á valkostinum ClickOnce til að sækja valkostinn biðlara Skýrsluhönnunar. Ef verið er að nota huliðsstillingu, ganga úr skugga um að ClickOnce viðbótin sé einnig virk fyrir huliðsstillingu.
     1. Opna nýjan vafraglugga í Microsoft Edge.
     2. Sláið inn **edge://flags** og veljið **Færa inn**.
     3. Leitið að valkostinn **ClickOnce stuðningur** eða notið þennan beina tengil: **edge://flags/#edge-click-once**.
     4. Stilla valkostinn fellivalmynd á **Virkt**.
     5. Veljið **Endurræsa vafra**.

Vandamál 2: Notanda hefur ekki verið úthlutað nauðsynlegum heimildum til að nota Financial Reporting. 

* Til að sannprófa hvort notandi hafi ekki heimild skal velja **Já** þegar villan „Ekki var hægt að tengjast netþjóni Financial Reporting“ kemur upp. Veldu Já ef þú vilt halda áfram og tilgreina annað vistfang þjóns Veljið síðan **Prófa tengingu**. Ef þú ert ekki með heimild sérðu skilaboð sem segja „Tilraun til tengingar mistókst. Notandi hefur ekki nægilegar heimildir til að tengjast þjóninum. Hafa skal samband við kerfisstjóra.
* Nauðsynlegar heimildir eru taldar upp hér að ofan í [Veita öryggisaðgang að Financial Reporting](#granting-security-access-to-financial-reporting). Öryggi í Financial Reporting byggir á þessum réttindum. Þú færð ekki aðgang nema þér sé úthlutað þessum réttindum (eða öðru öryggishlutverki sem felur í sér þessi réttindi). 
* Innleiðingarverkið **Fyrirtækjanotendaveita til fyrirtækis** (sem einnig er ábyrg fyrir og þekkt sem innleiðing notanda) keyrir með 5 mínútna millibili. Það kann að taka allt að 10 mínútur fyrir allar heimildabreytingar að taka gildi í Financial Reporting. 
  Ef annar notandi getur opnað skýrsluhönnun skal velja **Verkfæri** og síðan velja **Samþættingarstaða**. Staðfestið að samþættingarvörpunin „Fyrirtækjanotendaveita til fyrirtækis“ hafi keyrt vegna þess að þér var úthlutað réttindum til að nota Financial Reporting. 
* Hugsanlegt er að önnur villa hafi komið í veg fyrir að **Samþætting Dynamics-notanda við Financial Reporting-notanda** hafi náð að klárast. Eða að hugsanlega hafi endurstilling gagnaskemmu hafi verið sett af stað og ekki lokið enn, eða að önnur kerfisvilla hafi komið upp. Reynið að keyra ferlið aftur síðar. Hafið samband við kerfisstjóra ef vandamálið er viðvarandi.

Vandamál 3: Þú getur haldið áfram framhjá ClickOnce innskráningarsíðu skýrsluhönnunar, en getur ekki lokið innskráningu innan skýrsluhönnunar. 

* Tíminn sem stilltur er á staðbundinni tölvu þegar þú slærð inn innskráningarupplýsingarnar þínar verður að vera innan fimm mínútna af tímanum á netþjóni Financial Reporting. Ef það er mismunur upp á meira en fimm mínútur mun kerfið ekki leyfa innskráningu. 
* Í slíku tilfelli er mælt með því að virkja Windows-valkostinn um að stilla tíma tölvunnar sjálfkrafa. 

## <a name="additional-resources"></a>Frekari upplýsingar
- [Skoða fjárhagsskýrslur](view-financial-reports.md)
- [Skilgreiningar skipurits í fjárhagsskýrslum](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]