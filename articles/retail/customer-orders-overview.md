---
title: "Yfirlit pantana viðskiptavina"
description: "Þetta efnisatriði gefur upplýsingar um pantanir viðskiptavinar í Retail Modern POS (MPOS). Pantanir viðskiptavinar eru einnig þekktar sem sérpantanir. Efnisatriðið inniheldur umræðu um tengdar færibreytur og færsluflæði."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ce6774ede836eb29e6ef2cd8d4baa9efb931020c
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="customer-orders-overview"></a>Yfirlit pantana viðskiptavina

[!INCLUDE [banner](includes/banner.md)]

Þetta efnisatriði gefur upplýsingar um pantanir viðskiptavinar í Retail Modern POS (MPOS). Pantanir viðskiptavinar eru einnig þekktar sem sérpantanir. Efnisatriðið inniheldur umræðu um tengdar færibreytur og færsluflæði.

Í alhliða samskiptum smásölu veita margir smásalar valkost pantana viðskiptavina eða sérpantana til að mæta ýmsum þörfum afurða og uppfyllingar. Hér eru nokkrar dæmigerðar aðstæður.

-   Viðskiptavinur vill að afurð sé afhent á tilgreint aðsetur á tilgreindum degi.
-   Viðskiptavinur vill taka til afurðir úr verslun eða staðsetningu sem er önnur en verslunin eða staðsetningin þar sem viðskiptamaðurinn keypti þær afurðir.
-   Viðskiptavinur vill að einhver annar taki til afurðir sem viðskiptamaðurinn keypti.

Smásalar nota einnig pantanir viðskiptavinar til að lágmarka tapaða sölu sem birgðastöðvanir gætu annars valdið, þar sem varninginn má afhenda eða taka til á mismunandi tíma eða stað.

## <a name="set-up-customer-orders"></a>Setja upp pantanir viðskiptavinar
Hér eru nokkrar af færibreytur sem hægt er að stilla á síðunni **smásölufæribreytur** til að skilgreina hvernig pantanir viðskiptavinar eru uppfylltar:

-   **Prósenta sjálfgefinnar innborgunar** – Tilgreina upphæð sem viðskiptamaðurinn verður að borga sem innistæða áður en hægt er að staðfesta pöntun. Sjálfgefin innborgunarupphæð er reiknuð sem prósenta af virði pöntunar. Það fer eftir réttindum en aðili tengdur verslun gæti hnekkt upphæð með því að nota **Hnekking innborgunar**.
-   **Afpöntunargjald prósenta** – Ef gjald verður jafnað þegar hætt er við pöntun viðskiptavinar, skal skilgreina upphæð þess gjalds.
-   **Kóði afpöntunargjalds** – Ef gjald er sett á þegar pöntun frá viðskiptavini er afturkölluð, er það gjald sýnt með gjaldkóða á sölupöntuninni. Notaðu þessa færibreytu til að skilgreina kóða afpöntunargjalds.
-   **Kóði sendingargjalds** – Smásalar geta rukkað sérstaka þóknun fyrir afhendingu á varningi til viðskiptavinur. Upphæð þess sendingargjalds er sýnt undir gjaldkóða á sölupöntuninni. Notaðu þessa færibreytu til að varpa kóða sendingargjalds í sendingargjöld á pöntun viðskiptavinar.
-   **Endurgreiðsla sendingargjöld** – Tilgreina hvort sendingargjöld sem eru sem tengist a pöntun viðskiptavinar eru endurgreiðanleg.
-   **Hámarksupphæð án samþykkis** – Ef sendingargjöld eru endurgreiðanleg skal tilgreina hámarksupphæð endurgreiðslu sendingargjalda í skilapöntunum. Ef farið er upp fyrir þessa upphæð er hnekkingu stjórnanda þörf til að halda áfram með endurgreiðsluna. Til að koma fyrir eftirfarandi sviðsmyndum getur endurgreiðsla á sendingargjöldum farið yfir upphæðina sem var upphaflega greidd:
    -   Gjöld eru jafnað á stigi sölupöntunarhauss, og þegar sumu magni afurðarlínu er skilað, er ekki hægt að ákvarða hámarksendurgreiðslu sendingargjalda sem er leyfileg fyrir afurðir og magn á þann hátt sem virkar fyrir alla viðskiptavini smásölu.
    -   Stofnað er til sendingargjalda fyrir hvert tilvik sendingar. Ef viðskiptavinur skilar afurð mörgum sinnum og stefna smásala tilgreinir að smásalinn beri kostnað af gjöldum skilasendingar, verða sendingargjöld skila meiri en raunveruleg sendingargjöld.

