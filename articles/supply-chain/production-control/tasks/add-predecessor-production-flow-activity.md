---
title: Bæta forvera við framleiðsluflæðisverkþátt
description: Í framleiðsluflæðisútgáfu, verður að vera raðaðar öllum verkþáttum.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9036c33cfea590148bb74de026410ecdb8ce9fbc516489ccb2f864ca8c0dd0bc
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715699"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a>Bæta forvera við framleiðsluflæðisverkþátt

[!include [banner](../../includes/banner.md)]

Í framleiðsluflæðisútgáfu, verður að vera raðaðar öllum verkþáttum. Aðgerð getur haft eitt eða mörg forvera eða arftaka. 

Þessi verklýsing sýnir hvernig á að tengja forvera við verkþætti. 

Til að framkvæma þetta verk, Þú þarft framleiðsluflæði sem hefur drög að útgáfu með að minnsta kosti tvær aðgerðir sem má tengja. 

Nánari upplýsingar, sjá hvítbókina með yfirskriftinni "Framleiðsluflæði og verkþættir í Lean-framleiðslu."


## <a name="find-the-production-flow-and-version"></a>Finndu útgáfu og framleiðsluflæði
1. Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
5. Smellt er á Verkþætti.

## <a name="select-an-activity-and-add-a-predecessor"></a>Veldu verkþátt og bæta við forvera
1. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
2. Smelltu á Bæta við forvera.
3. Í reitinn verkþáttur skal slá inn eða velja gildi.
4. Færið inn tölu í reitnum Hlutfall ferlistíma.
    * Sjálfgefið hlutfall ferlistíma fyrir verkþáttarvensl er 1. Þetta gerir ráð fyrir að báðir verkþættir keyri á sama hraða eða framleiðslutími á einingu. Ef forveri keyrir á hærra hraða (lægri framleiðslutími á einingu), ætti hlutfall að vera lægri en 1, ef forveri keyrir á hægari hraða (hærri framleiðslutími á einingu) er hlutfall ferlistíma hærri en 1.  
5. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]