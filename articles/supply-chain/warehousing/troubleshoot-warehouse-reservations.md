---
title: Úrræðaleit fyrir frátekningar í vöruhúsastjórnun
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsafrátektir í Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a9a5d20732a802fc58c392853af8334bbc07de73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248716"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a>Úrræðaleit fyrir frátekningar í vöruhúsastjórnun

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsafrátektir í Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a>Ég fæ eftirfarandi villuboð: „Ekki er hægt að fjarlægja frátekningar vegna þess að búið er að stofna vinnu sem byggir á frátekningunum.“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ekki er hægt að taka frá birgðir á sölulínu, þar sem það er opin vinna á móti línunni.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Kanna hvort opin pökkunarhópvinna er til staðar til að koma vörunni úr pökkunarstöð á aðra staðsetningu (t.d. *útskot*). Farið yfir færslurnar í **Ferilannál vinnustofnunar** og **Upplýsingar um verk** til að ákvarða hvað er efnislega verið að taka frá í birgðum og ljúka því eða eyða vinnu til að losa frátektina.

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a>Ég fæ eftirfarandi villuboð: „Ekki var hægt að uppfæra birgðamagnið %1 vegna þess að ekki voru nógu margar birgðafærslur fyrir vöruna %2...“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál getur komið upp ef kerfið getur ekki að uppfært birgðamagn vegna þess að það eru ekki nægar birgðafærslur sem eru með tilgreindar stærðir. Hér er allur texti villuskilaboða:

> Ekki var hægt að uppfæra birgðamagnið -%1 vegna þess að ekki voru nógu margar birgðafærslur fyrir vöruna %2 með málin Stærð=%3, Litur=%4, Viðbætur=%5, Staður=%6, Vöruhús=%7, Staðsetning=%8, Birgðastaða=Tiltækar, Leyfisplata=%9, Lotunúmer=%10 tilvísunarauðkenni %11 á lotukenni %12.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Ganga skal úr skugga um að engar birgðafærslur séu efnislega í frátekt á móti magninu. Til dæmis gætu þessar færslur opnað gæðapantanir, birgðalokunarfærslur eða úttakspantanir.

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a>Ég fæ eftirfarandi villuboð: „Efnislega á lager... Ekki er hægt að taka frá vegna þess að aðeins 0,00 eru tiltæk í birgðum.“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þetta vandamál getur komið upp ef kerfið getur ekki að uppfært birgðamagn vegna þess að það eru ekki nægar birgðafærslur sem eru með tilgreindar stærðir. Hér er allur texti villuskilaboða:

> Efnislegt lagersvæði =%1, Vöruhús=%2, Birgðastaða =Tiltækt, Rununúmer=%3, Eigandi=%4: %5 er ekki hægt að taka frá vegna þess að aðeins 0,00 eru tiltæk í birgðum.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þetta vandamál stafar líklega af opinni vinnu. Annaðhvort skal ljúka vinnu eða taka við án þess að stofna vinnu. Ganga skal úr skugga um að engar birgðafærslur séu efnislega í frátekt á móti magninu. Til dæmis gætu þessar færslur verið opnar gæðapantanir, birgðalokunarfærslur eða úttakspantanir.

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a>Ég fæ eftirfarandi villuboð: „Til að úthluta bylgju verða hleðslulínur að tilgreina víddirnar fyrir ofan staðsetninguna. Til að úthluta þessum víddum skal taka hleðslulínuna frá og endurgera hana.“

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þegar vara með "runu fyrir ofan" frátekningarstigveldi er notuð (með **rununúmeri** vídd sem er sett *fyrir ofan* vídd **staðsetningar**) mun skipunin **Losa í vöruhús** á síðunni **Áætlunarvinnusvæði** fyrir hlutamagn ekki virka. Þessi villuskilaboð berast og engin vinna er stofnuð fyrir hlutamagnið.

Hins vegar, ef notuð er vara sem inniheldur "runu fyrir neðan" frátekningarstigveldi (með **Rununúmer** vídd sem er sett fyrir *neðan* vídd **Staðsetning**), er hægt að losa úr síðunni **Áætlunarvinnusvæði** fyrir hlutamagn.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni. Ef vídd fyrir ofan víddina **Staðsetning** er sett upp í frátekningarstigveldi verður að tilgreina hana áður en hún er losuð í vöruhúsið. Microsoft hefur metið þetta vandamál og hefur ákvarðað að takmörkun á eiginleika við losanir í vöruhúsi frá áætlunarvinnusvæði hleðsluáætlunar sé til staðar. Ekki er hægt að losa hlutamagn ef ein eða fleiri vídd fyrir ofan **Staðsetning** eru ekki tilgreindar.

Frekari upplýsingar er að finna í [Sveigjanleg frátektarregla á vídd vöruhúsastigs](flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]