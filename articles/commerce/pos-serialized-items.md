---
title: Vinna með raðaðar vörur á sölustaðnum
description: Í þessu efnisatriði er útskýrt hvernig á að stjórna röðuðum vörum í forriti sölustaðar.
author: boycezhu
manager: annbe
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycezhu
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eedb64ae04345cb94bdd8cc68de833cfcfd40119
ms.sourcegitcommit: 39981582778b0a62567324452485a6721ca18284
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2020
ms.locfileid: "3407499"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Vinna með raðaðar vörur á sölustaðnum

[!include [banner](includes/banner.md)]

Margir smásalar selja vörur sem krefjast raðstjórnunar. Þessar vörur eru nefndar *raðaðar vörur*. Sumir smásalar gætu viljað viðhalda raðnúmerum til rakningar. Aðrir smásalar gætu viljað sækja raðnúmer í söluferlinu vegna þjónustu og ábyrgðar. Í þessu efnisatriði er útskýrt hvernig þú getur stjórnað röðuðum vörum í Microsoft Dynamics 365 Commerce forriti sölustaðar.

## <a name="serial-number-configurations"></a>Skilgreiningar raðnúmers

Vara er talin röðuð vöru ef henni hefur verið úthlutað rakningarvíddarflokki sem er settur upp til að heimila raðnúmer. Í höfuðstöðvum Commerce, á síðunni **Rakningarvíddarflokkar**, skal velja valkostinn **Virkt** til að leyfa raðnúmer fyrir birgðir. Til að virkja raðnúmer fyrir söluferlið skal velja valkostinn **Virkt í söluferli**.

Í flýtiflipanum **Rakningarvíddir**, ef kveikt er á valkostinum **Auð innhreyfing heimil**, er raðnúmerið valfrjáls innsláttur í ferli birgðamóttöku. Ef slökkt er á valkostinum þarf raðnúmerið að vera til staðar.

Í flýtiflipanum **Raðnúmer**, ef kveikt er á valkostinum **Stjórnun raðnúmera**, verður raðnúmerið að vera einkvæmt á hverja einingu. Tvítekin raðnúmer eru sem sagt ekki heimiluð.

## <a name="serialized-items-in-the-receiving-process"></a>Raðaðar vörur í móttökuferlinu

Aðgerðin **Birgðir á innleið** í forriti sölustaðar gerir notendum kleift að framkvæma eftirfarandi verk fyrir raðaðar vörur:

- Skrá raðnúmer á móti röðuðum vörum þegar þessar vörur eru mótteknar í versluninni í gegnum innkaupapöntun.
- Staðfesta forskráð raðnúmer á móti röðuðum vörum þegar þessar vörur eru mótteknar í versluninni í gegnum innkaupapöntun eða flutningspöntun.

> [!NOTE]
> Til að nota aðgerðina **Birgðir á innleið** til að skrá eða staðfesta raðaða vöru, verður vörunni að vera úthlutað rakningarvíddarflokki sem er settur upp til að leyfa raðnúmer fyrir valkostinn **Virkt**, ekki valkostinn **Virkt í söluferli**.

Til að hefja móttökuferlið, í aðgerðinni **Birgðir á innleið**, er hægt að byrja í yfirlitinu **Móttaka núna** með því að skanna strikamerki vörunnar eða slá inn auðkenni hennar. Að öðrum kosti er hægt að byrja í yfirlitinu **Ítarlegur pöntunarlisti** með því að velja vöruna handvirkt.

Ef varan sem er valin eða móttekin er röðuð vara, inniheldur glugginn **Upplýsingar** fyrir vöruna tengilinn **Stjórna raðnúmeri** sem opnar síðuna **Stjórnun raðnúmers**. Að öðrum kosti er hægt að opna síðuna **Stjórnun raðnúmers** annaðhvort með því að velja **Raðnúmer** í forritastiku fyrir yfirlit pöntunarupplýsinga eða með því að velja **Stjórna raðnúmeri** í svarglugganum sem birtist þér í móttökuferlinu. Síðan **Stjórnun raðnúmers** sýnir allar opnar línur raðnúmers sem bíða skráningu eða staðfestingar. Það kunna að vera tveir flipar á þessari síðu: einn fyrir núverandi vöru og einn fyrir allar raðaðar vörur í pöntuninni.

