---
title: "Bókunarskilgreiningar"
description: "Þessi skrá gefur dæmi sýna hvernig bókunarskilgreiningar notaðar fyrir innkaupapantana og fjárveitingar úr fjárhagsáætlun."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4afe88012b28b74e25c30befb261b5ea2f633ce9
ms.openlocfilehash: 1091a37007146b36ba05aee3d047c4ae58f87168
ms.lasthandoff: 03/31/2017


---

# <a name="posting-definition-examples"></a>Dæmi um skilgreining bókun

Þessi skrá gefur dæmi sýna hvernig bókunarskilgreiningar notaðar fyrir innkaupapantana og fjárveitingar úr fjárhagsáætlun.

Áður en í þessu efnisatriði er lesið, ætti að kynna sér bókunarskilgreiningar og skilgreining færslubókunar. Sjá upplýsingar í [Bókunarskilgreiningar](posting-definitions.md). Eftirfarandi dæmi er hægt að setja á upp á **Bókunarskilgreiningar** síðu. hvert Dæmi inniheldur þessum hlutum:

-   Bókunarskilgreining – jöfnunarskilyrði
-   bókunarskilgreining – Myndað færslur
-   Færslur með lykla, víddargildi og upphæðir
-   fjárhagsfærslur myndaðar úr bókunarskilgreiningu

Þegar samsvörun á sér stað milli lykla og víddargildi í **skilyrði fyrir samsvörun** rúðunni fyrir bókunarskilgreiningu og lykla og víddargildi á færslunni, myndast fjárhagsfærslur á grundvelli **Myndaðar færslur** rúðunni fyrir bókunarskilgreiningar. 
> [!NOTE]
> Til að tengja ákveðna færslugerð bókunarskilgreiningu, í **bókunarskilgreiningar Færslna** síðu. Eftir að tengja bókunarskilgreiningu færslugerð og veljið **Nota bókunarskilgreiningar** í í **fjárhagsfæribreytur** síðu allar færslur af valinni gerð verður að nota bókunarskilgreiningar.

## <a name="example-purchase-order-encumbrances"></a>Dæmi: Fjárúthlutun innkaupapöntunar
Þegar þú virkjar fjárúthlutunar með því að velja **Virkja ferli fjárúthlutunar** á **fjárhagsfæribreytur** síðu, verður að nota  bókunarskilgreiningar til að skrá fjárúthlutanir í fjárhaginn fyrir hvaða lykla sem á að taka frá. Í flestum tilvikum, alla kostnaðarlykla eru teknar frá á efnahagsreikningi. 

Bókunarskilgreiningar fyrir fjárúthlutanir eru settir upp fyrir í **Innkaup** kerfiseiningu á **Bókunarskilgreiningar** síðunni. Svo í **Innkaup** svæði í **bókunarskilgreiningar Færslna** síðu er hægt að velja færslugerð **Innkaupapöntunar**  til að tengja bókunarskilgreiningar við innkaupapöntunum. 

Allar fylgiskjalafærslur fyrir fjárúthlutanir innkaupapantana að að vera í jafnvægi (debet verða að vera sama og inneign) í hverri einkvmri vídd á fylgiskjal.

### <a name="posting-definition--match-criteria"></a>Bókunarskilgreining – jöfnunarskilyrði

| Lykilskipulag       | Samsvarandi lykilnúmer | Forgangur |
|-------------------------|----------------------|----------|
| Lykilskipulag- P&L | \*                   | 1        |

* Autt gildi í **Samsvörunarlykilnúmer** svæði þýðir að allir samsvörunarlyklar í skilgreindu lykilskipulagi eru hluti af jöfnunarreglan.

### <a name="posting-definition--generated-entries"></a>bókunarskilgreining – Myndað færslur

| Lykilskipulag | Myndað lykilnúmer                    | Myndað debet/kredit |
|-------------------|---------------------------------------------|------------------------|
| Staða           | 300143 - -(fjárúthlutunarlykill)             | Sama                   |
| Staða           | 300144 - -(Frátekning fyrir fjárúthlutunarlykill) | Jafnvægi              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Færslur með lykla, víddargildi og upphæðir

Lyklar og víddargildi koma annað hvort úr dreifing á fjárhagsupphæð sem eru færðar inn fyrir innkaupapöntunarlínu, eða úr lykla og víddir sem eru myndaðar sjálfvirkt á grundvelli sjálfgefnar stillingar fyrir lánardrottna, vörur, flokka og sniðmát víddar.

| Lykill + víddir           | Debet  | Kredit | Athugasemd |
|--------------------------------|--------|--------|---------|
| 606400-Samkvæmt\_1 Samkvæmt\_3566 Þjálfun | 250,00 |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>fjárhagsfærslur myndaðar úr bókunarskilgreiningu

