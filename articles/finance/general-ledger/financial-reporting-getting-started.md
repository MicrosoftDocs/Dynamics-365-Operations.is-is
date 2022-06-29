---
title: Yfirlitssíða fjárhagsskýrslugerðar
description: Þessi grein lýsir því hvar á að nálgast fjárhagsskýrslur í Microsoft Dynamics 365 Fjármál og hvernig á að nota fjárhagsskýrslugetu.
author: aprilolson
ms.date: 06/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "10444"
- intro-internal
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f2c31e8b8b8022e5dfdb1f8dc4836d3d95174078
ms.sourcegitcommit: d9d111d7420ca8f1071689afe38a1ccf4b8051f4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/21/2022
ms.locfileid: "9033661"
---
# <a name="get-started-with-financial-reporting"></a>Hafist handa með fjárhagsskýrslugerð 

[!include [banner](../includes/banner.md)]

Þessi grein lýsir hvar á að fá aðgang að Fjárhagsskýrslugerð og hvernig á að nota fjárhagsskýrslugetu. Það inniheldur einnig lýsingu á sjálfgefið fjárhagsskýrslur sem er veitt.

## <a name="enable-financial-reporting"></a>Virkja fjárhagsskýrslu
Til að nota fjárhagsskýrsluþjónustuna fyrir fyrirtæki þitt, verður líftímaþjónustustjóri (LCS) að virkja þessa þjónustu í LCS gáttinni fyrir fyrirtæki þitt. Ef fjárhagsskýrslur hafa ekki verið útvegaðar fyrir umhverfið þitt, hafðu samband við LCS stjórnanda til að virkja þjónustuna. 

## <a name="accessing-financial-reporting"></a>Aðgangur að fjárhagsskýrslu

Hægt er að finna **Fjárhagskýrslugerð** valmyndina á eftirfarandi stöðum:

- **Aðalbók** > **Fyrirspurnir og skýrslur**
- **Fjárhagsáætlun** > **Fyrirspurnir og skýrslur** > **Grunn fjárhagsáætlunargerð**
- **Fjárhagsáætlun** > **Fyrirspurnir og skýrslur** > **Fjárhagsáætlun**
- **Fjárhagsáætlun** > **Fyrirspurnir og skýrslur** > **Fjárlagaeftirlit**
- Samstæður

Til að stofna og búa til fjárhagsskýrslur fyrir lögaðila, verður að setja upp eftirfarandi upplýsingar fyrir lögaðilann:

- Fjárhagsdagatal
- Ledger
- Bókhaldslykill
- Gjaldmiðill
- Bóka færslu á að minnsta kosti einum reikningi
- MainAccount er skráð í dálknum **Valið** á síðunni **Uppsetning reikningsskila** (**Fjárhagur > Fjárhagsuppsetning > Uppsetning reikningsskila**)

## <a name="granting-security-access-to-financial-reporting"></a>Veita öryggisaðgang að Financial Reporting

Fjárhagsleg skýrslugerð aðgerðir eru tiltækar fyrir notendur sem hafa fengið viðeigandi réttindi og skyldur úthlutað gegnum öryggishlutverk þeirra. Eftirfarandi kaflar telja upp þessi réttindi og skyldur, ásamt tengdum hlutverkum.

### <a name="duties"></a>Skyldur

| Merki skyldu                            | lýsing                                                             | AOT-heiti                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna og framkvæma stjórnunarverk. | FinancialReportsSecurityMaintain |
| Vinna með fjárhagsskýrslur            | Hanna og vinna með fjárhagsskýrslur.                                  | FinancialReportsMaintain         |
| Mynda fjárhagsskýrslur            | Mynda og uppfæra fjárhagsskýrslur.                                 | FinancialReportsGenerate         |
| Yfirfara fjárhagslega frammistöðu          | Yfirfara og greina fjárhagslega frammistöðu.                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>Heimildir

