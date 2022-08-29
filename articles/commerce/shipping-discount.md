---
title: Sendingarafsláttur
description: Þessi grein lýsir sendingarafsláttargetu í Microsoft Dynamics 365 Commerce og uppsetninguna sem þarf til að nota þau.
author: ShalabhjainMSFT
ms.date: 08/23/2020
ms.topic: overview
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2019-01-31
ms.openlocfilehash: f19566ce64becea4a53a8479cb5a08579567cda1
ms.sourcegitcommit: 1dbff0b5fa1f4722a1720fac35cce94606fa4320
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/24/2022
ms.locfileid: "9346101"
---
# <a name="shipping-discount"></a>Sendingarafsláttur

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þessi grein lýsir sendingarafsláttargetu í Microsoft Dynamics 365 Commerce og uppsetninguna sem þarf til að nota þau.

Ókeypis sendingarkostnaður eða afsláttur er einn þáttur sem hefur áhrif á kaupákvarðanir viðskiptavina á netinu. Til að auka tekjur sínar fyrir hverja færslu nota margir smásalar ókeypis sendingarkostnað til að hvetja viðskiptavini til að stækka körfu sína.

Commerce styður möguleika á sendingarafslætti sem gerir smásöluaðilum kleift að stilla afsláttarprósentu af sendingargjöldum fyrir tiltekna sendingaraðferð þegar heildarsöluupphæð fyrir viðurkenndar vörur í viðskiptunum uppfyllir ákveðin skilyrði. Dæmi um atburðarás sem notar möguleika á sendingarafslætti er "Eyddu $50 eða meira til að fá ókeypis sendingu yfir nótt."

## <a name="prerequisites"></a>Forkröfur

Sendingarafsláttargetan er studd af Commerce [alhliða háþróuð sjálfvirk hleðsla](/dynamics365/unified-operations/retail/omni-auto-charges) eiginleikar. Til að flutningsafsláttargetan virki verður þú að virkja **Notaðu háþróaða sjálfvirka hleðslu** stillingar á **Pantanir viðskiptavina** flipi á **Viðskiptabreytur** síðu í höfuðstöðvum Commerce. Söluaðilar geta notað háþróaða sjálfvirka gjaldtöku til að setja upp ýmsar gerðir gjalda, svo sem meðhöndlun, uppsetningu og förgun.

Sendingarafslátturinn gildir aðeins á sendingarkostnað. Þess vegna verður smásali að tilgreina hvaða gjöld eru sendingarkostnaður. Til að tilgreina sendingarkostnað, í höfuðstöðvum Commerce, farðu á **Rásaruppsetning \> Gjöld \> Gjaldkóði**, og stilltu **Sendingargjald** valmöguleika til **Já** fyrir æskileg gjöld.

![Tilgreina gjald sem sendingargjald.](./media/Specify_shipping_charge.png)

## <a name="configuration"></a>Skilgreining

Sendingarafsláttargetan er flokkabundin og styður aðeins **Prósenta afsláttur** tegund útreiknings. Til að setja upp sendingarafslátt, í höfuðstöðvum Commerce, farðu á **Verð og afslættir \> Afsláttur fyrir sendingarmörk**. Síðan er hægt að tilgreina þann afhendingarmáta sem afslátturinn á við, skilgreina einn eða fleiri upphæðaþröskulda og stilla afsláttarprósentu fyrir hvern þröskuld. Þú getur líka stillt lista yfir flokka eða vörur sem hæfa hluti. Þannig verður aðeins söluupphæð á móti þessum hlutum í viðskiptum talin þegar verðlagsvélin metur hvort heildarviðskiptin standist viðmiðunarmörkin.

> [!NOTE]
> Ólíkt öðrum afsláttartegundum skapar sendingarafslátturinn ekki afsláttarlínur. Þess í stað breytir það sendingargjaldinu beint og bætir nafni afsláttarins við gjaldlýsinguna.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
