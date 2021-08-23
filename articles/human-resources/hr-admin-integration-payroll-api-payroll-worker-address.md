---
title: Heimilisfang starfskrafts á launaskrá
description: Þetta efnisatriði veitir upplýsingar og dæmi um fyrirspurn fyrir einingu aðseturs fyrir starfsmann á launaskrá í Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 898ca7b33e39ec33990fecc4c3a7229620fbfddd5ce8ad14423af38047187e55
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761975"
---
# <a name="payroll-worker-address"></a>Heimilisfang starfskrafts á launaskrá

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir heimilisfangaeiningu starfskrafts launaskráar fyrir Dynamics 365 Human Resources.

Efnislegt heiti: mshr_payrollworkeraddressentity.

### <a name="description"></a>lýsing

Þessi eining gefur upp búsetu fyrir launaskrá og vinnustað launaskráar fyrir tiltekinn starfsmann.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | lýsing |
| --- | --- | --- |
| **Póststöð**</br>mshr_city</br>*Strengur* | Lesa eingöngu</br>Krafa | Borgin sem er skilgreind fyrir aðsetrið.   |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu</br>Krafa | Einkvæmt númer starfsmanns.  |
| **Landsvæði**</br>mshr_countryregionid</br>*Strengur* | Lesa eingöngu</br>Krafa | Landsvæðið sem er skilgreint fyrir heimilisfangið.  |
| **Gildir frá**</br>mshr_postaladdressvalidfrom</br>*Mótfærð dagsetning og tími* | Lesa eingöngu </br>Krafa | Dagsetningin sem aðsetrið gildir frá. |
| **Starfað á aðsetri** </br> mshr_isworkedinaddressbr </br>*[Valmöguleikar mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Lesa eingöngu</br>Krafa | Táknar hvort starfsmaðurinn starfi á viðkomandi heimilisfangi. |
| **Sýsla**</br>mshr_county</br>*Strengur* | Lesa eingöngu</br>Krafa | Sýsla sem er skilgreind fyrir aðsetrið.  |
| **Kenni heimilisfangs starfskrafts á launaskrá**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Krafa</br>Búið til af kerfi | GUID-gildi myndað af kerfinu til að auðkenna heimilisfang á einkvæman hátt.  |
| **Aðalsvæði**</br>mshr_primaryfield</br>*Strengur* | Lesa eingöngu</br>Krafa |  |
| **Gata**</br>mshr_street</br>*Strengur* | Lesa eingöngu</br>Krafa | Gatan sem er skilgreind fyrir aðsetrið. |
| **Gildir til**</br>mshr_postaladdressvalidto</br>*Mótfærð dagsetning og tími* | Lesa eingöngu </br>Krafa | Dagsetningin sem aðsetrið gildir til.  |
| **Staðsetningarkenni**</br>mshr_locationidbr>*String* | Lesa eingöngu <br>Krafa | Auðkenni aðsetursins.  |
| **Póstnúmer**</br>mshr_zipcode<br>*Strengur* | Lesa eingöngu <br>Krafa |Auðkennisnúmerið sem er skilgreint fyrir starfsmanninn.  |
| **Bjó á aðsetri**</br>mshr_islivedinaddressbr </br> *[Valmöguleikar mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Lesa eingöngu</br>Krafa | Táknar hvort starfsmaðurinn búi á viðkomandi heimilisfangi. |
| **Ríki**</br>mshr_state</br>*Strengur* | Lesa eingöngu</br>Krafa | Fylkið sem er skilgreint fyrir aðsetrið.  |

## <a name="example-query"></a>Dæmi um fyrirspurn

**Beiðni**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Svar**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Sjá einnig

[Kynning á API launasamþættingar](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
