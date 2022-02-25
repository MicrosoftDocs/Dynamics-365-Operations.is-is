---
title: Skilgreina greiðsluskilmála lánardrottna
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluskilmála fyrir lánardrottnareikninga.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2199c12e92d631d3eb058637c48b53335d779f2d
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109808"
---
# <a name="define-vendor-payment-terms"></a>Skilgreina greiðsluskilmála lánardrottna

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluskilmála fyrir lánardrottnareikninga. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptaskuldir > Greiðsluuppsetning > Greiðsluskilmálar**.
2. Veljið **Nýtt**. The **Greiðsluskilmálar** síða er notuð til að skilgreina hvernig gjalddagi verður reiknaður út. Það er ekki notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar.  
3. Færðu inn gildi í reitnum **greiðsluskilmálar**.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitinn **Dagar** skal slá inn númer. Númerið sem er slegið inn hér verður notað til að bæta við gjalddaga eða við lok tímabilsins sem tilgreint er í **Greiðslumáti**. Til dæmis, ef **Nettó** er valið, verður tölunni bætt við gjalddaga. Ef valið er **Gildandi mánuður**, bætir það tölunni við síðasta dag núverandi mánaðar til að reikna út gjalddaga.  
6. Veljið **Vista**.
7. Lokið síðunni.
8. Farðu í **Viðskiptaskuldir > Greiðsluuppsetning > Staðgreiðsluafsláttur**.
9. Veljið **Nýtt**.
10. Færið inn kenni í reitnum **Staðgreiðsluafsláttur**.
11. Í reitinn **Lýsing** skal slá inn gildi.
12. Ef lánardrottinn býður upp á lagskipt afslátt, velja næsta staðgreiðsluafsláttinn eftir að sá gildandi er útrunnið.
13. Lokið síðunni.
14. Í reitinn **Dagar** skal slá inn númer. Magnið sem er slegið inn í **Dagar** reiturinn verður notaður til að reikna út **Dagsetning staðgreiðsluafsláttar**, byggt á því hvaða valkostur var valinn í **Nettó/Núverandi** sviði. Ef **Nettó** var valinn er magni bætt við dagsetningu reiknings til að ákvarða dagsetningu staðgreiðsluafsláttar. Ef **Núverandi mánuður** var valinn er magn verður bætt við lok gjaldmiðilsmánaðar til að ákvarða dagsetningu staðgreiðsluafsláttar.  
15. Færið inn hlutfall staðgreiðsluafslátt í reitnum **Afsláttur**. 
16. Sláðu inn aðalreikninginn sem staðgreiðsluafslátturinn verður bókaður fyrir reikninga viðskiptavina og sláðu síðan inn aðalreikninginn sem staðgreiðsluafslátturinn verður bókaður fyrir reikninga lánardrottins. Ef **Afsláttarmótlyklar** er stillt til að **Nota aðallykill fyrir afslátt lánardrottins**, þá verður aðallykill notaður. Ef valkosturinn er stillt á **Lyklana á reikningslínum**, verður staðgreiðsluafslátturinn bókaður á eignar/kostnaðarlykla í línum á reikningi.  
17. Veljið **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
