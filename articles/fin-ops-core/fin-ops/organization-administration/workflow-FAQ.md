---
title: Algengar spurningar um verkflæði
description: Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14aa9b56da005e8e3ca121589d0e22c60f34343b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189776"
---
# <a name="workflow-faq"></a>Algengar spurningar um verkflæði

[!include [banner](../includes/banner.md)]

Þetta efnisatriði svarar algengum spurningum um verkflæðiskerfið.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvers vegna koma margar tilkynningar þegar vinnulið er hafnað?
Þegar vinnulið er hafnað er honum lokið sem höfnuðum. Annar vinnuliður er stofnaður og honum er úthlutað á upphaflegan aðila. Þetta þýðir að tilkynning er send á upphaflegan aðila vegna hafnaðs vinnuliðar og aðskilin tilkynning send á notandann sem fær úthlutaðan nýja vinnuliðinn „beiðni um breytingu“. 

Hver tilkynning er fyrir mismunandi vinnulið, en líkindin geta valdið ruglingi. Við erum að skoða leiðir til að bæta þetta í framtíðarútgáfu.

## <a name="why-are-my-workflow-exports-failing"></a>Afhverju eru útflutningar á verkflæðum að mistakast?
Sem stendur eru takmörk á eiginleikanum fyrir útflutning verkflæðis sem koma í veg fyrir að heiti verkflæða séu lengri en 48 stafir. Að nota heiti sem er lengra en 48 stafir getur leitt til villunnar „Þjónn gat ekki sannvottað beiðnina“ og/eða komið í veg fyrir að skrá verði flutt út án skráargerðar. Eftirfarandi bloggfærsla veitir frekari upplýsingar [Úrræðaleit fyrir útflutning verkflæðis](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Getur sendandi verkflæðis einnig samþykkt verkflæðið?
Já, sendandi verkflæðis getur einnig samþykkt verkflæðið ef það er stillt þannig. Til að koma í veg fyrir þessa hegðun skaltu stilla **Færibreytur verkflæðis > Almennar > Samþykktaraðili > Afturkalla heimild innsendingaraðila** á **Já**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Get ég bætt við viðvörunum í verkflæði til að veita notendum tilkynningar?
Hér eru nokkrur lykilatriði til að hafa í huga varðandi viðbót viðvarana í verkflæði til að veita tilkynningar:
- Viðvörun á móti kerfum verkflæðistilkynninga
    - Hægt er að setja upp viðvörun fyrir skráarbreytingar. Verkflæði breyta skrám, þannig að hægt er að setja upp viðvörun sem tengist skráarskiptum vegna verkflæðis. Hins vegar, þar sem verkflæða hafa mismunandi innbyggða tilkynningavalkosti er notkun viðvarana ekki tilvalin.
- Staðlaðar tilkynningar úr verkflæði 
    - Verkflæði hafa innbyggðar tilkynningar í tölvupósti. Viðskiptavinur getur stillt tilkynningarnar þannig að notendum sé sendur tölvupóstur. Þessar tilkynningar leiða ekki til skilaboða úr aðgerðarmiðstöð fyrir notendur.
    - Í framtíðaruppfærslu munum við bæta við skilaboðum aðgerðarmiðstöðvar þannig að notanda sé úthlutað verkflæði. 
- Tilkynningum bætt við verkflæði
    - Skilaboð aðgerðarmiðstöðvar geta verið stofnuð fyrir tiltekna notendur, eins og silkaboð stofnuð í verkflæði í X ++.
    - [Verkflæði hafa viðskiptatilvik](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) sem viðskiptavinurinn gæti notað til að kveikja á flæði, hafa þær tilkynningar sem þeir leita að.   

Í stuttu máli, ef notandi fær ekki rétta tilkynningu frá aðgerðamiðstöðinni þegar honum er úthlutað verkflæðisliður, þá notar hann [Viðskiptatilvik verkflæðis](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) með Microsoft Flow til að veita viðbótar eða mismunandi tilkynningar.
