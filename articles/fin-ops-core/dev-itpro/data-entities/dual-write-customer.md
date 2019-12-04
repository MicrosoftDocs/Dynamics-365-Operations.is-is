---
title: Samþættur aðalviðskiptavinur
description: Þetta efni lýsir samþættingu viðskiptavinaupplýsinga milli Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 09d985e5c6816ec0c718aaf418f4e85fb828f1c6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769684"
---
# <a name="integrated-customer-master"></a>Samþættur aðalviðskiptavinur

[!include [banner](../includes/banner.md)]

Það er dæmigert að skrár viðskiptavina nái tökum á fleiri en einu forriti. Til dæmis getur sölustarfsemi komið með viðskiptamannaskrár í gegnum forritið Sales og rafræn viðskipti eða smásala geta komið með viðskiptavinaskrár í gegnum umsókn Finance and Operations. Óháð því hvaðan viðskiptavinaskráin er upprunnin, þá er hún samþætt bak við tjöldin þvert á forritamörk og mismun á innviðum. Að ná tökum á samþættum viðskiptavini hjálpar til við að takast á við margvíslega atburðarás og veitir yfirgripsmikla sýn á viðskiptavininn í Dynamics 365 forritasvítunni.

## <a name="customer-data-flow"></a>Gagnaflæði viðskiptavinar

*Viðskiptavinur* er vel skilgreint hugtak í forritum. Þess vegna felur samþætting gagna viðskiptavina bara í sér að samræma viðskiptavinahugtakið milli forritanna tveggja. Eftirfarandi skýringarmynd sýnir gagnaflæði viðskiptavinar.

![Gagnaflæði viðskiptavinar](media/dual-write-customer-data-flow.png)

Viðskiptavini er hægt að flokka í stórum dráttum í tvær gerðir: viðskiptamenn/fyrirtækjaviðskiptavini og neytendur/endanotendur. Þessar tvær tegundir viðskiptavina eru geymdar og meðhöndlaðar á annan hátt í Finance and Operations og Common Data Service.

Í Finance and Operations eru bæði viðskiptamenn/fyrirtækjaviðskiptamenn og neytendur/endanotendur þjálfaðir í að ná tökum á einni töflu sem er nefnd **CustTable** (CustomerCustomerV3Entity), og þeir eru flokkaðir eftir eigindinu **Gerð**. (Ef **Gerð** er stillt á **Fyrirtæki** er viðskiptavinurinn viðskiptamaður/fyrirtækjaviðskiptavinur og ef **Gerð** er stillt á **Einstaklingur** er viðskiptavinurinn neytandi/notandi.) Aðalupplýsingar tengiliða eru meðhöndlaðar í gegnum SMMContactPersonEntity eininguna.

Í Common Data Service eru viðskiptaenn/fyrirtækjaviðskiptavinir þjálfaðir í lykileiningunni og eru auðkenndir sem viðskiptavinir þegar eigindin **Gerð vensla** er stillt á **Viðskiptavinur**. Bæði neytendur/notendur og tengiliður eiga fulltrúa fyrir tengiliðinn. Til að veita skýran aðskilnað milli neytenda/endanotanda og tengiliðs er einingin **Hafðu samband** með Boole-flöggun sem er nefnd **Seljanlegt**. Þegar **Seljanlegt** er **Satt** er tengiliðurinn neytandi/notandi og hægt er að búa til tilvitnanir og pantanir fyrir þann tengilið. Þegar **Seljanlegt** er **Rangt** er tengiliðurinn er bara aðaltengiliður viðskiptavinar.

Þegar tengiliður sem ekki er seljanlegur tekur þátt í tilboði eða pöntunarferli er **Seljanlegt** stillt á **Satt** til að merkja tengiliðinn sem seljanlegan tengilið. Tengiliður sem hefur orðið seljanlegur tengiliður er áfram seljanlegur tengiliður.

## <a name="templates"></a>Sniðmát

Viðskiptavinagögn innihalda allar upplýsingar um viðskiptavininn, svo sem viðskiptavinahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið, reikningssnið og vildarstöðu. Safn af einingakortum virka saman á meðan samskipti við viðskiptavini eru í gangi, eins og sýnt er í eftirfarandi töflu.

Forrit Finance and Operations | Önnur Dynamics 365 forrit         | Lýsing
----------------------------|---------------------------------|------------
Tengiliðir fyrir skuldatryggingu V2             | tengiliðir                        | Þetta sniðmát samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.
Viðskiptavinaflokkar             | msdyn_customergroups            | Þetta sniðmát samstillir upplýsingar um hóp viðskiptavina.
Greiðslumáti viðskiptavinar     | msdyn_customerpaymentmethods    | Þetta sniðmát samstillir upplýsingar um greiðslumáta viðskiptavina.
Viðskiptavinir V3                | lyklar                        | Þetta sniðmát samstillir aðalupplýsingar viðskiptavina fyrir viðskiptamenn og fyrirtækjaviðskiptavini.
Viðskiptavinir V3                | tengiliðir                        | Þetta sniðmát samstillir aðalgögn viðskiptavina fyrir neytendur og endanotendur.
Vildarkort                | msdyn_loyaltycards              | Þetta sniðmát samstillir upplýsingar um vildarkort viðskiptavina.
Viðskeyti nafna                | msdyn_nameaffixes               | Þetta sniðmát samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.
Greiðsludagalínur CDS V2    | msdyn_paymentdaylines           | Þetta sniðmát samstillir tilvísunargögn greiðsludagalína, bæði fyrir viðskiptavini og lánardrottna.
Greiðsludagar CDS            | msdyn_paymentdays               | Þetta sniðmát samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.
Greiðsluáætlunarlínur      | msdyn_paymentschedulelines      | Samstillir tilvísunargögn greiðsluáætlunarlína, bæði fyrir viðskiptavini og lánardrottna.
Greiðsluáætlun            | msdyn_paymentschedules          | Þetta sniðmát samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.
Greiðsluskilmálar            | msdyn_paymentterms              | Þetta sniðmát samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.

[!include [banner](../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](dual-write/CDSContactsV2-contacts.md)]

[!include [mapping customer group](dual-write/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](dual-write/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](dual-write/CustomersV3-accounts.md)]

[!include [mapping customer contacts](dual-write/CustomersV3-contacts.md)]

[!include [mapping loyalty card](dual-write/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping name affixes](dual-write/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](dual-write/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](dual-write/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](dual-write/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](dual-write/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](dual-write/TermsofPayment-msdyn-paymentterms.md)]
