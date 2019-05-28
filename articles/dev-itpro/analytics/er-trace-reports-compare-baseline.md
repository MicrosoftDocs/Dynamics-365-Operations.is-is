---
title: Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi
description: Í þessu efnisatriði eru veittar upplýsingar um hvernig hægt er að bera saman niðurstöður myndaðar skýrslur rafrænnar skýrslugerðar við skýrslugildi grunnlínu.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 7f7877ccaa0c45ab5f0032d6808280e3c47a43ca
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554116"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Rekja myndaðar skýrsluniðurstöður og bera þær saman við grunnlínugildi

[!include[banner](../includes/banner.md)]

Hægt er að rekja niðurstöður fyrir snið rafrænnar skýrslugerðar sem býr til rafræn skjöl á útleið. Þegar kveikt er á rakningu myndunar (færibreyta notanda rafrænnar skýrslugerðar **Keyra í kembiham**) er búin til ný rakningarfærsla í aðgerðarskráningu rafrænnar skýrslugerðar í hvert sinn sem skýra rafrænnar skýrslugerðar er keyrð. Eftirfarandi upplýsingar eru geymdar í hverri rakningu sem er mynduð:

- Allar viðvaranir sem voru myndaðar eftir villuleitarreglum
- Allar villur sem voru myndaðar eftir villuleitarreglum
- Allir myndaðar skrár sem eru geymdar sem viðhengi rakningarfærslunnar

Hægt er að geyma einstakar hugbúnaðarskrár grunnlínu fyrir hvaða snið rafrænnar skýrslugerðar sem er. Skrár eru álitnar grunnlínuskrár þegar þær lýsa væntanlegum niðurstöðum skýrslna sem eru keyrðar. Ef grunnlínuskrá er tiltæk fyrir snið rafrænnar skýrslugerðar sem var keyrt á meðan kveikt var á rakningarmyndun geymir rakningin, til viðbótar við upplýsingarnar sem minnst var á áður, niðurstöður á samanburðinum á milli myndaða rafræna skjalsins og grunnlínuskráarinnar. Í einum smelli er einnig hægt að fá myndaða rafræna skjalið og grunnlínuskrána í einni zip-skrá. Síðan er hægt að gera ítarlegan samanburð með því að nota ytri verkfæri eins og Windiff.

Hægt er að meta rakninguna til að greina hvort rafrænu skjölin sem eru mynduð innihaldi væntanlegt efni. Hægt er að gera þetta mat í samþykktarprófsumhverfi notanda þegar kóðagrunninum hefur verið breytt (til dæmis þegar nýtt tilvik af hugbúnaðinu var flutt, bráðabót var sett upp eða kóðabreytingar voru virkjaðar). Þannig er hægt að tryggja að matið hafi ekki áhrif á framkvæmd á skýrslum rafrænnar skýrslugerðar sem eru notaðar. Fyrir margar skýrslur rafrænnar skýrslugerðar er hægt að gera matið í eftirlitslausum ham.

Til að læra meira um þennan eiginleika skal spila verkefnaleiðbeiningarnar **Myndun skýrslna með rafrænni skýrslugerð og samanburður á niðurstöðum (hluti 1)** og **Myndun skýrslna með rafrænni skýrslugerð og samanburður á niðurstöðum (hluti 2)** sem eru hluti af viðskiptaferlinu **7.5.4.3 Prófun tækniþjónustu/lausna (10679)** og sem hægt er að hlaða niður af [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). Þessar verkefnaleiðbeiningar fylgja þér í gegnum ferlið við að grunnstilla ramma rafrænnar skýrslugerðar til að nota grunnlínuskrár til að meta mynduð rafræn skjöl.
