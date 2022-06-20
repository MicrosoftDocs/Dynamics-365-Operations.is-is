---
title: Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 1 - Stofna snið)
description: Þessi grein lýsir því hvernig á að stilla rafrænt skýrslusnið til að telja og leggja saman byggt á gögnum um textaúttak sem þegar er búið til. (Hluti 1)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85a25715018f30d2fd8f1405d50cee0b420c0d34
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902626"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 1 - Stofna snið)

[!include [banner](../../includes/banner.md)]

Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað. Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.

Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.

Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Fá aðgang að lista yfir skilgreiningar sem Microsoft veitir
1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.
    * Gakktu úr skugga um að „Litware, Inc.“ veitandi sé tiltæk og merkt Virk.  
2. Veldu „Litware, Inc.” veita.
3. Smella á Geymslur.
    * Sleppa önnur þrep í núverandi undirverki ef gagnasafn af gerð 'Rekstrartilföngum' er þegar til.  
4. Smelltu á Bæta við til að opna felligluggann.
5. Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".
6. Smellið á Stofna gagnasafn.
7. Smellið á „Í lagi“.

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Sækja Intrastat-skilgreiningar sem Microsoft veitir
1. Smellt er á Opin.
2. Í trénu skal velja 'Intrastat model\Intrastat (DE)'.
3. Smelltu á Flytja inn.
    * Smelltu á innflutning fyrir útgáfu 1.1 fyrir valda skilgreiningu.  
4. Smella á Já.
5. Lokið síðunni.
6. Lokið síðunni.
7. Smelltu á Grunnstillingar skýrslugerðar
8. Í trénu skal víkka út 'Intrastat model'.
9. Í trénu skal velja 'Intrastat model\Intrastat (DE)'.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]