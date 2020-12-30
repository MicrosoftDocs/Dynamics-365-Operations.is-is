---
title: Grunnstilla færibreytur Mannauðs
description: Stillingar fyrir sumar færibreytur Human Resources eru eins milli fyrirtækja, á meðan stillingar annara færibreyta eru bundnar tilteknu fyrirtæki. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs sem eru bundnar tilteknu fyrirtæki.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: bac50c5f302797e28df2bc792893c8a682899a93
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418967"
---
# <a name="configure-human-resources-parameters"></a>Grunnstilla færibreytur Mannauðs

Stillingar fyrir sumar færibreytur Mannauðs (HR) eru eins milli fyrirtækja, á meðan stillingar annara færibreyta eru bundnar tilteknu fyrirtæki. Í þessari grein er því lýst hvernig á að setja upp færibreytur Mannauðs sem eru bundnar tilteknu fyrirtæki.

Tvær síður eru notaðar til að setja upp færibreytur mannauðs (HR). Fyrir Færibreytur sem fyrirtæki samnýta, notarðu **samnýttar færibreytur fyrir mannauð** síðu. Fyrir færibreytur sem eru bundin tilteknu fyrirtæki (með öðrum orðum, stillingar eiga við um eitt fyrirtæki), notarðu **færibreytum mannauðs** síðu. Á **færibreytur Mannauðs** síða, er stillingum deild á sex flipa:

-   Almennt
-   Ráðningar - þetta er ekki innifalið í Dynamics 365 Human Resources
-   Laun
-   Númeraraðir
-   Family and Medical Leave Act (lög um leyfi vegna fjölskyldu eða veikinda)
-   Sjálfsafgreiðsla starfsmanna

Hver flipi inniheldur upplýsingar sem tengjast einu fyrirtæki. Stillingar á í **Almennt** flipanum skilgreina útlit hvers upplýsinga um fjarvistir, meiðsla og veikinda og nýráðningar. Stillingar á þessum flipa skilgreina einnig sumar sjálfgefnar færslur sem birtast meðfram vinnu. Þessi flipi leyfir þér nákvæmlega að velja lit til að hafa á opnum fjarvistarfærslum, stílblað til að nota fyrir skýrslur, virkja á samþættinguna á milli þjálfunarnámskeiða og fjarvistarskráningar og veljið fjarvistarkóðann sem á að nota til að stýra þessari samþættingu. Einnig er hægt að tilgreina hversu lengi atvikum meiðsla og veikindamála á að halda og tilgreina sjálfgefið auðkennisnúmer sem er sýnt þegar nýr starfsmaður er ráðinn. 

Stillingar á **Ráðningarverk** flipa er að skilgreina gerðir skjala sem eru notaðar fyrir samskipti sem er sjálfkrafa sent umsækjendum og ráðningarverkið sem er notað fyrir óumbeðnar umsóknir (umsóknir sem ekki eru fyrir tiltekið ráðningarverk). Tímabilið sem er skilgreint fyrir aldursgreiningu ráðningarverks ákvarðar ráðningarverk sem eru innifalin á **aldursgreiningarverk** reitnum í **umsjón með ráðningum** vinnusvæði. Tímabilið sem er skilgreint fyrir viðvörun lokafrests umsóknar er notað til að birta ráðningarverk sem eru að nálgast skilafrest sinn á í **skilafrestur umsóknar nálgast** reit í **Ráðningarverk** vinnusvæði. 

Stillingar á **Laun** flipanum skilgreina hvort notendur verða staðfesta að þeir vilji að vista upplýsingar fyrir fast eða breytilegt launafyrirkomulag. Ef gátreiturinn **Virkja villuleit vistunar** er valinn fá notendur skilaboð þegar þeir loka síðu sem tengist launum þar sem spurt er hvort þeir vilji vista færsluna. Sumar síður í lausnastjórnun leyfa ekki notendum að eyða upplýsingum. Þess vegna, með því að senda kvaðningu til notenda til að staðfesta að þeir vilja að vista upplýsingar, gætirðu takmarkað magn upplýsinga sem er vistað en ekki er hægt að eyða síðar. Ef **Virkja villuleit vistunar** gátreiturinn er hreinsaður eru færslur alltaf vistaðar strax, mögulega áður en notandinn er tilbúinn. Ef þú er ekki að nota frammistöðustjórnun er leyfir **Launa** flipinn þér einnig að velja einkunnalíkan til að nota í staðinn fyrir líkanið sem er úthlutað á launafyrirkomulag þegar verið er að gefa frammistöðu einkunn. 

### <a name="previously-released-functionality"></a>Áður losaðar virkni

Stillingarnar á flipanum **númeraröð** ákvarða raðir sem verða notuð til að úthluta sjálfkrafa auðkenni á liði í mannauði, svo sem umsókn, fjarvistarskráningar, viðburðir, niðurstöður launavinnsla, málsnúmer, námskeið og námskeiðsdagskrá. Til að vinna með tilvísanir númeraraða og kóða í **Númeraraðir** listasíðu (smellt er á **Fyrirtækisstjórnun** &gt; **Númeraraðir** &gt; **Númeraraðir**).

> [!NOTE]
> Fjölda stunda sem er unnið má ekki fara yfir 1,250 og lengd ráðningar má ekki fara yfir 12 mánuði. Þessi hámarksgildi eru samkvæmt alríkislögum í Bandaríkjunum. Að lokum, stillingar á í **sjálfsafgreiðslu Starfsmanns** flipanum ákvarða upplýsingar sem stjórnandi getur fært inn fyrir hönd starfsmanns hans eða hennar.
