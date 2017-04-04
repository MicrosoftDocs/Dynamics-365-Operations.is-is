---
title: "Yfirlit yfir pantanir viðskiptavina"
description: "Þetta efni veitir upplýsingar um pantanir viðskiptavina í Retail Modern POS (MPOS). Pantanir viðskiptavinar eru einnig þekkt sem ákveðnar pantanir. Efnisatriði umræðu flæði færsluna og tengdar færibreytur."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2f466dfe53ccf0be15ed0793b4a6dd371bdacc0d
ms.lasthandoff: 03/31/2017


---

# <a name="customer-orders-overview"></a>Yfirlit yfir pantanir viðskiptavina

Þetta efni veitir upplýsingar um pantanir viðskiptavina í Retail Modern POS (MPOS). Pantanir viðskiptavinar eru einnig þekkt sem ákveðnar pantanir. Efnisatriði umræðu flæði færsluna og tengdar færibreytur.

Á omni rásina retail heiminum og margar smásala útvega valkostinn viðskiptavina eða ákveðnar pantanir á kröfum mismunandi afurð og uppfyllingar. Hér eru sum dæmigerðar aðstæður:

-   Viðskiptavinur vill afurðir sem á að afhenda tilteknar aðsetur á tiltekinni dagsetningu.
-   Viðskiptavinur vill taka afurðir úr verslun eða staðsetningu sem er önnur en verslunina eða staðsetningu þar sem viðskiptavinurinn keypt þessar afurðir.
-   Viðskiptavinur vill sannvottunarverkefni til að taka til vörur sem viðskiptavinurinn er keypt.

Smásala einnig nota pantanir viðskiptavina til að lágmarka tapað birgðatalning stöðvanir annars leitt, þar sem hægt er að afhenda varninginn eða taka til í mismunandi tíma eða stað vsk.

## <a name="set-up-customer-orders"></a>Setja upp pantanir viðskiptavina
Hér eru sumra færibreytanna sem hægt er að setja á í **færibreytur Retail** síðu til að tilgreina hvernig pantanir viðskiptavina eru uppfyllt:

-   **Sjálfgefin innborgunarprósenta** – Tilgreinið upphæð sem viðskiptavinur verður að greiða sem innborgun áður en hægt er að staðfesta pöntun. Sjálfgefin innborgunarupphæð er reiknaður sem prósenta af pöntuninni gildi. Eftir réttindi, aðstoðarmaður í verslun gæti verið hægt að hnekkja upphæð með því að nota **hnekking Innborgunar**.
-   **Prósenta afpöntunargjalds** – Ef gjald verða notaðar þegar hætt er við pöntun viðskiptavinar tilgreina upphæð gjalds sem.
-   **Kóði afpöntunargjalds** – Ef gjald verða notaðar þegar hætt er við pöntun viðskiptavinar gjald verður fram undir kóði sendingargjalds á sölupöntun í Microsoft Dynamics AX. Notið þessa færibreytu til að skilgreina kóða gjalda afturköllunar.
-   **Kóða sendingargjalds** – Smásala hægt er að færa inn aukalegar gjald fyrir varninginn á sendingu til viðskiptavinar. Upphæð sem sendingargjald endurspeglast undir kóði sendingargjalds á sölupöntun í Dynamics AX. Notið þessa færibreytu til að varpa kóði sendingargjalds sendingargjöld pöntun viðskiptavinar.
-   **Endurgreiða sendingargjöld** – Tilgreinir hvort sendingargjöld sem eru tengdar við pöntun viðskiptavinar refundable.
-   **Hámarksupphæð án samþykkis** – Ef sendingargjöld eru refundable, tilgreina hámarksupphæð sendingu endurgreiðslur gjöld fyrir skilapantanir. Ef farið er yfir þá upphæð hnekkingu stjórnanda þarf að halda áfram með endurgreiðsluna. Til að hýsa við eftirfarandi kringumstæður, endurgreiðsla fyrir sendingargjöld yfir upphæðin sem var upphaflega greidd:
    -   Gjöld eru notuð stigi í haus sölupöntunarinnar og þegar eitthvert magn línunnar afurð er skilað, hámark endurgreiðsla fyrir sendingargjöld sem er leyfð fyrir afurðir og magnið er ekki hægt að ákvarða hátt virkar fyrir alla viðskiptavini í smásölu.
    -   Sendingargjöld eru til fyrir hvert tilvik sendingar. Ef viðskiptavinur skilar vörur mörgum sinnum og retailer sem reglan tilgreinir að á retailer verður hafið hámarksjöfnunin kostnaðar vegna skila flutningsgjalda, skila sendingargjöld verður hærri en raunveruleg sendingargjöld.

