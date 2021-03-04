---
title: Endurmat á banka – erlendum gjaldmiðli
description: Þetta efnisatriði veitir yfirlit yfir endurmatsferli banka á erlendum gjaldmiðli. Það inniheldur upplýsingar um uppsetningu, keyrslu á ferli, útreikning ferlisins og bakfærslu á endurmatsfærslum.
author: mikefalkner
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankCurrencyRevalHistory
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-03-08
ms.dyn365.ops.version: 10
ms.openlocfilehash: f99a5ed82fd4d74a5d20620dbe19b4f18e332432
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444477"
---
# <a name="bank-foreign-currency-revaluation"></a>Endurmat á banka – erlendum gjaldmiðli

[!include [banner](../includes/banner.md)]


Þetta efnisatriði veitir yfirlit yfir endurmatsferli banka á erlendum gjaldmiðli. Það útskýrir hvernig á að setja upp og keyra ferlið og veitir upplýsingar um útreikning ferlisins. Það útskýrir einnig hvernig á að bakfæra endurmatsfærslur, ef bakfærslu er krafist.

Sem hluti af lokum tímabils, krefjast reikningsskilavenjur að staða bankareikninga í erlendum gjaldmiðlum verði endurmetnar með því að nota mismunandi gerðir gengis (núverandi, sögulegt, meðaltal og svo framvegis). Eiginleikann fyrir endurmat banka á erlendum gjaldmiðli er hægt að nota endurmeta einn eða fleiri bankareikninga. Eiginleikinn er einnig altækur. Þar af leiðandi geturðu frá einni síðu endurmetið banka yfir alla lögaðila sem þú hefur aðgang að.

> [!NOTE]
> Þegar endurmatsferlið er keyrt verður staða hvers bankareiknings sem er bókaður í erlendum gjaldmiðli endurmetin. Óinnleystur hagnaður eða tap sem stofnað er til við endurmatsferli eru mynduð af kerfinu. Hugsanlega eru tvær færslur stofnaðar, ein fyrir bókhaldsgjaldmiðil og ein fyrir skýrslugjaldmiðil, ef skýrslugjaldmiðill á við. Hver lykilfærsla verður bókuð í óinnleystum hagnaði eða tapi og í aðallyklinum sem verið er að endurmeta.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Undirbúa keyrslu á endurmati á erlendum gjaldmiðli

Eftirfarandi uppsetningar er krafist áður en endurmatsferlið er keyrt.

- Á síðunni **Fjárhagur** skaltu tilgreina gerð gengis. Ef gerð gengis er ekki tilgreint í aðallyklinum, verður þessi gerð gengis notuð við endurmat á erlendum gjaldmiðli.
- Á síðunni **Fjárhagur** skaltu tilgreina lykla fyrir innleystan hagnað, innleyst tap, óinnleystan hagnað og óinnleyst tap fyrir endurmat gjaldmiðils. Lyklar fyrir innleystan hagnað og innleyst tap eru notaðir þegar færslur viðskiptakrafna og viðskiptaskulda eru jafnaðar. Lyklar fyrir óinnleystan hagnað og óinnleyst tap eru notaðir til að endurmeta opnar færslur og aðallykla fjárhags.
- Á síðunni **Lyklar gjaldmiðilsendurmats** skal velja mismunandi lykla fyrir endurmat gjaldmiðils fyrir hvern gjaldmiðil og fyrirtæki. Ef engin lyklar eru skilgreindir, eru lyklar af síðunni **Fjárhagur** notaðir.

## <a name="enable-foreign-currency-revaluation"></a>Virkja endurmat á erlendum gjaldmiðli

Þú verður að kveikja á eiginleikanum fyrir endurmat banka í erlendum gjaldmiðli áður en hægt er að vinna úr endurmati á erlendum gjaldmiðlum.

1. Fara í **Reiðufjár- og bankastjórnun \> Uppsetning \> Færibreytur reiðufjár- og bankastjórnunar**.
2. Í flipanum **Almennt**, undir **Endurmat á erlendum gjaldmiðli**, skal stilla valkostinn **Virkja endurmat á banka** á **Já** til að kveikja á eiginleikanum fyrir núgildandi lögaðila. 
3. Í flipanum **Númeraraðir** skal bæta við númeraröð fyrir endurmat á erlendum gjaldmiðli.
4. Endurhlaða skal vafrann til að sjá **Endurmat á erlendum gjaldmiðli** í hlutanum **Reglubundin verkefni** á svæðissíðunni.

Þú verður að kveikja á eiginleikanum fyrir hvern lögaðila sem notar endurmat á erlendum gjaldmiðli. Ef þér er úthlutað hlutverki kerfisstjóra eða hlutverki sem stjórnandi eiginleika geturðu eytt þessu skrefi með því að virkja eiginleikann sem heitir **Virkja endurmat á banka án færibreytu** á vinnusvæðinu **Stjórnun eiginleika**.

> [!NOTE]
> Ef lögaðilinn þinn notar rússneskan, pólskan eða ungverskan lands-/svæðiskóða geturðu þegar gert endurmat á erlendum gjaldmiðli. Þú getur ekki notað endurmat á erlendum gjaldmiðli sem önnur lönd eða svæði nota.

## <a name="process-foreign-currency-revaluation"></a>Vinna endurmat á erlendum gjaldmiðli

