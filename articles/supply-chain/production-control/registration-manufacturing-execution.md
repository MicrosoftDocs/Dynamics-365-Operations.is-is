---
title: Skráning fyrir framkvæmd framleiðslu
description: Þessi efnisgrein lýsir grundvallarhugtökum sem verður að skilja til að skilgreina og nota framkvæmd framleiðslu.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 70103
ms.assetid: 52ba1cdd-767f-4edd-896f-61adce8479d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df34d1c0a57f8890dab83ad2284deb0514b128fb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430613"
---
# <a name="registration-for-manufacturing-execution"></a>Skráning fyrir framkvæmd framleiðslu

[!include [banner](../includes/banner.md)]

Þessi efnisgrein lýsir grundvallarhugtökum sem verður að skilja til að skilgreina og nota framkvæmd framleiðslu. 

Framkvæmd framleiðslu er fyrst og fremst ætlað að vera notuð af framleiðslufyrirtækjum. Starfsmenn geta skráð tíma og vörunotkun í framleiðsluvinnslu með því að nota síðuna **Starfsskráning**. Allar skráningar eru samþykktar og síðan fluttar í viðkomandi einingar. Samfelld samþykkt og flutningur skráninga gefa stjórnendum kleift að rekja auðveldlega raunkostnað í framleiðslupöntunum.

## <a name="manufacturing-execution-and-registration-terminology"></a>Framkvæmd og skráning framleiðslu, orðalisti
Eftirfarandi tafla inniheldur hugtök sem tengjast framkvæmd framleiðslu og tengd skráningarverkefni.

| Hugtak                          | lýsing                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Framkvæmd framleiðslu       | Aðgerð sem er notuð til að skrá tíma, efnisnotkun, kostnað á framleiðsluvinnslu, verk og óbeina verkþætti. Skráning er framkvæmd í skráningarbiðlara framkvæmd framleiðslu.                                                                                                                                                                                                                                                                                                                                                                                                   |
| Vinnslulisti                      | Á síðunni **Starfsskráning** sjá starfsmenn lista yfir vinnslur sem þeir verða að framkvæma á tiltekin tilföng, eins og vél. Starfsmaður getur skrá vörunotkun og tími á hvert verk eða verkefni í vinnslulista.                                                                                                                                                                                                                                                                                                                                                                           |
| Vinnslusamtvinnun                  | Ef starfsmaður byrjar fleiri en eina vinnslu á sama tíma á síðunni **Starfsskráning** er það kallað vinnslusamtvinnun. Tími sem notaður er í samtvinnaðar vinnslur er hægt að úthluta á einstakar vinnslur á mismunandi hátt með því að nota úthlutunarlykla.                                                                                                                                                                                                                                                                                                                                                         |
| Verkefnisstjóra/aðstoðarmanns skráningar | Starfsmaður getur skráð sig sem aðstoðarmann á tilfang og stofna lítið teymi þar sem nokkrir starfsmenn vinna við sama framleiðsluverk. Tilföng sem starfsmenn eru tengdir sem aðstoðarmenn eru kallaðir hafnsögumaður. Aðeins verkefnisstjóri tilfanga á að gera skráningar. Allir aðstoðarmenn fá sjálfkrafa sömu skráningu. Ef t.d. vél virkar sem verkefnisstjóri, geta starfsmenn sem er skráðir sem aðstoðarmaður þeirrar vélar gert skráningu á síðunni **Starfsskráning**, og bæði vélin og starfsmennirnir sem eru tengdir sem aðstoðarmenn fá sömu skráningu. |
| Óbeinn verkþáttur             | Verkþáttur eða verkefni sem er ekki í beinum tengslum við framleiðsluverk eða -verkefni, t.d. deildarfundur, þrif eða viðhaldsverk í vinnslusal. Starfsmenn geta gert skráningu á óbeinum aðgerðum°á sama hátt og°þeir geta skráð sig í framleiðsluvinnslu og verk.                                                                                                                                                                                                                                                                                                |

