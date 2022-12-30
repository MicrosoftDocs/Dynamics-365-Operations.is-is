---
title: Færibreytur Sensor Data Intelligence
description: Þessi grein veitir upplýsingar um skilgreiningarstillingar sem eru í boði á færibreytusíðu Sensor Data Intelligence.
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
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689374"
---
# <a name="sensor-data-intelligence-parameters"></a>Færibreytur Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Síðan **Færibreytur Sensor Data Intelligence** býður upp á nokkrar stillingar sem þú getur notað til að skilgreina eiginleikann. Þessar stillingar innihalda færibreytur Azure-tengingar og færibreytu fyrir líftíma á viðvörunarboðum sem eru send til notenda vegna skynjaramælinga.

## <a name="read-and-change-connection-details-for-your-azure-iot-solution"></a>Lesa og breyta tengingarupplýsingum fyrir Azure IoT lausnina þína

Yfirleitt er Azure IoT-lausnin sett upp og tengd við Microsoft Dynamics 365 Supply Chain Management á síðunni **Setja upp og tengja Azure-tilföng** sem leiðir þig í gegnum bæði ferlin. (Frekari upplýsingar er að finna í [Setja upp IoT-lausn í Azure](sdi-deploy-iot-solution-on-azure.md).) Einnig er hægt að skoða og breyta upplýsingum um tenginguna hvenær sem er í Supply Chain Management með því að fylgja þessum skrefum.

1. Farðu í **Kerfisstjórnun \> Uppsetning \> Sensor Data Intelligence \> Færibreytur Sensor Data Intelligence**.
1. Í flipanum **Tímaraðir**, í reitinn **Tengistrengur fyrir mælingageymslu Redis**, skal færa inn gildið **Aðaltengistrengur (StackExchange.Redis)** fyrir Azure IoT-lausnina sem á að tengjast við. Fyrir frekari upplýsingar um hvernig á að finna þetta gildi, sjá [Uppsetning IoT lausnar á Azure](sdi-deploy-iot-solution-on-azure.md).
1. Í flipann **Samþættingar**, í reitinn **Biðlarakenni Azure AD forrits**, skal færa inn gildið **Biðlarakenni** fyrir Azure IoT-lausnina sem á að tengjast við. Fyrir frekari upplýsingar um hvernig á að finna þetta gildi, sjá [Uppsetning IoT lausnar á Azure](sdi-deploy-iot-solution-on-azure.md).

## <a name="set-the-lifetime-of-alert-messages"></a>Stilla líftíma viðvörunarskilaboða

Í hvert sinn sem Gagnagreining skynjara greinir aðstæður sem krefjast athygli notenda sendir hún viðkomandi notanda tilkynningu. Til að koma í veg fyrir að þessar tilkynningar safnist upp í kerfinu ættir þú að stilla þær á að þær renni út eftir nokkra daga.

1. Farðu í **Kerfisstjórnun \> Uppsetning \> Sensor Data Intelligence \> Færibreytur Sensor Data Intelligence**.
1. Í flipann **Tilkynningar**, í reitinn **Tilkynningadagar sem eftir eru**, skal færa inn fjölda daga sem á að halda tilkynningu. Tilkynningunni verður eytt að tilteknum tíma liðnum.
