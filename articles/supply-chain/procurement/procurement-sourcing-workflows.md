---
title: "Verkflæði innkaupa og aðfanga"
description: "Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna. Til að setja upp samþykktarferli er hægt að stofna verkflæði."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 75daeed0d0e979165d3669e83e98cf278d7fb736
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="procurement-and-sourcing-workflows"></a>Verkflæði innkaupa og aðfanga

[!include [banner](../includes/banner.md)]

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
| Endurskoða innkaupabeiðni      | Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupabeiðnir.            |
| Endurskoða innkaupabeiðnilínu | Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupabeiðnalínur.       |
| Verkflæði innkaupapöntunar          | Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir     |
| Verkflæði innkaupapöntunarlínu     | stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir |
| Verkflæði umsóknar um að bæta við lánardrottni  | Stofna endurskoðunar- og samþykkisverkflæði til að bæta við nýjum lánardrottnum gegnum beiðnir lánardrottna. |

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



<a name="additional-resources"></a>Frekari upplýsingar
--------

[Skilgreina viðskiptaferli verkflæði fyrir innkaupabeiðnir](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[Verkflæði innkaupabeiðni](purchase-requisitions-workflow.md)

[Innleiðing nýrra lánardrottna](vendor-onboarding.md)


