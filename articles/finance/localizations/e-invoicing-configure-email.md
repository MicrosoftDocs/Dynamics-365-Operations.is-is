---
title: Stilltu tölvupóstrás
description: Þetta efni útskýrir hvernig á að stilla tölvupóstrás til að taka á móti rafrænum reikningum.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6a5896a033212cf0f29f686eec0ab6fb3bc1d2a6
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371928"
---
# <a name="configure-an-email-channel"></a>Stilltu tölvupóstrás

[!include [banner](../includes/banner.md)]

Ef rafræn reikningseiginleikinn sem þú bjóst til flytur inn rafræna lánardrottnareikninga úr meðfylgjandi skrám sem berast með tölvupósti, ættir þú að stilla tölvupóstreikningsrás.

1. Í Regulatory Configuration Service (RCS) skaltu velja eiginleikann Rafræn reikningagerð sem þú bjóst til. Gakktu úr skugga um að þú veljir útgáfuna sem hefur stöðuna **Drög**.
2. Á **Uppsetningar** flipa, veldu **Bæta við**.
3. Í **Búðu til eiginleikauppsetningu** fellivalmynd, í **Nýtt** reitahópur, veldu **Sérsniðin uppsetning** valmöguleika.
4. Í **Gerð uppsetningar** reitahópur, veldu **Gagnarás** valmöguleika.
5. Í **Veldu gagnarás** reit, slá inn **Kominn tölvupóstur**.
6. Velja **Stofna**.
7. Veldu línuna sem þú bjóst til og veldu síðan **Breyta**.
8. Á **Gagnarás** flipa, í **Færibreytur** kafla, stilltu eftirfarandi nauðsynlega reiti.

    | Reitur                | Lýsing |
    |----------------------|-------------|
    | Gagnarás         | Sláðu inn einstakt nafn til að auðkenna gagnarásina. Nafnið má að hámarki vera 10 stafir. Það verður vísað til þess í gildandi reglum og í tengdum forritum meðan á samskiptaferlinu stendur. |
    | Vistfang þjóns       | Sláðu inn netfang netþjóns netþjónustuveitunnar. Til dæmis, vistfang netþjónsins fyrir`https://outlook.live.com` veitandi er imap-mail.outlook.com. |
    | Tengi þjóns          | Sláðu inn númer gáttarinnar sem póstveitan notar. Til dæmis, miðlarahöfnin fyrir`https://outlook.live.com` veitandi er 993. |
    | Leynilykill notandanafns     | Sláðu inn nafnið á Microsoft Azure Key Vault leyndarmál sem inniheldur auðkenni notendareiknings tölvupóstsins. Þetta leyndarmál verður að búa til í Key Vault og setja upp í þjónustuumhverfi þínu. |
    | Leynilykill fyrir aðgangsorð notanda | Sláðu inn nafn Key Vault leyndarmálsins sem inniheldur lykilorð notendareiknings tölvupóstsins. |
    | Tímalokun              | Hámarkstími, í millisekúndum (ms), sem kerfið ætti að bíða eftir svari. Sjálfgefið gildi er 10.000 ms (10 sekúndur). |
    | Aðalmappa          | Tilgreindu innflutningsuppsprettu tölvupósts eða möppuna sem þjónustan á að vinna tölvupóst úr. |
    | Skjalasafnsmappa       | Tilgreindu möppuna þar sem unnin tölvupóstur ætti að geyma. Ef þú tilgreinir ekki þessa möppu mun kerfið sjálfkrafa búa hana til. |
    | Villumappa         | Tilgreindu möppuna sem kerfið á að flytja tölvupóst í ef vinnslan mistekst. Ef þú tilgreinir ekki þessa möppu mun kerfið sjálfkrafa búa hana til. |
    | Hámarksstærð skilaboða     | Sláðu inn hámarksstærð, í bætum, af einstökum skilaboðum sem eru unnin. Sjálfgefið gildi er 20,000,000 bæti. |
    | Hámarksfjöldi skilaboða   | Sláðu inn hámarksfjölda skeyta til að vinna úr fyrir eina aðgerð. Ef þú vilt ekki takmarka fjölda skeyta skaltu stilla gildið á **0** (núll). |
    | Frá sía          | Sláðu inn streng til að sía eftir heimilisfangi sendanda. Aðeins tölvupóstur þar sem heimilisfang sendanda passar við síuna verða unnar. Þessi reitur er valfrjáls. Til að tilgreina mörg sendandanetföng, notaðu semíkommur (;) sem skilgreinar. |
    | Efnissía       | Sláðu inn streng til að sía eftir efni. Aðeins tölvupóstur þar sem viðfangsefnið passar við síuna verða unnin. Þessi reitur er valfrjáls. Einfaldur maski eins og **\* smth\* .ext** er stutt, þar sem hver stjörnu (\*) táknar núll eða fleiri tilvik af hvaða staf sem er. |
    | Dagsetningarafmörkun          | Tilgreindu dagsetningu til að skilgreina hámarksaldur, í dögum, á skilaboðum sem eru unnin. Þessi reitur er valfrjáls. Sjálfgefið gildi er 30 dagar. |
    | Vinnslustilling      | <p>Veldu einn af eftirfarandi valkostum til að tilgreina hvort hægt sé að vinna öll viðhengi í tölvupósti saman eða hvort vinna eigi hvert viðhengi sérstaklega:</p><ul><li><b>Með viðhengi</b> – Nýtt rafrænt skjal verður búið til fyrir hvert viðhengi í tölvupóstinum. Til dæmis, ef einn tölvupóstur inniheldur nokkrar skrár sem innihalda rafræn reikningsgögn, mun hver skrá teljast nýr rafrænn reikningur í kerfinu.</li><li><b>Með tölvupósti</b> – Eitt viðhengi telst grunnviðhengi og einn rafrænn reikningur verður til í kerfinu. Hægt er að nota önnur viðhengi sem stuðningsskrár.</li></ul> |

9. Í **Viðhengissía** kafla skaltu bæta við skráasíuupplýsingunum. Aðeins viðhengi sem uppfylla skilgreinda síu verða unnin. Til dæmis, **\* .xml** mun sía fyrir viðhengi sem hafa .xml skráarheiti. Heiti viðhengisins er notað í Dynamics 365 Finance eða Dynamics 365 Supply Chain Management við uppsetningu.

    - Ef þú stillir **Vinnsluhamur** sviði til **Með tölvupósti** í fyrra skrefi geturðu bætt við mörgum síum hér. Nafnið mun auðkenna tiltekna skjalið.
    - Ef þú stillir **Vinnsluhamur** sviði til **Með viðhengi**, þú getur aðeins bætt við einni síu.

10. Á **Gildisreglur** flipa, endurskoða og uppfæra viðmiðin eftir þörfum. Verðmæti **Rás** reiturinn verður að jafngilda gildinu sem þú slóst inn í **Gagnarás** reit í skrefi 8.
11. Veljið **Vista** og lokið skjámyndinni.
