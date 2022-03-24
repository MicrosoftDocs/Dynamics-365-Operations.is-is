---
title: Óvæntur munur á beiðni og lotugögnum meðan á prófun stendur
description: Óvæntur munur kemur upp á milli beiðni- og lotugagna í niðurstöðum verkefna vöruhúsaapps.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456954"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Óvæntur munur á beiðni og lotugögnum meðan á prófun stendur

Villukóði: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Einkenni

Þegar þú ert að nota [verkefnaprófunarrammi vöruhúsaapps](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat), sannprófunartækið skilar eftirfarandi villuboði:

> Óvæntur munur á beiðni og lotugögnum. Brotið á XML samskiptareglum vöruhúss farsímatækja.REQUEST_XML_TAMPERING

## <a name="cause"></a>Orsök

Villan kemur upp þegar úttak síðasta skrefs sem tókst að keyra í prufukeyrslu passar ekki við skráð inntak fyrir næsta skref. Þessi staða getur komið upp vegna þess að verkefnaprófari notar ekki úttak fyrra skrefs sem inntak fyrir skref í röð. Þess í stað notar það skráð XML sem inntak fyrir hvert skref.

Í flestum tilfellum kemur villa þegar þú keyrir verkefni aftur, en prófið krefst nokkurra skráa sem voru breytt eða fjarlægð með fyrri keyrslu sama verkefnis.

## <a name="resolution"></a>Upplausn

Staðfestingarprófun vöruhúsaforritsins er ekki óvirk aðgerð heldur breytir undirliggjandi gögnum. Þess vegna gætirðu þurft að endurstilla viðeigandi gögn áður en þú keyrir verkefni aftur.

1. Skoðaðu úttaks-XML síðasta prófunarskrefsins sem heppnaðist til að ákvarða hvar prufukeyrslan þín hætti.
1. Skoðaðu prófið þitt og vertu viss um að allar nauðsynlegar sölupantanir, flutningspantanir, verkhausar og aðrar færslur séu enn til staðar og í væntanlegu ástandi.
1. Búðu til aftur eða breyttu færslunum sem vantar eða breyttar. Að öðrum kosti skaltu búa til nýja prófunaruppsetningu og hanna prófið til að nota gildar fyrirliggjandi færslur.
