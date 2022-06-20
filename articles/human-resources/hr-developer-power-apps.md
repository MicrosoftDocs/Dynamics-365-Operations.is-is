---
title: Stækka Talent með Power Apps og Power Automate
description: Þessi grein lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Human Resources sem notar Microsoft Power Apps og Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5fe8ecd368bc63eed43c86053084ca67ef9beac6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859518"
---
# <a name="extend-with-power-apps-and-power-automate"></a>Stækka með Power Apps og Power Automate


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Þessi grein lýsir sumum dæmum um atburðarás stækkunarhæfni fyrir Microsoft Dynamics 365 Human Resources sem notar Microsoft Power Apps og Microsoft Power Automate. Hægt er að flytja lausnapakkann sem tengist hverju dæmi inn í Power Apps-umhverfið. Síðan er hægt að nota pakkana annaðhvort sem leiðarvísi eða sem upphafspunkta til að innleiða atburðarásir sem eiga við um fyrirtækið þitt.

> [!IMPORTANT]
> Ef þú vilt nota sniðmátin og öppin sem lýst er í þessari grein "eins og þau eru," vertu viss um að prófa þau til að ganga úr skugga um að þau nái yfir allar aðstæður sem eru sértækar fyrir útfærslu þína.

## <a name="prerequisites"></a>Forkröfur

- Til að flytja inn pakka verða notendur að hafa heimildina **Umhverfishönnuður**.
- Til að flytja forrit út eða inn verða notendur að hafa Power Apps Plan 2 leyfi eða Power Apps Plan 2 prufuleyfi.

## <a name="integration-with-microsoft-365-power-automate"></a>Samþætting við Microsoft 365, Power Automate

Forritið **Samþætting við Microsoft 365** er hægt að nota til að draga út upplýsingar um hóp fyrir innskráða notendur úr Microsoft 365. Í henni er vísað til starfsmanna í Human Resources til að draga út kennitegundir starfsmanna. Stjórnendur geta athugað lokadaga kennigerða starfsmanna. Þeir geta einnig sent tölvupóst áminningu ef kennitölu starfsmanns er að renna út. Power Automate samþættist við Power Apps til að senda þessa áminningu. Staðfesting verður send aftur til Power Apps frá Power Automate þegar áminningin er send. Auðkenningargerðir innihalda ökuskírteini, vegabréf og önnur ásættanleg skilríki.

Þú getur lengt þetta forrit fyrir aðrar aðstæður. Til dæmis er hægt að nota það til að sýna upplýsingar um frí hóps, viðburði dagatals og alla viðburði sem tengjast hópnum.

Til að hlaða niður forritnu **Samþætting við Microsoft 365, Power Automate** skal fara í [Samþætting við Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) í Microsoft Download Center.

## <a name="power-automate--sql-connect-and-execute"></a>Power Automate - SQL Connect og framkvæmd

Sniðmátið **Power Automate - SQL Connect og framkvæmd** tengist við Microsoft SQL Server og virkjar keyrslu á SQL-fyrirspurnum.

Þrátt fyrir að þetta sniðmát lesi og uppfærir SQL töflur, geturðu lengt það og notað það fyrir aðrar sviðsmyndir. Til dæmis er hægt að nota það til að fylla út millistigsvistunartöflu í Dataverse með skrám úr SQL-þjóni, og til að gera reglubundna samstillingu á millistigsvistunartöflu með því að nota stigvaxandi færslu úr SQL-þjóni.

Háþróaður fyrirspurn er samþætt með flæði til að gera gagnaflutning og stigvaxandi ýtingu möguleg.

Til að hlaða niður sniðmátinu **Power Automate - SQL Connect og framkvæmd** skal fara í [Power Automate - SQL Connect og framkvæmd](https://go.microsoft.com/fwlink/?linkid=2081789) í Microsoft Download Center.

## <a name="additional-resources"></a>Frekari upplýsingar

[Microsoft Power Platform](/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
