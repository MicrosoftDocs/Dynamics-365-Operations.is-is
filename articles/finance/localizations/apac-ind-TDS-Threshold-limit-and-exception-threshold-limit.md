---
title: Mörk og undantekningarmörk
description: Í þessu efnisatriði er mörkum og undantekningarmörkum lýst fyrir skatt sem dreginn er frá í upphafi (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7fa7d871fdf25f29b003a68cacd9fc0d487dce5b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726017"
---
# <a name="threshold-limit-and-exception-threshold-limit"></a>Mörk og undantekningarmörk

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er mörkum og undantekningarmörkum lýst fyrir skatt sem dreginn er frá í upphafi (TDS). TDS á reikningum og greiðslum er alltaf reiknað með hliðsjón af mörkum og undantekningarmörkum sem skilgreind eru fyrir TDS-skatthluta á síðunni **Staðgreiðsluskattshlutar**. TDS-skatthlutar eru hengdir við TDS-skattkóða sem eru innifaldir í TDS-skattflokkum. TDS-skattflokkar eru hengdir við lánardrottna og viðskiptavinir til að reikna út TDS á reikningsstigi eða greiðslustigi.

TDS er reiknað ef upphæð fyrir færslu eða uppsafnaðar færslur sem eru bókaðar með tilteknum TDS-flokki fyrir lánardrottin fer umfram mörkin sem tilgreind eru á síðunni **Staðgreiðsluskattshlutar**. TDS verður ekki reiknað fyrr en uppsöfnuð færsluupphæð fer umfram tiltekin mörk.

Ef undantekningarmörk eru tilgreind ásamt mörkunum fyrir TDS-hluta, þá er TDS reiknað þegar tiltekin færsluupphæð fyrir umfram undantekningarmörkin þótt uppsöfnuð færsluupphæð fer ekki umfram tiltekin mörk.

### <a name="example"></a>Dæmi
Skatthluti sem kallast TDS er settur upp og hengdur við TDS-skattflokk sem kallast verktaki. Mörkin hafa verið skilgreind sem 50.000 og undantekningarmörkin sem 20.000 fyrir TDS-skatthluta. TDS-flokkurinn verktaki er skilgreindur sem sjálfgefinn TDS-flokkur fyrir lánardrottin 1.

Innkaupareikningur 001 er bókaður fyrir lánardrottin 1 að upphæð 10000. TDS er ekki reiknað fyrir reikninginn vegna þess að upphæð reiknings hefur ekki farið yfir mörkin eða undantekningarmörkin. Innkaupareikningur 002 er bókaður fyrir lánardrottin 1 að upphæð 25.000. TDS er reiknað fyrir reikninginn vegna þess að upphæð reiknings hefur ekki farið yfir undantekningarmörkin. Innkaupareikningur 003 er bókaður fyrir lánardrottin 1 að upphæð 20.000. TDS er reiknað fyrir reikninginn vegna þess að heildarupphæð reikninganna þriggja sem gefnir eru út fyrir lánardrottin hefur farið yfir mörkin. TDS er reiknað fyrir alla reikninga sem gefnir eru út fyrir lánardrottin þar sem TDS hefur ekki verið reiknað áður. Þess vegna er TDS reiknað á 30.000 sem er heildarupphæð reiknings 001 og 003.

Mörkin og undantekningarmörkin eru ekki tekin til greina fyrir TDS-útreikninginn ef gátreiturinn **Horfa fram hjá mörkum** er valinn fyrir TDS-skattkóðana í TDS-flokknum sem er hengdur við færsluna. Mörkin verða ekki notuð í TDS-skattkóðunum í TDS-flokknum sem gátreiturinn **Horfa fram hjá mörkum** er fyrir.

Ef gátreiturinn **Horfa fram hjá mörkum** er valinn fyrir tiltekinn TDS-flokk fyrir suma reikninga, en ekki valinn fyrir aðra reikninga sem voru stofnaðir fyrir tiltekinn lánardrottin/viðskiptavin, gæti útreikningur á TDS án þess að líta fram hjá mörkunum fyrir nokkra reikninga átt sér stað með tilliti til uppsafnaðrar upphæðar á öllum reikningum þar sem TDS hefur ekki verið reiknað áður.

Þröskuldurinn er til dæmis 25000. Eftirfarandi reikningar eru stofnaðir fyrir lánardrottin A.

- Reikningur 1 - 20.000 - (Gátreiturinn **Horfa fram hjá mörkum** er ekki valinn): TDS er ekki reiknað.

- Reikningur 2 - 4.000 - (Gátreiturinn **Horfa fram hjá mörkum** er ekki valinn): TDS er reiknaður fyrir 4.000.

- Reikningur 2 - 3.000 - (Gátreiturinn **Horfa fram hjá mörkum** er ekki valinn): TDS er reiknað sem uppsöfnuð reikningsupphæð, þ.e. 27.000 (20000+4000+3000) fer yfir mörkin. TDS er reiknað fyrir uppsafnaða upphæð reikninga þar sem TDS hefur ekki verið reiknað áður, þ.e. 23.000 (20000+3000).
