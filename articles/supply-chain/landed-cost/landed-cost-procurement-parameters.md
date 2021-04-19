---
title: Færibreytur innkaupa og aðfanga fyrir heildarkostnað
description: Þetta efnisatriði lýsir því hvernig setja á upp viðeigandi færibreytur fyrir innkaup og aðföng þegar Heildarkostnaður einingin er notuð.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833930"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Færibreytur innkaupa og aðfanga fyrir heildarkostnað

[!include [banner](../../includes/banner.md)]

Síðan **Færibreytur innkaupa og aðfanga** er með nokkrar stillingar sem eiga sérstaklega við þegar einingin **Heildarkostnaður** er notuð. Nota skal svargluggann **Uppfæra pöntunarlínur** sem er opnaður af síðunni **Færibreytur innkaupa og aðfanga** til að tilgreina hvort innkaupapöntunarlínur eigi að vera uppfærðar sjálfkrafa þegar breytingar eru gerðar á haus innkaupapöntunar.

Fylgið eftirfarandi skrefum til að ljúka þessari uppsetningu.

1. Opnið **Innkaup og aðföng \> Uppsetning \> Færibreytur innkaupa og aðfanga**.
1. Í flipanum **Almennt** skal velja tengilinn **Uppfæra pöntunarlínur**.
1. Svarglugginn **Uppfæra pöntunarlínur** birtir lista yfir reitina í pöntunarhausnum sem geta einnig sett á sjálfvirkar uppfærslur á viðeigandi reitum í pöntunarlínunum. Veljið hvern reit á listanum á eitt af eftirfarandi gildum:

    - **Alltaf** – Pantanalínur á að uppfæra sjálfkrafa þegar pöntunarhausinn er uppfærður.
    - **Aldrei** – Pantanalínur ætti aldrei að uppfæra sjálfkrafa þegar pöntunarhausinn er uppfærður.
    - **Kvaðning** – Notandi fær kvaðningu um að velja hvort uppfæra eigi pöntunarlínurnar eða ekki.
