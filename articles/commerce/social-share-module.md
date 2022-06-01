---
title: Samfélagsmiðlaeining
description: Þetta efnisatriði fjallar um samfélagsmiðlaeiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d145602a217b32b97142251c65d51945569be9ac
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780894"
---
# <a name="social-share-module"></a>Samfélagsmiðlaeining

[!include [banner](includes/banner.md)]

Þetta efnisatriði fjallar um samfélagsmiðlaeiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.

Samfélagsmiðlaeiningar gera notendum kleift að miðla vefslóðum rafrænna viðskipta á samfélagsmiðla á borð við Facebook, Twitter, Pinterest og LinkedIn. Einnig er hægt að samnýta vefslóðið vefsíðna með tölvupósti. Samfélagsmiðlaeiningar eru almennt notaðar á upplýsingasíðum vöru (PDPs) til að auðvelda notendum að miðla upplýsingum um vöru.

Hver samfélagsmiðlaeining er gámur fyrir einingar samfélagsmiðlaatriða. Hægt er að skilgreina hverja einingu þannig að hún beinist á tiltekna samfélagsmiðlasíðu. Samþætti við Facebook, Twitter, Pinterest, LinkedIn og tölvupóst er studd. Þegar vefsvæðisnotandi velur samfélagsmiðlatákn er HTML iframe opnað fyrir viðkomandi samfélagsmiðil. Innan iframe getur notandinn skráð sig inn og birt efni síðunnar sem hann var að skoða.

Sérhver verkvangur samfélagsmiðla kann að rekja kökur og því þurfa svæðanotendur að staðfesta samþykkisboð fyrir kökur. Þegar kökur eru ekki samþykktar er einingin falin á síðunni. Nánari upplýsingar eru í [Reglufylgni köku](cookie-compliance.md).

Eftirfarandi mynd sýnir dæmi um samfélagsmiðlaeiningu sem er notuð á upplýsingasíðu afurðar.

![Dæmi um samfélagsmiðlaeiningu.](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Eiginleikar samfélagsmiðlaeiningar

| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Myndatexti                  | Texti | Þessi eiginleiki tilgreinir fyrirsögn einingarinnar. |
| Stefna | **Lárétt** eða **Lóðrétt**  | Þessi eiginleiki skilgreinir útlitsátt fyrir atriði á samfélagsmiðlum. |

## <a name="social-share-item-module-properties"></a>Eiginleikaeiningar samfélagsmiðlaeiningar
| Nafn eiginleika             | Virði                 | lýsing |
|---------------------------|-----------------------|-------------|
| Netsamfélög              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail** | Fellivalmynd með lista yfir samfélagsmiðla. |
| Tákn |Mynd    | Þetta verður myndin sem birtist fyrir viðkomandi samfélagsmiðil. Bestu starfsvenju um notkun mynda fyrir verkvanga er að finna í SDK fyrir verkvang samfélagsmiðilsins. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Bæta samfélagsmiðlaeiningu við kaupgluggaeiningu

Til að bæta við samfélagsmiðlaeiningu við kaupgluggaeiningu skal fylgja þessum skrefum.

1. Á Fabrikam-svæðinu skal velja **Síður**, og síðan velja **DefaulPDP** síðuna til að opna upplýsingasíðu afurðar. 
1. Í **Kaupbox (krafist)** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **Samfélagsmiðlun** mát og veldu síðan **Allt í lagi**.
1. Í **Samfélagsmiðlun** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **SocialShare** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæðinu í **SocialShare** einingunni, undir **Stefna**, skal velja **Lárétt**. Bættu við myndatexta eins og nauðsynlegt er.
1. Í **SocialShare** rauf, veldu sporbaug (**...**), og veldu síðan **Bæta við einingu**.
1. Í **Veldu einingar** valmynd, veldu **SocialShareItem** mát og veldu síðan **Allt í lagi**.
1. Á eiginleikasvæði **SocialShareItem** einingarinnar, undir **Samfélagsmiðlar** skal velja **Facebook**.
1. Á eiginleikasvæði **SocialShareItem** einingarinnar, undir **Tákn** skal velja **+ Bæta við mynd**.
1. Í glugganum **Val á miðli** skal velja Facebook lógómynd og svo **Í lagi**. Ef engin Facebook-lógómynd er til staðar skal velja **Hlaða upp nýju margmiðlunaratriði** til að hlaða upp einni.
1. Bætið við og skilgreinið frekari **SocialShareItem** einingar eins og þörf er á.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Síðan sýnir samfélagsmiðlaeiningu.
1. Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit einingasafns](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Reglufylgni köku](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
