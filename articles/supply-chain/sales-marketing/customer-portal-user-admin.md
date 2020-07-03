---
title: Stofna og stjórna notendum fyrir viðskiptavinagátt
description: Þetta efnisatriði útskýrir hvernig á að stofna notendareikninga viðskiptavinagáttar og stilla heimildir þeirra.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: c56e41b8ea5039531205083b5b42aff05e05cf66
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413975"
---
# <a name="create-and-manage-customer-portal-users"></a>Stofna og stjórna notendum fyrir viðskiptavinagátt

Í tilbúnu innleiðingunni er engin leið fyrir notendur að skrá sig sjálfir fyrir vefsvæðum sem búin eru til með því að nota viðskiptavinagáttina. Til að skrá sig inn og nota vefsvæði verða stjórnendur að bjóða notendum. Microsoft hefur viljandi hindrað möguleika notenda á að skrá sig sjálfir.

Áður en notandi getur notað vefsvæði þarf að stofna tengiliðafærslu fyrir þann notanda. Þessi færsla gefur til kynna hvaða viðskiptavinalykil og lögaðila notandi tilheyrir. Þessar upplýsingar eru nauðsynlegar til að tryggja að notandinn geti stofnað og skoðað sölupantanir.

Þegar notendur skrá sig sjálfir eru tengiliðafærslur sjálfkrafa búnar til fyrir þá. Þess vegna er ekki hægt að tryggja að notandi velji réttan viðskiptavinalykil og lögaðila. Aftur á móti gerir boðsferlið stjórnanda kleift að úthluta réttum viðskiptavinalykli og lögaðila til tengiliðafærslunnar áður en boð er sent. Ef þú ert að hugsa um að sérsníða lausnina svo notendur geti skráð sig sjálfir skaltu fyrst huga að hugsanlegum afleiðingum.

## <a name="prerequisite-setup"></a>Uppsetning frumskilyrða

Tengiliðir í Power Apps-gáttum eru vistaðir sem færslur í einingunni **Tengiliðir** í Common Data Service. Tvíritun samstillir síðan þessar færslur við Microsoft Dynamics 365 Supply Chain Management eftir þörfum.

![![Skýringarmynd kerfis fyrir tengiliði viðskiptavinagáttar](media/customer-portal-contacts.png "Skýringarmynd kerfis fyrir tengiliði viðskiptavinagáttar")](media/customer-portal-contacts.png "System diagram for Customer portal contacts")

Áður en hafist er handa við að bjóða nýja viðskiptavini skal ganga úr skugga um að búið sé að virkja einingavörpunina **Tengiliðir** í tvíritun.

## <a name="the-invitation-process"></a>Boðsferlið

Ef bjóða á fyrirliggjandi tengiliði í viðskiptavinagáttina skal fylgja skrefunum í [Bjóða tengiliðum í gáttirnar](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) í fylgiskjölum Power Apps-gátta.

Áður en viðskiptavini er boðið í viðskiptavinagáttina skal ganga úr skugga um að [tengiliðafærsla](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) viðskiptavinar sé til staðar og uppsett á eftirfarandi hátt:

1. Stillið reitinn **Fyrirtæki** á lögaðilann sem viðskiptavinurinn á að tilheyra í Supply Chain Management.
2. Stillið reitinn **Lykilnúmer** á númer viðskiptavinalykilsins sem notandinn á að hafa í Supply Chain Management.

Eftir að tengiliður er stofnaður ætti að vera hægt að sjá hann í Supply Chain Management.

Frekari upplýsingar er að finna í [Skilgreina tengilið til að nota í gátt](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) í fylgiskjali Power Apps-gátta.

## <a name="out-of-box-web-roles-and-entity-permissions"></a>Tilbúin vefhlutverk og heimildir eininga