## <a name="registrations-in-manufacturing-execution"></a>Skráningar í framkvæmd framleiðslu
Starfsmenn geta gert ýmsar gerðir af skráningum í framleiðsluframkvæmd fyrir vinnslur í°framleiðsluverkum. Eftir uppsetningu kerfisins, gæti einnig gæti verið mögulegt fyrir starfsmenn að gera skráningu í verkþætti og óframleiðinna verkefni svo sem hlé, fjarvistir og óbeina verkþætti. Skráningargerðir eru eftirfarandi:

-   **Innstimplun/útstimplun** (tiltækur með Tími og viðvera) -°Starfsmenn stimpla sig inn þegar þeir°koma í vinnuna og stimpla sig út þegar þeir fara heim.
-   **Skrá í framleiðsluvinnslur** - Starfsmaður getur gert skráningar, eins og vinnsla er ræst og skýrslusvörun vegna verks við framleiðsluvinnslur sem eru birtar í vinnslulista hans. Starfsmenn geta ræst nokkrar vinnslur samtímis. Vísað er í þetta sem vinnslusamtvinnun.
-   **Skrá í birgðum** - Starfsmenn geta gert skráningar á efni sem er notað í vinnslusal en°sem eru ekki tengd beint við framleiðsluverk. Dæmi eru feiti, smurefni eða önnur efni notuð til að halda vélum í gangi. Skráning er gerð í birgðabók.
-   **Skrá verk** (tiltækt í Tími og viðvera) - Starfsmenn geta gert skráningar, eins og upphaf og lok vinnu á verk eða verkþætti sem birtast í vinnslulista þeirra.
-   **Skrá verkgjöld og verkatriði** (tiltækt í Tími og viðvera) - Starfsmenn geta skráð þóknanir (útgjöld) sem eru tengdar við verk í verkþóknunarbók, eins og akstur og brúartolla. Starfsmenn geta einnig skráð notkun vara í verkum. Þetta er framkvæmt í vörubók verks.
-   **Skrá sig sem aðstoðarmann annars starfsmanns** Ef tveir eða fleiri starfsmenn vinna saman framleiðsluvinnslu eða verk, getur starfsmaður skráð sig sem aðstoðarmaður vélar eða annars starfsmanns sem mun þá vera eins og verkefnisstjórinn. Ef þörf krefur, getur verkefnisstjóri valið annan starfsmann sem verkefnisstjóra.
-   **Skrá fjarvist** (tiltækt í Tími og viðvera) - Starfsmenn geta skráð tíma á mismunandi fjarvistarkóða sem eru settir upp. Það er hægt að gefa til kynna°fjarvist ef starfsmaður kemur of seint, þarf fjarveru á vinnudegi, eða fer fyrr en búist er við í samræmi við staðlaðar forstillingar vinnutíma.
-   **Skrá hlé** (tiltækt í Tími og viðvera) - Yfir vinnudaginn geta starfsmenn skráð ef þeir yfirgefa vinnustöð sína til að taka sér hlé. Setja má upp ýmsar gerðir hlé. Þegar starfsmaðurinn kemur og skráir sig aftur, skráir kerfið að starfsmaðurinn er kominn aftur og stöðvar skráningu vinnuhléa.
-   **Skrá óbeina verkþætti** (tiltækt í Tími og viðvera) –°Óbeinir verkþættir eru framleiðslulausir verkþættir sem starfsmenn gætu sinnt yfir vinnudaginn, eins og deildarfundur, hópfundur eða viðhaldsverk sem fer fram í vinnslusal. Starfsmenn geta gert skráningar á óbeina verkþætti sem eru settir upp.
-   **Skrá yfirvinnu** (tiltækt í Tími og viðvera) -°Starfsmenn sem hafa verið beðnir að vinna lengri vinnudag°geta valið hvort á að skrá aukavinnuna sem sveigjanlegan vinnutíma eða yfirvinnu.




