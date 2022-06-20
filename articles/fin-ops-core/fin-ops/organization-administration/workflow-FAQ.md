---
title: Algengar spurningar um verkflæði
description: Þessi grein svarar algengum spurningum um verkflæðiskerfið.
author: ChrisGarty
ms.date: 03/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a72fd141bb1178a3a83385c512d1a655064d5b00
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896580"
---
# <a name="workflow-faq"></a>Algengar spurningar um verkflæði

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Þessi grein svarar algengum spurningum um verkflæðiskerfið.

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a>Hvers vegna koma margar tilkynningar þegar vinnulið er hafnað?
Þegar vinnulið er hafnað er honum lokið sem höfnuðum. Annar vinnuliður er stofnaður og honum er úthlutað á upphaflegan aðila. Þetta þýðir að tilkynning er send á upphaflegan aðila vegna hafnaðs vinnuliðar og aðskilin tilkynning send á notandann sem fær úthlutaðan nýja vinnuliðinn „beiðni um breytingu“. 

Hver tilkynning er fyrir mismunandi vinnulið, en líkindin geta valdið ruglingi. Við erum að skoða leiðir til að bæta þetta í framtíðarútgáfu.

## <a name="why-are-my-workflow-exports-failing"></a>Afhverju eru útflutningar á verkflæðum að mistakast?
Sem stendur eru takmörk á eiginleikanum fyrir útflutning verkflæðis sem koma í veg fyrir að heiti verkflæða séu lengri en 48 stafir. Að nota heiti sem er lengra en 48 stafir getur leitt til villunnar „Þjónn gat ekki sannvottað beiðnina“ og/eða komið í veg fyrir að skrá verði flutt út án skráargerðar. Eftirfarandi bloggfærsla veitir frekari upplýsingar, [Úrræðaleit fyrir útflutning verkflæðis](https://community.dynamics.com/365/financeandoperations/b/elandaxdynamicsaxupgradesanddevelopment/posts/workflow-export-troubleshooting).

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a>Getur sendandi verkflæðis einnig samþykkt verkflæðið?
Já, sendandi verkflæðis getur einnig samþykkt verkflæðið ef það er stillt þannig. Til að koma í veg fyrir þessa hegðun skaltu stilla **Kerfisstjórnun > Verkflæði > Færibreytur verkflæðis > Almennar > Samþykktaraðili > Afturkalla heimild innsendingaraðila** á **Já**.

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a>Get ég bætt við viðvörunum í verkflæði til að veita notendum tilkynningar?
Hér eru nokkrur lykilatriði til að hafa í huga varðandi viðbót viðvarana í verkflæði til að veita tilkynningar:
- Viðvörun á móti kerfum verkflæðistilkynninga
    - Hægt er að setja upp viðvörun fyrir skráarbreytingar. Verkflæði breyta skrám, þannig að hægt er að setja upp viðvörun sem tengist skráarskiptum vegna verkflæðis. Hins vegar, þar sem verkflæða hafa mismunandi innbyggða tilkynningavalkosti er notkun viðvarana ekki tilvalin.
- Staðlaðar tilkynningar úr verkflæði 
    - Verkflæði hafa innbyggðar tilkynningar í tölvupósti. Viðskiptavinur getur stillt tilkynningarnar þannig að notendum sé sendur tölvupóstur. Þessar tilkynningar leiða ekki til skilaboða úr aðgerðarmiðstöð fyrir notendur.
    - Í framtíðaruppfærslu munum við bæta við skilaboðum aðgerðarmiðstöðvar þannig að notanda sé úthlutað verkflæði. 
- Tilkynningum bætt við verkflæði
    - Skilaboð aðgerðarmiðstöðvar geta verið stofnuð fyrir tiltekna notendur, eins og silkaboð stofnuð í verkflæði í X ++.
    - [Verkflæði hafa viðskiptatilvik](../../dev-itpro/business-events/business-events-workflow.md) sem viðskiptavinurinn gæti notað til að kveikja á flæði, hafa þær tilkynningar sem þeir leita að.   

Tekið saman, ef notandi fær ekki rétta tilkynningu frá Aðgerðamiðstöð þegar þeim er úthlutað vinnulið verkflæðis, skal nota [Viðskiptatilvik verkflæðis](../../dev-itpro/business-events/business-events-workflow.md) með Microsoft Power Automate til að veita frekari eða aðrar tilkynningar.

## <a name="why-is-workflow-editor-not-able-to-start-under-ad-fs"></a>Af hverju er ritstjórinn á verkflæðinu ekki fær um að byrja undir AD FS?
Þegar keyrt er undir Active Directory Federation Services (AD FS) í uppfærðu umhverfi, getur ritstjórinn á verkflæðinu átt í vandræðum með að byrja. Ef það gerist skaltu passa að slóðinni „https://dynamicsaxworkfloweditor/" hafi verið bætt við eiginleikann **Microsoft Dynamics 365 for Operations Innanhúss - Vinnuflæði - Native forrit** í ADFS-stillingum.

## <a name="why-am-i-getting-sql-deadlocks-on-workflow-processing"></a>Af hverju fæ ég SQL sjálfheldu við vinnsluflæðisvinnslu? 
Sjálfgefna reitgildið fyrir **Fjöldi verkflæðisatriða á runu** á síðunni **Færibreytur verkflæðis** er 0. Gildi 0 veldur því að sjálfgefið breytist í 20 hluti í hverri runu. Vertu varkár þegar þú stillir þetta gildi vegna þess að mikill fjöldi atriða í hverri runu (> 40) getur valdið SQL sjálfheldum.

## <a name="what-is-the-workflow-enhanced-error-feature"></a>Hvað er eiginleiki Aukinnar villu í verkflæði?
Eiginleikinn Aukin villa í verkflæði í útgáfu 10.0.13 bætir við villukóðum til að aðgreina mismunandi klasa af verkflæðissvillum. Villuboðin sem gefin voru upp verða að mestu leyti svipuð með minniháttar frávikum til að gera þau skýrari.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
