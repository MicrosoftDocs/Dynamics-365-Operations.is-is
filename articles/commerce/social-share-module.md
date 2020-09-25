---
title: Samfélagsmiðlaeining
description: Þetta efnisatriði fjallar um samfélagsmiðlaeiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0fd81aa1f4b1358528f0135c1334dc7b4ac4461f
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761398"
---
# <a name="social-share-module"></a>Samfélagsmiðlaeining

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Þetta efnisatriði fjallar um samfélagsmiðlaeiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Samfélagsmiðlaeiningar gera notendum kleift að miðla vefslóðum rafrænna viðskipta á samfélagsmiðla á borð við Facebook, Twitter, Pinterest og LinkedIn. Einnig er hægt að samnýta vefslóðið vefsíðna með tölvupósti. Samfélagsmiðlaeiningar eru almennt notaðar á upplýsingasíðum vöru (PDPs) til að auðvelda notendum að miðla upplýsingum um vöru.

Hver samfélagsmiðlaeining er gámur fyrir einingar samfélagsmiðlaatriða. Hægt er að skilgreina hverja einingu þannig að hún beinist á tiltekna samfélagsmiðlasíðu. Samþætti við Facebook, Twitter, Pinterest, LinkedIn og tölvupóst er studd. Þegar vefsvæðisnotandi velur samfélagsmiðlatákn er HTML iframe opnað fyrir viðkomandi samfélagsmiðil. Innan iframe getur notandinn skráð sig inn og birt efni síðunnar sem hann var að skoða.

Sérhver verkvangur samfélagsmiðla kann að rekja kökur og því þurfa svæðanotendur að staðfesta samþykkisboð fyrir kökur. Þegar kökur eru ekki samþykktar er einingin falin á síðunni. Nánari upplýsingar eru í [Reglufylgni köku](cookie-compliance.md).

Eftirfarandi mynd sýnir dæmi um samfélagsmiðlaeiningu sem er notuð á upplýsingasíðu afurðar.

![Dæmi um samfélagsmiðlaeiningu](./media/ecommerce-socialshare.png)

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
1. Í hólfinu **Kaupgluggi (krafist)**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **Deila á samfélagsmiðlum** og síðan **Í lagi**.
1. Í hólfinu **Deila á samfélagsmiðlum**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **SocialShare** og síðan velja **Í lagi**.
1. Á eiginleikasvæðinu í **SocialShare** einingunni, undir **Stefna**, skal velja **Lárétt**. Bættu við myndatexta eins og nauðsynlegt er.
1. Í hólfinu **SocialShare**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.
1. Í glugganum **Bæta við einingu** skal velja eininguna **SocialShareItem** og síðan velja **Í lagi**.
1. Á eiginleikasvæði **SocialShareItem** einingarinnar, undir **Samfélagsmiðlar** skal velja **Facebook**.
1. Á eiginleikasvæði **SocialShareItem** einingarinnar, undir **Tákn** skal velja **+ Bæta við mynd**.
1. Í glugganum **Val á miðli** skal velja Facebook lógómynd og svo **Í lagi**. Ef engin Facebook-lógómynd er til staðar skal velja **Hlaða upp nýju margmiðlunaratriði** til að hlaða upp einni.
1. Bætið við og skilgreinið frekari **SocialShareItem** einingar eins og þörf er á.
1. Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna. Síðan sýnir samfélagsmiðlaeiningu.
1. Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit byrjendaeiningar](starter-kit-overview.md)

[Kaupgluggaeining](add-buy-box.md)

[Reglufylgni köku](cookie-compliance.md)
