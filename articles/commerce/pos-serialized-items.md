---
title: Vinna með raðaðar vörur á sölustaðnum
description: Í þessu efnisatriði er útskýrt hvernig á að stjórna röðuðum vörum í forriti sölustaðar.
author: boycezhu
manager: annbe
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 6ba01abc3d1a4496ec586a621aa03b4981f84d76
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413272"
---
# <a name="work-with-serialized-items-in-the-pos"></a>Vinna með raðaðar vörur á sölustaðnum

[!include [banner](includes/banner.md)]

Margir smásalar selja vörur sem krefjast raðstjórnunar. Þessar vörur eru nefndar *raðaðar vörur*. Sumir smásalar gætu viljað viðhalda raðnúmerum í verslun eða vöruhúsabirgðum til rakningar. Aðrir smásalar gætu viljað sækja raðnúmer í söluferlinu vegna þjónustu og ábyrgðar. Í þessu efnisatriði er útskýrt hvernig þú getur stjórnað röðuðum vörum í Microsoft Dynamics 365 Commerce forriti sölustaðar.

## <a name="serial-number-configurations"></a>Skilgreiningar raðnúmers

Vara er talin röðuð vöru ef henni hefur verið úthlutað rakningarvíddarflokki sem er settur upp til að heimila raðnúmer. Í höfuðstöðvum Commerce, á síðunni **Rakningarvíddarflokkar**, skal velja valkostinn **Virkt** til að leyfa raðnúmer fyrir birgðaferli, eða velja **Virkt í söluferli** valkostinn til að leyfa raðnúmer fyrir söluferli.

Í flýtiflipanum **Rakningarvíddir**, skal kveikja á færibreytunni **Auð innhreyfing heimil** til að leyfa valkvæman innslátt raðnúmers við birgðamóttöku raðaðra vara. Ef slökkt er á þessari færibreytu þarf að slá inn raðnúmer. Á sama hátt stjórnar færibreytan **Auð úthreyfing heimil** því hvort raðnúmer er nauðsynlegt á meðan verið er að senda birgðir.

> [!NOTE]
> Til að nota **Birgðir á innleið** og **Birgðir á útleið** aðgerðir í sölustað til að skrá eða staðfesta raðnúmer gegn raðaðri vöru, verður þú að stilla vöruna þannig að henni sé úthlutað rakningarvíddarflokki sem eru uppsettur þannig að hann leyfi raðnúmer fyrir valkostinn **Virkt** og ekki valkostinn **Virkt í söluferli**.

## <a name="serial-number-management-page"></a>Stjórnunarsíða raðnúmers

Í **Birgðir á innleið** og **Birgðir á útleið** aðgerðir í sölustað, ef varan sem verið er að taka á móti, senda eða velja er vara með raðnúmer inniheldur **Upplýsingasvæðið** valkostinn **Stjórna raðnúmeri** sem tengist **Stjórnunarsíða raðnúmers** þar sem þú getur skráð eða staðfest raðnúmer fyrir vöruna. Að öðrum kosti er hægt að opna síðuna **Stjórnun raðnúmers** annaðhvort með því að velja **Raðnúmer** aðgerðina í forritastiku fyrir yfirlit pöntunarupplýsinga eða með því að velja **Stjórna raðnúmeri** valkostinn í svarglugganum sem birtist þér í móttöku- eða sendingarferlinu. 

Síðan **Stjórnun raðnúmers** sýnir allar opnar línur raðnúmers sem bíða skráningu eða staðfestingar. Það kunna að vera tveir flipar á þessari síðu: einn fyrir núverandi vöru og annar fyrir allar raðaðar vörur í pöntuninni.

Reiturinn **Staða** á síðunni **Stjórnun raðnúmers** veitir upplýsingar um núverandi stöðuna á hverju raðnúmeri fyrir sig í:

- **Ekki skráð** - Ekki hefur verið útvegað raðnúmeri eða forskráð raðnúmer hefur ekki verið staðfest (í móttökuferli).
- **Skráning** – Raðnúmerið hefur verið skráð og vistað staðbundið í gagnagrunnsrás verslunarinnar eða forskráð raðnúmer hefur verið staðfest. Aðeins raðnúmer með stöðuna **Skráning** verða send til höfuðstöðva Commerce þegar móttöku eða uppfyllingu lýkur.

## <a name="receive-serialized-items"></a>Móttaka á röðuðum vörum

Aðgerðin **Birgðir á innleið** í sölustað gerir notendum kleift að framkvæma eftirfarandi verk fyrir raðaðar vörur:

- Skrá raðnúmer á móti röðuðum vörum þegar þessar vörur eru mótteknar í versluninni í gegnum innkaupapöntun.
- Staðfesta forskráð raðnúmer á móti röðuðum vörum þegar þessar vörur eru mótteknar í versluninni í gegnum innkaupapöntun eða flutningspöntun.

### <a name="register-serial-numbers-against-serialized-items"></a>Skrá raðnúmer á móti röðuðum vörum

Fyrir innkaupapöntun birtist svargluggi með **Stjórna raðnúmeri** valkostinum meðan á móttökuferlinu stendur fyrir raðaða vöru. Hægt er að velja þann valkost til að opna síðuna **Stjórnun raðnúmers** og hefja skráningu raðnúmera. Einnig er hægt að sleppa þessu skrefi í móttökuferlinu og gefa upp innsláttinn seinna, áður en móttakan er bókuð.