## <a name="transaction-flow-for-customer-orders"></a>Færsluflæði fyrir pantanir viðskiptavinar
### <a name="create-a-customer-order-in-retail-modern-pos"></a>Stofna pöntun viðskiptavinar í Retail Modern POS

1.  Bæta skal viðskiptavini við færsluna.
2.  Bæta afurðum við körfuna.
3.  Smellið á **Stofna pöntun viðskiptavinar**, og svo velurðu gerð pöntunar. Gerð pöntunar getur verið annaðhvort **Pöntun viðskiptavinar** eða **Tilboð**.
4.  Smellt er á **Senda valið** eða **Senda allt** til að senda afurðir á aðsetur á viðskiptavinalykli, skal tilgreina áskilda sendingardagsetningu og sendingargjöld.
5.  Smellt er á **Taka til valið** eða **Taka allt til** til að velja afurðir sem verða teknar til úr núgildandi verslun eða annarri verslun á tilgreindum degi.
6.  Innheimtu innborgunarupphæðina ef innborgunar er þörf.

### <a name="edit-an-existing-customer-order"></a>Breyta fyrirliggjandi pöntun viðskiptavinar

1.  Á heimasíðunni smellirðu á **Finna pöntun**.
2.  Finna og velja pöntunina sem á að breyta. Í valmyndinni neðst á síðunni er valið **Breyta**.

### <a name="pick-up-an-order"></a>Taka til pöntun

1.  Á heimasíðunni smellirðu á **Finna pöntun**.
2.  Velja pöntunina sem á að taka til. Í valmyndinni neðst á síðunni er valið **Tiltekt og pökkun**.
3.  Smelltu á **Taka tiltaka til**.

### <a name="cancel-an-order"></a>Hætta við pöntun

1.  Á heimasíðunni smellirðu á **Finna pöntun**.
2.  Velja pöntunina sem á að hætta við. Í valmyndinni neðst á síðunni er valið **Hætta við**.

#### <a name="create-a-return-order"></a>Stofna skilapöntun

1.  Á heimasíðunni smellirðu á **Finna pöntun**.
2.  Velurðu pöntun til að skila, velurðu reikningur fyrir pöntun, og svo velurðu afurðarlínu fyrir varninginn til að skila.
3.  Í valmyndinni neðst á síðunni er valið **Skilapöntun**.

## <a name="asynchronous-transaction-flow-for-customer-orders"></a>Ósamstillt færsluflæði fyrir pantanir viðskiptavinar
Hægt er að stofna pantanir viðskiptavinar úr biðlara sölustaðar (POS) í annaðhvort samstilltum eða ósamstilltum ham.

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a>Gera virkt að pantanir viðskiptavinar séu stofnaðar í ósamstilltum ham

1.  Smelltu á **Smásala** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Forstilling sölustaðar** &gt; **Virknireglur**.
2.  Á flipanum **Almennt** stillirðu valkostinn **Stofna viðskiptavinapöntun í ósamstilltri stillingu** á **Já**.

Þegar valkosturinn **Stofna pöntun viðskiptavinar í ósamstilltri stillingu** er stilltur á **Já** verða pantanir viðskiptavinar alltaf stofnaðar í ósamstilltum ham, jafnvel þó að Retail Transaction Service (RTS) er tiltækt. Ef þessi valkostur er stilltur á **Nei** verða pantanir viðskiptavinar alltaf stofnaðar í samstilltum ham með því að nota RTS. Þegar pantanir frá viðskiptavinum eru stofnaðar í ósamstilltum ham eru þær sóttar og settar inn í Retail með P-vinnslum. Samsvarandi sölupantanir eru stofnaðar í Retail þegar **Samstilla pantanir** er keyrt annaðhvort handvirkt eða með runuvinnslu.

<a name="see-also"></a>Sjá einnig
--------

[Fjölpantanir viðskiptavinar](hybrid-customer-orders.md)




