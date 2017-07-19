---
title: "Verkflæði innkaupa og aðfanga"
description: "Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna. Til að setja upp samþykktarferli er hægt að stofna verkflæði."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 67bdb8436ff379b0e55cfe1660597e8f93235eeb
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="procurement-and-sourcing-workflows"></a>Verkflæði innkaupa og aðfanga

[!include[banner](../includes/banner.md)]


Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna. Til að setja upp samþykktarferli er hægt að stofna verkflæði.

Verkflæði endurspeglar viðskiptaferli. Það skilgreinir flæði skjals í gegnum kerfið og gefur til kynna hver verður að ljúka við verk eða samþykkja skjal. Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:
-   **Samræmt ferli** — Hægt er að skilgreina samþykktarferli fyrir einstök skjöl, eins og innkaupabeiðnir og kostnaðarskýrslur. Með því að nota verkflæðiskerfi má betur ganga úr skugga um að skjölin séu unnin og samþykkt með samræmdum og skilvirkum hætti.
-   **Sýnileiki ferlis** — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks. Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.
-   **Miðlægur verkefnalisti** — Notendur geta skoðað miðlægan verkefnalisti og séð verkefni í verkflæðinu og samþykktir sem tilheyra þeim þvert á allt verkflæði sem þeir taka þátt í.. Þetta er tiltæk á síðunni Vinnuliðir.

## <a name="the-types-of-workflows-that-you-can-create"></a> Gerðir verkflæðis sem hægt er að stofna
Eftirfarandi verkflæðisgerðir eru tiltækar fyrir innkaup og aðföng.

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| **Gerð**                         | **Notið þessa gerð til að**                                          |
| Endurskoða innkaupabeiðni      | Stofna endurskoðunarverkflæði fyrir innkaupabeiðni.            |
| Endurskoða innkaupabeiðnilínu | Stofna endurskoðunarverkflæði fyrir innkaupabeiðnilína.       |
| Verkflæði innkaupapöntunar          | Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir     |
| Verkflæði innkaupapöntunarlínu     | stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir |

## <a name="creating-a-workflow"></a>verkflæði stofnuð
Til að stofna verkflæði er farið í Innkaup og aðföng &gt; Uppsetning &gt; verkflæði Innkaupa og uppruna og stofnað nýtt verkflæði með því að velja gerð verkflæðis sem á að stofna.  

Í Verkflæðistriga er hægt að draga verkflæðiseiningar yfir hönnuðinn og tengja einingarnar í flæði. einingar verkflæðisins ætti að skilgreina Fyrir verkflæðiseiningar Samþykkis og verkefnis má skilgreina hvaða þátttakandi á að framkvæma aðgerðina.
Gerð þátttakenda
----------------------

Hægt er að úthluta samþykktarskrefi til eftirfarandi flokka þátttakenda.

| Notendaflokkur    | Lýsing                                                               |
|---------------|---------------------------------------------------------------------------|
| Þátttakendur   | Úthluta samþykktarskrefinu til aðila í hópi eða hlutverki.                   |
| Stigveldi     | Úthluta samþykktarskrefi til notenda í tilteknu stigveldi fyrirtækis. |
| Verkflæðisnotandi | Úthluta samþykktarskrefinu til notenda í þessu verkflæði.                       |
| Biðröð         | Úthluta samþykktarskrefinu til vinnuliðalista.                            |
| Notandi          | Úthluta samþykktarskrefinu til tiltekinna notenda .                               |



<a name="see-also"></a>Sjá einnig
--------

[Skilgreina viðskiptaferli verkflæði fyrir innkaupabeiðnir](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Verkflæði fyrir innkaupabeiðni](purchase-requisitions-workflow.md)




