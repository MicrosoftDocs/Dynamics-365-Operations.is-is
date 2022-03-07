---
title: Setja upp ítarlegan innflutning bankaafstemmingarferlis
description: Ítarleg bankaafstemming aðgerð gerir það mögulegt að flytja inn rafrænt bankayfirlit og afstemma þau sjálfkrafa við bankafærslu í Microsoft Dynamics 365 Finance. Þessi skrá útskýrir hvernig á að setja upp mikilvægar aðgerðir fyrir innflutning fyrir bankayfirlitið.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0efe960bee8f5c2c0b683ad641379345ce6d470180d29893b373acc6e1de8aa
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726039"
---
# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Setja upp ítarlegan innflutning bankaafstemmingarferlis

[!include [banner](../includes/banner.md)]

Ítarleg bankaafstemming aðgerð gerir það mögulegt að flytja inn rafrænt bankayfirlit og afstemma þau sjálfkrafa við bankafærslu í Dynamics 365 Finance. Þessi skrá útskýrir hvernig á að setja upp mikilvægar aðgerðir fyrir innflutning fyrir bankayfirlitið. 

Uppsetning fyrir innflutning bankayfirlits er breytileg, eftir snið rafrænnar bankayfirliti. Finance styður þrjú bankauppgjörssnið sem eru utan við: ISO20022, MT940 og BAI2.

## <a name="set-time-zone-preference"></a>Stilltu kjörstillingar tímabelta
Þegar þú stillir innflutningsstillingar bankayfirlitsins getur verið mikilvægt að hafa í huga tímabelti dagsetningartímabilsins innan bankayfirlitsskrár sem fluttar verða inn. Sjálfgefið er að gera ráð fyrir hvaða dag- og tímagildi séu þegar í samhæfðum alheimstíma (UTC) og því verður ekki breytt neinu tímabelti þegar þú flytur gögnin inn. 

Það er möguleiki í boði til að tilgreina tímabelti sem á að nota til að flytja inn gögn. Þessi valkostur er tiltækur á reitnum **Kjörstillingar tímabelta** á hverri **Upplýsingar um snið upprunagagna** (**Gagnastjórnunarvinnusvæði > Skilgreina gagnagjafa > Velja gagnasnið > Svæðisbundnar stillingar** flýtiflipi). Þessi tímabeltisval sem þú slærð inn á við um allan innflutning sem notar það upprunagagnasnið. Þú getur búið til eins mörg snið gagnaheimilda og þarf til að flytja inn gögn frá mörgum tímabeltum.  

Þetta tímabelti er ef til vill ekki það sama og tímabelti notanda eða fyrirtækis, svo vertu viss um að skýra hvaða tímabelti dagsetning og tímagögn eru að nota. Við mælum með að þú lítir á eftirfarandi atriði þegar þú stillir tímabeltisval. 

 - Tímabeltisvalið sem þú slærð inn á við um allan innflutning sem notar það upprunagagnasnið. Þú getur búið til eins mörg snið gagnaheimilda og þarf til að meðhöndla innflutning á gögnum frá mörgum tímabeltum. 
 
 - Tímabeltisvalið ætti að vera staðartímabelti dagsetningar- og tímagagna í innflutningsskránni. 
 
 - Tímabelti dagsetningar og tímagagna er ef til vill ekki það sama og tímabelti notanda eða fyrirtækis.
 
 - Notendur geta aðlagað sitt eigið tímabelti með því að nota þeirra **Valkostir notenda**.

Athugaðu að eftirfarandi aðgerðir geta hjálpað til við að lágmarka hugsanleg átök á dagsetningu og tíma þegar þú flytur inn bankayfirlit. 

 - Forðist að breyta tímabeltisstillingunum fyrir bankareikninga sem þegar hafa verið fluttir inn yfirlýsingar. Að breyta vali á tímabelti gæti haft áhrif á röðun nýrra fullyrðinga miðað við fyrirliggjandi yfirlýsingar vegna aðlögunar tímabeltisins. 
 
 - Skoðaðu allan innflutning sem notar valið snið gagnagrunna. Tímabeltisvalið sem tilgreint er fyrir sniðið gildir um öll innflutningsverkefni sem nota það snið. Sannprófaðu að tímabeltisvalið sé viðeigangi fyrir öll innflutningsverkefni sem nota það snið.

## <a name="sample-files"></a>Sýnisskrár
Fyrir allar þrjár snið verður að hafa skrár sem þýða rafræna bankayfirlitið úr upprunalegu sniði á snið sem Finance getur notað. Hægt er að finna nauðsynlegar skrár undir **Tilföng** hnút í Explorer Forritinu í Microsoft Visual Studio. Þegar búið er að finna skrár, skal afrita þær á einn þekktan stað svo að hægt sé að hlaða upp á einfaldan hátt meðan á uppsetningu stendur.

