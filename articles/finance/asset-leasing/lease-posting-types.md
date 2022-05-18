---
title: Bókunargerðir leigusamnings
description: Þetta efnisatriði lýsir bókunargerðunum sem eru notaðar fyrir eignaleigufærslur.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6c06f68aebe7ed1ccc944793591202a9a221c42b
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720140"
---
# <a name="lease-posting-types"></a>Bókunargerðir leigusamnings

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir bókunargerðunum sem eru notaðar fyrir eignaleigufærslur.

## <a name="lease-asset"></a>Leigja eign

Lykillinn er tengdur við afnotaréttinn af eign. Þessi lykill er debetfærður þegar leigusamningur er skráður upphaflega samkvæmt nýjum bókhaldsreglum um leigusamninga, efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16). Fyrir breyttan leigusamning kann þessi lykill að vera debet- eða kreditfærður, allt eftir því hvort breytingin hækkar eða lækkar leiguskuldbindinguna.

**Dæmi um bókarfærslur:** Upphafleg viðurkenning<br>
**Debet:** Leigueign XXX<br>
**Kredit:** Leiguskuldbinding XXX

## <a name="lease-liability"></a>Leiguskuldbinding

Lykilinn tengist leiguskuldbindingu sem verður til þegar veittur er afsláttur af greiðslum samkvæmt hinum nýju IFRS 16 og ASC 842-stöðlunum. Þessi lykill er kreditfærður þegar leigusamningurinn er viðurkenndur upphaflega samkvæmt nýja staðlinum. Hann er debetfærðu fyrir leigugreiðslum og kreditfærður fyrir uppsöfnun vaxta.

**Dæmi um bókarfærslur:** Upphafleg viðurkenning<br>
**Debet:** Leigueign XXX<br>
**Kredit:** Leiguskuldbinding XXX

**Dæmi um bókarfærslur:** Uppsöfnun vaxta<br>
**Debet:** Vaxtarkostnaður XXX<br>
**Kredit:** Leiguskuldbinding XXX

**Dæmi um bókarfærslur:** Leigugreiðsla<br>
**Debet:** Leiguskuldbinding XXX<br>
**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX

## <a name="short-term-lease-liability"></a>Skuldbinding skammtímaleigu

Lykilinn er tengdur við skuldbindingu skammtímaleigu þegar bókarfærsla endurflokkunar fyrir skuldbiningu skammtímaleigu er bókað. Lykillinn er kreditfærður fyrir skuldbindingu skammtímaleigu frá afskriftaráætlun á síðasta degi mánaðarins. Sama upphæð er hins vegar debetfærð á fyrsta degi næsta mánaðar.

**Dæmi um bókarfærslur:** Endurflokkun skuldbindingar skammtímaleigu<br>
**Debet:** Leiguskuldbinding XXX<br>
**Kredit:** Skuldbinding skammtímaleigu XXX<br>
**Debet:** Skuldbinding skammtímaleigu XXX<br>
**Kredit:** Leiguskuldbinding XXX

## <a name="depreciation-expense"></a>Afskriftakostnaður

Lykillinn er tengdur við kostnaðinn sem tengist afskriftum á afnotarétti af eign samkvæmt IFRS 16, ASC 842 og fjármögnunarleigusamningum samkvæmt IAS 17 og ASC 840. Þessi lykill er skuldfærður þegar afnotaréttur af eign er afskrifaður í hverjum mánuði.

**Dæmi um færslubókarfærslur:** Afskriftauppsöfnun<br>
**Debet:** Afskriftakostnaður XXX<br>
**Kredit:** Uppsafnaðar afskriftir XXX

## <a name="gainloss-on-lease-modification"></a>Hagnaður/tap vegna breytinga á leigusamningi

Lykillinn tengist öllum hagnaði eða tapi sem hlýst af breytingum á leigusamningi. Hagnaður gæti orðið vegna breytinga á leigusamningi ef breytingin fæli í sér lægri leiguskuldbindingu sem nemur upphæð sem er hærri en bókfært virði afnotaréttar af eign.

Sem dæmi má nefna að leigusamningur er með núverandi bókfært virði leiguskuldbindingar upp á $150.000 og bókfært virði afnotaréttar af eign upp á $100.000. Leigusamningnum er breytt og þessar breytingar mynda nýtt núverandi virði á lágmarksleigugreiðslum (PVFMLP) upp á $40.000. Af þeim sökum verður leiguskuldbindingin debetfærð upp á $110.000 ($150.000 – $40.000). Þar sem afnotaréttur af eign er aðeins $100.000 mun minnkun upp á $110.000 lækka eignina umfram 0 (núll). Þess vegna segir í leiðbeiningum um bókhald að eftirstöðvar eigi að vera bókaðar á hagnaðarlykil. Hér verður endanleg færsla í færslubók því debetfærð á leiguskuldbindingu upp á $110.000, kreditfærð á leigueignina upp á $100.000 og kreditfærð á hagnaðarlykilinn upp á $10.000.

