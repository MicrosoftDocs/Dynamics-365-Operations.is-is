---
title: Verkflæði innkaupa og aðfanga
description: Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna. Til að setja upp samþykktarferli er hægt að stofna verkflæði.
author: GalynaFedorova
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebfd96690eea762d0797db1b485544d957d17ce0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671927"
---
# <a name="procurement-and-sourcing-workflows"></a>Verkflæði innkaupa og aðfanga

[!include [banner](../includes/banner.md)]

Í sumum fyrirtækjum er þess krafist að innkaupabeiðnir og innkaupapantanir séu samþykktar af öðrum en þeim aðila sem setti inn færsluna. Til að setja upp samþykktarferli er hægt að stofna verkflæði.

Verkflæði endurspeglar viðskiptaferli. Það skilgreinir flæði skjals í gegnum kerfið og gefur til kynna hver verður að ljúka við verk eða samþykkja skjal. Nokkrir kostir eru við að nota verkflæðiskerfi í fyrirtækinu:

- **Samræmt ferli** — Hægt er að skilgreina samþykktarferli fyrir einstök skjöl, eins og innkaupabeiðnir og kostnaðarskýrslur. Með því að nota verkflæðiskerfi má betur ganga úr skugga um að skjölin séu unnin og samþykkt með samræmdum og skilvirkum hætti.
- **Sýnileiki ferlis** — Hægt er að rekja stöðu, sögu og afkastamælikvarða tiltekins verkflæðistilviks. Þetta auðveldar ákvörðun um hvort breyta þurfi verkflæðinu til að auka skilvirkni.
- **Miðlægur verkefnalisti** — Notendur geta skoðað miðlægan verkefnalisti og séð verkefni í verkflæðinu og samþykktir sem tilheyra þeim þvert á allt verkflæði sem þeir taka þátt í.. Þetta er tiltæk á síðunni Vinnuliðir.

## <a name="the-types-of-workflows-that-you-can-create"></a> Gerðir verkflæðis sem hægt er að stofna

Eftirfarandi verkflæðisgerðir eru tiltækar fyrir innkaup og aðföng.

| Gerð | Notið þessa gerð til að |
|---|---|
| Endurskoða innkaupabeiðni | Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupabeiðnir. |
| Endurskoða innkaupabeiðnilínu | Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupabeiðnalínur. |
| Verkflæði innkaupapöntunar | Stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir |
| Verkflæði innkaupapöntunarlínu | stofna endurskoðunar- og samþykkisverkflæði fyrir innkaupapantanir |
| Verkflæði umsóknar um að bæta við lánardrottni | Stofna endurskoðunar- og samþykkisverkflæði til að bæta við nýjum lánardrottnum gegnum beiðnir lánardrottna. |

> [!IMPORTANT]
> Þegar verið er að bæta við nýju verkflæði er einnig hægt að sjá eftirfarandi úrelt verkflæði sem skráð eru í svarglugganum **Stofna verkflæði**. Þetta tengist *staðfestingu kvittunar* virkninni sem var tiltæk í [Dynamics AX 2012](/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), en sem ekki er lengur boðið upp á. Þessi verkflæði eru ekki studd eins og er.
> 
> - Verkflæði tilkynningar um skiladag sendingar
> - Verkflæði tilkynninga um móttekinn reikning
> - Verkflæði tilkynninga um misheppnuð innhreyfingarskjöl afurða
> - Verkflæði tilkynninga um höfnun óstaðfestra innhreyfinga afurða

## <a name="creating-a-workflow"></a>verkflæði stofnuð

Til að stofna verkflæði er farið í Innkaup og aðföng &gt; Uppsetning &gt; verkflæði Innkaupa og uppruna og stofnað nýtt verkflæði með því að velja gerð verkflæðis sem á að stofna. 

Í Verkflæðistriga er hægt að draga verkflæðiseiningar yfir hönnuðinn og tengja einingarnar í flæði. einingar verkflæðisins ætti að skilgreina Fyrir verkflæðiseiningar Samþykkis og verkefnis má skilgreina hvaða þátttakandi á að framkvæma aðgerðina.

## <a name="types-of-participants"></a>Gerð þátttakenda

Hægt er að úthluta samþykktarskrefi til eftirfarandi flokka þátttakenda.

| Notendaflokkur | Lýsing |
|---|---|
| Þátttakendur | Úthluta samþykktarskrefinu til aðila í hópi eða hlutverki. |
| Stigveldi | Úthluta samþykktarskrefi til notenda í tilteknu stigveldi fyrirtækis. |
| Verkflæðisnotandi | Úthluta samþykktarskrefinu til notenda í þessu verkflæði. |
| Biðröð | Úthluta samþykktarskrefinu til vinnuliðalista. |
| Notandi | Úthluta samþykktarskrefinu til tiltekinna notenda . |

## <a name="additional-resources"></a>Frekari upplýsingar

- [Skilgreina viðskiptaferli verkflæði fyrir innkaupabeiðnir](https://www.microsoft.com/download/details.aspx?id=101821)
- [Verkflæði innkaupabeiðni](purchase-requisitions-workflow.md)
- [Nýliðun lánardrottna](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]