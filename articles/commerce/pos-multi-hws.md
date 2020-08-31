---
title: Sérstakar greiðslustöðvar og kvaðningar fyrir prentara og peningaskúffu
description: Í þessu efnisatriði er að finna upplýsingar um möguleikann á því að vera með sérstaka greiðslustöð og biðja notandann að velja peningaskúffu og kvittanaprentara.
author: rubendel
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 41b0faa7ef24bdae229f7e6760d22357cb87eb0d
ms.sourcegitcommit: 7b7cc93c0f78c6bfc7a3ea66a74a29ba0f218553
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/04/2020
ms.locfileid: "3658359"
---
# <a name="dedicated-payment-terminals-and-prompts-for-a-printer-and-cash-drawer"></a>Sérstakar greiðslustöðvar og kvaðningar fyrir prentara og peningaskúffu

[!include [banner](includes/banner.md)]

Í þessu efnisatriði er að finna upplýsingar um möguleikann á því að vera með sérstaka greiðslustöð og biðja notandann að velja peningaskúffu og kvittanaprentara.

## <a name="overview"></a>Yfirlit

Smásöluaðilar nú til dags leita leiða til að einfalda greiðsluupplifun í verslun. Nýleg þróun í átt að pappírslausu greiðsluferli í gegnum rafrænar greiðslur auðvelda ekki aðeins að gera innkaupaupplifunina þægilegri heldur einnig draga úr nauðsyn þess að vera með öll jaðartæki til reiðu fyrir hvern starfsmann verslunar.

Microsoft Dynamics 365 Commerce styður þessa þróun með því að virkja aðstæður þar sem tæki sölustaðar er með sérstaka greiðslustöð úthlutaða allan tímann, en er ekki með eigin kvittanaprentara eða peningaskúffu. Þegar söluaðilar verða að prenta kvittun eða taka við peningagreiðslu eru þeir beðnir um að velja vélbúnaðarstöð þar sem þessi tæki eru skilgreind.

## <a name="key-terms"></a>Lykilhugtök

| Hugtak | lýsing |
|---|---|
| Skrá | Einingin sem er notuð til að skilgreina tilvik afgreiðslukassa. |
| Tæki | Framsetning á efnislegu tilviki afgreiðslukassa og Modern POS-forriti sem því er úthlutað. |
| Sérhæfð vélbúnaðarstöð | Viðskiptagrunnur vélbúnaðarstöðvar sem er byggður inn í Modern POS fyrir Windows og Modern POS fyrir Android-forrit. |
| Tengi skúffuopnara | Hefðbundin aðferð til að tengja peningaskúffu við kvittanaprentara. |
| Net jaðarbúnaðar | Innbyggður stuðningur fyrir nettengdar greiðslustöðvar, kvittanaprentara og peningaskúffur. |

## <a name="supported-pos-clients-and-devices"></a>Studdir biðlarar sölustaðar og tæki

Virkninni sem lýst er í þessu efnisatrið er studd af Modern POS fyrir Windows og Modern POS fyrir biðlara Android POS.

Þessi virkni styður nettengdar greiðslustöðvar og kvittanaprentara. Hægt er að bjóða upp á stuðning við peningaskúffu með því að tengja peningaskúffuna við nettengdan kvittanaprentara í gegnum tengi skúffuopnara.

