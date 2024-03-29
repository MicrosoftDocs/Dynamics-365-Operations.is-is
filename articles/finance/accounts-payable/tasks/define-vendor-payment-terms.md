---
title: Skilgreina greiðsluskilmála lánardrottna
description: Þessi grein útskýrir hvernig á að setja upp greiðsluskilmála fyrir reikninga lánardrottins.
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
ms.openlocfilehash: a676856ed43bf1b78684eac0682e0fdef9c84083
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906472"
---
# <a name="define-vendor-payment-terms"></a>Skilgreina greiðsluskilmála lánardrottna

[!include [banner](../../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp greiðsluskilmála fyrir reikninga lánardrottins. Þetta verkefni notar USMF-sýnifyrirtækið.

1. Farðu í **Skoðunarrúðu > Kerfiseiningar > Viðskiptaskuldir > Greiðsluuppsetning > Greiðsluskilmálar**.
2. Veljið **Nýtt**. **Greiðsluskilmálar** síðan er notuð til að skilgreina hvernig verður að reikna út gjalddaga. Það er ekki notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar.  
3. Færðu inn gildi í reitnum **greiðsluskilmálar**.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitinn **Dagar** skal slá inn númer. Númerið sem fært er inn hér verður notað til að bæta við gjalddaga eða við lok tímabils sem skilgreind er í **Greiðsluaðferð**. Til dæmis, ef **Nettó** er valið, verður tölunni bætt við gjalddaga. Ef valið er **Gildandi mánuður**, bætir það tölunni við síðasta dag núverandi mánaðar til að reikna út gjalddaga.  
6. Veljið **Vista**.
7. Lokið síðunni.
8. Farðu í **Viðskiptaskuldir > Greiðsluuppsetning > Staðgreiðsluafsláttur**.
9. Veljið **Nýtt**.
10. Færið inn kenni í reitnum **Staðgreiðsluafsláttur**.
11. Í reitinn **Lýsing** skal slá inn gildi.
12. Ef lánardrottinn býður upp á lagskipt afslátt, velja næsta staðgreiðsluafsláttinn eftir að sá gildandi er útrunnið.
13. Lokið síðunni.
14. Í reitinn **Dagar** skal slá inn númer. Magnið sem var slegið inn í **Dagar** verður notað til að reikna út **Dagsetning staðgreiðsluafsláttar**, á grundvelli þess hvaða valkostur var valinn í svæðinu **Nettó/gildandi** field. Ef **Nettó** var valinn er magni bætt við dagsetningu reiknings til að ákvarða dagsetningu staðgreiðsluafsláttar. Ef **Núverandi mánuður** var valinn er magn verður bætt við lok gjaldmiðilsmánaðar til að ákvarða dagsetningu staðgreiðsluafsláttar.  
15. Færið inn hlutfall staðgreiðsluafslátt í reitnum **Afsláttur**. 
16. Sláðu inn aðalreikninginn sem staðgreiðsluafslátturinn verður bókaður fyrir reikninga viðskiptavina og sláðu síðan inn aðalreikninginn sem staðgreiðsluafslátturinn verður bókaður fyrir reikninga lánardrottins. Ef **Afsláttarmótlyklar** er stillt til að **Nota aðallykill fyrir afslátt lánardrottins**, þá verður aðallykill notaður. Ef valkosturinn er stillt á **Lyklana á reikningslínum**, verður staðgreiðsluafslátturinn bókaður á eignar/kostnaðarlykla í línum á reikningi.  
17. Veljið **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
