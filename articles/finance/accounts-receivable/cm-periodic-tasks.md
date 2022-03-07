---
title: Regluleg verk kreditstjórnunar
description: Þetta efni lýsir reglubundnum verkefnum sem eru nauðsynlegur hluti af ferlinu við að stjórna lánamörkum fyrir viðskiptavini.
author: mikefalkner
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5e5d1ad7b0b151d67bd96513e9ce0c82c172a601
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835293"
---
# <a name="periodic-credit-management-tasks"></a>Reglubundin verk lánastýringar

[!include [banner](../includes/banner.md)]

Þetta efni lýsir reglubundnum verkefnum sem eru nauðsynlegur hluti af ferlinu við að stjórna lánamörkum fyrir viðskiptavini.

## <a name="update-risk-scores"></a>Uppfæra áhættueinkunnir

Þegar fyrirtæki þróast og aðstæður breytast getur útlánaáhætta tiltekins viðskiptavinar einnig breyst. Til að hjálpa við að viðhalda viðeigandi lánamörkum fyrir viðskiptavini þína, verður þú að fara reglulega yfir viðmið fyrir hvert áhættustig og uppfæra skora fyrir hvern viðskiptavin. Þú getur uppfært eftirfarandi stig með því að nota síðuna **Uppfæra áhættumat** (**Skuldir og innheimta \> Reglubundin verk \> Lánastjórnun \> Uppfæra áhættumat**). Allir notendaskilgreindir útreikningar eru einnig unnir.

- **Meðalgreiðsludagar** - Þetta stig er meðalfjöldi daga sem viðskiptavinur tekur til að greiða reikninga.
- **Viðskiptavinur síðan** - Þetta stig er fjöldi ára sem viðskiptavinur hefur verið viðskiptavinur fyrirtækisins.
- **Í viðskiptum síðan** - Þetta stig er fjöldi ára sem viðskiptavinur hefur verið í viðskiptum. Það notar gildið í reitnum **Upphaf viðskipta** á síðunni **Viðskiptavinir**.
- **Dagasala framúrskarandi** - Þessi skora er byggð á viðskiptakröfu, sölutekjum og fjölda daga fyrir 12 mánaða tímabilið á undan.
- **Meðaljafnvægi** - Einkunnin er byggð á viðskiptakröfu fyrir 12 mánaða tímabil.
- **Lánastjórnunarhópur**, **Staða reiknings** og **Land** - Þessar stigatölur nota upplýsingar frá viðskiptavininum.

## <a name="update-customer-balance-statistics"></a>Uppfæra tölfræði um stöður viðskiptavina

Þú getur keyrt ferlið **Uppfæra tölfræði um stöður viðskiptavina** til að uppfæra útreikning á tölfræði um jafnvægi sem sést á síðunni **Fyrirspurn um stöðutölur**. Þessar upplýsingar eru notaðar til að reikna út áhættustig og gildi sem sýnd eru í útlánatölfræði upplýsingareita á síðunni **Viðskiptavinur**.

Þegar þú keyrir ferlið uppfærir það tölfræði um jafnvægi viðskiptavina fyrir einn viðskiptavin. Til að setja upp hópvinnu til að keyra ferlið fyrir marga viðskiptavini er hægt að nota síðuna **Reikna stöðutölur** (**Lánastjórnun \> Reglubundin verk \> Reikna stöðutölur**).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]