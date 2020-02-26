---
title: Skilja svæði fyrir dagsetningu og tíma
description: Fáðu skilning á við hverju má búast við notkun á dagsetningar- og tímareitum í Microsoft Dynamics 365 Human Resources. Fáðu betri yfirsýn yfir við hverju má búast við samskipti við dagsetningar- og tímagögn í skjámynd í Human Resources, ytri uppruna, eða Common Data Service.
author: Darinkramer
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9dd80415f33a4d671bdc2662704799775daad177
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009376"
---
# <a name="understand-date-and-time-fields"></a>Skilja svæði fyrir dagsetningu og tíma

Reitirnir **Dagsetning og tími** eru grundvallarhugtak í Dynamics 365 Human Resources. Mikilvægt er að öðlast skilning hvernig á að vinna með gögn í **Dagsetningu og tíma** í skjámyndum Dynamics 365 Human Resources, Common Data Service og ytri uppruna.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Að skilja muninn á gagnagerðum dagsetningar- og tímareita

Reitirnir **Dagsetning og tími** innihalda upplýsingar um tímabelti en reitirnir **Dagsetning** gera það ekki. Reitirnir **Dagsetning** sýna sömu upplýsingar á hvaða stað sem er. Þegar þú slærð inn dagsetningu í reitinn **Dagsetning** skrifar Human Resources sömu dagsetninguna í gagnagrunninn.

Þegar gögn eru birt í reitnum **Dagsetning og tími** aðlagar Human Resources dagsetningu og tíma út frá tímabelti notandans sem er stillt í glugganum **Notendastillingar** (**Sameiginlegt > Uppsetning > Notendastillingar**). Upplýsingar um dagsetningu og tíma sem þú slærð inn í reitinn eru ef til vill ekki þær sömu og upplýsingarnar sem skrifaðar eru í gagnagrunninn.

[![Skjámyndin Notendastillingar](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Að öðlast skilning á dagsetninga- og tímareitum 

Þegar gögn eru færð inn í reitinn **Dagsetning og tími** eru gögnin sem birtast á skjánum ekki þau sömu og gögnin sem eru geymd í gagnagrunninum ef tímabelti notandans er ekki stillt á samhæfðan alþjóðlegan tíma (UTC). Gögn í reitunum **Dagsetning og tími** eru alltaf geymdir sem UTC.

[![Skjámyndin Starfskraftur](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Fáðu öðlast skilning á dagsetninga- og tímareitum í gagnagrunninum 

Þegar Human Resources skrifar gildi **Dagsetningar og tíma** í gagnagrunninum geymir það gögnin í UTC. Þetta gerir notendum kleift að sjá öll gögn í **Dagsetningu og tíma** miðað við tímabeltið sem er skilgreint í notendastillingum þeirra.
 
Í dæminu hér að ofan er upphafstíminn tímapunktur, ekki ákveðin dagsetning. Með því að breyta tímabelti notandans sem er skráður inn frá GMT +12: 00 í GMT UTC sýnir sama skráin og var stofnuð 04/30/2019 12:00:00 í staðinn 05/01/2019 12:00:00.
  
Í dæminu hér að neðan verður starf starfsmanns 000724 virkt á umleið, óháð tímabelti. Starfsmaðurinn verður virkur þann 04/30/2019 á GMT-tímabeltinu, sem er það sama og 05/01/2019 á GMT+12:00-tímabeltinu. Hvort tveggja vísar til sama tímapunkts og ekki til ákveðinnar dagsetningar. 

[![Skjámyndin Starfskraftur](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-common-data-service-and-power-bi"></a>Dagsetninga- og tímagögn í gagnastjórnunarramma, Excel, Common Data Service og Power BI 

Gagnastjórnunarrammi, Excel-innbót, Common Data Service og Power BI skýrslugerð eru öll hönnuð til að hafa samskipti við gögn beint á gagnagrunnsstigi. Þar sem það er enginn viðskiptavinur til að aðlagast gögnunum **Dagsetning og tími** á tímabelti notandans eru öll gildi **Dagsetningar og tíma** í UTC, sem getur leitt til rangra forsendna þegar gögn eru slegin inn eða skoðuð.  
 
Gagnagrunnurinn gerir ráð fyrir að gögn í **Dagsetningum og tíma** sem eru lögð fram í gegnum DMF, Excel eða Common Data Service séu í UTC. Þetta getur valdið nokkrum ruglingi þegar innsent gildi í **Dagsetningu og tíma** birtist ekki eins og búist var við vegna þess að notandi sem skoðar gögnin er ekki með tímabelti notanda stillt á UTC. 
 
Það sama getur gerst á öfugan hátt þegar gögn eru flutt út. Gögnin **Dagsetning og tími** í útfluttu DMF-einingunni geta verið önnur en það sem birtist í Dynamics biðlaranum. 
 
Þegar þú notar utanaðkomandi heimildir eins og DMF til að skoða eða skrifa gögn er mikilvægt að hafa í huga að gildin í **Dagsetningu og tíma** teljast sjálfkrafa vera í UTC óháð tímabelti í tölvu notandans eða núverandi tímabeltisstillingum hans. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Dæmi um sömu skrá sem birtist á mismunandi afurðasvæðum 

**Human Resources með tímabelti notanda stillt á UTC**

[![Skjámyndin Starfskraftur](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources með tímabelti notanda stillt á GMT +12:00** 

[![Skjámyndin Starfskraftur](./media/worker-form4.png)](./media/worker-form4.png)

**Excel í gegnum OData**

[![Excel í gegnum OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-sviðsetning**

[![DMF-sviðsetning](./media/DMFStaging.png)](./media/DMFStaging.png)

**Útflutningur á DMF**

[![DMF-sviðsetning](./media/DMFexport.png)](./media/DMFexport.png)

**Excel í gegnum Common Data Service**

[![Excel í gegnum Common Data Service](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Sjá einnig

[Dagsetningar- og tímagögn](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Valin tímabelti notanda](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 
