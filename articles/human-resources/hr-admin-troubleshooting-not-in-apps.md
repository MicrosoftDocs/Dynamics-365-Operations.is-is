---
title: Human Resources birtist ekki í forritum Microsoft Dynamics 365
description: Þetta efnisatriði útskýrir hvað á að gera ef Microsoft Dynamics 365 Human Resources er ekki á meðal forrita Microsoft Dynamics 365.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bdbe6c4065a8266fd30a3b093743ded91524f6a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069681"
---
# <a name="human-resources-app-doesnt-appear-in-microsoft-dynamics-365-apps"></a>Forritið Human Resources birtist ekki í forritum Microsoft Dynamics 365


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Gefa út**

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
