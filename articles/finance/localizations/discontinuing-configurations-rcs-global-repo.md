---
title: Hætta með skilgreiningar í altækri geymslu RCS
description: Þetta efnisatriði lýsir hvernig á að hætta að nota skilgreiningar í altækri geymslu RCS.
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 1d25d583580af3d73a3ac1eaebc9f7d8413c6563
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360207"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>Hætta með skilgreiningar í altækri geymslu RCS

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig á að hætta að nota skilgreiningu í altækri geymslu RCS. Áður var aðeins hægt að eyða skilgreiningum sem ekki þurfti að nota lengur. Nú er hins vegar hægt að merkja útgefna skilgreiningu sem **Hætt að nota** í altækri geymslu RCS. Með þessari aðgerð er einnig hægt að gera eftirfarandi: 
 
 - Bjóða upp á tilkynningar fyrirfram þegar áformað er að hætta að nota skilgreiningu.
 - Hafa með viðeigandi upplýsingar um skilgreininguna sem kemur í staðinn.
 - Setja á dagsetningu fyrir **Stutt fram til** fyrir tiltekna skilgreiningu til að láta notandann vita hvenær hætt verður að nota hana.

Þegar hætt verður að nota útgáfu skilgreiningar er hægt að tilgreina eftirfarandi valfrjálsar upplýsingar:

  - **Skilgreining sem kemur í staðinn**
  - **Útgáfa skilgreiningar sem kemur í staðinn**
  - **Athugasemd með frjálsum texta**: Notið þennan reiti til að gefa upp tengla eða tilvísanir í fylgigögn
  - **Stutt fram til**: Þessi reitur gefur upp framlagða dagsetningu sem núverandi skilgreining/útgáfa verður studd fram að. Þessa dagsetningu þarf að uppfæra handvirkt.
  
Til að hætta að nota skilgreininguna skal ljúka eftirfarandi skrefum. 

1. Veljið hvort eigi að hætta að nota eina útgáfu eða allar útgáfur með sömu stillingunum í einni aðgerð með því að stilla **Allar útgáfur** á **Já**. 
2. Stillið færibreytuna **Hætta að nota** á **Já**.
3. Veljið **Í lagi** til að hætta að nota skilgreiningarnar. Fyllt verður í reitinn **Dagsetning niðurfellingar** þegar breytingarnar eru vistaðar.

![Upplýsingar um niðurfellingu skilgreiningar.](media/Discontinue-details-2.png)
  
Hægt er að snúa skilgreiningu aftur í **Samnýtt** eða breyta upplýsingum um niðurfellingu hvenær sem er. Ef skilgreining er samnýtt skal tilgreina dagsetningu fyrir **Stutt fram til** og allar aðrar upplýsingar sem tengjast niðufrfellingunni til að gefa til kynna áform um niðurfellingar í framtíðinni.

Ef ætlunin er að deila upplýsingum um áætlaða niðurfellingu, áður en skilgreiningin verður felld niður, þá er hægt að fylla fyrirfram í alla reiti sem tengjast skiptingu en skilja eftir færibreytuna **Hætta að nota** á **Nei**.

> [!NOTE]
> Niðurfelling takmarkar ekki aðgerðir á skilgreiningum. Áfram verður hægt að flytja inn, keyra eða hafa upp á skilgreiningum, þessir reitir eru til upplýsingar.

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finance styður við upplýsingagjöfina frá og með útgáfu 10.0.14

Frá og með útgáfu 10.0.14 mun Dynamics 365 Finance styðja við upplýsingagjöf um niðurfellingu. Á síðunni **Altæk geymsla** er hægt að skoða uppfærðar upplýsingar sem tengjast niðurfellingu. Skilgreiningar sem hætt er að nota eru sjálfgefið síaðar frá.
  
Síðan **Innfluttar skilgreiningar** (ERSolutionTable) sýnir skilgreiningar sem var hætt að nota áður en þær voru fluttar inn. Fyrir þær skilgreiningar sem hætt var að nota eftir innflutning, er hægt að samstilla upplýsingar um niðurfellingu með því að keyra vinnsluna **Uppfærslur á innflutningi skilgreininga**.


