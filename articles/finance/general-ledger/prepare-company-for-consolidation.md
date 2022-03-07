---
title: Undirbúa lögaðila fyrir sameiningarferlið
description: Við sameiningu er færslum safnað saman úr nokkrum settum af lyklum lögaðila í eitt sett af lyklum lögaðila. Þetta efnisatriði útskýrir hvernig á að undirbúa lögaðila undir sameiningu.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: a1ffbf79cdccab457b1aee1bc0f1d963bca49b3e390187c6be5da475f278a3d8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720503"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a>Undirbúa lögaðila fyrir sameiningarferlið

[!include [banner](../includes/banner.md)]

Við sameiningu er færslum safnað saman úr nokkrum settum af lyklum lögaðila í eitt sett af lyklum lögaðila. Þetta efnisatriði útskýrir hvernig á að undirbúa lögaðila undir sameiningu.

> [!NOTE]
> Mælt er með því að nota Management reporter fyrir Microsoft Dynamics 365 Finance til að sameina fjárhagsniðurstöður fyrir marga lögaðila á sameinuðu sniði. Management Reporter gerir kleift að stofna sameinaðar fjárhagsskýrslur yfir alla lögaðila, nota Excel til að flytja inn samstæðugögn frá öðrum upprunum og umbreyta upphæðum í hvaða fjölda skýrslugjaldmiðla sem er án þess að þurfa að keyra sameiningarferlið í Dynamics 365 Finance.

Hægt er að prenta skýrslur, t.d. fjárhagsskýrslur, úr sameinuðum lögaðila. Hins vegar er ekki hægt að nota sameinaðan lögaðila fyrir daglegar færslur.

Hægt er að sameina gögn úr lögaðila sem nota aðra gagnagrunna en þann fyrir sameinaða lögaðilann. Þessi sameiningarferli kallast *innflutnings-sameining*. Að öðrum kosti geta lögaðilar notað sama gagnagrunn og samsteypulögaðili. Þessi sameiningarferli kallast *sameining á neti*.

Sameinaði lögaðilinn safnar saman niðurstöðum og stöðum dótturfyrirtækjanna. Til að undirbúa sameinaðan lögaðila fyrir sameiningu skal fylgja þessum skrefum.

1. Farið í **Fjárhagur \> Uppsetning \> Fyrirtæki \> Lögaðilar**.
2. Veljið **Nýr** til að stofna lögaðilann sem verður sameinaður lögaðili.
3. Veljið gátreitinn **Nota fyrir sameiningarferli fjárhags** og færið síðan inn upplýsingar um sameinaðan lögaðila. Verið viss um að færa inn þessar upplýsingar nákvæmlega eins og þær eiga að birtast í fjárhagsskýrslum fyrir sameinaðan lögaðila.
4. Lokið síðunni.
5. Veljið sameinaðan lögaðila í reitnum efst í hægra horni síðunnar og veljið því næst **Í lagi**.
6. Farið í **Almennur fjárhagur \> Uppsetning \> Fjárhagur**.
7. Veljið bókhaldslykilinn, fjárhagsdagatalið, bókhaldsgjaldmiðlinn, valfrjálsan skýrslugjaldmiðil og sjálfgefna gerð gengis fyrir sameinaðan lögaðila. 
8. Farið í **Almennur fjárhagur \> Uppsetning \> Gjaldmiðill \> Gengi gjaldmiðils**.
9. Setja upp gengi gjaldmiðla í viðeigandi tímabila fyrir gjaldmiðla dótturfyrirtækis lögaðila.
10. Lokið síðunni.
11. Ef sameinaður lögaðili er með dótturfyrirtæki sem nota erlenda gjaldmiðla skal fylgja þessum skrefum:

    1. Farið í **Almennur fjárhagur \> Uppsetning \> Bókun \> Lyklar fyrir sjálfvirkar færslur**.
    2. Í reitnum **Bókunargerð** skal velja viðeigandi lykil:

        - Ef lögaðili er með erlend dótturfyrirtæki sem eru fjárhagslega og rekstrarlega háð yfirlögaðilanum skal velja viðeigandi lykil fyrir bókunargerðina **Rekstrarreikningur fyrir samstæðumismun**.
        - Ef verið er að sameina dótturfyrirtæki sem er fjárhagslega og rekstarlega óháð yfirlögaðila eða lögaðila sem inniheldur niðurstöður nokkur dótturfyrirtæki sem eru fjárhagslega og rekstrarlega óháð yfirlögaðila, og ef verið er að nota umreikningsaðgerðir til að sameina gögnin, skal velja viðeigandi lykil fyrir bókunargerðina **Efnahagslykill fyrir samstæðumismun**.

    3. Í reitnum **Aðallykill** skal velja aðallyklana sem á að nota fyrir breytingar á endurmati erlends gjaldmiðils.
    4. Lokið síðunni.

    Ef sameinaður lögaðili er stofnaður snemma á tímabili er hægt að endurmeta upphæði í erlendum gjaldmiðli þar sem gengi breytist á samstæðutímabilinu.

Sameinaður lögaðili er nú uppsettur fyrir reglubundnu vinnsluna **Sameina**. Hægt er að framkvæma annaðhvort innflutningssameiningu eða sameiningu á netinu.

- Til að framkvæma innflutningssameiningu skal fara í **Almennur fjárhagur \> Reglubundið \> Sameina \> Sameina \[Flytja inn úr\]**.
- Til að framkvæma sameiningu á netinu skal fara í **Almennur fjárhagur \> Reglubundið \> Sameina \> Sameina \[Á netinu\]**.

> [!NOTE]
> Áður en hægt er að keyra sameininguna þarf að undirbúa lögaðila dótturfyrirtækis fyrir sameiningu. Frekari upplýsingar er að finna í [Setja upp dótturfyrirtæki lögaðila fyrir sameiningu](set-up-subsidiary-company-for-consolidation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]