| Merki réttinda                       | lýsing                                                             | AOT-heiti                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna og framkvæma stjórnunarverk. | FinancialReportsSecuritySystemMaintain |
| Vinna með fjárhagsskýrslur            | Hanna og vinna með fjárhagsskýrslur.                                  | FinancialReportsMaintainReports  |
| Mynda fjárhagsskýrslur            | Mynda og uppfæra fjárhagsskýrslur.                                 | FinancialReportsGenerateReports  |
| Skoða fjárhagsskýrslur                | Skoða fjárhagsskýrslur.                                                 | FinancialReportsView             |

### <a name="roles"></a>Hlutverk

| Merki réttinda                       | Skuldbinding                                  | Hlutverk                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| Vinna með öryggi fjárhagsskýrslna | Vinna með öryggi fjárhagsskýrslna | Öryggisstjóri                                                          |
| Vinna með fjárhagsskýrslur            | Vinna með fjárhagsskýrslur            | Aðalbókari, yfirmaður bókhalds, fjármálastjóri, stjórnandi fjárhagsáætlunar |
| Mynda fjárhagsskýrslur            | Mynda fjárhagsskýrslur            | Forstjóri, framkvæmdastjóri, bókhaldari                                                            |
| Skoða fjárhagsskýrslur                | Yfirfara fjárhagslega frammistöðu          | Ekki úthlutað                                                                   |

Eftir að notanda er bætt við eða hlutverki er breytt, á notandinn að geta opnað fjárhagsskýrslugerð innan nokkrar mínútur. 

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
| 12 mánaða Leitni Tekjuyfirlits – Sjálfgefið                 | Skoða arðsemisgreiningu fyrirtækis síðustu 12 mánuði, hvern mánuð fyrir sig. Þessir 12 mánuðir geta náð yfir meira en eitt fjárhagsár.                                                                                                                                                                                             |
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
| [Rekstrarreikningur – Sjálfgefin](income-statement-financial-report.md)| Skoða arðsemi fyrirtækisins fyrir gildandi tímabil og ár til dagsetningar.                                                                                                                                                                                                                                   |
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

Af listanum yfir fjárhagsskýrslur er hægt að stofna nýja skýrslu eða breyta fyrirliggjandi skýrslu. Ef notandi hefur viðeigandi heimildir, er hægt að stofna nýja fjárhagsskýrslu með því að velja **Nýtt** í Aðgerðarúðunni. Skýrsluhönnunarforriti er hlaðið niður á tækið og opnast síðan. Eftir að skýrsluhönnun opnast er hægt að stofna nýja skýrslu. Þegar búið er að vista nýja skýrslu birtist hún í lista yfir fjárhagsskýrslur. Listinn sýnir aðeins skýrslur sem voru búnar til fyrir fyrirtækið sem þú ert að nota í Dynamics 365 Finance. 

## <a name="reporting-tree-definitions"></a>Skilgreiningar skipurits

Einn af íhlutunum sem eru notaðir til að búa til fjárhagsskýrslur er skilgreining skipurits. skipuritsskilgreining aðstoðar við að skilgreina byggingu og stigveldi fyrirtækisins þíns. Hún er þvervíddarlegt stigveldi sem byggist á víddarvenslum innan fjárhagsgagnanna. Hún veitir upplýsinga á stigi einingar skipuritsins og á stigi samantektarinnar fyrir allar einingar í trénu.

Hægt er að stofna ótakmarkaðan fjölda af skipuritum til að sýna gögn fyrirtækisins á mismunandi vegu. Hvert skipurit getur innihaldið hvaða samsetningu af deildum og samantektareiningum sem er en skýrsluskilgreining getur haft tengil á aðeins eitt skipurit í einu. 

## <a name="update-the-financial-reporting-version-through-slipstreaming"></a>Uppfæra útgáfu fjárhagsskýrslugerðar í gegnum innlimun

Fjármála- og rekstraröpp eru uppfærð í hverjum mánuði. Aftur á móti er fjárhagsskýrslugerð ekki endilega uppfærð með sömu tíðni. Þar að auki hafa viðskiptavinir fleiri valkosti um hvenær þeir innleiða uppfærslur fyrir Finance and Operations öpp. Uppfærslur fjárhagsskýrslugerðar eru sjálfkrafa settar upp. Fjárhagsskýrslugerð er með uppgefna útgáfu sem er notuð í umhverfi viðskiptavinar þegar þjónustuuppfærsla er innleidd, þegar niðurtími fer í gang eða þegar umhverfi viðskiptavinar er í viðhaldsham. Þetta ferli er þekkt sem *innlimun* eða *jöfnun* vegna þess að allar innleiðingar viðskiptavinar eru stilltar á sömu útgáfu af fjárhagsskýrslugerð.

