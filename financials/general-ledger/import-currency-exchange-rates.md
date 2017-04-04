---
title: "Gengi innflutningsgjaldmiðils"
description: "Lögaðili hefur tekið á móti reikningum í erlendum gjaldmiðlum, er nauðsynlegt til að umbreyta í erlendum gjaldmiðli í gjaldmiðli landsins. Þetta þýðir að stöðugt gengi fyrir mismunandi gjaldmiðlar eru áskilin. Þetta efnisatriði gefur yfirlit yfir stillingar sem þarf og vinnslu fyrir innflutning erlendir tilvísun gengi birt í gegnum netið með þær gengisveitur, eins og Evrópska Seðlabanka og Seðlabanka Rússland."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ExchangeRateProviderConfiguration
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261374
ms.assetid: b2b22868-de68-439f-914c-78c6930b7340
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: bf66a1b1c9314b454223274810a21913d54b702d
ms.lasthandoff: 03/31/2017


---

# <a name="import-currency-exchange-rates"></a>Gengi innflutningsgjaldmiðils

Lögaðili hefur tekið á móti reikningum í erlendum gjaldmiðlum, er nauðsynlegt til að umbreyta í erlendum gjaldmiðli í gjaldmiðli landsins. Þetta þýðir að stöðugt gengi fyrir mismunandi gjaldmiðlar eru áskilin. Þetta efnisatriði gefur yfirlit yfir stillingar sem þarf og vinnslu fyrir innflutning erlendir tilvísun gengi birt í gegnum netið með þær gengisveitur, eins og Evrópska Seðlabanka og Seðlabanka Rússland.

Eftirfarandi kaflar lýsa flæði upplýsingar sem er notað fyrir uppsetningu og vinnslu á innflutningi erlendir gengi.

## <a name="configure-an-exchange-rate-provider"></a>Skilgreina gerð gengisveitu
Áður en hægt er að flytja inn gengi gjaldmiðla, verður að setja upp upplýsingarnar sem er krafist af veitur sem bjóða gengi. Nota skal **Skilgreina gengisveitur** síðu til að velja þær gengisveitur. Sumar gengisveitur fylgja með sýnigögn í Microsoft Dynamics 365 fyrir Aðgerðir. Eftirfarandi tafla lýsir stýringum í þessari síðu.

|           |                                                                                                                                                                                                                             |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field** | **Description**                                                                                                                                                                                                             |
| **Name**  | Nafn gengisveitunnar.                                                                                                                                                                                     |
| **Lykill**   | Einkvæmt kennimerki fyrir hverjar skilgreiningarupplýsinganna sem nauðsynlegar eru fyrir veituna. Þessar upplýsingar sjálfkrafa bætt við hverja gengisveitu sem er bætt við þegar smellt er á **Bæta** hnappinn. |
| **Value** | Upplýsingar fyrir hvern lykil. Þessum upplýsingum er bætt við fyrir hverja gengisveitu sem er bætt við þegar smellt er á **Bæta** hnappinn.                                                                                         |

## <a name="import-currency-exchange-rates"></a>Gengi innflutningsgjaldmiðils
Hægt er að flytja inn gengi úr gengi veitur uppruna og setja þær upp á **gengi gjaldmiðla** síðu. Nota skal **gengi Innflutningsgjaldmiðils** síðu til að flytja inn gengi gjaldmiðla. Eftirfarandi tafla lýsir svæðum sem þarf að ljúka innflutningurinn tókst.

|                                        |                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Field**                              | **Description**                                                                                                                                                                                                                                                                                                                                                             |
| **Exchange rate type**                 | Gerð gengis.                                                                                                                                                                                                                                                                                                                                                      |
| **Exchange rate provider**             | Gerð gengisveitu.                                                                                                                                                                                                                                                                                                                                                  |
| **Import as of**                       | Þessi færibreyta stjórnar hvort á að flytja inn frá og með deginum í dag eða fyrir tímabil. Ef óskað er að nota tímabil skal færa inn eða veljið upphafs- og lokadagsetningar.                                                                                                                                                                                                                |
| **Create necessary currency pairs**    | Þessi gátreitur er valinn vinnur með sjálfvirka stofnun gjaldmiðilspör, ef gjaldmiðilspör sem eru flutt inn er ekki til. Þessi valkostur gætu verið tiltækar fyrir sumar veitur.                                                                                                                                                                                               |
| **Override existing exchange rates**   | Þessi gátreitur er valinn stjórnar uppfærslu á fyrirliggjandi gengi fyrir gjaldmiðilspör þegar gengi fyrir ákveðna dagsetningu er þegar til. Ef þessi gátreitur er ekki valinn gengi fyrir tilteknar dagsetningar er ekki flutt inn ef annað gengi er þegar til.                                                                                       |
| **Prevent import on national holiday** | Þessi gátreitur er valinn vinnur innflutning gengi fyrir dagsetningu sem er almennur frídagur. Til dæmis ef gátreiturinn er valinn og nota Evrópska Seðlabanka sem gengisveitan er kerfið mun ekki uppfæra gengi á frídagurinn sem er tengdur núverandi lögaðila. Þessi valkostur gætu verið tiltækar fyrir sumar veitur. |