Tilbúinn stuðningur fyrir þessa virkni er í boði [Greiðslutengil Dynamics 365 fyrir Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Hins vegar gætu aðrir greiðslutenglar verið studdir í gegnum hugbúnaðarþróunarpakka Commerce fyrir greiðslur. Studdir kvittanaprentarar samanstanda af nettengdum kvittanaprenturum frá Star Micronics og Epson.

Til að setja upp kvittanaprentara Star Micronics skal nota hjálparforrit Star Micronics Printer til að skilgreina tækið svo hægt sé að nota það yfir netið. Þetta hjálparforrit gefur einnig upp IP-tölu tækisins.

Til að setja upp kvittanaprentara Epson skal nota hjálparforrit Epson ePOS-Print til að setja upp tækið til að nota netsamskiptareglur.

Frekari upplýsingar um hvernig á að setja upp netjaðartæki er að finna í [Yfirlit notendaþjónustu netjaðartækja](https://go.microsoft.com/fwlink/?linkid=2129965).

## <a name="set-up-a-dedicated-payment-terminal-and-a-prompt-for-a-printer-and-cash-drawer"></a>Setja upp sérhæfða greiðslustöð og kvaðningu fyrir prentara og peningaskúffu

### <a name="set-up-hardware-profiles"></a>Setja upp vélbúnaðarreglur

Nauðsynlegt er að vera með tvær gerðir af vélbúnaðarreglum. Þeirri fyrri er úthlutað á afgreiðslukassann. Þeirri seinni er úthlutað á vélbúnaðarstöð á verslunarstigi, og er notuð til að flokka á röklegan hátt nettengda kvittunarprentara og peningaskúffur.

#### <a name="set-up-a-hardware-profile-for-the-register"></a>Setja upp vélbúnaðarreglu fyrir afgreiðslukassa

Til að setja upp vélbúnaðarreglu sem úthlutað er á afgreiðslukassa skal fylgja þessum skrefum.

1. Í Dynamics 365 Commerce skal leita að **Vélbúnaðarregla**.
2. Veljið **Nýtt**.
3. Úthlutið númeri vélbúnaðarreglu og færið síðan inn lýsingu. Þessari vélbúnaðarreglu verður úthlutað á afgreiðslukassann sjálfan. Þess vegna nægir lýsing á borð við **Sérhæfð með til vara**.
4. Í flýtiflipanum fyrir mismunandi tækjagerðir skal setja upp eftirfarandi tækjagerðir.

    | Tæki | Gerð | Nafn tækis | Frekari upplýsingar |
    |---|---|---|---|
    | Prentari | Til vara | **Epson** eða **Star** | Heiti tækis er stafrétt. **Forstillingarkenni kvittunar** ætti að vera það sama og **Forstillingarkenni kvittunar** sem er varpað í nettengdan prentara sem er uppsettur í vélbúnaðarreglunni sem úthlutað er á vélbúnaðarstöðina á stigi rásar. |
    | Peningaskúffa | Til vara | **Epson** eða **Star** | Heiti tækis er stafrétt. Stillið **Notaðu samnýtta vakt** valkostinn á **Já**. |
    | Kortamillifærsla | Adyen | Ekki tiltækt | Frekari upplýsingar um hvernig setja á upp tilbúinn Adyen-tengil er að finna í [Greiðslutengill Dynamics 365 fyrir Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3). Aðra greiðslutengla er hægt að styðja í gegnum [Hugbúnaðarþróunarpakka Commerce fyrir greiðslur](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/end-to-end-payment-extension). |
    | PIN-takkaborð | Net | **MicrosoftAdyenDeviceV001** | Ekkert. |

5. Í Dynamics 365 Commerce skal leita að **Afgreiðslukassar**.
6. Velja skal afgreiðslukassa með því að velja númer afgreiðslukassa og velja svo **Breyta**.
7. Úthlutið vélbúnaðarreglunni sem var búin til á afgreiðslukassa sem á að nota sérhæfða greiðslustöð. Tækið sem er varpað í þennan afgreiðslukassa verður að nota annaðhvort Windows-forrit eða Modern POS fyrir Android-forrit.
8. Veljið **Vista**.
9. Á aðgerðasvæðinu, í flipanum **Afgreiðslukassar**, skal velja **Skilgreina IP-tölur**.
10. Í flýtiflipanum **PIN-takkaborð** skal slá inn IP-tölu greiðslustöðvarinnar. Frekari upplýsingar um hvernig finna á IP-tölu greiðslustöðvarinnar með því að nota Adyen-tengilinn er að finna í [Greiðslutengill Dynamics 365 fyrir Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3).
11. Veljið **Vista**.

#### <a name="set-up-a-hardware-profile-for-the-receipt-printer-and-cash-drawer"></a>Setja upp vélbúnaðarreglu fyrir kvittanaprentara og peningaskúffu

Til að setja upp vélbúnaðarreglu sem er notuð til að flokka nettengda kvittanaprentara og peningaskúffur skal fylgja þessum skrefum.

1. Í Dynamics 365 Commerce skal leita að **Vélbúnaðarregla**.
2. Veljið **Nýtt**.
3. Úthlutið númeri vélbúnaðarreglu og færið síðan inn lýsingu. Þessi vélbúnaðarregla verður notuð til að flokka kvittanaprentara og peningaskúffu. Þess vegna nægir lýsing á borð við **Nettengdur prentari og peningaskúffa**.
4. Í flýtiflipanum fyrir mismunandi tækjagerðir skal setja upp eftirfarandi tækjagerðir.

    | Tæki | Gerð | lýsing | Frekari upplýsingar |
    |---|---|---|---|
    | Prentari | Net | **Epson** eða **Star** | Heiti tækis er stafrétt. **Forstillingarkenni kvittunar** ætti að vera það sama og **Forstillingarkenni kvittunar** sem er varpað í prentara sem er uppsettur í vélbúnaðarreglunni sem úthlutað er á afgreiðslukassann. |
    | Peningaskúffa | Til vara | **Epson** eða **Star** | Heiti tækis er stafrétt. stillið **Notaðu samnýtta vakt** valkostinn á **Já**. |

5. Veljið **Vista**.

### <a name="set-up-hardware-stations"></a>Setja upp vélbúnaðarstöðvar

Tvær vélbúnaðarstöðvar eru nauðsynlegar. Þeirri fyrri verður varpað í afgreiðslukassann. Sú seinni verður valin því gerð er krafa um slíkt í hvert skipti sem prenta þarf kvittun eða opna þarf peningaskúffu.

#### <a name="register-a-hardware-station"></a>Skrá vélbúnaðarstöð

1. Í Dynamics 365 Commerce skal leita að **Allar verslanir**.
2. Veljið verslun með því að velja gildið **Auðkenni smásölurásar** og velja svo **Breyta**.
3. Í flýtiflipanum **Vélbúnaðarstöðvar** skal velja **Bæta við**.
4. Stillið reitinn **Gerð vélbúnaðarstöðvar** á **Sérnýtt**.
5. Sláið inn lýsingu, en ekki stilla önnur gildi fyrir þessa vélbúnaðarstöð. Þessi vélbúnaðarstöð verður notuð fyrir afgreiðslukassann öllum stundum. 

#### <a name="set-up-a-hardware-station-for-the-receipt-printer-and-cash-drawer"></a>Setja upp vélbúnaðarstöð fyrir kvittunarprentara og peningaskúffu

1. Í Dynamics 365 Commerce skal leita að **Allar verslanir**.
2. Veljið verslun með því að velja gildið **Auðkenni smásölurásar** og velja svo **Breyta**.
3. Í flýtiflipanum **Vélbúnaðarstöðvar** skal velja **Bæta við**.
4. Stillið reitinn **Gerð vélbúnaðarstöðvar** á **Sérnýtt**.
5. Færðu inn lýsingu. Þessi vélbúnaðarstöð verður notuð fyrir kvittanaprentara og peningaskúffu.
6. Í reitnum **Vélbúnaðarregla** skal velja vélbúnaðarregluna sem var búin til fyrir kvittanaprentara og peningaskúffu.
7. Veljið **Vista**.
8. Á meðan vélbúnaðarstöðin fyrir kvittanaprentara og peningaskúffu er enn valin skal velja **Skilgreina IP-tölur**.
9. Fáið IP-töluna fyrir prentarann og færið hana inn sem IP-tölu fyrir bæði kvittanaprentara og peningaskúffu.
10. Veljið **Vista**
11. Leitið að **Dreifingaráætlanir**.
12. Veljið dreifingaráætlun **1090** og veljið síðan **Keyra núna**.
13. Veljið dreifingaráætlun **1070** og veljið síðan **Keyra núna**.

### <a name="set-up-the-system-to-prompt-for-receipt-printer-and-cash-drawer-selection-as-its-required"></a>Setja upp kerfið til að biðja um val á kvittanaprentara og peningaskúffu eins og þörf er á

1. Í studdum biðlara sölustaðar skal loka núverandi vakt ef vakt er opin.
2. Skráðu þig inn og veldu síðan **Skúffuaðgerðir utan skúffu**.
3. Notið aðgerðina **Stjórna vélbúnaðarstöðvum** til að kveikja á vélbúnaðarstöð.
4. Veljið vélbúnaðarstöðina sem var búin til fyrir afgreiðslukassann til að gera hana virkan.
5. Skráðu þig út úr sölustað, inn aftur og opnaðu vakt.

Greiðslustöðinni sem er úthlutað á vélbúnaðaregluna verður nú alltaf virk og beðið verður um kvittanaprentara eða peningaskúffu ef slíkt er nauðsynlegt.

Margir söluaðilar sem óskuðu eftir þessum eiginleika hafa áhuga á því að draga úr sóun með því að bjóða kvittanir í tölvupósti og hvetja til rafrænna greiðslna. Það fer eftir skilgreiningu sölustaðarins hvort söluaðilar verslunar eru beðnir að velja kvittanaprentara eða peningaskúffu eingöngu þegar viðskiptavinur vill efnislega kvittun eða vill greiða í reiðufé.

Söluaðilar verslunar eru beðnir um að velja vélbúnaðarstöð í aðeins eitt skipti fyrir hverja færslu, nema ef þurfi að prenta kvittun og greitt er í reiðufé, en vélbúnaðarreglan sem var upphaflega valin felur ekki í sér bæði tækin. Í því tilfelli verður söluaðili verslunar aftur beðinn um að velja vélbúnaðarstöð sem hægt er að nota til að ljúka færslu.

## <a name="related-articles"></a>Tengdar greinar

- [Setja upp POS Hybrid-forrit í Android og iOS](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/hybridApp)
- [Dynamics 365-greiðslutengill fyrir Adyen](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)
- [Yfirlit notendaþjónustu nettengdra jaðartækja](https://go.microsoft.com/fwlink/?linkid=2129965)
