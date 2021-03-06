---
title: Skanna strikamerki með myndavél í farsímaforriti vöruhúsakerfis
description: Þetta efnisatriði útskýrir hvernig eigi að setja upp farsímaforrit vöruhúsakerfis til að skanna strikamerki með því að nota myndavél á fartæki.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831219"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Skanna strikamerki með myndavél í farsímaforriti vöruhúsakerfis

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig eigi að setja upp farsímaforrit vöruhúsakerfis til að skanna strikamerki með því að nota myndavél á fartæki.

## <a name="setup"></a>Setja upp

Í skjástillingum farsímaforrits vöruhúsakerfis er hægt að velja hvort eigi að nota myndavélina til að skanna strikamerki. Ef þú virkjar **Nota myndavél sem skanna** getur þú notað myndavélina fyrir öll ílagssvæði sem eru með æskilegan ílagsham stilltan á **Skönnun**.

Til að stjórna því hvort ílagssvæði eigi að vera skannanlegt skal á síðunni **Reitaheiti vöruhúsaforrits** stilla **Æskilegan ílagsham** á **Skönnun**. Þegar þessi valkostur er valinn er hægt að nota myndavél sem skanna í farsímaforrit vöruhúsakerfis. Frekari upplýsingar eru í [Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis](configure-app-field-names-priorities-warehouse.md).

## <a name="supported-bar-code-formats"></a>Studd snið strikamerkja

Algengustu snið strikamerkja eru studd, þ.á.m. kóði 128, kóði 39, kóði 93, EAN-8, EAN-13, UPC-E, UPC-A og QR kóðar.

## <a name="navigation"></a>Yfirlit

Myndavélasíðan mun ræsast fyrir allar síður þar sem færslureiturinn er með **Æskilega inntaksstilingu** stillta á *Skönnun*. Þegar þú ert á síðu myndavélar skaltu nota eftirfarandi valmöguleika til að fletta:

- Bakkhnappurinn er valinn til að fara aftur á **verk- og upplýsingasíðuna**.
- Veljið blýantinn á **verk- og upplýsingasíðunni** til að fara á síðuna þar sem hægt er að færa innsláttinn inn handvirkt.
- Valin er myndavélin á **Verk- og upplýsingasíða** til að fara aftur á myndavélasíðuna.

Þegar myndavélahnappurinn er valinn á myndavélasíðunni mun hann sýnast deyfður á meðan reynt er að auðkenna strikamerki. Ef ekki er hægt að auðkenna strikamerki innan 5 sekúndna mun ferlið renna út á tíma og myndavélahnappurinn verður aftur tiltækur. Þá er aftur hægt að skanna strikamerki.

Þegar myndavél er beint að strikamerki skal staðsetja strikamerkið innan hornklofanna til að fá sem bestar niðurstöðu. Þegar tekst að skanna strikamerki er unnið úr niðurstöðunni og þér verður vísað yfir á næsta skref. Ef næsta skref inniheldur annað ílagssvæði með æskilegan ílagsham stilltan á skönnun mun myndavélasíðan ræsast á ný. Ef næsta skref er ekki skönnunarsvæði mun myndavélasíðan ekki ræsast.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]