Fjárhagsfærslur sem myndaðar eru eru stofnaðar til að skrá fjárúthlutanir.

| Lykill + víddir           | Debet  | Kredit | Athugasemd |
|--------------------------------|--------|--------|---------|
| 300143-Samkvæmt\_1 Samkvæmt\_3566 Þjálfun | 250,00 |        |         |
| 300144-Samkvæmt\_1 Samkvæmt\_3566 Þjálfun |        | 250,00 |         |

Í þessu dæmi, hvaða lykil sem er hluti af Lykilskipulagi - P & L samsvarar skilyrði bókunarskilgreiningar. Þess vegna, þegar 606500-Samkvæmt\_1 Samkvæmt\_3566 Þjálfun er metin, myndast færslur eru stofnaðar fyrir reikninga sem eru skilgreindar í á **Myndaðar færslur** rúðunni fyrir bókunarskilgreiningar.

## <a name="example-budget-appropriations"></a>Dæmi: fjárveiting fjárhagsáætlunar
Þegar þú leyfa fjárveitingu fjárhagsáætlunar með því að velja **virkja fjárveitingu fjárhagsáætlunar** á **fjárhagsfæribreytur** síðunni, verður að nota bókunarskilgreiningar til að skrá færslur fjárhagsáætlunarskrár í fjárhag. þegar skilgreining fjárhagsáætlunarstýringar er virk og kveitk á henni, má nota bókunarskilgreiningar og færslu bókunarskilgreiningar til að styðja við skráningu á færslum fyrir greiðsluheimilda, , endurskoðun, flutninga, verk, eignir og framboð og eftirspurnarspár í fjárhag. 

Til að setja upp bókunarskilgreining fyrir færslur fjárhagsáætlunar í með fjárhagsáætlunargerðina **Upprunalega fjárhagsáætlun**, og sem hefur fjárveiting virkjað, veljið **Fjárhagsáætlun** kerfiseiningu á **Bókunarskilgreiningar** síðu. Síðan, í **Fjárhagsáætlunar** svæði í **skilgreiningar færslubókunar** síðu er hægt er að nota fjárhagsáætlunarkóðana til að tengja bókunarskilgreiningar við færslur fjárhagsáætlunarskrár sem eru með fjárhagsáætlunargerðina **Upprunalega fjárhagsáætlun**. 

Þegar fjárveitingar úr fjárhagsáætlun og bókunarskilgreiningar eru virkjaðar, eru færslur fjárhagsáætlunarskrár skráðar fyrir fjárhagsáætlunarstýringu og í fjárhag.

### <a name="posting-definition--match-criteria"></a>Bókunarskilgreining – jöfnunarskilyrði

| Lykilskipulag       | Samsvarandi lykilnúmer | Forgangur |
|-------------------------|----------------------|----------|
| Lykilskipulag- P&L | \*                   | 1        |

* Autt gildi í **Samsvörunarlykilnúmer** svæði þýðir að allir samsvörunarlyklar í skilgreindu lykilskipulagi eru hluti af jöfnunarreglan.

### <a name="posting-definition--generated-entries"></a>bókunarskilgreining – Myndað færslur

| Lykilskipulag | Myndað lykilnúmer              | Myndað debet/kredit |
|-------------------|---------------------------------------|------------------------|
| Lykilskipulag | 300145 - -(Áætlað tekjur lykill) | Sama                   |
| Lykilskipulag | 300146 - -(fjárúthlutunarlykill)     | Jafnvægi              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a>Færslur með lykla, víddargildi og upphæðir

Færa inn lykla, víddargildi og upphæðir fyrir færsla fjárhagsáætlunarlykils við **færsla í fjárhagsáætlunarskrá** síðu.

| Lykill + víddir           | Debet | Kredit | Athugasemd |
|--------------------------------|-------|--------|---------|
| 606400-Samkvæmt\_1 Samkvæmt\_3566 Þjálfun |       | 250,00 |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a>fjárhagsfærslur myndaðar úr bókunarskilgreiningu

Fjárhagsfærslur eru myndaðar til að skrá upprunalega fjárhagsáætlun á hverja vídd.

| Lykill + víddir           | Debet  | Kredit | Athugasemd |
|--------------------------------|--------|--------|---------|
| 300145-Samkvæmt\_1 Samkvæmt\_3566 Þjálfun |        | 250,00 |         |
| 300146-Samkvæmt\_1 Samkvæmt\_3566 Þjálfun | 250,00 |        |         |

Í þessu dæmi, hvaða lykil sem er hluti af Lykilskipulagi - P & L samsvarar skilyrði bókunarskilgreiningar. Þess vegna, þegar 606400-Samkvæmt\_1 Samkvæmt\_3566 Þjálfun er metin, fjárhagsfærslur sem myndaðar eru stofnaðar.




