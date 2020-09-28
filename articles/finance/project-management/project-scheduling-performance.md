---
title: Frammistaða tilfangaáætlunar verks
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að bæta afköst tilfangaáætlunar fyrir mikinn fjölda verkefna.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760579"
---
# <a name="project-resource-scheduling-performance"></a>Frammistaða tilfangaáætlunar verks

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Afkastavandamálum sem tengjast tilfangaáætlun getur átt sér stað þegar um þúsundir verka er að ræða. Til að bæta afköst tilfangaáætlunar gerir tiltekinn eiginleiki notendum kleift að stytta tímann sem tekur að opna skjámyndina fyrir tilföng til ráðstöfunar. Sérstaklega fjarlægir þetta samstillingu tilfangagetu samantekta og notar **ResProjectResource** töfluna til að flýta leit tilfanga. Athugið að ekki er lengur hægt að nota töfluna **ResRollup**.

> [!IMPORTANT]
> Ef samstillingarferli forðagetu eða **ResProjectResource** taflan eru tengd ekki skal nota þennan eiginleika.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Virkja afkastaaukningu tilfangaáætlunar
Til að virkja endurbætt frammistöðu tilfangaáætlunar skal ljúka eftirfarandi skrefum.

1. Farðu í **Eiginleikastjórnun** > **Allt** og á eiginleikalistanum skal finna **Virkja eiginleika afkastaaukningar fyrir áætlanagerð verktilfangs**.
2. Veldu **Virkja núna**.

> [!NOTE]
> Ef ekki er hægt að finna eiginleikann á listanum skal velja **Leita að uppfærslum** til að uppfæra listann.

3. Endurhlaðið vafrann og farið síðan í **Verkefnastjórnun og bókhald** > **Reglubundið** > **Verktilföng** > **Samstilla afkastagetu tilfangadagatala í öllum fyrirtækjum**.
4. Stilltu **Fjarlæga fyrirliggjandi afkastagetuskrár** á **Já** til að fjarlægja fyrri gögn. Ef búa á til stigvaxandi gögn skal stilla það á **Nei**.
5. Í reitnum **Tímabilskóði** skal velja tímabilið sem á að mynda gögn fyrir. Ef tímabilskóði er valinn þarf ekki að skilgreina upphafs- og lokadagsetningar.
6. Ef reiturinn **Tímabilskóði** er skilinn eftir auður skal velja tilteknar upphafs- og lokadagsetningar til að búa til gögn.
7. Veljið **Í lagi**.

 > [!NOTE]
 > Þetta dreifir almennum gögnum á **ResCalendarCapacity** töflu yfir öll fyrirtæki í umhverfinu og því þarf aðeins að keyra runuvinnsluna hjá einum lögaðila. Gögnin í þessari runuvinnslu eru nauðsynleg til að reikna afkastagetu tilfanga í gegnum tengda dagatalið.

8. Farðu í **Verkefnastjórnun og bókhald** > **Reglubundið** > **Verktilföng** > **Færa inn verktilföng í öll fyrirtæki** og veldu síðan **Í lagi**. Þetta er gagnauppfærsluforskriftin fyrir almenn gögn í töflunum **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**. Gildin fyrir svæðið **PSAPRojSchedRole.RootActivity** eru einnig uppfærð. Ef þetta er ekki keyrt birtist viðvörun þegar reynt er að keyra tilfangaáætlanir.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Slökkva á afkastaaukningu tilfangaáætlunar

1. Farðu í **Eiginleikastjórnun** > **Allt** og leitaðu að **Virkja eiginleika afkastaaukningar fyrir áætlanagerð verktilfangs**.
2. Veldu eiginleikann og svo hnappinn **Óvirkja**.
3. Uppfærðu vafrann þinn.
4. Farðu í **Verkefnastjórnun og bókhald** > **Reglubundið** > **Samstilling afkastagetu** > **Samstilla tilfangagetu samantekta**.
5. Á síðunni **Samstilling samantektar á afkastagetu** skal stilla **Fjarlæga fyrirliggjandi afkastagetuskrár** á **Já** til að fjarlægja fyrri gögn. Ef ætlunin er að búa til stigvaxandi gögn skal stilla þetta á **Nei**.
6. Í reitnum **Tímabilskóði** skal velja tímabilið sem á að mynda gögn fyrir. Ef tímabilskóði er valinn þarf ekki að skilgreina upphafs- og lokadagsetningar.
7. Ef reiturinn **Tímabilskóði** er skilinn eftir auður skal velja tilteknar upphafs- og lokadagsetningar til að búa til gögn.
8. Veljið **Í lagi**.

> [!NOTE]
> Þetta dreifir almennum gögnum á töfluna **ResRollup** á milli allra fyrirtækja í umhverfinu og því þarf aðeins að keyra runuvinnsluna hjá einum lögaðila. Þessi runuvinnsla er nauðsynleg fyrir **Tilföng til ráðstöfunar**. Ef þessi runuvinnsla er ekki keyrð verða **ResRollup** gögn búið til um leið og getur það tekið tíma.
