---
title: Gera upp eftirstöðvar
description: Hægt er að gera upp eftirstandandi upphæð uppgjörsaðgerðar með því að jafna þessa upphæð við fjárhagslykil.
author: roschlom
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 216c5c1d7db72e5f5071f2cd03656df538a64e72
ms.sourcegitcommit: 408786b164b44bee4e16ae7c3d956034d54c3f80
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/05/2021
ms.locfileid: "7754097"
---
# <a name="settle-remainder"></a>Gera upp eftirstöðvar

[!include [banner](../includes/banner.md)]

Hægt er að gera upp eftirstandandi upphæð uppgjörsaðgerðar með því að jafna þessa upphæð við fjárhagslykil eða annan viðskiptavin. Hægt er að gera upp eftirstöðvarnar við uppgjör upphæða sem færðar eru inn í færslubók eða þegar opnar færslur eru gerðar upp.

## <a name="setting-up-defaults"></a>Uppsetning sjálfgilda 
Þú verður að virkja eiginleikann fyrir uppgjör eftirstöðva og setja upp sjálfgefnar stillingar áður en uppgjör eftirstöðva er notað

1)  Smelltu á **Viðskiptakröfur > Færibreytur > Uppgjör** eða **Viðskiptaskuldir > Færibreytur > Uppgjör**
2)  Veldu flipann **Uppgjör** og smelltu á **Virkja uppgjör eftirstöðva**
3)  Í **Sjálfgefinn ástæðukóði** skal velja sjálfgefinn ástæðukóða. Ástæðukóðar verða að hafa verið settir upp í **Viðskiptakröfur > Uppsetning > Ástæðukóðar afskrifta viðskiptavina** eða **Viðskiptaskuldir > Uppsetning > Ástæðukóðar afskrifta viðskiptavina**. **Sjálfgefinn lykill fyrir uppgjör eftirstöðva** verður sjálfgefið að lykli sem er úthlutað til ástæðukóða afskriftar.
3)  Uppfæra **Sjálfgefinn lykill fyrir uppgjör eftirstöðva** eftir þörfum.
4)  Í **Sjálfgefið dagbókarheiti**, veldu greiðslubók sem verður notuð ef þú vilt búa til greiðslubók þegar þú jafnar aðeins opnar færslur. Ef eiginleikinn fyrir uppgjör eftirstöðva er virkjaður þarf að bæta við sjálfgefnu færslubókarheiti.

## <a name="settle-remainder-from-a-journal"></a>Gera upp eftirstöðvar úr færslubók
Ef þú virkjar ekki eiginleikann **Gera upp eftirstöðvar** er samt hægt að færa inn færslu í færslubók og síðan gera upp færslur á móti henni líkt og hefur áður verið gert. Þegar þú smellir á hnappinn **Í lagi** mun upphæð reiðufjár minnka opna stöðu reikningsins. Ef reiðuféð gerir ekki reikninginn upp að fullu er reikningurinn skilinn eftir opinn með eftirstandandi upphæð sem verður gerð upp seinna.

Þegar eiginleikinn **Gera upp eftirstöðvar** er virkjaður er hægt að jafna eftirstandandi upphæð við fjárhagslykil. Einnig er hægt að flytja eftirstöðvarnar yfir á annan viðskiptavinalykil (fyrir færslur viðskiptavinar) eða annan lánardrottin (fyrir lánardrottnafærslur) í staðinn fyrir að skilja reikningana eftir opna. 

Til að gera upp eftirstöðvarnar af síðunni **Uppgjör** skal framkvæma eftirfarandi skref:

