---
title: Einstaklingur
description: Þetta efnisatriði lýsir einingu einstaklingsins fyrir Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 448be7ada2825d3cdd846650821579d1d6797d00
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800358"
---
# <a name="person"></a>Einstaklingur

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir einingu einstaklingsins fyrir Dynamics 365 Human Resources.

Raunlægt heiti: mshr_dirpersonentity

### <a name="description"></a>lýsing

Þessi eining býður upp á persónulegar upplýsingar einstaklingsins sem er umsækjandi.

## <a name="json-representation"></a>JSON-framsetning

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Eiginleikar

| Eiginleiki<br>**Efnislegt heiti**<br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Auðkenni einstaklingseiningar**<br>mshr_dirpersonentityid<br>*GUID* | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Kerfismyndað einkvæmt kenni fyrir færslueininguna. |
| **Aðilanúmer**<br>mshr_partynumber<br>*Strengur* | Lesa eingöngu<br>Krafa<br>Myndað af kerfinu | Einkvæmt notendalesvænt kenni myndað af kerfinu fyrir einstaklinginn.  |
| **Nafn**<br>mshr_name<br>*Strengur* | Lesa eingöngu<br>Krafa | Reitargildið er samhangandi röð fornafns, millinafns, forskeyti eftirnafns og eftirnafns í röðinni sem skilgreind er í reitnum **Nafnaröð sýnd sem**. |
| **Annað nafn**<br>mshr_namealias<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Annað nafn sem má gefa einstaklingnum. |
| **Þekkt(ur) sem**<br>mshr_knownas<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Nafn sem má nota fyrir einstaklinginn ef hann er yfirleitt þekktur undir öðru nafni. |
| **Kenni tungumáls**<br>mshr_languageid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Kenni tungumáls fyrir fyrsta tungumál einstaklingsins eins og það er skilgreint í ISO 639-1 sniði. |
| **Aðsetursbækur**<br>mshr_addressbooks<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Aðsetursbók sem einstaklingurinn gæti verið í. Aðsetursbækur sem hafa verið settar upp fyrir fyrirtækið eru gefnar upp í einingunni mshr_diraddressbooksentity. |
| **Afmælisdagur**<br>mshr_anniversaryday<br>*Int* | Lesa/skrifa<br>Valfrjálst | Afmælisdagur einstaklingsins. |
| **Mánuður afmælis**<br>mshr_anniversarymonth<br>*Safn valkosta mshr_monthsofyear* | Lesa/skrifa<br>Valfrjálst | Mánuður afmælisdags einstaklingsins. |
| **Afmælisár**<br>msdyn_anniversaryyear<br>*Int* | Lesa/skrifa<br>Valfrjálst | Árið sem einstaklingur á afmælisdag. |
| **Fæðingardagur**<br>mshr_birthday<br>*Int* | Lesa/skrifa<br>Valfrjálst | Dagur afmælisdags einstaklingsins. |
| **Fæðingarmánuður**<br>mshr_birthmonth<br>*Safn valkosta mshr_monthsofyear* | Lesa/skrifa<br>Valfrjálst | Mánuður afmælisdags einstaklingsins. |
| **Fæðingarár**<br>mshr_birthyear<br>*Int* | Lesa/skrifa<br>Valfrjálst | Árið sem einstaklingur á afmæli. |
| **Nöfn barna**<br>mshr_childrennames<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Strengur fyrir nöfn barna einstaklingsins. Engin þörf á afmörkun. |
| **Kyn**<br>mshr_gender<br>*Valkostir mshr_hcmpersongender* | Lesa/skrifa<br>Valfrjálst | Kyn einstaklings. |
| **Áhugamál**<br>mshr_hobbies<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Áhugamál einstaklings. |
| **Upphafsstafir**<br>mshr_initials<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Upphafsstafir í nafni einstaklings. |
| **Hjúskaparstaða**<br>mshr_maritalstatus<br>*Valkostir mshr_hcmpersonmaritalstatus* | Lesa/skrifa<br>Valfrjálst | Hjúskaparstaða einstaklingsins. |
| **Hljóðritun fornafns**<br>mshr_phoneticfirstname<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Hljóðfræðilegur framburður á fornafni einstaklingsins. |
| **Hljóðritun eftirnafns**<br>mshr_phoneticlastname<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Hljóðfræðilegur framburður á eftirnafni einstaklingsins. |
| **Hljóðritun millinafns**<br>mshr_phoneticmiddlename<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Hljóðfræðilegur framburður á eftirnafni einstaklingsins. |
| **Eigið viðskeyti**<br>mshr_personalsuffix<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Eigið viðskeyti einstaklingsins. Gild gildi í einingunni mshr_dirnameaffixentity þar sem mshr_type er viðskeyti (200000001). |
| **Persónulegur titill**<br>mshr_personaltitle<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Persónulegur titill einstaklingsins. Gild gildi í einingunni mshr_dirnameaffixentity þar sem mshr_type er titill (200000000).
| **Faglegt viðskeyti**<br>mshr_professionalsuffix<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Faglegt viðskeyti. |
| **Starfstitill**<br>mshr_professionaltitle<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Starfstitill. |
| **Fullt aðalheimilisfang**<br>mshr_fullprimaryaddress<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Fullt aðalheimilisfang einstaklingsins, samhangandi röð á reitum aðalheimilisfangs. |
| **Borg aðseturs**<br>mshr_addresscity<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Borg aðalheimilisfangs einstaklingsins. Setja upp í einingu mshr_logisticsaddresscityentity. |
| **Land/svæði heimilisfangs**<br>mshr_addresscountryregionid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Land/svæði aðalheimilisfangs einstaklingsins. Gild gildi í einingunni mshr_logisticsaddresscountryregionentity. |
| **ISO-kóði fyrir land/svæði heimilisfangs**<br>mshr_addresscountryregionisocode<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | ISO-kóði landsins fyrir aðalheimilisfang einstaklingsins. |
| **Sýsla heimilisfangs**<br>mshr_addresscounty<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Sýsla aðalheimilisfangs einstaklingsins. Setja upp í einingu mshr_logisticsaddresscountyentity. |
| **Heiti á umdæmi heimilisfangs**<br>mshr_addressdistrictname<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Umdæmi fyrir aðalheimilisfang einstaklingsins. Setja upp í mshr_logisticsaddressdistrictentity einingu. |
| **Breiddargráða heimilisfangs**<br>mshr_addresslatitude<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Breiddargráða á aðaheimlisfangi einstaklingsins. |
| **Staðsetningarkenni heimilisfangs**<br>mshr_addresslocationid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Einkvæmt kenni fyrir staðsetningu á aðalheimilisfangi einstaklingsins. Gild gildi í einingu mshr_logisticspostaladdresslocationcdsentity. |
| **Staðsetningarhlutverk heimilisfangs**<br>mshr_addresslocationroles<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Staðsetningarhlutverkið fyrir aðalaðsetur einstaklingsins. Setja upp í mshr_logisticslocationrolecdsentity einingu. |
| **Lengdargráða heimilisfangs**<br>mshr_addresslongitude<br>*Strengur* |  Lesa/skrifa<br>Valfrjálst | Lengdargráða á aðalheimilisfangi einstaklingsins. |
| **Ríki heimilisfangs**<br>mshr_addressstate<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Staða aðalheimilisfangs einstaklingsins. Setja upp í einingu mshr_logisticsaddressstateentity. |
| **Götuheiti**<br>mshr_addressstreet<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Götuheiti aðalheimilisfangs einstaklingsins. |
| **Heimilisfang gildir frá**<br>mshr_addressvalidfrom<br>*Dagsetning* | Lesa/skrifa<br>Valfrjálst | Dagsetningin frá því að aðalheimilisfang einstaklingsins er gilt. |
| **Heimilisfang gildir til**<br>mshr_addressvalidto<br>*Dagsetning* | Lesa/skrifa<br>Valfrjálst | Dagsetningin þangað til aðalheimilisfang einstaklingsins er í gildi. |
| **Póstnúmer heimilisfangs**<br>mshr_addresszipcode<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Póstnúmer aðalheimilisfangs einstaklingsins. Setja upp í einingu mshr_logisticsaddresspostalcodeentity. |
| **Heimilisfang er einkamál**<br>mshr_addressisprivate<br>*Safn valkosta mshr_noyes* | Lesa/skrifa<br>Valfrjálst | Ákvarðar hvort aðalheimilisfang einstaklingsins er deilt með öðrum í fyrirtækinu. |
| **Aðseturslýsing**<br>mshr_addressdescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing á aðalheimilisfangi einstaklingsins. |
| **Aðalnetfang tengiliðar**<br>mshr_primarycontactemail<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Aðalnetfang einstaklingsins. |
| **Lýsing á aðalnetfangi tengiliðar**<br>mshr_primarycontactemaildescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing gefin upp fyrir aðalnetfangið. |
| **Aðalnetfang tengiliðar er spjallskilaboð**<br>mshr_primarycontactemailisim<br>*Safn valkosta mshr_noyes* | Lesa/skrifa<br>Valfrjálst | Ákvarðar hvort aðalnetfangið er opið fyrir spjallskilaboð. |
| **Tilgangur aðalnetfangs**<br>mshr_primarycontactemailpurpose<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur aðalnetfangsins. Setja upp í mshr_logisticslocationroleentity einingu. |
| **Aðalfaxnúmer tengiliðar**<br>mshr_primarycontactfax<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Aðalfaxnúmer. |
| **Lýsing aðalfaxnúmers**<br>mshr_primarycontactfaxdescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing gefin upp fyrir aðalfaxnúmerið. |
| **Viðbót aðalfaxnúmers tengiliðar**<br>mshr_primarycontactfaxextension<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Viðbót aðalfaxnúmersins. |
| **Tilgangur aðalfaxnúmers tengiliðar**<br>mshr_primarycontactfaxpurpose<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur aðalfaxnúmers. Setja upp í mshr_logisticslocationroleentity einingu.
| **Aðalsímanúmer tengiliðar**<br>mshr_primarycontactphone<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Aðalsímanúmer. |
| **Lýsing á aðalsíma tengiliðar**<br>mshr_primarycontactphonedescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing gefin upp á aðalsímanúmerinu. |
| **Viðbót aðalsímanúmers tengiliðar**<br>mshr_primarycontactphoneextension<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Viðbót aðalsímanúmersins. |
| **Aðalsími tengiliðar er farsími**<br>mshr_primarycontactphoneismobile<br>*Safn valkosta mshr_noyes* | Lesa/skrifa<br>Valfrjálst | Ákvarðar hvort aðalsímanúmer sé farsímanúmer. |
| **Tilgangur aðalsíma tengiliðar**<br>mshr_primarycontactphonepurpose<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur aðalsímanúmersins. Setja upp í mshr_logisticslocationroleentity einingu. |
| **Aðalfjarriti tengiliðar**<br>mshr_primarycontacttelex<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Númer aðalfjarrita. |
| **Lýsing á aðalfjarrita tengiliðar**<br>mshr_primarycontacttelexdescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing gefin upp á aðalfjarritanúmeri einstaklingsins. |
| **Tilgangur aðalfjarrita tengiliðar**<br>mshr_primarycontacttelexpurpose<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur aðalfjarritanúmers einstaklingsins. Setja upp í mshr_logisticslocationroleentity einingu. |
| **Vefslóð aðaltengiliðar**<br>mshr_primarycontacturl<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Aðalvefslóðin. |
| **Lýsing aðalvefslóðar tengiliðar**<br>mshr_primarycontacturldescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing sem er gefin upp fyrir aðalvefslóð einstaklingsins. |
| **Tilgangur aðalvefslóðar tengiliðar**<br>mshr_primarycontacturldescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur aðalvefslóðar einstaklingsins. Setja upp í mshr_logisticslocationroleentity einingu. |
| **Aðaltengiliður Facebook**<br>mshr_primarycontactfacebook<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Aðal Facebook-reikningur. Auðkennt af notandakenni. |
| **Aðaltengiliður Facebook Lýsing**<br>mshr_primarycontactfacebookdescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing sem er gefin upp fyrir Facebook-aðalreikning einstaklingsins. |
| **Aðaltengiliður Facebook er einkamál**<br>mshr_primarycontactfacebookisprivate<br>*Safn valkosta mshr_noyes* | Lesa/skrifa<br>Valfrjálst | Ákvarðar hvort Facebook-aðalreikningur er sýnilegur öðrum notendum. |
| **Aðaltengiliður Facebook Tilgangur**<br>mshr_primarycontactfacebookpurpose<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur Facebook-aðalreiknings einstaklingsins. Setja upp í mshr_logisticslocationroleentity einingu. |
| **LinkedIn tengiliðar**<br>mshr_primarycontactlinkedin<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | LinkedIn-aðalreikningur. Auðkennt með notandanafni. |
| **Lýsing á LinkedIn-aðalreikningi**<br>mshr_primarycontactlinkedindescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing sem er gefin upp fyrir LinkedIn-aðalreikning einstaklingsins. |
| **LinkedIn tengiliðar er einkamál**<br>mshr_primarycontactlinkedinisprivate<br>*Safn valkosta mshr_noyes* | Lesa/skrifa<br>Valfrjálst | Ákvarðar hvort upplýsingum um LinkedIn-reikning einstaklingsins sé deilt með öðrum notendum. |
| **Tilgangur LinkedIn tengiliðar**<br>mshr_primarycontactlinkedinpurpose<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur LinkedIn-aðalreiknings einstaklingsins. Setja upp í mshr_logisticslocationroleentity einingu. |
| **Twitter tengiliðar**<br>mshr_primarycontacttwitter<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Twitter-aðalreikningur einstaklingsins. Auðkennt með @username. |
| **Lýsing á Twitter tengiliðar**<br>mshr_primarycontacttwitterdescription<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Lýsing sem er gefin upp fyrir Twitter-aðalreikning einstaklingsins. |
| **Twitter tengiliðar er einkamál**<br>mshr_primarycontacttwitterisprivate<br>*Safn valkosta mshr_noyes* | Lesa/skrifa<br>Valfrjálst | Ákvarðar hvort upplýsingum um Twitter-reikning einstaklingsins sé deilt með öðrum notendum. |
| **Tilgangur Twitter-aðalreiknings tengiliðar**<br>mshr_primarycontacttwitterpurpose<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Tilgangur Twitter-aðalreiknings einstaklingsins. Setja upp í mshr_logisticslocationroleentity einingu. |
| **Gerð aðila**<br>mshr_partytype<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Aðilagerð einstaklingsins. Verður alltaf **Einstaklingur** fyrir umsækjendur. |
| **Nafnaröð birtist sem**<br>mshr_namesequencedisplayas<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Röðin sem eiginleikar fyrir nöfn einstaklings er raðað í til að mynda gildi fyrir eiginleika nafnsins (mshr_name). |
| **Fornafn**<br>mshr_firstname<br>*Strengur* | Lesa/skrifa<br>Krafa | Fornafn einstaklingsins. |
| **Millinafn**<br>mshr_middlename<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Millinafn einstaklingsins. |
| **Forskeyti eftirnafns**<br>mshr_lastnameprefix<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Forskeytið fyrir eftirnafn einstaklingsins. |
| **Eftirnafn**<br>mshr_lastname<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Eftirnafn einstaklingsins. |
| **Rafrænt staðsetningarkenni**<br>mshr_electroniclocationid<br>*Strengur* | Lesa/skrifa<br>Valfrjálst | Auðkenni rafrænnar staðsetningar einstaklingsins. |
| **Tímabelti heimilisfangs**<br>mshr_addresstimezone<br>*Int* | Lesa/skrifa<br>Valfrjálst | Tímabelti aðalheimilisfangs einstaklingsins. |

## <a name="see-also"></a>Sjá einnig

[Leiðbeiningar um API-samþættingu á rakningakerfi umsækjanda](hr-admin-integration-ats-api-introduction.md)<br>
[Dæmi um fyrirspurn fyrir umsækjanda til ráðningar](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]