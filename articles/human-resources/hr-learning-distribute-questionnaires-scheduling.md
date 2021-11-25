---
title: Dreifa spurningalistum með áætlanagerð
description: Röðun spurningalista er hægt að nota til að áætla og dreifa spurningalistum á marga svarendur.
author: twheeloc
ms.date: 10/28/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2336cafe7e2c914c2592c91c888b1e0ae1bc608
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728677"
---
# <a name="distribute-questionnaires-using-scheduling"></a>Dreifa spurningalistum með áætlanagerð

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Röðun spurningalista er hægt að nota til að áætla og dreifa spurningalistum á marga svarendur. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.

## <a name="create-a-questionnaire-schedule"></a>Stofna áætlun spurningalista

1. Fara til **Spurningalisti** > **Dreifa** > **Áætlanir spurningalista**.

2. Smellt er á **Nýtt**.

3. Í **Tímasetningar** reit, sláðu inn gildi.

4. Í reitinn **Lýsing** skal slá inn gildi.
    * Stilltu áætlunina á **Nafnlaus** ef skrá ætti svör án nöfnum tengdum svarinu.  
    * Leyfa nafnlausar niðurstöður verður fyrst að setja upp í færibreytum Mannauður.  

5. Í **Gerð** reit, veldu áætlanagerð.  Í þessu dæmi munum við nota **Ánægja** gerð.

6. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

7. Í listanum skal smella á tengilinn í valinni línu.

8. í retinum **Dagsetning** ritarðu dagsetningu.

9. Stækkaðu **Tölvupóstur fyrir sjálfsafgreiðslu starfsmanna** kafla.

10. Í reitinn **Efni** skal slá inn gildi.

    * Dæmi: Tiltæka Spurningalista  

11. Í **Texti** reit, sláðu inn meginmál tölvupóstskeytisins. Athugið að hægt er að neyta breytuna til að skipta út gildum í kerfinu.

    * Dæmi: Hæ %P%, Vinsamlegast skráðu þig inn í Sjálfsafgreiðsla Starfsmanns til að ljúka spurningalistanum heilbrigði Vinnuafls.  Contoso  

12. Smelltu á **Vista**.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>Nota upplýsingar um Uppsetningu til að velja spurningalista sem á að svara auk hvaða fyrirspurnir á að nota til að velja svarendur.

1. Smellur **Upplýsingar um uppsetningu**.

2. Í listanum skal finna spurningalista til að nota til að finna svarendur fyrir spurningalistann.

    * Dæmi: Starfsmenn  

3. Smellur **Skoða eða breyta fyrirspurn** til að velja tiltekið fólk eða stilla fyrirspurnina til að finna fólk sem passar við ákveðin skilyrði.

    * Athugið að allir svarendur verður einnig að vera notendur kerfisins.  

4. Í listanum, merktu línuna fyrir Persónu.

5. Í reitinn **Skilyrði** skal slá inn eða velja gildi.

    * Velja Julia Funderburk  

6. Veldu Julia Funderburk í listanum.

7. Smellt er á **OK**.

8. Smelltu á **Spurningalistar** flipa.

9. Í trénu skaltu stækka hnútinn fyrir gerð spurningalista **Ánægjukönnun**.

10. Í trénu skal mekja við "heilbrigðisskoðun vinnuafls".

11. Smellt er á **OK**.

12. Smellur **Fyrirhugaður svarfundur**.

    * Athugið að **Fyrirhugaðir svartímar** hafa verið búnar til fyrir hvern valinn/fyrirspurður notanda.  

13. Lokið síðunni.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>Hefja áætlun spurningalista til að gera spurningalista tiltæka fyrir svarendur til að ljúka.

1. Smelltu á **Aðgerðir**.

2. Smellt er á **Byrja**.

3. Smellt er á **OK**.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>Senda tölvupóst til að tilkynna svarendum um tiltæka spurningalista.

1. Smelltu á **Aðgerðir**.

2. Smellur **Senda tölvupóst**.

3. Smelltu á **Hætta við**.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Notið Áætlaðar svarsetur til að fylgjast með hver þarf að ljúka spurningalistanum.

1. Smellur **Fyrirhugaður svarfundur**.

    * Eyðið öllum eftirstandandi áætluðum svarsetum þegar er verið að ljúka áætlaðri svarsetu.  

2. Smellið á **Eyða**.

3. Smellið á **Já**.

4. Lokið síðunni.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Þegar tekið hefur verið á móti öllum svörunum er hægt að ljúka áætlun og/eða þegar búið er að eyða öllum eftirstandandi svarsetum.

1. Smelltu á **Aðgerðir**.
2. Smellur **Enda**.
3. Smellt er á **OK**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