Eftir að uppsetningu er lokið skal nota síðuna **Endurmat á erlendum gjaldmiðli** í Reiðufjár- og bankastjórnun til að endurmeta stöðurnar á einum eða fleiri bankareikningum þvert yfir alla lögaðila. Hægt er að keyra ferlið í rauntíma eða áætla að keyra það með því að nota runu.

Síðan **Endurmat á erlendum gjaldmiðli** sýnir söguna fyrir hvert endurmatsferli. Hún sýnir hvenær ferlið var keyrt og hvaða skilyrði voru skilgreind, og hún býður upp á tengil á fylgiskjalið sem var búið til fyrir endurmatið. Hún sýnir einnig hvort fyrra endurmat var bakfært. Til að keyra endurmatsferlið skal velja **Endurmat á erlendum gjaldmiðli** í aðgerðasvæðinu til að opna svargluggann **Banki - endurmat á erlendum gjaldmiðli**.

Reiturinn **Dagsetning endurmats** skilgreinir lokadagsetningu fyrir útreikning á stöðu erlends gjaldmiðils sem verður endurmetin. Samtala allra bankafærslna sem gerðust fram að þessum degi er endurmetin.

Reiturinn **Gengisdagsetning** skilgreinir dagsetningu gengis sem verður notuð til að endurmeta stöðu gjaldmiðils. Til dæmis er hægt að endurmeta stöður frá og með 31. janúar, en nota gengið sem er skilgreint fyrir 1. febrúar.

Hægt er að keyra endurmatsferli fyrir einn eða fleiri lögaðila. Uppflettingin sýnir eingöngu þá lögaðila sem þú hefur aðgang að. Veldu lögaðilana sem þú vilt velja bankareikninga fyrir sem eru gjaldgengir fyrir endurmat á erlendum gjaldmiðli. Allir bankareikningar þessara lögaðila verða sýndir í hnitanetinu.

Stilltu valkostinn **Forskoða fyrir bókun** á **Já** ef þú vilt forskoða niðurstöður endurmatsins áður en þú bókar þær. Endurmat á erlendum gjaldmiðli er með forskoðun sem hægt er að bóka. Ekki þarf að keyra endurmatsferlið aftur. Hægt er að flytja út niðurstöður forskoðunarinnar í Microsoft Excel til að halda utan um upplýsingarnar um hvernig upphæðir voru reiknaðar. Ekki er hægt að nota runuvinnslu ef forskoða á niðurstöður á endurmati.

Veldu **Í lagi** til að vinna úr endurmati á erlendum gjaldmiðli. Búin er til færsla til að fylgjast með ferli hverrar keyrslu. Sérstök færsla er búin til fyrir hvern lögaðila og bókunarlag.

## <a name="calculate-unrealized-gainloss"></a>Reikna óinnleystan hagnað/tap

Í Reiðufjár- og bankastjórnun er litið á gjaldmiðil bankans sem grunngjaldmiðil og er hann ekki endurmetinn. Staða bankareikningsins í bókhaldsgjaldmiðli er endurmetin með því að nota gengið milli bankagjaldmiðils og bókhaldsgjaldmiðils í **Gengisdagsetning**. Staða bankareikningsins í skýrslugjaldmiðli er einnig endurmetin með því að nota gengið milli bankagjaldmiðils og skýrslugjaldmiðils í **Gengisdagsetning**.

Færsla er búin til fyrir mismuninn milli stöðu bankareikningsins og nýju stöðunnar sem er reiknuð fyrir bókhaldsgjaldmiðil. Önnur færsla er búin til fyrir mismuninn milli stöðu bankareikningsins og nýju stöðunnar sem er reiknuð fyrir skýrslugjaldmiðil. Þessar færslur eru merktar sem afstemmdar. 

Engin færsla er gerð fyrir bókhaldsgjaldmiðilinn ef bankagjaldmiðill samsvarar bókhaldsgjaldmiðli. Að sama skapi er engin færsla gerð fyrir skýrslugjaldmiðilinn ef bankagjaldmiðill samsvarar skýrslugjaldmiðli.

Endurmatsfærsla á erlendum gjaldmiðli er einnig dreift á milli víddanna sem finnast í bankafærslunum. Dreifingin byggir á stöðunni fyrir hverja vídd. Til dæmis er heildarbankastaðan 10.000 en staðan fyrir viðskiptaeiningu 001 er 4.000, á meðan staðan fyrir viðskiptaeiningu 002 er 6.000. Í þessu tilfelli er 40 prósent af upphæð endurmatsins bókað á endurmatslykilinn sem er með viðskiptaeininguna 001 og 60 prósent er bókað á endurmatslykilinn sem er með viðskiptaeininguna 002. Ef lykilskipulagið inniheldur ekki viðskiptaeiningu, er heildarupphæðin bókuð á endurmatslykilinn.

## <a name="reverse-foreign-currency-revaluation"></a>Bakfæra endurmat á erlendum gjaldmiðli

Ef bakfæra þarf endurmatsfærsluna, skal velja **Bakfæra færslu** á aðgerðarsvæðinu á síðunni **Endurmat á erlendum gjaldmiðli**. Ný söguleg færsla fyrir endurmat á erlendum gjaldmiðli er stofnuð til að viðhalda sögulegri endurskoðunarslóð yfir því hvenær endurmatið átti sér stað eða var bakfært.

Til að bakfæra fleiri en eitt endurmat þarf að bakfæra nýlegasta endurmatið fyrst. Svo skal halda áfram til að bakfæra eldra endurmat í dagsetningarröð. Þú getur síðan unnið með nýtt endurmat fyrir þau tímabil sem þú bakfærðir.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]