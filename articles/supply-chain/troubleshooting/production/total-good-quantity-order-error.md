---
title: Villa um samtals gallalaust magn þegar reynt er að ljúka pöntun
description: Villa um samtals gallalaust magn kann að koma upp þegar reynt er að ljúka framleiðslupöntun og tilkynna hana lokna. Á þessari síðu er útskýrt hvers vegna og hvernig má laga vandamálið.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476650"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Villa um samtals gallalaust magn þegar reynt er að ljúka framleiðslupöntun

## <a name="symptoms"></a>Einkenni

Þegar reynt er að bóka skýrslu sem tilbúna færslubók í framleiðslupöntun birtast eftirfarandi villuboð:

> Samtals gallalaust magn, skráð tilbúið úr framleiðslunni, verður %1. Heildarsvörun síðustu aðgerðar er 0,00 alls.

## <a name="cause"></a>Orsök

Þetta vandamál á sér stað ef magnið sem var bókað í síðustu aðgerðum var rangt. Ef framleiðsla er til dæmis hafin, en magninu sem þarf að hefja er ekki úthlutað, verður færslubók leiðarspjalds bókuð án nokkurra lína. Til að staðfesta ástandið skal opna framleiðslupöntunina og síðan, á aðgerðasvæðinu á flipanum **Skoða** skal velja **Leiðarspjald**.

## <a name="resolution"></a>Lausn

Hægt er að lagfæra þetta með því að bóka viðbótarbækur fyrir aðgerðirnar sem bækurnar voru ekki rétt bókaðar fyrir. Endurræsið framleiðslupöntunina og veljið að bóka fleiri færslubækur. Þessi aðgerð mun ekki ræsa framleiðslupöntunina, en hún bókar færslubækurnar. Leiðarspjaldið ætti síðan að sýna magnið sem var bókað og það ætti að vera hægt að ljúka framleiðslupöntunum.