| Nafn tilfangs                                           | Skrárnafn                            |
|---------------------------------------------------------|--------------------------------------|
| BankStmtImport\_BAI2CSV\_í\_BAI2XML\_xslt              | BAI2CSV-to-BAI2XML.xslt              |
| BankStmtImport\_BAI2XML\_í\_Afstemming\_xslt       | BAI2XML-to-Reconciliation.xslt       |
| BankStmtImport\_BankReconciliation\_í\_Samsett\_xslt | BankReconciliation-to-Composite.xslt |
| BankStmtImport\_ISO20022XML\_í\_Afstemming\_xslt   | ISO20022XML-to-Reconciliation.xslt   |
| BankStmtImport\_MT940TXT\_í\_MT940XML\_xslt            | MT940TXT-to-MT940XML.xslt            |
| BankStmtImport\_MT940XML\_í\_Afstemming\_xslt      | MT940XML-to-Reconciliation.xslt      |
| BankStmtImport\_SampleBankCompositeEntity\_xml          | SampleBankCompositeEntity.xml        |

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Dæmi um bankayfirlitssnið og tæknilegar útlit
Hér að neðan eru dæmi um skilgreiningar tæknilegs útlits fyrir innflutningsskrá ítarlegrar bankaafstemmingar og þrjú skráardæmi um tengd bankayfirlit: [Flytja inn skrá dæmi](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Skilgreining tæknilegs útlits                             | Dæmi bankayfirlitsskránni          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |



## <a name="set-up-the-import-of-iso20022-bank-statements"></a>Setja upp innflutning á bankayfirlitum ISO20022
Fyrst verður að skilgreina vinnsluhóp fyrir snið bankayfirlits fyrir ISO20022 bankayfirlit með því að nota rammann fyrir gagnaeiningu.

1.  Fara á **vinnusvæði** &gt; **Gagnastjórnun**.
2.  Smellt er á **Flytja inn**.
3.  Færa inn heiti á sniðsins, eins og **ISO20022**.
4.  Stillið **snið upprunagagna** reitinn á **XML-eining**.
5.  Stilltu **Einingarheiti** reitinn á **Bankayfirlit**.
6.  Til að hlaða upp innflutningsskrár, smellið á **Hlaða upp**, og flettið svo til að velja **SampleBankCompositeEntity.xml** skrár sem var vistuð fyrr.
7.  Eftir að einingu bankayfirlits er hlaðið upp og vörpun er lokið, smellið á **Skoða kort** aðgerð fyrir eininguna.
8.  Einingin bankayfirlit er samsett eining sem samanstendur úr fjórum mismunandi einingum. Á listanum, veljið **BankStatementDocumentEntity**, og smellið á **Skoða kort** aðgerð.
9.  Á flipanum **umbreyting** smellirðu á **Nýtt**.
10. Fyrir Raðnúmer 1, smellið á **Hlaða upp skrá**, og veljið **ISO20022XML-to-Reconciliation.xslt** skrár sem vistuð var fyrr. **Athugasemd:** Umbreytingarskrár eru búnar til fyrir stöðluð snið. Þar sem bankar nota oft annað snið en þetta, þarf að uppfæra breytingaskrá svo hún varpi í snið bankayfirlits. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
11. Smellt er á **Nýtt**.
12. Fyrir Raðnúmer 2, smellið **Hlaða upp skrá**, og veljið **BankReconciliation-to-Composite.xslt** skrár sem vistuð var fyrr.
13. Smellið á **Nota umbreytingar**

Eftir að vinnsluhópur sniðs hefur verið sett upp, er næsta skref að skilgreina sniðsreglur bankayfirlits fyrir ISO20022 bankayfirlit.

1.  Fara í **Reiðufjár- og bankastjórnun** &gt; **Uppsetning** &gt; **Ítarleg uppsetning bankaafstemmingar** &gt; **Snið bankayfirlits**.
2.  Smellt er á **Nýtt**.
3.  Tilgreina snið yfirlits, eins og **ISO20022**.
4.  Færið inn heiti fyrir sniðið.
5.  Stilla skal **vinnsluhóp** reitinn á hópinn sem þú skilgreind fyrr, eins og **ISO20022**.
6.  Vekldy **XML-skránni** gátreitinn.

Síðasta skrefið er að virkja Ítarlega bankaafstemmingu og stilla snið yfirlits á bankareikning.

1.  Farið í **Reiðufjár- og bankastjórnun** &gt; **Bankareikningar**.
2.  Velja bankareikning og opnið til að skoða upplýsingarnar.
3.  Á **Afstemmingu** flipanum, skal stilla **Ítarlegri bankaafstemmingu** valkostinn á **Já**.
4.  Stilla skal **snið yfirlits** svæðið á sniðið sem var skilgreind fyrr, eins og **ISO20022**.

## <a name="set-up-the-import-of-mt940-bank-statements"></a>Setja upp innflutning á bankayfirlitum MT940
Fyrst verður að skilgreina vinnsluhóp fyrir snið bankayfirlits fyrir MT940 bankayfirlit með því að nota rammann fyrir gagnaeiningu.

1.  Fara á **vinnusvæði** &gt; **Gagnastjórnun**.
2.  Smellt er á **Flytja inn**.
3.  Færa inn heiti á sniðsins, eins og **MT940**.
4.  Stillið **snið upprunagagna** reitinn á **XML-eining**.
5.  Stilltu **Einingarheiti** reitinn á **Bankayfirlit**.
6.  Til að hlaða upp innflutningsskrár, smellið á **hlaða upp**, og síðan fletta til að velja **SampleBankCompositeEntity.xml** skrár sem var vistuð fyrr.
7.  Eftir að einingu bankayfirlits er hlaðið upp og vörpun er lokið, smellið á **Skoða kort** aðgerð fyrir eininguna.
8.  Einingin bankayfirlit er samsett eining sem samanstendur úr fjórum mismunandi einingum. Á listanum, veljið **BankStatementDocumentEntity**, og smellið á **Skoða kort** aðgerð.
9.  Á flipanum **umbreyting** smellirðu á **Nýtt**.
10. Fyrir Raðnúmer 1, smellið á **Hlaða upp skrá**, og veljið **MT940TXT-to-MT940XML.xslt** skrár sem vistuð var fyrr.
11. Smellt er á **Nýtt**.
12. Fyrir Raðnúmer 2, smellið **Hlaða upp skrá**, og veljið **MT940XML-to-Reconciliation.xslt** skrár sem vistuð var fyrr. **Athugasemd:** Umbreytingarskrár eru búnar til fyrir stöðluð snið. Þar sem bankar nota oft annað snið en þetta, þarf að uppfæra breytingaskrá svo hún varpi í snið bankayfirlits. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
13. Smellt er á **Nýtt**.
14. Fyrir Raðnúmer 3, smellið **Hlaða upp skrá**, og veljið **BankReconciliation-to-Composite.xslt** skrár sem vistuð var fyrr.
15. Smellið á **Nota umbreytingar**

Eftir að vinnsluhópur sniðs hefur verið sett upp, er næsta skref að skilgreina sniðsreglur bankayfirlits fyrir MT940 bankayfirlit.

1.  Fara í **Reiðufjár- og bankastjórnun** &gt; **Uppsetning** &gt; **Ítarleg uppsetning bankaafstemmingar** &gt; **Snið bankayfirlits**.
2.  Smellt er á **Nýtt**.
3.  Tilgreina snið yfirlits, eins og **MT940**.
4.  Færið inn heiti fyrir sniðið.
5.  Stilla skal **vinnsluhóp** reitinn á hópinn sem þú skilgreind fyrr, eins og **MT940**.
6.  Stillið **skáargerð** reit á **txt**.

Síðasta skrefið er að virkja Ítarlega bankaafstemmingu og stilla snið yfirlits á bankareikning.

1.  Farið í **Reiðufjár- og bankastjórnun** &gt; **Bankareikningar**.
2.  Velja bankareikning og opnið til að skoða upplýsingarnar.
3.  Á **Afstemmingu** flipanum, skal stilla **Ítarlegri bankaafstemmingu** valkostinn á **Já**.
4.  Þegar þú hefur verið beðinn um að staðfesta valið og virkjar Ítarlegri bankaafstemmingu er smellt á **í lagi**.
5.  Stilla skal **snið yfirlits** svæðið á sniðið sem var skilgreind fyrr, eins og **MT940**.

## <a name="set-up-the-import-of-bai2-bank-statements"></a>Setja upp innflutning á bankayfirlitum BAI2
Fyrst verður að skilgreina vinnsluhóp fyrir snið bankayfirlits fyrir BAI2 bankayfirlit með því að nota rammann fyrir gagnaeiningu.

1.  Fara á **vinnusvæði** &gt; **Gagnastjórnun**.
2.  Smellt er á **Flytja inn**.
3.  Færa inn heiti á sniðsins, eins og **BAI2**.
4.  Stillið **snið upprunagagna** reitinn á **XML-eining**.
5.  Stilltu **Einingarheiti** reitinn á **Bankayfirlit**.
6.  Til að hlaða upp innflutningsskrár, smellið á **hlaða upp**, og síðan fletta til að velja **SampleBankCompositeEntity.xml** skrár sem var vistuð fyrr.
7.  Eftir að einingu bankayfirlits er hlaðið upp og vörpun er lokið, smellið á **Skoða kort** aðgerð fyrir eininguna.
8.  Einingin bankayfirlit er samsett eining sem samanstendur úr fjórum mismunandi einingum. Á listanum, veljið **BankStatementDocumentEntity**, og smellið á **Skoða kort** aðgerð.
9.  Á flipanum **umbreyting** smellirðu á **Nýtt**.
10. Fyrir Raðnúmer 1, smellið **Hlaða upp skrá**, og velja **BAI2CSV-to-BAI2XML.xslt** skrár sem vistuð var fyrr.
11. Smellt er á **Nýtt**.
12. Fyrir Raðnúmer 2, smellið **Hlaða upp skrá**, og veljið **BAI2XML-to-Reconciliation.xslt** skrár sem vistuð var fyrr. **Athugasemd:** Umbreytingarskrár eru búnar til fyrir stöðluð snið. Bankar nota oft annað snið en þetta og þú kannt að þurfa að uppfæra breytingaskrá svo hún varpi í snið bankayfirlits. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
13. Smellt er á **Nýtt**.
14. Fyrir Raðnúmer 3, smellið **Hlaða upp skrá**, og veljið **BankReconciliation-to-Composite.xslt** skrár sem vistuð var fyrr.
15. Smellið á **Nota umbreytingar**

Eftir að vinnsluhópur sniðs hefur verið sett upp, er næsta skref að skilgreina sniðsreglur bankayfirlits fyrir BAI2 bankayfirlit.

1.  Fara í **Reiðufjár- og bankastjórnun** &gt; **Uppsetning** &gt; **Ítarleg uppsetning bankaafstemmingar** &gt; **Snið bankayfirlits**.
2.  Smellt er á **Nýtt**.
3.  Tilgreina snið yfirlits, eins og **BAI2**.
4.  Færið inn heiti fyrir sniðið.
5.  Stilla skal **vinnsluhóp** reitinn á hópinn sem þú skilgreind fyrr, eins og **BAI2**.
6.  Stillið **skáargerð** reit á **txt**.

Síðasta skrefið er að virkja Ítarlega bankaafstemmingu og stilla snið yfirlits á bankareikning.

1.  Farið í **Reiðufjár- og bankastjórnun** &gt; **Bankareikningar**.
2.  Velja bankareikning og opnið til að skoða upplýsingarnar.
3.  Á **Afstemmingu** flipanum, skal stilla **Ítarlegri bankaafstemmingu** valkostinn á **Já**.
4.  Þegar þú hefur verið beðinn um að staðfesta valið og virkjar Ítarlegri bankaafstemmingu er smellt á **í lagi**.
5.  Stilla skal **snið yfirlits** svæðið á sniðið sem var skilgreind fyrr, eins og **BAI2**.

## <a name="test-the-bank-statement-import"></a>Prófun á innflutningi bankayfirlits
Síðasta skrefið er að prófa hvort hægt sé að flytja inn bankayfirliti.

1.  Farið í **Reiðufjár- og bankastjórnun** &gt; **Bankareikningar**.
2.  Veljið bankareikning sem ítarlega bankaafstemming virkni er virkt fyrir.
3.  Á **Afstemming** flipanum, smellið á **Bankayfirlit**.
4.  Á við **Bankayfirlit** síðunni er smellt á **flytja Inn yfirlit**.
5.  Stilla skal **bankareikning** reitinn á valinn bankareikning. **uppgjörssnið** svæði verður stillt sjálfkrafa, byggt á stillingunni á bankareikning.
6.  Smellið á **Fletta**, og veljið rafræn bankayfirlitsskránni þíns.
7.  Smelltu á **Senda inn**.
8.  Smelltu á **Í lagi**.

Ef innflutningurinn heppnast, munu berast boð sem tilgreinir að uppgjör þitt var flutt inn. Ef innflutningur heppnaðist ekki, í **gagnastjórnun** vinnusvæði í í **Vinnslusögu** hlutanum, finna vinnslu. Smellið á **framkvæmdaupplýsingar** fyrir vinnslu til að opna **samantekt Framkvæmdar** síðuna og smellið síðan á **Skoða aðgerðaskrá** til að skoða villur innflutnings.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
