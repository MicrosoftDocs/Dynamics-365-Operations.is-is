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
ms.openlocfilehash: 6f6fdfef0bc377418ed8a9c8830e74526a0b95eb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026604"
---
# <a name="missing-field-settings-when-item-model-groups-are-copied-to-another-legal-entity"></a>Vantar reitarstillingar þegar vörulíkanaflokkareru afritaðir á annan lögaðila

KB númer: 4612800

## <a name="symptoms"></a>Einkenni

Þegar þú afritar vörulíkanahópa til annars lögaðila (fyrirtækis) með eininguna *Birgðareglur vörulíkanaflokks* vantar sumar reitastillingar (til dæmis birgðalíkanið og lýsingin) í nýja líkanahópinn í lögaðilann.

## <a name="resolution"></a>Upplausn

Til að búa til heildarafrit af vörulíkanaflokki á annan lögaðila verður einnig að velja bæði birgðareglur vörulíkanaflokks (`InventInventoryPolicyEntity`) og áætlunarreglur kostnaðarflæðis (`InventCostFlowAssumptionPolicyEntity`) sem eru tengdar vörulíkanaflokknum.
