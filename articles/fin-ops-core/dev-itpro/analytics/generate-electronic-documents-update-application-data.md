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
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="47fff-103">Búa til rafræn skjöl og uppfæra forritsgögn með því að nota rafræna skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="47fff-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="47fff-104">Hægt er að hanna snið fyrir rafræna skýrslugerð (ER) sem nota má í forritinu til að búa til rafræn skjöl á útleið.</span><span class="sxs-lookup"><span data-stu-id="47fff-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="47fff-105">Einnig er hægt að hanna rafræn skýrslugerðarsnið sem þátta rafræn skjöl á innleið og nota innihaldið í þeim skjölum til að uppfæra gögn í forritinu.</span><span class="sxs-lookup"><span data-stu-id="47fff-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="47fff-106">Með þessari virkni er hægt að nota eitt rafrænt skýrslugerðarsnið til að búa til rafræn skjöl á útleið og uppfæra svo gögn í forritinu.</span><span class="sxs-lookup"><span data-stu-id="47fff-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="47fff-107">Þessa aðgerð er einnig hægt að nota við eftirfarandi aðstæður:</span><span class="sxs-lookup"><span data-stu-id="47fff-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="47fff-108">Til að koma í veg fyrir endurtekna notkun á gögnum í forritinu í ferlum sem koma á eftir, getur þú merkt forritsgögn strax eftir að þau eru notuð til að búa til rafræn skjöl.</span><span class="sxs-lookup"><span data-stu-id="47fff-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="47fff-109">Til dæmis er hægt að merkja greiðslufærslur sem þegar unnar strax eftir að þær hafa verið innifaldar í greiðsluskilaboðum.</span><span class="sxs-lookup"><span data-stu-id="47fff-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="47fff-110">Til að geyma úrvinnsluupplýsingar um rafræn skjöl sem hafa verið mynduð með ER-segðum.</span><span class="sxs-lookup"><span data-stu-id="47fff-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="47fff-111">Til dæmis einkvæmt auðkenni fyrir greiðsluskilaboð sem er myndað með ER-segð.</span><span class="sxs-lookup"><span data-stu-id="47fff-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="47fff-112">Segðin er byggð á upplýsingunum sem færðar eru inn í ER-svarglugga þegar ER-snið er keyrt til að mynda skjöl.</span><span class="sxs-lookup"><span data-stu-id="47fff-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="47fff-113">Til að fá frekari upplýsingar um þessa aðgerð skaltu spila verkefnaleiðbeiningarnar Rafræn skýrslugerð - Myndun skjala með uppfærslu forritsgagna (hluti af viðskiptaferlinu 7.5.4.3 Komast yfir/þróa íhluti fyrir upplýsingatækniþjónustu/lausnir (10677)), sem leiða þig í gegnum smáatriði Intrastat-skýrslugerðar og skjalageymslu.</span><span class="sxs-lookup"><span data-stu-id="47fff-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="47fff-114">Eftirfarandi skrár eru nauðsynlegar til að ljúka skrefum í þessum verkefnaleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="47fff-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="47fff-115">Sæktu og vistaðu þessar skrár í staðbundinni vél.</span><span class="sxs-lookup"><span data-stu-id="47fff-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="47fff-116">Stilling á gagnalíkani í rafrænni skýrslugerð: Intrastat (líkan)</span><span class="sxs-lookup"><span data-stu-id="47fff-116">ER data model configuration: Intrastat (model)</span></span>](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [<span data-ttu-id="47fff-117">Stilling líkansvörpunar í rafrænni skýrslugerð: Intrastat (vörpun)</span><span class="sxs-lookup"><span data-stu-id="47fff-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [<span data-ttu-id="47fff-118">Sniðsskilgreining í rafrænni skýrslugerð: Intrastat (snið)</span><span class="sxs-lookup"><span data-stu-id="47fff-118">ER format configuration: Intrastat (format)</span></span>](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