## <a name="transaction-flow-for-customer-orders"></a>Flæði færslu fyrir pantanir viðskiptavina
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Stofna pöntun viðskiptavinar í Retail Modern POS

1.  Bæta skal viðskiptavini við færsluna.
2.  Bæta afurðum í körfuna.
3.  Smellið á **pöntun viðskiptavinar Stofnuð**, og veljið síðan gerð pöntunar. Gerð pöntunar getur verið annað hvort **pöntun Viðskiptavinar** eða **Tilboðs**.
4.  Smellið á **Senda valið** eða **Senda allt** senda afurðir til aðsetur á reikningi viðskiptavinar, tilgreina umbeðin sendingardagsetning og tilgreina sendingargjöld.
5.  Smellið á **valið að Sækja** eða **þar sem sótt allar** til að velja afurðir sem verður að sækja úr núgildandi verslun eða aðra verslun á tiltekinni dagsetningu.
6.  Safna innborgunarupphæð, ef þörf er á innborgun.

### <a name="edit-an-existing-customer-order"></a>Breyta fyrirliggjandi pöntun viðskiptavinar

1.  Fara á upphafssíðu, smellið á **Finna pöntun**.
2.  Finna og velja pöntunina sem á að breyta. Neðst á síðunni, smellið á **Breyta**.

### <a name="pick-up-an-order"></a>Sækja pöntun

1.  Fara á upphafssíðu, smellið á **Finna pöntun**.
2.  Veldu pöntunina sem á að sækja. Neðst á síðunni, smellið á **Tiltekt og pökkun**.
3.  Smellið á **Sækja**.

### <a name="cancel-an-order"></a>Hætta við pöntun

1.  Fara á upphafssíðu, smellið á **Finna pöntun**.
2.  Veldu pöntunina sem á að hætta við. Neðst á síðunni, smellið á **hætta Við**.

#### <a name="create-a-return-order"></a>Stofna skilapöntun

1.  Fara á upphafssíðu, smellið á **Finna pöntun**.
2.  Velja pöntunina sem á að skila, veljið reiknings fyrir pöntun og veljið svo framleiðslulína fyrir varning að skila.
3.  Neðst á síðunni, smellið á **Skilapöntun**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Flæði ósamstillt færslu fyrir pantanir viðskiptavina
Hægt er að stofna pantanir viðskiptavina af biðlara sölustaðar í ham fyrir samstillt eða ósamstillt ham.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Virkja pantanir viðskiptavina til að stofna í ham fyrir ósamstillt

1.  Í Dynamics AX er smellt á **Smásölu og commerce**&gt;**Rásar uppsetningu**&gt;**uppsetning Smásölustaðar**&gt;**POS forstillingu**&gt;**virknireglur**.
2.  Á við **Almennt** FastTab, setja í **Stofna pöntun viðskiptavinar í ham fyrir async** valkostinn að **Já**.

Þegar á **Stofna pöntun viðskiptavinar í stillingu async** valkostur er stilltur á **Já**pantanir viðskiptavina eru alltaf stofnuð í ham fyrir ósamstillt, jafnvel þó að Retail Transaction Service (RTS) er tiltækt. Ef þessi valkostur er stilltur á **Nei**, pantanir viðskiptavina eru alltaf stofnuð í samstillt afhendingarmáta með notkun RTS. Þegar pantanir viðskiptavina eru stofnaðar í ham fyrir ósamstillt, eru þær tekið og fært inn í Dynamics AX með vinnslur Sækja (P). Samsvarandi sölupantanir eru stofnaðar í Dynamics AX þegar **Samstilla pantanir** er að keyra annað hvort handvirkt eða með runu vinnslu.

<a name="see-also"></a>Sjá einnig
--------

[Hybrid pantanir viðskiptavina](hybrid-customer-orders.md)


