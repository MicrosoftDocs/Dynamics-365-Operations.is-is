---
title: Verið er að nota ferli vöruhúsakerfa
description: Þegar þú frátekur eða losar vinnu gætir þú fengið skilaboð um að verið sé að nota vöruhúsakerfisferli. Lagaðu vandamálið með einu af þessum skrefum.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bfda2fae824cdc64d722310d20cf16e6306d766c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476612"
---
# <a name="cant-reserve-or-release-work-because-processes-are-currently-being-used"></a>Ekki er hægt að taka frá eða losa verk vegna þess að ferli eru í notkun

## <a name="symptoms"></a>Einkenni

Eftirfarandi villuboð berst á meðan unnið er við afmarkaða framleiðslu:

> Verið er að nota ferli vöruhúsakerfa. Ef verklínur hafa ekki enn verið skráðar er hægt að hætta við stofnaða verkið og hvaða hleðslu- eða sendingarlínur sem er og halda svo áfram með tiltektar- eða sendingarferlið.

## <a name="cause"></a>Orsök

Þetta vandamál á sér stað ef reynt er að taka frá eða losa vinnu fyrir línu, en birgðafærslan er með stöðuna *Tínd*, sem gefur til kynna að búið sé að taka hana til.

## <a name="resolution"></a>Lausn

Fylgið einu af eftirfarandi skrefum til að laga þetta.

- Breytið stöðu framleiðslupöntunarinnar aftur í *Áætluð* eða *Losuð*.
- Opnar upplýsingasíða fyrir tengdu framleiðslupöntunina. Í aðgerðasvæði, á flipanum **Vöruhús**, í **Stöðva** skal velja **Stöðva og afturkalla tiltekt** til að afturkalla tiltekt allra færslna. Síðan skal velja **Fjarlægja stöðvun** til að vinna úr framleiðslupöntuninni.

Hér er útskýring á aðgerðunum *Afturkalla tiltekt* og *Stöðva*:
  
- **Afturkalla tiltekt** – Þessi aðgerð bakfærir stöðu birgðafærslna fyrir uppskriftalínur og formúlulínur sem hafa stöðuna úr *Tiltekið* til *Í pöntun*. Þegar vinnu við hráefnistínslu er lokið er staða línanna stillt á *Tekið til*. Þessi staða kemur í veg fyrir að framleiðslupöntunin sé endurstillt á stöðuna *Stofnað*. Í þessu tilvikum er hægt að nota aðgerðina *Afturkalla tiltekt* til að snúa færslunum aftur úr *Tekið til* stöðunni og endurstilla svo framleiðslupöntunina í stöðuna *Stofnað*.
- **Stöðva** – Þessi aðgerð setur flaggið **Stöðvað** á framleiðslupöntun til að koma í veg fyrir stöðuuppfærslu á pöntuninni. Hægt er að finna **Stöðvað** flaggið í flipanum **Vöruhús** á upplýsingasíðu framleiðslupöntunar.

> [!NOTE]
>
> - Hnapparnir eru aðeins sýnilegir þegar framleiðslupöntunin er stofnuð fyrir vörur sem eru virkar fyrir vöruhúsaferli.
> - **Stöðva** flokkurinn er aðeins sýnilegur á flipanum **Vöruhús** á aðgerðasvæði á upplýsingasíðu framleiðslupöntunar. Það er ekki sýnilegt á flipanum **Vöruhús** á listasíðunni **Framleiðslupantanir**.
