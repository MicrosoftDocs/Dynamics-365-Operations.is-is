---
title: Birgðabókin þín er læst og runuvinnsla verkflæðisins virkar ekki
description: Ein af birgðabókum notanda er læst af einhverri aðgerð og ekki er verið að losa hana
author: sherry-zheng
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8b21ec2e2b3b8546dcb138422c5540053392c179
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476633"
---
# <a name="your-inventory-journal-is-locked-and-the-workflow-batch-job-doesnt-work"></a>Birgðabókin þín er læst og runuvinnsla verkflæðisins virkar ekki

## <a name="symptoms"></a>Einkenni

Ein af birgðabókum notanda er læst af einhverri aðgerð og ekki er verið að losa hana. Ef óþekkt villa kemur til dæmis upp við bókun (sem er aðgerð kerfislæsingar) gæti færslubókin áfram verið í læstri stöðu. Í þessu tilviki mun rekill vinnuliðar í verkflæði birta villu á meðan sannprófun á læsingu er gerð.

## <a name="resolution"></a>Lausn

Skráið ykkur inn í SQL-þjónstilvik fyrir Supply Chain Management og athugið hvort **InventJournalTable.SystemBlocked** sé stillt á *1*. Ef svo er skal ganga úr skugga um að færslubókin eigi ekki að vera í læstri stöðu og síðan endurstilla **InventJournalTable.SystemBlocked** á *0*.
