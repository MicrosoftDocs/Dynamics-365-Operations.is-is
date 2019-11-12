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
ms.openlocfilehash: a66beb6338ea593247c79a11feb7f301d56f32a9
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572519"
---
# <a name="integrated-customer-master"></a>Samþættur aðalviðskiptavinur

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

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

Forrit Finance and Operations    | Önnur Dynamics 365 forrit
--------------------------|---------------------------------
V3-númer viðskiptavinar               | Reikningur
V3-númer viðskiptavinar               | Tengiliður
Tengiliðir fyrir skuldatryggingu V2           | Tengiliður
Viðskiptavinaflokkar           | Msdyn\_customergroups
Greiðslumáti viðskiptavinar   | Msdyn\_customerpaymentmethods
Vildarkort              | Msdyn\_loyaltycards
Greiðsluáætlun          | Msdyn\_paymentschedules
Greiðsluáætlun          | Msdyn\_paymentschedulelines
Greiðsludagur CDS           | Msdyn\_paymentdays
Greiðsludagalínur CDS     | Msdyn\_paymentdaylines
Greiðsluskilmálar          | Msdyn\_paymentterms
Viðskeyti nafna              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>V3-númer viðskiptavinar til lykils:

Þetta sniðmát samstillir aðalupplýsingar viðskiptavina fyrir viðskiptamenn og fyrirtækjaviðskiptavini milli forrita Finance and Operations og Common Data Service.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | heiti
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | lýsing
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | none
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
none | \>\> | address1\_addresstypecode
none | \>\> | customertypecode
PARTYTYPE | \<\< | none
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>V3-númer viðskiptavinar til tengiliðar

Þetta sniðmát samstillir aðalupplýsingar viðskiptavina fyrir neytendur og endanotendur milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
none | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | none
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | none
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | none
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
none | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
none | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
none | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTPHONEDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | lýsing

## <a name="contacts"></a>Tengiliðir

Þetta sniðmát samstillir allar upplýstingar um aðal-, aðrar og þriðju tengiliði fyrir bæði viðskiptavini og lánardrottna milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-contacts.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | none
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | department
ATHUGASEMDIR | = | lýsing
KYN | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
none | \>\> | msdyn\_contactforvendor
none | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Viðskiptavinaflokkar

Þetta sniðmát samstillir upplýsingar um flokka viðskiptavina milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-customer-groups.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
LÝSING | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Greiðslumátar viðskiptavinar

Þetta sniðmát samstillir upplýsingar um greiðslumáta viðskiptavina milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
HEITI | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
LÝSING | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Vildarkort

Þetta sniðmát samstillir upplýsingar um vildarkort viðskiptavina milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Greiðsluáætlanir

Þetta sniðmát samstillir tilvísunargögn greiðsluáætlunar fyrir bæði viðskiptavini og lánardrottna milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-payment-schedules.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
HEITI | = | msdyn\_name
LÝSING | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
ATHUGASEMDIR | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Greiðsluáætlunarlínur

Samstillir tilvísunarlínur greiðsluáætlunar fyrir bæði viðskiptavini og lánardrottna milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Greiðsludagar

Þetta sniðmát samstillir tilvísunargögn greiðsludaga fyrir bæði viðskiptavini og lánardrottna milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-payment-days.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
HEITI | = | msdyn\_name
LÝSING | = | msdyn\_description

## <a name="payment-day-lines"></a>Greiðsludagalínur

Þetta sniðmát samstillir tilvísunargögn greiðsludagalína fyrir bæði viðskiptavini og lánardrottna milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
HEITI | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Greiðsluskilmálar

Þetta sniðmát samstillir tilvísunargögn greiðsluskilmála (greiðsluskilmálar) fyrir bæði viðskiptavini og lánardrottna milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-payment-terms.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
LÝSING | = | msdyn\_description
HEITI | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Viðskeyti nafna

Þetta sniðmát samstillir tilvísunargögn viðskeyta nafna fyrir bæði viðskiptavini og lánardrottna milli Finance and Operations og annarra forrita Dynamics 365.

<!-- ![](media/dual-write-name-affixes.png) -->

Upprunasvæði | Gerð vörpunar | Áfangasvæði
---|---|---
AFFIX | = | msdyn\_affix
GERÐ | \>\< | msdyn\_affixtype
LÝSING | = | msdyn\_description