1)  Á síðunni **Uppgjör** skal merkja við reikningana eða færslurnar sem þú vilt gera upp.
2)  Smelltu á hnappinn **Gera upp eftirstöðvar**.
3)  Svargluggi birtist sem sýnir upphæðina sem verður jöfnuð við fjárhagslykil, dagsetninginu sem verður notuð til að gera upp eftirstöðvarnar, sjálfgefinn ástæðukóða færibreytanna og sjálfgefinn lykil færibreytanna. 
4)  Veldu nýja ástæðu uppgjörs ef þú vilt breyta sjálfgefinni ástæðu. Uppgjörslykillinn breytist í lykil sem tengist ástæðukóðanum.
5)  Breyttu uppgjörslyklinum ef þú vilt.
6)  Ef þú ert að gera upp færslur viðskiptavinar og þú vilt að eftirstöðvarnar verðir færðar yfir á annan viðskiptavin skaltu velja viðskiptavin í **Jafna eftirstöðvar við viðskiptavinalykil**. Ef þú ert að gera upp færslur lánardrottins og þú vilt að eftirstöðvarnar verðir færðar yfir á annan lánardrottin skaltu velja lánardrottin í **Jafna eftirstöðvar við lánardrottnalykil**.
6)  Smelltu á **Gera upp eftirstöðvar**.
7)  Síðan **Færslubók** birtist. Aukalegri færslubókarlínu verður bætt við færslubókina þar sem upphæðin verður sú sem er á uppgjöri eftirstöðva og með mótlykilinn sem lykil fyrir uppgjör eftirstöðva. Ef þú bættir við viðskiptavini eða lánardrottni svo þú getir fært uppgjörsupphæðina yfir á annan viðskiptavin eða lánardrottin, þá verður aukalegri línu bætt við færslubókina til að færa upphæð uppgjörsins til þess viðskiptavinar eða lánardrottins.

Þegar þú bókar færslubókina verður opna færslan gerð upp að fullu. 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a>Gera upp eftirstöðvar þegar eingöngu opnar færslur eru gerðar upp
Einnig er hægt að gera upp eftirstöðvarnar þegar opnar færslur eru gerðar upp án færslubókar.

Til að gera upp eftirstöðvarnar skal framkvæma eftirfarandi skref:

1)  Á síðunni **Uppgjör** skal merkja við reikningana eða færslurnar sem þú vilt gera upp
2)  Smelltu á **Gera upp eftirstöðvar**
3)  Svargluggi birtist sem sýnir upphæðina sem verður jöfnuð við fjárhagslykil, dagsetninginu sem verður notuð til að gera upp eftirstöðvarnar, sjálfgefinn ástæðukóða færibreytanna og sjálfgefinn lykil færibreytanna. 
4)  Veldu nýja ástæðu uppgjörs ef þú vilt breyta sjálfgefinni ástæðu. Uppgjörslykillinn breytist í lykil sem tengist ástæðukóðanum.
5)  Breyttu **Uppgjörslyklinum** ef þú vilt.
6)  Ef þú ert að gera upp færslur viðskiptavinar og þú vilt að eftirstöðvarnar verðir færðar yfir á annan viðskiptavin skaltu velja viðskiptavin í **Jafna eftirstöðvar við viðskiptavinalykil**. Ef þú ert að gera upp færslur lánardrottins og þú vilt að eftirstöðvarnar verðir færðar yfir á annan lánardrottin skaltu velja lánardrottin í **Jafna eftirstöðvar við lánardrottnalykil**
7)  Einnig er hægt að velja að stofna greiðslubók með uppgjöri eftirstöðva eða einfaldlega bóka þær án greiðslubókar. Veldu **Já** fyrir **Breyta í færslubók** til að stofna greiðslubók. Þú munt geta breytt greiðslubókinni sem þú stofnar.
8)  Smelltu á **Gera upp eftirstöðvar**. Ef þú velur að stofna færslubók breytist hnappurinn í **Stofna færslubók**. Smelltu á **Stofna færslubók** í staðinn.
9)  Ef þú stofnaðir greiðslubók mun síða færslubókar opnast eftir að smellt er á **Gera upp eftirstöðvar**. Færslubókarlínu verður bætt við færslubókina þar sem upphæðin verður sú sem er á uppgjöri eftirstöðva og lykill fyrir uppgjör eftirstöðva sem mótlykilinn. Ef þú bættir við viðskiptavini eða lánardrottni svo þú getir fært uppgjörsupphæðina yfir á annan viðskiptavin eða lánardrottin, þá verður aukalegri línu bætt við færslubókina til að færa upphæð uppgjörsins til þess viðskiptavinar eða lánardrottins.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
