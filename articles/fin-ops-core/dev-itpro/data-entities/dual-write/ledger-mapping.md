---
title: Samþættur fjárhagur
description: Þessi grein lýsir samþættingu fjárhagsgagna milli fjármála og rekstrar og annarra Dynamics 365 forrita sem nota Dataverse.
author: tonyafehr
ms.date: 09/06/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: tfehr
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e5598295a25e31b33cd8b4d7ce3250a982ab4e87
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112241"
---
# <a name="integrated-ledger"></a>Samþættur fjárhagur

[!include [banner](../../includes/banner.md)]



Í viðskiptaforriti skilgreina fjárhagsgögn kjarna sem settur er upp fyrir hvernig fyrirtæki stundar viðskipti. Til dæmis lýsa fjárhagsupplýsingar fjárhagsárinu sem fyrirtækið fylgir, gjaldmiðlinum sem það stundar viðskipti í og reikninga sem það notar. Þessi grein lýsir samþættingu þessara helstu fjárhagsgagna.

## <a name="templates"></a>Sniðmát

Fjárhagsgögn innihalda safn af kjarnatöflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla     | lýsing
---------------------------------|----------------------------------|------------
[CDS-gengi](mapping-reference.md#123) | msdyn_currencyexchangerates |
[Bókhaldslykill](mapping-reference.md#121) | msdyn_chartofaccountses |
[Gjaldmiðlar](mapping-reference.md#218) | transactioncurrencies |
[Gjaldmiðlapar gengis](mapping-reference.md#122) | msdyn_currencyexchangeratepairs |
[Gerð gengis](mapping-reference.md#129) | msdyn_exchangeratetypes |
[Snið fjárhagsvíddar](mapping-reference.md#130) | msdyn_financialdimensionformats |
[Fjárhagsvíddir](mapping-reference.md#128) | msdyn_dimensionattributes |
[Samþættingareining fjárhagsdagatals](mapping-reference.md#132) | msdyn_fiscalcalendars |
[Tímabil fjárhagsdagatals](mapping-reference.md#131) | msdyn_fiscalcalendarperiods |
[Samþættingareining fjárhagsdagatalsárs](mapping-reference.md#133) | msdyn_fiscalcalendaryears |
[Ledger](mapping-reference.md#148) | msdyn_ledgers |
[Aðallykill](mapping-reference.md#152) | msdyn_mainaccounts |
[Tegundir aðallykils](mapping-reference.md#151) | msdyn_mainaccountcategories |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

