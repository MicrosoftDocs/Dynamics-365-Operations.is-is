---
title: Gengi innflutningsgjaldmiðils
description: Þessi grein veitir upplýsingar um þær kröfur sem gerðar eru til innflutnings á erlendum viðmiðunargengi sem birtar eru af gengisfyrirtækjum.
author: EvgenyPopovMBS
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: kfend
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 27f9b06646d9ce948a6b4528c38c5df9784b24b2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894936"
---
# <a name="import-currency-exchange-rates"></a>Flytja inn gengi gjaldmiðla

[!include [banner](../includes/banner.md)]

Ef lögaðili hefur móttekið reikningur í erlendum gjaldmiðli verður að umreikna erlendan gjaldmiðil í staðbundinn gjaldmiðill. Þetta þýðir að nýjasta gengi mismunandi gjaldmiðla er áskilið. Þessi grein veitir yfirlit yfir þær stillingar og vinnslu sem þarf til að flytja inn erlenda gengisviðmiðunargengi sem birt eru af gengisveitendum, svo sem Seðlabanka Evrópu og Seðlabanka Rússlands.

Eftirfarandi kaflar lýsa flæði upplýsinga sem er notað til að setja upp og vinna úr innflutningi á gengi erlendrar myntar.

## <a name="configure-an-exchange-rate-provider"></a>Skilgreina gengisveitu
Áður en hægt er að flytja inn gengi þarf að setja upp upplýsingarnar sem eru áskildar af gengisveitunum. Notaðu síðuna **Skilgreina gengisveitur** page to til að velja gegnisveitu. Sumar gengisveitur fylgja með kynningargögnum í Dynamics 365 Finance. Eftirfarandi tafla lýsir stýringum í þessari síðu.

| Svæði | lýsing                   |
|-----------|-----------------------------------|
| **Heiti**  | Nafn gengisveitunnar.                                                                                                                                                                                     |
| **Lykill**   | Einkvæmt kennimerki fyrir hverjar skilgreiningarupplýsinganna sem nauðsynlegar eru fyrir veituna. Þessar upplýsingar er sjálfkrafa bætt fyrir hverja gengisveitu sem bætt er við. |
| **Value** | Upplýsingar fyrir hvern lykil. Þessar upplýsingum er bætt fyrir hverja gengisveitu sem bætt er við.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Flytja inn gengi gjaldmiðla
Þú getur flutt inn gengi gjaldmiðils úr uppruna gengisveita og bætt þeim við á síðunni **Gengi gjaldmiðils**. Notaðu síðuna **Flytja inn gengi gjaldmiðla** til að flytja inn gengi gjaldmiðla Eftirfarandi tafla inniheldur lýsingar á svæðunum sem eru áskilin til að ljúka við innflutningsferlið.

| Svæði | lýsing                   |
|-----------|-----------------------------------|
| **Gerð gengis**                 | Gerð gengis.                                                                                                                                                                                                                                                                                                                                                      |
| **Gengisveita**             | Gengisveita                                                                                                                                                                                                                                                                                                                                                  |
| **Innflutningur frá og með**                       | Þessi færibreyta stjórnar því hvort á að flytja inn frá og með deginum í dag eða miðað við tiltekið dagsetningabil. Ef ætlunin er að nota dagsetningabil, skal færa inn eða velja upphafs- og lokadagsetningar.                                                                                                                                                                                                                |
| **Stofna nauðsynleg gjaldmiðilspör**    | This gátreitur stjórnar sjálfvirk stofnun gjaldmiðilspara, ef gjaldmiðill para sem eru flutt inn er ekki til. Þessi valkostur er hugsanlega ekki í boði fyrir einhverjar veitur.                                                                                                                                                                                               |
| **Hnekkja fyrirliggjandi gengi**   | Þessi gátreitur stjórnar uppfærslu fyrirliggjandi gengis fyrir gjaldmiðilspar þegar gengi fyrir tiltekna dagsetningu er þegar til. Ef þessi gátreitur er ekki valinn verður gengi fyrir tilgreindar dagsetningar ekki flutt inn ef annað gengi er þegar til.                                                                                       |
| **Koma í veg fyrir innflutning á þjóðhátíðardegi** | Þessi gátreitur stjórnar innflutningi á gengi fyrir þjóðhátíðardag. Til dæmis, ef þú velur þennan gátreit og notar Seðlabanki Evrópu sem gengisveitur mun kerfið ekki uppfæra gengið á þjóðhátíðardegi sem tengist núverandi lögaðila. Þessi valkostur er hugsanlega ekki í boði fyrir einhverjar veitur. |
| **Gengi fyrri dags** | Þessi gátreitur er í boði ef þú virkjar hann í eiginleikanum **Innflutningur ECB á núverandi eða fyrri dagsetningu** á **Stjórnun eiginleika** síðu. Þessi gátreitur er aðeins í boði fyrir veituna, *Seðlabanki Evrópu*. Veljið þennan gátreit til að flytja inn gengi gjaldmiðils sem birt er af evrópska seðlabankanum á síðasta virka degi um kl. 16:00 CET. Sjálfgefið er að gátreiturinn sé valinn. Hreinsaðu þennan gátreit til að flytja inn gengi gjaldmiðilsins sem birt er á sama virkum degi.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]