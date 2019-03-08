---
title: Gengi innflutningsgjaldmiðils
description: Ef lögaðili hefur móttekið reikningur í erlendum gjaldmiðli er nauðsynlegt að umreikna erlendan gjaldmiðil í staðbundinn gjaldmiðill. Þetta þýðir að nýjasta gengi mismunandi gjaldmiðla er áskilið. Þetta umfjöllunarefni veitir yfirlit yfir áskilið stillingar og ferli fyrir innflutningur tilvísana í gengi erlendra gjaldmiðla sem birt er á netinu af gengisveitum, svo sem Seðlabanki Evrópu og og Seðlabanki Rússlands.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: edd72b48a640126577dd7a2add3a4891ae505fdf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "333393"
---
# <a name="import-currency-exchange-rates"></a>Gengi innflutningsgjaldmiðils

[!include [banner](../includes/banner.md)]

Ef lögaðili hefur móttekið reikningur í erlendum gjaldmiðli er nauðsynlegt að umreikna erlendan gjaldmiðil í staðbundinn gjaldmiðill. Þetta þýðir að nýjasta gengi mismunandi gjaldmiðla er áskilið. Þetta umfjöllunarefni veitir yfirlit yfir áskilið stillingar og ferli fyrir innflutningur tilvísana í gengi erlendra gjaldmiðla sem birt er á netinu af gengisveitum, svo sem Seðlabanki Evrópu og og Seðlabanki Rússlands.

Eftirfarandi kaflar lýsa flæði upplýsinga sem er notað til að setja upp og vinna úr innflutningi á gengi erlendrar myntar.

## <a name="configure-an-exchange-rate-provider"></a>Skilgreina gengisveitu
Áður en hægt er að flytja inn gengi þarf að setja upp upplýsingarnar sem eru áskildar af gengisveitunum. Notaðu síðuna **Skilgreina gengisveitur** page to til að velja gegnisveitu. Sumar gengisveitur eru hluti af sýnigögnum í Microsoft Dynamics 365 for Finance and Operations. Eftirfarandi tafla lýsir stýringum í þessari síðu.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Svæði** | **Lýsing**                                                                                                                                                                                                             |
| **Heiti**  | Nafn gengisveitunnar.                                                                                                                                                                                     |
| **Lykill**   | Einkvæmt kennimerki fyrir hverjar skilgreiningarupplýsinganna sem nauðsynlegar eru fyrir veituna. Þessar upplýsingar er sjálfvirkt bæta við fyrir hverja gengisveitu sem er bætt við þegar smellt er á hnappinn **Bæta við**. |
| **Gildi** | Upplýsingar fyrir hvern lykil. Þessar upplýsingar er sjálfvirkt bæta við fyrir hverja gengisveitu sem er bætt við þegar smellt er á hnappinn **Bæta við**.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Gengi innflutningsgjaldmiðils
Þú getur flutt inn gengi gjaldmiðils úr uppruna gengisveita og sett það upp á síðunni **Gengi gjaldmiðils**. Notaðu síðuna **Flytja inn gengi gjaldmiðla** til að flytja inn gengi gjaldmiðla Eftirfarandi tafla inniheldur lýsingar á svæðunum sem eru áskilin til að ljúka við innflutningsferlið.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Svæði**                              | **Lýsing**                                                                                                                                                                                                                                                                                                                                                             |
| **Gerð gengis**                 | Gerð gengis.                                                                                                                                                                                                                                                                                                                                                      |
| **Gengisveita**             | Gengisveita                                                                                                                                                                                                                                                                                                                                                  |
| **Innflutningur frá og með**                       | Þessi færibreyta stjórnar því hvort á að flytja inn frá og með deginum í dag eða miðað við dagsetningabil. Ef ætlunin er að nota dagsetningabil, skal færa inn eða velja upphafs- og lokadagsetningar.                                                                                                                                                                                                                |
| **Stofna nauðsynleg gjaldmiðilspör**    | This gátreitur stjórnar sjálfvirk stofnun gjaldmiðilspara, ef gjaldmiðill para sem eru flutt inn er ekki til. Þessi valkostur er hugsanlega ekki í boði fyrir einhverjar veitur.                                                                                                                                                                                               |
| **Hnekkja fyrirliggjandi gengi**   | Þessi gátreitur stjórnar uppfærslu fyrirliggjandi gengis fyrir gjaldmiðilspar þegar gengi fyrir tiltekna dagsetningu er þegar til. Ef þessi gátreitur er ekki valinn verður gengi fyrir tilgreindar dagsetningar ekki flutt inn ef annað gengi er þegar til.                                                                                       |
| **Koma í veg fyrir innflutning á þjóðhátíðardegi** | Þessi gátreitur stjórnar innflutningi á gengi fyrir dagsetningu sem er þjóðhátíðardagur. Til dæmis, ef þú velur þennan gátreit og notar Seðlabanki Evrópu sem gengisveitur mun kerfið ekki uppfæra gengið á þjóðhátíðardegi sem tengist núverandi lögaðila. Þessi valkostur er hugsanlega ekki í boði fyrir einhverjar veitur. |





