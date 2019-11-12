---
title: Skanna strikamerki með myndavél í forritinu Dynamics 365 for Finance and Operations – Warehousing
description: Þetta efnisatriði útskýrir hvernig eigi að setja upp forritið Dynamics 365 for Finance and Operations – Warehousing til að skanna strikamerki með myndavél á fartæki.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 58cf27a250778d68bdffa1eefa5e939276e467fc
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578150"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a>Skanna strikamerki með myndavél í forritinu Dynamics 365 Supply Chain Management - Warehousing

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig eigi að setja upp forritið Dynamics 365 for Finance and Operations – Warehousing til að skanna strikamerki með myndavél á fartæki. 

## <a name="prerequisites"></a>Forkröfur
Til að nota þessa aðgerð þarf að vera með útgáfu 1.2.0.0 af forritinu Warehousing uppsetta og tækið þitt verður að vera með myndavél. Þegar forritið er opnað eftir uppfærslu mun forritið biðja um leyfi til að nota myndavélina. Ef tækið er ekki með myndavél mun engin beiðni koma upp og ekki verður hægt að nota myndavélina sem skanna. 

## <a name="setup"></a>Setja upp
Í skjástillingum vöruhúsaforrits er hægt að velja hvort eigi að nota myndavélina til að skanna strikamerki. Ef þú virkjar **Nota myndavél sem skanna** getur þú notað myndavélina fyrir öll ílagssvæði sem eru með æskilegan ílagsham stilltan á **Skönnun**. 

Til að stjórna því hvort ílagssvæði eigi að vera skannanlegt skal á síðunni **Reitaheiti vöruhúsaforrits** stilla **Æskilegan ílagsham** á **Skönnun**. Þegar þessi valkostur er valinn er hægt að nota myndavél sem skanna í vöruhúsaforritinu. Upplýsingar um hvernig eigi að skilgreina svæðaheita í vöruhúsi er hægt að finna í [Skilgreina svæðaheiti forrits í vöruhúsaforriti](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).

## <a name="supported-bar-code-formats"></a>Studd snið strikamerkja
Algengustu snið strikamerkja eru studd, þ.á.m. kóði 128, kóði 39, kóði 93, EAN-8, EAN-13, UPC-E, UPC-A og QR kóðar. 

## <a name="navigation"></a>Yfirlit
Myndavélasíðan mun ræsast fyrir allar síður þar sem ílagssvæðið er með æskilegan ílagsham stilltan á skönnun. Þegar þú ert á síðu myndavélar skaltu nota eftirfarandi valmöguleika til að fletta:
- Smellt er á hnappinn Til baka til að fara aftur á verk- og upplýsingasíðuna. 
- Smellt er á blýantinn á verk- og upplýsingasíðunni til að fara á síðuna þar sem hægt er að færa innsláttinn inn handvirkt.
- Smellt er á myndavélina á verk- og upplýsingasíðunni til að fara aftur á myndavélasíðuna. 

| Verk- og upplýsingasíða | Myndavélasíða | 
| :---------------------: | :--------------------: |
| ![Síðan Dæmi um verkupplýsingar myndavélarskönnunar](./media/camera-scanning-example-task-detail-page50.png)          | ![Minni síða myndavélar dæmi um myndavélarskönnun](./media/camera-scanning-example-camera-page50.png)          |

Þegar smellt er á myndavélahnappinn á myndavélasíðunni mun hún sýnast deyfð á meðan reynt er að auðkenna strikamerki. Ef ekki er hægt að auðkenna strikamerki innan 5 sekúndna mun ferlið renna út á tíma og myndavélahnappurinn verður aftur tiltækur. Þá er aftur hægt að skanna strikamerki.

Þegar myndavél er beint að strikamerki skal staðsetja strikamerkið innan hornklofanna til að fá sem bestar niðurstöðu. Þegar tekst að skanna strikamerki er unnið úr niðurstöðunni og þér verður vísað yfir á næsta skref. Ef næsta skref inniheldur annað ílagssvæði með æskilegan ílagsham stilltan á skönnun mun myndavélasíðan ræsast á ný. Ef næsta skref er ekki skönnunarsvæði mun myndavélasíðan ekki ræsast.

