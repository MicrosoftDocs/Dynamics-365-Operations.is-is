---
title: Skipulagning viðtala og ábendingar
description: Þetta efnisatriði veitir upplýsingar um skipulagningu viðtala og ábendingar í Attract.
author: ''
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: hasrivas
ms.openlocfilehash: 7bc5a66bb221cb0ab2c69fcb1013ed48a7c664a6
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2019
ms.locfileid: "374919"
---
# <a name="interview-scheduling-and-feedback"></a>Skipulagning viðtala og ábendingar

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Tímáætlunaraðgerð

Tímaáætlunaraðgerðin er valfrjáls og er með tvo þætti: Beiðni um tímaupplýsingar umsækjanda og tímaáætlun. Tímaupplýsingar umsækjanda leyfir þér að nota tölvupóst til að biðja um tímaupplýsingar umsækjanda. Tímaáætlunin veitir möguleika á að skipuleggja viðtöl við umsækjanda og ráðningarteymið.

### <a name="candidate-availability-request"></a>Beiðni um tímaupplýsingar umsækjanda

Til að senda tölvupóst til umsækjenda til að biðja um tímaupplýsingar þeirra skal velja reitinn **Biðja um tímaupplýsingar umsækjanda**. Ef reiturinn er ekki valinn, birtist þetta skref ekki í ráðningarferlinu fyrir starfið.

Til að senda beiðni um tímaupplýsingar skal smella á **Senda beiðni**, velja tiltækar dagsetningar og sniðmát fyrir tölvupóst, og síðan senda póstinn á umsækjandann.

