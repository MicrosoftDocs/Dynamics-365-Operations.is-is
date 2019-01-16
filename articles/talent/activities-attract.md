---
title: "Aðgerðir í ferlunum"
description: "Þetta efnisatriði gefur upplýsingar um ýmis konar aðgerðir sem hægt er að nota í ráðningarferlinu."
author: 
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: be66d9f95551066bb8bc25445c652d4fa59066d4
ms.openlocfilehash: 4f59193991420fd9ec05a83049e569058bf81932
ms.contentlocale: is-is
ms.lasthandoff: 12/07/2018

---

# <a name="activities-in-the-hiring-processes"></a>Aðgerðir í ráðningarferlunum

[!include[banner](../includes/banner.md)]

Aðgerðum má bæta við sem hluti af ráðningarferlinu í Microsoft Dynamics 365 for Talent: Attract. Aðgerðum má bæta við sniðmát ferlis, eða hægt er að bæta þeim beint við ráðningarferlið í starfi. Þegar starf er skilgreint er sniðmát ferlis valið og aðgerðir sem er innifalinn í sniðmátið er beitt í starfið. Ef sniðmát er ekki valið er sjálfgefið sniðmát notað. Ráðningarferlið er einnig hægt að breyta í starfi eftir að sniðmátið er beitt.

> [!NOTE] 
> Felissniðmát eru fáanlegar með Viðbót við alhliða ráðningar.

## <a name="prospect-activity"></a>Aðgerð fyrir viðfang

Aðgerð fyrir viðfang stýrir hvort viðföngum getur verið bætt við starf. Sjálfgefið er að hægt sé að bæta viðföngum við starf. Til að slökkva á aðgerð fyrir viðföng skaltu stilla **Virkja viðföng** valkostinn á **Slökkt**. Þegar kveikt er á aðgerð fyrir viðföng, geta mannauðsstjórar bætt við og skoðað viðföng og **Viðföng** flipinn er sýndur í starfinu.

## <a name="application-activity"></a>Umsóknaraðgerð

Umsóknaraðgerðar er krafist í sniðmát ráðningarferlisins. Til að senda tölvupóst til umsækjenda þegar þeir leggja inn umsóknina eða eru bætt við umsóknarstigið skaltu stilla **Senda póst til umsækjanda** valkosts til **Á**.

## <a name="scheduler-activity"></a>Tímáætlunaraðgerð

Tímaáætlunaraðgerðin er valfrjáls. Þessi aðgerð hefur tvö þætti: Tímaupplýsingar umsækjanda og tímaáætlun. Tímaupplýsingar umsækjanda leyfir þér að nota tölvupóst til að biðja um tímaupplýsingar umsækjanda. Tímaáætlunin veitir möguleika á að skipuleggja viðtöl við umsækjanda og ráðningarteymið. Í tímaáætlunaraðgerðinni, eftirfarandi valkosti er hægt að stilla: **Biðja um tímaupplýsingar umsækjanda**, **Netfund** og **Senda póst til umsækjanda**.

- Til að senda tölvupóst til umsækjenda til að biðja um tímaupplýsingar þeirra, stilltu **Biðja um tímaupplýsingar umsækjanda** á **Á**. Ef þú stillir kost á **Slökkva**, verður þetta skref ekki sýnt í ráðningarferlinu í starfinu.
- Til að streyma í beinni eða hafa símafund með því að nota Skype for Business skaltu stilla **Netfund** reitinn á **Skype for Business**. Réttur **Taka þátt í Skype-fundi** tengilinn verður síðan bætt við í viðstalsboðið sem er sent til umsækjenda.
- Til að senda tölvupóst til umsækjenda til að ljúka tímaáætluninni skaltu stilla **Senda póst til umsækjanda** valkostur til **Á**. Ef þú stillir kost á **Slökkva**, fá umsækjendur aðeins viðtalsáætlunina þegar þeir skrá sig inn á umsækjendagáttina.

## <a name="feedback-activity"></a>Endurgjafaraðgerð

