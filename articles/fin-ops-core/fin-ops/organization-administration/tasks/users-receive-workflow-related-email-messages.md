---
title: Gera notendum kleift að fá tölvupóst sem tengjast verkflæði
description: Hægt er að grunnstilla kerfið til að senda tölvupóst til notenda þegar tilvik verkflæðis sem tengjast eiga sér stað.
author: jasongre
ms.date: 06/01/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 368fe2fbf1f8a1adcabe37ced5ed942f9fb86fc8
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070426"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a>Gera notendum kleift að fá tölvupóst sem tengjast verkflæði

[!include [banner](../../includes/banner.md)]


[!INCLUDE [PEAP](../../../../includes/peap-1.md)]

Hægt er að grunnstilla kerfið til að senda tölvupóst til notenda þegar tilvik verkflæðis sem tengjast eiga sér stað. Til dæmis er hægt að senda tölvupóstskilaboð til notenda þegar skjöl eru send þeim til samþykktar. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Kerfisstjórnun > Notendur > Notendur**.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
3. Í **Aðgerðarrúðunni** smellirðu á **Valkostir notanda**.
4. Smelltu á flipann **Verkflæði**. Gakktu úr skugga um að hlutinn **Tilkynningar** sé stækkaður. Í hlutanum **Tilkynningar** er hægt að tilgreina hvernig notandi látinn vita um tilvik sem tengjast verkflæði.  
5. Veljið valkost í reitnum **Gerð tilkynningar verkflæðis fyrir línuvöru**.
    - Flokkað - Tilkynningar fyrir línuatriði eru flokkaðar í einn tölvupóst.
    - Stakt - Tölvupóstur eru send fyrir hvern línuatriði.  
    - Ef óskað er eftir að notandi fái tilkynningar í biðlaranum velurðu gátreitinn **Senda tilkynningar í tölvupósti**.  
6. Smellt er á **Vista**.
7. Lokið síðunni.

> [!NOTE]
> Tölvupóstssniðmát verkflæðis verða fengin frá annaðhvort tölvupóstssniðmátum kerfis eða fyrirtækis, fer eftir því hvort verkflæðið is á kerfisstigi (miðast ekki við fyrirtæki) eða verkflæði á fyrirtækisstigi (miðast við fyrirtæki).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]