[![Yfirlit Attract-ráðningaraðila til að senda beiðni um tímaupplýsingar umsækjanda](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Þegar umsækjandinn fær tölvupóst til að bregðast við beiðninni, getur hann skráð sig inn á gátt umsækjanda, valið dagsetningar sem henta honum og smellt á **Senda inn**.

### <a name="schedule"></a>Áætlun
Það eru margar skilgreiningar í boði fyrir þann sem tímasetur viðtal og hann getur stofnað og sent viðtalsmengið á spyrlana og umsækjanda á fljótlegan hátt.

1. Smelltu á **Stofna tímasetningu** og í kassanum **Bæta við spyrlum** skal tilgreina alla spyrlana sem koma til með að vera hluti af viðtalsmenginu.
[![Yfirlit Attract-ráðningaraðila til að hefja tímaáætlun á viðtalsmengi](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Ef umsækjandinn brást við tímaupplýsingum viðtalsbeiðninnar verður reiturinn **Dagsetning viðtals** þegar útfylltur af honum. Hægt er að velja aðra dagsetningu ef þörf er á.
    
    Ef þú velur reitinn **Gera þetta að viðtalssvæði** verður viðtalshópurinn vinstra megin færður í stakt mengjasvæði til að stofna viðtalið. Þá verður þú að skilgreina tiltekna röð fyrir viðtölin.
    
    Haga ætti tímaáætlun viðtals þannig að hún passi best tímaáætlun þátttakandans. Ef þetta er umsækjandi innan fyrirtækis er hægt taka með í reikninginn hvenær hann er laus sem hluti af ráðleggingu um tímaáætlun.
    
    Til að halda fund á netinu skal velja reitinn **Bæta við Skype-fundum** og hvert viðtalstilvik verður með tiltækan tengil fyrir **Skype for Business**.

2. Veldu lengd viðtals fyrir hvert viðtalstilvik og smelltu síðan á **Í lagi** til að búa til tímaáætlunina.

    Ef **Ráðleggingar** er valið, verða ráðleggingar sýndar og hnitanet viðtals verður fyllt út. Hægt verður að sjá tiltækileika á núverandi dagatali fyrir alla valda spyrla. Einnig verður hægt að skoða dagatal umsækjanda ef hann er innan fyrirtækis.

3. Ef engar tillögur eru tiltækar, í dálknum **Spyrlar**, skal færa inn tímasetningu, gefa upp titil viðtals, upplýsingar og fylla út upplýsingar um staðsetningu eftir þörfum. Hægt er að velja að hafa með tengilinn **Skype for Business** fyrir viðtalið.

4. Til að bæta við fleiri spyrlum skal smella á hnitanetsdálkinn **Bæta við viðtali** til að velja einn eða fleiri spyrla. Hægt er að nota úrfellingarvalkostinn (...) til að fjarlægja viðtal úr menginu.
    
5. Ef viðtölin eru tímasett í öðru tímabelti skal velja viðeigandi borg/tímabelti úr fellilistanum efst hægra megin. Hnitanet yfir lausan tíma spyrils verður uppfært til að endurspegla nýja tímabeltið. Þetta val á tímabelti verður nú einnig birt í yfirlitinu **Samantekt viðtals**, sem verður deilt með spyrlum og umsækjanda. 

6. Smelltu á **Senda til spyrla** til að senda fundarboðin á spyrla sem hlut eiga að máli.

    Eftir að viðtalsbeiðnirnar hafa verið sendar á spyrlana, geta þeir svarað beint í gegnum tölvupóstsboðið sem þeir fengu.

    >[!NOTE]
    > Áminningar eru sendar á spyrla á sólarhringsfresti fyrir einstaklingsviðtöl ef spyrillinn hefur ekki svarað (samþykkt eða hafnað) viðtalsbeiðninni.

    > Fyrir nefndarviðtöl eru engar sjálfvirkar áminningar fyrir viðtalsbeiðnina. Til að kveikja á áminningu handvirkt skal breyta viðtali og nota valkostinn **Uppfæra og senda** til að senda beiðnina aftur á spyrlana.

    Viðbrögð spyrils eru sótt og sýnd í Attract. Ef spyrill hafnar boðinu, berst þér tilkynning um að gera breytingu. Til að skoða svör þeirra í hnitaneti yfirlitsins **Áætlanagerð** skal smella á blöðrutáknið.

[![Yfirlit Attract-ráðningaraðila yfir svör spyrils](./media/schedule-interviewer-response.png)](./media/schedule-interviewer-response.png)

7. Eftir að viðtalsáætlun er tilbúin til að vera deild með umsækjanda skal smella á **Senda til umsækjanda**. Hægt er að velja um að fela eða sýna spyrlinum nöfn og tíma með umsækjandanum.

8. Veldu sniðmát tölvupósts og sendu samantekt viðtals til umsækjanda. Umsækjandinn getur skoðað þessar upplýsingar í tölvupósti sínum sem og í umsækjendagáttinni.
    
>[!NOTE] 
> Dagatal yfir lausan tíma umsækjanda er einungis sýndur ef umsækjandinn er innan fyrirtækis. Á sama hátt má aðeins nota umsækjanda innan fyrirtækis til að bæta ráðleggingar spyrils um tímasetningar. Sem stendur fá umsækjendur (innan og utan fyrirtækis) ekki tölvupóst með fundarboði. Í staðinn fær umsækjandinn aðeins samantekt viðtalanna.

## <a name="feedback-activity"></a>Endurgjafaraðgerð

Endurgjafaraðgerð er valfrjáls í starfssniðmáti. Þessi aðgerð gerir þátttakendum í viðtali kleift að setja inn tillögur eða endurgjöf fyrir umsækjanda. Ef reiturinn **Erfa þátttakendur sem gefa ábendingar frá ráðningarhópi** er valinn, er ráðningaraðilinn, mannauðsstjórinn og spyrlar sjálfkrafa færðir inn í endurgjafaraðgerðina. Fyrirtæki geta leyft spyrlum að skoða endurgjöf annarra áður en þeir leggja inn eigin endurgjöf. Fyrirtæki geta einnig leyft spyrlum að breyta viðbrögðunum sínum eftir að þeir hafa sent það inn. Spyrlar eru minntir á að senda inn endurgjöf fyrir viðtalið sem þeir tóku nýlega sem byggist á fyrirfram stilltri skilgreiningu sem hluti af starfssniðmátinu. Ráðningarstjóri eða ráðningaraðili starfsins getur einnig valið að minna spyril handvirkt á að senda inn endurgjöf.

## <a name="interview-activity"></a>Viðtalsaðgerðir

Viðtalsaðgerðin er valfrjáls aðgerð sem inniheldur þrjá þætti: Beiðni um tímaupplýsingar umsækjanda, áætlun og endurgjöf. Notaðu viðtalsaðgerðina í starfssniðmátinu ef þú vilt allar beiðnir um tímaupplýsingar umsækjanda, áætlun. og endurgjöf sem hluti af ferlinu í staðinn fyrir að nota þá fyrir hvert tilfelli fyrir sig sem hluta af ráðningarferlinu.