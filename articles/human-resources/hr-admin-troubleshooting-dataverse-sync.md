---
title: Endurstilla Dataverse samstillingu
description: Þetta efnisatriði lýsir því hvernig hægt er að úrræðaleita færslur sem samstillast ekki á réttan hátt milli Microsoft Dynamics 365 Human Resources og lausn Human Capital Management (HCM) Common í Microsoft Dataverse.
author: jaredha
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-27
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: d88f538fbf22313feaca6771b7cb1757a3c3fbad
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559655"
---
# <a name="reset-dataverse-synchronization"></a>Endurstilla Dataverse samstillingu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Gefa út

Færslur eru ekki samstilltar milli Microsoft Dynamics 365 Human Resources og einingunum í lausn Human Capital Management (HCM) Common í Microsoft Dataverse. Nánari upplýsingar um samstillingu er að finna í [Skilgreina Dataverse samþættingu](hr-admin-integration-common-data-service.md). Samstilling getur misheppnast þegar runuvinnslurnar **Endurtekin tilraun Dataverse-samþættingar** eða **Samstilling ósvaraðra beiðna Dataverse-samþættingar** eru fastar í stöðunni **Í gangi**.

## <a name="resolution"></a>Upplausn

Þegar runuvinnslurnar **Endurtekin tilraun Dataverse-samþættingar** eða **Samstilling ósvaraðra beiðna Dataverse-samþættingar** eru fastar í stöðunni **Í gangi** eða **Hættir við** er hægt að endurstilla stöðuna. Þetta er hægt að gera með því að hætta við runuvinnsluna með því að fylgja leiðsögninni í [Endurstilla fastar runuvinnslur](hr-admin-troubleshooting-batch-execution.md). Eftir að hætt hefur verið við runuvinnslu er hægt að endurstilla runuvinnsluna með því að setja hana í stöðuna **Í bið**. Runuvinnslan keyrir þá á næsta áætlaða keyrslutíma.

1. Ef þú hefur ekki þegar gert það skaltu virkja eiginleikann **Ítarleg runuafturköllun** í **Eiginleikastjórnun**.
   1. Farðu á síðuna **Eiginleikastjórnun** (**Kerfisstjórnun** > **Samantekt** > **Eiginleikastjórnun**).
   2. Veldu flipann **Allt**.
   3. Veldu dálkinn **Heiti eiginleika** og síaðu eftir **Ítarlegri runuafturköllun**.
   4. Hafi slíkt ekki þegar verið virkjað skaltu velja aðgerðina **Virkja**.

2. Slökktu á Dataverse-samþættingunni.
   1. Farðu á síðuna **Microsoft Dataverse-samþætting** (**Kerfisstjórnun** farðu í **Tenglar** > **Samþættingar** > **Dataverse skilgreining**).
   2. Stilltu **Virkja Dataverse-samþættingu** á **Nei**.

3. Hætta við runuvinnsluna **Reyna Dataverse samþættingu aftur**.
   1. Opnaðu síðuna **Runuvinnslur** (**Kerfisstjórnun** farðu í **Tenglar** > **Runuvinnslur** > **Runuvinnslur**).
   2. Síaðu dálkinn **Starfslýsing** eftir **Samþættingu**.
   3. Veldu runuvinnsluna **Reyna Dataverse samþættingu aftur**.
   4. Á aðgerðarborðanum skal velja **Runuvinnsla**, **Þvinga afturköllun** og síðan velja **Já** til að staðfesta.

   > [!NOTE]
   > Það fer eftir því hvenær samþættingin var fyrst virkjuð hvort runuvinnslan sé með lýsinguna **Endurtekin tilraun Common Data Service-samþættingar**. Veldu þessa runuvinnslu ef hún er gefin upp í staðinn fyrir runuvinnsluna **Endurtekin tilraun Dataverse-samþættingar**.

4. Eyða öllum Dataverse samþættingarrunuvinnslum.
   1. Á síðunni **Runuvinnslur** skal velja runuvinnslurnar **Samstilling ósvaraðra beiðna Dataverse-samþættingar**, **Endurtekin tilraun Dataverse-samþættingar** og **Upphafleg samstilling Dataverse-samþættingar**.
   2. Á aðgerðaborðanum skal velja aðgerðina **Breyta stöðu**. 
   3. Veljið **Staðgreiðsla** og svo **Í lagi**.
   4. Á aðgerðaborðanum skal velja aðgerðina **Eyða** og síðan velja **Já** til að staðfesta aðgerðina.

5. Kveikið á Dataverse samþættingarrunuvinnslunum.
   1. Farðu á síðuna **Microsoft Dataverse-samþætting** (**Kerfisstjórnun** > **Tenglar** > **Samþætting** > **Dataverse skilgreining**).
   2. Stilltu **Virkja Dataverse-samþættingu** á **Já**.

6. Farðu á síðuna **Runuvinnslur** og staðfestu að runuvinnslurnar **Endurtekin tilraun Dataverse-samþættingar** og **Samstilling ósvaraðra beiðna Dataverse-samþættingar** hafi verið stofnaðar.

Með runuvinnslurnar stofnaðar að nýju getur þú nú fylgst með runuvinnslunni **Endurtekin tilraun Dataverse-samþættingar** til að sjá hversu lengi vinnslan er í framkvæmd. Þú getur síðan staðfest að færslurnar séu að samstillast rétt við lausn HCM Common í Microsoft Dataverse.

## <a name="see-also"></a>Sjá einnig

[Skilgreina Dataverse-samþættingu](hr-admin-integration-common-data-service.md)<br>
[Endurstilla fastar runuvinnslur](hr-admin-troubleshooting-batch-execution.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]