---
title: Mynda rafræn skjöl og uppfæra forritagögn með rafrænni skýrslugerð
description: Hægt er að hanna snið fyrir rafræna skýrslugerð (ER) sem nota má í forritinu til að búa til rafræn skjöl á útleið.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f66a173c7d66f915a7802e42caf1a36f661eea1
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944318"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Búa til rafræn skjöl og uppfæra forritsgögn með því að nota rafræna skýrslugerð

[!include [banner](../includes/banner.md)]

Hægt er að hanna snið fyrir rafræna skýrslugerð (ER) sem nota má í forritinu til að búa til rafræn skjöl á útleið. Einnig er hægt að hanna rafræn skýrslugerðarsnið sem þátta rafræn skjöl á innleið og nota innihaldið í þeim skjölum til að uppfæra gögn í forritinu.

Með þessari virkni er hægt að nota eitt rafrænt skýrslugerðarsnið til að búa til rafræn skjöl á útleið og uppfæra svo gögn í forritinu. Þessa aðgerð er einnig hægt að nota við eftirfarandi aðstæður:

- Til að koma í veg fyrir endurtekna notkun á gögnum í forritinu í ferlum sem koma á eftir, getur þú merkt forritsgögn strax eftir að þau eru notuð til að búa til rafræn skjöl. Til dæmis er hægt að merkja greiðslufærslur sem þegar unnar strax eftir að þær hafa verið innifaldar í greiðsluskilaboðum.
- Til að geyma úrvinnsluupplýsingar um rafræn skjöl sem hafa verið mynduð með ER-segðum. Til dæmis einkvæmt auðkenni fyrir greiðsluskilaboð sem er myndað með ER-segð. Segðin er byggð á upplýsingunum sem færðar eru inn í ER-svarglugga þegar ER-snið er keyrt til að mynda skjöl.

Til að fá frekari upplýsingar um þessa aðgerð skaltu spila verkefnaleiðbeiningarnar Rafræn skýrslugerð - Myndun skjala með uppfærslu forritsgagna (hluti af viðskiptaferlinu 7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)), sem leiða þig í gegnum smáatriði Intrastat-skýrslugerðar og skjalageymslu. Eftirfarandi skrár eru nauðsynlegar til að ljúka skrefum í þessum verkefnaleiðbeiningum. Sæktu og vistaðu þessar skrár í staðbundinni vél.

- [Stilling á gagnalíkani í rafrænni skýrslugerð: Intrastat (líkan)](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [Stilling líkansvörpunar í rafrænni skýrslugerð: Intrastat (vörpun)](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [Sniðsskilgreining í rafrænni skýrslugerð: Intrastat (snið)](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
