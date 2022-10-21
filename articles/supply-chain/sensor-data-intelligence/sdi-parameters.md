---
title: Færibreytur Sensor Data Intelligence
description: Þessi grein veitir upplýsingar um stillingar sem eru tiltækar á færibreytum Sensor Data Intelligence síðu.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: IoTIntCoreServiceParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 5240537e3a6526ceb35253b9e68f46b1753c6a37
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689374"
---
# <a name="sensor-data-intelligence-parameters"></a>Færibreytur Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

The **Sensor Data Intelligence færibreytur** síða veitir nokkrar stillingar sem þú getur notað til að stilla eiginleikann. Þessar stillingar innihalda Azure-tengingarfæribreytur og færibreytu fyrir líftíma viðvörunarskilaboða sem eru send til notenda sem svar við skynjaramælingum.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Lestu og breyttu tengingarupplýsingum fyrir Azure IoT lausnina þína

Venjulega muntu setja upp Azure IoT lausnina þína og tengja hana við Microsoft Dynamics 365 Supply Chain Management frá **Settu upp og tengdu Azure auðlindir** síðu, sem mun leiða þig í gegnum báðar aðferðir. (Fyrir frekari upplýsingar, sjá [Settu upp IoT lausn á Azure](sdi-deploy-iot-solution-on-azure.md) .) Þú getur líka skoðað og breytt tengingarupplýsingunum hvenær sem er í Supply Chain Management með því að fylgja þessum skrefum.

1. Fara til **Kerfisstjórnun \> Uppsetning \> Sensor Data Intelligence \> Sensor Data Intelligence færibreytur**.
1. Á **Tímaröð** flipa, í **Redis metraverslun tengistrengur** reit, sláðu inn **Aðaltengingarstrengur (StackExchange.Redis)** gildi fyrir Azure IoT lausnina sem þú vilt tengjast. Fyrir frekari upplýsingar um hvernig á að finna þetta gildi, sjá [Settu upp IoT lausn á Azure](sdi-deploy-iot-solution-on-azure.md).
1. Á **Samþættingar** flipa, í **Azure AD auðkenni forrits viðskiptavinar** reit, sláðu inn **Auðkenni viðskiptavinar** gildi fyrir Azure IoT lausnina sem þú vilt tengjast. Fyrir frekari upplýsingar um hvernig á að finna þetta gildi, sjá [Settu upp IoT lausn á Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Stilltu endingartíma viðvörunarskilaboða

Í hvert sinn sem Sensor Data Intelligence greinir aðstæður sem krefjast athygli notenda sendir það tilkynningu til viðkomandi notanda. Til að koma í veg fyrir að þessar tilkynningar safnist upp í kerfinu ættirðu að stilla þær þannig að þær renna út eftir nokkra daga.

1. Fara til **Kerfisstjórnun \> Uppsetning \> Sensor Data Intelligence \> Sensor Data Intelligence færibreytur**.
1. Á **Tilkynningar** flipa, í **Tilkynningardagar eftir að lifa** reit, sláðu inn fjölda daga til að geyma tilkynningu. Eftir að tilgreindur tími er liðinn verður tilkynningunni eytt.
