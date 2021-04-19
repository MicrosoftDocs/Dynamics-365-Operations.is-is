---
title: Úrræðaleita Dynamics 365-greiðslutengil fyrir vandamál varðandi Adyen
description: Þetta efnisatriði veitir leiðsögn um úrræðaleit sem getur hjálpað til þegar vandamál koma upp varðandi Microsoft Dynamics 365-greiðslutengil fyrir Adyen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c779997d530d60f945bee19ee09bdabbff121fa6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801820"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a>Úrræðaleita Dynamics 365-greiðslutengil fyrir vandamál varðandi Adyen

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði veitir leiðsögn um úrræðaleit sem getur hjálpað til þegar vandamál koma upp varðandi Microsoft Dynamics 365-greiðslutengil fyrir Adyen.

## <a name="description"></a>lýsing

Vandamál kom upp farðandi greiðslutengil Dynamics 365 fyrir Adyen á eftirfarandi svæðum og þörf er á aðstoð frá Adyen-teyminu:

- Grunnstilling sölustaðar (POS), nútímasölustaðar (MPOS) símavers eða Dynamics 365 Commerce
- Tilvísunarnúmer Adyen-greiðsluþjónustuveitu (PSP) (til dæmis ef vakna spurningar um hafnanir, þ.m.t. hafnanir á handvirkum lyklainnslætti \[MKE\])
- Allt það sem virkar ekki í prófunarumhverfi eða virku umhverfi söluaðila

## <a name="resolution"></a>Upplausn

Notið eftirfarandi tölvupóstssniðmát til að hefja ferli notendaþjónustu hjá Adyen-teyminu. Til að flýta fyrir úrræðaleit skal ganga úr skugga um tölvupósturinn innihaldi allar nauðsynlegar upplýsingar.

| Svæði        | Virði |
|--------------|-------|
| Að           | `support@adyen.com` |
| Cc           | |
| Efnislína | Microsoft Dynamics Þjónustubeiðni  |
| Meginmál         | <p>Halló notendaþjónusta,</p><p>Vinsamlegast veitið aðstoð vegna eftirfarandi vandamáls:</p><ul><li>Lykill söluaðila</li><li>Umhverfi (prófun/framleiðsla)</li><li>Rás (sölustaður/símaver/rafræn viðskipti)</li><li>PSP-tilvísunarnúmer ef vandamálið tengdist ákveðinni færslu (hægt er að finna PSP-tilvísunarnúmerið á kvittuninni, á viðskiptavinasvæði Adyen, eða færsluvalmyndinni í afgreiðslukassanum.)</li><li>Skjámynd eða ljósmynd af villuboðinu ef það á við</li><li>Kladdar atvikaskoðunar (á .txt-sniði)</li><li>Lýsing á vandamálinu og skref úrræðaleitar sem búið er að reyna</li></ul> |

## <a name="additional-resources"></a>Frekari upplýsingar

[Samþykkja greiðslur með Adyen-tengli fyrir Dynamics 365 Commerce](https://www.adyen.com/partners/dynamics-365-commerce)

[Dynamics 365-greiðslutengill fyrir Adyen](../dev-itpro/adyen-connector.md)

[Setja upp Adyen-greiðslutengil fyrir Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
