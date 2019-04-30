---
title: Fylgjast með stöðum til að finna notendaupplýsingar og umsóknir umsækjenda
description: Þessi efnisatriði veitir upplýsingar um hvernig á að fylgjast með uppruna fyrir notendaupplýsingar og umsóknir umsækjanda.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/25/2019
ms.locfileid: "897466"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a>Fylgjast með stöðum til að finna notendaupplýsingar og umsóknir umsækjenda 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> Virkni sem getið er í þessu efnisatriði er í boði sem hluti af prufuútgáfu. Innihald og virkni geta tekið breytingum. Til að nota þennan eiginleika skal biðja stjórnanda að virkja hann með **Stjórnandastillingar** í Attract. Síðari útgáfa mun bjóða upp á rakningarskýrslur á uppruna. Frekari upplýsingar er að finna í [Fá aðgang að forskoðunareiginleikum í Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).

Þegar umsækjendur sækja um starf mun Attract sjálfkrafa fylgjast með uppruna umsókna þeirra, sem veitir þér mikilvægar upplýsingar til að auðvelda þér ráðningarvinnuna. Ráðningaraðilar og ráðningarstjórar geta einnig valið uppruna umsóknar á meðan þeir bæta umsækjanda handvirkt við starf eða hæfileikasafn.

Hægt er að skoða uppruna umsóknar í upplýsingum um umsóknaraðgerð undir flipanum **Aðgerð** sem og í umsóknarferli sem finnst undir **Notandaupplýsingar** í hæfileikasöfnum. Hægt er að finna upprunastað á notandasíðu umsækjanda í upplýsingum um umsækjanda undir flipanum **Notandaupplýsingar** í bæði umsóknum og hæfileikasöfnum.

> [!NOTE] 
> Hægt er að finna þessi sniðmát í [Viðbót við alhliða ráðningar](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).

## <a name="pre-configured-sources"></a>Forskilgreindir upprunastaðir

Sjálfgefinn upprunalisti inniheldur algenga upprunastaði umsóknar. Sumar upprunagerðir, eins og **Atvinnutorg** og **Samfélagsmiðill** eru með upplýsingar um fleiri upprunastaði. **Samfélagsmiðill** inniheldur til dæmis Facebook og Twitter. Upprunagerðin **Tilvísandi** gerir þér kleift að tilgreina starfsmann innan fyrirtækis sem tilvísanda. Sjálfgefinn upprunalisti inniheldur eftirfarandi forskilgreinda upprunastaði:

-   Ráðningarsíða Attract

-   Stofnun

-   Atvinnulífskynning

-   Markaðssetning fyrirtækis

-   Ráðstefnur og vörusýningar

-   Samband fagmanna

-   Atvinnutorg

    -   Indeed

    -   Leita

    -   CareerBuilder

    -   Google-störf

    -   Xing

    -   Glassdoor

    -   Monster Jobs

-   Tímarit og útgáfur

-   Samfélagsmiðill

    -   Facebook

    -   Twitter

-   Háskólaráðningar

-   LinkedIn

-   Smáauglýsingar

-   Tilvísun

-   Bætt við af ráðningaraðila

-   Annað

## <a name="customize-the-source-list"></a>Sérsníða upprunalista 

Þú getur stækkað upprunalistann til að innihalda fleiri upprunastaði umsóknar. Til að sérsníða þennan lista skaltu fylgja leiðbeiningunum í [Safn valkosta fyrir stækkunarhæfni í Attract](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract). Breyta einingunni **TalentSource** til að innihalda fleiri upprunastaði. 

Til að forðast að hafa neikvæð áhrif á notandaviðmótið skaltu ekki breyta eða eyða fasttextagildum **TalentCategory** (ekki nöfnum) fyrir eftirfarandi:

- **Tilvísun**
- **LinkedIn**
- **Annað**

Í staðinn geturðu stækkað fasttextann **TalentSource** til að bæta við öðrum gerðum uppruna.
