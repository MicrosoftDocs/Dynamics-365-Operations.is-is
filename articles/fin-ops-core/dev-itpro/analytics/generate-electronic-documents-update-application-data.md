---
title: Mynda rafræn skjöl og uppfæra forritagögn með rafrænni skýrslugerð
description: Hægt er að hanna snið fyrir rafræna skýrslugerð (ER) sem nota má í forritinu til að búa til rafræn skjöl á útleið. Einnig er hægt að hanna rafræn skýrslugerðarsnið sem þátta rafræn skjöl á innleið og nota innihaldið í þeim skjölum til að uppfæra gögn í forritinu.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 4b9e17d67c437d384ab941d28b8d5ce2b0e3738f
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688389"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Mynda rafræn skjöl og uppfæra forritagögn með rafrænni skýrslugerð

[!include [banner](../includes/banner.md)]

Hægt er að hanna snið fyrir rafræna skýrslugerð (ER) sem nota má í forritinu til að búa til rafræn skjöl á útleið. Einnig er hægt að hanna rafræn skýrslugerðarsnið sem þátta rafræn skjöl á innleið og nota innihaldið í þeim skjölum til að uppfæra gögn í forritinu.

Með þessari virkni er hægt að nota eitt rafrænt skýrslugerðarsnið til að búa til rafræn skjöl á útleið og uppfæra svo gögn í forritinu. Þessa aðgerð er einnig hægt að nota við eftirfarandi aðstæður:

- Til að koma í veg fyrir endurtekna notkun á gögnum í forritinu í ferlum sem koma á eftir, getur þú merkt forritsgögn strax eftir að þau eru notuð til að búa til rafræn skjöl. Til dæmis er hægt að merkja greiðslufærslur sem þegar unnar strax eftir að þær hafa verið innifaldar í greiðsluskilaboðum.
- Til að geyma úrvinnsluupplýsingar um rafræn skjöl sem hafa verið mynduð með ER-segðum. Til dæmis einkvæmt auðkenni fyrir greiðsluskilaboð sem er myndað með ER-segð. Segðin er byggð á upplýsingunum sem færðar eru inn í ER-svarglugga þegar ER-snið er keyrt til að mynda skjöl.

Til að fá frekari upplýsingar um þessa aðgerð skaltu spila verkefnaleiðbeiningarnar Rafræn skýrslugerð - Myndun skjala með uppfærslu forritsgagna (hluti af viðskiptaferlinu 7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)), sem leiða þig í gegnum smáatriði Intrastat-skýrslugerðar og skjalageymslu. Eftirfarandi skrár eru nauðsynlegar til að ljúka skrefum í þessum verkefnaleiðbeiningum. Sæktu og vistaðu þessar skrár í staðbundinni vél.

- [Stilling á gagnalíkani í rafrænni skýrslugerð: Intrastat (líkan)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Stilling líkansvörpunar í rafrænni skýrslugerð: Intrastat (vörpun)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Sniðsskilgreining í rafrænni skýrslugerð: Intrastat (snið)](https://go.microsoft.com/fwlink/?linkid=849038)