Breytingar sem eru gefnar út í hverri útgáfu má finna í [Hvað er nýtt eða breytt í Dynamics 365 Finance](../../finance/get-started/whats-new-home-page.md). Verkvangsuppfærslur og villuleiðréttingar er hægt að finna í hlutanum „Frekari tilföng“ neðst á síðunni fyrir hverja útgáfu.

Valin útgáfa innlimunar er yfirfarin og villuleituð útgáfa fjárhagsskýrslugerðar sem er tilbúin fyrir framleiðslu. Það er samhæft við hvaða fyrri eða framtíðarútgáfu af Dynamics 365 Finance sem er. Fjárhagsskýrslugerð getur til dæmis verið í nýjustu 10.0.19 smíði á meðan viðskiptavinurinn er enn í forritsútgáfu 10.0.16.

> [!NOTE]
> Einu kringumstæðurnar þar sem viðskiptavinir geta farið í fyrri útgáfu (niðurfærslu) eiga sér stað ef Microsoft stöðvar jöfnunaruppsetningu vegna vandamáls. Um leið og lagfæring er í boði verður hún notuð sjálfkrafa.

Innlimunarferlið er að fullu sjálfvirkt og þarfnast engra aðgerða frá viðskiptavini. Þrjár grannfræðir nota innlimun, hver þeirra með örlítið öðruvísi hætti:

- **Á staðnum** – Uppsetningar á staðnum styðja ekki innlimun og jöfnun.
- **IaaS-þjónusta** – Innlimunarrökin eru notuð í öllum aðgerðum sem reyna að uppfæra fjárhagsskýrslugerð. Hún inniheldur tvíundaruppfærslur eða útsendingar sem innihalda tvíundaruppfærslur.
- **Sjálfsafgreiðsla** – Allar aðgerðir sem þurfa á niðurtíma fjárhagsskýrslugerðar að halda nota innlimunarrökin:

    - Tvíundaruppfærslur eða útsendingar sem innihalda tvíundaruppfærslur
    - S-lagfæringar eða annar niðurtími tölvukerfis
    - AOT-pakkainnleiðingar

## <a name="troubleshooting-issues-opening-report-designer"></a>Úrræðaleit vegna vandamála við opnun skýrsluhönnunar

Nokkur algeng vandamál eru til staðar sem geta valdið vandræðum þegar Skýrsluhönnun er opnuð. Þessi vandamál og skrefin til að leysa úr þeim eru eftirfarandi.

Vandamál 1: Skýrsluhönnun hefst ekki þegar valið er **Nýtt** eða **Breyta**.

