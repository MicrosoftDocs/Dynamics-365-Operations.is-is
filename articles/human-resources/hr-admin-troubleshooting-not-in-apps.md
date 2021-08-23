---
title: Human Resources birtist ekki í forritum Microsoft Dynamics 365
description: Þessi grein útskýrir hvað á að gera ef viðskiptamaður sér ekki forritið Microsoft Dynamics 365 Human Resources á meðal forrita Microsoft Dynamics 365.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f90af26483cf82de57cbe8dd4237b39b281786804557319d5f6a7fc407027523
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782121"
---
# <a name="human-resources-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Human Resources birtist ekki í forritum Microsoft Dynamics 365

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Úthreyfing**

Viðskiptavinurinn sér ekki Dynamics 365 Human Resources meðal Microsoft Dynamics 365 forrita.

**Upplausn**

Bæta verður notanda við hlutverk umhverfishönnuðar fyrir umhverfið í Microsoft Power Apps.

1. Stjórnandi sem er með leyfi Power Apps Plan 2 verður að opna [Power Apps-stjórnandagátt](https://preview.admin.powerapps.com/).

2. Veljið **Umhverfi** og veljið rétta umhverfið fyrir Human Resources.

3. Á flipanum **Öryggi**, á flipanum **Umhverfishlutverk**, skal velja **Hönnuður umhverfis**.

    ![Flipi umhverfishlutverks.](media/environment-roles.png)

4. Á flipanum **Notendur** skal bæta við notanda eða fyrirtæki.

    ![Notandaflipi.](media/environment-maker.png)

5. Veldu **Vista**.

6. Notandi verður að skrá sig inn í [Microsoft Dynamics 365](https://home.dynamics.com/).

7. Veljið **Samstilling** til að uppfæra forrit notanda.

    ![Samstillingarhnappur.](media/get-more.png)

    Human Resources birtist á heimasíðunni þegar samstillingu lýkur.


[!INCLUDE[footer-include](../includes/footer-banner.md)]