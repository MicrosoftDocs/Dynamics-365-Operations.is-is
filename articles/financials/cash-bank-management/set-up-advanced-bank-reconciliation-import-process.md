---
title: "Setja upp ítarlegan innflutning bankaafstemmingarferlis"
description: "Ítarleg bankaafstemming gerir það mögulegt að flytja inn rafræn bankayfirlit og stemma þau sjálfkrafa við bankafærslur í Microsoft Dynamics 365 for Finance and Operations, Enterprise-útgáfu. Þessi skrá útskýrir hvernig á að setja upp mikilvægar aðgerðir fyrir innflutning fyrir bankayfirlitið."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 106853
ms.assetid: 45dae275-ea45-4c7e-b38f-89297c7b5352
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4d7bb0fc5abedcce973632434a5cc174449cdc22
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-the-advanced-bank-reconciliation-import-process"></a>Setja upp ítarlegan innflutning bankaafstemmingarferlis

[!include[banner](../includes/banner.md)]


Ítarleg bankaafstemming gerir það mögulegt að flytja inn rafræn bankayfirlit og stemma þau sjálfkrafa við bankafærslur í Microsoft Dynamics 365 for Finance and Operations, Enterprise-útgáfu. Þessi skrá útskýrir hvernig á að setja upp mikilvægar aðgerðir fyrir innflutning fyrir bankayfirlitið. 

Uppsetning fyrir innflutning bankayfirlits er breytileg, eftir snið rafrænnar bankayfirliti. Finance and Operations styður þrjú bankauppgjörssnið sem eru utan við: ISO20022, MT940 og BAI2.

## <a name="sample-files"></a>Sýnisskrár
Fyrir öll þrjú snið verður að hafa skrár sem þýða rafræna bankayfirlitið úr upprunalegu sniði á snið sem Dynamics 365 for Finance and Operations getur notað. Hægt er að finna nauðsynlegar skrár undir **Tilföng** hnút í Explorer Forritinu í Microsoft Visual Studio. Þegar búið er að finna skrár, skal afrita þær á einn þekktan stað svo að hægt sé að hlaða upp á einfaldan hátt meðan á uppsetningu stendur.

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
Hér að neðan eru dæmi um innflutning ítarlega afstemmingu skilgreiningar tæknilegar útlit og þriggja tengdum skrám bankayfirlits dæmi: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  

| Skilgreining tæknilegs útlits                             | Dæmi bankayfirlitsskránni          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |

 

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
10. Fyrir Raðnúmer 1, smellið á **Hlaða upp skrá**, og veljið **ISO20022XML-to-Reconciliation.xslt** skrár sem vistuð var fyrr. **Athugasemd:** Finance and Dynamics 365 for Operations umbreytingarskrár eru búnar til fyrir stöðluð snið. Þar sem bankar nota oft annað snið en þetta, þarf að uppfæra breytingaskrá svo hún varpi í snið bankayfirlits. <!-- For details about the expected format for ISO20022, see [Dynamics AX ISO20022 Layout](./media/dynamicsaxiso20022layout1.xlsx).-->
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
12. Fyrir Raðnúmer 2, smellið **Hlaða upp skrá**, og veljið **MT940XML-to-Reconciliation.xslt** skrár sem vistuð var fyrr. **Athugasemd:** Finance and Dynamics 365 for Operations umbreytingarskrár eru búnar til fyrir stöðluð snið. Þar sem bankar nota oft annað snið en þetta, þarf að uppfæra breytingaskrá svo hún varpi í snið bankayfirlits. <!--- For details about the expected format for MT940, see [Dynamics AX MT940 Layout](./media/dynamicsaxmt940layout1.xlsx)-->
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
12. Fyrir Raðnúmer 2, smellið **Hlaða upp skrá**, og veljið **BAI2XML-to-Reconciliation.xslt** skrár sem vistuð var fyrr. **Athugasemd:** Finance and Dynamics 365 for Operations umbreytingarskrár eru búnar til fyrir stöðluð snið. Bankar nota oft annað snið en þetta og þú kannt að þurfa að uppfæra breytingaskrá svo hún varpi í snið bankayfirlits. <!--- For details about the expected format for BAI2, see [Dynamics AX BAI2 Layout](./media/dynamicsaxbai2layout1.xlsx).-->
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