* Í Internet Explorer, veljið **Stillingar**, síðan skal velja **Internetvalkostir**. Velja skal flipann **Öryggi**. Veljið Traust vefsvæði og veljið síðan **Vefsvæði**. Í **Bæta þessu vefsvæði við svæði**, skal færa inn „\*\.dynamics.com“ (án gæsalappa) og síðan velja **Bæta við**. 
* Í Internet Explorer, veljið **Stillingar**, síðan skal velja **Internetvalkostir**. Velja skal flipann **Öryggi**. Veljið Traust vefsvæði. Á svæðinu sem merkt er Öryggisstig fyrir þetta svæði skal breyta valkostinum í **Miðlungs-lágt**.
* Slökkvið á sprettigluggavörninni í vafranum.
* Vinnutölvur eru nauðsynlegar til að setja upp Microsoft .NET Framework 4.7.2 eða nýrri. Hægt er að sækja og setja upp þessa útgáfu af Microsoft .NET Framework úr [Microsoft Download Center](https://dotnet.microsoft.com/download/dotnet-framework/net472).
* Ef verið er að nota Chrome vafra, verður að setja upp ClickOnce-viðauka til að sækja skýrslu Report Designer. Ef verið er að nota Chrome í huliðsstillingu skal ganga úr skugga um að ClickOnce viðbót sé einnig virkur fyrir huliðsstillingu. Frekari upplýsingar um Chrome ClickOnce viðbótina er að finna í [Kerfisskilyrði fyrir uppsetningu í skýi](../../fin-ops-core/fin-ops/get-started/system-requirements.md).
* Ef notað er Microsoft Edge með Chrome-vafra þarf ekki að setja upp ClickOnce viðbót fyrir Edge Chromium. Hins vegar verður að kveikja á valkostinum ClickOnce til að sækja valkostinn biðlara Skýrsluhönnunar. Ef verið er að nota huliðsstillingu, ganga úr skugga um að ClickOnce viðbótin sé einnig virk fyrir huliðsstillingu.

    1. Opna nýjan vafraglugga í Microsoft Edge.
    2. Sláið inn **edge://flags** og veljið **Færa inn**.
    3. Leitið að valkostinn **ClickOnce stuðningur** eða notið þennan beina tengil: **edge://flags/#edge-click-once**.
    4. Stilla valkostinn fellivalmynd á **Virkt**.
    5. Veljið **Endurræsa vafra**.

Vandamál 2: Notanda hefur ekki verið úthlutað nauðsynlegum heimildum til að nota Financial Reporting. 

* Til að sannprófa hvort notandi hafi ekki heimild skal velja **Já** þegar villan „Ekki var hægt að tengjast netþjóni Financial Reporting“ kemur upp. Veldu Já ef þú vilt halda áfram og tilgreina annað vistfang þjóns. Veljið síðan **Prófa tengingu**. Ef þú ert ekki með heimild sérðu skilaboð sem segja „Tilraun til tengingar mistókst. Notandi hefur ekki nægilegar heimildir til að tengjast þjóninum. Hafa skal samband við kerfisstjóra.
* Nauðsynlegar heimildir eru taldar upp hér að ofan í [Veita öryggisaðgang að Financial Reporting](#granting-security-access-to-financial-reporting). Öryggi í Financial Reporting byggir á þessum réttindum. Þú færð ekki aðgang nema þér sé úthlutað þessum réttindum (eða öðru öryggishlutverki sem felur í sér þessi réttindi). 
* Innleiðingarverkið **Fyrirtækjanotendaveita til fyrirtækis** (sem einnig er ábyrg fyrir og þekkt sem innleiðing notanda) keyrir með 5 mínútna millibili. Það kann að taka allt að 10 mínútur fyrir allar heimildabreytingar að taka gildi í Financial Reporting. 

    Ef annar notandi getur opnað skýrsluhönnun skal velja **Verkfæri** og síðan velja **Samþættingarstaða**. Staðfestið að samþættingarvörpunin „Fyrirtækjanotendaveita til fyrirtækis“ hafi keyrt vegna þess að þér var úthlutað réttindum til að nota Financial Reporting. 

* Hugsanlegt er að önnur villa hafi komið í veg fyrir að **Samþætting Dynamics-notanda við Financial Reporting-notanda** hafi náð að klárast. Eða að hugsanlega hafi endurstilling gagnaskemmu hafi verið sett af stað og ekki lokið enn, eða að önnur kerfisvilla hafi komið upp. Reynið að keyra ferlið aftur síðar. Hafið samband við kerfisstjóra ef vandamálið er viðvarandi.

Vandamál 3: Þú getur haldið áfram framhjá innskráningarsíðu **ClickOnce Report Designer**, en getur ekki lokið innskráningu innan Report Designer. 

* Tíminn sem stilltur er á staðbundinni tölvu þegar þú slærð inn innskráningarupplýsingarnar þínar verður að vera innan fimm mínútna af tímanum á netþjóni Financial Reporting. Ef það er mismunur upp á meira en fimm mínútur mun kerfið ekki leyfa innskráningu. 
* Ef tíminn á tölvunni þinni er annar en tíminn á netþjóni fjárhagsskýrslugerðar mælum við með því að virkja valkost Windows um að stilla tíma tölvunnar sjálfkrafa. 

## <a name="troubleshoot-report-designer-issues-with-event-viewer"></a>Úrræðaleita vandamál varðandi Report Designer með viðburðarskoðun

Viðburðaskoðarinn er notaður til að greina nokkur vandamál sem geta komið upp við notkun fjárhagsskýrslugerðar. 

### <a name="what-happens-when-you-have-connections-issues-with-financial-reporting"></a>Hvað gerist þegar vandamál koma upp varðandi tengingar við fjárhagsskýrslugerð? 

Hér eru nokkur skref sem þú getur tekið til að gera samtal þitt við notendaþjónustu Microsoft skilvirkara og fundið lausn mála á fljótlegri hátt. 
 
Eftirfarandi skref fara í gegnum ferlið við að kveikja á skilaboðum viðburðarskoðunar fyrir fjárhagsskýrslugerð. Kladdarnir sem viðburðarskoðunin býr til auðvelda tæknimönnum hjá notendaþjónustunni að koast að rót vandans varðandi tenginguna á fljótlegan hátt. Sendu inn afrit af þessum klöddum ásamt miðanum þínum þegar þú hefur samband við notendaþjónustuna.


1. Afritaðu skrána RegisterETW.zip í vinnutölvu biðlarans (helst borðtölvu) og dragðu út [RegisterETW.zip](https://mbs2.microsoft.com/fileexchange/?fileID=60b1106b-d5f8-4e0f-8041-039102505122).
2. Gakktu úr skugga um að viðburðarskoðun Windows sé lokuð.
3. Opnaðu skipanakvaðningu Administrator PowerShell og farðu í skráasafnið þar sem RegisterETW.ps1 er staðsett.
4. Keyrðu eftirfarandi skipun: .\RegisterETW.ps1

    Vel heppnað úttak í PowerShell verður staðfest með skilaboðunum **Forskrift RegisterETW lokið**.

    Opnaðu viðburðaskoðarann aftur og þú munt nú sjá þessa kladda undir **Microsoft > Dynamics**:

    * MR-biðlari
    * MR-DVT
    * MR-samþætting
    * MR-skráning
    * MR-skýrslur
    * MR_SchedulerTasks
    * MR-Sql
    * MR-TraceManager

5. Endurgerðu málið í Report Designer.
6. Flyttu út MR-Logger viðburði með því að nota viðburðarskoðun.

## <a name="troubleshoot-issues-connecting-to-financial-reporting"></a>Úrræðaleita vandamál varðandi tengingu við fjárhagsskýrslugerð

Vandamál: Þú færð villuna „Ekki tókst að koma á tengingu við netþjón fjárhagsskýrslugerðar“.

* Finndu út hvort vandamálið komi upp í netvöfrum Chrome og Edge.
* Ef vandamálið kemur aðeins upp í öðrum vafranum gæti það verið vandamál varðandi ClickOnce. 
* Þegar þú færð villuboð um tengingu skaltu velja **Próf** til að prófa tenginguna til að sjá hvaða skilaboð birtast. 
* Vandamálið gæti verið afleiðing þess að annar notandi hafi ekki aðgang að fjárhagsskýrslugerð. Ef notandi hefur ekki aðgang fær hann skilaboð um að hann hafi ekki heimild.
* Ef vandamálið kemur upp í mörgum vöfrum skaltu ganga úr skugga um að tímaklukkan í vinnutölvunni sé stillt á sjálfvirka stillingu.
* Vinna með notanda sem hefur réttindi öryggisstjóra í Dynamics 365 Finance, og stjórnandaréttindi á netléninu, til að skrá þig inn á vinnustöðina þína til að sjá hvort þeir geti tengst. Ef viðkomandi getur tengst gæti málið tengst netheimildum.
* Slökktu tímabundið á eldvegg í vinnutölvunni. Ef þú getur síðan tengst Report Designer tengist vandamálið eldveggnum þínum. Starfaðu með tæknideild fyrirtækisins til að leysa úr vandamálinu.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skoða fjárhagsskýrslur](view-financial-reports.md)
- [Skilgreiningar skipurits í fjárhagsskýrslum](../../fin-ops-core/dev-itpro/analytics/financial-reporting-tree-definitions.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
