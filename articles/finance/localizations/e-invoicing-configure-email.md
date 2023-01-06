---
title: Skilgreina tölvupóstsrás
description: Þessi grein útskýrir hvernig skilgreina á tölvupóstsrás til að taka á móti rafrænum reikningum.
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 19339cbcc59e93289609690363b0dd9195a66f6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279871"
---
# <a name="configure-an-email-channel"></a>Skilgreina tölvupóstsrás

[!include [banner](../includes/banner.md)]

Ef eiginleiki rafrænnar reikningsfærslu sem þú stofnaðir flytur inn rafræna reikninga lánardrottna úr viðhengdum skrám sem koma í tölvupósti ættirðu að skilgreina rás tölvupóstsreiknings.

1. Í Regulatory Configuration Service (RCS) skal velja eiginleika rafrænnar reikningsfærslu sem var búinn til. Gakktu úr skugga um að þú veljir útgáfuna með stöðuna **Drög**.
2. Í flipanum **Uppsetningar** skal velja **Bæta við**.
3. Í felliglugganum **Búa til uppsetningu eiginleika**, í reitahópnum **Nýtt**, skal velja valkostinn **Sérsniðin uppsetning**.
4. Í reitahópnum **Gerð uppsetningar** skal velja valkostinn **Gagnarás**.
5. Í reitinn **Velja gagnarás** skal færa inn **Móttekinn tölvupóstur**.
6. Velja **Stofna**.
7. Veldu línuna sem þú bjóst til og veldu síðan **Breyta**.
8. Í flipanum **Gagnarás**, í hlutanum **Færibreytur**, skal stilla eftirfarandi áskilda reiti.

    | Svæði                | Lýsing |
    |----------------------|-------------|
    | Gagnarás         | Færið inn einkvæmt heiti til að auðkenna gagnarásina. Mest má nota 10 stafi í heitinu. Vísað verður í hann í gildissviðsreglum og í tengdum forritum í samskiptaferlinu. |
    | Vistfang þjóns       | Færðu inn vistfang þjónsins fyrir þjónustuaðila tölvupóstsreikningsins. Til dæmis vistfang þjónsins fyrir `https://outlook.live.com` þjónustuaðilann er imap-mail.outlook.com. |
    | Tengi þjóns          | Færðu inn númer gáttarinnar sem þjónustuaðili tölvupóstsreikningsins notar. Til dæmis er gátt netþjónsins fyrir `https://outlook.live.com` þjónustuaðilann 993. |
    | Leynilykill notandanafns     | Færðu inn heiti á leynilykli Microsoft Azure lyklageymslu sem inniheldur auðkenni fyrir notandareikning tölvupóstsins. Þennan leynilykil þarf að búa til í lyklageymslu og setja upp í þjónustuumhverfinu. |
    | Leynilykill fyrir aðgangsorð notanda | Færðu inn heiti á leynilykli lyklageymslunnar sem inniheldur aðgangsorð fyrir notandareikning tölvupóstsins. |
    | Tími útrunninn              | Hámarkstími, í millisekúndum (ms), sem kerfið á að bíða eftir svari. Sjálfgefið gildi er 10.000 ms (10 sekúndur). |
    | Aðalmappa          | Tilgreindu uppruna á innflutningi tölvupóstsins eða möppuna sem þjónustan á að vinna úr tölvupóstum frá. |
    | Skjalasafnsmappa       | Tilgreindu möppuna þar sem á að vista unna tölvupósta. Ef þessi mappa er ekki tilgreind mun kerfið sjálfkrafa búa hana til. |
    | Villumappa         | Tilgreindu möppuna sem kerfið ætti að færa tölvupósta í ef vinnslan mistekst. Ef þessi mappa er ekki tilgreind mun kerfið sjálfkrafa búa hana til. |
    | Hámarksstærð skilaboða     | Sláðu inn hámarksstærð í bætum á einu skeyti sem unnið er úr. Sjálfgefið gildi er 20.000.000 bæti. |
    | Hámarksfjöldi skilaboða   | Sláðu inn hámarksfjöldi skeyta sem á að vinna úr fyrir eina aðgerð. Ef ekki á að takmarka fjölda skeyta skal stilla gildið á **0** (núll). |
    | Frá sía          | Færðu inn streng til að sía eftir netfangi sendanda. Aðeins verður unnið úr tölvupóstum þar sem netfang sendanda passar við síuna. Þetta svæði er valkostur. Til að tilgreina mörg netföng sendenda skal aðskilja með semikommum (;). |
    | Efnissía       | Færðu inn streng til að sía eftir efni. Aðeins verður unnið úr tölvupóstum þar sem efnið passar við síuna. Þetta svæði er valkostur. Einföld sía eins og **\*smth\*.ext** er studd, þar sem hver stjarna (\*) táknar núll eða fleiri tilvik á einhverjum staf. |
    | Dagsetningarafmörkun          | Tilgreindu dagsetningu til að skilgreina hámarksaldur í dögum á skeytum sem unnið er úr. Þetta svæði er valkostur. Sjálfgefið gildi er 30 dagar. |
    | Vinnslustilling      | <p>Veldu einn af eftirfarandi valkostum til að tilgreina hvort hægt sé að vinna úr öllum viðhengjum í tölvupósti saman eða hvort eigi að vinna úr hverju viðhengi fyrir sig:</p><ul><li><b>Eftir viðhengi</b> – Nýtt rafrænt skjal verður búið til fyrir hvert viðhengi í tölvupóstinum. Ef til dæmis einn tölvupóstur inniheldur nokkrar skrár sem innihalda rafræn reikningsgögn verður litið á hverja skrá sem nýjan rafrænan reikning í kerfinu.</li><li><b>Eftir tölvupósti</b> – Litið verður á eitt viðhengi sem grunnviðhengi og einn rafrænn reikningur verður búinn til í kerfinu. Önnur viðhengi er hægt að nota sem stuðningsskrár.</li></ul> |

9. Í hlutanum **Viðhengjasía** skal bæta við upplýsingum skrársíu. Aðeins verður unnið úr viðhengjum sem uppfylla skilgreinda síu. Til dæmis mun **\*.xml** sía eftir viðhengjum sem eru með skráarendinguna .xml. Heiti viðhengisins er notað í Dynamics 365 Finance eða Dynamics 365 Supply Chain Management við uppsetningu.

    - Ef reiturinn **Vinnslustilling** er stilltur á **Eftir tölvupósti** í fyrra skrefinu er hægt að bæta við mörgum skrám hér. Heitið mun auðkenna tiltekið skjal.
    - Ef reiturinn **Vinnslustilling** er stilltur á **Eftir viðhengi** er aðeins hægt að bæta við einni síu.

10. Í flipanum **Gildissviðsreglur** skal fara yfir og uppfæra skilyrðið ef á þarf að halda. Gildið í reitnum **Rás** verður að jafngilda gildinu sem þú færðir inn í reitinn **Gagnarás** í skrefi 8.
11. Veljið **Vista** og lokið skjámyndinni.