Notandahlutverk í Power Apps-gáttum eru skilgreind samkvæmt [vefhlutverkum](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) og [heimildum eininga](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions). Nokkur hlutverk eru skilgreind fyrir tilbúnu viðskiptavinagáttina. Hægt er að búa til ný hlutverk og hægt er að breyta eða fjarlægja fyrirliggjandi hlutverk.

### <a name="out-of-box-web-roles"></a>Tilbúin vefhlutverk

Þessi hluti útskýrir vefhlutverkin sem afhent eru með viðskiptavinagáttinni.

Frekari upplýsingar um hvernig á að breyta tilbúnum notendahlutverkum er að finna í [Búa til vefhlutverk fyrir gáttir](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) og [Bæta við öryggi byggt á færslum með því að nota heimildareiningar fyrir gáttir](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) í fylgiskjölum Power Apps-gátta.

#### <a name="administrator"></a>Kerfisstjóri

Stjórnandi hefur umsjón með og heldur úti vefsvæðinu. Þessi einstaklingur mun ráðstafa og setja upp viðskiptavinagáttina. Stjórnandi heldur utan um upplýsingatækni- og öryggismál gáttarinnar og gengur úr skugga um að allt gangi vel fyrir sig. Stjórnandinn getur einnig sérsniðið og/eða breytt vefgáttinni með því að bæta við nýrri virkni, búa til ný hlutverk og fleira.

#### <a name="customer-representative"></a>Fulltrúi viðskiptavinar

Fulltrúi viðskiptavinar starfar fyrir fyrirtæki viðskiptavinar og ber ábyrgð á því að sjá um pantanir sem fyrirtækið sendir. Fulltrúi viðskiptavinarins getur séð allar pantanir sem hafa verið gerðar fyrir fyrirtækið og notendurna sem sendu þær. Þar að auki getur fulltrúi viðskiptavinar séð upplýsingar um allan lykilinn og hvaða tengiliðir geta lagt inn pantanir fyrir hönd þess lykils.

#### <a name="authorized-users"></a>Heimilaðir notendur

Heimilaðir notendur geta lagt inn pantanir og skoðað stöðu pantana sem þeir hafa sett inn. Hins vegar geta þeir ekki skoðað stöðu pantana sem aðrir notendur fyrirtækisins hafa lagt inn.

#### <a name="unauthorized-users"></a>Ekki heimilaðir notendur

Notendur sem ekki eru með heimild geta ekki skoðað nein gögn. Þeir geta aðeins séð almennar upplýsingar, t.d. skilmála og upplýsingar um fyrirtækið sem keyrir viðskiptavinagáttina.

#### <a name="example"></a>Dæmi

Eftirfarandi tafla sýnir hvaða sölupantanir notendur í hverju vefhlutverki fyrir sig geta séð í kerfinu.

| Sölupöntun | Kerfisstjóri | Fulltrúi viðskiptavinar fyrir viðskiptavin&nbsp;X | Heimilaður notandi: Jane | Heimilaður notandi: Sam | Ekki heimilaður notandi: May |
|---|---|---|---|---|---|
| Viðskiptavinur&nbsp;X Pöntunaraðili:&nbsp;Jane | Já | Já | Já | Ekkert | Ekkert |
| Viðskiptavinur&nbsp;X Pöntunaraðili:&nbsp;Sam | Já | Já | Ekkert | Já | Ekkert |
| Viðskiptavinur&nbsp;Y Pöntunaraðili:&nbsp;May | Já | Ekkert | Ekkert | Ekkert | Ekkert |

> [!NOTE]
> Þótt bæði Sam og Jane séu tengiliðir sem vinna fyrir viðskiptavin X geta þau aðeins séð þær pantanir sem þau hafa gert og ekkert annað. Þótt May sé með pöntun í kerfinu, getur hún ekki séð pöntunina í viðskiptavinagáttinni því að hún er ekki með heimild. (Auk þess hlýtur hún að hafa verið lagt pöntunina inn í gegnum aðra rás en viðskiptavinagáttina.)
