---
title: Vantar reitarstillingar þegar vörulíkanaflokkareru afritaðir á annan lögaðila
description: Reitarstillingar vantar þegar vörulíkanaflokkareru afritaðir á annan lögaðila
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 128caead04cf467c65a50bc6cd2f9e76e318f536b7eafa7972ffc1b5da5bceba
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738844"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Vantar reitarstillingar þegar vörulíkanaflokkareru afritaðir á annan lögaðila

KB númer: 4612800

## <a name="symptoms"></a>Einkenni

Þegar þú afritar vörulíkanahópa til annars lögaðila (fyrirtækis) með eininguna *Birgðareglur vörulíkanaflokks* vantar sumar reitastillingar (til dæmis birgðalíkanið og lýsingin) í nýja líkanahópinn í lögaðilann.

## <a name="resolution"></a>Upplausn

Til að búa til heildarafrit af vörulíkanaflokki á annan lögaðila verður einnig að velja bæði birgðareglur vörulíkanaflokks (`InventInventoryPolicyEntity`) og áætlunarreglur kostnaðarflæðis (`InventCostFlowAssumptionPolicyEntity`) sem eru tengdar vörulíkanaflokknum.
