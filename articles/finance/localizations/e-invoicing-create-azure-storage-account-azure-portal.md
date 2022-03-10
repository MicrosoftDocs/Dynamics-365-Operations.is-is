---
title: Búðu til Azure geymslureikning í Azure gáttinni
description: Þetta efni útskýrir hvernig á að búa til Azure geymslureikning fyrir rafræna reikninga.
author: dkalyuzh
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3d9647e234b3603ef6305ec6031a793b744bbe98
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371951"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Búðu til Azure geymslureikning í Azure gáttinni

[!include [banner](../includes/banner.md)]

Allar rafrænar skrár sem eru búnar til af rafrænum reikningaþjónustu eða fara í þjónustuna við vinnslu eru geymdar í Microsoft Azure geymslureikningsílát. Til að tryggja að rafræn reikningagerð hafi aðgang að þessum gámum, verður þú að láta rafræna reikningsþjónustuna í té samnýtt aðgangsundirskrift (SAS) tákn geymslureikningsins. Að auki, til að tryggja að auðkennið sé geymt á öruggan hátt, skaltu ekki gefa SAS-táknið beint. Í staðinn skaltu geyma það í Azure lykilhólf og gefa upp Azure Key Vault leyndarmál.

1. Opnaðu geymslureikninginn sem þú ætlar að nota með rafrænum reikningaþjónustu.
2. Fara til **Stillingar** \> **Stillingar**, og vertu viss um að **Leyfa Blob almennan aðgang** færibreyta er stillt á **Virkt**.
3. Fara til **Gagnageymsla** \> **Gámar**, og búðu til ílát.
4. Sláið inn nafn geymslunnar og stillið reitinn **Almennt aðgangsstig** á **Einkaaðili (enginn nafnlaus aðgangur)**.
5. Opnaðu nýja ílátið og farðu í **Stillingar** \> **Aðgangsstefna**.
6. Veljið **Bæta við reglu** til að bæta við geymdri aðgangsreglu.
7. Stilltu **Auðkenni** reit eftir því sem við á.
8. Í **Heimildir** reit, veldu allar heimildir.

    ![Allar heimildir valdar í reitnum Heimildir í glugganum Bæta við stefnu.](media/e-invoicing-azure-1.png)

9. Færið inn upphafs- og lokadagsetningar. Lokadagsetningin á að vera fram í tímann.
10. Veljið **Í lagi** til að vista regluna og vistið síðan breytingarnar í geymsluna.
11. Fara til **Stillingar** \> **Sameiginleg aðgangsmerki**, og stilltu svæðisgildin.
12. Færið inn upphafs- og lokadagsetningar. Lokadagsetningin á að vera fram í tímann.
13. Í **Heimildir** reit, veldu eftirfarandi heimildir:

    - Lesið
    - Bæta við
    - Búa til
    - Skrifa
    - Virk útgáfa
    - Listi

14. Veljið **Mynda SAS-merki og vefslóð**.
15. Afritaðu og geymdu gildið í reitnum **Blob SAS-vefslóð**. Þetta gildi verður notað síðar í þessari aðferð og verður vísað til sem *URI undirskriftar fyrir sameiginlegan aðgang*.
16. Opnið lyklageymsluna sem ætlunin er að nota með rafrænni reikningsfærslu.
17. Fara til **Stillingar** \> **Leyndarmál**, og veldu **Búa til / flytja inn** að búa til leyndarmál.
18. Á síðunni **Stofna leynilykil**, í reitnum **Valkostir upphleðslu**, skal velja **Handvirkt**.
19. Færið inn heiti leynilykilsins. Þetta nafn verður notað við uppsetningu þjónustunnar í Regulatory Configuration Service (RCS) og verður vísað til sem *lykilhólf leyndarmál nafn*. Fyrir frekari upplýsingar um hvernig á að setja upp RCS, sjá [Settu upp reglustillingarþjónustu (RCS)](e-invoicing-set-up-rcs.md).
20. Í **Gildi** reit, sláðu inn URI undirskriftar fyrir sameiginlegan aðgang sem þú afritaðir áðan.
21. Velja **Stofna**.
