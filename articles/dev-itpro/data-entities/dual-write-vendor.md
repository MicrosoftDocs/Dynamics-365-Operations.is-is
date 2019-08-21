---
title: Samþættur aðallánardrottinn
description: Þetta efni lýsir samþættingu lánardrottnagagna milli Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 45808bc35aba04df6fcaf6b1cbfcc2461b0b65cb
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789200"
---
## <a name="integrated-vendor-master"></a>Samþættur aðallánardrottinn

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Hugtakið *Lánardrottinn* á við birgðasamtök eða einkaeigu sem er hluti af aðfangakeðjuferlinu og veitir vörur fyrir fyrirtækið. Þó að *Lánardrottinn* sé rótgróið hugtak í Microsoft Dynamics 365 for Finance and Operations er hugtakið lánardrottinn ekki til í Dynamics 365 fyrir Customer Engagement. Þess í stað, yfirhlaða sum fyrirtæki lykileininguna til að geyma bæði viðskiptavinaupplýsingar og upplýsingar um lánardrottna. Önnur fyrirtæki nota sérsniðið lánardrottinshugtak. Common Data Service samþætting styður bæði þessa hönnun. Þess vegna geturðu virkjað aðra hvora hönnunina, allt eftir aðstæðum fyrirtækisins.

Sameining gagna lánardrottins milli Finance and Operations og Customer Engagement gerir þér kleift að ná góðum tökum á gögnunum. Óháð því hvaðan lánardrottnagögnin eru upprunnin, þá eru þau samþætt bak við tjöldin þvert á forritamörk og mismun á innviðum. 

### <a name="vendor-data-flow"></a>Gagnaflæði lánardrottins

Ef þú vilt nota Customer Engagement við stjórnun lánardrottins og þú vilt einangra upplýsingar seljanda frá upplýsingum viðskiptavinarins, geturðu notað nýja lánardrottinshönnunina.

![Gagnaflæði lánardrottins](media/dual-write-vendor-data-flow.png)

Ef þú vilt nota Customer Engagement við stjórnun lánardrottins og þú vilt halda áfram að nota lyklaeininguna til að geyma upplýsingar lánardrottins geturðu notað nýju útvíkkuðu lánardrottinshönnunina. Í þessari hönnun eru útvíkkaðar upplýsingar um lánardrottinn, svo sem lánardrottnahópinn og bókunarforstillingar lánardrottins, geymdar í smáatriðum lánardrottins.

![Útvíkkað gagnaflæði lánardrottins](media/dual-write-vendor-detail.jpg)

Tengiliðsupplýsingar lánardrottins líkjast tengiliðsupplýsingum viðskiptavina. Bak við tjöldin eru upplýsingar tengiliðar vistaðar og sóttar frá sömu einingum.

## <a name="templates"></a>Sniðmát

Lánardrottnagögn innihalda allar upplýsingar um lánardrottinn, svo sem lánardrottnahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið og reikningssnið. Safn af einingakortum virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.

Finance and Operations  | Forritið Customer Engagement
------------------------|---------------------------------
Lánardrottinn V2               | Reikningur
Lánardrottinn V2               | Msdyn\_vendors
Tengiliðir fyrir skuldatryggingu V2         | Tengiliður
Lánardrottnaflokkar           | Msdyn\_vendorgroups
Greiðsluháttur lánardrottins   | Msdyn\_vendorpaymentmethods
Greiðsluáætlun        | Msdyn\_paymentschedules
Greiðsluáætlun        | Msdyn\_paymentschedulelines
Greiðsludagur CDS         | Msdyn\_paymentdays
Greiðsludagalínur CDS   | Msdyn\_paymentdaylines
Greiðsluskilmálar        | Msdyn\_paymentterms
Viðskeyti nafna            | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="vendor-v2-and-account"></a>Lánardrottinn V2 og lykill 

Fyrirtæki sem nota lyklaeininguna til að geyma upplýsingar um lánardrottna geta haldið áfram að nota hana á sama hátt. Þau geta einnig nýtt sér yfirlýsta virkni lánardrottins sem kemur vegna samþættingar Finance and Operations.

## <a name="vendor-v2-and-msdyn_vendors"></a>Lánardrottinn V2 og Msdyn\_vendors

Fyrirtæki sem nota sérsniðna lausn fyrir lánardrottna geta nýtt sér hugtakið tilbúinn lánardrottinn sem er kynntur til sögunnar í Common Data Service vegna samþættingar Finance and Operations. 

