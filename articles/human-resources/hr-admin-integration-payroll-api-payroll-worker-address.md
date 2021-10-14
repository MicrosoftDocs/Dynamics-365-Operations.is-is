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
ms.openlocfilehash: bf3fc5f333333b9a832ecb9c185473e476ac231d
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559510"
---
# <a name="payroll-worker-address"></a>Heimilisfang starfskrafts á launaskrá

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir heimilisfangaeiningu starfskrafts launaskráar fyrir Dynamics 365 Human Resources.

Efnislegt heiti: mshr_payrollworkeraddressentity.

### <a name="description"></a>lýsing

Þessi eining gefur upp búsetu fyrir launaskrá og vinnustað launaskráar fyrir tiltekinn starfsmann.

## <a name="properties"></a>Eiginleikar

| Eiginleiki</br>**Efnislegt heiti**</br>**_Gerð_** | Nota | Lýsing |
| --- | --- | --- |
| **Númer starfsmanns**</br>mshr_personnelnumber</br>*Strengur* | Lesa eingöngu | Einkvæmt númer starfsmanns. |
| **Staðsetningarkenni**</br>mshr_locationidbr>*String* | Lesa eingöngu | Auðkenni aðsetursins. |
| **Bjó á aðsetri**</br>mshr_islivedinaddressbr </br> *[Valmöguleikar mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Lesa eingöngu | Gild sem gefur til kynna hvort starfsmaðurinn búi á viðkomandi heimilisfangi. |
| **Starfað á aðsetri** </br> mshr_isworkedinaddressbr </br>*[Valmöguleikar mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Lesa eingöngu | Gild sem gefur til kynna hvort starfsmaðurinn vinni á viðkomandi heimilisfangi. |
| **Landsvæði**</br>mshr_countryregionid</br>*Strengur* | Lesa eingöngu</br>Krafa | Landið eða svæðið sem er skilgreint fyrir heimilisfangið. |
| **Póstnúmer**</br>mshr_zipcode<br>*Strengur* | Lesa eingöngu | Auðkennisnúmerið sem er skilgreint fyrir starfsmanninn. |
| **Gata**</br>mshr_street</br>*Strengur* | Lesa eingöngu | Gatan sem er skilgreind fyrir heimilisfangið. |
| **Borg**</br>mshr_city</br>*Strengur* | Lesa eingöngu | Borgin sem er skilgreind fyrir heimilisfangið. |
| **Ríki**</br>mshr_state</br>*Strengur* | Lesa eingöngu | Ríki eða hérað sem er skilgreint fyrir heimilisfangið. |
| **Sýsla**</br>mshr_county</br>*Strengur* | Lesa eingöngu | Sýsla sem skilgreind er fyrir heimilisfangið. |
| **Gildir frá**</br>mshr_postaladdressvalidfrom</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetningin sem heimilisfangið gildir frá. |
| **Gildir til**</br>mshr_postaladdressvalidto</br>*Mótfærð dagsetning og tími* | Lesa eingöngu | Dagsetningin sem heimilisfangið gildir til. |
| **Aðalsvæði**</br>mshr_primaryfield</br>*Strengur* | Lesa eingöngu | Aðalreiturinn. |
| **Kenni heimilisfangs starfskrafts á launaskrá**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Búið til af kerfi | Altækt einkvæmt kennimerki (GUID-gildi) myndað af kerfinu til að auðkenna heimilisfang á einkvæman hátt. |

## <a name="relations"></a>Vensl

| Gildi eiginleika | Tengdur aðili | Yfirlitseiginleiki | Tegund innheimtu |
| --- | --- | --- | --- |
| _mshr_fk_worker_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Worker_id | mshr_FK_PayrollEmployeeEntity_Address |

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
