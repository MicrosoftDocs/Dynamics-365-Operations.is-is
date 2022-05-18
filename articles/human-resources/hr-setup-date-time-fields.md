---
title: Skilja svæði fyrir dagsetningu og tíma
description: Þetta efnisatriði útskýrir hvers má búast við þegar þú notar reiti fyrir dagsetningu og tíma í Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f595e06d9ddc9b44e8820d814d888971444bdf6a
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688490"
---
# <a name="understand-date-and-time-fields"></a>Skilja svæði fyrir dagsetningu og tíma

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



**Dagsetning og tími** reiti eru grundvallarhugtak í Microsoft Dynamics 365 Human Resources. Það er mikilvægt að þú skiljir hvernig á að vinna með **Dagsetning og tími** gögn á síðum, í Dataverse, og í utanaðkomandi heimildum.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Að skilja muninn á gagnagerðum dagsetningar- og tímareita

**Dagsetning og tími** reitirnir innihalda upplýsingar um tímabelti, en **Dagsetning** sviðum ekki. **Dagsetning** reitir sýna sömu upplýsingar hvar sem er. Þegar þú slærð inn dagsetningu í a **Dagsetning** reit, er sama dagsetning skrifuð í gagnagrunninn.

Þegar gögn eru sýnd í a **Dagsetning og tími** reitnum er dagsetning og tími stillt út frá tímabelti notandans sem er valið á **Notendavalkostir** síða (**Sameiginlegt \> Uppsetning \> Notendavalkostir**). Upplýsingar um dagsetningu og tíma sem þú slærð inn í reitinn eru hugsanlega ekki þær sömu og upplýsingarnar sem eru skrifaðar í gagnagrunninn.

[![Valkostasíðu notenda.](./media/Useroptionsform.png)](./media/Useroptionsform.png)

## <a name="understanding-date-and-time-fields-on-pages"></a>Skilningur á dagsetningu og tímareitum á síðum 

Gögn **Dagsetningar og tíma** sem birtast á skjánum eru ekki þau sömu og gögnin sem eru geymd í gagnagrunninum ef tímabelti notanda er ekki stillt á samræmdan alþjóðlegan tíma (UTC). Gögn í reitunum **Dagsetning og tími** eru alltaf geymdir sem UTC.

[![Starfsmannasíða UTC.](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Fáðu öðlast skilning á dagsetninga- og tímareitum í gagnagrunninum 

Þegar a **Dagsetning og tími** gildi er skrifað í gagnagrunninn, gögnin eru geymd sem UTC. Þess vegna geta notendur séð hvaða sem er **Dagsetning og tími** gögn miðað við tímabeltið sem er skilgreint í notendavalkostum þeirra.
 
Í dæminu hér að ofan er upphafstíminn tímapunktur, ekki ákveðin dagsetning. Með því að breyta tímabelti innskráða notanda úr GMT +12:00 í GMT UTC, sýnir sama færslan 04/30/2019 12:00:00 í stað 05/01/2019 12:00:00.

Í dæminu hér að neðan verður starf starfsmanns 000724 virk á sama tíma óháð tímabelti. Starfsmaðurinn verður virkur þann 04/30/2019 á GMT-tímabeltinu, sem er það sama og 05/01/2019 á GMT+12:00-tímabeltinu. Hvort tveggja vísar til sama tímapunkts og ekki til ákveðinnar dagsetningar. 

[![Starfsmannasíða GMT.](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Dagsetninga- og tímagögn í gagnastjórnunarramma, Excel, Dataverse og Power BI 

Gagnastjórnunarrammi (DMF), Excel viðbót,Dataverse, og Power BI skýrslugerð er öll hönnuð til að hafa samskipti við gögn beint á gagnagrunnsstigi. Þar sem enginn biðlari er til staðar til að stilla gögnin fyrir **Dagsetningu og tíma** á tímabelti notandans, eru öll gildi **Dagsetningar og tíma** á UTC, sem getur valdið misskilningi þegar gögn eru slegin inn eða skoðuð.
 
Hvenær **Dagsetning og tími** gögnum er skilað í gegnum DMF, Excel, eða Dataverse, gagnagrunnurinn gerir ráð fyrir að hann sé í UTC. Hins vegar, ef notendur sem skoða gögnin eru ekki með tímabelti notanda stillt á UTC, þá er sent inn **Dagsetning og tími** gildi mun ekki birtast eins og búist var við og notendur gætu ruglast. 
 
Það sama getur gerst á öfugan hátt þegar gögn eru flutt út. Gögnin **Dagsetning og tími** í útfluttri DMF-einingu geta verið öðruvísi en það sem er sýnt í biðlara Dynamics. 
 
Þegar ytri upprunar eins og DMF eru notaðir til að skoða eða heimila gögn skal hafa í huga að gildin **Dagsetning og tími** eru sjálfgefið stillt á UTC alveg óháð því í hvaða tímabelti tölva notandans er eða hverjar gildandi stillingar á tímabelti notandans eru. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Dæmi um sömu skrá sem birtist á mismunandi afurðasvæðum 

**Human Resources með tímabelti notanda stillt á UTC**

[![Starfsmannasíða stillt á UTC.](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources með tímabelti notanda stillt á GMT +12:00** 

[![Starfsmannasíða stillt á GMT.](./media/worker-form4.png)](./media/worker-form4.png)

**Excel í gegnum OData**

[![Excel í gegnum OData.](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-sviðsetning**

[![DMF-sviðsetning.](./media/DMFStaging.png)](./media/DMFStaging.png)

**Útflutningur á DMF**

[![Útflutningur á DMF.](./media/DMFExport.png)](./media/DMFExport.png)

**Excel í gegnum Dataverse**

[![Excel í gegnum Dataverse.](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Sjá einnig

[Dagsetningar- og tímagögn](/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Valin tímabelti notanda](/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
