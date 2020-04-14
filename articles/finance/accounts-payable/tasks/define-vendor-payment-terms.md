---
title: Skilgreina greiðsluskilmála lánardrottna
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluskilmála fyrir lánardrottnareikninga.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e6778f61a9367399e4b71d5b2bb2459c09ba508
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143904"
---
# <a name="define-vendor-payment-terms"></a>Skilgreina greiðsluskilmála lánardrottna

[!include [banner](../../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluskilmála fyrir lánardrottnareikninga. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptaskuldir > Greiðsluuppsetning > Greiðsluskilmálar**.
2. Veljið **Nýtt**. Skilmála greiðslu síða er notuð til að skilgreina hvernig verður að reikna út gjalddaga. Það er ekki notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar.  
3. Færðu inn gildi í reitnum **greiðsluskilmálar**.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitinn **Dagar** skal slá inn númer. Númerið sem fært er inn hér verður notað til að bæta við gjalddaga eða við lok tímabils sem skilgreind er í greiðsluaðferðina. Til dæmis, ef **Nettó** er valið, verður tölunni bætt við gjalddaga. Ef valið er **Gildandi mánuður**, bætir það tölunni við síðasta dag núverandi mánaðar til að reikna út gjalddaga.  
6. Veljið **Vista**.
7. Lokið síðunni.
8. Farðu í **Viðskiptaskuldir > Greiðsluuppsetning > Staðgreiðsluafsláttur**.
9. Veljið **Nýtt**.
10. Færið inn kenni í reitnum **Staðgreiðsluafsláttur**.
11. Í reitinn **Lýsing** skal slá inn gildi.
12. Ef lánardrottinn býður upp á lagskipt afslátt, velja næsta staðgreiðsluafsláttinn eftir að sá gildandi er útrunnið.
13. Lokið síðunni.
14. Í reitinn **Dagar** skal slá inn númer. Magnið sem er fært inn í reitinn **Dagar** verður notað til að reikna út dagsetningu staðgreiðsluafsláttar, á grundvelli hvaða valkostur var valinn í reitnum **Nettó/Gildandi**. Ef **Nettó** var valinn er magni bætt við dagsetningu reiknings til að ákvarða dagsetningu staðgreiðsluafsláttar. Ef **Núverandi mánuður** var valinn er magn verður bætt við lok gjaldmiðilsmánaðar til að ákvarða dagsetningu staðgreiðsluafsláttar.  
15. Færið inn hlutfall staðgreiðsluafslátt í reitnum **Afsláttur**. 
16. Sláðu inn aðalreikninginn sem staðgreiðsluafslátturinn verður bókaður fyrir reikninga viðskiptavina og sláðu síðan inn aðalreikninginn sem staðgreiðsluafslátturinn verður bókaður fyrir reikninga lánardrottins. Ef **Afsláttarmótlyklar** er stillt til að **Nota aðallykill fyrir afslátt lánardrottins**, þá verður aðallykill notaður. Ef valkosturinn er stillt á **Lyklana á reikningslínum**, verður staðgreiðsluafslátturinn bókaður á eignar/kostnaðarlykla í línum á reikningi.  
17. Veljið **Vista**.