Sjálfgefið er að flipinn fyrir núverandi vöru er sýndur. Allar raðnúmeralínur eru með autt raðnúmer og stöðuna **Ekki skráð**. Hægt er að gefa strikamerkjum raðnúmer eða velja **Raðnúmer** í forritastikunni til að halda áfram að slá inn raðnúmer. Raðnúmerin sem slegin eru inn birtast í listanum og staða þeirra breytist í **Skráir**. Hámarksfjöldi raðnúmera sem hægt er að skrá í listanum samsvarar móttökumagninu. Ef mistök eru gerð er hægt að velja **Breyta** eða **Hreinsa** á svæðinu **Upplýsingar** til að gera breytingar á raðnúmerunum sem voru slegin inn.

Einnig er hægt að skrá raðnúmer í flipanum **Allar raðaðar vörur** á síðunni **Stjórnun raðnúmers**. Veljið vöruna sem á að skráð raðnúmer fyrir af listanum.

### <a name="validate-serial-numbers-on-serialized-items"></a>Villuleita raðnúmer á númeruðum atriðum

Fyrir flutningspöntun verður að forskrá raðnúmer á röðuðum vörur fyrir hlutann sem er á útleið í sendingarferlinu. Fyrir innkaupapöntun gæti birginn útvegað upplýsingar um raðnúmer í gegnum ítarlega sendingartilkynningu og hægt er að forskrá númerin á vörunum sem verða send. Í báðum tilvikum eru raðnúmerin þekkt á undan móttökunni. Þess vegna þarf í hluta innleiðar aðeins að staðfesta að tekið hafi verið á móti því sem átti að taka á móti.

Til að staðfesta raðnúmer er hægt að opna síðuna **Stjórnun raðnúmers** annaðhvort í móttökuferlinu eða hvenær sem er áður en móttakan er bókuð. Fyrir hverja raðaða vöru sem er með forskráð raðnúmer eru öll raðnúmerin sjálfkrafa stillt á upphafsstöðuna **Ekki skráð** á þessari síðu. Til að staðfesta raðnúmer er hægt að skanna eða slá þau inn. Þar sem raðnúmer er slegin inn staðfestir forritið hvort þau samsvari forskráðum raðnúmerum. Ef þau stemma er stöðu þeirra breytt í **Skráir**. Annars færðu villuboð. Einnig er hægt að velja raðnúmer beint og velja svo valkostinn **Staðfesta raðnúmer** á **Upplýsingasvæði** til að merkja á fljótlegan hátt raðnúmerið sem staðfest. Hámarksfjöldi raðnúmera sem hægt er að staðfesta í listanum samsvarar móttökumagninu.

Einnig er hægt að staðfesta raðnúmer í flipanum **Allar raðaðar vörur** á síðunni **Stjórnun raðnúmers**. Veljið vöruna sem á að staðfesta raðnúmer fyrir af listanum.

## <a name="ship-serialized-items"></a>Senda raðaðar vörur

Hægt er að nota **Birgðir á útleið** aðgerð í sölustað til að skrá raðnúmer á móti vörum með raðnúmerum þegar þær eru fluttar úr núverandi verslun í gegnum flutningspöntun.

### <a name="register-serial-numbers-against-serialized-items"></a>Skrá raðnúmer á móti röðuðum vörum

Fyrir flutningspöntun birtist svargluggi með **Stjórna raðnúmeri** valkostinum meðan á sendingarferlinu stendur fyrir raðaða vöru. Hægt er að velja valkostinn til að opna síðuna **Stjórnun raðnúmers** og hefja skráningu raðnúmera. Einnig er hægt að sleppa þessu skrefi í sendingarferlinu og gefa upp innsláttinn seinna, áður en sendingin er bókuð.

Sjálfgefið er að flipinn fyrir núverandi vöru er sýndur. Allar raðnúmeralínur eru með autt raðnúmer og stöðuna **Ekki skráð**. Hægt er að gefa strikamerkjum raðnúmer eða velja **Raðnúmer** í forritastikunni til að halda áfram að slá inn raðnúmer. Raðnúmerin sem slegin eru inn birtast í listanum og staða þeirra breytist í **Skráir**. Hámarksfjöldi raðnúmera sem hægt er að skrá í listanum samsvarar sendingarmagninu. Ef mistök eru gerð er hægt að velja **Breyta** eða **Hreinsa** á svæðinu **Upplýsingar** til að gera breytingar á raðnúmerunum sem voru slegin inn.

Einnig er hægt að skrá raðnúmer í flipanum **Allar raðaðar vörur** á síðunni **Stjórnun raðnúmers**. Veljið vöruna sem á að skráð raðnúmer fyrir af listanum.

Einnig er hægt að virkja staðfestingu tiltækis raðnúmers við skráningu raðnúmers geng flutningspöntun á útleið. Með þessari staðfestingu, ef reynt er að senda raðnúmer sem er ekki í boði í birgðum sendingar birtast villuboð og gefa verður upp annað númer.

Til að virkja slíka staðfestingu þarf að áætla eftirfarandi verk til að keyra á endurteknum grunni:

- **Retail og Commerce** > **Upplýsingatækni Retail og Commerce** > **Vörur og birgðir** > **Afurðaframboð með rakningarvíddum**
- **Retail og Commerce** > **Dreifingaráætlanir** > **1130** (**Afurðarframboð**)

## <a name="additional-resources"></a>Frekari upplýsingar

[Birgðaaðgerð á innleið á sölustað](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation)

[Birgðaaðgerð á útleið á sölustað](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation)


[!INCLUDE[footer-include](../includes/footer-banner.md)]