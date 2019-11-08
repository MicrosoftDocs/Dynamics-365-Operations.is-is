---
title: Verkþættir í ráðningarferli
description: Þetta efnisatriði gefur upplýsingar um ýmis konar aðgerðir sem hægt er að nota í ráðningarferlinu í Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 09ac8f5431de0809b9a3a23e1175d5027153e96c
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552164"
---
# <a name="activities-in-hiring-processes"></a>Verkþættir í ráðningarferli

[!include[banner](../includes/banner.md)]

Aðgerðum má bæta við sem hluti af ráðningarferlinu í Microsoft Dynamics 365 Talent: Attract. Aðgerðum má bæta við sniðmát ferlis, eða hægt er að bæta þeim beint við ráðningarferlið í starfi. Þegar starf er skilgreint er sniðmát ferlis valið og aðgerðir sem er innifalinn í sniðmátið er beitt í starfið. Ef sniðmát er ekki valið er sjálfgefið sniðmát notað. Ráðningarferlið er einnig hægt að breyta í starfi eftir að sniðmátið er beitt.

> [!NOTE] 
> Felissniðmát eru fáanlegar með Viðbót við alhliða ráðningar. Frekari upplýsingar er að finna í [Attract-viðbótareiginleikar við alhliða ráðningar](./attract-comprehensive-hiring.md).

## <a name="prospect-activity"></a>Aðgerð fyrir viðfang

Aðgerð fyrir viðfang stýrir hvort viðföngum getur verið bætt við starf. Sjálfgefið er að hægt sé að bæta viðföngum við starf. Til að slökkva á aðgerð fyrir viðföng skaltu stilla **Virkja viðföng** valkostinn á **Slökkt**. Þegar kveikt er á aðgerð fyrir viðföng, geta mannauðsstjórar bætt við og skoðað viðföng og **Viðföng** flipinn er sýndur í starfinu.

> [!NOTE]
> Til að leyfa frambjóðendum að bæta við starf frá LinkedIn verður þú að stilla valkostinn **Virkja viðföng** á **Á**.

## <a name="application-activity"></a>Umsóknaraðgerð

Umsóknaraðgerðar er krafist í sniðmát ráðningarferlisins. Til að senda tölvupóst til umsækjenda þegar þeir leggja inn umsóknina eða eru bætt við umsóknarstigið skaltu stilla **Senda póst til umsækjanda** valkosts til **Á**.

## <a name="interview-schedule-and-feedback-activity"></a>Viðtalsáætlun og endurgjafaraðgerð

Þessi aðgerð hefur þrjá þætti: Beiðni um tímaupplýsingar umsækjanda, tímaáætlun og endurgjöf. Notaðu viðtalsaðgerðina í starfssniðmátinu ef þú vilt hafa með beiðni um tímaupplýsingar umsækjanda, áætlun og endurgjöf sem hluti af ferlinu í staðinn fyrir að nota það hvert fyrir sig sem hluta af ráðningarferlinu. Nánari upplýsingar er að finna í [Viðtalsáætlun og endurgjöf](interview-scheduling-feedback.md).

## <a name="powerapps-activity"></a>PowerApps verkþáttur

PowerApps-aðgerðin gerir þér kleift að fella Microsoft PowerApps-forrit inn í ráðningarferli þitt. Forritið kann að vera nauðsynlegt fyrir alla umsækjendur, aðeins innri umsækjendur, aðeins ytri umsækjendur eða enga umsækjendur. Ef forritið er merkt sem áskilið verður það að vera lokið áður en stigið getur haldið áfram. Til að teljast lokið þarf reiturinn **JobApplicationStatus** að vera stilltur á **Ljúka**. Þetta reitur er staðsettur í JobApplicationActivity einingunni, þannig að PowerApps-forritið verður að uppfæra þennan reit áður en stigið getur haldið áfram. Ef forritið er ekki merkt sem áskilið er aðgerðin valfrjáls skref og stigið getur haldið áfram, jafnvel þótt forritið sé ekki lokið.