Endurgjafaraðgerð er valfrjáls. Þessi aðgerð gerir þátttakendum í viðtali kleift að setja inn tillögur að umsækjanda. Þeir geta einnig slegið inn endurgjöf við athugasemdir sem þeir hafa. Ef þú kveikir á **Erfa þátttakendur sem gefa ábendingar frá ráðningarhópi** valkostinum, er ráðningaraðilinn, mannauðsstjórinn og spyrlar sjálfkrafa færðir inn í endurgjafaraðgerðina. Fyrirtæki geta leyft spyrlum að skoða endurgjöf annarra áður en þeir leggja inn eigin endurgjöf. Fyrirtæki geta einnig leyft spyrlum að breyta viðbrögðunum sínum eftir að þeir hafa sent það inn.

## <a name="interview-activity"></a>Viðtalsaðgerðir

Viðtalsaðgerðir eru valfrjálsar. Þessi aðgerð hefur þrjá þætti: Tímaupplýsingar umsækjanda, tímaáætlun og endurgjöf. Tímaupplýsingar umsækjanda leyfir þér að nota tölvupóst til að biðja um tímaupplýsingar umsækjanda. Tímaáætlunin veitir möguleika á að skipuleggja viðtöl við umsækjanda og ráðningarteymið. Í tímaáætlunaraðgerðinni, eftirfarandi valkosti er hægt að stilla: **Biðja um tímaupplýsingar umsækjanda**, **Netfund** og **Senda póst til umsækjanda**.

- Til að senda tölvupóst til umsækjenda til að biðja um tímaupplýsingar þeirra, stilltu **Biðja um tímaupplýsingar umsækjanda** á **Á**. Ef þú stillir kost á **Slökkva**, verður þetta skref ekki sýnt í ráðningarferlinu í starfinu.
- Til að streyma í beinni eða hafa símafund með því að nota Skype for Business skaltu stilla **Netfund** reitinn á **Skype for Business**. Rétt **Taka þátt í Skype-fundi** tengilinn verður síðan bætt við viðtalsbeiðnina.
- Til að senda tölvupóst til umsækjenda til að ljúka tímaáætluninni skaltu stilla **Senda póst til umsækjanda** valkostur til **Á**. Ef þú stillir kost á **Slökkva**, fá umsækjendur aðeins viðtalsáætlunina þegar þeir skrá sig inn á umsækjendagáttina.

>[!NOTE]
> - Áminningar eru sendar á spyrla á sólarhringsfresti fyrir einstaklingsviðtöl ef spyrillinn hefur ekki svarað (samþykkt eða hafnað) viðtalsbeiðninni.
> - Fyrir nefndarviðtöl eru engar áminningar um að svara þurfi viðtalsbeiðni. Til að kveikja á áminningu handvirkt skal breyta viðtali og nota valkostinn **Uppfæra og senda** til að senda beiðnina aftur á spyrlana.

Endurgjafarhluti leyfir fólki að slá inn ráðleggingar fyrir umsækjanda. Þeir geta einnig slegið inn endurgjöf við athugasemdir sem þeir hafa. Ef þú kveikir á **Erfa þátttakendur sem gefa ábendingar frá ráðningarhópi** valkostinum, er ráðningaraðilinn, mannauðsstjórinn og spyrlar sjálfkrafa færðir inn í endurgjafarhlutann. Fyrirtæki geta leyft spyrlum að skoða endurgjöf annarra áður en þeir leggja inn eigin endurgjöf. Fyrirtæki geta einnig leyft spyrlum að breyta viðbrögðunum sínum eftir að þeir hafa sent það inn.

## <a name="powerapps-activity"></a>PowerApps-aðgerð

PowerApps-aðgerðin gerir þér kleift að fella Microsoft PowerApps-forrit inn í ráðningarferlinu þínu. Forritið kann að vera nauðsynlegt fyrir alla umsækjendur, aðeins innri umsækjendur, aðeins ytri umsækjendur eða enga umsækjendur. Ef forritið er merkt sem áskilið verður það að vera lokið áður en stigið getur haldið áfram. Ef forritið er ekki merkt sem áskilið er aðgerðin valfrjáls skref og stigið getur haldið áfram, jafnvel þótt forritið sé ekki lokið.

