---
title: Virknigloppur á milli birgðavirðis/aldursgreiningaskýrslna og geymsluútgáfa þeirra
description: Virknigloppur á milli birgðavirðis/aldursgreiningaskýrslna og geymsluútgáfa þeirra
author: AndersGirke
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f74389648034bf036ce48ac84b3421a8a340f105
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686654"
---
# <a name="functional-gaps-between-inventory-valueaging-reports-and-their-storage-versions"></a>Virknigloppur á milli birgðavirðis/aldursgreiningaskýrslna og geymsluútgáfa þeirra

Eiginleikarnir [Skýrsla um aldursgreiningu birgða](/dynamics365/supply-chain/cost-management/inventory-aging-report-storage) og [Skýrsla um birgðavirði í geymslu](/dynamics365/supply-chain/cost-management/inventory-value-report-storage) gerir Supply Chain Management kleift að birta mikinn fjölda birgðafærslna. Í hverju tilviki fyrir eru niðurstöður skýrslugjafar fyrir leit og útflutning, ólíkt því sem gert er við útgáfur þessara skýrslna sem eru ekki til geymslu. Hins vegar er tiltekin virkni til staðar í útgáfum þessara skýrslna sem eru ekki til geymslu sem eru ekki til staðar í geymsluútgáfunum. Í eftirfarandi undirköflum er fjallað um mismuninn og boðið upp á hjáleið.

## <a name="storage-reports-dont-include-subtotals-even-if-they-are-enabled-in-the-report-layout"></a>Geymsluskýrslur innihalda ekki millisamtölur, jafnvel þótt þær séu virkar í skýrsluútlitinu

Millisamtölur geta valdið vandamálum þegar niðurstaðan er flutt út, sérstaklega ef notendur breyta færslustöðinni.

Til að skoða millisamtölur er hægt að flytja niðurstöðuna út í Microsoft Excel. Að öðrum kosti ef þú vilt athuga millisamtölur innan Supply Chain Management skaltu nota [Eiginleikastjórnun](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) til að virkja eiginleikana *Ný hnitanetsstjórnun* og *Hópar í hnitanetum* sem gefa upp mun sveigjanlegri leið til að sjá millisamtölu fyrir alla flokka eftir dálki. Nánari upplýsingar eru að finna í [Möguleikar hnitanets](/dynamics365/fin-ops-core/fin-ops/get-started/grid-capabilities).

## <a name="inventory-value-storage-report-doesnt-support-ledger-account-information"></a>Skýrsla um birgðavirði í geymslu styður ekki upplýsingar um fjárhagslykil

Hægt er að keyra prófjöfnuð til að fá stöðu birgðalykla og bera saman við **Skýrslu um birgðavirði í geymslu** .
