---
title: Samþættur aðalviðskiptavinur
description: Þetta efni lýsir samþættingu viðskiptavinaupplýsinga milli Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 41e4b6c192b6125a144e4d5ef952ba0975821d44
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063290"
---
# <a name="integrated-customer-master"></a>Samþætt aðalsniðmát viðskiptavinar

[!include [banner](../../includes/banner.md)]



Hægt er að ná góðum tökum á gögnum viðskiptavina í fleiri en einu Dynamics 365 forriti. Til dæmis getur viðskiptavinarlína átt uppruna í söluaðgerð í Dynamics 365 Sales (forriti viðskiptavinar) eða lína getur átt uppruna sinn í smásöluaðgerð í Dynamics 365 Commerce (fjármála- og rekstrarforrit). Óháð því hvaðan viðskiptavinagögnin eiga uppruna sinn eru þau samofin bak við tjöldin. Innbyggður viðskiptavinameistari veitir þér sveigjanleika til að ná góðum tökum á gögnum viðskiptavina í hvaða Dynamics 365 forriti sem er og gefur yfirgripsmikla sýn yfir viðskiptavininn í Dynamics 365 forritssvítunni.

## <a name="customer-data-flow"></a>Gagnaflæði viðskiptavinar

*Viðskiptavinur* er vel skilgreint hugtak í forritum. Þess vegna felur samþætting gagna viðskiptavina bara í sér að samræma viðskiptavinahugtakið milli forritanna tveggja. Eftirfarandi skýringarmynd sýnir gagnaflæði viðskiptavinar.

![Gagnaflæði viðskiptavinar.](media/dual-write-customer-data-flow.png)

Viðskiptavini er hægt að flokka í stórum dráttum í tvær gerðir: viðskiptamenn/fyrirtækjaviðskiptavini og neytendur/endanotendur. Þessar tvær tegundir viðskiptavina eru geymdar og meðhöndlaðar á annan hátt í Finance and Operations og Dataverse.

Í Finance and Operations eru bæði viðskipta-/fyrirtækjaviðskiptavinir og neytendur/endir notendur náð tökum á einni töflu sem er nefnd **CustTable** (CustCustomerV3Entity), og þau eru flokkuð út frá **Tegund** eiginleiki. (Ef **Gerð** er stillt á **Fyrirtæki** er viðskiptavinurinn viðskiptamaður/fyrirtækjaviðskiptavinur og ef **Gerð** er stillt á **Einstaklingur** er viðskiptavinurinn neytandi/notandi.) Aðalupplýsingar tengiliða eru meðhöndlaðar í gegnum SMMContactPersonEntity töfluna.

Í Dataverse eru viðskiptamenn/fyrirtækjaviðskiptavinir þjálfaðir í lykiltöflunni og eru auðkenndir sem viðskiptavinir þegar eigindin **Gerð vensla** er stillt á **Viðskiptavinur**. Bæði neytendur/notendur og tengiliður eiga fulltrúa í tengiliðatöflunni. Til að veita skýran aðskilnað milli neytenda/endanotanda og tengiliðs er taflan **Hafðu samband** með Boole-flöggun sem er nefnd **Seljanlegt**. Þegar **Seljanlegt** er **Satt** er tengiliðurinn neytandi/notandi og hægt er að búa til tilvitnanir og pantanir fyrir þann tengilið. Þegar **Seljanlegt** er **Rangt** er tengiliðurinn er bara aðaltengiliður viðskiptavinar.

Þegar tengiliður sem ekki er seljanlegur tekur þátt í tilboði eða pöntunarferli er **Seljanlegt** stillt á **Satt** til að merkja tengiliðinn sem seljanlegan tengilið. Tengiliður sem hefur orðið seljanlegur tengiliður er áfram seljanlegur tengiliður.

## <a name="templates"></a>Sniðmát

Viðskiptavinagögn innihalda allar upplýsingar um viðskiptavininn, svo sem viðskiptavinahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið, reikningssnið og vildarstöðu. Safn af töflukortum vinna saman í gagnasamskiptum viðskiptavinar, eins og sýnt er í eftirfarandi töflu.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla         | lýsing
----------------------------|---------------------------------|------------
[Tengiliðir fyrir skuldatryggingu V2](mapping-reference.md#115) | tengiliðir | Þetta sniðmát samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.
[Viðskiptavinaflokkar](mapping-reference.md#126) | msdyn_customergroups | Þetta sniðmát samstillir upplýsingar um hóp viðskiptavina.
[Greiðslumáti viðskiptavinar](mapping-reference.md#127) | msdyn_customerpaymentmethods | Þetta sniðmát samstillir upplýsingar um greiðslumáta viðskiptavina.
[Viðskiptavinir V3](mapping-reference.md#101) | lyklar | Þetta sniðmát samstillir aðalupplýsingar viðskiptavina fyrir viðskiptamenn og fyrirtækjaviðskiptavini.
[Viðskiptavinir V3](mapping-reference.md#116) | tengiliðir | Þetta sniðmát samstillir aðalgögn viðskiptavina fyrir neytendur og endanotendur.
[Viðskeyti nafna](mapping-reference.md#155) | msdyn_nameaffixes | Þetta sniðmát samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsludagalínur CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Þetta sniðmát samstillir tilvísunargögn greiðsludagalína, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsludagar CDS](mapping-reference.md#158) | msdyn_paymentdays | Þetta sniðmát samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsluáætlunarlínur](mapping-reference.md#159) | msdyn_paymentschedulelines | Samstillir tilvísunargögn greiðsluáætlunarlína, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsluáætlun](mapping-reference.md#160) | msdyn_paymentschedules | Þetta sniðmát samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsluskilmálar](mapping-reference.md#161) | msdyn_paymentterms | Þetta sniðmát samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
