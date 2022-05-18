---
title: Human Resources birtist ekki í forritum Microsoft Dynamics 365
description: Þetta efnisatriði útskýrir hvað á að gera ef Microsoft Dynamics 365 Human Resources er ekki á meðal forrita Microsoft Dynamics 365.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a973b10a15846f7a27bff955deb2a961f45d9701
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687730"
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