Til að vista PowerApps-aðgerð í ráðningarferlið verður þú að slá inn PowerApps-kenni. Til að finna PowerApps-kennið, farðu í [PowerApps](https://web.powerapps.com), veldu **Forrit** og veldu síðan **Upplýsingar**.

Ef þú velur **Leyfa að bæta þátttakendum við þessa aðgerð** valkostur, er hægt að bæta öðrum þátttakendum við fyrir forrit sem notar PowerApps-aðgerðina. Til dæmis hefur fyrirtæki búið til PowerApps-forrit sem er safn af viðtalsspurningum fyrir tæknistörf. Fyrirtækið er nú að ráða nýjan forritara og hefur bætt virkni PowerApps aðgerðinni við ráðningarferlið fyrir forritarastarfið. Ef **Leyfa að bæta við þátttakendum fyrir þennan aðgerð** valkostur er valinn, getur ráðningaraðili eða mannauðsstjóri sem er að skoða umsækjanda um forritarastarfið, bætt fólki við PowerApps-aðgerðina. Þessir aðilar geta þá skoðað forritið sem hefur viðtalsspurningarnar.

> [!NOTE]
> PowerApps-aðgerðin er aðeins í boði með Viðbót við alhliða ráðningar.

## <a name="youtube-activity"></a>YouTube-aðgerð

YouTube-aðgerð gerir þér kleift að deila YouTube myndbandi sem hluti af ráðningarferlinu þínu. Til að vista YouTube-aðgerð á ráðningarferlinu verður þú að tilgreina slóðina að YouTube myndbandinu. Hvað varðar PowerApps-aðgerðina geturðu leyft að bæta þátttakendum við aðgerðina. Ef þú velur **Bara sýnilegt umsækjanda** valkostur, er myndbandið aðeins sýnt sem hluti af upplifun umsækjanda. Það er ekki sýnt í ráðningarferlinu í Attract.

> [!NOTE]
> YouTube-aðgerð er aðeins í boði með Viðbót við alhliða ráðningart.

## <a name="web-content-activity"></a>Vefefnisaðgerð

Með vefefnisaðgerð er hægt að fella inn efni á netinu í ráðningarferlinu þínu. Til að vista vefefnisaðgerðina í ráðningarferlinu verður þú að tilgreina vefslóð efnisins. Hvað varðar PowerApps- og YouTube-aðgerðir geturðu leyft að bæta þátttakendum við aðgerðina. Ef þú velur **Bara sýnilegt umsækjanda** valkostur, er aðeins efnið sýnt sem hluti af upplifun umsækjanda. Það er ekki sýnt í ráðningarferlinu í Attract. Þú getur valið stærð efnisins sem birtist.

> [!NOTE]
> Vefefnisaðgerðin er aðeins í boði með Viðbót við alhliða ráðningar.

## <a name="microsoft-forms-activity"></a>Microsoft Forms-aðgerð

Microsoft Forms-aðgerð gerir þér kleift að fella inn Microsoft Forms inn í ráðningarferlinu þínu. Microsoft Forms gerir þér kleift að búa til þekkingarpróf, mat og kannanir. Til að vista virkni Microsoft Forms í ráðningarferlið verður þú að tilgreina vefslóð eyðublaðsins. Hvað varðar PowerApps-, YouTube- og vefefnisaðgerðir getur þú leyft að bæta þátttakendum við aðgerðina. Ef þú velur **Bara sýnilegt umsækjanda** valkostur, er eyðublaðið aðeins sýnt sem hluti af upplifun umsækjanda. Það er ekki sýnt í ráðningarferlinu í Attract.

Í Microsoft Forms geta höfundar breytt stillingum sínum til að láta notendur utan fyrirtækisins svara könnunum eða þekkingarprófum sínum. Í þessu tilfelli, notendur senda inn svar á nafnlausan hátt. Ef þú vilt sjá hver hefur fyllt út könnunina þína eða þekkingarprófið geturðu krafist þess að svarendur slá inn nöfn sín sem hluta af könnuninni eða þekkingarprófinu.

> [!NOTE]
> Virkni Microsoft Forms er aðeins í boði með Viðbót við alhliða ráðningar.

