---
title: Flýtiinnflutningur/-útflutningur
description: Tilgangur Flýti inn útflutning er að láta innflutningur og útflutningur með skrefunum færri.
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: 7655de1399c49328bae1736c796325e546796bd5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181152"
---
# <a name="quick-import-export"></a><span data-ttu-id="5f2e4-103">Flýtiinnflutningur/-útflutningur</span><span class="sxs-lookup"><span data-stu-id="5f2e4-103">Quick import export</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5f2e4-104">Tilgangur Flýti inn útflutning er að láta innflutningur og útflutningur með skrefunum færri.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-104">The purpose of Quick import export is to let you import and export with fewer steps.</span></span>

<span data-ttu-id="5f2e4-105">Við bætt Flýti flytja inn Flytja Út eiginleikann til að láta notendur innflutning eða útflutning einfalt vinnslur sem þeir vilja að keyra á fljótlegan hátt.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-105">We added the Quick Import Export feature to let users import or export simple jobs that they want to execute quickly.</span></span> <span data-ttu-id="5f2e4-106">Æskilegast þessi eiginleiki er notaður í aðstæðum þar sem skrá varpanir sjálfkrafa inn í kerfið og notandi þarf ekki að fara í gegnum ítarlega vörpun eða stofna endurtekin innflutnings eða útflutnings vinnslur.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-106">Ideally this feature is used in scenarios in which a file automatically maps to the system and user does not need to go through advanced mapping or create repeated import or export jobs.</span></span>

- <span data-ttu-id="5f2e4-107">Eiginleikinn styður unnið með bæði út úr kassanum og sérsniðinnar einingar.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-107">This feature supports working with both out-of-the-box and custom entities.</span></span>
- <span data-ttu-id="5f2e4-108">Hægt er að flytja inn úr skrám og ef verið er að nota ODBC gagnagjafi hægt að velja fyrirspurn til að skilgreina innflutning.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-108">You can import from files, and if you are using an ODBC data source, you can select a query to use to define your import.</span></span>
- <span data-ttu-id="5f2e4-109">Verður hafa áður skilgreindar uppruna gagna snið fyrir AX eða Skrá og vita þar sem þær eru.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-109">You must have previously defined source data formats for either AX or File, and know where they are located.</span></span>
- <span data-ttu-id="5f2e4-110">Ekki þarf að stofna vinnsluhóp sem nota á flýti inn-og útflutning, eitt verður sjálfkrafa stofnuð í kerfinu við keyrslu vinnslunnar innflutnings eða útflutnings.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-110">You do not need to create a processing group to use quick import/export, one will be automatically created by the system when executing the import or export job.</span></span> <span data-ttu-id="5f2e4-111">Einnig er hægt að velja halda á feril flutt inn með flýti innflutning og útflutning gagna.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-111">You can also choose keep the history of the data imported by the quick import/export.</span></span>

  <span data-ttu-id="5f2e4-112">Athugið að Flýti inn útflutning gerir ráð fyrir því sem verið er að þekkja hugtökin DIXF.</span><span class="sxs-lookup"><span data-stu-id="5f2e4-112">Note that Quick import export assumes that you are familiar with the concepts of DIXF.</span></span>


