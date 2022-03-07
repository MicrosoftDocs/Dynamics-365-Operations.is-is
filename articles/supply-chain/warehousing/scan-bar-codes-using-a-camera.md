---
title: Skanna strikamerki með myndavél í vöruhúsaforriti
description: Þetta efnisatriði útskýrir hvernig eigi að setja upp vöruhúsaforritið til að skanna strikamerki með því að nota myndavél á fartæki.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: fd4818ab936e1c93000793da756c97df6d05b2a9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430126"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-app"></a>Skanna strikamerki með myndavél í vöruhúsaforriti

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig eigi að setja upp vöruhúsaforritið til að skanna strikamerki með því að nota myndavél á fartæki. 

## <a name="prerequisites"></a>Forkröfur
Til að nota þessa aðgerð þarf að vera með útgáfu 1.2.0.0 af vöruhúsaforrit uppsetta og tækið þitt verður að vera með myndavél. Þegar forritið er opnað eftir uppfærslu mun forritið biðja um leyfi til að nota myndavélina. Ef tækið er ekki með myndavél mun engin beiðni koma upp og ekki verður hægt að nota myndavélina sem skanna. 

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

