---
title: Tilgreina meðalgengið
description: Þetta efni veitir upplýsingar um krossgengi í Microsoft Dynamics 365 Fjármál.
author: abruer
ms.date: 05/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed1db707cf6aed7c9def76ebbbdef7032b8776b6
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735291"
---
# <a name="specify-the-cross-rate"></a>Tilgreina meðalgengið

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði útskýrir tilgang meðalgengi og hvernig á að tilgreina meðalgengi þegar greiðsla með reikningi er jafnaður. Notaðu krosshlutfall þegar eftirfarandi viðmið eiga við: 
-   Jafnað er á milli greiðslu með reikningi. 
-   Nota aðra gjaldmiðla greiðslulínu og reikningslínu. 
-   Hvorugur gjaldmiðill er uppgjörsmynt. 

Meðalgengi er ekki notað til að umreikna gjaldmiðil greiðslufærslu yfir á bókahaldsgjaldmiðil greiðslunnar. Í staðinn eru gengi gengistöflunnar sóttar til að reikna út virðið á gjaldmiðilsupphæð greiðslufærslunnar og gjaldmiðilsupphæð bókhaldsgreiðslunnar. 

Til dæmis bókhaldsgjaldmiðli er USD, er gjaldmiðill reikningsins er CAD og gjaldmiðil greiðslunnar er EUR. Meðalgengi er hægt að færa inn gengi til að þýða beint á milli CAD og EUR og ekki þarf að þýða gegnum USD. Þegar reikningur og aðalgreiðsla eru valin er hægt að slá inn meðalgengi fyrir reikningslínuna. Meðalgengið er gengið á milli gjaldmiðlanna fyrir þær færslur sem og fyrir jöfnunardagsetninguna.

1.  Farðu inn á eina af eftirfarandi síðum:
- **Viðskiptakröfur > Almennt > Viðskiptavinir > Allir viðskiptavinir** 
- **Viðskiptaskuldir > Algengar > Lánardrottnar > Allir lánardrottnar** 
- **Innkaup og aðföng > Algengt > Lánardrottnar > Allir lánardrottnar**
2.  Veljið viðskiptavininn eða lánardrottinninn sem eiga þær opnu færslur sem eru jafnaðar. 
3.  Fyrir viðskiptavin, á listasíðunni **Allir viðskiptavinir**, skal fara í **Safna > Jafna opnar færslur**. Fyrir lánardrottin, á listasíðunni **Allir lánardrottnar**, skal fara í **Reikningur > Jafna opnar færslur**. 
4.  Veldu færsluna sem er aðalgreiðslan og smelltu síðan á **Merkja greiðslu**. Gátreiturinn í dálknum **Merkja** er valinn og upplýsingatákn birtist í dálknum **Aðalgreiðsla**. 
5.  Í reitnum **Meðalgengi** skal færa inn gengi milli gjaldmiðils reiknings og gjaldmiðils greiðslu frá og með jöfnunardagsetningunni. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
