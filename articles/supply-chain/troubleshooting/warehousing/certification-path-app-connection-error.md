---
title: Villa í slóð vottorðs þegar forritstenging er sett upp
description: Ef Warehouse Management-forritið sýnir villuna „Traustakkeri fyrir slóð vottorðs finnst ekki“ skaltu nota þessa síðu til að leysa úr eða finna leið framhjá vandamálinu.
author: ivanv-microsoft
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: WMA
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e4a36874ac4982c9c92a7dcc17c13c7c7c02bf8c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476663"
---
# <a name="trust-anchor-for-certification-path-not-found-when-setting-up-app-connection"></a>Traustakkeri fyrir slóð vottorðs finnst ekki þegar forritstenging er sett upp

## <a name="symptoms"></a>Einkenni

Þegar reynt er að tengjast við Supply Chain Management gæti Warehouse Management-forritið sýnt þér eftirfarandi villuboð:

> java.security.cert.certPathValidatorException: Traustakkeri fyrir slóð vottorðs finnst ekki.

Þetta vandamál getur haft áhrif á tæki með eftirfarandi eiginleikum:

- **Útgáfa stýrikerfis**: Android 4.4.x (t.d. Zebra TC55). Þetta er ekki vandamál í nýlegum útgáfum af Android.
- **Staðsetning Supply Chain Management**: Ský
- **Tengingarhamur**: Leynilykill biðlara eða vottorð

## <a name="possible-cause"></a>Möguleg orsök

Microsoft gæti hafa uppfært SSL-vottorð netþjóns sem Supply Chain Management notar. Þar af leiðandi gæti rótarvottorðið og/eða eitt af millivottorðunum hafa breyst þannig að nýja vottorðið er ekki á lista yfir örugg kerfisvottorð fyrir fartækið. Nýrri útgáfur af Android uppfæra sjálfkrafa listana yfir örugg vottorð en Android 4.4.x gerir það ekki.

## <a name="resolution"></a>Lausn

Til að leysa þetta vandamál þarf að gera eitt af eftirfarandi:

- Notaðu hjáleiðina sem er lýst í næsta hluta til að uppfæra hvert viðeigandi tæki.
- Það er *hugsanlega* hægt að hafa samband við Zebra eða Google til að fá uppfærslu á öruggum vottorðum vottorðaútgefenda kerfisins. Þetta höfum við hins vegar ekki staðfest.
- Ef mögulegt er skal íhuga að skipta út eldri tækjum fyrir tæki sem keyra nýlegri útgáfu af Android (þar sem örugg vottorð vottorðaútgefenda eru uppfærð sjálfkrafa).

### <a name="workaround"></a>Hjáleið

#### <a name="step-1-export-the-new-root-certificate-from-supply-chain-management"></a>Skref 1: Flytja út nýja rótarvottorðið úr Supply Chain Management

Sæktu nýja rótarvottorðið handvirkt með netvafranum með því að gera eftirfarandi:

1. Skráðu þig inn í Dynamics Supply Chain Management og opnaðu forsíðuna.

1. Á veffangastikunni í vafranum þínum skaltu velja lástáknið til að opna svargluggann **Staðsetning er örugg**.
1. Í svarglugganum skal velja **Vottorð (í gildi)** til að opna gluggann **Vottorð** fyrir það vottorð.
1. Opnaðu flipann **Slóð vottorðs** í glugganum **Vottorð**.
1. Veldu efsta vottorðið sem sýnt er í stigveldinu. (þetta er rótarskírteinið).
1. Opnaðu flipann **Upplýsingar** í glugganum **Vottorð**.
1. Veldu hnappinn **Afrita í skrá** neðst í flipanum **Upplýsingar**.
1. Leiðsagnarforrit fyrir **útflutning skírteinis** opnast. Veldu **Næst** til að halda áfram.
1. Síðan **Flytja út skráarsnið** opnast. Veldu „**DER encoded binary X.509“ (.CER)**. Veldu síðan **Næst** til að halda áfram.
1. Síðan **Skrár til að flytja út** opnast, tilgreindu skráarheiti og staðsetningu. Veldu síðan **Næst** til að halda áfram.
1. Síðan **Leiðsagnarforrit fyrir útflutning lokið** opnast, sem sýnir niðurstöðu útflutningsins. Veljið **Ljúka**.

#### <a name="step-2-install-the-downloaded-certificate-onto-the-affected-devices"></a>Skref 2: Setja upp sótt vottorð í tæki sem urðu fyrir áhrifum

Setja upp sótt vottorð með því að gera eftirfarandi:

1. Flyttu út vottorðið sem þú sóttir í skrefinu á undan í tækið sem þú vilt uppfæra. Til dæmis er hægt að nota SD-kort eða nettengingu til að gera skrána aðgengilega fyrir tækið þitt.
1. Opnaðu öryggisstillingarnar fyrir tækið þitt og veldu valmyndarvalkostinn til að setja upp vottorð úr skrá. (Nákvæm skref fyrir þetta eru mismunandi eftir tæki og útgáfu stýrikerfisins.)
1. Nú ætti nýja vottorðið að sjást í flipanum **Notandi** fyrir örugg vottorð.
1. Endurtaktu þetta ferli fyrir hvert tæki sem verður fyrir áhrifum.