Til að vista PowerApps-aðgerð í ráðningarferlið verður þú að slá inn PowerApps-kenni. Til að finna PowerApps-kennið, farðu í [PowerApps](https://web.powerapps.com), veldu **Forrit** og veldu síðan **Upplýsingar**.

Sjálfgefið er að PowerApps-virknin sé tiltæk ráðningarstjóra, ráðningaraðila og fulltrúum þeirra. Ef þú velur valkostinn **Leyfa að bæta þátttakendum við þessa aðgerð** er hægt að bæta öðrum þátttakendum úr ráðningarhópnum við fyrir forrit sem notar PowerApps-virknina. Til dæmis hefur fyrirtæki búið til PowerApps-forrit sem er safn af viðtalsspurningum fyrir tæknistörf. Fyrirtækið er nú að ráða nýjan forritara og hefur bætt virkni PowerApps-aðgerðinni við ráðningarferlið fyrir forritarastarfið. Ef valkosturinn **Leyfa að bæta við þátttakendum fyrir þessa aðgerð** er valinn, getur ráðningaraðili eða mannauðsstjóri sem er að skoða umsækjanda um forritarastarfið, bætt viðmælendum við PowerApps-aðgerðina. Þessir aðilar geta þá skoðað forritið sem hefur viðtalsspurningarnar.

> [!NOTE]
> PowerApps-aðgerð er aðeins í boði með Viðbót við alhliða ráðningar. Frekari upplýsingar er að finna í [Attract-viðbótareiginleikar við alhliða ráðningar](./attract-comprehensive-hiring.md).

## <a name="youtube-activity"></a>YouTube verkþáttur

YouTube-aðgerð gerir þér kleift að deila YouTube-myndbandi sem hluti af ráðningarferlinu þínu. Til að vista YouTube-aðgerðina í ráðningarferlinu verður þú að tilgreina vefslóð YouTube myndskeiðsins. Þú getur valið að birta innihaldið í **Ráðningarhópur**, **Eingöngu umsækjendur innan fyrirtækis**, **Eingöngu umsækjendur utan fyrirtækis** eða **Allir umsækjendur**. Eins og PowerApps-aðgerðin er hægt að leyfa að bæta þátttakendum ráðningarhóps við aðgerðina. Ef þú velur að sýna umsækjendum innihaldið er myndbandið aðeins sýnt sem hluti af reynslu umsækjanda og ekki í ráðningarferlinu.

> [!NOTE]
> YouTube-aðgerð er aðeins í boði með Viðbót við alhliða ráðningar. Frekari upplýsingar er að finna í [Attract-viðbótareiginleikar við alhliða ráðningar](./attract-comprehensive-hiring.md).

## <a name="web-content-activity"></a>Vefefnisaðgerð

Með vefefnisaðgerð er hægt að fella inn efni á netinu í ráðningarferlinu þínu. Til að vista vefefnisaðgerðina í ráðningarferlinu verður þú að tilgreina vefslóð efnisins. Þú getur valið að birta innihaldið í **Ráðningarhópur**, **Eingöngu umsækjendur innan fyrirtækis**, **Eingöngu umsækjendur utan fyrirtækis** eða **Allir umsækjendur**. Eins og aðgerðir PowerApps og YouTube er hægt að leyfa að bæta þátttakendum ráðningarhóps við aðgerðina. Ef þú velur að sýna umsækjendum innihaldið er vefefnið aðeins sýnt sem hluti af upplifun umsækjanda og ekki í ráðningarferlinu. Þú getur valið stærð efnisins sem er sýnt.

> [!NOTE]
> Vefefnisaðgerðin er aðeins í boði með Viðbót við alhliða ráðningar. Frekari upplýsingar er að finna í [Attract-viðbótareiginleikar við alhliða ráðningar](./attract-comprehensive-hiring.md).

## <a name="microsoft-forms-activity"></a>Microsoft Forms-aðgerð

Microsoft Forms-aðgerðin gerir þér kleift að fella Microsoft Forms-aðgerð inn í ráðningarferlið þitt. Microsoft Forms gerir þér kleift að búa til þekkingarpróf, mat og kannanir. Til að vista virkni Microsoft Forms í ráðningarferlið verður þú að tilgreina vefslóð eyðublaðsins. Þú getur valið að birta innihaldið í **Ráðningarhópur**, **Eingöngu umsækjendur innan fyrirtækis**, **Eingöngu umsækjendur utan fyrirtækis** eða **Allir umsækjendur**. Eins og aðgerðir PowerApps, YouTube og vefefnis er hægt að leyfa að bæta þátttakendum ráðningarhóps við aðgerðina. Ef þú velur að sýna umsækjendum innihaldið er skjámyndin aðeins sýnd sem hluti af upplifun umsækjanda og ekki í ráðningarferlinu.

Í Microsoft Forms geta höfundar breytt stillingum sínum til að láta notendur utan fyrirtækisins svara könnunum eða þekkingarprófum sínum. Í þessu tilfelli, notendur senda inn svar á nafnlausan hátt. Ef þú vilt sjá hver hefur fyllt út könnunina þína eða þekkingarprófið geturðu krafist þess að svarendur slá inn nöfn sín sem hluta af könnuninni eða þekkingarprófinu.

> [!NOTE]
> Virkni Microsoft Forms er aðeins í boði með Viðbót við alhliða ráðningar. Frekari upplýsingar er að finna í [Attract-viðbótareiginleikar við alhliða ráðningar](./attract-comprehensive-hiring.md).

## <a name="offer-activity"></a>Tilboðsvirkni

Sniðmát ráðningarferlis krefst virkni tilboðs. Til að nota samþætt forrit tilboðsstjórnunar skal stilla **Ræsa forrit tilboðsstjórnunar í Undirbúa tilboð** á **Kveikt**. Ef slökkt er á þessari stillingu mun umsækjandinn ekki birtast í tilboðsforritinu, svo þú verður að fylgjast handvirkt með uppfærslum á tilboðsaðgerðum umsækjanda. Til að skilgreina hvort ráðningarstjórar geti undirbúið tilboðið fyrir umsækjanda í tilboðsforritinu skal stilla **Ráðningarstjórar geta undirbúið tilboð** á **Kveikt**. Ef margar stöður tengjast starfinu er hægt að ákveða hvort eigi að undirbúa mörg tilboð gagnvart sama númeri á stöðu. Ef þú vilt aðeins leyfa eitt tilboð fyrir hverja stöðu fyrir hvert starf skal stilla **Leyfa að stöður verði notaðar aftur innan starfs** á **Slökkt**.

> [!NOTE]
> Samþætt forrit tilboðsstjórnunar er aðeins í boði með viðbót alhliða ráðningar. Frekari upplýsingar er að finna í [Attract-viðbótareiginleikar við alhliða ráðningar](./attract-comprehensive-hiring.md).