**Dæmi um bókarfærslur:** Breyting á leigusamningi<br>
**Debet:** Leiguskuldbinding XXX<br>
**Kredit:** Leigueign XXX<br>
**Kredit:** Hagnaður XXX

## <a name="accumulated-depreciation"></a>Uppsöfnuð afskrift

Lykillinn er tengdur við andstæðan eignalykil fyrir afnotarétt af eign. Þessi lykill er kreditfærður þegar afskriftarkostnaður er bókaður.

**Dæmi um færslubókarfærslur:** Afskriftauppsöfnun<br>
**Debet:** Afskriftakostnaður XXX<br>
**Kredit:** Uppsafnaðar afskriftir XXX

## <a name="variable-payment"></a>Breytileg greiðsla

Lykillinn tengist breytilegum leigugreiðslum sem eru myndaðar af endurmatsferli vísitölu samkvæmt ASC 842-, ASC 840- og IAS 17-leigusamningum. Í greiðsluáætlun leigusamnings eru breytilegar greiðslur innifaldar í dálknum **Breytileg greiðsla**. Þessi lykill er skuldfærður þegar reikningur er stofnaður gegn greiðsluáætlunarlínu sem inniheldur breytilega greiðslu.

**Dæmi um bókarfærslur:** Leigugreiðsla<br>
**Debet:** Leiguskuldbinding XXX<br>
**Skuldfærsla:** Breytileg greiðsla XXX<br>
**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX

## <a name="deferred-rent-asset-liability"></a>Frestaðar leigugreiðslur eignar (skuld)

Lykillinn er tengdur við frestaðar leigugreiðslur eignar eða skuldar sem er mynduð af frestuðum leigugreiðslum leigusamnings. Þessi lykill er debetfærður þegar reikningur er bókaður á móti frestuðum leigugreiðslum leigusamnings ef upphæð leigugreiðslu er hærri en línulegur leigukostnaður tímabilsins. Hann er kreditfærður ef leigugreiðslan er lægri en línulegur leigukostnaður tímabilsins.

**Dæmi um bókarfærslur:** Leigugreiðsla (frestaðar leigugreiðslur leigusamnings)<br>
**Debet:** Leigukostnaður XXX<br>
**Kredit:** Skuldbinding vegna frestaðra leigugreiðslna XXX<br>
**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX

## <a name="lease-expense"></a>Leigukostnaður

Lykillinn tengist leigukostnaðinum ef leigan er flokkuð sem frestaðar leigugreiðslur leigusamnings. Þessi lykill er debetfærður þegar reikningur er bókaður á móti frestuðum leigugreiðslum leigusamnings.

**Dæmi um bókarfærslur:** Leigugreiðsla (frestaðar leigugreiðslur leigusamnings)<br>
**Debet:** Leigukostnaður XXX<br>
**Kredit:** Skuldbinding vegna frestaðra leigugreiðslna XXX<br>
**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX

## <a name="impairment-expense"></a>Kostnaður virðisrýrnunar

Lykillinn er mótbókaður þegar leigusamningur skerðist. Þessi lykill er debetfærður á meðan lykill afnotaréttar af eign er kreditfærður beint.

**Dæmi um bókarfærslur:** Leigugreiðsla<br>
**Debet:** Kostnaður virðisrýrnunar XXX<br>
**Kredit:** Afnotaréttur af eign XXX

## <a name="lease-payment"></a>Leigugreiðsla

Lykillinn er mótbókaður ef slökkt er á færibreytunni **Greiða lánardrottni**. Lykillinn er kreditfærður í stað lánardrottnaskuldar ef slökkt er á færibreytunni.

**Dæmi um bókarfærslur:** Leigugreiðsla<br>
**Debet:** Leiguskuldbinding XXX<br>
**Kredit:** Leigugreiðsla XXX

## <a name="expense-type-postings"></a>Bókun kostnaðargerðar

Lykillinn sem er valinn fyrir hverja kostnaðargerð er debetfærður þegar greiðsla fyrir þá kostnaðargerð er mynduð. Til dæmis er lykillinn sem er tilgreindur fyrir kostnaðargerðina **Trygging** debetfærður í hvert sinn sem reikningur eða greiðslubókarfærsla er stofnuð úr rekstrarkostnaðaráætlun vegna tryggingakostnaðar.

**Dæmi um bókarfærslur:** Tryggingagreiðsla<br>
**Debet:** Tryggingakostnaðarlykill XXX<br>
**Kredit:** Mótlykill XXX

> [!NOTE]
> Mótlykill er valinn á leigustigi á línunum fyrir greiðsluáætlun rekstrarkostnaðar. Þessi mótlykill getur tengst lánardrottni eða með fjárhagslykli.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
