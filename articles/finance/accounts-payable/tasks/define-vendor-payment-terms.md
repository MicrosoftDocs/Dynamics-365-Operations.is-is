---
title: Skilgreina greiðsluskilmála lánardrottna
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp greiðsluskilmála fyrir lánardrottnareikninga.
author: abruer
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e70a68ab5e14e8dadfd8d61f696f5971c8e60262d0fd55c5de1589e572ff8085
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722984"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]