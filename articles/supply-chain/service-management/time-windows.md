---
title: Tímaskjámyndir
description: Hægt er að nota tímaglugga til að bæta röðun á þjónustupöntunarlínum.
author: ShylaThompson
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATimeAgreement
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 29c43d5c21d435086bcc272e89b4c877f4057a44374e4d0005a842e10fe43a88
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741238"
---
# <a name="time-windows"></a>Tímaskjámyndir  

[!include [banner](../includes/banner.md)]

Hægt er að nota tímaglugga til að bæta röðun á þjónustupöntunarlínum. Hægt er að setja upp kerfið þannig að það stofni þjónustupantanir sjálfkrafa. Byggt á skilyrðinu sem er tilgreint með tímaglugga er hægt að tengja eins margar þjónustupöntunarlínur og mögulegt er og niður í eins fáar þjónustupantanir og mögulegt er.

Tímagluggar tilgreina hversu langt þjónustupöntunarlína getur færst til frá útreiknaðri dagsetningu. Útreiknaða dagsetningin er sú dagsetning þegar þjónustupöntunarlínan var látin eiga sér stað. Dagsetningin byggist á bilstillingunni og þjónustutímabilinu sem var skilgreint á síðunni **Þjónustupantanir**. Tímagluggi er skilgreindur með því að nota gildin í eftirfarandi töflu.

| Aðferð | lýsing                                                                                                                                                                                                                                                                                           |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vika   | Hægt er að færa þjónustupöntunarlínuna yfir á hvaða opinn dag í sömu vikunni og upprunalega útreiknaða dagsetningin.                                                                                                                                                                                    |
| Mánuður  | Hægt er að færa þjónustupöntunarlínuna yfir á hvaða opinn dag í sama mánuðinum og upprunalega útreiknaða dagsetningin. Útreiknuð dagsetning þjónustupöntunarlínu er til dæmis 15. febrúar, 2017. Hægt er að raða þjónustupöntunarlínu á hvaða vikudag milli 1. febrúar og 28. febrúar, 2017. |
| Beinskiptur | Hámarksfjöldi daga fyrir og eftir upprunalegu útreiknuðu dagsetninguna þar sem hægt er að færa þjónustupöntunarlínuna er skilgreint.                                                                                                                                                                           |

Ef tímagluggi er ekki tilgreindur fyrir þjónustupöntunarlínu þarf þjónustupöntunarlínan sem er afleidd af þjónustusamningnum að vera á nákvæmlega sömu dagsetningu og hún var upprunalega áætluð á.

## <a name="related-topics"></a>Tengd efnisatriði

[Stofna tímaskjámyndir](create-time-windows.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]