Reiturinn **Staða** á síðunni **Stjórnun raðnúmers** veitir upplýsingar um núverandi stöðuna á hverju raðnúmeri fyrir sig í:

- **Ekki skráð** - Ekki hefur verið útvegað raðnúmeri eða forskráð raðnúmer hefur ekki verið staðfest.
- **Skráning** – Raðnúmerið hefur verið skráð og vistað staðbundið í gagnagrunnsrás verslunarinnar eða forskráð raðnúmer hefur verið staðfest. Aðeins raðnúmer með stöðuna **Skráning** verða send til höfuðstöðva Commerce þegar móttöku lýkur.

### <a name="register-serial-numbers-against-serialized-items"></a>Skrá raðnúmer á móti röðuðum vörum

Fyrir innkaupapöntun býður svargluggi sem birtist þér í móttökuferli raðaðrar vöru valkostinn **Stjórna raðnúmeri**. Hægt er að velja þann valkost til að opna síðuna **Stjórnun raðnúmers** og hefja skráningu raðnúmera. Einnig er hægt að sleppa þessu skrefi í móttökuferlinu og gefa upp innsláttinn seinna, áður en móttakan er bókuð.

Sjálfgefið er að flipinn fyrir núverandi vöru er sýndur. Allar raðnúmeralínur eru með autt raðnúmer og stöðuna **Ekki skráð**. Hægt er að gefa strikamerkjum raðnúmer eða velja **Raðnúmer** í forritastikunni til að halda áfram að slá inn raðnúmer í svarglugganum. Raðnúmerin sem slegin eru inn birtast í listanum og staða á raðnúmeralínum breytist í **Skráir**. Hámarksfjöldi raðnúmera sem hægt er að skrá í listanum samsvarar móttökumagninu. Ef mistök eru gerð er hægt að velja **Breyta** eða **Hreinsa** á svæðinu **Upplýsingar** til að gera breytingar á raðnúmerunum sem voru slegin inn.

Einnig er hægt að skrá raðnúmer í flipanum **Allar raðaðar vörur** á síðunni **Stjórnun raðnúmers**. Veljið vöruna sem á að skráð raðnúmer fyrir af listanum.

Við skráningu raðnúmers á þessari síðu á sér stað staðfesting á tvítekningu. Ef reynt er að slá inn tvítekið raðnúmer á móti vöru þar sem kveikt er á stjórnun raðnúmers kemur upp villa og gefa verður upp annað númer.

### <a name="validate-serial-numbers-on-serialized-items"></a>Villuleita raðnúmer á númeruðum atriðum

Fyrir flutningspöntun verður að forskrá raðnúmer á röðuðum vörur fyrir hlutann sem er á útleið í sendingarferlinu. Fyrir innkaupapöntun gæti birginn útvegað upplýsingar um raðnúmer í gegnum ítarlega sendingartilkynningu og hægt er að forskrá númerin á vörunum sem verða send. Í báðum tilvikum eru raðnúmerin þekkt á undan móttökunni. Þess vegna þarf í hluta innleiðar aðeins að staðfesta að tekið hafi verið á móti því sem átti að taka á móti.

Til að staðfesta raðnúmer er hægt að opna síðuna **Stjórnun raðnúmers** annaðhvort í móttökuferlinu eða hvenær sem er áður en móttakan er bókuð. Fyrir hverja raðaða vöru sem er með forskráð raðnúmer eru öll raðnúmerin sjálfkrafa stillt á upphafsstöðuna **Ekki skráð** á þessari síðu. Til að staðfesta raðnúmer er hægt að skanna eða slá þau inn. Þar sem raðnúmer er slegin inn staðfestir forritið hvort þau samsvari forskráðum raðnúmerum. Ef þau stemma er stöðu þeirra breytt í **Skráir**. Annars færðu villuboð. Hámarksfjöldi raðnúmera sem hægt er að staðfesta í listanum samsvarar móttökumagninu.

Einnig er hægt að staðfesta raðnúmer í flipanum **Allar raðaðar vörur** á síðunni **Stjórnun raðnúmers**. Veljið vöruna sem á að staðfesta raðnúmer fyrir af listanum.

## <a name="additional-resources"></a>Frekari upplýsingar

[Birgðaaðgerð á innleið á sölustað](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)
