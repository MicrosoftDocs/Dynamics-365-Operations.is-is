---
title: Eining kökusamþykkis
description: Þessi grein fjallar um samþykkiseiningar fyrir vafrakökur og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: 8ca4cc1ffcf8229589591dce6e4666b78bba3890
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276267"
---
# <a name="cookie-consent-module"></a>Eining kökusamþykkis

[!include [banner](includes/banner.md)]

Þessi grein fjallar um samþykkiseiningar fyrir vafrakökur og lýsir því hvernig á að bæta þeim við vefsíður í Microsoft Dynamics 365 Commerce.

Eining kökusamþykkis biður notendur vefsvæðis um að veita sérstaklega samþykki fyrir kökum fyrir alla eiginleika eða einingar sem rekja vafrakökur. Samþykki er nauðsynlegt í fyrsta skipti sem notandi skoðar svæði í nýrri vafralotu. Þegar samþykki er móttekið er það rakið og notandinn er ekki beðinn um samþykki aftur. Nánari upplýsingar eru í [Reglufylgni köku](cookie-compliance.md).

Ef samþykki fyrir kökum er ekki móttekið birtast eiginleikar eða einingar sem þurfa samþykki köku ekki á síðunni. Til dæmis krefst greiðslueining, samfélagsmiðlaeining og eiginleiki æskilegrar verslunar samþykkis köku og birtast ekki ef samþykki er ekki móttekið. 

Hægt er að stilla einingu fyrir kökusamþykki á hausbroti síðu til að hægt sé að framfylgja því þegar síðu er hlaðið. Samþykkiseining kökunnar á að vera með skýrum skilaboðum sem upplýsa notanda vefsvæðisins um notkun á kökunni á vefsvæðinu og ætti að veita tengil á persónuverndarsíðu svæðisins.

Eftirfarandi mynd sýnir dæmi um kökusamþykkisskilaboðum með tengli á persónuverndarstefnu svæðisins sem birtist á haus vefsvæðis.
![Dæmi um einingu fyrir kökusamþykki.](./media/ecommerce-cookieconsent.png)

## <a name="cookie-consent-module-properties"></a>Einingareiginleikar kökusamþykkis

| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Sniðinn texti                  | Sniðinn texti | Tilgreinir tilkynningu sniðins text til notenda síðunnar um að vefsvæðið notar vafrakökur og að notendur ættu að samþykkja fulla virkni fyrir notkun á kökum. |
| Tenglar | URL | Hægt er að bæta einum eða fleiri tenglum við persónuverndarsíðu svæðis sem lýsir þeim gerðum af kökum sem raktar eru á vefsvæðinu. |

## <a name="add-a-cookie-consent-module-to-site-pages"></a>Bæta við samþykkiseiningu fyrir köku á síður svæðis

Til að hægt sé að bæta samþykkiseiningu köku við margar svæðissíður má bæta henni við samnýtt brot síðuhauss. Eftir að hausbrotum er bætt við allar síður verður tilkynning um kökusamþykki sjálfkrafa birti í fyrsta skipti sem notandi sem er á svæðinu fer yfir á einhverja síðu.

Frekari upplýsingar um síðubrot og einingar má finna í [Hauseining](author-header-module.md).

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Eining síðuhauss](author-header-module.md) 

[Reglufylgni köku](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
