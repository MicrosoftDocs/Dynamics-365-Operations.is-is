---
title: Stofna Azure-geymslureikning í Azure-gáttinni
description: Þessi grein útskýrir hvernig á að stofna Azure-geymslureikning fyrir rafræna reikningagerð.
author: gionoder
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 5eca23985c48f4e577bd4567cc2e324df5aa9690
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291637"
---
# <a name="create-an-azure-storage-account-in-the-azure-portal"></a>Stofna Azure-geymslureikning í Azure-gáttinni

[!include [banner](../includes/banner.md)]

Allar rafrænar skrár sem eru myndaðar af rafrænum reikningum eða fara í þjónustuna meðan á vinnslu stendur eru geymdar í Microsoft Azure geymslu reikningsins þíns. Til að tryggja að rafrænn reikningur hafi aðgang að þessum gámum verður þú að framvísa undirskrift fyrir sameiginlegan aðgang (SAS) að geymslureikningi til rafrænu reikningagerðarþjónustunnar. Til að tryggja að merkið sé geymt á öruggan hátt skaltu auk þess ekki framvísa SAS merkinu beint. Í staðinn skaltu geyma það í Azure lyklahvelfingu, og velja leynilykil fyrir Azure lyklahvelfingu.

1. Opnið geymslureikninginn sem ætlunin er að nota með rafrænni reikningsfærslu.
2. Farðu í **Stillingar** \> **Skilgreining** og gakktu úr skugga um að færibreytan **Leyfa opinn Blob-aðgang** sé stillt á **Virkt**.
3. Farið í **Gagnageymslu**\>**Geymslur** og stofnið geymslu.
4. Sláið inn nafn geymslunnar og stillið reitinn **Almennt aðgangsstig** á **Einkaaðili (enginn nafnlaus aðgangur)**.
5. Opnið nýju geymsluna og farið í **Stillingar** \> **Aðgangsregla**.
6. Veljið **Bæta við reglu** til að bæta við geymdri aðgangsreglu.
7. Stillið reitinn **Kennimerki** og eftir því sem við á.
8. Í reitnum **Aðgangsheimildir** á að velja allar heimildir.

    ![Allar heimildir valdar í reitnum Heimildir í svarglugganum Bæta við stefnu.](media/e-invoicing-azure-1.png)

9. Færið inn upphafs- og lokadagsetningar. Lokadagsetningin á að vera fram í tímann.
10. Veljið **Í lagi** til að vista regluna og vistið síðan breytingarnar í geymsluna.
11. Farið í **Stillingar** \> **Samnýttir aðgangslyklar** og stillið gildin í reitnum.
12. Færið inn upphafs- og lokadagsetningar. Lokadagsetningin á að vera fram í tímann.
13. Í reitnum **Heimildir** skal velja eftirfarandi heimildir:

    - Lesið
    - Bæta við
    - Búa til
    - Skrifa
    - Eyða
    - List

14. Veljið **Mynda SAS-merki og vefslóð**.
15. Afritaðu og geymdu gildið í reitnum **Blob SAS-vefslóð**. Þetta gildi verður notað síðar í þessu ferli og verður vísað til þess sem *URI-undirskrift samnýtts aðgangs*.
16. Opnið lyklageymsluna sem ætlunin er að nota með rafrænni reikningsfærslu.
17. Farið í **Stillingar** \> **Leynilyklar** og veljið **Búa til/Flytja inn** til að stofna nýjan leynilykil.
18. Á síðunni **Stofna leynilykil**, í reitnum **Valkostir upphleðslu**, skal velja **Handvirkt**.
19. Færið inn heiti leynilykilsins. Þetta heiti verður notað við uppsetningu þjónustunnar í Regulatory Configuration Service (RCS) og verður vísað í það sem *leyniheiti lyklageymslu*. Frekari upplýsingar um hvernig á að setja upp RCS eru í [Setja upp Regulatory Configuration Service (RCS)](e-invoicing-set-up-rcs.md).
20. Í reitinn **Gildi** skal færa inn samnýtta URI-undirskrift sem áður var afrituð.
21. Velja **Stofna**.
