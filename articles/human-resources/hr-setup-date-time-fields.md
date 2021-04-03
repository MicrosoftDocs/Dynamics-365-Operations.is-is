---
title: Skilja svæði fyrir dagsetningu og tíma
description: Fáðu skilning á við hverju má búast við notkun á dagsetningar- og tímareitum í Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 924d7369129d4115d45f23864e7b851d318c52a4
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467362"
---
# <a name="understand-date-and-time-fields"></a>Skilja svæði fyrir dagsetningu og tíma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Reitirnir **Dagsetning og tími** eru grundvallarhugtak í Dynamics 365 Human Resources. Mikilvægt er að skilja hvernig vinna á með gögn **Dagsetningu og tíma** í skjámyndum, Dataverse, og ytri upprunum.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Að skilja muninn á gagnagerðum dagsetningar- og tímareita

Reitirnir **Dagsetning og tími** innihalda upplýsingar um tímabelti en reitirnir **Dagsetning** gera það ekki. Reitirnir **Dagsetning** sýna sömu upplýsingar á hvaða stað sem er. Þegar þú slærð inn dagsetningu í reitinn **Dagsetning** skrifar Human Resources sömu dagsetninguna í gagnagrunninn.

Þegar gögn eru birt í reitnum **Dagsetning og tími** aðlagar Human Resources dagsetningu og tíma út frá tímabelti notandans sem er stillt í glugganum **Notendastillingar** (**Sameiginlegt > Uppsetning > Notendastillingar**). Upplýsingar um dagsetningu og tíma sem þú slærð inn í reitinn eru ef til vill ekki þær sömu og upplýsingarnar sem skrifaðar eru í gagnagrunninn.

[![Skjámyndin Notendastillingar](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Að öðlast skilning á dagsetninga- og tímareitum 

Gögn **Dagsetningar og tíma** sem birtast á skjánum eru ekki þau sömu og gögnin sem eru geymd í gagnagrunninum ef tímabelti notanda er ekki stillt á samræmdan alþjóðlegan tíma (UTC). Gögn í reitunum **Dagsetning og tími** eru alltaf geymdir sem UTC.

[![UTC í skjámynd starfsmanns](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Fáðu öðlast skilning á dagsetninga- og tímareitum í gagnagrunninum 

Þegar Human Resources skrifar gildi fyrir **Dagsetningu og tíma** í gagnagrunninn, eru gögnin geymd á UTC. Þetta gerir notendum kleift að sjá öll gögn í **Dagsetningu og tíma** miðað við tímabeltið sem er skilgreint í notendastillingum þeirra.
 
Í dæminu hér að ofan er upphafstíminn tímapunktur, ekki ákveðin dagsetning. Með því að breyta tímabelti innskráða notanda úr GMT +12:00 í GMT UTC, sýnir sama færslan 04/30/2019 12:00:00 í stað 05/01/2019 12:00:00.
  
Í dæminu hér að neðan verður starf starfsmanns 000724 virkt á umleið, óháð tímabelti. Starfsmaðurinn verður virkur þann 04/30/2019 á GMT-tímabeltinu, sem er það sama og 05/01/2019 á GMT+12:00-tímabeltinu. Hvort tveggja vísar til sama tímapunkts og ekki til ákveðinnar dagsetningar. 

[![GMT í skjámynd starfsmanns](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Dagsetninga- og tímagögn í gagnastjórnunarramma, Excel, Dataverse og Power BI 

Gagnastjórnunarrammi, Excel-innbót, Dataverse og Power BI skýrslugerð eru öll hönnuð til að hafa samskipti við gögn beint á gagnagrunnsstigi. Þar sem enginn biðlari er til staðar til að stilla gögnin fyrir **Dagsetningu og tíma** á tímabelti notandans, eru öll gildi **Dagsetningar og tíma** á UTC, sem getur valdið misskilningi þegar gögn eru slegin inn eða skoðuð.  
 
Gögn **Dagsetningar og tíma** sem send eru inn í gegnum DMF, Excel eða Dataverse eru álitin vera á UTC af gagnagrunninum. Þetta getur valdið nokkrum ruglingi þegar innsent gildi í **Dagsetningu og tíma** birtist ekki eins og búist var við vegna þess að notandi sem skoðar gögnin er ekki með tímabelti notanda stillt á UTC. 
 
Það sama getur gerst á öfugan hátt þegar gögn eru flutt út. Gögnin **Dagsetning og tími** í útfluttri DMF-einingu geta verið öðruvísi en það sem er sýnt í biðlara Dynamics. 
 
Þegar ytri upprunar eins og DMF eru notaðir til að skoða eða heimila gögn skal hafa í huga að gildin **Dagsetning og tími** eru sjálfgefið stillt á UTC alveg óháð því í hvaða tímabelti tölva notandans er eða hverjar gildandi stillingar á tímabelti notandans eru. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Dæmi um sömu skrá sem birtist á mismunandi afurðasvæðum 

**Human Resources með tímabelti notanda stillt á UTC**

[![Skjámynd starfsmanns stillt á UTC](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources með tímabelti notanda stillt á GMT +12:00** 

[![Skjámynd starfsmanns stillt á GMT](./media/worker-form4.png)](./media/worker-form4.png)

**Excel í gegnum OData**

[![Excel í gegnum OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-sviðsetning**

[![DMF-sviðsetning](./media/DMFStaging.png)](./media/DMFStaging.png)

**Útflutningur á DMF**

[![Útflutningur á DMF](./media/DMFexport.png)](./media/DMFexport.png)

**Excel í gegnum Dataverse**

[![Excel í gegnum Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Sjá einnig

[Dagsetningar- og tímagögn](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Valin tímabelti notanda](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]