<!-- ![vendor mappings](media/dual-write-vendors-1.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-2.png) -->

<!-- ![vendor mappings](media/dual-write-vendors-3.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
VENDORACCOUNTNUMBER | = | msdyn\_vendoraccountnumber
VENDORGROUPID | = | msdyn\_vendorgroupid.msdyn\_vendorgroup
VENDORORGANIZATIONNAME | = | msdyn\_name
VENDORPARTYTYPE | \>\< | msdyn\_isperson
PERSONFIRSTNAME | = | msdyn\_firstname
PERSONLASTNAME | = | msdyn\_lastname
CREDITLIMIT | = | msdyn\_vendorcreditlimit
ISFOREIGNENTITY | \>\< | msdyn\_isforeignentity
ISONETIMEVENDOR | \>\< | msdyn\_isonetimevendor
ADDRESSBUILDINGCOMPLIMENT | = | msdyn\_addressbuildingcompliment
PERSONCHILDRENNAMES | = | msdyn\_childrennames
ADDRESSCITY | = | msdyn\_addresscity
ADDRESSCOUNTRYREGIONID | = | msdyn\_addresscountryregionid
ADDRESSCOUNTRYREGIONISOCODE | = | msdyn\_addresscountryregionisocode
ADDRESSCOUNTYID | = | msdyn\_addresscountyid
CREDITRATING | = | msdyn\_creditrating
ADDRESSDESCRIPTION | = | msdyn\_addressdescription
ADDRESSDISTRICTNAME | = | msdyn\_addressdistrictname
DUNSNUMBER | = | msdyn\_dunsnumber
ETHNICORIGINID | = | msdyn\_ethnicorigin
FORMATTEDPRIMARYADDRESS | = | msdyn\_formattedprimaryaddress
PERSONHOBBIES | = | msdyn\_hobbies
PERSONINITIALS | = | msdyn\_initials
LANGUAGEID | = | msdyn\_languageid
PERSONLASTNAMEPREFIX | = | msdyn\_lastnameprefix
PERSONMIDDLENAME | = | msdyn\_middlename
ORGANIZATIONNUMBER | = | msdyn\_organizationnumber
OURACCOUNTNUMBER | = | msdyn\_ourvendoraccountnumber
PAYMENTID | = | msdyn\_paymentid
PERSONPHONETICFIRSTNAME | = | msdyn\_phoneticfirstname
PERSONPHONETICMIDDLENAME | = | msdyn\_phoneticmiddlename
PERSONPHONETICLASTNAME | = | msdyn\_phoneticlastname
ORGANIZATIONPHONETICNAME | = | msdyn\_organizationphoneticname
ADDRESSPOSTBOX | = | msdyn\_addresspostbox
PRIMARYURL | = | msdyn\_primarycontacturl
PRIMARYEMAILADDRESS | = | msdyn\_primaryemailaddress
PRIMARYEMAILADDRESSDESCRIPTION | = | msdyn\_primaryemailaddressdescription
PRIMARYFACEBOOK | = | msdyn\_primaryfacebook
PRIMARYFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYFAXNUMBER | = | msdyn\_primaryfaxnumber
PRIMARYFAXNUMBERDESCRIPTION | = | msdyn\_primaryfaxnumberdescription
PRIMARYFAXNUMBEREXTENSION | = | msdyn\_primaryfaxnumberextension
PRIMARYLINKEDIN | = | msdyn\_primarylinkedin
PRIMARYLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescription
PRIMARYPHONENUMBER | = | msdyn\_pimaryphonenumber
PRIMARYPHONENUMBERDESCRIPTION | = | msdyn\_primaryphonenumberdescription
PRIMARYPHONENUMBEREXTENSION | = | msdyn\_primaryphonenumberextension
PRIMARYTELEX | = | msdyn\_primarytelex
PRIMARYTELEXDESCRIPTION | = | msdyn\_primarytelexdescription
PRIMARYTWITTER | = | msdyn\_primarytwitter
PRIMARYTWITTERDESCRIPTION | = | msdyn\_primarytwitterdescription
PRIMARYURLDESCRIPTION | = | msdyn\_primaryurldescription
PERSONPROFESSIONALSUFFIX | = | msdyn\_professionalsuffix
PERSONPROFESSIONALTITLE | = | msdyn\_professionatitle
ADDRESSSTATEID | = | msdyn\_addressstateid
ADDRESSSTREET | = | msdyn\_addressstreet
ADDRESSSTREETNUMBER | = | msdyn\_addressstreetnumber
VENDORKNOWNASNAME | = | msdyn\_vendorknownasname
ADDRESSZIPCODE | = | msdyn\_addresszipcode
DEFAULTPAYMENTDAYNAME | = | msdyn\_defaultpaymentdayname.msdyn\_name
DEFAULTPAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
DEFAULTPAYMENTTERMSNAME | = | msdyn\_paymentterms.msdyn\_name
HASONLYTAKENBIDS | \>\< | msdyn\_hasonlytakenbids
ISMINORITYOWNED | \>\< | msdyn\_isminorityowned
ISVENDORLOCALLYOWNED | \>\< | msdyn\_isvendorlocallyowned
ISSERVICEVETERANOWNED | \>\< | msdyn\_isserviceveteranowned
ISOWNERDISABLED | \>\< | msdyn\_ownerisdisabled
ISWOMANOWNER | \>\< | msdyn\_womanowner
PERSONANNIVERSARYDAY | = | msdyn\_personanniversaryday
PERSONANNIVERSARYYEAR | = | msdyn\_anniversaryyear
PERSONBIRTHDAY | = | msdyn\_birthday
PERSONBIRTHYEAR | = | msdyn\_birthyear
ORGANIZATIONEMPLOYEEAMOUNT | = | msdyn\_numberofemployees
VENDORHOLDRELEASEDATE | = | msdyn\_vendoronholdreleasedate
VENDORPARTYNUMBER | = | msdyn\_vendorpartynumber
ADDRESSLOCATIONID | = | msdyn\_addresslocationid
PERSONANNIVERSARYMONTH | = | msdyn\_vendorpersonanniversarymonth
PERSONBIRTHMONTH | = | msdyn\_vendorpersonbirthmonth
PERSONMARITALSTATUS | \>\< | msdyn\_maritalstatus
ADDRESSLATITUDE | \>\> | msdyn\_addresslatitude
ADDRESSLONGITUDE | \>\> | msdyn\_addresslongitude
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
CURRENCYCODE | = | msdyn\_currencycode.isocurrencycode
ISVENDORLOCATEDINHUBZONE | \>\< | msdyn\_isvendorlocatedinhubzone
DEFAULTVENDORPAYMENTMETHODNAME | = | msdyn\_vendorpaymentmethod.msdyn\_name
INVOICEVENDORACCOUNTNUMBER | = | msdyn\_invoicevendoraccountnumber.msdyn\_vendoraccountnumber
PERSONGENDER | \>\< | msdyn\_gender
AREPRICESINCLUDINGSALESTAX | \>\< | msdyn\_priceincludessalestax
SALESTAXGROUPCODE | = | msdyn\_taxgroup.msdyn\_name
VENDORPRICETOLERANCEGROUPID | = | msdyn\_pricetolerancegroup.msdyn\_groupid

## <a name="contacts"></a>Tengiliðir

Þetta sniðmát samstillir allar upplýstingar um aðal-, aðrar og þriðju tengiliði fyrir bæði viðskiptavini og lánardrottna milli Finance and Operations og Customer Engagement. Sjá upplýsingar um einingakortið [Innbyggður viðskiptavinameistari](dual-write-customer.md#contacts).

## <a name="vendor-groups"></a>Lánardrottnaflokkar

Þetta sniðmát samstillir upplýsingar um flokka lánardrottna milli Finance and Operations og Customer Engagement.

<!-- ![vendor groups mappings](media/dual-write-vendor-groups.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
DEFAULTPAYMENTTERMNAME | = | msdyn\_paymentterms.msdyn\_name
LÝSING | = | msdyn\_description
VENDORGROUPID | = | msdyn\_vendorgroup
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymentpermname.msdyn\_name

### <a name="vendor-payment-method"></a>Greiðsluháttur lánardrottins

Þetta sniðmát samstillir upplýsingar um greiðsluaðferð lánardrottins á milli Finance and Operations og Customer Engagement.

<!-- ![vendor payment method mappings](media/dual-write-vendor-payment-method.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
HEITI | = | msdyn\_name
LÝSING | = | msdyn\_description
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
ALLOWPAYMENTCOPIES | \>\< | msdyn\_allowpaymentcopies
PAYMENTTYPE | \>\< | msdyn\_paymenttype
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
ACCOUNTTYPE | \>\< | msdyn\_accounttype
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingposting
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_postdatedcheckclearingposting
PROMISSORYNOTEDRAFTTYPE | \>\< | msdyn\_promissorynotedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

