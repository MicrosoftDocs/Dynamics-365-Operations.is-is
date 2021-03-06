---
title: Dreifa spurningalistum með áætlanagerð
description: Röðun spurningalista er hægt að nota til að áætla og dreifa spurningalistum á marga svarendur.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 952048ce0a2ac94be70d7bde0dc52610f19151ed
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056301"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Dreifa spurningalistum með áætlanagerð

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Röðun spurningalista er hægt að nota til að áætla og dreifa spurningalistum á marga svarendur. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.

## <a name="create-a-questionnaire-schedule"></a>Stofna áætlun spurningalista

1. Fara í Spurningalista > Dreifa > Áætlanir Spurningalista.

2. Smellið á „Nýtt“.

3. Í reitinn Áætlun skal slá inn gildi.

4. Sláið inn gildi í reitnum „Lýsing“.
    * Stilla áætlun á Nafnlaus ef það á að skrá svörin án þess að tengja þau nafni.  
    * Leyfa nafnlausar niðurstöður verður fyrst að setja upp í færibreytum Mannauður.  

5. Í reitnum Tegund er gerð áætlunar valin.  Í þessu dæmi munum við nota Ánægju-gerð.

6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

7. Í listanum skal smella á tengilinn í valinni línu.

8. Dagsetning er rituð í reitinn Dagetning.

9. Stækka hlutann Tölvupóstur fyrir sjálfsafgreiðslu starfsmanna.

10. Í reitinn Efni skal slá inn gildi.

    * Dæmi: Tiltæka Spurningalista  

11. Meginmál tölvupóstskilaboða skal slá inn í svæðið Texti. Athugið að hægt er að neyta breytuna til að skipta út gildum í kerfinu.

    * Dæmi: Hæ %P%, Vinsamlegast skráðu þig inn í Sjálfsafgreiðsla Starfsmanns til að ljúka spurningalistanum heilbrigði Vinnuafls.  Contoso  

12. Smelltu á Vista.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Nota upplýsingar um Uppsetningu til að velja spurningalista sem á að svara auk hvaða fyrirspurnir á að nota til að velja svarendur.

1. Smellið á Upplýsingar um uppsetningu.

2. Í listanum skal finna spurningalista til að nota til að finna svarendur fyrir spurningalistann.

    * Dæmi: Starfsmenn  

3. Smellið á Skoða eða breyta fyrirspurn til að velja ákveðna einstaklinga eða lagfæra fyrirspurnina til að finna einstaklinga sem passa við sérstök skilyrði.

    * Athugið að allir svarendur verður einnig að vera notendur kerfisins.  

4. Í listanum skal merkja línu fyrir einstakling

5. Í reitinn Skilyrði skal slá inn eða veldu gildi.

    * Velja Julia Funderburk  

6. Veldu Julia Funderburk í listanum.

7. Smellið á „Í lagi“.

8. Smellið á flipann Spurningalisti.

9. Í trénu, útvíkkið hnútinn fyrir gerð spurningalista af gerðini ánægjukönnun.

10. Í trénu skal mekja við "heilbrigðisskoðun vinnuafls".

11. Smellið á „Í lagi“.

12. Smellið á Áætluð svarseta.

    * Athugið að Áætlaðar svarsetur hafa verið stofnaðar fyrir hvern notanda sem hefur verið valinn eða fengið fyrirspurn.  

13. Lokið síðunni.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Hefja áætlun spurningalista til að gera spurningalista tiltæka fyrir svarendur til að ljúka.

1. Smellið á Aðgerðir.

2. Smellið á „Byrja“.

3. Smellið á „Í lagi“.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Senda tölvupóst til að tilkynna svarendum um tiltæka spurningalista.

1. Smellið á Aðgerðir.

2. Smellið á Senda tölvupóst.

3. Smellið á Hætta við.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Notið Áætlaðar svarsetur til að fylgjast með hver þarf að ljúka spurningalistanum.

1. Smellið á Áætluð svarseta.

    * Eyðið öllum eftirstandandi áætluðum svarsetum þegar er verið að ljúka áætlaðri svarsetu.  

2. Smellið á Eyða.

3. Smella á Já.

4. Lokið síðunni.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Þegar tekið hefur verið á móti öllum svörunum er hægt að ljúka áætlun og/eða þegar búið er að eyða öllum eftirstandandi svarsetum.

1. Smellið á Aðgerðir.
2. Smellt er á Ljúka.
3. Smellið á „Í lagi“.



[!INCLUDE[footer-include](../includes/footer-banner.md)]