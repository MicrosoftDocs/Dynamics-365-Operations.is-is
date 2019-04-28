---
title: Búa til sniðmát ferlis í Attract
description: Þetta efnisatriði gefur upplýsingar um hvernig á að búa til sniðmát ferlis í Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: ca04bb623b9ddd19f02efbf99289461a78ddd7f1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "856624"
---
# <a name="create-a-process-template-in-attract"></a>Búa til sniðmát ferlis í Attract

[!include [banner](includes/banner.md)]

*Sniðmát ráðningarferlisins* inniheldur allar aðgerðir sem ætti að vera hluti af ráðningarferli fyrir starf. Þetta efni lýsir grunnatriðum sniðmáts ferlis í Dynamics 365 for Talent: Attract. Það útskýrir einnig hvernig á að búa til sniðmát.

> [!NOTE]
> Sköpun sniðmáts er hluti af Viðbót við alhliða ráðningar fyrir Attract.

## <a name="template-management"></a>Stjórnun sniðmáts

Fyrirtæki geta ákveðið hvort teymismeðlimir eða aðeins stjórnendur geta búið til sniðmát ferlis í Attract. Til að stilla stjórnun sniðmáts skaltu fara í **Stjórnendamiðstöðina** \> **Stjórnun sniðmáts**. Til að leyfa teymismeðlimum að búa til eigin sniðmát skaltu kveikja á stjórnun sniðmáts. Ef þú kveikir ekki á stjórnun sniðmáts geta aðeins stjórnendur búið til sniðmát.

## <a name="default-template"></a>Sjálfgefið sniðmát

Aðeins stjórnendur geta stillt sjálfgefið sniðmát. Sjálfgefið sniðmát er notað ef sniðmát er ekki valið þegar starf er búið til. Til að stilla sjálfgefið sniðmát skaltu fara í **Stjórnendamiðstöðina** \> **Stjórnun sniðmáts**. Á spjaldinu fyrir sniðmátið sem ætti að vera sjálfgefið sniðmát skaltu velja þrípunktahnappinn (**...**) og veldu síðan **Velja sem sjálfgefið**.

## <a name="create-a-process-template"></a>Búa til sniðmát ferlis

Stjórnendur, ráðningaraðilar og mannauðsstjórar geta búið til sniðmát ferlis. Sniðmát ferlis samanstendur af *stigum* og *aðgerðum*. Stig hópa saman einum eða fleiri aðgerðum. Sjálfgefið hefur hvert sniðmát ferlis Viðfangs-, Umsóknar- og Tilboðsaðgerðir. Stigunum sem innihalda þessar aðgerðir má endurnefna. Þú getur bætt fleiri stigum með því að velja **+ Nýtt stig**. Þú getur virkjað aðgerðir á stigi annaðhvort með því að draga þá á viðeigandi stig eða með því að tvísmella þá á aðgerðalistanum.

> [!NOTE]
> Heiti stiga eru sýnileg umsækjendurm á **Staða umsóknar** síðu. Þú ættir að íhuga þessa staðreynd þegar þú velur nöfn fyrir stig.

Til að læra meira um aðgerðir, sjá [Ráðningarferli í Attract](./activities-attract.md).

Fylgdu þessum skrefum til að búa til sniðmát fyrir ráðningarferli.

1. Farðu í **Sniðmát**.
2. Veljið **Nýtt**.
3. Í **Heiti sniðmáts** reitnum, slá inn heiti fyrir sniðmátið, og þá velja **Búa til**.
4. Í **Veldu samþykktarferli** listi, veldu **Sjálfgefið** til að krefjast samþykkis fyrir starf.
5. Veldu til að kveikja eða slökkva á viðföngum.
6. Valfrjáls: Bæta við eða fjarlægja stig.

    - Til að bæta við stigi skaltu velja **+ Nýtt stig**.
    - Til að fjarlægja stig skaltu setja bendilinn yfir stigið og veldu síðan ruslakörfuhnappinn sem birtist.

        > [!NOTE]
        > Ekki er hægt að fjarlægja viðfangs-, umsóknar- og tilboðsstig. en þau geta verið endurnefnd.

7. Valfrjáls: Bæta við eða fjarlægja aðgerðir.

    - Til að bæta við aðgerð skaltu draga það úr aðgerðalistanum hægra megin við viðeigandi stig. Einnig er hægt að tvísmella á aðgerðina og velja síðan stigið til að bæta því við.
    - Til að fjarlægja aðgerð skaltu stækka aðgerðina og velja síðan ruslakörfuhnappinn á verkþáttarhausnum.

8. Veldu **Vista**.
