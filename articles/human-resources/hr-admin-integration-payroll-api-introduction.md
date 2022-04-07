---
title: Kynning á API launasamþættingar
description: Þetta efnisatriði lýsir API Dynamics 365 Human Resources launasamþættingar.
author: twheeloc
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3743561e3ea3c798c37d71d851eb6b197c8d1c41
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533827"
---
# <a name="payroll-integration-api-introduction"></a>Kynning á API launasamþættingar


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta skjal lýsir API Dynamics 365 Human Resources launasamþættingar. API virkjar einfaldaða heildarsamþættingu á milli Human Resources og launakerfa samstarfsaðila. Samþætta upplifunin hefst í Human Resources með upplýsingar um forstillingu starfsmanns, laun og frádrátt og framlag. Þegar starfsmaður er ráðinn og færðar er inn nauðsynleg forstilling og launaupplýsingar í Human Resources, sækir launakerfið þessar upplýsingar til að nota þegar unnið er úr launum. Allar uppfærslur sem gerðar eru á upplýsingum um starfsmann eða laun eru einnig sóttar til að nota í síðari launakeyrslum.

[![Flæði launasamþættingar.](media/hr-admin-integration-payroll-api-introduction-flow.png)](media/hr-admin-integration-payroll-api-introduction-flow-2.png#lightbox)

Til að virkja samþættinguna hefur Human Resources bætt við eftirfarandi þáttum:

- [Virkni til að merkja starfsmann sem tilbúinn til að greiða.](hr-compensation-payroll.md)
- API-samþætting sem opnar nýju virknina til að samþætta forrit.

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Þetta API er byggt á Microsoft Dataverse (áður Common Data Service). Öll RESTful-samþætting við þetta API er gert í gegnum Microsoft Dataverse vef-API sem notar OData. Þetta API er undirsafn Dataverse vef-API. Dataverse Vef-API skilgreinir einkenni á borð við auðkenningu, þjónustustigssamninga, runu, samvinnslustýringu og villumeðhöndlun.

Til að fá frekari almennar upplýsingar um Microsoft Dataverse vef-API skal sjá:

- [Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Nota Microsoft Dataverse vef-API](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse leiðbeiningar þróunaraðila](/powerapps/developer/data-platform)

Þessi fylgigögn innihalda nánari upplýsingar og leiðbeiningar þróunaraðila til að nota Dataverse vef API, þ.m.t. eftirfarandi efnisatriði:

- [Sannvotta fyrir Microsoft Dataverse með vef-API](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [Framkvæma aðgerðir með vef-API](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [Nota Postman með vef-API](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [Nota breytingarrakningu til að samstilla gögn við ytri kerfi](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Sýndartöflur fyrir Human Resources í Dataverse

Endastöðvar fyrir API-samþættingu launa nota verkvangsmöguleika sýndartöflunnnar fyrir Microsoft Dataverse. Sjálfgefið er að sýndartöflurnar og tengdu API-endastöðvarnar þeirra eru ekki uppsettar fyrir umhverfi Human Resources sem gerir fyrirtækjum kleift að ákveða hvaða OData-endastöðvar verða notaðar í umhverfinu. Til að nota API þarf að mynda sýndartöflur fyrir einingar Human Resources fyrir umhverfið.

Frekari upplýsingar um myndun sýndartaflna fyrir API er að finna í [Skilgreina Dataverse sýndartöflur](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Gagnalíkan

Eftirfarandi skýringarmynd sýnir vensl innan API. Nokkrar gerðir eru með ytri lykla fyrir aðrar fyrirliggjandi einingar í Human Resources sem ekki eru sýndar hér. Í þessu skjali eru upplýsingar um einingar sem eiga sérstaklega við samþættingaraðstæður launa. Hins vegar eru margar aðrar einingar í Dataverse vef-API fyrir Human Resources sem kunna einnig að skipta máli fyrir samþættingu þína. Vísað er í sumar þessara eininga í tengslum ytri lykla eða skoðunareiginleikum.

[![Gagnalíkan API-samþættingar launa.](media/hr-admin-payroll-api-data-model.png)](media/hr-admin-payroll-api-data-model.png#lightbox)

## <a name="payroll-employee-and-related-entities"></a>Starfsmaður á launaskrá og tengdar einingar

Einingar:

- [Starfsmaður á launaskrá](hr-admin-integration-payroll-api-payroll-employee.md)
- [Heimilisfang starfskrafts á launaskrá](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [Launafyrirkomulag fastra launa](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md)
- [Launafyrirkomulag breytilegra launa](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md)
- [Launastöðuvinnsla](hr-admin-integration-payroll-api-payroll-position-job.md)
- [Launastaða](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a>Sjá einnig

[Mynda og yfirfara launaaðila](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[Grunnstilla færibreytur Human Resources](hr-setup-parameters.md)<br>
[Grunnstilla samnýttar færibreytur Human Resources](hr-setup-shared-parameters.md)<br>
[Hvað er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Nota Microsoft Dataverse vef-API](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
